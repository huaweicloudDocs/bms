# BMS自定义策略<a name="ZH-CN_TOPIC_0170005209"></a>

如果系统预置的BMS权限不满足您的授权要求，可以创建自定义策略。自定义策略中可以添加的授权项（Action）请参考：[策略及授权项说明](https://support.huaweicloud.com/api-bms/zh-cn_topic_0169929480.html)。

目前华为云支持以下两种方式创建自定义策略：

-   可视化视图创建自定义策略：无需了解策略语法，按可视化视图导航栏选择云服务、操作、资源、条件等策略内容，可自动生成策略。
-   JSON视图创建自定义策略：可以在选择策略模板后，根据具体需求编辑策略内容；也可以直接在编辑框内编写JSON格式的策略内容。

具体创建步骤请参见：[创建自定义策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html)。本章为您介绍常用的BMS自定义策略样例。

## BMS自定义策略样例<a name="section1737354083912"></a>

-   示例1：授权用户修改裸金属服务器名称。

    ```
    {
        "Version": "1.1",
        "Statement": [
            {
                "Effect": "Allow",
                "Action": [
                    "bms:servers:list",
                    "bms:servers:get",
                    "bms:servers:put"
                ]
            }
        ]
    }
    ```

-   示例2：授权用户批量启动服务器。

    ```
    {
        "Version": "1.1",
        "Statement": [
            {
                "Effect": "Allow",
                "Action": [
                    "bms:servers:list",
                    "bms:servers:get",
                    "bms:servers:start"
                ]
            }
        ]
    }
    ```

-   示例3：拒绝用户下电服务器。

    拒绝策略需要同时配合其他策略使用，否则没有实际作用。用户被授予的策略中，一个授权项的作用如果同时存在Allow和Deny，则遵循**Deny优先原则**。

    如果您给用户授予BMS Admin的系统策略，但不希望用户拥有BMS Admin中定义的下电裸金属服务器权限（bms:servers:stop），您可以创建一条拒绝下电服务器的自定义策略，然后同时将BMS Admin和拒绝策略授予用户，根据Deny优先原则，则用户可以对BMS执行除了下电以外的所有操作。以下策略样例表示：拒绝用户下电裸金属服务器。

    ```
    {
        "Version": "1.1",
        "Statement": [
            {
                "Effect": "Deny",
                "Action": [
                    "bms:servers:stop"
                ]
            }
        ]
    }
    ```


