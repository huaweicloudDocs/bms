# SUSE Linux Enterprise Server 12系列<a name="bms_01_0044"></a>

下面以SUSE Linux Enterprise Server 12 SP1 \(x86\_64\)操作系统为例，举例介绍裸金属服务器的自定义VLAN网络配置方法：

1.  以“root“用户，使用密钥或密码登录裸金属服务器。
2.  <a name="li1143133511162"></a>进入裸金属服务器的命令行界面，查询网卡信息。

    **ip link**

    返回信息示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default 
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state DOWN mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state DOWN mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8e brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    7: bond0.3133@bond0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:57:87:6e brd ff:ff:ff:ff:ff:ff
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，“eth0”和“eth1”为承载VPC网络的网络设备，“eth2”和“eth3”为承载自定义VLAN网络的网络设备。  

3.  设置udev规则。

    执行以下命令创建“80-persistent-net.rules“文件。

    **cp /etc/udev/rules.d/70-persistent-net.rules /etc/udev/rules.d/80-persistent-net.rules**

    将[2](#li1143133511162)中查询到的，且“80-persistent-net.rules“中未体现的网卡MAC地址和名称，写入该文件中，使得裸金属服务器重启复位后，网卡名称和顺序不会发生改变。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >网卡的MAC地址和名称中的字母，请使用小写字母。  

    **vim /etc/udev/rules.d/80-persistent-net.rules**

    修改后的示例如下：

    ```
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="38:4c:4f:29:0b:e0", NAME="eth0"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="38:4c:4f:29:0b:e1", NAME="eth1"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="38:4c:4f:89:55:8d", NAME="eth2"
    SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="38:4c:4f:89:55:8e", NAME="eth3"
    ```

    修改完成后，保存并退出。

4.  查询网卡的IP信息。

    **ifconfig**

    返回信息示例如下，其中的“bond0“和“bond0.313“为申请裸金属服务器时自动分配的网卡平面IP地址。

    ```
    bond0     Link encap:Ethernet  HWaddr FA:16:3E:3D:1C:E0  
              inet addr:10.0.1.2  Bcast:10.0.1.255  Mask:255.255.255.0
              inet6 addr: fe80::f816:3eff:fe3d:1ce0/64 Scope:Link
              UP BROADCAST RUNNING MASTER MULTICAST  MTU:8888  Metric:1
              RX packets:852 errors:0 dropped:160 overruns:0 frame:0
              TX packets:1121 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:0 
              RX bytes:125429 (122.4 Kb)  TX bytes:107221 (104.7 Kb)
    
    bond0.313 Link encap:Ethernet  HWaddr FA:16:3E:57:87:6E  
              inet addr:10.0.3.2  Bcast:10.0.3.255  Mask:255.255.255.0
              inet6 addr: fe80::f816:3eff:fe57:876e/64 Scope:Link
              UP BROADCAST RUNNING MULTICAST  MTU:8888  Metric:1
              RX packets:169 errors:0 dropped:0 overruns:0 frame:0
              TX packets:13 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:0 
              RX bytes:8684 (8.4 Kb)  TX bytes:1696 (1.6 Kb)
    
    eth0      Link encap:Ethernet  HWaddr FA:16:3E:3D:1C:E0  
              UP BROADCAST RUNNING SLAVE MULTICAST  MTU:8888  Metric:1
              RX packets:428 errors:0 dropped:10 overruns:0 frame:0
              TX packets:547 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:1000 
              RX bytes:64670 (63.1 Kb)  TX bytes:50132 (48.9 Kb)
    
    eth1      Link encap:Ethernet  HWaddr FA:16:3E:3D:1C:E0  
              UP BROADCAST RUNNING SLAVE MULTICAST  MTU:8888  Metric:1
              RX packets:424 errors:0 dropped:7 overruns:0 frame:0
              TX packets:574 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:1000 
              RX bytes:60759 (59.3 Kb)  TX bytes:57089 (55.7 Kb)
    
    lo        Link encap:Local Loopback  
              inet addr:127.0.0.1  Mask:255.0.0.0
              inet6 addr: ::1/128 Scope:Host
              UP LOOPBACK RUNNING  MTU:65536  Metric:1
              RX packets:8 errors:0 dropped:0 overruns:0 frame:0
              TX packets:8 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:0 
              RX bytes:520 (520.0 b)  TX bytes:520 (520.0 b)
    ```

5.  查询组成bond的网卡的名称。

    已组成bond且在使用中的网卡，不能用于内部通信平面，因此需要查询相应的网卡名称。

    **cd /etc/sysconfig/network**

    **vi ifcfg-**_bond0_

    返回信息示例如下，可见“bond0“由“eth0“和“eth1“组成。

    ```
    BONDING_MASTER=yes
    TYPE=Bond
    STARTMODE=auto
    BONDING_MODULE_OPTS="mode=4 xmit_hash_policy=layer3+4 miimon=100"
    NM_CONTROLLED=no
    BOOTPROTO=dhcp
    DEVICE=bond0
    USERCONTRL=no
    LLADDR=fa:16:3e:3d:1c:e0
    BONDING_SLAVE1=eth1
    BONDING_SLAVE0=eth0
    ```

    查询完成后，退出。

6.  查询所有网卡的状态。

    **ip link**

    返回信息示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default 
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state DOWN mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state DOWN mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8e brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    7: bond0.3133@bond0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:57:87:6e brd ff:ff:ff:ff:ff:ff
    ```

7.  将所有状态为“qdisc mq state DOWN“的网卡，设置为“qdisc mq state UP“，示例中为“eth2“和“eth3“。

    **ip link set** _eth2_ **up**

    **ip link set** _eth3_ **up**

8.  <a name="li345243551618"></a>重新查询网卡的状态。

    **ip link**

    返回信息示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default 
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP mode DEFAULT group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP mode DEFAULT group default qlen 1000
        link/ether 38:4c:4f:89:55:8e brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    7: bond0.3133@bond0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default 
        link/ether fa:16:3e:57:87:6e brd ff:ff:ff:ff:ff:ff
    ```

9.  查看[8](#li345243551618)中对应的网卡的状态，获取状态为“qdisc mq state UP“的网卡名称。

    只有状态为“qdisc mq state UP“且未被使用过的网卡，才能组成bond，示例中为“eth2“和“eth3“。

    “eth2“的LLADR为“38:4c:4f:89:55:8d“，“eth3“的LLADR为“38:4c:4f:89:55:8e“。

10. 创建“eth2“和“eth3“网卡的配置文件。

    可通过复制已有网卡配置文件的方式快速创建。

    **cp** _ifcfg-eth0 ifcfg-eth2_

    **cp** _ifcfg-eth__1 ifcfg-eth3_

11. 修改“eth2“和“eth3“网卡的配置文件。

    **vi** _ifcfg-eth2_

    **vi** _ifcfg-eth3_

    “eth2“网卡配置文件的修改示例如下。

    其中，参数参数“MTU“配置为“8888“,，“BOOTPROTO“需要配置为“STATIC“，参数“DEVICE“、“LLADDR“根据实际需要填写。

    ```
    STARTMODE=auto
    MTU=8888
    NM_CONTROLLED=no
    BOOTPROTO=STATIC
    DEVICE=eth2
    USERCONTRL=no
    LLADDR=38:4c:4f:89:55:8d
    TYPE=Ethernet
    ```

    “eth3“网卡配置文件的修改示例如下：

    ```
    STARTMODE=auto
    MTU=8888
    NM_CONTROLLED=no
    BOOTPROTO=STATIC
    DEVICE=eth3
    USERCONTRL=no
    LLADDR=38:4c:4f:89:55:8e
    TYPE=Ethernet
    ```

    修改完成后，保存并退出。

12. 将“eth2“和“eth3“组bond，假设为“bond1“。

    创建ifcfg-bond1文件并修改配置。

    **cp** _ifcfg-bond0 ifcfg-bond1_

    **vi** _ifcfg-bond1_

    “bond1“网卡配置文件的修改示例如下。

    其中，参数“MTU“配置为“8888“，“BONDING\_MODULE\_OPTS“配置为“mode=1 miimon=100“，“BOOTPROTO“需要配置为“STATIC“，“DEVICE“、“BONDING\_SLAVE1“、“BONDING\_SLAVE0“、“IPADDR“、“NETMASK“、“NETWORK“根据实际需要填写，“LLADDR“配置为参数“BONDING\_SLAVE1“对应网卡的LLADDR。

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
    LLADDR=38:4c:4f:89:55:8d
    BONDING_SLAVE1=eth2
    BONDING_SLAVE0=eth3
    IPADDR=10.0.2.2
    NETMASK=255.255.255.0
    NETWORK=10.0.2.0
    ```

    修改完成后，保存并退出。

13. 使配置文件生效。
    1.  创建临时目录，并将网络配置文件复制到该目录下。

        **mkdir /opt**_/tmp/_

        **mkdir /opt/tmp/**_xml_

        **cp /etc/sysconfig/network/ifcfg\* /opt/tmp/**

        **cp /etc/sysconfig/network/config /opt/tmp/**

        **cp /etc/sysconfig/network/dhcp /opt/tmp/**

    2.  停止待组成bond1的网卡。

        **ip link set** _eth2_ **down**

        **ip link set** _eth3_ **down**

    3.  将网卡配置文件转换成操作系统可辨识的配置文件。

        **/usr/sbin/wicked --log-target=stderr --log-level=debug3 --debug all convert --output /opt/tmp/xml /opt/tmp/**

    4.  重新启用待组成bond1的网卡。

        **ip link set** _eth2_ **up**

        **/usr/sbin/wicked --log-target=stderr --log-level=debug3 --debug all ifup --ifconfig /opt/tmp/xml/**_eth2_**.xml** _eth2_

        **ip link set** _eth3_ **up**

        **/usr/sbin/wicked --log-target=stderr --log-level=debug3 --debug all ifup --ifconfig /opt/tmp/xml/**_eth3_**.xml** _eth3_

        **/usr/sbin/wicked --log-target=stderr --log-level=debug3 --debug all ifup --ifconfig /opt/tmp/xml/bond1.xml** _bond1_


14. 重新查询IP地址信息，可查看到IP地址已分配。

    **ip addr show**

    示例如下：

    ```
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default 
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
        inet 127.0.0.1/8 scope host lo
           valid_lft forever preferred_lft forever
        inet6 ::1/128 scope host 
           valid_lft forever preferred_lft forever
    2: eth0: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    3: eth1: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond0 state UP group default qlen 1000
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
    4: eth2: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond1 state UP group default qlen 1000
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
    5: eth3: <BROADCAST,MULTICAST,SLAVE,UP,LOWER_UP> mtu 8888 qdisc mq master bond1 state UP group default qlen 1000
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
    6: bond0: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP group default 
        link/ether fa:16:3e:3d:1c:e0 brd ff:ff:ff:ff:ff:ff
        inet 10.0.1.2/24 brd 10.0.1.255 scope global bond0
           valid_lft forever preferred_lft forever
        inet6 fe80::f816:3eff:fe3d:1ce0/64 scope link 
           valid_lft forever preferred_lft forever
    7: bond0.3133@bond0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP group default 
        link/ether fa:16:3e:57:87:6e brd ff:ff:ff:ff:ff:ff
        inet 10.0.3.2/24 brd 10.0.2.255 scope global bond0.3133
           valid_lft forever preferred_lft forever
        inet6 fe80::f816:3eff:fe57:876e/64 scope link 
           valid_lft forever preferred_lft forever
    8: bond1: <BROADCAST,MULTICAST,MASTER,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP group default 
        link/ether 38:4c:4f:89:55:8d brd ff:ff:ff:ff:ff:ff
        inet 10.0.2.2/24 brd 10.0.2.255 scope global bond1
           valid_lft forever preferred_lft forever
        inet6 fe80::3a4c:4fff:fe29:b36/64 scope link 
           valid_lft forever preferred_lft forever
    ```

15. 删除创建的临时目录。

    **cd /opt**

    **rm -rf tmp/**

16. 参考上述步骤，完成其他裸金属服务器上的配置。

