# 查询指定裸金属服务器IP地址（OpenStack原生）<a name="ZH-CN_TOPIC_0053158662"></a>

## 功能介绍<a name="section53922917165259"></a>

查询指定裸金属服务器IP地址。

## URI<a name="section51121191165259"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/ips/\{networkName\}

参数说明请参见[表1](#table6532183934016)。

**表 1**  参数说明

<a name="table6532183934016"></a>
<table><thead align="left"><tr id="row1753243915409"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p58268319165259"><a name="p58268319165259"></a><a name="p58268319165259"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p22113407165259"><a name="p22113407165259"></a><a name="p22113407165259"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p46355523165259"><a name="p46355523165259"></a><a name="p46355523165259"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row253363924014"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1217433165259"><a name="p1217433165259"></a><a name="p1217433165259"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p31503226165259"><a name="p31503226165259"></a><a name="p31503226165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1624545165259"><a name="p1624545165259"></a><a name="p1624545165259"></a>项目ID。</p>
</td>
</tr>
<tr id="row45331439194017"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p43442641165259"><a name="p43442641165259"></a><a name="p43442641165259"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p29193009165259"><a name="p29193009165259"></a><a name="p29193009165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p15823538165259"><a name="p15823538165259"></a><a name="p15823538165259"></a>裸金属服务器ID。</p>
</td>
</tr>
<tr id="row853312391409"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p39194593144447"><a name="p39194593144447"></a><a name="p39194593144447"></a>networkName</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p20645494144447"><a name="p20645494144447"></a><a name="p20645494144447"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p61672340144447"><a name="p61672340144447"></a><a name="p61672340144447"></a>裸金属服务器网络名称。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8194118165259"></a>

不涉及。

## 响应消息<a name="section58140617165259"></a>

-   响应参数

    <a name="table56891490143956"></a>
    <table><thead align="left"><tr id="row33903869143956"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.369999999999997%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.629999999999995%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row33776430143956"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p51536339143956"><a name="p51536339143956"></a><a name="p51536339143956"></a>裸金属服务器所在网络名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.1.4.1.2 "><p id="p13693953143956"><a name="p13693953143956"></a><a name="p13693953143956"></a>List &lt;Dict&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.629999999999995%" headers="mcps1.1.4.1.3 "><p id="p54366741143956"><a name="p54366741143956"></a><a name="p54366741143956"></a>裸金属服务器所在网络，内嵌裸金属服务器网络详细信息，格式参见“[1] 网络参数结构说明”。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] 网络参数结构说明

    <a name="table22651992144025"></a>
    <table><thead align="left"><tr id="row15576094144025"><th class="cellrowborder" valign="top" width="25.040000000000003%" id="mcps1.1.4.1.1"><p id="p18294205151113"><a name="p18294205151113"></a><a name="p18294205151113"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.96%" id="mcps1.1.4.1.2"><p id="p52953511116"><a name="p52953511116"></a><a name="p52953511116"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52%" id="mcps1.1.4.1.3"><p id="p1329719531112"><a name="p1329719531112"></a><a name="p1329719531112"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1498246144025"><td class="cellrowborder" valign="top" width="25.040000000000003%" headers="mcps1.1.4.1.1 "><p id="p54249095144025"><a name="p54249095144025"></a><a name="p54249095144025"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.96%" headers="mcps1.1.4.1.2 "><p id="p32100540144025"><a name="p32100540144025"></a><a name="p32100540144025"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.4.1.3 "><p id="p16571197144025"><a name="p16571197144025"></a><a name="p16571197144025"></a>IP地址版本，IPv4或者IPv6。</p>
    </td>
    </tr>
    <tr id="row14923052144025"><td class="cellrowborder" valign="top" width="25.040000000000003%" headers="mcps1.1.4.1.1 "><p id="p807709144025"><a name="p807709144025"></a><a name="p807709144025"></a>addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.96%" headers="mcps1.1.4.1.2 "><p id="p65424470144025"><a name="p65424470144025"></a><a name="p65424470144025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.4.1.3 "><p id="p39086769144025"><a name="p39086769144025"></a><a name="p39086769144025"></a>IP地址。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "5849fdf1-9d79-4589-80c2-fe557990c417": [
            {
                "version": 4,
                "addr": "192.168.1.159"
            }
        ]
    }
    ```


## 返回值<a name="section38817202165259"></a>

请参考[通用返回值](通用返回值.md)。

