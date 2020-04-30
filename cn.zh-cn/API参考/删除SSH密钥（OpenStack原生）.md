# 删除SSH密钥（OpenStack原生）<a name="ZH-CN_TOPIC_0060384661"></a>

## 功能介绍<a name="section63429208111321"></a>

根据SSH密钥的名称，删除指定SSH密钥。

## URI<a name="section1885963111321"></a>

DELETE /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table155384213575)。

**表 1**  参数说明

<a name="table155384213575"></a>
<table><thead align="left"><tr id="row1561427572"><th class="cellrowborder" valign="top" width="24.21242124212421%" id="mcps1.2.4.1.1"><p id="p7634079111321"><a name="p7634079111321"></a><a name="p7634079111321"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.952395239523952%" id="mcps1.2.4.1.2"><p id="p14380623111321"><a name="p14380623111321"></a><a name="p14380623111321"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.83518351835183%" id="mcps1.2.4.1.3"><p id="p23979787111321"><a name="p23979787111321"></a><a name="p23979787111321"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17561542205718"><td class="cellrowborder" valign="top" width="24.21242124212421%" headers="mcps1.2.4.1.1 "><p id="p28210634111321"><a name="p28210634111321"></a><a name="p28210634111321"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.952395239523952%" headers="mcps1.2.4.1.2 "><p id="p3360028111321"><a name="p3360028111321"></a><a name="p3360028111321"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.83518351835183%" headers="mcps1.2.4.1.3 "><p id="p3726875111321"><a name="p3726875111321"></a><a name="p3726875111321"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row45619423574"><td class="cellrowborder" valign="top" width="24.21242124212421%" headers="mcps1.2.4.1.1 "><p id="p32537635111321"><a name="p32537635111321"></a><a name="p32537635111321"></a>keypair_name</p>
</td>
<td class="cellrowborder" valign="top" width="23.952395239523952%" headers="mcps1.2.4.1.2 "><p id="p18302768111321"><a name="p18302768111321"></a><a name="p18302768111321"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.83518351835183%" headers="mcps1.2.4.1.3 "><p id="p6129221111321"><a name="p6129221111321"></a><a name="p6129221111321"></a>密钥名称。</p>
<p id="p1345123817411"><a name="p1345123817411"></a><a name="p1345123817411"></a>可以通过<a href="查询SSH密钥列表（OpenStack原生）.md">查询SSH密钥列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section26704907111321"></a>

-   请求参数

    无

-   请求样例

    ```
    DELETE https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/os-keypairs/keypair-test
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

