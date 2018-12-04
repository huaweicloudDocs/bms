# 查询裸金属服务器IP地址（OpenStack原生）<a name="ZH-CN_TOPIC_0053158696"></a>

## 功能介绍<a name="section53922917165259"></a>

查询裸金属服务器IP地址信息。

## 约束<a name="section64211377173223"></a>

不支持分页查询。

## URI<a name="section51121191165259"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/ips

参数说明请参见[表1](#table1152617127395)。

**表 1**  参数说明

<a name="table1152617127395"></a>
<table><thead align="left"><tr id="row195261122394"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p58268319165259"><a name="p58268319165259"></a><a name="p58268319165259"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p22113407165259"><a name="p22113407165259"></a><a name="p22113407165259"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p46355523165259"><a name="p46355523165259"></a><a name="p46355523165259"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6528101219392"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1217433165259"><a name="p1217433165259"></a><a name="p1217433165259"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p31503226165259"><a name="p31503226165259"></a><a name="p31503226165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1624545165259"><a name="p1624545165259"></a><a name="p1624545165259"></a>项目ID。</p>
</td>
</tr>
<tr id="row8528101220397"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p43442641165259"><a name="p43442641165259"></a><a name="p43442641165259"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p29193009165259"><a name="p29193009165259"></a><a name="p29193009165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p15823538165259"><a name="p15823538165259"></a><a name="p15823538165259"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8194118165259"></a>

不涉及。

## 响应消息<a name="section58140617165259"></a>

-   响应参数

    <a name="table53480673143936"></a>
    <table><thead align="left"><tr id="row28382388143936"><th class="cellrowborder" valign="top" width="24.8%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.869999999999997%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.33%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8940324143936"><td class="cellrowborder" valign="top" width="24.8%" headers="mcps1.1.4.1.1 "><p id="p53077645143936"><a name="p53077645143936"></a><a name="p53077645143936"></a>addresses</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.869999999999997%" headers="mcps1.1.4.1.2 "><p id="p4322023143936"><a name="p4322023143936"></a><a name="p4322023143936"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.33%" headers="mcps1.1.4.1.3 "><p id="p36857741143936"><a name="p36857741143936"></a><a name="p36857741143936"></a>裸金属服务器网络信息，请参见“[1] addresses参数结构说明”。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] addresses参数结构说明

    <a name="table56891490143956"></a>
    <table><thead align="left"><tr id="row33903869143956"><th class="cellrowborder" valign="top" width="24.86%" id="mcps1.1.4.1.1"><p id="p9236182413102"><a name="p9236182413102"></a><a name="p9236182413102"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.51%" id="mcps1.1.4.1.2"><p id="p19238124121016"><a name="p19238124121016"></a><a name="p19238124121016"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.629999999999995%" id="mcps1.1.4.1.3"><p id="p52411424141017"><a name="p52411424141017"></a><a name="p52411424141017"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row33776430143956"><td class="cellrowborder" valign="top" width="24.86%" headers="mcps1.1.4.1.1 "><p id="p51536339143956"><a name="p51536339143956"></a><a name="p51536339143956"></a>裸金属服务器所在网络名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.51%" headers="mcps1.1.4.1.2 "><p id="p13693953143956"><a name="p13693953143956"></a><a name="p13693953143956"></a>List &lt;Dict&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.629999999999995%" headers="mcps1.1.4.1.3 "><p id="p54366741143956"><a name="p54366741143956"></a><a name="p54366741143956"></a>裸金属服务器所在网络，内嵌裸金属服务器网络详细信息，格式参见“[2] 网络参数结构说明”。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] 网络参数结构说明

    <a name="table22651992144025"></a>
    <table><thead align="left"><tr id="row15576094144025"><th class="cellrowborder" valign="top" width="25.41%" id="mcps1.1.4.1.1"><p id="p355273111016"><a name="p355273111016"></a><a name="p355273111016"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.1.4.1.2"><p id="p16554153131017"><a name="p16554153131017"></a><a name="p16554153131017"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.17%" id="mcps1.1.4.1.3"><p id="p055523151012"><a name="p055523151012"></a><a name="p055523151012"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1498246144025"><td class="cellrowborder" valign="top" width="25.41%" headers="mcps1.1.4.1.1 "><p id="p54249095144025"><a name="p54249095144025"></a><a name="p54249095144025"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.1.4.1.2 "><p id="p32100540144025"><a name="p32100540144025"></a><a name="p32100540144025"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.17%" headers="mcps1.1.4.1.3 "><p id="p16571197144025"><a name="p16571197144025"></a><a name="p16571197144025"></a>IP地址版本，IPv4或者IPv6。</p>
    </td>
    </tr>
    <tr id="row14923052144025"><td class="cellrowborder" valign="top" width="25.41%" headers="mcps1.1.4.1.1 "><p id="p807709144025"><a name="p807709144025"></a><a name="p807709144025"></a>addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.1.4.1.2 "><p id="p65424470144025"><a name="p65424470144025"></a><a name="p65424470144025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.17%" headers="mcps1.1.4.1.3 "><p id="p39086769144025"><a name="p39086769144025"></a><a name="p39086769144025"></a>IP地址。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "addresses": {
            "08a7715f-7de6-4ff9-a343-95ba4209f24a": [
                {
                    "version": 4,
                    "addr": "192.168.2.90"
                }
            ]
        }
    }
    ```


## 返回值<a name="section38817202165259"></a>

请参考[通用返回值](通用返回值.md)。

