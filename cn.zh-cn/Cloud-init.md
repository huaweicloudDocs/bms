# Cloud-init<a name="bms_01_0008"></a>

Cloud-init是开源的云初始化程序，能够对新创建裸金属服务器中指定的自定义信息（主机名、密钥和用户数据等）进行初始化配置。

当前，除部分社区镜像（Community\_xxx形式）外，所有标准镜像（Standard\_xxx形式）和企业镜像（Enterprise\_xxx形式）均支持Cloud-init特性。

通过Cloud-init进行裸金属服务器的初始化配置，将对您使用裸金属服务器、镜像服务产生影响。

## 对镜像服务的影响<a name="section528893335315"></a>

为了保证使用私有镜像新创建的裸金属服务器可以自定义配置，您需要在创建私有镜像时安装Cloud-init/Cloudbase-init。

-   如果是Windows操作系统，需下载并安装Cloudbase-init。
-   如果是Linux操作系统，需下载并安装Cloud-init。

在镜像上安装Cloud-init/Cloudbase-init后，即可在创建裸金属服务器时，按照用户的需要自动设置裸金属服务器的初始属性。更多关于安装的信息，请参见《裸金属服务器私有镜像制作指南》。

## 对裸金属服务器的影响<a name="section951214112013"></a>

-   在创建裸金属服务器时，如果选择的镜像支持Cloud-init特性，此时，您可以通过系统提供的“用户数据注入”功能，注入初始化自定义信息（例如为裸金属服务器设置登录密码），完成裸金属服务器的初始化配置。具体操作请参见[用户数据注入](https://support.huaweicloud.com/usermanual-bms/bms_01_0021.html)。
-   对于运行中的裸金属服务器，支持Cloud-init特性后，用户可以通过查询、使用元数据服务，对正在运行的裸金属服务器进行配置和管理。更多信息，请参见[元数据](https://support.huaweicloud.com/usermanual-bms/bms_01_0040.html)。

## 使用须知<a name="section14228108367"></a>

-   使用Cloud-init特性时，需开启裸金属服务器所在VPC中子网的DHCP。
-   使用Cloud-init特性时，安全组出方向规则需满足如下要求，才能正常访问元数据服务：

    -   协议：TCP
    -   端口范围：80
    -   远端地址：169.254.0.0/16

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果您使用的是默认安全组出方向规则，则已经包括了如上要求，可以正常访问元数据服务。默认安全组出方向规则为：  
    >-   协议：ANY  
    >-   端口范围：ANY  
    >-   远端地址：0.0.0.0/16  


