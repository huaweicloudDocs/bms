# 查询裸金属服务器网卡信息（OpenStack原生）<a name="ZH-CN_TOPIC_0053158678"></a>

## 功能介绍<a name="section36073588"></a>

查询裸金属服务器的网卡信息，比如网卡的MAC地址、私网IP信息。

## URI<a name="section56226836"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-interface

参数说明请参见[表1](#table132771041114617)。

**表 1**  参数说明

<a name="table132771041114617"></a>
<table><thead align="left"><tr id="row8277114114465"><th class="cellrowborder" valign="top" width="24.682468246824683%" id="mcps1.2.4.1.1"><p id="p27097356"><a name="p27097356"></a><a name="p27097356"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.24252425242524%" id="mcps1.2.4.1.2"><p id="p47402253"><a name="p47402253"></a><a name="p47402253"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="50.07500750075008%" id="mcps1.2.4.1.3"><p id="p14377323"><a name="p14377323"></a><a name="p14377323"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17277041134613"><td class="cellrowborder" valign="top" width="24.682468246824683%" headers="mcps1.2.4.1.1 "><p id="p41666396"><a name="p41666396"></a><a name="p41666396"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.24252425242524%" headers="mcps1.2.4.1.2 "><p id="p19534911"><a name="p19534911"></a><a name="p19534911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="50.07500750075008%" headers="mcps1.2.4.1.3 "><p id="p38823967"><a name="p38823967"></a><a name="p38823967"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row1127715418461"><td class="cellrowborder" valign="top" width="24.682468246824683%" headers="mcps1.2.4.1.1 "><p id="p6481999114812"><a name="p6481999114812"></a><a name="p6481999114812"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.24252425242524%" headers="mcps1.2.4.1.2 "><p id="p55279920114812"><a name="p55279920114812"></a><a name="p55279920114812"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="50.07500750075008%" headers="mcps1.2.4.1.3 "><p id="p48488537114812"><a name="p48488537114812"></a><a name="p48488537114812"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从裸金属服务器控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section36279478"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/os-interface
    ```


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
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.1.4.1.2 "><p id="p34453949"><a name="p34453949"></a><a name="p34453949"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.1.4.1.3 "><p id="p18214233"><a name="p18214233"></a><a name="p18214233"></a>裸金属服务器网卡信息列表。详情请参见<a href="#table49805933">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  interfaceAttachments字段数据结构说明

    <a name="table49805933"></a>
    <table><thead align="left"><tr id="row9026257"><th class="cellrowborder" valign="top" width="28.799999999999997%" id="mcps1.2.4.1.1"><p id="p1725119981520"><a name="p1725119981520"></a><a name="p1725119981520"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.38%" id="mcps1.2.4.1.2"><p id="p1725215901512"><a name="p1725215901512"></a><a name="p1725215901512"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.82%" id="mcps1.2.4.1.3"><p id="p1325513931517"><a name="p1325513931517"></a><a name="p1325513931517"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10727144"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.2.4.1.1 "><p id="p63592346"><a name="p63592346"></a><a name="p63592346"></a>port_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.2.4.1.2 "><p id="p13579756"><a name="p13579756"></a><a name="p13579756"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.2.4.1.3 "><p id="p34639550"><a name="p34639550"></a><a name="p34639550"></a>网卡端口状态，取值为：<span>ACTIVE、BUILD、DOWN。</span></p>
    </td>
    </tr>
    <tr id="row43320496"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.2.4.1.1 "><p id="p19299281"><a name="p19299281"></a><a name="p19299281"></a>fixed_ips</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.2.4.1.2 "><p id="p55265559"><a name="p55265559"></a><a name="p55265559"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.2.4.1.3 "><p id="p23274750"><a name="p23274750"></a><a name="p23274750"></a>网卡私网IP信息列表。详情请参见<a href="#table19750463">表3</a>。</p>
    </td>
    </tr>
    <tr id="row8146160"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.2.4.1.1 "><p id="p55859239"><a name="p55859239"></a><a name="p55859239"></a>net_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.2.4.1.2 "><p id="p10966323"><a name="p10966323"></a><a name="p10966323"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.2.4.1.3 "><p id="p8495130"><a name="p8495130"></a><a name="p8495130"></a>网卡端口所属子网的网络ID（network_id）。</p>
    </td>
    </tr>
    <tr id="row9347313"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.2.4.1.1 "><p id="p18934887"><a name="p18934887"></a><a name="p18934887"></a>port_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.2.4.1.2 "><p id="p13287175"><a name="p13287175"></a><a name="p13287175"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.2.4.1.3 "><p id="p22674843"><a name="p22674843"></a><a name="p22674843"></a>网卡端口ID。</p>
    </td>
    </tr>
    <tr id="row2747002"><td class="cellrowborder" valign="top" width="28.799999999999997%" headers="mcps1.2.4.1.1 "><p id="p21180630"><a name="p21180630"></a><a name="p21180630"></a>mac_addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.38%" headers="mcps1.2.4.1.2 "><p id="p50770908"><a name="p50770908"></a><a name="p50770908"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.82%" headers="mcps1.2.4.1.3 "><p id="p35008393"><a name="p35008393"></a><a name="p35008393"></a>网卡MAC地址信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  fixed\_ips字段数据结构说明

    <a name="table19750463"></a>
    <table><thead align="left"><tr id="row60761195"><th class="cellrowborder" valign="top" width="29.18%" id="mcps1.2.4.1.1"><p id="p1975316192155"><a name="p1975316192155"></a><a name="p1975316192155"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.589999999999996%" id="mcps1.2.4.1.2"><p id="p9754171910158"><a name="p9754171910158"></a><a name="p9754171910158"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.230000000000004%" id="mcps1.2.4.1.3"><p id="p17562199153"><a name="p17562199153"></a><a name="p17562199153"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row61624137"><td class="cellrowborder" valign="top" width="29.18%" headers="mcps1.2.4.1.1 "><p id="p25499238"><a name="p25499238"></a><a name="p25499238"></a>subnet_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.589999999999996%" headers="mcps1.2.4.1.2 "><p id="p65213800"><a name="p65213800"></a><a name="p65213800"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.2.4.1.3 "><p id="p27784979"><a name="p27784979"></a><a name="p27784979"></a>网卡私网IP对应子网的子网ID（subnet_id）。</p>
    </td>
    </tr>
    <tr id="row48738220"><td class="cellrowborder" valign="top" width="29.18%" headers="mcps1.2.4.1.1 "><p id="p55481787"><a name="p55481787"></a><a name="p55481787"></a>ip_address</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.589999999999996%" headers="mcps1.2.4.1.2 "><p id="p17532027"><a name="p17532027"></a><a name="p17532027"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.2.4.1.3 "><p id="p30163672"><a name="p30163672"></a><a name="p30163672"></a>网卡私网IP信息。</p>
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


## 返回值<a name="section7610951"></a>

正常返回值：

<a name="zh-cn_topic_0106040941_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0106040941_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0106040941_p19735204616177"><a name="zh-cn_topic_0106040941_p19735204616177"></a><a name="zh-cn_topic_0106040941_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0106040941_p207355465176"><a name="zh-cn_topic_0106040941_p207355465176"></a><a name="zh-cn_topic_0106040941_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0106040941_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0106040941_p13735144611178"><a name="zh-cn_topic_0106040941_p13735144611178"></a><a name="zh-cn_topic_0106040941_p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0106040941_p207351246161711"><a name="zh-cn_topic_0106040941_p207351246161711"></a><a name="zh-cn_topic_0106040941_p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

