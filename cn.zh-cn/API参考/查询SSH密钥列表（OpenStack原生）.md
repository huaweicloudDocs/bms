# 查询SSH密钥列表（OpenStack原生）<a name="bms_api_0738"></a>

## 功能介绍<a name="section17769131"></a>

查询SSH密钥信息列表。

## 约束<a name="section25186711103718"></a>

不支持分页查询。

## URI<a name="section40393097103718"></a>

GET /v2.1/\{project\_id\}/os-keypairs

参数说明请参见[表1](#table875418115417)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|


## 请求消息<a name="section43810255103718"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/os-keypairs
    ```


## 响应消息<a name="section60965769103718"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|keypairs|Array of objects|密钥信息列表，详情请参见表2。|


    **表 2**  keypairs字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|keypair|Object|密钥信息详情，详情请参见表3。|


    **表 3**  keypair字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|fingerprint|String|密钥对应指纹信息。|
|name|String|密钥名称。|
|type|String|密钥类型，默认为“ssh”。微版本2.2以上支持。|
|public_key|String|密钥对应publicKey信息。|



-   响应样例

    ```
    {
        "keypairs": [
            {
                "keypair": {
                    "fingerprint": "15:b0:f8:b3:f9:48:63:71:cf:7b:5b:38:6d:44:2d:4a",
                    "name": "keypair-test",
                    "type": "ssh",
                    "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC+Eo/RZRngaGTkFs7I62ZjsIlO79KklKbMXi8F+KITD4bVQHHn+kV+4gRgkgCRbdoDqoGfpaDFs877DYX9n4z6FrAIZ4PES8TNKhatifpn9NdQYWA+IkU8CuvlEKGuFpKRi/k7JLos/gHi2hy7QUwgtRvcefvD/vgQZOVw/mGR9Q== Generated-by-Nova"
                }
            }
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

