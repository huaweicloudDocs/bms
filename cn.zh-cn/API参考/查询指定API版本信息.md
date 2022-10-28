# 查询指定API版本信息<a name="bms_api_0604"></a>

## 功能介绍<a name="section553655182144"></a>

查询裸金属服务指定API版本的信息。

## 调试<a name="section28095313113"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=BMS&api=ShowSpecifiedVersion)中调试该接口。

## URI<a name="section961608182144"></a>

GET /\{api\_version\}

参数说明请参见[表1](#table46110007)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|api_version|是|API版本号。例如：v1|


## 请求消息<a name="section19667838182144"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/v1
    ```


## 响应消息<a name="section43666554182144"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|version|Object|描述裸金属服务器API指定版本信息。详情请参见表2。|


    **表 2**  version字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|API版本ID。|
|links|Array of objects|API的url地址。详情请参见表3。|
|min_version|String|API支持的最小微版本号。|
|status|String|API版本状态：CURRENT：表示该版本为主推版本。SUPPORTED：表示为老版本，但是现在还在继续支持。DEPRECATED：表示为废弃版本，存在后续删除的可能。|
|updated|String|API版本发布时间。时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2018-09-30T00:00:00Z|
|version|String|API支持的最大微版本号。|


    **表 3**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|href|String|API的url地址。|
|rel|String|API的url地址依赖。取值为：self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|



-   响应样例

    ```
    {
        "version": {
            "id": "v1",
            "links": [
                {
                    "href": "http://bms.xxx.com/v1/",
                    "rel": "self"
                }
            ],
            "min_version": "",
            "status": "CURRENT",
            "updated": "2018-09-30T00:00:00Z",
            "version": ""
        }
    }
    ```


## 返回值<a name="section12571834"></a>

正常返回值：

|返回值|说明|
|--|--|
|200|服务器已成功处理了请求。|


其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section12157147171520"></a>

请参考[错误码](错误码.md)。

