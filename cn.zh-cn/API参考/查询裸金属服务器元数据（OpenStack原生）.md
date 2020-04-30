# 查询裸金属服务器元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0060402469"></a>

## 功能介绍<a name="section61558535185333"></a>

裸金属服务器元数据包含了裸金属服务器在云平台的基本信息，例如服务器ID、主机名、网络信息等。通过该接口，您可以查询裸金属服务器的元数据。

## 约束<a name="section57278039123222"></a>

不支持分页查询。

## URI<a name="section47451206185333"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table3831319143216)。

**表 1**  参数说明

<a name="table3831319143216"></a>
<table><thead align="left"><tr id="row38322019153219"><th class="cellrowborder" valign="top" width="24.972497249724974%" id="mcps1.2.4.1.1"><p id="p49662088185333"><a name="p49662088185333"></a><a name="p49662088185333"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.27272727272727%" id="mcps1.2.4.1.2"><p id="p63206191185333"><a name="p63206191185333"></a><a name="p63206191185333"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47.75477547754775%" id="mcps1.2.4.1.3"><p id="p19427838185333"><a name="p19427838185333"></a><a name="p19427838185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15832181913211"><td class="cellrowborder" valign="top" width="24.972497249724974%" headers="mcps1.2.4.1.1 "><p id="p26317623185333"><a name="p26317623185333"></a><a name="p26317623185333"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.2.4.1.2 "><p id="p51352688185333"><a name="p51352688185333"></a><a name="p51352688185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.75477547754775%" headers="mcps1.2.4.1.3 "><p id="p65927025185333"><a name="p65927025185333"></a><a name="p65927025185333"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row78321619103218"><td class="cellrowborder" valign="top" width="24.972497249724974%" headers="mcps1.2.4.1.1 "><p id="p10854909185333"><a name="p10854909185333"></a><a name="p10854909185333"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.2.4.1.2 "><p id="p6832475185333"><a name="p6832475185333"></a><a name="p6832475185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.75477547754775%" headers="mcps1.2.4.1.3 "><p id="p16559613185333"><a name="p16559613185333"></a><a name="p16559613185333"></a><span id="text956081517186"><a name="text956081517186"></a><a name="text956081517186"></a>裸金属服务器</span><span id="text11560151581814"><a name="text11560151581814"></a><a name="text11560151581814"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section14818796185333"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata
    ```


## 响应消息<a name="section22254218185333"></a>

-   响应参数

    <a name="table48150236185333"></a>
    <table><thead align="left"><tr id="row64499137185333"><th class="cellrowborder" valign="top" width="22.259999999999998%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.24%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.50000000000001%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row51055328185333"><td class="cellrowborder" valign="top" width="22.259999999999998%" headers="mcps1.1.4.1.1 "><p id="p41840919185333"><a name="p41840919185333"></a><a name="p41840919185333"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.1.4.1.2 "><p id="p33671307185333"><a name="p33671307185333"></a><a name="p33671307185333"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.50000000000001%" headers="mcps1.1.4.1.3 "><p id="p51647808185333"><a name="p51647808185333"></a><a name="p51647808185333"></a>用户自定义metadata键值对。详情请参见<a href="#table22722954185333">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  metadata字段数据结构说明

    <a name="table22722954185333"></a>
    <table><thead align="left"><tr id="row5305371185333"><th class="cellrowborder" valign="top" width="22.957704229577043%" id="mcps1.2.4.1.1"><p id="p1640481205915"><a name="p1640481205915"></a><a name="p1640481205915"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.467853214678534%" id="mcps1.2.4.1.2"><p id="p1440581220594"><a name="p1440581220594"></a><a name="p1440581220594"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.57444255574442%" id="mcps1.2.4.1.3"><p id="p1340841217596"><a name="p1340841217596"></a><a name="p1340841217596"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2696702185333"><td class="cellrowborder" valign="top" width="22.957704229577043%" headers="mcps1.2.4.1.1 "><p id="p17106284185333"><a name="p17106284185333"></a><a name="p17106284185333"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.467853214678534%" headers="mcps1.2.4.1.2 "><p id="p43431730185333"><a name="p43431730185333"></a><a name="p43431730185333"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57444255574442%" headers="mcps1.2.4.1.3 "><p id="p5719410617654"><a name="p5719410617654"></a><a name="p5719410617654"></a>metadata键、值。</p>
    <p id="p4498490617654"><a name="p4498490617654"></a><a name="p4498490617654"></a>键、值长度均不大于255字节。</p>
    </td>
    </tr>
    </tbody>
    </table>

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

<a name="zh-cn_topic_0106040941_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0106040941_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0106040941_p19735204616177"><a name="zh-cn_topic_0106040941_p19735204616177"></a><a name="zh-cn_topic_0106040941_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0106040941_p207355465176"><a name="zh-cn_topic_0106040941_p207355465176"></a><a name="zh-cn_topic_0106040941_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0106040941_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0106040941_p13735144611178"><a name="zh-cn_topic_0106040941_p13735144611178"></a><a name="zh-cn_topic_0106040941_p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0106040941_p207351246161711"><a name="zh-cn_topic_0106040941_p207351246161711"></a><a name="zh-cn_topic_0106040941_p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

