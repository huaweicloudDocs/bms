# 查询裸金属服务器详情列表（OpenStack原生）<a name="bms_api_0710"></a>

## 功能介绍<a name="section33716833"></a>

查询裸金属服务器详情信息列表。

## 约束<a name="section29822855153557"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section35016046"></a>

GET /v2.1/\{project\_id\}/servers/detail\{?changes-since=\{changes-since\}&image=\{image\}&flavor=\{flavor\}&name=\{name\}&status=\{status\}&limit=\{limit\}&marker=\{marker\}&tags=\{tags\}&not-tags=\{not-tags\}&reservation\_id=\{reservation\_id\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table0524112565)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|


## 请求消息<a name="section46708959"></a>

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
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail
        ```

    -   携带一个可选参数

        ```
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail?tags=__type_baremetal
        ```

    -   携带多个可选参数

        ```
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail?tags=__type_baremetal&name=bms-test01
        ```



## 响应消息<a name="section17727455"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|servers|Array of objects|裸金属服务器信息列表详情。内容参见表2。|


    **表 2**  server字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|name|String|裸金属服务器名称。|
|id|String|裸金属服务器唯一标识ID。|
|status|String|裸金属服务器当前状态信息。取值范围：ACTIVE：运行中/正在关机/删除中BUILD：创建中ERROR：故障HARD_REBOOT：强制重启中REBOOT：重启中SHUTOFF：关机/正在开机/删除中/重建中/重装操作系统中/重装操作系统失败/冻结|
|created|String|裸金属服务器创建时间。时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2019-05-22T03:30:52Z|
|updated|String|裸金属服务器上一次更新时间。时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2019-05-22T04:30:52Z|
|flavor|Object|裸金属服务器规格信息。详情请参见表3。|
|image|Object|裸金属服务器镜像信息。详情请参见表4。|
|tenant_id|String|裸金属服务器所属租户ID，UUID格式。该参数和project_id表示相同的概念。|
|key_name|String|SSH密钥名称。|
|user_id|String|裸金属服务器所属用户ID。|
|metadata|Map<String,String>|裸金属服务器元数据。用户自定义metadata键值对。键、值长度均不大于255字节。|
|hostId|String|裸金属服务器对应的主机ID。|
|addresses|Map<String,Array of address objects>|裸金属服务器对应的网络地址信息。裸金属服务器所属网络信息。key：表示裸金属服务器使用的虚拟私有云的ID。value：网络详细信息。|
|security_groups|Array of objects|裸金属服务器所属安全组列表。详情请参见表7。|
|links|Array of objects|裸金属服务器相关快捷链接信息。详情请参见表5。|
|OS-DCF:diskConfig|String|扩展属性，磁盘配置方式，取值为以下两种：MANUAL：API使用镜像中的分区方案和文件系统创建裸金属服务器。如果目标flavor磁盘较大，则API不会对剩余磁盘空间进行分区。AUTO：API使用与目标flavor磁盘大小相同的单个分区创建裸金属服务器，API会自动调整文件系统以适应整个分区。|
|OS-EXT-AZ:availability_zone|String|扩展属性，裸金属服务器所在可用区名称。|
|OS-EXT-SRV-ATTR:host|String|扩展属性，裸金属服务器宿主机名称。|
|OS-EXT-SRV-ATTR:hypervisor_hostname|String|扩展属性，hypervisor主机名称，由Nova virt驱动提供。|
|OS-EXT-SRV-ATTR:instance_name|String|扩展属性，裸金属服务器别名。|
|OS-EXT-STS:power_state|Integer|扩展属性，裸金属服务器电源状态。取值范围：0，1，2，3，40：pending1：running2：paused3：shutdown4：crashed|
|OS-EXT-STS:task_state|String|扩展属性，裸金属服务器当前的任务状态。取值范围：rebooting：重启中reboot_started：普通重启reboot_started_hard：强制重启powering-off：关机中powering-on：开机中rebuilding：重建中scheduling：调度中deleting：删除中|
|OS-EXT-STS:vm_state|String|扩展属性，裸金属服务器的稳定状态。取值范围：active：运行中shutoff：关机suspended：暂停reboot：重启|
|OS-SRV-USG:launched_at|String|扩展属性，裸金属服务器启动时间。时间戳格式为ISO 8601，例如：2019-05-22T03:23:59.000000|
|OS-SRV-USG:terminated_at|String|扩展属性，裸金属服务器删除时间。时间戳格式为ISO 8601，例如：2019-05-22T04:23:59.000000|
|os-extended-volumes:volumes_attached|Array of objects|裸金属服务器挂载的云磁盘信息。详情请参见表8。|
|accessIPv4|String|预留属性。|
|accessIPv6|String|预留属性。|
|fault|Object|故障原因，如果裸金属服务器为故障状态，则返回该字段。详情请参见表9。|
|config_drive|String|预留属性。|
|progress|Integer|预留属性。|
|description|String|描述信息。微版本2.19新增|
|host_status|String|裸金属服务器宿主机状态。UP：服务正常UNKNOWN：状态未知DOWN：服务异常MAINTENANCE：维护状态空字符串：裸金属服务器无主机信息微版本2.16新增|
|OS-EXT-SRV-ATTR:hostname|String|裸金属服务器的主机名。微版本2.3新增|
|OS-EXT-SRV-ATTR:reservation_id|String|批量创建场景，裸金属服务器的预留id。微版本2.3新增|
|OS-EXT-SRV-ATTR:launch_index|Integer|批量创建场景，裸金属服务器的启动顺序。微版本2.3新增|
|OS-EXT-SRV-ATTR:kernel_id|String|若使用AMI格式的镜像，则表示kernel image的UUID；否则，留空。微版本2.3新增|
|OS-EXT-SRV-ATTR:ramdisk_id|String|若使用AMI格式镜像，则表示ramdisk image的UUID；否则，留空。微版本2.3新增|
|OS-EXT-SRV-ATTR:root_device_name|String|裸金属服务器系统盘的设备名称，例如“/dev/sda”。微版本2.3新增|
|OS-EXT-SRV-ATTR:user_data|String|创建裸金属服务器时指定的user_data，取值为base64编码的结果或空字符串。|
|locked|Boolean|裸金属服务器实例是否为锁定状态。true：锁定false：未锁定微版本2.9新增|
|tags|Array of strings|裸金属服务器标签列表。微版本2.26新增，如果不使用微版本查询，响应中无tags字段。tag值遵循如下规则：key与value使用“=”连接，如“key=value”。如果value为空字符串，则仅返回key。|
|sys_tags|Array of objects|裸金属服务器系统标签。详情请参见表3。|
|enterprise_project_id|String|企业项目ID。|
|os:scheduler_hints|Object|裸金属服务器调度信息。详情请参见表4。|


    **表 3**  sys\_tags字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|key|String|系统标签的Key值。|
|value|String|系统标签的value值。|


    **表 4**  os:scheduler\_hints字段数据结构说明（响应参数）

|参数|参数类型|描述|
|--|--|--|
|group|Array of strings|云服务器组ID，UUID格式。|


    **表 5**  flavor字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|裸金属服务器类型ID。|
|links|Array of objects|裸金属服务器类型相关快捷链接信息。详情请参见表5。|


    **表 6**  image字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|裸金属服务器镜像ID。|
|links|Array of objects|裸金属服务器镜像相关快捷链接信息。详情请参见表5。|


    **表 7**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|rel|String|快捷链接标记名称。取值为：self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|
|href|String|对应快捷链接。|


    **表 8**  address字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|addr|String|IP地址信息。|
|version|Integer|IP地址类型，值为4或6。4：IP地址类型是IPv46：IP地址类型是IPv6|
|OS-EXT-IPS-MAC:mac_addr|String|扩展属性，MAC地址。|
|OS-EXT-IPS:type|String|扩展属性，IP地址类型。fixed：代表私有IP地址。floating：代表弹性IP地址。|


    **表 9**  security\_groups字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|name|String|创建裸金属服务器时未指定安全组，该值为default。创建裸金属服务器时指定了安全组，该值为安全组名称。|


    **表 10**  os-extended-volumes:volumes\_attached字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|云磁盘ID。|
|delete_on_termination|Boolean|删除裸金属服务器时是否一并删除该卷。true：是false：否微版本2.3新增|


    **表 11**  fault字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|message|String|故障信息。|
|code|Integer|故障code。|
|details|String|故障详情。|
|created|String|故障时间，ISO 8601格式。|



-   响应样例

    ```
    {
        "servers": [
            {
                "tenant_id": "c685484a8cc2416b97260938705deb64",
                "addresses": {
                    "08a7715f-7de6-4ff9-a343-95ba4209f24a": [
                        {
                            "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:0e:c4:77",
                            "OS-EXT-IPS:type": "fixed",
                            "addr": "192.168.0.107",
                            "version": 4
                        }
                    ]
                },
                "metadata": {
                    "op_svc_userid": "1311c433dd9b408886f57d695c229cbe"
                },
                "OS-EXT-STS:task_state": null,
                "OS-DCF:diskConfig": "MANUAL",
                "OS-EXT-AZ:availability_zone": "az-dc-1",
                "links": [
                    {
                        "rel": "self",
                        "href": "https://openstack.example.com/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                    }
                ],
                "OS-EXT-STS:power_state": 1,
                "id": "95bf2490-5428-432c-ad9b-5e3406f869dd",
                "os-extended-volumes:volumes_attached": [
                    {
                        "id": "dfa375b5-9856-44ad-a937-a4802b6434c3"
                    },
                    {
                        "id": "bb9f1b27-843b-4561-b62e-ca18eeaec417"
                    },
                    {
                        "id": "86e801c3-acc6-465d-890c-d43ba493f553"
                    },
                    {
                        "id": "0994d3ac-3c6a-495c-a439-c597a4f08fa6"
                    }
                ],
                "OS-EXT-SRV-ATTR:host": "bms.az1",
                "image": {
                    "links": [
                        {
                            "rel": "bookmark",
                            "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/images/1a6635d8-afea-4f2b-abb6-27a202bad319"
                        }
                    ],
                    "id": "1a6635d8-afea-4f2b-abb6-27a202bad319"
                },
                "OS-SRV-USG:terminated_at": null,
                "accessIPv4": "",
                "accessIPv6": "",
                "created": "2017-05-24T06:14:05Z",
                "hostId": "e9c3ee0fcc58ab6085cf30df70b5544eab958858fb50d925f023e53e",
                "OS-EXT-SRV-ATTR:hypervisor_hostname": "nova004@2",
                "key_name": "KeyPair-JX",
                "flavor": {
                    "links": [
                        {
                            "rel": "bookmark",
                            "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/flavors/physical.83.medium"
                        }
                    ],
                    "id": "physical.83.medium"
                },
                "security_groups": [
                    {
                        "name": "0011b620-4982-42e4-ad12-47c95ca495c4"
                    }
                ],
                "config_drive": "",
                "OS-EXT-STS:vm_state": "active",
                "OS-EXT-SRV-ATTR:instance_name": "instance-0000ebd3",
                "user_id": "1311c433dd9b408886f57d695c229cbe",
                "name": "bms",
                "progress": 0,
                "OS-SRV-USG:launched_at": "2017-05-25T03:40:25.066078",
                "updated": "2017-05-25T03:40:25Z",
                "status": "ACTIVE"
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

