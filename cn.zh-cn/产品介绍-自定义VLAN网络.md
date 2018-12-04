# 自定义VLAN网络<a name="bms_01_0055"></a>

未被系统默认使用的以太网卡（10GE，在裸金属服务器规格中定义）可用于自定义VLAN网络，物理上采用QinQ技术实现用户的网络隔离，提供额外的物理平面和网络带宽。用户能够自由划分所需的VLAN子网来分隔流量，适用于SAP HANA、VMware等场景。自定义VLAN网络的网卡是成对出现的，用户可以通过配置bond实现高可用。自定义VLAN网络当前不支持跨AZ互通。

>![](public_sys-resources/icon-note.gif) **说明：**   
>QinQ：一种基于802.1Q封装的二层隧道协议，它将用户私网VLAN TAG封装在公网VLAN TAG中，报文带着两层TAG穿越服务商的骨干网络，从而为用户提供二层VPN隧道。  

