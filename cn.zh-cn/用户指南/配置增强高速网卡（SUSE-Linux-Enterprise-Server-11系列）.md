# 配置增强高速网卡（SUSE Linux Enterprise Server 11系列）<a name="bms_01_0072"></a>

下面以SUSE Linux Enterprise Server 11 SP4操作系统为例，举例介绍裸金属服务器增强高速网卡的配置方法。

## 增加网卡<a name="section9801122916212"></a>

1.  以“root”用户，使用密钥或密码登录裸金属服务器。
2.  <a name="li14997248288"></a>进入裸金属服务器的命令行界面，查询网卡信息。

    **ip** **link**

    返回信息示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN mode DEFAULT group default qlen 1000
        link/ether 40:7d:0f:52:e3:a5 brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN mode DEFAULT group default qlen 1000
        link/ether 40:7d:0f:52:e3:a6 brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，“eth0”和“eth1”为承载VPC网络的网络设备，“eth2”和“eth3”为承载自定义VLAN网络的网络设备。  

3.  设置udev规则。

    执行以下命令创建“80-persistent-net.rules”文件。

    **cp** **/etc/udev/rules.d/70-persistent-net.rules** **/etc/udev/rules.d/80-persistent-net.rules**

    将[2](#li14997248288)中查询到的，且“80-persistent-net.rules”中未体现的网卡MAC地址和名称，写入该文件中，使得裸金属服务器重启复位后，网卡名称和顺序不会发生改变。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >网卡的MAC地址和名称中的字母，请使用小写字母。  

    **vim** **/etc/udev/rules.d/80-persistent-net.rules**

    修改后的示例如下：

    ```
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="f4:4c:7f:5d:b7:2a", NAME="eth0"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="f4:4c:7f:5d:b7:2b", NAME="eth1"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="40:7d:0f:52:e3:a5", NAME="eth2"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="40:7d:0f:52:e3:a6", NAME="eth3"
    ```

4.  创建“eth2”和“eth3”网卡的配置文件。

    可通过复制已有网卡配置文件的方式快速创建。

    **cd** **/etc/sysconfig/network**

    **cp** **ifcfg-eth0** **ifcfg-eth2**

    **cp** **ifcfg-eth1** **ifcfg-eth3**

    修改“eth2”和“eth3”网卡的配置文件。

    **vi** **ifcfg-eth2**

    “eth2”网卡配置文件的修改示例如下：

    ```
    STARTMODE=auto
    MTU=8888
    NM_CONTROLLED=no
    BOOTPROTO=STATIC
    DEVICE=eth2
    USERCONTRL=no
    LLADDR=40:7d:0f:52:e3:a5
    TYPE=Ethernet 
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，参数参数“MTU”配置为“8888”,“BOOTPROTO”需要配置为“STATIC”，参数“DEVICE”、“LLADDR”根据实际需要填写。  

    **vi** **ifcfg-eth3**

    “eth3”网卡配置文件的修改示例如下：

    ```
    STARTMODE=auto
    MTU=8888
    NM_CONTROLLED=no
    BOOTPROTO=STATIC
    DEVICE=eth3
    USERCONTRL=no
    LLADDR=40:7d:0f:52:e3:a6
    TYPE=Ethernet
    ```

    修改完成后，保存并退出。

5.  将“eth2”和“eth3”组bond，假设为“bond1”。

    创建ifcfg-bond1文件并修改配置：

    **cp** **ifcfg-bond0** **ifcfg-bond1**

    **vi** **ifcfg-bond1**

    “bond1”网卡配置文件的修改示例如下：

    ```
    BONDING_MASTER=yes
    TYPE=Bond
    MTU=8888
    STARTMODE=auto
    BONDING_MODULE_OPTS="mode=1 miimon=100"
    NM_CONTROLLED=no
    BOOTPROTO=STATIC
    DEVICE=bond1
    USERCONTRL=no
    LLADDR=40:7d:0f:52:e3:a5
    BONDING_SLAVE1=eth2
    BONDING_SLAVE0=eth3
    IPADDR=10.10.10.104
    NETMASK=255.255.255.0
    NETWORK=10.10.10.0
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，参数“MTU”配置为“8888”，“BONDING\_MODULE\_OPTS”配置为“mode=1 miimon=100”，“BOOTPROTO”需要配置为“STATIC”，“DEVICE”、“BONDING\_SLAVE1”、“BONDING\_SLAVE0”、“IPADDR”、“NETMASK”、“NETWORK”根据实际需要填写，“LLADDR”配置为参数“BONDING\_SLAVE1”对应网卡的LLADDR。  

    修改完成后，保存并退出。

6.  执行以下命令，启动新增的bond1网卡。

    **ifup** **bond1**

7.  查询IP地址信息，可查看到IP地址已分配。

    **ip** **addr** **show**

    示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
        inet 127.0.0.1/8 scope host lo
           valid_lft forever preferred_lft forever
        inet6 ::1/128 scope host 
           valid_lft forever preferred_lft forever
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 1500 qdisc mq master bond1 state UP group default qlen 1000
        link/ether 40:7d:0f:52:e3:a5 brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 1500 qdisc mq master bond1 state UP group default qlen 1000
        link/ether 40:7d:0f:52:e3:a5 brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP group default qlen 1000
        link/ether fa:16:00:57:90:c9 brd ff:ff:ff:ff:ff:ff
        inet 172.16.2.44/24 brd 172.16.2.255 scope global bond0
           valid_lft forever preferred_lft forever
        inet6 fe80::f816:ff:fe57:90c9/64 scope link 
           valid_lft forever preferred_lft forever
    7: bond1: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
        link/ether 40:7d:0f:52:e3:a5 brd ff:ff:ff:ff:ff:ff
        inet 10.10.10.104/24 brd 10.10.10.255 scope global bond1
           valid_lft forever preferred_lft forever
        inet6 fe80::427d:fff:fe52:e3a5/64 scope link 
           valid_lft forever preferred_lft forever
    ```

8.  参考上述步骤，完成其他裸金属服务器上的配置。

## 删除网卡<a name="section68171429202111"></a>

1.  获取待删除增强高速网卡的bond网卡地址。
2.  以“root”用户，使用密钥或密码登录裸金属服务器。
3.  找到bond网络设备，然后执行命令关闭并删除网络设备。

    **ifdown** **bond1**

4.  执行以下命令，删除网络配置文件“/etc/sysconfig/network-scripts/ifcfg-eth2”、“/etc/sysconfig/network-scripts/ifcfg-eth3”和“/etc/sysconfig/network-scripts/ifcfg-bond1”。

    **rm** **-f** **/etc/sysconfig/network-scripts/ifcfg-eth2**

    **rm** **-f** **/etc/sysconfig/network-scripts/ifcfg-eth3**

    **rm** **/etc/sysconfig/network/ifcfg-bond1**


