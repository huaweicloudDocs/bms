# 查询裸金属服务器列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158693"></a>

## 功能介绍<a name="section56354875"></a>

查询裸金属服务器信息列表。

## 约束<a name="section54054835151740"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section37431827"></a>

GET /v2.1/\{project\_id\}/servers\{?changes-since=\{changes-since\}&image=\{image\}&flavor=\{flavor\}&name=\{name\}&status=\{status\}&limit=\{limit\}&marker=\{marker\}&tags=\{tags\}&not-tags=\{not-tags\}&reservation\_id=\{reservation\_id\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table67612156510)。

**表 1**  参数说明

<a name="table67612156510"></a>
<table><thead align="left"><tr id="row67810155512"><th class="cellrowborder" valign="top" width="25.83258325832583%" id="mcps1.2.4.1.1"><p id="p47678793154517"><a name="p47678793154517"></a><a name="p47678793154517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.71257125712571%" id="mcps1.2.4.1.2"><p id="p62557569154517"><a name="p62557569154517"></a><a name="p62557569154517"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.45484548454845%" id="mcps1.2.4.1.3"><p id="p37549795154517"><a name="p37549795154517"></a><a name="p37549795154517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17821535110"><td class="cellrowborder" valign="top" width="25.83258325832583%" headers="mcps1.2.4.1.1 "><p id="p1019106154517"><a name="p1019106154517"></a><a name="p1019106154517"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.71257125712571%" headers="mcps1.2.4.1.2 "><p id="p15438763154517"><a name="p15438763154517"></a><a name="p15438763154517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.45484548454845%" headers="mcps1.2.4.1.3 "><p id="p42580325154517"><a name="p42580325154517"></a><a name="p42580325154517"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section131361554145510"></a>

-   请求参数

    <a name="table1758718426522"></a>
    <table><thead align="left"><tr id="row1458874235211"><th class="cellrowborder" valign="top" width="19.85%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.39%" id="mcps1.1.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.75%" id="mcps1.1.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="41.010000000000005%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row686311283276"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p10447191065310"><a name="p10447191065310"></a><a name="p10447191065310"></a>changes-since</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p644915104533"><a name="p644915104533"></a><a name="p644915104533"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p13454131016536"><a name="p13454131016536"></a><a name="p13454131016536"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p445791014538"><a name="p445791014538"></a><a name="p445791014538"></a><span id="text121698161638"><a name="text121698161638"></a><a name="text121698161638"></a>裸金属服务器</span><span id="text216912161937"><a name="text216912161937"></a><a name="text216912161937"></a></span>上次更新状态的时间戳信息。格式为ISO 8601时间格式，例如：2013-06-09T06:42:18Z。</p>
    </td>
    </tr>
    <tr id="row16588164215216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p17387161075313"><a name="p17387161075313"></a><a name="p17387161075313"></a>image</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p123900108538"><a name="p123900108538"></a><a name="p123900108538"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p2393161013538"><a name="p2393161013538"></a><a name="p2393161013538"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p1339701010533"><a name="p1339701010533"></a><a name="p1339701010533"></a>镜像ID。</p>
    <p id="p1870622242917"><a name="p1870622242917"></a><a name="p1870622242917"></a>可以在镜像服务控制台查询，也可以调用“<a href="https://support.huaweicloud.com/api-ims/ims_03_0602.html" target="_blank" rel="noopener noreferrer">查询镜像列表</a>”API获取。</p>
    <div class="note" id="note623794911339"><a name="note623794911339"></a><a name="note623794911339"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p17237114943316"><a name="p17237114943316"></a><a name="p17237114943316"></a>在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row05881842195216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p839991012531"><a name="p839991012531"></a><a name="p839991012531"></a>flavor</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p12402210155311"><a name="p12402210155311"></a><a name="p12402210155311"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p15406610135318"><a name="p15406610135318"></a><a name="p15406610135318"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p1040881015311"><a name="p1040881015311"></a><a name="p1040881015311"></a>规格ID。</p>
    <p id="p7741128113511"><a name="p7741128113511"></a><a name="p7741128113511"></a>可以在<span id="text9235625735"><a name="text9235625735"></a><a name="text9235625735"></a>裸金属服务器</span><span id="text32351725734"><a name="text32351725734"></a><a name="text32351725734"></a></span>控制台查询，也可以调用<a href="查询裸金属服务器规格信息列表（OpenStack原生）.md">查询裸金属服务器规格信息列表（OpenStack原生）</a>API获取。</p>
    </td>
    </tr>
    <tr id="row058811420527"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p5413201085313"><a name="p5413201085313"></a><a name="p5413201085313"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p1941781012535"><a name="p1941781012535"></a><a name="p1941781012535"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p3422121055318"><a name="p3422121055318"></a><a name="p3422121055318"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p842631015536"><a name="p842631015536"></a><a name="p842631015536"></a><span id="text13209132811312"><a name="text13209132811312"></a><a name="text13209132811312"></a>裸金属服务器</span><span id="text920922816319"><a name="text920922816319"></a><a name="text920922816319"></a></span>名称，使用模糊匹配的方式查询。</p>
    <p id="p7429181015313"><a name="p7429181015313"></a><a name="p7429181015313"></a>例如，“?name=bob”正则表达式会同时返回bob和bobb。如果必须仅匹配bob，则可以使用与基础数据库服务器的语法相匹配的正则表达式，如MySQL或PostgreSQL（官方网站：<a href="https://www.postgresql.org/docs/9.2/static/functions-matching.html" target="_blank" rel="noopener noreferrer">https://www.postgresql.org/docs/9.2/static/functions-matching.html</a>）。</p>
    </td>
    </tr>
    <tr id="row105881642195217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p1743421075315"><a name="p1743421075315"></a><a name="p1743421075315"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p843711020539"><a name="p843711020539"></a><a name="p843711020539"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p11440101010537"><a name="p11440101010537"></a><a name="p11440101010537"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p7441161020531"><a name="p7441161020531"></a><a name="p7441161020531"></a><span id="text4817131535"><a name="text4817131535"></a><a name="text4817131535"></a>裸金属服务器</span><span id="text1781773117312"><a name="text1781773117312"></a><a name="text1781773117312"></a></span>状态。</p>
    <p id="p117067951617"><a name="p117067951617"></a><a name="p117067951617"></a>取值范围：</p>
    <a name="ul29109448426"></a><a name="ul29109448426"></a><ul id="ul29109448426"><li>ACTIVE：运行中/正在关机/删除中</li><li>BUILD：创建中</li><li>ERROR：故障</li><li>HARD_REBOOT：强制重启中</li><li>REBOOT：重启中</li><li>SHUTOFF：关机/正在开机/删除中/重建中/重装操作系统中/重装操作系统失败/冻结</li></ul>
    </td>
    </tr>
    <tr id="row16588142145219"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p1445843114279"><a name="p1445843114279"></a><a name="p1445843114279"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p15457103122713"><a name="p15457103122713"></a><a name="p15457103122713"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p15455113112714"><a name="p15455113112714"></a><a name="p15455113112714"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p345110316275"><a name="p345110316275"></a><a name="p345110316275"></a>每页返回<span id="text59831335739"><a name="text59831335739"></a><a name="text59831335739"></a>裸金属服务器</span><span id="text1098373515319"><a name="text1098373515319"></a><a name="text1098373515319"></a></span>的条数。</p>
    </td>
    </tr>
    <tr id="row12307152919453"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p34602410233"><a name="p34602410233"></a><a name="p34602410233"></a>marker</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p1946094112310"><a name="p1946094112310"></a><a name="p1946094112310"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p14460249231"><a name="p14460249231"></a><a name="p14460249231"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p174601046239"><a name="p174601046239"></a><a name="p174601046239"></a>从marker指定的<span id="text71323381731"><a name="text71323381731"></a><a name="text71323381731"></a>裸金属服务器</span><span id="text613212389311"><a name="text613212389311"></a><a name="text613212389311"></a></span>ID的下一条数据开始查询。</p>
    </td>
    </tr>
    <tr id="row14320610478"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p5324615479"><a name="p5324615479"></a><a name="p5324615479"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p143218664715"><a name="p143218664715"></a><a name="p143218664715"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p143211619479"><a name="p143211619479"></a><a name="p143211619479"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p123246194714"><a name="p123246194714"></a><a name="p123246194714"></a>查询tag字段中包含该值的<span id="text142391140333"><a name="text142391140333"></a><a name="text142391140333"></a>裸金属服务器</span><span id="text162393401630"><a name="text162393401630"></a><a name="text162393401630"></a></span>。</p>
    <p id="p12820165216471"><a name="p12820165216471"></a><a name="p12820165216471"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="row1658884211523"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p203418324539"><a name="p203418324539"></a><a name="p203418324539"></a>not-tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p173673215532"><a name="p173673215532"></a><a name="p173673215532"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p238132105317"><a name="p238132105317"></a><a name="p238132105317"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p154313328536"><a name="p154313328536"></a><a name="p154313328536"></a>查询tag字段中不包含该值的<span id="text179892421232"><a name="text179892421232"></a><a name="text179892421232"></a>裸金属服务器</span><span id="text149891342231"><a name="text149891342231"></a><a name="text149891342231"></a></span>，值为标签的Key。</p>
    <div class="note" id="note124521913175616"><a name="note124521913175616"></a><a name="note124521913175616"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1745221311560"><a name="p1745221311560"></a><a name="p1745221311560"></a>如果之前添加的Tag为“Key.Value”的形式，则查询的时候需要使用“Key”来查询。</p>
    <p id="p213418685710"><a name="p213418685710"></a><a name="p213418685710"></a>例如：之前添加的tag为“a.b”,则升级后，查询时需使用“not-tags=a”。</p>
    </div></div>
    <p id="p19441232135317"><a name="p19441232135317"></a><a name="p19441232135317"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="row1158812424528"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p184717323539"><a name="p184717323539"></a><a name="p184717323539"></a>reservation_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p1650832195311"><a name="p1650832195311"></a><a name="p1650832195311"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p1453143220535"><a name="p1453143220535"></a><a name="p1453143220535"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p5551832185311"><a name="p5551832185311"></a><a name="p5551832185311"></a>批量创建<span id="text63205019314"><a name="text63205019314"></a><a name="text63205019314"></a>裸金属服务器</span><span id="text734501833"><a name="text734501833"></a><a name="text734501833"></a></span>时，指定该预留ID，可以查询同批次创建的<span id="text281110523312"><a name="text281110523312"></a><a name="text281110523312"></a>裸金属服务器</span><span id="text281195211313"><a name="text281195211313"></a><a name="text281195211313"></a></span>。</p>
    <p id="p45753218534"><a name="p45753218534"></a><a name="p45753218534"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="row1758864217526"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p10633321531"><a name="p10633321531"></a><a name="p10633321531"></a>sort_key</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p106613212531"><a name="p106613212531"></a><a name="p106613212531"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p196963275311"><a name="p196963275311"></a><a name="p196963275311"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p167133212536"><a name="p167133212536"></a><a name="p167133212536"></a>用于排序的属性，包括uuid（<span id="text62627567316"><a name="text62627567316"></a><a name="text62627567316"></a>裸金属服务器</span><span id="text1726217563313"><a name="text1726217563313"></a><a name="text1726217563313"></a></span>的uuid）、vm_state（<span id="text142381559638"><a name="text142381559638"></a><a name="text142381559638"></a>裸金属服务器</span><span id="text22392599316"><a name="text22392599316"></a><a name="text22392599316"></a></span>的状态）、display_name（<span id="text135136112411"><a name="text135136112411"></a><a name="text135136112411"></a>裸金属服务器</span><span id="text6513116415"><a name="text6513116415"></a><a name="text6513116415"></a></span>名称）、task_state（<span id="text1810916516416"><a name="text1810916516416"></a><a name="text1810916516416"></a>裸金属服务器</span><span id="text17109175241"><a name="text17109175241"></a><a name="text17109175241"></a></span>任务状态）、power_state（电源状态）、created_at（创建时间）、updated_at（更新时间）、availability_zone（可用区）。可以指定多对sort_key和sort_dir。</p>
    <p id="p1321581482211"><a name="p1321581482211"></a><a name="p1321581482211"></a>默认排序顺序为created_at逆序。</p>
    </td>
    </tr>
    <tr id="row135891242165217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="p1327414444539"><a name="p1327414444539"></a><a name="p1327414444539"></a>sort_dir</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="p16275104445317"><a name="p16275104445317"></a><a name="p16275104445317"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="p202804443536"><a name="p202804443536"></a><a name="p202804443536"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="p15283154425314"><a name="p15283154425314"></a><a name="p15283154425314"></a>排序方向。</p>
    <a name="ul22858441530"></a><a name="ul22858441530"></a><ul id="ul22858441530"><li>asc：升序</li><li>desc：降序（默认值）</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例
    -   不带可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers
        ```

    -   携带一个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers?tags=__type_baremetal
        ```

    -   携带多个可选参数

        ```
        GET https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers?tags=__type_baremetal&name=bms-test01
        ```



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
    <td class="cellrowborder" valign="top" width="25.22%" headers="mcps1.1.4.1.2 "><p id="p16804102"><a name="p16804102"></a><a name="p16804102"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.42%" headers="mcps1.1.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a><span id="text542414112416"><a name="text542414112416"></a><a name="text542414112416"></a>裸金属服务器</span><span id="text74251911344"><a name="text74251911344"></a><a name="text74251911344"></a></span>信息列表。详情请参见<a href="#table11253402">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  servers字段数据结构说明

    <a name="table11253402"></a>
    <table><thead align="left"><tr id="row10267559"><th class="cellrowborder" valign="top" width="23.599999999999998%" id="mcps1.2.4.1.1"><p id="p689134705020"><a name="p689134705020"></a><a name="p689134705020"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.380000000000003%" id="mcps1.2.4.1.2"><p id="p79316472500"><a name="p79316472500"></a><a name="p79316472500"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.019999999999996%" id="mcps1.2.4.1.3"><p id="p1991747185016"><a name="p1991747185016"></a><a name="p1991747185016"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15663"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.1 "><p id="p1268752"><a name="p1268752"></a><a name="p1268752"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.2.4.1.2 "><p id="p2786131"><a name="p2786131"></a><a name="p2786131"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.2.4.1.3 "><p id="p24350086"><a name="p24350086"></a><a name="p24350086"></a><span id="text46502131440"><a name="text46502131440"></a><a name="text46502131440"></a>裸金属服务器</span><span id="text16500131412"><a name="text16500131412"></a><a name="text16500131412"></a></span>名称。</p>
    </td>
    </tr>
    <tr id="row17824184"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.1 "><p id="p34472770"><a name="p34472770"></a><a name="p34472770"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.2.4.1.2 "><p id="p18974148"><a name="p18974148"></a><a name="p18974148"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.2.4.1.3 "><p id="p60510987"><a name="p60510987"></a><a name="p60510987"></a><span id="text163215161641"><a name="text163215161641"></a><a name="text163215161641"></a>裸金属服务器</span><span id="text6321216147"><a name="text6321216147"></a><a name="text6321216147"></a></span>唯一标识。</p>
    </td>
    </tr>
    <tr id="row7727977"><td class="cellrowborder" valign="top" width="23.599999999999998%" headers="mcps1.2.4.1.1 "><p id="p21986423"><a name="p21986423"></a><a name="p21986423"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.380000000000003%" headers="mcps1.2.4.1.2 "><p id="p14181463161150"><a name="p14181463161150"></a><a name="p14181463161150"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.019999999999996%" headers="mcps1.2.4.1.3 "><p id="p52375797"><a name="p52375797"></a><a name="p52375797"></a><span id="text14899617746"><a name="text14899617746"></a><a name="text14899617746"></a>裸金属服务器</span><span id="text28997171941"><a name="text28997171941"></a><a name="text28997171941"></a></span>相关快捷链接信息。详情请参见<a href="#table64121649">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  links字段数据结构说明

    <a name="table64121649"></a>
    <table><thead align="left"><tr id="row59320951"><th class="cellrowborder" valign="top" width="23.86%" id="mcps1.2.4.1.1"><p id="p189635514509"><a name="p189635514509"></a><a name="p189635514509"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.240000000000002%" id="mcps1.2.4.1.2"><p id="p79654516507"><a name="p79654516507"></a><a name="p79654516507"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.9%" id="mcps1.2.4.1.3"><p id="p12968551135019"><a name="p12968551135019"></a><a name="p12968551135019"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row61486274"><td class="cellrowborder" valign="top" width="23.86%" headers="mcps1.2.4.1.1 "><p id="p14332335"><a name="p14332335"></a><a name="p14332335"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.4.1.2 "><p id="p14933841"><a name="p14933841"></a><a name="p14933841"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.4.1.3 "><p id="p1681623"><a name="p1681623"></a><a name="p1681623"></a>快捷链接标记名称。取值为：</p>
    <a name="ul207311644172510"></a><a name="ul207311644172510"></a><ul id="ul207311644172510"><li>self：包含版本号的资源链接，需要立即跟踪时使用此类链接。</li><li>bookmark：提供了适合长期存储的资源链接。</li></ul>
    </td>
    </tr>
    <tr id="row15134612"><td class="cellrowborder" valign="top" width="23.86%" headers="mcps1.2.4.1.1 "><p id="p17944037"><a name="p17944037"></a><a name="p17944037"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.240000000000002%" headers="mcps1.2.4.1.2 "><p id="p21885054"><a name="p21885054"></a><a name="p21885054"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.4.1.3 "><p id="p27858965"><a name="p27858965"></a><a name="p27858965"></a>对应快捷链接。</p>
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
                        "href": "https://openstack.example.com/v2.1/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8b-4bc5-ae46-69cacfd4fbaa"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/servers/820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
                    }
                ],
                "id": "820abbd0-2d8e-4bc5-ae46-69cacfd4fbaa"
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

