# 查询裸金属服务器IP地址（OpenStack原生）<a name="ZH-CN_TOPIC_0053158696"></a>

## 功能介绍<a name="section53922917165259"></a>

查询裸金属服务器私有IP地址信息。

## 约束<a name="section64211377173223"></a>

不支持分页查询。

## URI<a name="section51121191165259"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/ips

参数说明请参见[表1](#table1152617127395)。

**表 1**  参数说明

<a name="table1152617127395"></a>
<table><thead align="left"><tr id="row195261122394"><th class="cellrowborder" valign="top" width="26.742674267426747%" id="mcps1.2.4.1.1"><p id="p58268319165259"><a name="p58268319165259"></a><a name="p58268319165259"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.532553255325535%" id="mcps1.2.4.1.2"><p id="p22113407165259"><a name="p22113407165259"></a><a name="p22113407165259"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47.724772477247726%" id="mcps1.2.4.1.3"><p id="p46355523165259"><a name="p46355523165259"></a><a name="p46355523165259"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6528101219392"><td class="cellrowborder" valign="top" width="26.742674267426747%" headers="mcps1.2.4.1.1 "><p id="p1217433165259"><a name="p1217433165259"></a><a name="p1217433165259"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.532553255325535%" headers="mcps1.2.4.1.2 "><p id="p31503226165259"><a name="p31503226165259"></a><a name="p31503226165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.724772477247726%" headers="mcps1.2.4.1.3 "><p id="p1624545165259"><a name="p1624545165259"></a><a name="p1624545165259"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row8528101220397"><td class="cellrowborder" valign="top" width="26.742674267426747%" headers="mcps1.2.4.1.1 "><p id="p43442641165259"><a name="p43442641165259"></a><a name="p43442641165259"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.532553255325535%" headers="mcps1.2.4.1.2 "><p id="p29193009165259"><a name="p29193009165259"></a><a name="p29193009165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.724772477247726%" headers="mcps1.2.4.1.3 "><p id="p15823538165259"><a name="p15823538165259"></a><a name="p15823538165259"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从裸金属服务器控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8194118165259"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/ips
    ```


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
    <td class="cellrowborder" valign="top" width="22.869999999999997%" headers="mcps1.1.4.1.2 "><p id="p4322023143936"><a name="p4322023143936"></a><a name="p4322023143936"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.33%" headers="mcps1.1.4.1.3 "><p id="p36857741143936"><a name="p36857741143936"></a><a name="p36857741143936"></a>裸金属服务器网络信息，详情请参见<a href="#table56891490143956">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  addresses参数结构说明

    <a name="table56891490143956"></a>
    <table><thead align="left"><tr id="row33903869143956"><th class="cellrowborder" valign="top" width="24.86%" id="mcps1.2.4.1.1"><p id="p9236182413102"><a name="p9236182413102"></a><a name="p9236182413102"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.51%" id="mcps1.2.4.1.2"><p id="p19238124121016"><a name="p19238124121016"></a><a name="p19238124121016"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.629999999999995%" id="mcps1.2.4.1.3"><p id="p52411424141017"><a name="p52411424141017"></a><a name="p52411424141017"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row33776430143956"><td class="cellrowborder" valign="top" width="24.86%" headers="mcps1.2.4.1.1 "><p id="p51536339143956"><a name="p51536339143956"></a><a name="p51536339143956"></a>裸金属服务器所在虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.51%" headers="mcps1.2.4.1.2 "><p id="p13693953143956"><a name="p13693953143956"></a><a name="p13693953143956"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p54366741143956"><a name="p54366741143956"></a><a name="p54366741143956"></a>裸金属服务器所在虚拟私有云ID，格式请参见<a href="#table22651992144025">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  网络参数结构说明

    <a name="table22651992144025"></a>
    <table><thead align="left"><tr id="row15576094144025"><th class="cellrowborder" valign="top" width="25.41%" id="mcps1.2.4.1.1"><p id="p355273111016"><a name="p355273111016"></a><a name="p355273111016"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.2"><p id="p16554153131017"><a name="p16554153131017"></a><a name="p16554153131017"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.17%" id="mcps1.2.4.1.3"><p id="p055523151012"><a name="p055523151012"></a><a name="p055523151012"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1498246144025"><td class="cellrowborder" valign="top" width="25.41%" headers="mcps1.2.4.1.1 "><p id="p54249095144025"><a name="p54249095144025"></a><a name="p54249095144025"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.2 "><p id="p32100540144025"><a name="p32100540144025"></a><a name="p32100540144025"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.17%" headers="mcps1.2.4.1.3 "><p id="p16571197144025"><a name="p16571197144025"></a><a name="p16571197144025"></a>IP地址版本，取值为：</p>
    <a name="ul1882101316162"></a><a name="ul1882101316162"></a><ul id="ul1882101316162"><li>4：IPv4</li><li>6：IPv6</li></ul>
    </td>
    </tr>
    <tr id="row14923052144025"><td class="cellrowborder" valign="top" width="25.41%" headers="mcps1.2.4.1.1 "><p id="p807709144025"><a name="p807709144025"></a><a name="p807709144025"></a>addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.2 "><p id="p65424470144025"><a name="p65424470144025"></a><a name="p65424470144025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.17%" headers="mcps1.2.4.1.3 "><p id="p39086769144025"><a name="p39086769144025"></a><a name="p39086769144025"></a>IP地址。</p>
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

