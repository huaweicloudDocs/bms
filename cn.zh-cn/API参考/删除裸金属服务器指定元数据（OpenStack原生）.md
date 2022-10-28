# 删除裸金属服务器指定元数据（OpenStack原生）<a name="bms_api_0721"></a>

## 功能介绍<a name="section5520708185439"></a>

删除裸金属服务器指定元数据。

## 约束<a name="section5072450814374"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active、stopped、paused或者suspended。

## URI<a name="section65173692185439"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table12474435113619)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|
|key|是|待删除的裸金属服务器metadata键值。|


## 请求消息<a name="section21460169185439"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata/{key}
    ```


## 响应消息<a name="section31286738185439"></a>

不涉及。

## 返回值<a name="section27037160"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

