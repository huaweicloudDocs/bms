# 查询裸金属服务器是否存在标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060410930"></a>

## 功能介绍<a name="section66970384144623"></a>

查看裸金属服务器是否存在指定标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="section20295111144623"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table6300135020116)。

**表 1**  参数说明

<a name="table6300135020116"></a>
<table><thead align="left"><tr id="row6301650413"><th class="cellrowborder" valign="top" width="20.67206720672067%" id="mcps1.2.4.1.1"><p id="p29933752144623"><a name="p29933752144623"></a><a name="p29933752144623"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.902190219021904%" id="mcps1.2.4.1.2"><p id="p8714817144623"><a name="p8714817144623"></a><a name="p8714817144623"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="57.425742574257434%" id="mcps1.2.4.1.3"><p id="p34811538144623"><a name="p34811538144623"></a><a name="p34811538144623"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1830145014117"><td class="cellrowborder" valign="top" width="20.67206720672067%" headers="mcps1.2.4.1.1 "><p id="p27039406144623"><a name="p27039406144623"></a><a name="p27039406144623"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.902190219021904%" headers="mcps1.2.4.1.2 "><p id="p42708297144623"><a name="p42708297144623"></a><a name="p42708297144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="57.425742574257434%" headers="mcps1.2.4.1.3 "><p id="p36820045144623"><a name="p36820045144623"></a><a name="p36820045144623"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row030112504112"><td class="cellrowborder" valign="top" width="20.67206720672067%" headers="mcps1.2.4.1.1 "><p id="p65376104144623"><a name="p65376104144623"></a><a name="p65376104144623"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.902190219021904%" headers="mcps1.2.4.1.2 "><p id="p60973080144623"><a name="p60973080144623"></a><a name="p60973080144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="57.425742574257434%" headers="mcps1.2.4.1.3 "><p id="p39872428144623"><a name="p39872428144623"></a><a name="p39872428144623"></a><span id="text166801037185316"><a name="text166801037185316"></a><a name="text166801037185316"></a>裸金属服务器</span><span id="text96808374535"><a name="text96808374535"></a><a name="text96808374535"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row33016506115"><td class="cellrowborder" valign="top" width="20.67206720672067%" headers="mcps1.2.4.1.1 "><p id="p8862197144623"><a name="p8862197144623"></a><a name="p8862197144623"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="21.902190219021904%" headers="mcps1.2.4.1.2 "><p id="p46749363144623"><a name="p46749363144623"></a><a name="p46749363144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="57.425742574257434%" headers="mcps1.2.4.1.3 "><p id="p28602098144623"><a name="p28602098144623"></a><a name="p28602098144623"></a>待查询标签的key。</p>
<p id="p15688120112814"><a name="p15688120112814"></a><a name="p15688120112814"></a>约束：</p>
<a name="ul926591942418"></a><a name="ul926591942418"></a><ul id="ul926591942418"><li>中文或特殊字符需要进行URLEncode。</li><li>如果未指定标签的key，将返回该<span id="text1873714012533"><a name="text1873714012533"></a><a name="text1873714012533"></a>裸金属服务器</span><span id="text197378408537"><a name="text197378408537"></a><a name="text197378408537"></a></span>所有的标签。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section56092298144623"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/2d85af7c-cbfe-40c5-a378-4d03b42fb0e2/tags/{tag}
    ```


## 响应消息<a name="section21987090144623"></a>

如果存在指定标签，不涉及。

如果不存在指定标签，响应消息如下：

```
{
    "itemNotFound": {
        "message": "Server 2d85af7c-cbfe-40c5-a378-4d03b42fb0e2 has no tag 'abc'",
        "code": 404
    }
}
```

## 返回值<a name="section27037160"></a>

正常返回值：

<a name="zh-cn_topic_0053158659_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0053158659_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0053158659_p19735204616177"><a name="zh-cn_topic_0053158659_p19735204616177"></a><a name="zh-cn_topic_0053158659_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0053158659_p207355465176"><a name="zh-cn_topic_0053158659_p207355465176"></a><a name="zh-cn_topic_0053158659_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0053158659_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0053158659_p13735144611178"><a name="zh-cn_topic_0053158659_p13735144611178"></a><a name="zh-cn_topic_0053158659_p13735144611178"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0053158659_p81516575011"><a name="zh-cn_topic_0053158659_p81516575011"></a><a name="zh-cn_topic_0053158659_p81516575011"></a>服务器成功处理了请求，但没有返回任何内容。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

