# 查询裸金属服务器挂载的单个云硬盘信息（OpenStack原生）<a name="ZH-CN_TOPIC_0053158665"></a>

## 功能介绍<a name="section21764736"></a>

根据磁盘ID，查询裸金属服务器挂载的单个云硬盘信息。

## URI<a name="section61664903"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-volume\_attachments/\{volume\_id\}

参数说明请参见[表1](#table17269134917502)。

**表 1**  参数说明

<a name="table17269134917502"></a>
<table><thead align="left"><tr id="row127284919508"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p52189740"><a name="p52189740"></a><a name="p52189740"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p66619401"><a name="p66619401"></a><a name="p66619401"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p27462382"><a name="p27462382"></a><a name="p27462382"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5272549205014"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p3763337517142"><a name="p3763337517142"></a><a name="p3763337517142"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p2840453517142"><a name="p2840453517142"></a><a name="p2840453517142"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1906601217142"><a name="p1906601217142"></a><a name="p1906601217142"></a>项目ID。</p>
</td>
</tr>
<tr id="row92726495508"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p2068039117144"><a name="p2068039117144"></a><a name="p2068039117144"></a>volume_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6449900717144"><a name="p6449900717144"></a><a name="p6449900717144"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p5703706317144"><a name="p5703706317144"></a><a name="p5703706317144"></a>磁盘ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section18113219"></a>

不涉及。

## 响应消息<a name="section28801245"></a>

-   响应参数

    <a name="table769899"></a>
    <table><thead align="left"><tr id="row6968742"><th class="cellrowborder" valign="top" width="28.4%" id="mcps1.1.4.1.1"><p id="p19987085"><a name="p19987085"></a><a name="p19987085"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.69%" id="mcps1.1.4.1.2"><p id="p4546697"><a name="p4546697"></a><a name="p4546697"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.910000000000004%" id="mcps1.1.4.1.3"><p id="p32738149"><a name="p32738149"></a><a name="p32738149"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13299239"><td class="cellrowborder" valign="top" width="28.4%" headers="mcps1.1.4.1.1 "><p id="p3496541"><a name="p3496541"></a><a name="p3496541"></a>volumeAttachment</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.69%" headers="mcps1.1.4.1.2 "><p id="p56686067"><a name="p56686067"></a><a name="p56686067"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.910000000000004%" headers="mcps1.1.4.1.3 "><p id="p52192065"><a name="p52192065"></a><a name="p52192065"></a>裸金属服务器挂载信息列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] volumeAttachment字段数据结构说明

    <a name="table42716605"></a>
    <table><thead align="left"><tr id="row6429"><th class="cellrowborder" valign="top" width="28.050000000000004%" id="mcps1.1.4.1.1"><p id="p144716112213"><a name="p144716112213"></a><a name="p144716112213"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.39%" id="mcps1.1.4.1.2"><p id="p184476111218"><a name="p184476111218"></a><a name="p184476111218"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.56%" id="mcps1.1.4.1.3"><p id="p0448211142115"><a name="p0448211142115"></a><a name="p0448211142115"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54793251"><td class="cellrowborder" valign="top" width="28.050000000000004%" headers="mcps1.1.4.1.1 "><p id="p9068361"><a name="p9068361"></a><a name="p9068361"></a>device</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.2 "><p id="p39066822"><a name="p39066822"></a><a name="p39066822"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.56%" headers="mcps1.1.4.1.3 "><p id="p25555552"><a name="p25555552"></a><a name="p25555552"></a>挂载目录。</p>
    </td>
    </tr>
    <tr id="row28673382"><td class="cellrowborder" valign="top" width="28.050000000000004%" headers="mcps1.1.4.1.1 "><p id="p40842582"><a name="p40842582"></a><a name="p40842582"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.2 "><p id="p2490560"><a name="p2490560"></a><a name="p2490560"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.56%" headers="mcps1.1.4.1.3 "><p id="p3679585"><a name="p3679585"></a><a name="p3679585"></a>挂载资源ID。</p>
    </td>
    </tr>
    <tr id="row33116269"><td class="cellrowborder" valign="top" width="28.050000000000004%" headers="mcps1.1.4.1.1 "><p id="p65172112"><a name="p65172112"></a><a name="p65172112"></a>serverId</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.2 "><p id="p43655223"><a name="p43655223"></a><a name="p43655223"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.56%" headers="mcps1.1.4.1.3 "><p id="p15056362"><a name="p15056362"></a><a name="p15056362"></a>所属裸金属服务器ID。</p>
    </td>
    </tr>
    <tr id="row1289536"><td class="cellrowborder" valign="top" width="28.050000000000004%" headers="mcps1.1.4.1.1 "><p id="p37343614"><a name="p37343614"></a><a name="p37343614"></a>volumeId</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.2 "><p id="p64098994"><a name="p64098994"></a><a name="p64098994"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.56%" headers="mcps1.1.4.1.3 "><p id="p20397636"><a name="p20397636"></a><a name="p20397636"></a>挂载云磁盘ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "volumeAttachment": {
            "device": "/dev/vdb",
            "serverId": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa",
            "id": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6",
            "volumeId": "b53f23bd-ee8f-49ec-9420-d1acfeaf91d6"
        }
    }
    ```


## 返回值<a name="section57884614"></a>

请参考[通用返回值](通用返回值.md)。

