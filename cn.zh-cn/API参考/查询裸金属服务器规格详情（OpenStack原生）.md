# 查询裸金属服务器规格详情（OpenStack原生）<a name="bms_api_0727"></a>

## 功能介绍<a name="section64833508"></a>

根据裸金属服务器的规格ID，查询规格的详细信息，比如规格名称、CPU核数、内存大小等。

## URI<a name="section46630661"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavor\_id\}

参数说明请参见[表1](#table1857156445)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|flavor_id|是|规格ID。可以在裸金属服务器控制台查询，也可以通过查询裸金属服务器规格信息列表（OpenStack原生）API获取。|


## 请求消息<a name="section17022773"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium
    ```


## 响应消息<a name="section18987236"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|flavor|Object|裸金属服务器规格。详情请参见表2。|


    **表 2**  flavor数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|裸金属服务器规格ID。|
|name|String|裸金属服务器规格名称。|
|vcpus|Integer|该裸金属服务器规格对应的CPU核数。|
|ram|Integer|该裸金属服务器规格对应的内存大小，单位为MB。|
|disk|Integer|该裸金属服务器规格对应要求磁盘大小，单位为GB。|
|swap|String|未使用。|
|OS-FLV-EXT-DATA:ephemeral|Integer|未使用。|
|OS-FLV-DISABLED:disabled|Boolean|未使用。|
|rxtx_factor|Float|未使用。|
|os-flavor-access:is_public|Boolean|未使用。|
|links|Array of objects|规格相关快捷链接地址。详情请参见表3。|


    **表 3**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|rel|String|快捷链接标记名称。self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|
|href|String|对应快捷链接。|



-   响应样例

    ```
    {
        "flavor": {
            "name": "physical.o2.medium",
            "links": [
                {
                    "href": "https://openstack.example.com/v2/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium",
                    "rel": "self"
                },
                {
                    "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium",
                    "rel": "bookmark"
                }
            ],
            "ram": 192705,
            "OS-FLV-DISABLED:disabled": false,
            "vcpus": 24,
            "swap": "",
            "os-flavor-access:is_public": true,
            "rxtx_factor": 1,
            "OS-FLV-EXT-DATA:ephemeral": 0,
            "disk": 1862,
            "id": "physical.o2.medium"
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

