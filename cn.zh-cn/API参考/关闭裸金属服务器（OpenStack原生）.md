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
<table><thead align="left"><tr id="row1697157163111"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p61356140"><a name="p61356140"></a><a name="p61356140"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p3791404"><a name="p3791404"></a><a name="p3791404"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p38668280"><a name="p38668280"></a><a name="p38668280"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1973711316"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p31084503"><a name="p31084503"></a><a name="p31084503"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p34816825"><a name="p34816825"></a><a name="p34816825"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1590600"><a name="p1590600"></a><a name="p1590600"></a>项目ID。</p>
</td>
</tr>
<tr id="row39716712314"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p18697032"><a name="p18697032"></a><a name="p18697032"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p38064613"><a name="p38064613"></a><a name="p38064613"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p63334794"><a name="p63334794"></a><a name="p63334794"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section42887128"></a>

-   请求参数

    <a name="table54550461"></a>
    <table><thead align="left"><tr id="row11842506"><th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.529999999999998%" id="mcps1.1.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.97%" id="mcps1.1.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="37.5%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row48896832"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.1 "><p id="p1220438"><a name="p1220438"></a><a name="p1220438"></a>os-stop</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.529999999999998%" headers="mcps1.1.5.1.2 "><p id="p21345065"><a name="p21345065"></a><a name="p21345065"></a>null或者字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.97%" headers="mcps1.1.5.1.3 "><p id="p1432442618145"><a name="p1432442618145"></a><a name="p1432442618145"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.5%" headers="mcps1.1.5.1.4 "><p id="p58405349"><a name="p58405349"></a><a name="p58405349"></a>标识关闭裸金属服务器操作。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] os-stop字段数据结构说明

    <a name="table10346346162744"></a>
    <table><thead align="left"><tr id="row45993853162744"><th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.1"><p id="p15821544165817"><a name="p15821544165817"></a><a name="p15821544165817"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22%" id="mcps1.1.5.1.2"><p id="p105851844185813"><a name="p105851844185813"></a><a name="p105851844185813"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.87%" id="mcps1.1.5.1.3"><p id="p1758610448586"><a name="p1758610448586"></a><a name="p1758610448586"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="37.13%" id="mcps1.1.5.1.4"><p id="p858711445580"><a name="p858711445580"></a><a name="p858711445580"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row41908639162744"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.1 "><p id="p39156593162744"><a name="p39156593162744"></a><a name="p39156593162744"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.2 "><p id="p13677446162744"><a name="p13677446162744"></a><a name="p13677446162744"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.1.5.1.3 "><p id="p5646265181336"><a name="p5646265181336"></a><a name="p5646265181336"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.13%" headers="mcps1.1.5.1.4 "><p id="p34131354162744"><a name="p34131354162744"></a><a name="p34131354162744"></a>关机类型：</p>
    <a name="ul1169415154044"></a><a name="ul1169415154044"></a><ul id="ul1169415154044"><li>SOFT：普通关机。</li><li>HARD：强制关机。<div class="note" id="note3080306151059"><a name="note3080306151059"></a><a name="note3080306151059"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p27722756151059"><a name="p27722756151059"></a><a name="p27722756151059"></a>当前该参数无效，即均为强制关机。</p>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    {
        "os-stop": {}
    }
    ```


## 响应消息<a name="section50439840"></a>

不涉及。

## 返回值<a name="section51305376"></a>

请参考[通用返回值](通用返回值.md)。

