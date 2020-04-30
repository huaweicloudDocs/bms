# 查询裸金属服务器的指定IP地址（OpenStack原生）<a name="ZH-CN_TOPIC_0053158662"></a>

## 功能介绍<a name="section53922917165259"></a>

根据网络名称查询裸金属服务器的指定IP地址。

## URI<a name="section51121191165259"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/ips/\{vpc\_id\}

参数说明请参见[表1](#table6532183934016)。

**表 1**  参数说明

<a name="table6532183934016"></a>
<table><thead align="left"><tr id="row1753243915409"><th class="cellrowborder" valign="top" width="24.562456245624563%" id="mcps1.2.4.1.1"><p id="p58268319165259"><a name="p58268319165259"></a><a name="p58268319165259"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.432343234323433%" id="mcps1.2.4.1.2"><p id="p22113407165259"><a name="p22113407165259"></a><a name="p22113407165259"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="52.00520052005201%" id="mcps1.2.4.1.3"><p id="p46355523165259"><a name="p46355523165259"></a><a name="p46355523165259"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row253363924014"><td class="cellrowborder" valign="top" width="24.562456245624563%" headers="mcps1.2.4.1.1 "><p id="p1217433165259"><a name="p1217433165259"></a><a name="p1217433165259"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.432343234323433%" headers="mcps1.2.4.1.2 "><p id="p31503226165259"><a name="p31503226165259"></a><a name="p31503226165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.00520052005201%" headers="mcps1.2.4.1.3 "><p id="p1624545165259"><a name="p1624545165259"></a><a name="p1624545165259"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row45331439194017"><td class="cellrowborder" valign="top" width="24.562456245624563%" headers="mcps1.2.4.1.1 "><p id="p43442641165259"><a name="p43442641165259"></a><a name="p43442641165259"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.432343234323433%" headers="mcps1.2.4.1.2 "><p id="p29193009165259"><a name="p29193009165259"></a><a name="p29193009165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.00520052005201%" headers="mcps1.2.4.1.3 "><p id="p15823538165259"><a name="p15823538165259"></a><a name="p15823538165259"></a><span id="text15688205618557"><a name="text15688205618557"></a><a name="text15688205618557"></a>裸金属服务器</span><span id="text3688155685511"><a name="text3688155685511"></a><a name="text3688155685511"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row853312391409"><td class="cellrowborder" valign="top" width="24.562456245624563%" headers="mcps1.2.4.1.1 "><p id="p39194593144447"><a name="p39194593144447"></a><a name="p39194593144447"></a>vpc_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.432343234323433%" headers="mcps1.2.4.1.2 "><p id="p20645494144447"><a name="p20645494144447"></a><a name="p20645494144447"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="52.00520052005201%" headers="mcps1.2.4.1.3 "><p id="p37275314377"><a name="p37275314377"></a><a name="p37275314377"></a><span id="text61205995512"><a name="text61205995512"></a><a name="text61205995512"></a>裸金属服务器</span><span id="text71859185516"><a name="text71859185516"></a><a name="text71859185516"></a></span>所在虚拟私有云ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8194118165259"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/ips/{vpc_id}
    ```


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
    <tbody><tr id="row33776430143956"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p51536339143956"><a name="p51536339143956"></a><a name="p51536339143956"></a><span id="text186011383567"><a name="text186011383567"></a><a name="text186011383567"></a>裸金属服务器</span><span id="text16601158145615"><a name="text16601158145615"></a><a name="text16601158145615"></a></span>所在虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.1.4.1.2 "><p id="p13693953143956"><a name="p13693953143956"></a><a name="p13693953143956"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.629999999999995%" headers="mcps1.1.4.1.3 "><p id="p54366741143956"><a name="p54366741143956"></a><a name="p54366741143956"></a><span id="text101948516566"><a name="text101948516566"></a><a name="text101948516566"></a>裸金属服务器</span><span id="text1219417514566"><a name="text1219417514566"></a><a name="text1219417514566"></a></span>所在虚拟私有云ID，格式参见<a href="#table22651992144025">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  网络参数结构说明

    <a name="table22651992144025"></a>
    <table><thead align="left"><tr id="row15576094144025"><th class="cellrowborder" valign="top" width="25.040000000000003%" id="mcps1.2.4.1.1"><p id="p18294205151113"><a name="p18294205151113"></a><a name="p18294205151113"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.96%" id="mcps1.2.4.1.2"><p id="p52953511116"><a name="p52953511116"></a><a name="p52953511116"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52%" id="mcps1.2.4.1.3"><p id="p1329719531112"><a name="p1329719531112"></a><a name="p1329719531112"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1498246144025"><td class="cellrowborder" valign="top" width="25.040000000000003%" headers="mcps1.2.4.1.1 "><p id="p54249095144025"><a name="p54249095144025"></a><a name="p54249095144025"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.96%" headers="mcps1.2.4.1.2 "><p id="p32100540144025"><a name="p32100540144025"></a><a name="p32100540144025"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.3 "><p id="p16571197144025"><a name="p16571197144025"></a><a name="p16571197144025"></a>IP地址版本，取值为：</p>
    <a name="ul95681331131713"></a><a name="ul95681331131713"></a><ul id="ul95681331131713"><li>4：IPv4</li><li>6：IPv6</li></ul>
    </td>
    </tr>
    <tr id="row14923052144025"><td class="cellrowborder" valign="top" width="25.040000000000003%" headers="mcps1.2.4.1.1 "><p id="p807709144025"><a name="p807709144025"></a><a name="p807709144025"></a>addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.96%" headers="mcps1.2.4.1.2 "><p id="p65424470144025"><a name="p65424470144025"></a><a name="p65424470144025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.4.1.3 "><p id="p39086769144025"><a name="p39086769144025"></a><a name="p39086769144025"></a>IP地址。</p>
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

