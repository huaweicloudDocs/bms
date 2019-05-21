# API参考

-   [使用前必读](使用前必读.md)
-   [接口简介](接口简介.md)
-   [环境准备]
    -   [获取请求认证](获取请求认证.md)
    -   [获取项目ID](获取项目ID.md)

-   [接口调用方法]
    -   [REST API介绍](REST-API介绍.md)
    -   [示例](示例.md)

-   [API]
    -   [裸金属服务器接口使用说明](裸金属服务器接口使用说明.md)
    -   [裸金属服务器生命周期管理]
        -   [创建裸金属服务器](创建裸金属服务器.md)
        -   [查询裸金属服务器详情](查询裸金属服务器详情.md)

    -   [裸金属服务器状态管理]
        -   [修改裸金属服务器名称](修改裸金属服务器名称.md)

    -   [裸金属服务器云硬盘管理]
        -   [裸金属服务器挂载云硬盘](裸金属服务器挂载云硬盘.md)
        -   [裸金属服务器卸载云硬盘](裸金属服务器卸载云硬盘.md)

    -   [Job管理]
        -   [查询Job状态](查询Job状态.md)

    -   [裸金属服务器生命周期管理（OpenStack原生）]
        -   [查询裸金属服务器详情（OpenStack原生）](查询裸金属服务器详情（OpenStack原生）.md)
        -   [查询裸金属服务器列表（OpenStack原生）](查询裸金属服务器列表（OpenStack原生）.md)
        -   [查询裸金属服务器详情列表（OpenStack原生）](查询裸金属服务器详情列表（OpenStack原生）.md)

    -   [裸金属服务器状态管理（OpenStack原生）]
        -   [启动裸金属服务器（OpenStack原生）](启动裸金属服务器（OpenStack原生）.md)
        -   [重启裸金属服务器（OpenStack原生）](重启裸金属服务器（OpenStack原生）.md)
        -   [关闭裸金属服务器（OpenStack原生）](关闭裸金属服务器（OpenStack原生）.md)
        -   [查询裸金属服务器元数据（OpenStack原生）](查询裸金属服务器元数据（OpenStack原生）.md)
        -   [更新裸金属服务器元数据（OpenStack原生）](更新裸金属服务器元数据（OpenStack原生）.md)
        -   [修改裸金属服务器指定元数据（OpenStack原生）](修改裸金属服务器指定元数据（OpenStack原生）.md)
        -   [删除裸金属服务器指定元数据（OpenStack原生）](删除裸金属服务器指定元数据（OpenStack原生）.md)

    -   [裸金属服务器IP地址查询（OpenStack原生）]
        -   [查询裸金属服务器IP地址（OpenStack原生）](查询裸金属服务器IP地址（OpenStack原生）.md)
        -   [查询指定裸金属服务器IP地址（OpenStack原生）](查询指定裸金属服务器IP地址（OpenStack原生）.md)

    -   [裸金属服务器规格查询（OpenStack原生）]
        -   [查询裸金属服务器规格信息列表（OpenStack原生）](查询裸金属服务器规格信息列表（OpenStack原生）.md)
        -   [查询裸金属服务器规格详情（OpenStack原生）](查询裸金属服务器规格详情（OpenStack原生）.md)
        -   [查询裸金属服务器规格extra\_specs的详情（OpenStack原生）](查询裸金属服务器规格extra_specs的详情（OpenStack原生）.md)

    -   [裸金属服务器网卡管理（OpenStack原生）]
        -   [查询裸金属服务器网卡信息（OpenStack原生）](查询裸金属服务器网卡信息（OpenStack原生）.md)
        -   [查询指定裸金属服务器网卡信息（OpenStack原生）](查询指定裸金属服务器网卡信息（OpenStack原生）.md)

    -   [裸金属服务器云硬盘管理（OpenStack原生）]
        -   [查询裸金属服务器挂载云硬盘信息（OpenStack原生）](查询裸金属服务器挂载云硬盘信息（OpenStack原生）.md)
        -   [查询裸金属服务器挂载的单个云硬盘信息（OpenStack原生）](查询裸金属服务器挂载的单个云硬盘信息（OpenStack原生）.md)

    -   [裸金属服务器SSH密钥管理（OpenStack原生）]
        -   [查询SSH密钥列表（OpenStack原生）](查询SSH密钥列表（OpenStack原生）.md)
        -   [查询SSH密钥详情（OpenStack原生）](查询SSH密钥详情（OpenStack原生）.md)
        -   [创建和导入SSH密钥（OpenStack原生）](创建和导入SSH密钥（OpenStack原生）.md)
        -   [删除SSH密钥（OpenStack原生）](删除SSH密钥（OpenStack原生）.md)

    -   [裸金属服务器一维标签管理（OpenStack原生）]
        -   [查询裸金属服务器标签（OpenStack原生）](查询裸金属服务器标签（OpenStack原生）.md)
        -   [为裸金属服务器添加标签（OpenStack原生）](为裸金属服务器添加标签（OpenStack原生）.md)
        -   [删除裸金属服务器标签（OpenStack原生）](删除裸金属服务器标签（OpenStack原生）.md)
        -   [为裸金属服务器添加一个标签（OpenStack原生）](为裸金属服务器添加一个标签（OpenStack原生）.md)
        -   [查询裸金属服务器是否存在标签（OpenStack原生）](查询裸金属服务器是否存在标签（OpenStack原生）.md)
        -   [删除裸金属服务器的一个标签（OpenStack原生）](删除裸金属服务器的一个标签（OpenStack原生）.md)


-   [返回码]
    -   [通用返回值](通用返回值.md)
    -   [错误码](错误码.md)
    -   [提交任务类响应]
        -   [任务Id的响应](任务Id的响应.md)
        -   [订单Id的响应](订单Id的响应.md)

-   [附录]
    -   [网络相关API说明](网络相关API说明.md)
    -   [专属分布式存储相关API说明](专属分布式存储相关API说明.md)
    -   [API授权项列表]
        -   [API授权项说明](API授权项说明.md)
        -   [生命周期管理](生命周期管理.md)
        -   [状态管理](状态管理.md)
        -   [磁盘管理](磁盘管理.md)

