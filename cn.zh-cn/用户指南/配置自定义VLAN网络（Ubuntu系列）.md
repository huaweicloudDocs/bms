# 配置自定义VLAN网络（Ubuntu系列）<a name="bms_01_0047"></a>

下面以Ubuntu 16.04 LTS \(Xenial Xerus x86\_64\)操作系统为例，举例介绍裸金属服务器的自定义VLAN网络配置方法：

>![](public_sys-resources/icon-note.gif) **说明：**   
>Ubuntu系列其他操作系统的配置方法与Ubuntu 16.04 LTS \(Xenial Xerus x86\_64\)类似。  

1.  以“root”用户，使用密钥或密码登录裸金属服务器。
2.  <a name="li0616194735713"></a>进入裸金属服务器的命令行界面，查询网卡信息。

    **ip link**

    返回信息示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:1c:35:37 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:1c:35:37 brd ff:ff:ff:ff:ff:ff
    4: enp129s0f0: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN mode DEFAULT group default qlen 1000
        link/ether f4:4c:7f:3f:da:07 brd ff:ff:ff:ff:ff:ff
    5: enp129s0f1: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN mode DEFAULT group default qlen 1000
        link/ether f4:4c:7f:3f:da:08 brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:1c:35:37 brd ff:ff:ff:ff:ff:ff
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，“eth0”和“eth1”为承载VPC网络的网络设备，“enp129s0f0”和“enp129s0f1”为承载自定义VLAN网络的网络设备。下面步骤将使用“enp129s0f0”和“enp129s0f1”配置自定义VLAN网络。  

3.  执行以下命令，查看“/etc/udev/rules.d/”目录下是否有“80-persistent-net.rules”配置文件。

    **ll /etc/udev/rules.d/ | grep 80-persistent-net.rules**

    -   如果存在“80-persistent-net.rules”，且该配置文件中已存在[2](#li0616194735713)中查询到的除“bond0”和“lo”以外的其它所有网卡和对应的MAC地址，请执行[6](#li283725272415)。
    -   否则，继续执行[4](#li116366367312)。

4.  <a name="li116366367312"></a>执行以下命令，将“/etc/udev/rules.d/70-persistent-net.rules”文件拷贝一份（文件名为“/etc/udev/rules.d/80-persistent-net.rules”）。

    **cp -p /etc/udev/rules.d/70-persistent-net.rules /etc/udev/rules.d/80-persistent-net.rules**

5.  设置udev规则。

    将[2](#li0616194735713)中查询到的除“lo”、“eth0”、“eth1”和“bond0”以外的网卡和MAC对应关系添加到“/etc/udev/rules.d/80-persistent-net.rules”文件中，使得裸金属服务器重启复位后，网卡名称和顺序不会发生改变。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >网卡的MAC地址和名称中的字母，请使用小写字母。  

    **vim /etc/udev/rules.d/80-persistent-net.rules**

    修改后的示例如下：

    ```
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="e8:4d:d0:c8:99:5b", NAME="eth0"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="e8:4d:d0:c8:99:5c", NAME="eth1"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="f4:4c:7f:3f:da:07", NAME="enp129s0f0"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="f4:4c:7f:3f:da:08", NAME="enp129s0f1"
    ```

    修改完成后，按“Esc”，输入**:wq**保存并退出。

6.  <a name="li283725272415"></a>执行以下命令，将网卡配置文件“/etc/network/interfaces.d/50-cloud-init.cfg”拷贝为“/etc/network/interfaces.d/60-cloud-init.cfg”。

    **cp -p /etc/network/interfaces.d/50-cloud-init.cfg /etc/network/interfaces.d/60-cloud-init.cfg**

7.  执行以下命令，编辑“/etc/network/interfaces.d/60-cloud-init.cfg”，配置“enp129s0f0”设备和“enp129s0f1”设备的网络配置文件“/etc/network/interfaces.d/60-cloud-init.cfg”。

    **vim /etc/network/interfaces.d/60-cloud-init.cfg**

    按如下格式编辑：

    ```
    auto enp129s0f0
    iface enp129s0f0 inet manual
    bond_mode 1
    bond-master bond1
    bond_miimon 100
    mtu 8888
    auto enp129s0f1
    iface enp129s0f1 inet manual
    bond_mode 1
    bond-master bond1
    bond_miimon 100
    mtu 8888
    auto bond1
    iface bond1 inet static
    bond_miimon 100
    bond-slaves none
    bond_mode 1
    address 10.10.10.3
    netmask 255.255.255.0
    hwaddress f4:4c:7f:3f:da:07
    mtu 8888
    ```

    其中，

    -   “enp129s0f0”和“enp129s0f1”为承载自定义VLAN网络配置的网卡名称。
    -   “hwaddress”为“enp129s0f0”设备对应的MAC地址。
    -   “address”的取值为给自定义VLAN网络“bond1”配置的IP（给自定义VLAN网络规划的IP地址在没有与VPC网段冲突的情况下可任意规划，需要通过自定义VLAN网络通信的裸金属服务器须将自定义VLAN网络配置在同一个网段）。
    -   “netmask”的取值为给自定义VLAN网络“bond1”配置的IP的掩码。

    各个设备的其他参数可参考如上信息进行配置，如“mtu”配置为“8888”，“bond\_miimon”配置为“100”，“bond\_mode”配置为“1”等。

    修改完成后，按“Esc”，输入**:wq**保存并退出。

8.  执行以下命令，重启网络。

    **ifup** _enp129s0f0_

    **ifup** _enp129s0f1_

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，“enp129s0f0”和“enp129s0f1”分别为承载自定义VLAN网络的网卡。  

9.  执行以下命令，查看网卡设备的状态和“bond1”配置文件是否生效。

    **ip link**

    **图 1**  ip link命令示例<a name="fig1087414331534"></a>  
    ![](figures/ip-link命令示例-8.png "ip-link命令示例-8")

    **ifconfig**

    **图 2**  ifconfig命令示例<a name="fig1843371419410"></a>  
    ![](figures/ifconfig命令示例-9.png "ifconfig命令示例-9")

10. 参见上述步骤，完成其他裸金属服务器的配置。
11. 待其他裸金属服务器配置完成后，互相ping对端自定义VLAN网络配置的同网段IP，检查是否可以ping通。

    **图 3**  网络连通性验证<a name="fig473120814515"></a>  
    ![](figures/网络连通性验证-10.png "网络连通性验证-10")


