# 修改裸金属服务器指定元数据（OpenStack原生）<a name="bms_api_0720"></a>

## 功能介绍<a name="section19950704192629"></a>

修改裸金属服务器指定元数据。

## 约束<a name="section48821040143631"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active、stopped、paused或者suspended。

## URI<a name="section48549151192629"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table1370626163519)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|
|key|是|待修改的裸金属服务器metadata键值。|


## 请求消息<a name="section42256947192629"></a>

-   请求参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|meta|是|Object|用户自定义metadata键值对。详情请参见表2。|


    **表 2**  meta数据结构说明

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|用户自定义字段键值对|是|String|用户自定义metadata键值对。键、值长度均不大于255字节。键名key不支持如下特殊字符：:`~!@#$%^&*()=+<,>?/'";{[]}|\键值value不支持如下特殊字符：\"|



-   请求样例

    ```
    PUT https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata/{key}
    ```

    ```
    {
        "meta": {
            "key": "value"
        }
    }
    ```


## 响应消息<a name="section12391939192629"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|meta|Object|用户自定义metadata键值对。详情请参见表3。|


    **表 3**  meta字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|用户自定义字段键值对|String|用户自定义metadata键值对。键、值长度均不大于255字节。|


-   响应样例

    ```
    {
        "meta": {
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

