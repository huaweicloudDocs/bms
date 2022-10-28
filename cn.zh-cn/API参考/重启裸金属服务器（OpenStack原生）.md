# 重启裸金属服务器（OpenStack原生）<a name="bms_api_0714"></a>

## 功能介绍<a name="section6488958"></a>

重启单台裸金属服务器。

## 约束<a name="section57278039123222"></a>

当前仅支持强制重启。

## URI<a name="section58400626"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table6943612162916)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section55843593"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|reboot|是|Object|标记为重启裸金属服务器操作。详情请参见表2。|


    **表 2**  reboot字段数据结构说明

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|type|是|String|重启类型：SOFT：普通重启。HARD：强制重启。当前SOFT参数无效，即均为强制重启。|



-   请求样例

    ```
    POST https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/action
    ```

    ```
    {
        "reboot": {
            "type": "HARD"
        }
    }
    ```


## 响应消息<a name="section32830290"></a>

不涉及。

## 返回值<a name="section27037160"></a>

正常返回值：

|返回值|说明|
|--|--|
|204|服务器成功处理了请求，但没有返回任何内容。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

