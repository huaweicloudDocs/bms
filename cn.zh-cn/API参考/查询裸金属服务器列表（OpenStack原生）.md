# 查询裸金属服务器列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158693"></a>

## 功能介绍<a name="section56354875"></a>

查询裸金属服务器信息列表，接口版本为v2.1，支持带微版本号查询。在请求Header中增加一组Key-Value值， Key固定为“X-OpenStack-Nova-API-Version” ，Value为可选的微版本号，例如“2.26”。表示使用微版本号为2.26进行查询。

## 约束<a name="section54054835151740"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section37431827"></a>

GET /v2.1/\{project\_id\}/servers

参数说明请参见[表1](#table67612156510)。

**表 1**  参数说明

<a name="table67612156510"></a>
<table><thead align="left"><tr id="row67810155512"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p47678793154517"><a name="p47678793154517"></a><a name="p47678793154517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p62557569154517"><a name="p62557569154517"></a><a name="p62557569154517"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p37549795154517"><a name="p37549795154517"></a><a name="p37549795154517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17821535110"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1019106154517"><a name="p1019106154517"></a><a name="p1019106154517"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p15438763154517"><a name="p15438763154517"></a><a name="p15438763154517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p42580325154517"><a name="p42580325154517"></a><a name="p42580325154517"></a>项目ID。</p>
</td>
</tr>
</tbody>
</table>

查询裸金属服务器列表时，可选的查询检视参数如[表2](#table1758718426522)所示。

**表 2**  可选的查询检视参数

<a name="table1758718426522"></a>
<table><thead align="left"><tr id="row1458874235211"><th class="cellrowborder" valign="top" width="19.85%" id="mcps1.2.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.39%" id="mcps1.2.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="18.75%" id="mcps1.2.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="41.010000000000005%" id="mcps1.2.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16588164215216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p17387161075313"><a name="p17387161075313"></a><a name="p17387161075313"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p123900108538"><a name="p123900108538"></a><a name="p123900108538"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p2393161013538"><a name="p2393161013538"></a><a name="p2393161013538"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p1339701010533"><a name="p1339701010533"></a><a name="p1339701010533"></a>镜像ID。</p>
</td>
</tr>
<tr id="row05881842195216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p839991012531"><a name="p839991012531"></a><a name="p839991012531"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p12402210155311"><a name="p12402210155311"></a><a name="p12402210155311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p15406610135318"><a name="p15406610135318"></a><a name="p15406610135318"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p1040881015311"><a name="p1040881015311"></a><a name="p1040881015311"></a>规格ID。</p>
</td>
</tr>
<tr id="row058811420527"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p5413201085313"><a name="p5413201085313"></a><a name="p5413201085313"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p1941781012535"><a name="p1941781012535"></a><a name="p1941781012535"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p3422121055318"><a name="p3422121055318"></a><a name="p3422121055318"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p842631015536"><a name="p842631015536"></a><a name="p842631015536"></a>裸金属服务器名称，使用模糊匹配的方式查询。</p>
<p id="p7429181015313"><a name="p7429181015313"></a><a name="p7429181015313"></a>例如，“?name=bob”正则表达式会同时返回bob和bobb。如果必须仅匹配bob，则可以使用与基础数据库服务器的语法相匹配的正则表达式，如MySQL或PostgreSQL（官方网站：<a href="https://www.postgresql.org/docs/9.2/static/functions-matching.html" target="_blank" rel="noopener noreferrer">https://www.postgresql.org/docs/9.2/static/functions-matching.html</a>）。</p>
</td>
</tr>
<tr id="row105881642195217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p1743421075315"><a name="p1743421075315"></a><a name="p1743421075315"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p843711020539"><a name="p843711020539"></a><a name="p843711020539"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p11440101010537"><a name="p11440101010537"></a><a name="p11440101010537"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p7441161020531"><a name="p7441161020531"></a><a name="p7441161020531"></a>裸金属服务器状态，只有管理员可以使用“deleted”状态过滤查询已经删除的裸金属服务器。</p>
</td>
</tr>
<tr id="row16588142145219"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p10447191065310"><a name="p10447191065310"></a><a name="p10447191065310"></a>changes-since</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p644915104533"><a name="p644915104533"></a><a name="p644915104533"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p13454131016536"><a name="p13454131016536"></a><a name="p13454131016536"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p445791014538"><a name="p445791014538"></a><a name="p445791014538"></a>过滤在changes-since时间之后更新过的裸金属服务器。格式为ISO8601时间格式，例如：2013-06-09T06:42:18Z。</p>
</td>
</tr>
<tr id="row11588114205218"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p2463171085314"><a name="p2463171085314"></a><a name="p2463171085314"></a>all_tenants</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p11467141018532"><a name="p11467141018532"></a><a name="p11467141018532"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p1547116106534"><a name="p1547116106534"></a><a name="p1547116106534"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p12473710165311"><a name="p12473710165311"></a><a name="p12473710165311"></a>是否查询所有租户的裸金属服务器，只有管理员才能使用；0表示不查询，1表示查询。</p>
</td>
</tr>
<tr id="row1588204214521"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p697153165318"><a name="p697153165318"></a><a name="p697153165318"></a>ip</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p1397453185317"><a name="p1397453185317"></a><a name="p1397453185317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p597743111535"><a name="p597743111535"></a><a name="p597743111535"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p798123113539"><a name="p798123113539"></a><a name="p798123113539"></a>IP地址，使用模糊匹配查询。</p>
</td>
</tr>
<tr id="row2588542125217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p99841631185310"><a name="p99841631185310"></a><a name="p99841631185310"></a>deleted</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p398743135316"><a name="p398743135316"></a><a name="p398743135316"></a>boolean</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p19911631205315"><a name="p19911631205315"></a><a name="p19911631205315"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p999613318537"><a name="p999613318537"></a><a name="p999613318537"></a>过滤查询已经删除的裸金属服务器，只有管理员可以使用。</p>
</td>
</tr>
<tr id="row165888428529"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p011232155315"><a name="p011232155315"></a><a name="p011232155315"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p15443216530"><a name="p15443216530"></a><a name="p15443216530"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p128193255311"><a name="p128193255311"></a><a name="p128193255311"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p3111132145315"><a name="p3111132145315"></a><a name="p3111132145315"></a>tags列表。返回匹配全部tags的裸金属服务器。多个tag使用逗号分隔。</p>
<p id="p1813132175314"><a name="p1813132175314"></a><a name="p1813132175314"></a>微版本2.26新增</p>
</td>
</tr>
<tr id="row4588942165217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p1186328533"><a name="p1186328533"></a><a name="p1186328533"></a>tags-any</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p1523532135315"><a name="p1523532135315"></a><a name="p1523532135315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p1325113235310"><a name="p1325113235310"></a><a name="p1325113235310"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p8281832205311"><a name="p8281832205311"></a><a name="p8281832205311"></a>tags列表。返回匹配任意tags的裸金属服务器。多个tag使用逗号分隔。</p>
<p id="p1631113212539"><a name="p1631113212539"></a><a name="p1631113212539"></a>微版本2.26新增</p>
</td>
</tr>
<tr id="row1658884211523"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p203418324539"><a name="p203418324539"></a><a name="p203418324539"></a>not-tags</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p173673215532"><a name="p173673215532"></a><a name="p173673215532"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p238132105317"><a name="p238132105317"></a><a name="p238132105317"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p154313328536"><a name="p154313328536"></a><a name="p154313328536"></a>tags列表。返回不匹配全部tags的裸金属服务器。多个tag使用逗号分隔。</p>
<p id="p19441232135317"><a name="p19441232135317"></a><a name="p19441232135317"></a>微版本2.26新增</p>
</td>
</tr>
<tr id="row1158812424528"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p184717323539"><a name="p184717323539"></a><a name="p184717323539"></a>not-tags-any</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p1650832195311"><a name="p1650832195311"></a><a name="p1650832195311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p1453143220535"><a name="p1453143220535"></a><a name="p1453143220535"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p5551832185311"><a name="p5551832185311"></a><a name="p5551832185311"></a>tags列表。返回不匹配任意tags的裸金属服务器。多个tag使用逗号分隔。</p>
<p id="p45753218534"><a name="p45753218534"></a><a name="p45753218534"></a>微版本2.26新增</p>
</td>
</tr>
<tr id="row1758864217526"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p10633321531"><a name="p10633321531"></a><a name="p10633321531"></a>sort_key</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p106613212531"><a name="p106613212531"></a><a name="p106613212531"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p196963275311"><a name="p196963275311"></a><a name="p196963275311"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p167133212536"><a name="p167133212536"></a><a name="p167133212536"></a>用于排序的属性，包括uuid（裸金属服务器的uuid）、vm_state（裸金属服务器的状态）、display_name（裸金属服务器名称）、task_state（裸金属服务器任务状态）、power_state（电源状态）、created_at（创建时间）、updated_at（更新时间）、availability_zone（可用分区）。可以指定多对sort_key和sort_dir。</p>
</td>
</tr>
<tr id="row135891242165217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.2.5.1.1 "><p id="p1327414444539"><a name="p1327414444539"></a><a name="p1327414444539"></a>sort_dir</p>
</td>
<td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.2.5.1.2 "><p id="p16275104445317"><a name="p16275104445317"></a><a name="p16275104445317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.2.5.1.3 "><p id="p202804443536"><a name="p202804443536"></a><a name="p202804443536"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="p15283154425314"><a name="p15283154425314"></a><a name="p15283154425314"></a>排序方向。</p>
<a name="ul22858441530"></a><a name="ul22858441530"></a><ul id="ul22858441530"><li>asc：升序</li><li>desc：降序（默认值）</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1342126"></a>

不涉及。

## 响应消息<a name="section12079142"></a>

-   响应参数

    <a name="table44736746"></a>
    <table><thead align="left"><tr id="row8242429"><th class="cellrowborder" valign="top" width="23.36%" id="mcps1.1.4.1.1"><p id="p09797427505"><a name="p09797427505"></a><a name="p09797427505"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.22%" id="mcps1.1.4.1.2"><p id="p8982164210504"><a name="p8982164210504"></a><a name="p8982164210504"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.42%" id="mcps1.1.4.1.3"><p id="p1898519426507"><a name="p1898519426507"></a><a name="p1898519426507"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row18745119"><td class="cellrowborder" valign="top" width="23.36%" headers="mcps1.1.4.1.1 "><p id="p41959665"><a name="p41959665"></a><a name="p41959665"></a>servers</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.22%" headers="mcps1.1.4.1.2 "><p id="p16804102"><a name="p16804102"></a><a name="p16804102"></a>列表数据结构[2]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.42%" headers="mcps1.1.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a>裸金属服务器信息列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] servers字段数据结构说明

    <a name="table11253402"></a>
    <table><thead align="left"><tr id="row10267559"><th class="cellrowborder" valign="top" width="23.599999999999998%" id="mcps1.1.4.1.1"><p id="p689134705020"><a name="p689134705020"></a><a name="p689134705020"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.380000000000003%" id="mcps1.1.4.1.2"><p id="p79316472500"><a name="p79316472500"></a><a name="p79316472500"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.019999999999996%" id="mcps1.1.4.1.3"><p id="p1991747185016"><a name="p1991747185016"></a><a name="p1991747185016"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15663"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.1.4.1.1 "><p id="p1268752"><a name="p1268752"></a><a name="p1268752"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.1.4.1.2 "><p id="p2786131"><a name="p2786131"></a><a name="p2786131"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.1.4.1.3 "><p id="p24350086"><a name="p24350086"></a><a name="p24350086"></a>裸金属服务器名称。</p>
    </td>
    </tr>
    <tr id="row17824184"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.1.4.1.1 "><p id="p34472770"><a name="p34472770"></a><a name="p34472770"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.1.4.1.2 "><p id="p18974148"><a name="p18974148"></a><a name="p18974148"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.1.4.1.3 "><p id="p60510987"><a name="p60510987"></a><a name="p60510987"></a>裸金属服务器唯一标识。</p>
    </td>
    </tr>
    <tr id="row7727977"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.1.4.1.1 "><p id="p21986423"><a name="p21986423"></a><a name="p21986423"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.1.4.1.2 "><p id="p14181463161150"><a name="p14181463161150"></a><a name="p14181463161150"></a>列表数据结构[3]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.1.4.1.3 "><p id="p52375797"><a name="p52375797"></a><a name="p52375797"></a>裸金属服务器相关快捷链接信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[3\] links字段数据结构说明

    <a name="table64121649"></a>
    <table><thead align="left"><tr id="row59320951"><th class="cellrowborder" valign="top" width="23.86%" id="mcps1.1.4.1.1"><p id="p189635514509"><a name="p189635514509"></a><a name="p189635514509"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.240000000000002%" id="mcps1.1.4.1.2"><p id="p79654516507"><a name="p79654516507"></a><a name="p79654516507"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.9%" id="mcps1.1.4.1.3"><p id="p12968551135019"><a name="p12968551135019"></a><a name="p12968551135019"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row61486274"><td class="cellrowborder" valign="top" width="23.86%" headers="mcps1.1.4.1.1 "><p id="p14332335"><a name="p14332335"></a><a name="p14332335"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.1.4.1.2 "><p id="p14933841"><a name="p14933841"></a><a name="p14933841"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.1.4.1.3 "><p id="p1681623"><a name="p1681623"></a><a name="p1681623"></a>快捷链接标记名称。</p>
    </td>
    </tr>
    <tr id="row15134612"><td class="cellrowborder" valign="top" width="23.86%" headers="mcps1.1.4.1.1 "><p id="p17944037"><a name="p17944037"></a><a name="p17944037"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.1.4.1.2 "><p id="p21885054"><a name="p21885054"></a><a name="p21885054"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.1.4.1.3 "><p id="p27858965"><a name="p27858965"></a><a name="p27858965"></a>对应快捷链接。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "servers": [
            {
                "name": "bms",
                "links": [
                    {
                        "rel": "self",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/v2.1/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8b-4bc5-ae46-69cacfd4fbaa"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
                    }
                ],
                "id": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
            }
        ]
    }
    ```


## 返回值<a name="section41603419"></a>

请参考[通用返回值](通用返回值.md)。

