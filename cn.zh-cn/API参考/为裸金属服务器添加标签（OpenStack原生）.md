# 为裸金属服务器添加标签（OpenStack原生）<a name="bms_api_0744"></a>

## 功能介绍<a name="section59539732104217"></a>

为裸金属服务器添加标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section12956040151655"></a>

标签个数不超过50个。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   建议为裸金属服务器添加“\_\_type\_baremetal”标签，标识是一台裸金属服务器。否则，裸金属服务器将仅在ECS控制台可见，而不在BMS控制台。
>-   新增标签时，会覆盖原有标签。如需保留原有标签，请在添加时，将原有标签加入到新增标签的列表中。建议每次添加标签时，将“\_\_type\_baremetal”放在请求新增的tags列表中。

## URI<a name="section52138884104217"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#table7714219185912)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section18620476104217"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|tags|是|Array of strings|标签列表，每个标签不超过80个字符。标签不能以“.”开头。标签个数不超过50个。不支持创建空标签（空串）。|


-   请求样例

    ```
    PUT https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags
    ```

    ```
    {
        "tags": [
            "baz",
            "foo",
            "qux"
        ]
    }
    ```


## 响应消息<a name="section6196486814321"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|tags|Array of strings|用户自定义标签列表。|



-   响应样例

    ```
    {
        "tags": [
            "baz",
            "foo",
            "qux"
        ]
    }
    ```


## 返回值<a name="section7610951"></a>

正常返回值：

|返回值|说明|
|--|--|
|200|服务器已成功处理了请求。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

