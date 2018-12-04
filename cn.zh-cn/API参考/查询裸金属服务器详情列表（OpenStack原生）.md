# 查询裸金属服务器详情列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158679"></a>

## 功能介绍<a name="section33716833"></a>

查询裸金属服务器详情信息列表，接口版本为v2.1，支持带微版本号查询。在请求Header中增加一组Key-Value值， Key固定为“X-OpenStack-Nova-API-Version” ，Value为可选的微版本号，例如“2.26”。表示使用微版本号为2.26进行查询。

## 约束<a name="section29822855153557"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section35016046"></a>

GET /v2.1/\{project\_id\}/servers/detail

参数说明请参见[表1](#table0524112565)。

**表 1**  参数说明

<a name="table0524112565"></a>
<table><thead align="left"><tr id="row252211165610"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p55073076202321"><a name="p55073076202321"></a><a name="p55073076202321"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p44659366114813"><a name="p44659366114813"></a><a name="p44659366114813"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p19572211"><a name="p19572211"></a><a name="p19572211"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1524119564"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p6789122714241"><a name="p6789122714241"></a><a name="p6789122714241"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p4344474"><a name="p4344474"></a><a name="p4344474"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p16358126"><a name="p16358126"></a><a name="p16358126"></a>项目ID。</p>
</td>
</tr>
</tbody>
</table>

查询裸金属服务器列表时可选的查询检索参数请参考[查询裸金属服务器列表（OpenStack原生）](查询裸金属服务器列表（OpenStack原生）.md)中的[表2](查询裸金属服务器列表（OpenStack原生）.md#table1758718426522)。

## 请求消息<a name="section46708959"></a>

不涉及。

## 响应消息<a name="section17727455"></a>

-   响应参数

    <a name="table61256692"></a>
    <table><thead align="left"><tr id="row16697504"><th class="cellrowborder" valign="top" width="17.86%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="32.14%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row64050727"><td class="cellrowborder" valign="top" width="17.86%" headers="mcps1.1.4.1.1 "><p id="p20726409"><a name="p20726409"></a><a name="p20726409"></a>servers</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.4.1.2 "><p id="p491044173818"><a name="p491044173818"></a><a name="p491044173818"></a>列表数据结构。</p>
    <p id="p23416123"><a name="p23416123"></a><a name="p23416123"></a>内容参见<a href="查询裸金属服务器详情（OpenStack原生）.md">查询裸金属服务器详情（OpenStack原生）</a>中的“[1] server字段数据结构说明”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="32.14%" headers="mcps1.1.4.1.3 "><p id="p24702645"><a name="p24702645"></a><a name="p24702645"></a>裸金属服务器信息列表详情。</p>
    </td>
    </tr>
    </tbody>
    </table>


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
                "OS-EXT-AZ:availability_zone": "eu-de-01",
                "links": [
                    {
                        "rel": "self",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
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
                "OS-EXT-SRV-ATTR:host": "bms.eu-de-01",
                "image": {
                    "links": [
                        {
                            "rel": "bookmark",
                            "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/images/1a6635d8-afea-4f2b-abb6-27a202bad319"
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
                            "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/flavors/physical.83.medium"
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


## 返回值<a name="section25329374"></a>

请参考[通用返回值](通用返回值.md)。

