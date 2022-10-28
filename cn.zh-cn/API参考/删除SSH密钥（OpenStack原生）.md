# 删除SSH密钥（OpenStack原生）<a name="bms_api_0741"></a>

## 功能介绍<a name="section63429208111321"></a>

根据SSH密钥的名称，删除指定SSH密钥。

## URI<a name="section1885963111321"></a>

DELETE /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table155384213575)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|keypair_name|是|密钥名称。可以通过查询SSH密钥列表（OpenStack原生）API获取。|


## 请求消息<a name="section26704907111321"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/os-keypairs/keypair-test
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

