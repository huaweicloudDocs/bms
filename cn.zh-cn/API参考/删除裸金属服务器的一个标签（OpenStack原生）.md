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
<table><thead align="left"><tr id="row55201745523"><th class="cellrowborder" valign="top" width="23.03230323032303%" id="mcps1.2.4.1.1"><p id="p67050730103718"><a name="p67050730103718"></a><a name="p67050730103718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.782478247824784%" id="mcps1.2.4.1.2"><p id="p55073076202321"><a name="p55073076202321"></a><a name="p55073076202321"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.185218521852185%" id="mcps1.2.4.1.3"><p id="p21237868103718"><a name="p21237868103718"></a><a name="p21237868103718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row165207451427"><td class="cellrowborder" valign="top" width="23.03230323032303%" headers="mcps1.2.4.1.1 "><p id="p23650911103718"><a name="p23650911103718"></a><a name="p23650911103718"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p36675672103718"><a name="p36675672103718"></a><a name="p36675672103718"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p17939461103718"><a name="p17939461103718"></a><a name="p17939461103718"></a>项目ID。</p>
</td>
</tr>
<tr id="row1752024519217"><td class="cellrowborder" valign="top" width="23.03230323032303%" headers="mcps1.2.4.1.1 "><p id="p18738546141829"><a name="p18738546141829"></a><a name="p18738546141829"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p41427238141829"><a name="p41427238141829"></a><a name="p41427238141829"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p163111141829"><a name="p163111141829"></a><a name="p163111141829"></a>裸金属服务器ID。</p>
</td>
</tr>
<tr id="row4520184517219"><td class="cellrowborder" valign="top" width="23.03230323032303%" headers="mcps1.2.4.1.1 "><p id="p54908755151432"><a name="p54908755151432"></a><a name="p54908755151432"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p18424196151432"><a name="p18424196151432"></a><a name="p18424196151432"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.185218521852185%" headers="mcps1.2.4.1.3 "><p id="p3844311810"><a name="p3844311810"></a><a name="p3844311810"></a>标签信息。</p>
<p id="p1648373542814"><a name="p1648373542814"></a><a name="p1648373542814"></a>约束：</p>
<a name="ul16436151718351"></a><a name="ul16436151718351"></a><ul id="ul16436151718351"><li>标签的长度不超过80个字符，标签中如果包含non-URL-safe的字符，要进行URLEncode。</li><li>如果未指定具体的标签key，将删除该裸金属服务器的所有标签。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section61879170105534"></a>

不涉及。

## 响应消息<a name="section33789573105534"></a>

不涉及。

## 返回值<a name="section6245741105534"></a>

请参考[通用返回值](通用返回值.md)。

