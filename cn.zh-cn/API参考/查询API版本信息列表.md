# 查询API版本信息列表<a name="bms_api_0603"></a>

## 功能介绍<a name="section54478915181842"></a>

查询裸金属服务器当前所有可用的API版本。

## 调试<a name="section28095313113"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=BMS&api=ShowVersionsInfo)中调试该接口。

## URI<a name="section53791107181842"></a>

GET /

## 请求消息<a name="section39878380181842"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/
    ```


## 响应消息<a name="section201868180299"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|versions|Array of objects|描述裸金属服务器API版本信息列表。详情请参见表1。|


    **表 1**  versions字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|id|String|API版本ID。|
|links|Array of objects|API的url地址。详情请参见表2。|
|min_version|String|API支持的最小微版本号。|
|status|String|API版本状态：CURRENT：表示该版本为主推版本。SUPPORTED：表示为老版本，但是现在还在继续支持。DEPRECATED：表示为废弃版本，存在后续删除的可能。|
|updated|String|API版本发布时间。时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2018-09-30T00:00:00Z|
|version|String|API支持的最大微版本号。|


    **表 2**  links字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|href|String|API的url地址。|
|rel|String|API的url地址依赖。取值为：self：包含版本号的资源链接，需要立即跟踪时使用此类链接。bookmark：提供了适合长期存储的资源链接。|


-   响应样例

    ```
    {
        "versions": [
            {
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
        ]
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

