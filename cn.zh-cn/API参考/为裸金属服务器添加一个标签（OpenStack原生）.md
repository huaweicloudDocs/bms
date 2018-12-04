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
<table><thead align="left"><tr id="row371913559014"><th class="cellrowborder" valign="top" width="26.862686268626863%" id="mcps1.2.4.1.1"><p id="p67050730103718"><a name="p67050730103718"></a><a name="p67050730103718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.402840284028404%" id="mcps1.2.4.1.2"><p id="p62400032103718"><a name="p62400032103718"></a><a name="p62400032103718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="44.73447344734473%" id="mcps1.2.4.1.3"><p id="p21237868103718"><a name="p21237868103718"></a><a name="p21237868103718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row207198551306"><td class="cellrowborder" valign="top" width="26.862686268626863%" headers="mcps1.2.4.1.1 "><p id="p23650911103718"><a name="p23650911103718"></a><a name="p23650911103718"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="28.402840284028404%" headers="mcps1.2.4.1.2 "><p id="p36675672103718"><a name="p36675672103718"></a><a name="p36675672103718"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.73447344734473%" headers="mcps1.2.4.1.3 "><p id="p17939461103718"><a name="p17939461103718"></a><a name="p17939461103718"></a>项目ID。</p>
</td>
</tr>
<tr id="row1871913551206"><td class="cellrowborder" valign="top" width="26.862686268626863%" headers="mcps1.2.4.1.1 "><p id="p18738546141829"><a name="p18738546141829"></a><a name="p18738546141829"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="28.402840284028404%" headers="mcps1.2.4.1.2 "><p id="p41427238141829"><a name="p41427238141829"></a><a name="p41427238141829"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.73447344734473%" headers="mcps1.2.4.1.3 "><p id="p163111141829"><a name="p163111141829"></a><a name="p163111141829"></a>裸金属服务器ID。</p>
</td>
</tr>
<tr id="row2071917554012"><td class="cellrowborder" valign="top" width="26.862686268626863%" headers="mcps1.2.4.1.1 "><p id="p66048515144318"><a name="p66048515144318"></a><a name="p66048515144318"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="28.402840284028404%" headers="mcps1.2.4.1.2 "><p id="p48329483144318"><a name="p48329483144318"></a><a name="p48329483144318"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.73447344734473%" headers="mcps1.2.4.1.3 "><p id="p133533233165"><a name="p133533233165"></a><a name="p133533233165"></a>标签信息。</p>
<p id="p6856153762712"><a name="p6856153762712"></a><a name="p6856153762712"></a>约束：</p>
<a name="ul31181225141619"></a><a name="ul31181225141619"></a><ul id="ul31181225141619"><li>标签的长度不超过80个字符。</li><li>标签不能以点“.”开头。</li><li>不支持创建空标签（空串）。</li><li>中文或特殊字符需要进行URLEncode。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section26704907111321"></a>

不涉及。

## 响应消息<a name="section6307065111321"></a>

不涉及。

## 返回值<a name="section34448272111321"></a>

请参考[通用返回值](通用返回值.md)。

