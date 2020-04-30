# 查询裸金属服务器规格extra\_specs参数的详情（OpenStack原生）<a name="ZH-CN_TOPIC_0114885743"></a>

## 功能介绍<a name="section62221755111516"></a>

“extra\_specs”参数用于描述裸金属服务器规格的键值对，例如“baremetal:extBootType”表示裸金属服务器的启动源，取值有两种：“LocalDisk”（表示本地盘）和“Volume”（表示云硬盘）。如果您想确认某个规格是否支持快速发放，那么可以调用该接口进行查询。

## URI<a name="section116617920169"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavors\_id\}/os-extra\_specs

参数说明请参见[表1](#table955744812451)。

**表 1**  参数说明

<a name="table955744812451"></a>
<table><thead align="left"><tr id="row1155794814454"><th class="cellrowborder" valign="top" width="23.232323232323232%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057973064_p26298136"><a name="zh-cn_topic_0057973064_p26298136"></a><a name="zh-cn_topic_0057973064_p26298136"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.732273227322732%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057973064_p49774232"><a name="zh-cn_topic_0057973064_p49774232"></a><a name="zh-cn_topic_0057973064_p49774232"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="54.03540354035403%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057973064_p5180964"><a name="zh-cn_topic_0057973064_p5180964"></a><a name="zh-cn_topic_0057973064_p5180964"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13559114874517"><td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p35224963"><a name="zh-cn_topic_0057973064_p35224963"></a><a name="zh-cn_topic_0057973064_p35224963"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p34649765"><a name="zh-cn_topic_0057973064_p34649765"></a><a name="zh-cn_topic_0057973064_p34649765"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="54.03540354035403%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p55167604"><a name="zh-cn_topic_0057973064_p55167604"></a><a name="zh-cn_topic_0057973064_p55167604"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row255944854514"><td class="cellrowborder" valign="top" width="23.232323232323232%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p18974100"><a name="zh-cn_topic_0057973064_p18974100"></a><a name="zh-cn_topic_0057973064_p18974100"></a>flavors_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p60507121"><a name="zh-cn_topic_0057973064_p60507121"></a><a name="zh-cn_topic_0057973064_p60507121"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="54.03540354035403%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p2129750"><a name="zh-cn_topic_0057973064_p2129750"></a><a name="zh-cn_topic_0057973064_p2129750"></a>规格ID。</p>
<p id="p1461914516495"><a name="p1461914516495"></a><a name="p1461914516495"></a>可以在<span id="zh-cn_topic_0053158674_text374914110111"><a name="zh-cn_topic_0053158674_text374914110111"></a><a name="zh-cn_topic_0053158674_text374914110111"></a>裸金属服务器</span><span id="zh-cn_topic_0053158674_text1749131818"><a name="zh-cn_topic_0053158674_text1749131818"></a><a name="zh-cn_topic_0053158674_text1749131818"></a></span>控制台查询，也可以通过<a href="查询裸金属服务器规格信息列表（OpenStack原生）.md">查询裸金属服务器规格信息列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1517812126172"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/flavors/physical.s2.medium/os-extra_specs
    ```


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
    <td class="cellrowborder" valign="top" width="21.95%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0057973064_p42695066"><a name="zh-cn_topic_0057973064_p42695066"></a><a name="zh-cn_topic_0057973064_p42695066"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.10000000000001%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0057973064_p9931138"><a name="zh-cn_topic_0057973064_p9931138"></a><a name="zh-cn_topic_0057973064_p9931138"></a>描述<span id="text6300153138"><a name="text6300153138"></a><a name="text6300153138"></a>裸金属服务器</span><span id="text13005314316"><a name="text13005314316"></a><a name="text13005314316"></a></span>规格的键值对。</p>
    <a name="ul6746628171115"></a><a name="ul6746628171115"></a><ul id="ul6746628171115"><li>capabilities:cpu_arch：<span id="text46223511313"><a name="text46223511313"></a><a name="text46223511313"></a>裸金属服务器</span><span id="text3622651316"><a name="text3622651316"></a><a name="text3622651316"></a></span>的CPU架构，取值为x86_64（适用于x86机型）或aarch64（适用于ARM机型）</li><li>baremetal:disk_detail：磁盘的描述信息。</li><li>capabilities:hypervisor_type：hypervisor类型，固定为“ironic”。</li><li>baremetal:__support_evs：是否支持云硬盘，取值为true或false。</li><li>baremetal:extBootType：表示<span id="text193781491131"><a name="text193781491131"></a><a name="text193781491131"></a>裸金属服务器</span><span id="text1037816914313"><a name="text1037816914313"></a><a name="text1037816914313"></a></span>的启动源，取值为LocalDisk（表示本地盘）或Volume（表示云硬盘，即快速发放）</li><li>baremetal:net_num：<span id="text105681112318"><a name="text105681112318"></a><a name="text105681112318"></a>裸金属服务器</span><span id="text9568811236"><a name="text9568811236"></a><a name="text9568811236"></a></span>实际可绑定的网卡数量。</li><li>baremetal:netcard_detail：网卡的描述信息。</li><li>baremetal:cpu_detail：CPU的描述信息。</li><li>resource_type：资源类型，固定为“ironic”。</li><li>baremetal:memory_detail：内存的描述信息。</li></ul>
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

