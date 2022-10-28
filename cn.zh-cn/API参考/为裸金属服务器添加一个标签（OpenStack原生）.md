# 为裸金属服务器添加一个标签（OpenStack原生）<a name="bms_api_0746"></a>

## 功能介绍<a name="section63429208111321"></a>

为裸金属服务器添加一个标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section26150540144115"></a>

-   tag个数不超过50个。
-   tag的长度不超过80个字符。
-   tag不能以点“.”开头。
-   不支持创建空tag（空串）。

>![](public_sys-resources/icon-note.gif) **说明：** 
>建议为裸金属服务器添加“\_\_type\_baremetal”标签，标识是一台裸金属服务器。

## URI<a name="section1885963111321"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table19718185512020)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|
|tag|是|标签信息。约束：标签的长度不超过80个字符。标签不能以点“.”开头。不支持创建空标签（空串）。中文或特殊字符需要进行URLEncode。|


## 请求消息<a name="section26704907111321"></a>

-   请求参数

    无

-   请求样例

    ```
    PUT https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags/{tag}
    ```


## 响应消息<a name="section6307065111321"></a>

不涉及。

## 返回值<a name="section27037160"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

