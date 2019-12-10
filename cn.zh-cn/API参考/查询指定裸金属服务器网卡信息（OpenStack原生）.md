# 查询指定裸金属服务器网卡信息（OpenStack原生）<a name="ZH-CN_TOPIC_0053158687"></a>

## 功能介绍<a name="section44739342"></a>

根据网卡ID，查询裸金属服务器网卡信息。

## URI<a name="section901"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-interface/\{id\}

参数说明请参见[表1](#table1210415012480)。

**表 1**  参数说明

<a name="table1210415012480"></a>
<table><thead align="left"><tr id="row110416020487"><th class="cellrowborder" valign="top" width="25.95259525952595%" id="mcps1.2.4.1.1"><p id="p588929"><a name="p588929"></a><a name="p588929"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.432443244324432%" id="mcps1.2.4.1.2"><p id="p47703261"><a name="p47703261"></a><a name="p47703261"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="49.61496149614961%" id="mcps1.2.4.1.3"><p id="p38758958"><a name="p38758958"></a><a name="p38758958"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row51045024817"><td class="cellrowborder" valign="top" width="25.95259525952595%" headers="mcps1.2.4.1.1 "><p id="p22044110"><a name="p22044110"></a><a name="p22044110"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.432443244324432%" headers="mcps1.2.4.1.2 "><p id="p40742509"><a name="p40742509"></a><a name="p40742509"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49.61496149614961%" headers="mcps1.2.4.1.3 "><p id="p11808928"><a name="p11808928"></a><a name="p11808928"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row610413044818"><td class="cellrowborder" valign="top" width="25.95259525952595%" headers="mcps1.2.4.1.1 "><p id="p3575612917451"><a name="p3575612917451"></a><a name="p3575612917451"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.432443244324432%" headers="mcps1.2.4.1.2 "><p id="p1056536017451"><a name="p1056536017451"></a><a name="p1056536017451"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49.61496149614961%" headers="mcps1.2.4.1.3 "><p id="p5048782717451"><a name="p5048782717451"></a><a name="p5048782717451"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从裸金属服务器控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row210616034814"><td class="cellrowborder" valign="top" width="25.95259525952595%" headers="mcps1.2.4.1.1 "><p id="p18774354"><a name="p18774354"></a><a name="p18774354"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="24.432443244324432%" headers="mcps1.2.4.1.2 "><p id="p44327687"><a name="p44327687"></a><a name="p44327687"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49.61496149614961%" headers="mcps1.2.4.1.3 "><p id="p33772909"><a name="p33772909"></a><a name="p33772909"></a>网卡ID。</p>
<p id="p7979630184012"><a name="p7979630184012"></a><a name="p7979630184012"></a>可以在裸金属服务器详情页面“网卡”页签中查看；也可以通过<a href="查询裸金属服务器网卡信息（OpenStack原生）.md">查询裸金属服务器网卡信息（OpenStack原生）</a>API获取，对应的是参数“port_id”的取值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8117"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/os-interface/ce531f90-199f-48c0-816c-13e38010b442
    ```


## 响应消息<a name="section73053"></a>

-   响应参数

    <a name="table59131099"></a>
    <table><thead align="left"><tr id="row30342446"><th class="cellrowborder" valign="top" width="25.97%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.49%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.54%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row59560431"><td class="cellrowborder" valign="top" width="25.97%" headers="mcps1.1.4.1.1 "><p id="p59665636"><a name="p59665636"></a><a name="p59665636"></a>interfaceAttachment</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.49%" headers="mcps1.1.4.1.2 "><p id="p20239120"><a name="p20239120"></a><a name="p20239120"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.54%" headers="mcps1.1.4.1.3 "><p id="p57477322"><a name="p57477322"></a><a name="p57477322"></a>裸金属服务器网卡信息列表，详情请参见<a href="#table24005299">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  interfaceAttachment字段数据结构说明

    <a name="table24005299"></a>
    <table><thead align="left"><tr id="row46441279"><th class="cellrowborder" valign="top" width="26.08%" id="mcps1.2.4.1.1"><p id="p7555195314159"><a name="p7555195314159"></a><a name="p7555195314159"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.599999999999998%" id="mcps1.2.4.1.2"><p id="p2558155381518"><a name="p2558155381518"></a><a name="p2558155381518"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.32%" id="mcps1.2.4.1.3"><p id="p1456215301510"><a name="p1456215301510"></a><a name="p1456215301510"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row64586077"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.2.4.1.1 "><p id="p64089786"><a name="p64089786"></a><a name="p64089786"></a>port_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.2 "><p id="p56055356"><a name="p56055356"></a><a name="p56055356"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.32%" headers="mcps1.2.4.1.3 "><p id="p62165703"><a name="p62165703"></a><a name="p62165703"></a>网卡端口状态，取值为：<span>ACTIVE、BUILD、DOWN</span>。</p>
    </td>
    </tr>
    <tr id="row22620416"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.2.4.1.1 "><p id="p20314447"><a name="p20314447"></a><a name="p20314447"></a>fixed_ips</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.2 "><p id="p4888719"><a name="p4888719"></a><a name="p4888719"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.32%" headers="mcps1.2.4.1.3 "><p id="p7106508"><a name="p7106508"></a><a name="p7106508"></a>网卡IP信息列表，详情请参见<a href="#table53180163">表3</a>。</p>
    </td>
    </tr>
    <tr id="row63958576"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.2.4.1.1 "><p id="p13262169"><a name="p13262169"></a><a name="p13262169"></a>net_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.2 "><p id="p40009126"><a name="p40009126"></a><a name="p40009126"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.32%" headers="mcps1.2.4.1.3 "><p id="p41406050"><a name="p41406050"></a><a name="p41406050"></a>网卡端口所属子网的网络ID（network_id）。</p>
    </td>
    </tr>
    <tr id="row37110132"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.2.4.1.1 "><p id="p53130720"><a name="p53130720"></a><a name="p53130720"></a>port_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.2 "><p id="p27217289"><a name="p27217289"></a><a name="p27217289"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.32%" headers="mcps1.2.4.1.3 "><p id="p44289360"><a name="p44289360"></a><a name="p44289360"></a>网卡端口ID。</p>
    </td>
    </tr>
    <tr id="row63059925"><td class="cellrowborder" valign="top" width="26.08%" headers="mcps1.2.4.1.1 "><p id="p7580267"><a name="p7580267"></a><a name="p7580267"></a>mac_addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.2 "><p id="p6466753"><a name="p6466753"></a><a name="p6466753"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.32%" headers="mcps1.2.4.1.3 "><p id="p16643039"><a name="p16643039"></a><a name="p16643039"></a>网卡MAC地址信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  fixed\_ips字段数据结构说明

    <a name="table53180163"></a>
    <table><thead align="left"><tr id="row34896342"><th class="cellrowborder" valign="top" width="26.150000000000002%" id="mcps1.2.4.1.1"><p id="p720221141617"><a name="p720221141617"></a><a name="p720221141617"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.66%" id="mcps1.2.4.1.2"><p id="p5203141181611"><a name="p5203141181611"></a><a name="p5203141181611"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.19%" id="mcps1.2.4.1.3"><p id="p9205011169"><a name="p9205011169"></a><a name="p9205011169"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66523006"><td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.1 "><p id="p64293480112230"><a name="p64293480112230"></a><a name="p64293480112230"></a>subnet_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.66%" headers="mcps1.2.4.1.2 "><p id="p40389402112230"><a name="p40389402112230"></a><a name="p40389402112230"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.19%" headers="mcps1.2.4.1.3 "><p id="p50192196112230"><a name="p50192196112230"></a><a name="p50192196112230"></a>网卡私网IP对应子网的子网ID（subnet_id）。</p>
    </td>
    </tr>
    <tr id="row12592542"><td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.1 "><p id="p15780700112230"><a name="p15780700112230"></a><a name="p15780700112230"></a>ip_address</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.66%" headers="mcps1.2.4.1.2 "><p id="p3168304112230"><a name="p3168304112230"></a><a name="p3168304112230"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.19%" headers="mcps1.2.4.1.3 "><p id="p27992537112230"><a name="p27992537112230"></a><a name="p27992537112230"></a>网卡IP地址。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "interfaceAttachment": {
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

