# Windows裸金属服务器清除密码<a name="bms_api_0638"></a>

## 功能介绍<a name="section57769674"></a>

清除Windows裸金属服务器初始安装时系统生成的密码记录。清除密码后，不影响裸金属服务器密码登录功能，但不能再使用获取密码功能来查询该裸金属服务器密码。

如果裸金属服务器是通过私有镜像创建的，请确保已安装Cloudbase-init。公共镜像默认已安装该软件。

## 调试<a name="section28095313113"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=BMS&api=DeleteWindowsBareMetalServerPassword)中调试该接口。

## URI<a name="section50165025"></a>

DELETE /v1/\{project\_id\}/baremetalservers/\{server\_id\}/os-server-password

参数说明请参见[表1](#table23262209)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|server_id|是|裸金属服务器ID。可以从裸金属服务器控制台查询，或者通过调用查询裸金属服务器列表（OpenStack原生）API获取。|


## 请求消息<a name="section48832041"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{BMS Endpoint}/v1/bbf1946d374b44a0a2a95533562ba954/baremetalservers/cf2a8b97-b5c6-47ef-9714-eb27adf26e5b/os-server-password
    ```


## 响应消息<a name="section1927776"></a>

不涉及。

## 返回值<a name="section7610951"></a>

正常返回值：

|返回值|说明|
|--|--|
|202|服务器已接受请求，延迟处理|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

