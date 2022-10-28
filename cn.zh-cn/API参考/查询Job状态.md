# 查询Job状态<a name="bms_api_0640"></a>

## 功能介绍<a name="section1145624712615"></a>

查询Job的执行状态。

对于创建裸金属服务器、挂卸卷等异步API，命令下发后，会返回“job\_id”，通过“job\_id”可以查询任务的执行状态。

## 调试<a name="section28095313113"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=BMS&api=ShowJobInfos)中调试该接口。

## URI<a name="section12499172418819"></a>

GET /v1/\{project\_id\}/jobs/\{job\_id\}

参数说明请参见[表1](#table108782505134)。

**表 1**  参数说明

|参数|是否必选|描述|
|--|--|--|
|project_id|是|项目ID。获取方式请参见获取项目ID。|
|job_id|是|Job ID。|


## 请求消息<a name="section1707915201018"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/v1/bbf1946d374b44a0a2a95533562ba954/jobs/2c9eb2c5544cbf6101544f0635672b60
    ```


## 响应消息<a name="section32178181210"></a>

-   响应参数

|参数|参数类型|描述|
|--|--|--|
|status|String|Job的状态。SUCCESS：成功RUNNING：运行中FAIL：失败INIT：正在初始化|
|entities|Object|Job操作的对象。请参见表2。根据不同Job类型，显示不同的内容。裸金属服务器相关操作显示server_id；网卡相关操作显示nic_id；有子Job时为子Job的详情。|
|job_id|String|Job ID。|
|job_type|String|Job的类型，包含以下类型：baremetalBatchCreate：批量创建裸金属服务器baremetalBatchOperate：批量修改裸金属服务器电源状态baremetalVolumeBootReinstallOs：重装快速发放裸金属服务器操作系统baremetalReinstallOs：重装本地盘裸金属服务器操作系统baremetalAttachVolume：挂载单个磁盘baremetalDetachVolume：卸载单个磁盘|
|begin_time|String|开始时间。时间戳格式为ISO 8601，例如：2019-04-25T20:04:47.591Z|
|end_time|String|结束时间。时间戳格式为ISO 8601，例如：2019-04-26T20:04:47.591Z|
|error_code|String|Job执行失败时的错误码。|
|fail_reason|String|Job执行失败时的错误原因。|
|message|String|出现错误时，返回的错误消息。|
|code|String|出现错误时，返回的错误码。错误码和其对应的含义请参考状态码。|


    **表 2**  entities字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|sub_jobs_total|Integer|子任务数量。没有子任务时为0。|
|sub_jobs|Array of objects|每个子任务的执行信息。没有子任务时为空列表。请参见表3。|


    **表 3**  sub\_jobs字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|status|String|Job的状态。SUCCESS：成功RUNNING：运行中FAIL：失败INIT：正在初始化|
|entities|Array of objects|Job操作的对象。根据不同Job类型，显示不同的内容。裸金属服务器相关操作显示server_id；网卡相关操作显示nic_id。请参见表4。|
|job_id|String|Job ID。|
|job_type|String|Job的类型，包含以下类型：baremetalSingleCreate：创建单个裸金属服务器baremetalSingleOperate：修改单个裸金属服务器电源状态|
|begin_time|String|开始时间。时间戳格式为ISO 8601，例如：2019-04-25T20:04:47.591Z|
|end_time|String|结束时间。时间戳格式为ISO 8601，例如：2019-04-26T20:04:47.591Z|
|error_code|String|Job执行失败时的错误码。|
|fail_reason|String|Job执行失败时的错误原因。|
|message|String|出现错误时，返回的错误消息。|
|code|String|出现错误时，返回的错误码。错误码和其对应的含义请参考状态码。|


    **表 4**  entities字段数据结构说明

|参数|参数类型|描述|
|--|--|--|
|server_id|String|裸金属服务器相关操作显示server_id。|
|nic_id|String|网卡相关操作显示nic_id。|


-   响应样例

    ```
    {
        "status": "SUCCESS",
        "entities": {
            "sub_jobs_total": 1,
            "sub_jobs": [
                {
                    "status": "SUCCESS",
                    "entities": {
                        "server_id": "bae51750-0089-41a1-9b18-5c777978ff6d"
                    },
                    "job_id": "2c9eb2c5544cbf6101544f0635672b60",
                    "job_type": "baremetalSingleCreate",
                    "begin_time": "2019-04-25T20:04:47.591Z",
                    "end_time": "2019-04-25T20:08:21.328Z",
                    "error_code": null,
                    "fail_reason": null
                }
            ]
        },
        "job_id": "2c9eb2c5544cbf6101544f0602af2b4f",
        "job_type": "baremetalBatchCreate",
        "begin_time": "2019-04-25T20:04:34.604Z",
        "end_time": "2019-04-25T20:08:41.593Z",
        "error_code": null,
        "fail_reason": null
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

