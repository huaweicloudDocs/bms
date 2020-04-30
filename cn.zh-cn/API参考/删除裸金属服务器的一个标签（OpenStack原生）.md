# 删除裸金属服务器的一个标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060424486"></a>

## 功能介绍<a name="section46928615105534"></a>

删除裸金属服务器的一个标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section11729622194315"></a>

-   tag的长度不超过80个字符。
-   tag中如果包含non-URL-safe的字符，要进行URLEncode。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   “\_\_type\_baremetal”标识是一台裸金属服务器，建议不要删除“\_\_type\_baremetal”标签，否则，裸金属服务器将仅在ECS控制台可见，而不在BMS控制台中。  
>-   “\_\_type\_baremetal”删除后可通过[为裸金属服务器添加一个标签（OpenStack原生）](为裸金属服务器添加一个标签（OpenStack原生）.md)进行重新添加，添加后裸金属服务器会重新显示在BMS的控制台。  

## URI<a name="section3181044105534"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table105191945325)。

**表 1**  参数说明

<a name="table105191945325"></a>
<table><thead align="left"><tr id="row55201745523"><th class="cellrowborder" valign="top" width="24.18241824182418%" id="mcps1.2.4.1.1"><p id="p67050730103718"><a name="p67050730103718"></a><a name="p67050730103718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.632363236323634%" id="mcps1.2.4.1.2"><p id="p55073076202321"><a name="p55073076202321"></a><a name="p55073076202321"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.185218521852185%" id="mcps1.2.4.1.3"><p id="p21237868103718"><a name="p21237868103718"></a><a name="p21237868103718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row165207451427"><td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.2.4.1.1 "><p id="p23650911103718"><a name="p23650911103718"></a><a name="p23650911103718"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.632363236323634%" headers="mcps1.2.4.1.2 "><p id="p36675672103718"><a name="p36675672103718"></a><a name="p36675672103718"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p17939461103718"><a name="p17939461103718"></a><a name="p17939461103718"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row1752024519217"><td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.2.4.1.1 "><p id="p18738546141829"><a name="p18738546141829"></a><a name="p18738546141829"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.632363236323634%" headers="mcps1.2.4.1.2 "><p id="p41427238141829"><a name="p41427238141829"></a><a name="p41427238141829"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p163111141829"><a name="p163111141829"></a><a name="p163111141829"></a><span id="text20850214549"><a name="text20850214549"></a><a name="text20850214549"></a>裸金属服务器</span><span id="text138509110546"><a name="text138509110546"></a><a name="text138509110546"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row4520184517219"><td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.2.4.1.1 "><p id="p54908755151432"><a name="p54908755151432"></a><a name="p54908755151432"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="23.632363236323634%" headers="mcps1.2.4.1.2 "><p id="p18424196151432"><a name="p18424196151432"></a><a name="p18424196151432"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p3844311810"><a name="p3844311810"></a><a name="p3844311810"></a>标签信息。</p>
<p id="p1648373542814"><a name="p1648373542814"></a><a name="p1648373542814"></a>约束：</p>
<a name="ul16436151718351"></a><a name="ul16436151718351"></a><ul id="ul16436151718351"><li>标签的长度不超过80个字符，标签中如果包含non-URL-safe的字符，要进行URLEncode。</li><li>如果未指定具体的标签key，将删除该<span id="text14203744549"><a name="text14203744549"></a><a name="text14203744549"></a>裸金属服务器</span><span id="text62039475411"><a name="text62039475411"></a><a name="text62039475411"></a></span>的所有标签。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section61879170105534"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/53206ed0-56de-4d6b-b7ee-ffc62ca26f43/tags/{tag}
    ```


## 响应消息<a name="section33789573105534"></a>

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

