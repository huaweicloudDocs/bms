# 查询裸金属服务器规格信息列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158684"></a>

## 功能介绍<a name="section57769674"></a>

查询裸金属服务器规格信息列表。

## 约束<a name="section60580832213029"></a>

本接口查询出来的falvor为系统中所有的flavor，其中flavor的名称以“physical”开头的为裸金属服务器的flavor，可用于申请裸金属服务器。

## URI<a name="section50165025"></a>

GET /v2.1/\{project\_id\}/flavors/detail\{?minDisk,minRam,is\_public,sort\_key,sort\_dir\}

参数说明请参见[表1](#table1687344817416)。

**表 1**  参数说明

<a name="table1687344817416"></a>
<table><thead align="left"><tr id="row138741548164116"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row28741048144119"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p37195178"><a name="p37195178"></a><a name="p37195178"></a>项目ID。</p>
</td>
</tr>
</tbody>
</table>

查询裸金属服务器规格时可选的查询检索参数如[表2](#table1719300427)所示。

**表 2**  可选的查询检索参数

<a name="table1719300427"></a>
<table><thead align="left"><tr id="row57253084215"><th class="cellrowborder" valign="top" width="20.830000000000002%" id="mcps1.2.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.39%" id="mcps1.2.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="20.07%" id="mcps1.2.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="38.71%" id="mcps1.2.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row107363044215"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p7618124412423"><a name="p7618124412423"></a><a name="p7618124412423"></a>minDisk</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p26202446424"><a name="p26202446424"></a><a name="p26202446424"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p662344444214"><a name="p662344444214"></a><a name="p662344444214"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p116242044134216"><a name="p116242044134216"></a><a name="p116242044134216"></a>最小的硬盘规格，单位GB，大于等于此规格的都可以查询到。</p>
</td>
</tr>
<tr id="row17730303422"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p1562994419427"><a name="p1562994419427"></a><a name="p1562994419427"></a>minRam</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p146323449428"><a name="p146323449428"></a><a name="p146323449428"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p1663474417428"><a name="p1663474417428"></a><a name="p1663474417428"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p863714412422"><a name="p863714412422"></a><a name="p863714412422"></a>最小的内存规格，单位MB，大于等于此规格的都可以查询到。</p>
</td>
</tr>
<tr id="row5737306425"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p36401444174214"><a name="p36401444174214"></a><a name="p36401444174214"></a>is_public</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p14643174444210"><a name="p14643174444210"></a><a name="p14643174444210"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p17644134415420"><a name="p17644134415420"></a><a name="p17644134415420"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p7649204484210"><a name="p7649204484210"></a><a name="p7649204484210"></a>是否显示public的flavor，只有admin可以查询private的flavor。可选值为true/false/none。非admin用户指定is_public过滤无效，返回所有public镜像。</p>
</td>
</tr>
<tr id="row1673103013428"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p12651144417421"><a name="p12651144417421"></a><a name="p12651144417421"></a>sort_key</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p196558447427"><a name="p196558447427"></a><a name="p196558447427"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p36571044134220"><a name="p36571044134220"></a><a name="p36571044134220"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p366084404210"><a name="p366084404210"></a><a name="p366084404210"></a>排序字段，默认值为：flavorid。可以指定的其他key为name/ memory_mb/vcpus，/root_gb/flavorid。</p>
</td>
</tr>
<tr id="row87303017423"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p16663174412421"><a name="p16663174412421"></a><a name="p16663174412421"></a>sort_dir</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p466510447425"><a name="p466510447425"></a><a name="p466510447425"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p10669124420428"><a name="p10669124420428"></a><a name="p10669124420428"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p19672104424217"><a name="p19672104424217"></a><a name="p19672104424217"></a>升序/降序排序，默认值为：asc。可以指定的参数为asc/desc。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section48832041"></a>

不涉及。

## 响应消息<a name="section36835188"></a>

-   响应参数

    <a name="table23477058"></a>
    <table><thead align="left"><tr id="row2792905"><th class="cellrowborder" valign="top" width="23.94%" id="mcps1.1.4.1.1"><p id="p151621239131213"><a name="p151621239131213"></a><a name="p151621239131213"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.09%" id="mcps1.1.4.1.2"><p id="p17165183912124"><a name="p17165183912124"></a><a name="p17165183912124"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.970000000000006%" id="mcps1.1.4.1.3"><p id="p716920393129"><a name="p716920393129"></a><a name="p716920393129"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row9994955"><td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.1.4.1.1 "><p id="p4284989"><a name="p4284989"></a><a name="p4284989"></a>flavors</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.1.4.1.2 "><p id="p62312200"><a name="p62312200"></a><a name="p62312200"></a>列表数据结构[2]</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.970000000000006%" headers="mcps1.1.4.1.3 "><p id="p60002101"><a name="p60002101"></a><a name="p60002101"></a>裸金属服务器规格列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] flavors数据结构说明

    <a name="table13194498"></a>
    <table><thead align="left"><tr id="row35873632"><th class="cellrowborder" valign="top" width="24.22%" id="mcps1.1.4.1.1"><p id="p1934639181313"><a name="p1934639181313"></a><a name="p1934639181313"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.46%" id="mcps1.1.4.1.2"><p id="p1134716921317"><a name="p1134716921317"></a><a name="p1134716921317"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.32%" id="mcps1.1.4.1.3"><p id="p535259131314"><a name="p535259131314"></a><a name="p535259131314"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15349251"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p35329809"><a name="p35329809"></a><a name="p35329809"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p24536113173145"><a name="p24536113173145"></a><a name="p24536113173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p56261663"><a name="p56261663"></a><a name="p56261663"></a>裸金属服务器规格ID。</p>
    </td>
    </tr>
    <tr id="row36592919"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p11236435"><a name="p11236435"></a><a name="p11236435"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p54383891173145"><a name="p54383891173145"></a><a name="p54383891173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p61525259"><a name="p61525259"></a><a name="p61525259"></a>裸金属服务器规格名称。</p>
    </td>
    </tr>
    <tr id="row16856419"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p23192694"><a name="p23192694"></a><a name="p23192694"></a>vcpus</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p61992247173145"><a name="p61992247173145"></a><a name="p61992247173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p60827539"><a name="p60827539"></a><a name="p60827539"></a>该裸金属服务器规格对应的CPU核数。</p>
    </td>
    </tr>
    <tr id="row3097644510336"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p3929432310349"><a name="p3929432310349"></a><a name="p3929432310349"></a>ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p51423198173145"><a name="p51423198173145"></a><a name="p51423198173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p154673810349"><a name="p154673810349"></a><a name="p154673810349"></a>该裸金属服务器规格对应的内存大小，单位为MB。</p>
    </td>
    </tr>
    <tr id="row10576944"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p51426113"><a name="p51426113"></a><a name="p51426113"></a>disk</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p31344710173145"><a name="p31344710173145"></a><a name="p31344710173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p19756352"><a name="p19756352"></a><a name="p19756352"></a>该裸金属服务器规格对应要求的磁盘大小，单位为GB。</p>
    </td>
    </tr>
    <tr id="row56760689"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p34213098"><a name="p34213098"></a><a name="p34213098"></a>swap</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p31087024173145"><a name="p31087024173145"></a><a name="p31087024173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p3906895110328"><a name="p3906895110328"></a><a name="p3906895110328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row56925253"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p47542785"><a name="p47542785"></a><a name="p47542785"></a>OS-FLV-EXT-DATA:ephemeral</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p18132829173145"><a name="p18132829173145"></a><a name="p18132829173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p2710719510328"><a name="p2710719510328"></a><a name="p2710719510328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row44806966"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p5485596"><a name="p5485596"></a><a name="p5485596"></a>OS-FLV-DISABLED:disabled</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p52585611173145"><a name="p52585611173145"></a><a name="p52585611173145"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p3113915110328"><a name="p3113915110328"></a><a name="p3113915110328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row42184651"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p61513540"><a name="p61513540"></a><a name="p61513540"></a>rxtx_factor</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p7527547173145"><a name="p7527547173145"></a><a name="p7527547173145"></a>Float</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p1764564010328"><a name="p1764564010328"></a><a name="p1764564010328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row51313205"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p62728917"><a name="p62728917"></a><a name="p62728917"></a>os-flavor-access:is_public</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p43117912173145"><a name="p43117912173145"></a><a name="p43117912173145"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p3503996211722"><a name="p3503996211722"></a><a name="p3503996211722"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row2047803919452"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.1.4.1.1 "><p id="p6509154919455"><a name="p6509154919455"></a><a name="p6509154919455"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.1.4.1.2 "><p id="p3792414219455"><a name="p3792414219455"></a><a name="p3792414219455"></a>列表数据结构[3]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.1.4.1.3 "><p id="p6495712119455"><a name="p6495712119455"></a><a name="p6495712119455"></a>规格相关快捷链接地址。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[3\] links字段数据结构说明

    <a name="table15913898194628"></a>
    <table><thead align="left"><tr id="row37608132194628"><th class="cellrowborder" valign="top" width="23.1%" id="mcps1.1.4.1.1"><p id="p1387423241319"><a name="p1387423241319"></a><a name="p1387423241319"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.790000000000003%" id="mcps1.1.4.1.2"><p id="p1487693221320"><a name="p1487693221320"></a><a name="p1487693221320"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.11%" id="mcps1.1.4.1.3"><p id="p187911326136"><a name="p187911326136"></a><a name="p187911326136"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17692319194628"><td class="cellrowborder" valign="top" width="23.1%" headers="mcps1.1.4.1.1 "><p id="p23791739194628"><a name="p23791739194628"></a><a name="p23791739194628"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.790000000000003%" headers="mcps1.1.4.1.2 "><p id="p48082703194628"><a name="p48082703194628"></a><a name="p48082703194628"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.11%" headers="mcps1.1.4.1.3 "><p id="p2384900194628"><a name="p2384900194628"></a><a name="p2384900194628"></a>快捷链接标记名称。</p>
    </td>
    </tr>
    <tr id="row21464106194628"><td class="cellrowborder" valign="top" width="23.1%" headers="mcps1.1.4.1.1 "><p id="p60871059194628"><a name="p60871059194628"></a><a name="p60871059194628"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.790000000000003%" headers="mcps1.1.4.1.2 "><p id="p31608752194628"><a name="p31608752194628"></a><a name="p31608752194628"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.11%" headers="mcps1.1.4.1.3 "><p id="p10172138194628"><a name="p10172138194628"></a><a name="p10172138194628"></a>对应快捷链接。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "flavors": [
            "name": "physical.84.medium",
            "links": [
                {
                    "href": "https://compute.region.eu-de.otc-tsi.de/v2/c685484a8cc2416b97260938705deb65/flavors/physical.84.medium",
                    "rel": "self"
                },
                {
                    "href": "https://compute.region.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/flavors/physical.84.medium",
                    "rel": "bookmark"
                 }
            ],
            "ram": 321725,
            "OS-FLV-DISABLED:disabled": false,
            "vcpus": 56,
            "swap": "",
            "os-flavor-access:is_public": true,
            "rxtx_factor": 1,
            "OS-FLV-EXT-DATA:ephemeral": 0,
            "disk": 3725,
            "id": "physical.84.medium"
        ]
    }
    ```


## 返回值<a name="section63081244"></a>

请参考[通用返回值](通用返回值.md)。

