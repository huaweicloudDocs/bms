# 查询裸金属服务器规格extra\_specs的详情（OpenStack原生）<a name="ZH-CN_TOPIC_0114885743"></a>

## 功能介绍<a name="section62221755111516"></a>

查询指定规格的详细信息。

## URI<a name="section116617920169"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavors\_id\}/os-extra\_specs

参数说明请参见[表1](#table955744812451)。

**表 1**  参数说明

<a name="table955744812451"></a>
<table><thead align="left"><tr id="row1155794814454"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057973064_p26298136"><a name="zh-cn_topic_0057973064_p26298136"></a><a name="zh-cn_topic_0057973064_p26298136"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057973064_p49774232"><a name="zh-cn_topic_0057973064_p49774232"></a><a name="zh-cn_topic_0057973064_p49774232"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057973064_p5180964"><a name="zh-cn_topic_0057973064_p5180964"></a><a name="zh-cn_topic_0057973064_p5180964"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13559114874517"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p35224963"><a name="zh-cn_topic_0057973064_p35224963"></a><a name="zh-cn_topic_0057973064_p35224963"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p34649765"><a name="zh-cn_topic_0057973064_p34649765"></a><a name="zh-cn_topic_0057973064_p34649765"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p55167604"><a name="zh-cn_topic_0057973064_p55167604"></a><a name="zh-cn_topic_0057973064_p55167604"></a>项目ID。</p>
</td>
</tr>
<tr id="row255944854514"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p18974100"><a name="zh-cn_topic_0057973064_p18974100"></a><a name="zh-cn_topic_0057973064_p18974100"></a>flavors_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p60507121"><a name="zh-cn_topic_0057973064_p60507121"></a><a name="zh-cn_topic_0057973064_p60507121"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p2129750"><a name="zh-cn_topic_0057973064_p2129750"></a><a name="zh-cn_topic_0057973064_p2129750"></a>规格ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1517812126172"></a>

不涉及。

## 响应消息<a name="section3899184185"></a>

-   响应参数

    <a name="zh-cn_topic_0057973064_table28168569"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0057973064_row26406300"><th class="cellrowborder" valign="top" width="21.95%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.95%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.10000000000001%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0057973064_row46433444"><td class="cellrowborder" valign="top" width="21.95%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0057973064_p3012613"><a name="zh-cn_topic_0057973064_p3012613"></a><a name="zh-cn_topic_0057973064_p3012613"></a>extra_specs</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.95%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0057973064_p42695066"><a name="zh-cn_topic_0057973064_p42695066"></a><a name="zh-cn_topic_0057973064_p42695066"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.10000000000001%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0057973064_p9931138"><a name="zh-cn_topic_0057973064_p9931138"></a><a name="zh-cn_topic_0057973064_p9931138"></a>描述裸金属服务器规格的键值对。</p>
    <div class="note" id="note16909121093617"><a name="note16909121093617"></a><a name="note16909121093617"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p89091410153619"><a name="p89091410153619"></a><a name="p89091410153619"></a>本地盘："baremetal:extBootType": "LocalDisk"</p>
    <p id="p1637272041716"><a name="p1637272041716"></a><a name="p1637272041716"></a>系统盘（快速发放）："baremetal:extBootType": "Volume"</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "extra_specs": {
            "capabilities:cpu_arch": "x86_64",
            "baremetal:disk_detail": "SAS 8T",
            "capabilities:hypervisor_type": "ironic",
            "baremetal:__support_evs": "true",
            "baremetal:extBootType": "LocalDisk",
            "capabilities:board_type": "s2m",
            "baremetal:net_num": "2",
            "baremetal:netcard_detail": "2*10GE",
            "baremetal:cpu_detail": "2*8coreIntel Xeon E5-2667 V43.2GHz",
            "resource_type": "ironic",
            "baremetal:memory_detail": "256GB DDR4 RAM(GB)"
        }
    }
    ```


## 返回值<a name="section52956621"></a>

请参考[通用返回值](通用返回值.md)。

## 错误码<a name="section1582119227231"></a>

<a name="zh-cn_topic_0057973064_table19873637"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973064_row52823103"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0057973064_p50812955"><a name="zh-cn_topic_0057973064_p50812955"></a><a name="zh-cn_topic_0057973064_p50812955"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="31.15841584158416%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0057973064_p22208687"><a name="zh-cn_topic_0057973064_p22208687"></a><a name="zh-cn_topic_0057973064_p22208687"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="51.01980198019802%" id="mcps1.1.4.1.3"><p id="p1828952011341"><a name="p1828952011341"></a><a name="p1828952011341"></a>处理措施</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973064_row54073252"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0057973064_p17857314"><a name="zh-cn_topic_0057973064_p17857314"></a><a name="zh-cn_topic_0057973064_p17857314"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="31.15841584158416%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0057973064_p37156304"><a name="zh-cn_topic_0057973064_p37156304"></a><a name="zh-cn_topic_0057973064_p37156304"></a>The resource could not be found.</p>
</td>
<td class="cellrowborder" valign="top" width="51.01980198019802%" headers="mcps1.1.4.1.3 "><p id="p028972083416"><a name="p028972083416"></a><a name="p028972083416"></a>该错误一般是由于flavor不存在，请排查指定的flavor是否存在。</p>
</td>
</tr>
</tbody>
</table>

