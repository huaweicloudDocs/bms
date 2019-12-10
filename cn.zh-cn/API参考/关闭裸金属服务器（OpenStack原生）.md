# 关闭裸金属服务器（OpenStack原生）<a name="ZH-CN_TOPIC_0053158685"></a>

## 功能介绍<a name="section32841145"></a>

关闭单台裸金属服务器。

## 约束<a name="section57278039123222"></a>

-   裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active或error。
-   当前仅支持强制关闭。

## URI<a name="section27134857"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table1997078319)。

**表 1**  参数说明

<a name="table1997078319"></a>
<table><thead align="left"><tr id="row1697157163111"><th class="cellrowborder" valign="top" width="24.492449244924494%" id="mcps1.2.4.1.1"><p id="p61356140"><a name="p61356140"></a><a name="p61356140"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.96229622962296%" id="mcps1.2.4.1.2"><p id="p3791404"><a name="p3791404"></a><a name="p3791404"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.54525452545254%" id="mcps1.2.4.1.3"><p id="p38668280"><a name="p38668280"></a><a name="p38668280"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1973711316"><td class="cellrowborder" valign="top" width="24.492449244924494%" headers="mcps1.2.4.1.1 "><p id="p31084503"><a name="p31084503"></a><a name="p31084503"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.96229622962296%" headers="mcps1.2.4.1.2 "><p id="p34816825"><a name="p34816825"></a><a name="p34816825"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.54525452545254%" headers="mcps1.2.4.1.3 "><p id="p1590600"><a name="p1590600"></a><a name="p1590600"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row39716712314"><td class="cellrowborder" valign="top" width="24.492449244924494%" headers="mcps1.2.4.1.1 "><p id="p18697032"><a name="p18697032"></a><a name="p18697032"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.96229622962296%" headers="mcps1.2.4.1.2 "><p id="p38064613"><a name="p38064613"></a><a name="p38064613"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.54525452545254%" headers="mcps1.2.4.1.3 "><p id="p63334794"><a name="p63334794"></a><a name="p63334794"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从裸金属服务器控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section42887128"></a>

-   请求参数

    <a name="table54550461"></a>
    <table><thead align="left"><tr id="row11842506"><th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.529999999999998%" id="mcps1.1.5.1.2"><p id="p183901830522"><a name="p183901830522"></a><a name="p183901830522"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.97%" id="mcps1.1.5.1.3"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="37.5%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row48896832"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.1 "><p id="p1220438"><a name="p1220438"></a><a name="p1220438"></a>os-stop</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.529999999999998%" headers="mcps1.1.5.1.2 "><p id="p0389123016219"><a name="p0389123016219"></a><a name="p0389123016219"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.97%" headers="mcps1.1.5.1.3 "><p id="p21345065"><a name="p21345065"></a><a name="p21345065"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.5%" headers="mcps1.1.5.1.4 "><p id="p58405349"><a name="p58405349"></a><a name="p58405349"></a>标识关闭裸金属服务器操作。详情请参见<a href="#table10346346162744">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  os-stop字段数据结构说明

    <a name="table10346346162744"></a>
    <table><thead align="left"><tr id="row45993853162744"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.1"><p id="p15821544165817"><a name="p15821544165817"></a><a name="p15821544165817"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.2"><p id="p16821737324"><a name="p16821737324"></a><a name="p16821737324"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.5.1.3"><p id="p105851844185813"><a name="p105851844185813"></a><a name="p105851844185813"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="37.13%" id="mcps1.2.5.1.4"><p id="p858711445580"><a name="p858711445580"></a><a name="p858711445580"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row41908639162744"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p39156593162744"><a name="p39156593162744"></a><a name="p39156593162744"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.2 "><p id="p76815371823"><a name="p76815371823"></a><a name="p76815371823"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.5.1.3 "><p id="p13677446162744"><a name="p13677446162744"></a><a name="p13677446162744"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.13%" headers="mcps1.2.5.1.4 "><p id="p34131354162744"><a name="p34131354162744"></a><a name="p34131354162744"></a>关机类型：</p>
    <a name="ul1169415154044"></a><a name="ul1169415154044"></a><ul id="ul1169415154044"><li>SOFT：普通关机。</li><li>HARD：强制关机。<div class="note" id="note3080306151059"><a name="note3080306151059"></a><a name="note3080306151059"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p27722756151059"><a name="p27722756151059"></a><a name="p27722756151059"></a>当前该参数无效，即均为强制关机。</p>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    POST https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/action
    ```

    ```
    {
        "os-stop": {}
    }
    ```


## 响应消息<a name="section50439840"></a>

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

