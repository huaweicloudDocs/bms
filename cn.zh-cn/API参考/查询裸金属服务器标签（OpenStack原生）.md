# 查询裸金属服务器标签（OpenStack原生）<a name="bms_api_0743"></a>

## 功能介绍<a name="section17769131"></a>

查询裸金属服务器的所有标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="section40393097103718"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#table0142163245812)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section43810255103718"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags
    ```


## 响应消息<a name="section60965769103718"></a>

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

