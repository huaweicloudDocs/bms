# 接口使用说明（OpenStack原生）<a name="bms_api_0701"></a>

-   网络相关服务API，请参考《[虚拟私有云API参考](https://support.huaweicloud.com/api-vpc/zh-cn_topic_0050065465.html)》。
-   专属分布式存储相关API，请参考《[专属分布式存储API参考](https://support.huaweicloud.com/api-dss/dss_02_0001.html)》。
-   使用OpenStack原生接口时，您需要使用ECS服务的终端节点（Endpoint），获取方式请参见[地区和终端节点](https://developer.huaweicloud.com/endpoint)。
-   文档中没有体现的OpenStack原生接口（例如：挂载云硬盘），请使用弹性云服务器对应的原生接口，参考《[弹性云服务器API参考](https://support.huaweicloud.com/api-ecs/zh-cn_topic_0124385014.html)》了解详细操作。
-   为了支持功能不断扩展，Nova API支持版本号区分。Nova中有两种形式的版本号：
    -   主版本号：具有独立的URL。
    -   微版本号：通过HTTP请求头X-OpenStack-Nova-API-Version来使用，从2.27版本开始支持新的微版本头：OpenStack-API-Version。


