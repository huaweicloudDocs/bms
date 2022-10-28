# 删除裸金属服务器标签（OpenStack原生）<a name="bms_api_0745"></a>

## 功能介绍<a name="section46928615105534"></a>

删除裸金属服务器的所有标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section76881969360"></a>

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   “\_\_type\_baremetal”标识是一台裸金属服务器，建议不要删除“\_\_type\_baremetal”标签，否则，裸金属服务器将仅在ECS控制台可见，而不在BMS控制台。
>-   “\_\_type\_baremetal”删除后可通过[为裸金属服务器添加一个标签（OpenStack原生）](为裸金属服务器添加一个标签（OpenStack原生）.md)进行重新添加，添加后裸金属服务器会重新显示在BMS的控制台。

## URI<a name="section3181044105534"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#table17718161117017)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section61879170105534"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags
    ```


## 响应消息<a name="section33789573105534"></a>

不涉及。

## 返回值<a name="section27037160"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

