# 查询裸金属服务器IP地址（OpenStack原生）<a name="bms_api_0723"></a>

## 功能介绍<a name="section53922917165259"></a>

查询裸金属服务器私有IP地址信息。

## 约束<a name="section64211377173223"></a>

不支持分页查询。

## URI<a name="section51121191165259"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/ips

参数说明请参见[表1](#table1152617127395)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section8194118165259"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/ips
    ```


## 响应消息<a name="section58140617165259"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|addresses|Map<String,Array of address objects>|裸金属服务器所属网络信息。key：表示裸金属服务器使用的虚拟私有云的ID。value：网络详细信息。|


    **表 2**  address参数结构说明

|参数|参数类型|描述|
|--|--|--|
|version|Integer|IP地址版本，取值为：4：IPv46：IPv6|
|addr|String|IP地址。|



-   响应样例

    ```
    {
        "addresses": {
            "08a7715f-7de6-4ff9-a343-95ba4209f24a": [
                {
                    "version": 4,
                    "addr": "192.168.2.90"
                }
            ]
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

