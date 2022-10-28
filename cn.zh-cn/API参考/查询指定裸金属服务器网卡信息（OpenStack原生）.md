# 查询指定裸金属服务器网卡信息（OpenStack原生）<a name="bms_api_0731"></a>

## 功能介绍<a name="section44739342"></a>

根据网卡ID，查询裸金属服务器网卡信息。

## URI<a name="section901"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-interface/\{id\}

参数说明请参见[表1](#table1210415012480)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|
|id|是|网卡ID。可以在裸金属服务器详情页面“网卡”页签中查看；也可以通过查询裸金属服务器网卡信息（OpenStack原生）API获取，对应的是参数“port_id”的取值。|


## 请求消息<a name="section8117"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/os-interface/ce531f90-199f-48c0-816c-13e38010b442
    ```


## 响应消息<a name="section73053"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|interfaceAttachment|Object|裸金属服务器网卡信息列表，详情请参见表2。|


    **表 2**  interfaceAttachment字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|port_state|String|网卡端口状态，取值为：ACTIVE、BUILD、DOWN。|
|fixed_ips|Array of objects|网卡IP信息列表，详情请参见表3。|
|net_id|String|网卡端口所属子网的网络ID（network_id）。|
|port_id|String|网卡端口ID。|
|mac_addr|String|网卡MAC地址信息。|


    **表 3**  fixed\_ips字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|subnet_id|String|网卡私网IP对应子网的子网ID（subnet_id）。|
|ip_address|String|网卡IP地址。|



-   响应样例

    ```
    {
        "interfaceAttachment": {
            "port_state": "ACTIVE",
            "fixed_ips": [
                {
                    "subnet_id": "f8a6e8f8-c2ec-497c-9f23-da9616de54ef",
                    "ip_address": "192.168.1.3"
                }
            ],
            "net_id": "3cb9bc59-5699-4588-a4b1-b87f96708bc6",
            "port_id": "ce531f90-199f-48c0-816c-13e38010b442",
            "mac_addr": "fa:16:3e:4c:2c:30"
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

