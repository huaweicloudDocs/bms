# 查询裸金属服务器规格信息列表（OpenStack原生）<a name="bms_api_0726"></a>

## 功能介绍<a name="section57769674"></a>

查询裸金属服务器规格信息列表。

## 约束<a name="section60580832213029"></a>

本接口查询出来的规格为系统中所有的规格，其中规格的名称以“physical”开头的为裸金属服务器的规格，可用于申请裸金属服务器。

## URI<a name="section50165025"></a>

GET /v2.1/\{project\_id\}/flavors/detail\{?minDisk=\{minDisk\}&minRam=\{minRam\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table1687344817416)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|


查询裸金属服务器规格时可选的查询检索参数如[表2](#table1719300427)所示。

**表 2**  可选的查询检索参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|minDisk|否|String|最小的硬盘规格，单位GB，大于等于此规格的都可以查询到。|
|minRam|否|String|最小的内存规格，单位MB，大于等于此规格的都可以查询到。|
|sort_key|否|String|排序字段，默认值为：flavorid。可以指定的其他key为name/ memory_mb/vcpus，/root_gb/flavorid。|
|sort_dir|否|String|升序/降序排序。可以指定的参数为asc/desc，默认值为：asc|


## 请求消息<a name="section48832041"></a>

-   请求参数

    无

-   请求样例
    -   不带可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail
        ```

    -   携带一个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail?minDisk=3725
        ```

    -   携带多个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail?minDisk=3725&is_public=true
        ```



## 响应消息<a name="section36835188"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|flavors|Array of objects|裸金属服务器规格列表。详情请参见表3。|


    **表 3**  flavors数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|裸金属服务器规格ID。|
|name|String|裸金属服务器规格名称。|
|vcpus|Integer|该裸金属服务器规格对应的CPU核数。|
|ram|Integer|该裸金属服务器规格对应的内存大小，单位为MB。|
|disk|Integer|该裸金属服务器规格对应要求的磁盘大小，单位为GB。|
|swap|String|未使用。|
|OS-FLV-EXT-DATA:ephemeral|Integer|未使用。|
|OS-FLV-DISABLED:disabled|Boolean|未使用。|
|rxtx_factor|Float|未使用。|
|os-flavor-access:is_public|Boolean|未使用。|
|links|Array of objects|规格相关快捷链接地址。详情请参见表4。|


    **表 4**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|rel|String|快捷链接标记名称。self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|
|href|String|对应快捷链接。|



-   响应样例

    ```
    {
        "flavors": [
            {
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
                "ram": 321725,
                "OS-FLV-DISABLED:disabled": false,
                "vcpus": 56,
                "swap": "",
                "os-flavor-access:is_public": true,
                "rxtx_factor": 1,
                "OS-FLV-EXT-DATA:ephemeral": 0,
                "disk": 3725,
                "id": "physical.o2.medium"
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

