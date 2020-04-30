# 查询裸金属服务器规格信息列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158684"></a>

## 功能介绍<a name="section57769674"></a>

查询裸金属服务器规格信息列表。

## 约束<a name="section60580832213029"></a>

本接口查询出来的规格为系统中所有的规格，其中规格的名称以“physical”开头的为裸金属服务器的规格，可用于申请裸金属服务器。

## URI<a name="section50165025"></a>

GET /v2.1/\{project\_id\}/flavors/detail\{?minDisk=\{minDisk\}&minRam=\{minRam\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table1687344817416)。

**表 1**  参数说明

<a name="table1687344817416"></a>
<table><thead align="left"><tr id="row138741548164116"><th class="cellrowborder" valign="top" width="25.47254725472547%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.45234523452345%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.07510751075108%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row28741048144119"><td class="cellrowborder" valign="top" width="25.47254725472547%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.45234523452345%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.07510751075108%" headers="mcps1.2.4.1.3 "><p id="p37195178"><a name="p37195178"></a><a name="p37195178"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

查询裸金属服务器规格时可选的查询检索参数如[表2](#table1719300427)所示。

**表 2**  可选的查询检索参数

<a name="table1719300427"></a>
<table><thead align="left"><tr id="row57253084215"><th class="cellrowborder" valign="top" width="20.830000000000002%" id="mcps1.2.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.39%" id="mcps1.2.5.1.2"><p id="p15431544654"><a name="p15431544654"></a><a name="p15431544654"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.07%" id="mcps1.2.5.1.3"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="38.71%" id="mcps1.2.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row107363044215"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p7618124412423"><a name="p7618124412423"></a><a name="p7618124412423"></a>minDisk</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p14421144857"><a name="p14421144857"></a><a name="p14421144857"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p26202446424"><a name="p26202446424"></a><a name="p26202446424"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p116242044134216"><a name="p116242044134216"></a><a name="p116242044134216"></a>最小的硬盘规格，单位GB，大于等于此规格的都可以查询到。</p>
</td>
</tr>
<tr id="row17730303422"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p1562994419427"><a name="p1562994419427"></a><a name="p1562994419427"></a>minRam</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p104224419515"><a name="p104224419515"></a><a name="p104224419515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p146323449428"><a name="p146323449428"></a><a name="p146323449428"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p863714412422"><a name="p863714412422"></a><a name="p863714412422"></a>最小的内存规格，单位MB，大于等于此规格的都可以查询到。</p>
</td>
</tr>
<tr id="row1673103013428"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p12651144417421"><a name="p12651144417421"></a><a name="p12651144417421"></a>sort_key</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p1040164413513"><a name="p1040164413513"></a><a name="p1040164413513"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p196558447427"><a name="p196558447427"></a><a name="p196558447427"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p366084404210"><a name="p366084404210"></a><a name="p366084404210"></a>排序字段，默认值为：flavorid。可以指定的其他key为name/ memory_mb/vcpus，/root_gb/flavorid。</p>
</td>
</tr>
<tr id="row87303017423"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.5.1.1 "><p id="p16663174412421"><a name="p16663174412421"></a><a name="p16663174412421"></a>sort_dir</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p104012441155"><a name="p104012441155"></a><a name="p104012441155"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.07%" headers="mcps1.2.5.1.3 "><p id="p466510447425"><a name="p466510447425"></a><a name="p466510447425"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="38.71%" headers="mcps1.2.5.1.4 "><p id="p381417538211"><a name="p381417538211"></a><a name="p381417538211"></a>升序/降序排序。</p>
<p id="p19672104424217"><a name="p19672104424217"></a><a name="p19672104424217"></a>可以指定的参数为asc/desc，默认值为：asc</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section48832041"></a>

-   请求参数

    无

-   请求样例
    -   不带可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail
        ```

    -   携带一个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail?minDisk=3725
        ```

    -   携带多个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/flavors/detail?minDisk=3725&is_public=true
        ```



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
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.1.4.1.2 "><p id="p62312200"><a name="p62312200"></a><a name="p62312200"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.970000000000006%" headers="mcps1.1.4.1.3 "><p id="p60002101"><a name="p60002101"></a><a name="p60002101"></a><span id="text18472201045814"><a name="text18472201045814"></a><a name="text18472201045814"></a>裸金属服务器</span><span id="text547221045820"><a name="text547221045820"></a><a name="text547221045820"></a></span>规格列表。详情请参见<a href="#table13194498">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  flavors数据结构说明

    <a name="table13194498"></a>
    <table><thead align="left"><tr id="row35873632"><th class="cellrowborder" valign="top" width="24.22%" id="mcps1.2.4.1.1"><p id="p1934639181313"><a name="p1934639181313"></a><a name="p1934639181313"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.46%" id="mcps1.2.4.1.2"><p id="p1134716921317"><a name="p1134716921317"></a><a name="p1134716921317"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.32%" id="mcps1.2.4.1.3"><p id="p535259131314"><a name="p535259131314"></a><a name="p535259131314"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15349251"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p35329809"><a name="p35329809"></a><a name="p35329809"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p24536113173145"><a name="p24536113173145"></a><a name="p24536113173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p56261663"><a name="p56261663"></a><a name="p56261663"></a><span id="text14927171275818"><a name="text14927171275818"></a><a name="text14927171275818"></a>裸金属服务器</span><span id="text1927171245813"><a name="text1927171245813"></a><a name="text1927171245813"></a></span>规格ID。</p>
    </td>
    </tr>
    <tr id="row36592919"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p11236435"><a name="p11236435"></a><a name="p11236435"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p54383891173145"><a name="p54383891173145"></a><a name="p54383891173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p61525259"><a name="p61525259"></a><a name="p61525259"></a><span id="text913422265820"><a name="text913422265820"></a><a name="text913422265820"></a>裸金属服务器</span><span id="text12134172216588"><a name="text12134172216588"></a><a name="text12134172216588"></a></span>规格名称。</p>
    </td>
    </tr>
    <tr id="row16856419"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p23192694"><a name="p23192694"></a><a name="p23192694"></a>vcpus</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p61992247173145"><a name="p61992247173145"></a><a name="p61992247173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p60827539"><a name="p60827539"></a><a name="p60827539"></a>该<span id="text771542415817"><a name="text771542415817"></a><a name="text771542415817"></a>裸金属服务器</span><span id="text77151424115815"><a name="text77151424115815"></a><a name="text77151424115815"></a></span>规格对应的CPU核数。</p>
    </td>
    </tr>
    <tr id="row3097644510336"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p3929432310349"><a name="p3929432310349"></a><a name="p3929432310349"></a>ram</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p51423198173145"><a name="p51423198173145"></a><a name="p51423198173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p154673810349"><a name="p154673810349"></a><a name="p154673810349"></a>该<span id="text193481527175811"><a name="text193481527175811"></a><a name="text193481527175811"></a>裸金属服务器</span><span id="text23482272589"><a name="text23482272589"></a><a name="text23482272589"></a></span>规格对应的内存大小，单位为MB。</p>
    </td>
    </tr>
    <tr id="row10576944"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p51426113"><a name="p51426113"></a><a name="p51426113"></a>disk</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p31344710173145"><a name="p31344710173145"></a><a name="p31344710173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p19756352"><a name="p19756352"></a><a name="p19756352"></a>该<span id="text495612955816"><a name="text495612955816"></a><a name="text495612955816"></a>裸金属服务器</span><span id="text1495610298587"><a name="text1495610298587"></a><a name="text1495610298587"></a></span>规格对应要求的磁盘大小，单位为GB。</p>
    </td>
    </tr>
    <tr id="row56760689"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p34213098"><a name="p34213098"></a><a name="p34213098"></a>swap</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p31087024173145"><a name="p31087024173145"></a><a name="p31087024173145"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p3906895110328"><a name="p3906895110328"></a><a name="p3906895110328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row56925253"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p47542785"><a name="p47542785"></a><a name="p47542785"></a>OS-FLV-EXT-DATA:ephemeral</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p18132829173145"><a name="p18132829173145"></a><a name="p18132829173145"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p2710719510328"><a name="p2710719510328"></a><a name="p2710719510328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row44806966"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p5485596"><a name="p5485596"></a><a name="p5485596"></a>OS-FLV-DISABLED:disabled</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p52585611173145"><a name="p52585611173145"></a><a name="p52585611173145"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p3113915110328"><a name="p3113915110328"></a><a name="p3113915110328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row42184651"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p61513540"><a name="p61513540"></a><a name="p61513540"></a>rxtx_factor</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p7527547173145"><a name="p7527547173145"></a><a name="p7527547173145"></a>Float</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p1764564010328"><a name="p1764564010328"></a><a name="p1764564010328"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row51313205"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p62728917"><a name="p62728917"></a><a name="p62728917"></a>os-flavor-access:is_public</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p43117912173145"><a name="p43117912173145"></a><a name="p43117912173145"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p3503996211722"><a name="p3503996211722"></a><a name="p3503996211722"></a>未使用。</p>
    </td>
    </tr>
    <tr id="row2047803919452"><td class="cellrowborder" valign="top" width="24.22%" headers="mcps1.2.4.1.1 "><p id="p6509154919455"><a name="p6509154919455"></a><a name="p6509154919455"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.46%" headers="mcps1.2.4.1.2 "><p id="p3792414219455"><a name="p3792414219455"></a><a name="p3792414219455"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.4.1.3 "><p id="p6495712119455"><a name="p6495712119455"></a><a name="p6495712119455"></a>规格相关快捷链接地址。详情请参见<a href="#table15913898194628">表4</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  links字段数据结构说明

    <a name="table15913898194628"></a>
    <table><thead align="left"><tr id="row37608132194628"><th class="cellrowborder" valign="top" width="23.1%" id="mcps1.2.4.1.1"><p id="p1387423241319"><a name="p1387423241319"></a><a name="p1387423241319"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.790000000000003%" id="mcps1.2.4.1.2"><p id="p1487693221320"><a name="p1487693221320"></a><a name="p1487693221320"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.11%" id="mcps1.2.4.1.3"><p id="p187911326136"><a name="p187911326136"></a><a name="p187911326136"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17692319194628"><td class="cellrowborder" valign="top" width="23.1%" headers="mcps1.2.4.1.1 "><p id="p23791739194628"><a name="p23791739194628"></a><a name="p23791739194628"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.790000000000003%" headers="mcps1.2.4.1.2 "><p id="p48082703194628"><a name="p48082703194628"></a><a name="p48082703194628"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.11%" headers="mcps1.2.4.1.3 "><p id="p2384900194628"><a name="p2384900194628"></a><a name="p2384900194628"></a>快捷链接标记名称。</p>
    <a name="ul207311644172510"></a><a name="ul207311644172510"></a><ul id="ul207311644172510"><li>self：包含版本号的资源链接，需要立即跟踪时使用此类链接。</li><li>bookmark：提供了适合长期存储的资源链接。</li></ul>
    </td>
    </tr>
    <tr id="row21464106194628"><td class="cellrowborder" valign="top" width="23.1%" headers="mcps1.2.4.1.1 "><p id="p60871059194628"><a name="p60871059194628"></a><a name="p60871059194628"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.790000000000003%" headers="mcps1.2.4.1.2 "><p id="p31608752194628"><a name="p31608752194628"></a><a name="p31608752194628"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.11%" headers="mcps1.2.4.1.3 "><p id="p10172138194628"><a name="p10172138194628"></a><a name="p10172138194628"></a>对应快捷链接。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "flavors": [
            {
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
                "ram": 321725,
                "OS-FLV-DISABLED:disabled": false,
                "vcpus": 56,
                "swap": "",
                "os-flavor-access:is_public": true,
                "rxtx_factor": 1,
                "OS-FLV-EXT-DATA:ephemeral": 0,
                "disk": 3725,
                "id": "physical.o2.medium"
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

