# 任务ID的响应<a name="bms_api_0805"></a>

## 正常响应要素<a name="section19736153983212"></a>

**表 1**  正常响应要素说明

|名称|参数类型|说明|
|--|--|--|
|job_id|String|提交任务成功后返回的任务ID，用户可以使用该ID对任务执行情况进行查询。如何根据job_id来查询Job的执行状态，请参考查询Job状态。|


## 异常响应要素<a name="section179521572336"></a>

**表 2**  异常响应要素说明

|名称|参数类型|说明|
|--|--|--|
|error|字典数据结构|提交任务异常时返回的异常信息，详情请参见表1 error数据结构。|


**表 3**  error数据结构

|名称|参数类型|说明|
|--|--|--|
|message|String|任务异常错误信息描述。|
|code|String|任务异常错误信息编码。|


## 响应样例<a name="section19874359153411"></a>

-   正常响应

    ```
    { 
        "job_id": "70a599e0-31e7-49b7-b260-868f441e862b" 
    } 
    ```

-   异常响应

    ```
    { 
        "error": {"message": "", "code": XXX}
    } 
    ```


