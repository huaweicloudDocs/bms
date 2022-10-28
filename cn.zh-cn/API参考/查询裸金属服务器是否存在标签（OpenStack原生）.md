# 查询裸金属服务器是否存在标签（OpenStack原生）<a name="bms_api_0747"></a>

## 功能介绍<a name="section66970384144623"></a>

查看裸金属服务器是否存在指定标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="section20295111144623"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table6300135020116)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|
|tag|是|待查询标签的key。约束：中文或特殊字符需要进行URLEncode。如果未指定标签的key，将返回该裸金属服务器所有的标签。|


## 请求消息<a name="section56092298144623"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/2d85af7c-cbfe-40c5-a378-4d03b42fb0e2/tags/{tag}
    ```


## 响应消息<a name="section21987090144623"></a>

如果存在指定标签，不涉及。

如果不存在指定标签，响应消息如下：

```
{
    "itemNotFound": {
        "message": "Server 2d85af7c-cbfe-40c5-a378-4d03b42fb0e2 has no tag 'abc'",
        "code": 404
    }
}
```

## 返回值<a name="section27037160"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

