# 删除裸金属服务器指定元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0053158683"></a>

## 功能介绍<a name="section5520708185439"></a>

删除裸金属服务器指定元数据。

## 约束<a name="section5072450814374"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active、stopped、paused或者suspended。

## URI<a name="section65173692185439"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table12474435113619)。

**表 1**  参数说明

<a name="table12474435113619"></a>
<table><thead align="left"><tr id="row1947413503615"><th class="cellrowborder" valign="top" width="25.662566256625663%" id="mcps1.2.4.1.1"><p id="p54886041185439"><a name="p54886041185439"></a><a name="p54886041185439"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.93259325932593%" id="mcps1.2.4.1.2"><p id="p16584368185439"><a name="p16584368185439"></a><a name="p16584368185439"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.4048404840484%" id="mcps1.2.4.1.3"><p id="p1156530185439"><a name="p1156530185439"></a><a name="p1156530185439"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16474735103610"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p4696221185439"><a name="p4696221185439"></a><a name="p4696221185439"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.93259325932593%" headers="mcps1.2.4.1.2 "><p id="p44849621185439"><a name="p44849621185439"></a><a name="p44849621185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.4048404840484%" headers="mcps1.2.4.1.3 "><p id="p8940698185439"><a name="p8940698185439"></a><a name="p8940698185439"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row12474113573619"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p8209263185439"><a name="p8209263185439"></a><a name="p8209263185439"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.93259325932593%" headers="mcps1.2.4.1.2 "><p id="p60970546185439"><a name="p60970546185439"></a><a name="p60970546185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.4048404840484%" headers="mcps1.2.4.1.3 "><p id="p39667165185439"><a name="p39667165185439"></a><a name="p39667165185439"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从裸金属服务器控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row16474835173611"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p48209085185622"><a name="p48209085185622"></a><a name="p48209085185622"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="25.93259325932593%" headers="mcps1.2.4.1.2 "><p id="p12621798185622"><a name="p12621798185622"></a><a name="p12621798185622"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.4048404840484%" headers="mcps1.2.4.1.3 "><p id="p15732716185622"><a name="p15732716185622"></a><a name="p15732716185622"></a>待删除的裸金属服务器metadata键值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section21460169185439"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata/{key}
    ```


## 响应消息<a name="section31286738185439"></a>

不涉及。

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

