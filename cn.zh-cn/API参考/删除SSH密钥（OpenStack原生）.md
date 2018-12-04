# 删除SSH密钥（OpenStack原生）<a name="ZH-CN_TOPIC_0060384661"></a>

## 功能介绍<a name="section63429208111321"></a>

根据SSH密钥的名称，删除指定SSH密钥。

## URI<a name="section1885963111321"></a>

DELETE /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table155384213575)。

**表 1**  参数说明

<a name="table155384213575"></a>
<table><thead align="left"><tr id="row1561427572"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p7634079111321"><a name="p7634079111321"></a><a name="p7634079111321"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p14380623111321"><a name="p14380623111321"></a><a name="p14380623111321"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p23979787111321"><a name="p23979787111321"></a><a name="p23979787111321"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17561542205718"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p28210634111321"><a name="p28210634111321"></a><a name="p28210634111321"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p3360028111321"><a name="p3360028111321"></a><a name="p3360028111321"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p3726875111321"><a name="p3726875111321"></a><a name="p3726875111321"></a>项目ID。</p>
</td>
</tr>
<tr id="row45619423574"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p32537635111321"><a name="p32537635111321"></a><a name="p32537635111321"></a>keypair_name</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p18302768111321"><a name="p18302768111321"></a><a name="p18302768111321"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p6129221111321"><a name="p6129221111321"></a><a name="p6129221111321"></a>密钥名称。</p>
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

