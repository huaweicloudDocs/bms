# 查询裸金属服务器规格extra\_specs参数的详情（OpenStack原生）<a name="bms_api_0728"></a>

## 功能介绍<a name="section62221755111516"></a>

“extra\_specs”参数用于描述裸金属服务器规格的键值对，例如“baremetal:extBootType”表示裸金属服务器的启动源，取值有两种：“LocalDisk”（表示本地盘）和“Volume”（表示云硬盘）。如果您想确认某个规格是否支持快速发放，那么可以调用该接口进行查询。

## URI<a name="section116617920169"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavor\_id\}/os-extra\_specs

参数说明请参见[表1](#table955744812451)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|flavor_id|是|规格ID。可以在裸金属服务器控制台查询，也可以通过查询裸金属服务器规格信息列表（OpenStack原生）API获取。|


## 请求消息<a name="section1517812126172"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/flavors/physical.s2.medium/os-extra_specs
    ```


## 响应消息<a name="section3899184185"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|extra_specs|Object|描述裸金属服务器规格的键值对。capabilities:cpu_arch：裸金属服务器的CPU架构，取值为x86_64（适用于x86机型）或aarch64（适用于ARM机型）baremetal:disk_detail：磁盘的描述信息。capabilities:hypervisor_type：hypervisor类型，固定为“ironic”。baremetal:__support_evs：是否支持云硬盘，取值为true或false。如果裸金属服务器规格中没有此参数，表示不支持云硬盘。baremetal:extBootType：表示裸金属服务器的启动源，取值为LocalDisk（表示本地盘）或Volume（表示云硬盘，即快速发放）baremetal:net_num：裸金属服务器实际可绑定的网卡数量。baremetal:netcard_detail：网卡的描述信息。baremetal:cpu_detail：CPU的描述信息。resource_type：资源类型，固定为“ironic”。baremetal:memory_detail：内存的描述信息。|



-   响应样例

    ```
    {
        "extra_specs": {
            "capabilities:cpu_arch": "x86_64",
            "baremetal:disk_detail": "SAS 8T",
            "capabilities:hypervisor_type": "ironic",
            "baremetal:__support_evs": "true",
            "baremetal:extBootType": "LocalDisk",
            "capabilities:board_type": "s2m",
            "baremetal:net_num": "2",
            "baremetal:netcard_detail": "2*10GE",
            "baremetal:cpu_detail": "2*8coreIntel Xeon E5-2667 V43.2GHz",
            "resource_type": "ironic",
            "baremetal:memory_detail": "256GB DDR4 RAM(GB)"
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

