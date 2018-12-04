# 重启裸金属服务器（OpenStack原生）<a name="ZH-CN_TOPIC_0053158716"></a>

## 功能介绍<a name="section6488958"></a>

重启单台裸金属服务器。

## 约束<a name="section57278039123222"></a>

当前仅支持强制重启。

## URI<a name="section58400626"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table6943612162916)。

**表 1**  参数说明

<a name="table6943612162916"></a>
<table><thead align="left"><tr id="row1694351213299"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p17522362913"><a name="p17522362913"></a><a name="p17522362913"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p5642312299"><a name="p5642312299"></a><a name="p5642312299"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p1391023202918"><a name="p1391023202918"></a><a name="p1391023202918"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5943201292911"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p71132302912"><a name="p71132302912"></a><a name="p71132302912"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p91472372914"><a name="p91472372914"></a><a name="p91472372914"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p19165231293"><a name="p19165231293"></a><a name="p19165231293"></a>项目ID。</p>
</td>
</tr>
<tr id="row794311252918"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p318162392918"><a name="p318162392918"></a><a name="p318162392918"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1119162362913"><a name="p1119162362913"></a><a name="p1119162362913"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p192032314291"><a name="p192032314291"></a><a name="p192032314291"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section55843593"></a>

-   请求参数

    <a name="table37818817"></a>
    <table><thead align="left"><tr id="row57787318"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.21782178217822%" id="mcps1.1.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.306930693069308%" id="mcps1.1.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.47524752475247%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13875810"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.1 "><p id="p50198807"><a name="p50198807"></a><a name="p50198807"></a>reboot</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.21782178217822%" headers="mcps1.1.5.1.2 "><p id="p51181499"><a name="p51181499"></a><a name="p51181499"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.306930693069308%" headers="mcps1.1.5.1.3 "><p id="p38807254181114"><a name="p38807254181114"></a><a name="p38807254181114"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.47524752475247%" headers="mcps1.1.5.1.4 "><p id="p65893970"><a name="p65893970"></a><a name="p65893970"></a>标记为重启裸金属服务器操作。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] reboot字段数据结构说明

    <a name="table10346346162744"></a>
    <table><thead align="left"><tr id="row45993853162744"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.5.1.1"><p id="p85714617589"><a name="p85714617589"></a><a name="p85714617589"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.48%" id="mcps1.1.5.1.2"><p id="p1759116115816"><a name="p1759116115816"></a><a name="p1759116115816"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.380000000000003%" id="mcps1.1.5.1.3"><p id="p25916685817"><a name="p25916685817"></a><a name="p25916685817"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.14%" id="mcps1.1.5.1.4"><p id="p5615615814"><a name="p5615615814"></a><a name="p5615615814"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row41908639162744"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.1 "><p id="p39156593162744"><a name="p39156593162744"></a><a name="p39156593162744"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.48%" headers="mcps1.1.5.1.2 "><p id="p13677446162744"><a name="p13677446162744"></a><a name="p13677446162744"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.380000000000003%" headers="mcps1.1.5.1.3 "><p id="p63270434181210"><a name="p63270434181210"></a><a name="p63270434181210"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.14%" headers="mcps1.1.5.1.4 "><p id="p34131354162744"><a name="p34131354162744"></a><a name="p34131354162744"></a>重启类型：</p>
    <a name="ul1169415154044"></a><a name="ul1169415154044"></a><ul id="ul1169415154044"><li>SOFT：普通重启。</li><li>HARD：强制重启。<div class="note" id="note3080306151059"><a name="note3080306151059"></a><a name="note3080306151059"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p27722756151059"><a name="p27722756151059"></a><a name="p27722756151059"></a>当前SOFT参数无效，即均为强制重启。</p>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    {
        "reboot": {
            "type": "HARD"
        }
    }
    ```


## 响应消息<a name="section32830290"></a>

不涉及。

## 返回值<a name="section27037160"></a>

请参考[通用返回值](通用返回值.md)。

