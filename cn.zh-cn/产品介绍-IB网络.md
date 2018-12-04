# IB网络<a name="bms_01_0056"></a>

IB网络因其低延迟、高带宽的网络特性被用于很多高性能计算（High Performance Computing，HPC）项目，IB网络采用了100G Mellanox IB网卡，通过专用IB交换机和控制器软件UFM实现网络通信和管理。IB网络通过Partition Key实现网络隔离，不同租户的IB网络可通过不同的Partition Key来隔离，类似于以太网的vlan（如[图1](#fig187941511154518)所示）。

**图 1**  IB网络隔离方式<a name="fig187941511154518"></a>  
![](figures/IB网络隔离方式.png "IB网络隔离方式")

>![](public_sys-resources/icon-note.gif) **说明：**   
>UFM（Unified Fabric Manager）是IB网络上IB交换机控制器，基于OpenSM软件，提供北向服务接口。UFM采用主备部署方式。  

