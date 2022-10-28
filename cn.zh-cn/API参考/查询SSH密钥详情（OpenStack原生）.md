# 查询SSH密钥详情（OpenStack原生）<a name="bms_api_0739"></a>

## 功能介绍<a name="section59539732104217"></a>

根据SSH密钥名称查询指定SSH密钥。

## URI<a name="section52138884104217"></a>

GET /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table1179423205514)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|keypair_name|是|密钥名称信息。可以通过查询SSH密钥列表（OpenStack原生）API获取。|


## 请求消息<a name="section18620476104217"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/os-keypairs/keypair-test
    ```


## 响应消息<a name="section18336671104217"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|keypair|Object|SSH密钥信息，详情请参见表2。|


    **表 2**  keypair字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|public_key|String|密钥对应publicKey信息。|
|name|String|密钥名称。|
|fingerprint|String|密钥对应指纹信息。|
|created_at|String|密钥创建时间。时间戳格式为ISO 8601，例如：2019-05-07T12:06:13.681238|
|deleted|Boolean|密钥删除标记。true：表示密钥已被删除。false：表示密钥未被删除。|
|deleted_at|String|密钥删除时间。时间戳格式为ISO 8601，例如：2019-05-07T12:06:13.681238|
|id|String|密钥ID。|
|updated_at|String|密钥更新时间。时间戳格式为ISO 8601，例如：2019-05-07T12:06:13.681238|
|user_id|String|密钥所属用户信息。|


-   响应样例

    ```
    {
        "keypair": {
            "created_at": "2019-05-07T12:06:13.681238",
            "deleted": false,
            "deleted_at": null,
            "fingerprint": "9d:00:f4:d7:26:6e:52:06:4c:c1:d3:1d:fd:06:66:01",
            "id": 1,
            "name": "keypair-3582d8b7-e588-4aad-b7f7-f4e76f0e4314",
            "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDYJrTVpcMwFqQy/oMvtUSRofZdSRHEwrsX8AYkRvn2ZnCXM+b6+GZ2NQuuWj+ocznlnwiGFQDsL/yeE+/kurqcPJFKKp60mToXIMyzioFxW88fJtwEWawHKAclbHWpR1t4fQ4DS+/sIbX/Yd9btlVQ2tpQjodGDbM9Tr9/+/3i6rcR+EoLqmbgCgAiGiVV6VbM2Zx79yUwd+GnQejHX8BlYZoOjCnt3NREsITcmWE9FVFy6TnLmahs3FkEO/QGgWGkaohAJlsgaVvSWGgDn2AujKYwyDokK3dXyeX3m2Vmc3ejiqPa/C4nRrCOlko5nSgV/9IXRx1ERImsqZnE9usB Generated-by-Nova",
            "updated_at": null,
            "user_id": "fake"
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

