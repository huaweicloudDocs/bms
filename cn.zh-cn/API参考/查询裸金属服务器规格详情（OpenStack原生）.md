# 查询裸金属服务器规格详情（OpenStack原生）<a name="ZH-CN_TOPIC_0053158674"></a>

## 功能介绍<a name="section64833508"></a>

根据裸金属服务器的规格ID，查询规格的详细信息，比如规格名称、CPU核数、内存大小等。

## URI<a name="section46630661"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavors\_id\}

参数说明请参见[表1](#table1857156445)。

**表 1**  参数说明

<a name="table1857156445"></a>
<table><thead align="left"><tr id="row98631534416"><th class="cellrowborder" valign="top" width="23.792379237923793%" id="mcps1.2.4.1.1"><p id="p26298136"><a name="p26298136"></a><a name="p26298136"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.892489248924893%" id="mcps1.2.4.1.2"><p id="p49774232"><a name="p49774232"></a><a name="p49774232"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.315131513151314%" id="mcps1.2.4.1.3"><p id="p5180964"><a name="p5180964"></a><a name="p5180964"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row58681534411"><td class="cellrowborder" valign="top" width="23.792379237923793%" headers="mcps1.2.4.1.1 "><p id="p35224963"><a name="p35224963"></a><a name="p35224963"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.2 "><p id="p34649765"><a name="p34649765"></a><a name="p34649765"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.315131513151314%" headers="mcps1.2.4.1.3 "><p id="p55167604"><a name="p55167604"></a><a name="p55167604"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row98691534416"><td class="cellrowborder" valign="top" width="23.792379237923793%" headers="mcps1.2.4.1.1 "><p id="p18974100"><a name="p18974100"></a><a name="p18974100"></a>flavors_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.892489248924893%" headers="mcps1.2.4.1.2 "><p id="p60507121"><a name="p60507121"></a><a name="p60507121"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.315131513151314%" headers="mcps1.2.4.1.3 "><p id="p2129750"><a name="p2129750"></a><a name="p2129750"></a>规格ID。</p>
<p id="p1153834112450"><a name="p1153834112450"></a><a name="p1153834112450"></a>可以在裸金属服务器控制台查询，也可以通过<a href="查询裸金属服务器规格信息列表（OpenStack原生）.md">查询裸金属服务器规格信息列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section17022773"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium
    ```


## 响应消息<a name="section18987236"></a>

-   响应参数

    <a name="table61695723"></a>
    <table><thead align="left"><tr id="row52977523"><th class="cellrowborder" valign="top" width="25.41%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.619999999999997%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.97%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2794650"><td class="cellrowborder" valign="top" width="25.41%" headers="mcps1.1.4.1.1 "><p id="p25040094"><a name="p25040094"></a><a name="p25040094"></a>flavor</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.1.4.1.2 "><p id="p5563313"><a name="p5563313"></a><a name="p5563313"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.97%" headers="mcps1.1.4.1.3 "><p id="p29123463"><a name="p29123463"></a><a name="p29123463"></a>裸金属服务器规格。详情请参见<a href="#table20109663">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  flavor数据结构说明

    <a name="table20109663"></a>
    <table><thead align="left"><tr id="row50842877"><th class="cellrowborder" valign="top" width="26.169999999999998%" id="mcps1.2.4.1.1"><p id="p17447358101319"><a name="p17447358101319"></a><a name="p17447358101319"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.990000000000002%" id="mcps1.2.4.1.2"><p id="p14450195812134"><a name="p14450195812134"></a><a name="p14450195812134"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.839999999999996%" id="mcps1.2.4.1.3"><p id="p12452195881310"><a name="p12452195881310"></a><a name="p12452195881310"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37029065"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p46564252"><a name="p46564252"></a><a name="p46564252"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p28514710"><a name="p28514710"></a><a name="p28514710"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p50584809"><a name="p50584809"></a><a name="p50584809"></a>裸金属服务器规格ID。</p>
    </td>
    </tr>
    <tr id="row52610097"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p33559471"><a name="p33559471"></a><a name="p33559471"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p66621782"><a name="p66621782"></a><a name="p66621782"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p47570623"><a name="p47570623"></a><a name="p47570623"></a>裸金属服务器规格名称。</p>
    </td>
    </tr>
    <tr id="row25482430"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p50810959"><a name="p50810959"></a><a name="p50810959"></a>vcpus</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p40977906"><a name="p40977906"></a><a name="p40977906"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p9449599"><a name="p9449599"></a><a name="p9449599"></a>该裸金属服务器规格对应的CPU核数。</p>
    </td>
    </tr>
    <tr id="row2289826710437"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p6260494310453"><a name="p6260494310453"></a><a name="p6260494310453"></a>ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p3783561810453"><a name="p3783561810453"></a><a name="p3783561810453"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p42285210453"><a name="p42285210453"></a><a name="p42285210453"></a>该裸金属服务器规格对应的内存大小，单位为MB。</p>
    </td>
    </tr>
    <tr id="row17937528"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p43653635"><a name="p43653635"></a><a name="p43653635"></a>disk</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p57980147"><a name="p57980147"></a><a name="p57980147"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p56052334"><a name="p56052334"></a><a name="p56052334"></a>该裸金属服务器规格对应要求磁盘大小，单位为GB。</p>
    </td>
    </tr>
    <tr id="row43945239"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p2794612"><a name="p2794612"></a><a name="p2794612"></a>swap</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p14734188"><a name="p14734188"></a><a name="p14734188"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p1160474410518"><a name="p1160474410518"></a><a name="p1160474410518"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row34246806"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p22527890"><a name="p22527890"></a><a name="p22527890"></a>OS-FLV-EXT-DATA:ephemeral</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p31767774"><a name="p31767774"></a><a name="p31767774"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p414192310518"><a name="p414192310518"></a><a name="p414192310518"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row55347837"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p53989823"><a name="p53989823"></a><a name="p53989823"></a>OS-FLV-DISABLED:disabled</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p26649649"><a name="p26649649"></a><a name="p26649649"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p6667220510518"><a name="p6667220510518"></a><a name="p6667220510518"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row29760277"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p61772230"><a name="p61772230"></a><a name="p61772230"></a>rxtx_factor</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p17171756"><a name="p17171756"></a><a name="p17171756"></a>Float</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p1722029710518"><a name="p1722029710518"></a><a name="p1722029710518"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row5115727"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p11720763"><a name="p11720763"></a><a name="p11720763"></a>os-flavor-access:is_public</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p60282721"><a name="p60282721"></a><a name="p60282721"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p4354924810518"><a name="p4354924810518"></a><a name="p4354924810518"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row57014372193259"><td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p1587802219356"><a name="p1587802219356"></a><a name="p1587802219356"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.990000000000002%" headers="mcps1.2.4.1.2 "><p id="p1105141919356"><a name="p1105141919356"></a><a name="p1105141919356"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.839999999999996%" headers="mcps1.2.4.1.3 "><p id="p342100019356"><a name="p342100019356"></a><a name="p342100019356"></a>规格相关快捷链接地址。详情请参见<a href="#table35514108193545">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  links字段数据结构说明

    <a name="table35514108193545"></a>
    <table><thead align="left"><tr id="row23367815193545"><th class="cellrowborder" valign="top" width="26.85%" id="mcps1.2.4.1.1"><p id="p1992228131410"><a name="p1992228131410"></a><a name="p1992228131410"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.53%" id="mcps1.2.4.1.2"><p id="p159245814143"><a name="p159245814143"></a><a name="p159245814143"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.620000000000005%" id="mcps1.2.4.1.3"><p id="p792512831417"><a name="p792512831417"></a><a name="p792512831417"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37879124193545"><td class="cellrowborder" valign="top" width="26.85%" headers="mcps1.2.4.1.1 "><p id="p48310227193545"><a name="p48310227193545"></a><a name="p48310227193545"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.53%" headers="mcps1.2.4.1.2 "><p id="p20814310193545"><a name="p20814310193545"></a><a name="p20814310193545"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.620000000000005%" headers="mcps1.2.4.1.3 "><p id="p8237558193545"><a name="p8237558193545"></a><a name="p8237558193545"></a>快捷链接标记名称。</p>
    <a name="ul207311644172510"></a><a name="ul207311644172510"></a><ul id="ul207311644172510"><li>self：包含版本号的资源链接，需要立即跟踪时使用此类链接。</li><li>bookmark：提供了适合长期存储的资源链接。</li></ul>
    </td>
    </tr>
    <tr id="row7029160193545"><td class="cellrowborder" valign="top" width="26.85%" headers="mcps1.2.4.1.1 "><p id="p32491069193545"><a name="p32491069193545"></a><a name="p32491069193545"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.53%" headers="mcps1.2.4.1.2 "><p id="p14530947193545"><a name="p14530947193545"></a><a name="p14530947193545"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.620000000000005%" headers="mcps1.2.4.1.3 "><p id="p36156065193545"><a name="p36156065193545"></a><a name="p36156065193545"></a>对应快捷链接。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "flavor": {
            "name": "physical.o2.medium",
            "links": [
                {
                    "href": "https://openstack.example.com/v2/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium",
                    "rel": "self"
                },
                {
                    "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/flavors/physical.o2.medium",
                    "rel": "bookmark"
                }
            ],
            "ram": 192705,
            "OS-FLV-DISABLED:disabled": false,
            "vcpus": 24,
            "swap": "",
            "os-flavor-access:is_public": true,
            "rxtx_factor": 1,
            "OS-FLV-EXT-DATA:ephemeral": 0,
            "disk": 1862,
            "id": "physical.o2.medium"
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

