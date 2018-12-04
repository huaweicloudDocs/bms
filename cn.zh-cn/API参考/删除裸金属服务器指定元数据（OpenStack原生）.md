# 删除裸金属服务器指定元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0053158683"></a>

## 功能介绍<a name="section5520708185439"></a>

删除裸金属服务器指定元数据。

## 约束<a name="section5072450814374"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section65173692185439"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table12474435113619)。

**表 1**  参数说明

<a name="table12474435113619"></a>
<table><thead align="left"><tr id="row1947413503615"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p54886041185439"><a name="p54886041185439"></a><a name="p54886041185439"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p16584368185439"><a name="p16584368185439"></a><a name="p16584368185439"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p1156530185439"><a name="p1156530185439"></a><a name="p1156530185439"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16474735103610"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p4696221185439"><a name="p4696221185439"></a><a name="p4696221185439"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p44849621185439"><a name="p44849621185439"></a><a name="p44849621185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p8940698185439"><a name="p8940698185439"></a><a name="p8940698185439"></a>项目ID。</p>
</td>
</tr>
<tr id="row12474113573619"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p8209263185439"><a name="p8209263185439"></a><a name="p8209263185439"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p60970546185439"><a name="p60970546185439"></a><a name="p60970546185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p39667165185439"><a name="p39667165185439"></a><a name="p39667165185439"></a>裸金属服务器ID。</p>
</td>
</tr>
<tr id="row16474835173611"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p48209085185622"><a name="p48209085185622"></a><a name="p48209085185622"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p12621798185622"><a name="p12621798185622"></a><a name="p12621798185622"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p15732716185622"><a name="p15732716185622"></a><a name="p15732716185622"></a>待删除的裸金属服务器metadata键值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section21460169185439"></a>

不涉及。

## 响应消息<a name="section31286738185439"></a>

不涉及。

## 返回值<a name="section4253667185439"></a>

请参考[通用返回值](通用返回值.md)。

