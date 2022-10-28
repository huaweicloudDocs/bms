# 查询裸金属服务器挂载的云硬盘信息（OpenStack原生）<a name="bms_api_0733"></a>

## 功能介绍<a name="section61843920"></a>

查询裸金属服务器挂载的云硬盘信息。

## URI<a name="section19724370"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-volume\_attachments

参数说明请参见[表1](#table98221910184910)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section43301605"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/os-volume_attachments
    ```


## 响应消息<a name="section54170131"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|volumeAttachments|Object|裸金属服务器挂载信息列表，详情请参见表2。|


    **表 2**  volumeAttachments字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|device|String|挂载目录，例如“/dev/vdb”。|
|id|String|挂载资源ID。|
|serverId|String|所属裸金属服务器ID。|
|volumeId|String|挂载云硬盘ID。|



-   响应样例

    ```
    {
        "volumeAttachments": {
            "device": "/dev/vdb",
            "serverId": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa",
            "id": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6",
            "volumeId": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6"
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

