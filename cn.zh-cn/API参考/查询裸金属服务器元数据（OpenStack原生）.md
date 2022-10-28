# 查询裸金属服务器元数据（OpenStack原生）<a name="bms_api_0718"></a>

## 功能介绍<a name="section61558535185333"></a>

裸金属服务器元数据包含了裸金属服务器在云平台的基本信息，例如服务器ID、主机名、网络信息等。通过该接口，您可以查询裸金属服务器的元数据。

## 约束<a name="section57278039123222"></a>

不支持分页查询。

## URI<a name="section47451206185333"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table3831319143216)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section14818796185333"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata
    ```


## 响应消息<a name="section22254218185333"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|metadata|Map<String,String>|用户自定义metadata键值对。键、值长度均不大于255字节。|


-   响应样例

    ```
    {
        "metadata": {
            "key": "value"
        }
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

