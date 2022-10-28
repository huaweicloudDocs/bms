# 启动裸金属服务器（OpenStack原生）<a name="bms_api_0713"></a>

## 功能介绍<a name="section5894231"></a>

启动单台裸金属服务器。

## URI<a name="section53048087"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table15103162717019)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section7670737"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|os-start|是|null|标记为启动裸金属服务器操作，数据结构为空。|


-   请求样例

    ```
    POST https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/action
    ```

    ```
    {
        "os-start": {}
    }
    ```


## 响应消息<a name="section1927776"></a>

不涉及。

## 返回值<a name="section17349988"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

