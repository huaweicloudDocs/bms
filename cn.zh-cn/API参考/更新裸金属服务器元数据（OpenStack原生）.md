# 更新裸金属服务器元数据（OpenStack原生）<a name="bms_api_0719"></a>

## 功能介绍<a name="section61558535185333"></a>

更新裸金属服务器的元数据。

-   如果元数据中没有待更新字段，则自动添加该字段。
-   如果元数据中已存在待更新字段，则直接更新字段值。

## 约束<a name="section57278039123222"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section47451206185333"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table560512381338)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section14818796185333"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|metadata|是|Object|用户自定义metadata键值对。详情请参见表2。|


    **表 2**  metadata数据结构说明

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|用户自定义字段键值对|是|String|用户自定义metadata键值对。键、值长度均不大于255字节。键名key不支持如下特殊字符：:`~!@#$%^&*()=+<,>?/'";{[]}|\键值value不支持如下特殊字符：\"|



-   请求样例

    ```
    POST https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata
    ```

    ```
    {
        "metadata": {
            "key": "value"
        }
    }
    ```


## 响应消息<a name="section22254218185333"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|metadata|Object|用户自定义metadata键值对。详情请参见表3。|


    **表 3**  metadata字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|用户自定义字段键值对|String|metadata键、值。键、值长度大于0字节且小于256字节。键值value不支持如下特殊字符：\"|


-   响应样例

    ```
    {
        "metadata": {
            "key": "value"
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

