# 查询裸金属服务器列表（OpenStack原生）<a name="bms_api_0709"></a>

## 功能介绍<a name="section56354875"></a>

查询裸金属服务器信息列表。

## 约束<a name="section54054835151740"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section37431827"></a>

GET /v2.1/\{project\_id\}/servers\{?changes-since=\{changes-since\}&image=\{image\}&flavor=\{flavor\}&name=\{name\}&status=\{status\}&limit=\{limit\}&marker=\{marker\}&tags=\{tags\}&not-tags=\{not-tags\}&reservation\_id=\{reservation\_id\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table67612156510)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|


## 请求消息<a name="section131361554145510"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|changes-since|否|String|裸金属服务器上次更新状态的时间戳信息。格式为ISO 8601时间格式，例如：2013-06-09T06:42:18Z。|
|image|否|String|镜像ID。可以在镜像服务控制台查询，也可以调用“查询镜像列表”API获取。在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。|
|flavor|否|String|规格ID。可以在裸金属服务器控制台查询，也可以调用查询裸金属服务器规格信息列表（OpenStack原生）API获取。|
|name|否|String|裸金属服务器名称，使用模糊匹配的方式查询。例如，“?name=bob”正则表达式会同时返回bob和bobb。如果必须仅匹配bob，则可以使用与基础数据库服务器的语法相匹配的正则表达式，如MySQL或PostgreSQL（官方网站：https://www.postgresql.org/docs/9.2/static/functions-matching.html）。|
|status|否|String|裸金属服务器状态。取值范围：ACTIVE：运行中/正在关机/删除中BUILD：创建中ERROR：故障HARD_REBOOT：强制重启中REBOOT：重启中DELETED：实例已被正常删除SHUTOFF：关机/正在开机/删除中/重建中/重装操作系统中/重装操作系统失败/冻结|
|limit|否|Integer|每页返回裸金属服务器的条数。|
|marker|否|String|从marker指定的裸金属服务器ID的下一条数据开始查询。|
|tags|否|String|查询tag字段中包含该值的裸金属服务器。微版本2.26新增|
|not-tags|否|String|查询tag字段中不包含该值的裸金属服务器，值为标签的Key。如果之前添加的Tag为“Key.Value”的形式，则查询的时候需要使用“Key”来查询。例如：之前添加的tag为“a.b”,则升级后，查询时需使用“not-tags=a”。微版本2.26新增|
|reservation_id|否|String|批量创建裸金属服务器时，指定该预留ID，可以查询同批次创建的裸金属服务器。微版本2.26新增|
|sort_key|否|String|用于排序的属性，包括uuid（裸金属服务器的uuid）、vm_state（裸金属服务器的状态）、display_name（裸金属服务器名称）、task_state（裸金属服务器任务状态）、power_state（电源状态）、created_at（创建时间）、updated_at（更新时间）、availability_zone（可用区）。可以指定多对sort_key和sort_dir。默认排序顺序为created_at逆序。|
|sort_dir|否|String|排序方向。asc：升序desc：降序（默认值）|


-   请求样例
    -   不带可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers
        ```

    -   携带一个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers?tags=__type_baremetal
        ```

    -   携带多个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers?tags=__type_baremetal&name=bms-test01
        ```



## 响应消息<a name="section12079142"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|servers|Array of objects|裸金属服务器信息列表。详情请参见表2。|


    **表 2**  servers字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|name|String|裸金属服务器名称。|
|id|String|裸金属服务器唯一标识。|
|links|Array of objects|裸金属服务器相关快捷链接信息。详情请参见表3。|


    **表 3**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|rel|String|快捷链接标记名称。取值为：self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|
|href|String|对应快捷链接。|



-   响应样例

    ```
    {
        "servers": [
            {
                "name": "bms",
                "links": [
                    {
                        "rel": "self",
                        "href": "https://openstack.example.com/v2.1/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8b-4bc5-ae46-69cacfd4fbaa"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
                    }
                ],
                "id": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
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

