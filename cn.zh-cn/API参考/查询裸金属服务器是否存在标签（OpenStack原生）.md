# 查询裸金属服务器是否存在标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060410930"></a>

## 功能介绍<a name="section66970384144623"></a>

查看裸金属服务器是否存在指定标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="section20295111144623"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags/\{tag\}

参数说明请参见[表1](#table6300135020116)。

**表 1**  参数说明

<a name="table6300135020116"></a>
<table><thead align="left"><tr id="row6301650413"><th class="cellrowborder" valign="top" width="24.892489248924893%" id="mcps1.2.4.1.1"><p id="p29933752144623"><a name="p29933752144623"></a><a name="p29933752144623"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.892489248924893%" id="mcps1.2.4.1.2"><p id="p8714817144623"><a name="p8714817144623"></a><a name="p8714817144623"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="50.215021502150215%" id="mcps1.2.4.1.3"><p id="p34811538144623"><a name="p34811538144623"></a><a name="p34811538144623"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1830145014117"><td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.1 "><p id="p27039406144623"><a name="p27039406144623"></a><a name="p27039406144623"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.2 "><p id="p42708297144623"><a name="p42708297144623"></a><a name="p42708297144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="50.215021502150215%" headers="mcps1.2.4.1.3 "><p id="p36820045144623"><a name="p36820045144623"></a><a name="p36820045144623"></a>项目ID。</p>
</td>
</tr>
<tr id="row030112504112"><td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.1 "><p id="p65376104144623"><a name="p65376104144623"></a><a name="p65376104144623"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.2 "><p id="p60973080144623"><a name="p60973080144623"></a><a name="p60973080144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="50.215021502150215%" headers="mcps1.2.4.1.3 "><p id="p39872428144623"><a name="p39872428144623"></a><a name="p39872428144623"></a>裸金属服务器ID。</p>
</td>
</tr>
<tr id="row33016506115"><td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.1 "><p id="p8862197144623"><a name="p8862197144623"></a><a name="p8862197144623"></a>tag</p>
</td>
<td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.2 "><p id="p46749363144623"><a name="p46749363144623"></a><a name="p46749363144623"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="50.215021502150215%" headers="mcps1.2.4.1.3 "><p id="p28602098144623"><a name="p28602098144623"></a><a name="p28602098144623"></a>待查询标签的key。</p>
<p id="p15688120112814"><a name="p15688120112814"></a><a name="p15688120112814"></a>约束：</p>
<a name="ul926591942418"></a><a name="ul926591942418"></a><ul id="ul926591942418"><li>中文或特殊字符需要进行URLEncode。</li><li>如果未指定标签的key，将返回该裸金属服务器所有的标签。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section56092298144623"></a>

不涉及。

## 响应消息<a name="section21987090144623"></a>

不涉及。

## 返回值<a name="section56679127144623"></a>

请参考[通用返回值](通用返回值.md)。

