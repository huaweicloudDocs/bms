# 查询裸金属服务器网卡信息（OpenStack原生）<a name="ZH-CN_TOPIC_0053158678"></a>

## 功能介绍<a name="section36073588"></a>

查询裸金属服务器网卡信息。

## URI<a name="section56226836"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-interface

参数说明请参见[表1](#table132771041114617)。

**表 1**  参数说明

<a name="table132771041114617"></a>
<table><thead align="left"><tr id="row8277114114465"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p27097356"><a name="p27097356"></a><a name="p27097356"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p47402253"><a name="p47402253"></a><a name="p47402253"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p14377323"><a name="p14377323"></a><a name="p14377323"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17277041134613"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p41666396"><a name="p41666396"></a><a name="p41666396"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p19534911"><a name="p19534911"></a><a name="p19534911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p38823967"><a name="p38823967"></a><a name="p38823967"></a>项目ID。</p>
</td>
</tr>
<tr id="row1127715418461"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p6481999114812"><a name="p6481999114812"></a><a name="p6481999114812"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p55279920114812"><a name="p55279920114812"></a><a name="p55279920114812"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p48488537114812"><a name="p48488537114812"></a><a name="p48488537114812"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section36279478"></a>

不涉及。

## 响应消息<a name="section58079852"></a>

-   响应参数

    <a name="table25276401"></a>
    <table><thead align="left"><tr id="row30840926"><th class="cellrowborder" valign="top" width="28.799999999999997%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.38%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.82%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13119252"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p56026474"><a name="p56026474"></a><a name="p56026474"></a>interfaceAttachments</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p34453949"><a name="p34453949"></a><a name="p34453949"></a>列表数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p18214233"><a name="p18214233"></a><a name="p18214233"></a>裸金属服务器网卡信息列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] interfaceAttachments字段数据结构说明

    <a name="table49805933"></a>
    <table><thead align="left"><tr id="row9026257"><th class="cellrowborder" valign="top" width="28.799999999999997%" id="mcps1.1.4.1.1"><p id="p1725119981520"><a name="p1725119981520"></a><a name="p1725119981520"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.38%" id="mcps1.1.4.1.2"><p id="p1725215901512"><a name="p1725215901512"></a><a name="p1725215901512"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.82%" id="mcps1.1.4.1.3"><p id="p1325513931517"><a name="p1325513931517"></a><a name="p1325513931517"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10727144"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p63592346"><a name="p63592346"></a><a name="p63592346"></a>port_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p13579756"><a name="p13579756"></a><a name="p13579756"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p34639550"><a name="p34639550"></a><a name="p34639550"></a>网卡端口状态。</p>
    </td>
    </tr>
    <tr id="row43320496"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p19299281"><a name="p19299281"></a><a name="p19299281"></a>fixed_ips</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p55265559"><a name="p55265559"></a><a name="p55265559"></a>列表数据结构[2]</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p23274750"><a name="p23274750"></a><a name="p23274750"></a>网卡私网IP信息列表。</p>
    </td>
    </tr>
    <tr id="row8146160"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p55859239"><a name="p55859239"></a><a name="p55859239"></a>net_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p10966323"><a name="p10966323"></a><a name="p10966323"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p8495130"><a name="p8495130"></a><a name="p8495130"></a>网卡端口所属网络ID。</p>
    </td>
    </tr>
    <tr id="row9347313"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p18934887"><a name="p18934887"></a><a name="p18934887"></a>port_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p13287175"><a name="p13287175"></a><a name="p13287175"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p22674843"><a name="p22674843"></a><a name="p22674843"></a>网卡端口ID。</p>
    </td>
    </tr>
    <tr id="row2747002"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.1.4.1.1 "><p id="p21180630"><a name="p21180630"></a><a name="p21180630"></a>mac_addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p50770908"><a name="p50770908"></a><a name="p50770908"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p35008393"><a name="p35008393"></a><a name="p35008393"></a>网卡Mac地址信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] fixed\_ips字段数据结构说明

    <a name="table19750463"></a>
    <table><thead align="left"><tr id="row60761195"><th class="cellrowborder" valign="top" width="29.18%" id="mcps1.1.4.1.1"><p id="p1975316192155"><a name="p1975316192155"></a><a name="p1975316192155"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.589999999999996%" id="mcps1.1.4.1.2"><p id="p9754171910158"><a name="p9754171910158"></a><a name="p9754171910158"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.230000000000004%" id="mcps1.1.4.1.3"><p id="p17562199153"><a name="p17562199153"></a><a name="p17562199153"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row61624137"><td class="cellrowborder" valign="top" width="29.18%" headers="mcps1.1.4.1.1 "><p id="p25499238"><a name="p25499238"></a><a name="p25499238"></a>subnet_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.589999999999996%" headers="mcps1.1.4.1.2 "><p id="p65213800"><a name="p65213800"></a><a name="p65213800"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.1.4.1.3 "><p id="p27784979"><a name="p27784979"></a><a name="p27784979"></a>网卡私网IP对应子网信息。</p>
    </td>
    </tr>
    <tr id="row48738220"><td class="cellrowborder" valign="top" width="29.18%" headers="mcps1.1.4.1.1 "><p id="p55481787"><a name="p55481787"></a><a name="p55481787"></a>ip_address</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.589999999999996%" headers="mcps1.1.4.1.2 "><p id="p17532027"><a name="p17532027"></a><a name="p17532027"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.1.4.1.3 "><p id="p30163672"><a name="p30163672"></a><a name="p30163672"></a>网卡私网IP信息。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "interfaceAttachments": [
            {
                "port_state": "ACTIVE",
                "fixed_ips": [
                    {
                        "subnet_id": "f8a6e8f8-c2ec-497c-9f23-da9616de54ef",
                        "ip_address": "192.168.1.3"
                    }
                ],
                "net_id": "3cb9bc59-5699-4588-a4b1-b87f96708bc6",
                "port_id": "ce531f90-199f-48c0-816c-13e38010b442",
                "mac_addr": "fa:16:3e:4c:2c:30"
            }
        ]
    }
    ```


## 返回值<a name="section52956621"></a>

请参考[通用返回值](通用返回值.md)。

