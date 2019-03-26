# API授权项说明<a name="ZH-CN_TOPIC_0133195982"></a>

-   在裸金属服务中，OpenStack原生API授权项和授权项作用域与弹性云服务器的一致，具体请参考《[弹性云服务器API参考](https://support.huaweicloud.com/api-ecs/zh-cn_topic_0020805967.html)》附录中“API授权项列表”章节。
-   在IAM中自定义BMS的用户策略时，需要给BMS的用户策略中加入ecs:\*:get和ecs:\*:list两个权限，否则可能会因为权限不足导致部分云服务页面使用异常。
-   高速网络和自定义网络当前不支持企业项目，若企业项目的子账号需要使用这两个功能，需要在IAM中给子账号授予vpc:ports:get权限，否则在裸金属服务器中有高速网卡的情况下，弹性公网IP和安全组会显示异常。

