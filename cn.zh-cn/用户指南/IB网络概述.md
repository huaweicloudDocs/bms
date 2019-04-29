# IB网络概述<a name="bms_01_0079"></a>

## 介绍<a name="section349975925113"></a>

IB网络因其低延迟、高带宽的网络特性被用于很多高性能计算（High Performance Computing，HPC）项目，IB网络采用了100G Mellanox IB网卡，通过专用IB交换机和控制器软件UFM实现网络通信和管理。IB网络通过Partition Key实现网络隔离，不同租户的IB网络可通过不同的Partition Key来隔离，类似于以太网的VLAN。在BMS场景，IB网络支持RDMA和IPoIB通信方式。

裸金属服务器IB网络的发放是通过在创建BMS时选择支持IB网络的flavor实现的，即可动态创建IB网络。IB网络发放完成后，即可在裸金属服务器上通过RDMA方式实现高速通信。在IPoIB通信模式下，需要在IB网口上配置IP地址，有静态配置和DHCP动态分配两种方式。静态配置举例如下：

```
#/etc/sysconfig/network/ifcfg-ib0
DEVICE=ib0
TYPE=InfiniBand
ONBOOT=yes
HWADDR=80:00:00:4c:fe:80:00:00:00:00:00:00:f4:52:14:03:00:7b:cb:a1
BOOTPROTO=none
IPADDR=172.31.0.254
PREFIX=24
NETWORK=172.31.0.0
BROADCAST=172.31.0.255
IPV4_FAILURE_FATAL=yes
IPV6INIT=no
MTU=65520
CONNECTED_MODE=yes
NAME=ib0
```

>![](public_sys-resources/icon-note.gif) **说明：**   
>了解更多关于IPoIB通信方式的信息，请参考[https://www.kernel.org/doc/Documentation/infiniband/ipoib.txt](https://www.kernel.org/doc/Documentation/infiniband/ipoib.txt)。  

## 查看方式<a name="section10294132575216"></a>

IB网络是通过裸金属服务器的规格呈现给用户的，如[图1](#fig12134264236)所示。用户需要管理整个系统的VLAN/IP配置和规划。

**图 1**  裸金属服务器扩展配置<a name="fig12134264236"></a>  
![](figures/裸金属服务器扩展配置.png "裸金属服务器扩展配置")

