# 为裸金属服务器添加一个标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060410929"></a>

## 功能介绍<a name="section63429208111321"></a>

为裸金属服务器添加一个标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section26150540144115"></a>

-   tag个数不超过50个。
-   tag的长度不超过80个字符。
-   tag不能以点“.”开头。
-   不支持创建空tag（空串）。

>![](public_sys-resources/icon-note.gif) **说明：** 
>建议为裸金属服务器添加“\_\_type\_baremetal”标签，标识是一台裸金属服务器。

## URI<a name="section1885963111321"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table19718185512020)。

**表 1**  参数说明

<a name="table19718185512020"></a>
<table><thead align="left"><tr id="row371913559014"><th class="cellrowborder" valign="top" width="23.75237523752375%" id="mcps1.2.4.1.1"><p id="p67050730103718"><a name="p67050730103718"></a><a name="p67050730103718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.94239423942394%" id="mcps1.2.4.1.2"><p id="p62400032103718"><a name="p62400032103718"></a><a name="p62400032103718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.3052305230523%" id="mcps1.2.4.1.3"><p id="p21237868103718"><a name="p21237868103718"></a><a name="p21237868103718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row207198551306"><td class="cellrowborder" valign="top" width="23.75237523752375%" headers="mcps1.2.4.1.1 "><p id="p23650911103718"><a name="p23650911103718"></a><a name="p23650911103718"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.94239423942394%" headers="mcps1.2.4.1.2 "><p id="p36675672103718"><a name="p36675672103718"></a><a name="p36675672103718"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.3052305230523%" headers="mcps1.2.4.1.3 "><p id="p17939461103718"><a name="p17939461103718"></a><a name="p17939461103718"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row1871913551206"><td class="cellrowborder" valign="top" width="23.75237523752375%" headers="mcps1.2.4.1.1 "><p id="p18738546141829"><a name="p18738546141829"></a><a name="p18738546141829"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.94239423942394%" headers="mcps1.2.4.1.2 "><p id="p41427238141829"><a name="p41427238141829"></a><a name="p41427238141829"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.3052305230523%" headers="mcps1.2.4.1.3 "><p id="p163111141829"><a name="p163111141829"></a><a name="p163111141829"></a><span id="text718713247535"><a name="text718713247535"></a><a name="text718713247535"></a>裸金属服务器</span><span id="text1118792412539"><a name="text1118792412539"></a><a name="text1118792412539"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row2071917554012"><td class="cellrowborder" valign="top" width="23.75237523752375%" headers="mcps1.2.4.1.1 "><p id="p66048515144318"><a name="p66048515144318"></a><a name="p66048515144318"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="23.94239423942394%" headers="mcps1.2.4.1.2 "><p id="p48329483144318"><a name="p48329483144318"></a><a name="p48329483144318"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.3052305230523%" headers="mcps1.2.4.1.3 "><p id="p133533233165"><a name="p133533233165"></a><a name="p133533233165"></a>标签信息。</p>
<p id="p6856153762712"><a name="p6856153762712"></a><a name="p6856153762712"></a>约束：</p>
<a name="ul31181225141619"></a><a name="ul31181225141619"></a><ul id="ul31181225141619"><li>标签的长度不超过80个字符。</li><li>标签不能以点“.”开头。</li><li>不支持创建空标签（空串）。</li><li>中文或特殊字符需要进行URLEncode。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section26704907111321"></a>

-   请求参数

    无

-   请求样例

    ```
    PUT https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags/{tag}
    ```


## 响应消息<a name="section6307065111321"></a>

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

