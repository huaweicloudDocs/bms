# 查询裸金属服务器详情列表（OpenStack原生）<a name="ZH-CN_TOPIC_0053158679"></a>

## 功能介绍<a name="section33716833"></a>

查询裸金属服务器详情信息列表。

## 约束<a name="section29822855153557"></a>

-   该接口查询到的列表包括ECS和BMS全量列表，需要用户根据flavor或者创建时添加的tag信息进行进一步过滤。
-   用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。

## URI<a name="section35016046"></a>

GET /v2.1/\{project\_id\}/servers/detail\{?changes-since=\{changes-since\}&image=\{image\}&flavor=\{flavor\}&name=\{name\}&status=\{status\}&limit=\{limit\}&marker=\{marker\}&tags=\{tags\}&not-tags=\{not-tags\}&reservation\_id=\{reservation\_id\}&sort\_key=\{sort\_key\}&sort\_dir=\{sort\_dir\}\}

参数说明请参见[表1](#table0524112565)。

**表 1**  参数说明

<a name="table0524112565"></a>
<table><thead align="left"><tr id="row252211165610"><th class="cellrowborder" valign="top" width="26.25262526252625%" id="mcps1.2.4.1.1"><p id="p55073076202321"><a name="p55073076202321"></a><a name="p55073076202321"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.58255825582558%" id="mcps1.2.4.1.2"><p id="p44659366114813"><a name="p44659366114813"></a><a name="p44659366114813"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.16481648164816%" id="mcps1.2.4.1.3"><p id="p19572211"><a name="p19572211"></a><a name="p19572211"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1524119564"><td class="cellrowborder" valign="top" width="26.25262526252625%" headers="mcps1.2.4.1.1 "><p id="p6789122714241"><a name="p6789122714241"></a><a name="p6789122714241"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.58255825582558%" headers="mcps1.2.4.1.2 "><p id="p4344474"><a name="p4344474"></a><a name="p4344474"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.16481648164816%" headers="mcps1.2.4.1.3 "><p id="p16358126"><a name="p16358126"></a><a name="p16358126"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section46708959"></a>

-   请求参数

    <a name="table835318258318"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0053158693_row1458874235211"><th class="cellrowborder" valign="top" width="19.85%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0053158693_p59978491115233"><a name="zh-cn_topic_0053158693_p59978491115233"></a><a name="zh-cn_topic_0053158693_p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.39%" id="mcps1.1.5.1.2"><p id="zh-cn_topic_0053158693_p26419641115233"><a name="zh-cn_topic_0053158693_p26419641115233"></a><a name="zh-cn_topic_0053158693_p26419641115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.75%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0053158693_p59616187115233"><a name="zh-cn_topic_0053158693_p59616187115233"></a><a name="zh-cn_topic_0053158693_p59616187115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="41.010000000000005%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0053158693_p64181866115233"><a name="zh-cn_topic_0053158693_p64181866115233"></a><a name="zh-cn_topic_0053158693_p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0053158693_row686311283276"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p10447191065310"><a name="zh-cn_topic_0053158693_p10447191065310"></a><a name="zh-cn_topic_0053158693_p10447191065310"></a>changes-since</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p644915104533"><a name="zh-cn_topic_0053158693_p644915104533"></a><a name="zh-cn_topic_0053158693_p644915104533"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p13454131016536"><a name="zh-cn_topic_0053158693_p13454131016536"></a><a name="zh-cn_topic_0053158693_p13454131016536"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p445791014538"><a name="zh-cn_topic_0053158693_p445791014538"></a><a name="zh-cn_topic_0053158693_p445791014538"></a><span id="zh-cn_topic_0053158693_text121698161638"><a name="zh-cn_topic_0053158693_text121698161638"></a><a name="zh-cn_topic_0053158693_text121698161638"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text216912161937"><a name="zh-cn_topic_0053158693_text216912161937"></a><a name="zh-cn_topic_0053158693_text216912161937"></a></span>上次更新状态的时间戳信息。格式为ISO 8601时间格式，例如：2013-06-09T06:42:18Z。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row16588164215216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p17387161075313"><a name="zh-cn_topic_0053158693_p17387161075313"></a><a name="zh-cn_topic_0053158693_p17387161075313"></a>image</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p123900108538"><a name="zh-cn_topic_0053158693_p123900108538"></a><a name="zh-cn_topic_0053158693_p123900108538"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p2393161013538"><a name="zh-cn_topic_0053158693_p2393161013538"></a><a name="zh-cn_topic_0053158693_p2393161013538"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p1339701010533"><a name="zh-cn_topic_0053158693_p1339701010533"></a><a name="zh-cn_topic_0053158693_p1339701010533"></a>镜像ID。</p>
    <p id="zh-cn_topic_0053158693_p1870622242917"><a name="zh-cn_topic_0053158693_p1870622242917"></a><a name="zh-cn_topic_0053158693_p1870622242917"></a>可以在镜像服务控制台查询，也可以调用“<a href="https://support.huaweicloud.com/api-ims/ims_03_0602.html" target="_blank" rel="noopener noreferrer">查询镜像列表</a>”API获取。</p>
    <div class="note" id="zh-cn_topic_0053158693_note623794911339"><a name="zh-cn_topic_0053158693_note623794911339"></a><a name="zh-cn_topic_0053158693_note623794911339"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0053158693_p17237114943316"><a name="zh-cn_topic_0053158693_p17237114943316"></a><a name="zh-cn_topic_0053158693_p17237114943316"></a>在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。</p>
    </div></div>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row05881842195216"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p839991012531"><a name="zh-cn_topic_0053158693_p839991012531"></a><a name="zh-cn_topic_0053158693_p839991012531"></a>flavor</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p12402210155311"><a name="zh-cn_topic_0053158693_p12402210155311"></a><a name="zh-cn_topic_0053158693_p12402210155311"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p15406610135318"><a name="zh-cn_topic_0053158693_p15406610135318"></a><a name="zh-cn_topic_0053158693_p15406610135318"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p1040881015311"><a name="zh-cn_topic_0053158693_p1040881015311"></a><a name="zh-cn_topic_0053158693_p1040881015311"></a>规格ID。</p>
    <p id="zh-cn_topic_0053158693_p7741128113511"><a name="zh-cn_topic_0053158693_p7741128113511"></a><a name="zh-cn_topic_0053158693_p7741128113511"></a>可以在<span id="zh-cn_topic_0053158693_text9235625735"><a name="zh-cn_topic_0053158693_text9235625735"></a><a name="zh-cn_topic_0053158693_text9235625735"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text32351725734"><a name="zh-cn_topic_0053158693_text32351725734"></a><a name="zh-cn_topic_0053158693_text32351725734"></a></span>控制台查询，也可以调用<a href="查询裸金属服务器规格信息列表（OpenStack原生）.md">查询裸金属服务器规格信息列表（OpenStack原生）</a>API获取。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row058811420527"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p5413201085313"><a name="zh-cn_topic_0053158693_p5413201085313"></a><a name="zh-cn_topic_0053158693_p5413201085313"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p1941781012535"><a name="zh-cn_topic_0053158693_p1941781012535"></a><a name="zh-cn_topic_0053158693_p1941781012535"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p3422121055318"><a name="zh-cn_topic_0053158693_p3422121055318"></a><a name="zh-cn_topic_0053158693_p3422121055318"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p842631015536"><a name="zh-cn_topic_0053158693_p842631015536"></a><a name="zh-cn_topic_0053158693_p842631015536"></a><span id="zh-cn_topic_0053158693_text13209132811312"><a name="zh-cn_topic_0053158693_text13209132811312"></a><a name="zh-cn_topic_0053158693_text13209132811312"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text920922816319"><a name="zh-cn_topic_0053158693_text920922816319"></a><a name="zh-cn_topic_0053158693_text920922816319"></a></span>名称，使用模糊匹配的方式查询。</p>
    <p id="zh-cn_topic_0053158693_p7429181015313"><a name="zh-cn_topic_0053158693_p7429181015313"></a><a name="zh-cn_topic_0053158693_p7429181015313"></a>例如，“?name=bob”正则表达式会同时返回bob和bobb。如果必须仅匹配bob，则可以使用与基础数据库服务器的语法相匹配的正则表达式，如MySQL或PostgreSQL（官方网站：<a href="https://www.postgresql.org/docs/9.2/static/functions-matching.html" target="_blank" rel="noopener noreferrer">https://www.postgresql.org/docs/9.2/static/functions-matching.html</a>）。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row105881642195217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p1743421075315"><a name="zh-cn_topic_0053158693_p1743421075315"></a><a name="zh-cn_topic_0053158693_p1743421075315"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p843711020539"><a name="zh-cn_topic_0053158693_p843711020539"></a><a name="zh-cn_topic_0053158693_p843711020539"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p11440101010537"><a name="zh-cn_topic_0053158693_p11440101010537"></a><a name="zh-cn_topic_0053158693_p11440101010537"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p7441161020531"><a name="zh-cn_topic_0053158693_p7441161020531"></a><a name="zh-cn_topic_0053158693_p7441161020531"></a><span id="zh-cn_topic_0053158693_text4817131535"><a name="zh-cn_topic_0053158693_text4817131535"></a><a name="zh-cn_topic_0053158693_text4817131535"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text1781773117312"><a name="zh-cn_topic_0053158693_text1781773117312"></a><a name="zh-cn_topic_0053158693_text1781773117312"></a></span>状态。</p>
    <p id="zh-cn_topic_0053158693_p117067951617"><a name="zh-cn_topic_0053158693_p117067951617"></a><a name="zh-cn_topic_0053158693_p117067951617"></a>取值范围：</p>
    <a name="zh-cn_topic_0053158693_ul29109448426"></a><a name="zh-cn_topic_0053158693_ul29109448426"></a><ul id="zh-cn_topic_0053158693_ul29109448426"><li>ACTIVE：运行中/正在关机/删除中</li><li>BUILD：创建中</li><li>ERROR：故障</li><li>HARD_REBOOT：强制重启中</li><li>REBOOT：重启中</li><li>DELETED：实例已被正常删除</li><li>SHUTOFF：关机/正在开机/删除中/重建中/重装操作系统中/重装操作系统失败/冻结</li></ul>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row16588142145219"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p1445843114279"><a name="zh-cn_topic_0053158693_p1445843114279"></a><a name="zh-cn_topic_0053158693_p1445843114279"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p15457103122713"><a name="zh-cn_topic_0053158693_p15457103122713"></a><a name="zh-cn_topic_0053158693_p15457103122713"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p15455113112714"><a name="zh-cn_topic_0053158693_p15455113112714"></a><a name="zh-cn_topic_0053158693_p15455113112714"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p345110316275"><a name="zh-cn_topic_0053158693_p345110316275"></a><a name="zh-cn_topic_0053158693_p345110316275"></a>每页返回<span id="zh-cn_topic_0053158693_text59831335739"><a name="zh-cn_topic_0053158693_text59831335739"></a><a name="zh-cn_topic_0053158693_text59831335739"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text1098373515319"><a name="zh-cn_topic_0053158693_text1098373515319"></a><a name="zh-cn_topic_0053158693_text1098373515319"></a></span>的条数。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row12307152919453"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p34602410233"><a name="zh-cn_topic_0053158693_p34602410233"></a><a name="zh-cn_topic_0053158693_p34602410233"></a>marker</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p1946094112310"><a name="zh-cn_topic_0053158693_p1946094112310"></a><a name="zh-cn_topic_0053158693_p1946094112310"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p14460249231"><a name="zh-cn_topic_0053158693_p14460249231"></a><a name="zh-cn_topic_0053158693_p14460249231"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p174601046239"><a name="zh-cn_topic_0053158693_p174601046239"></a><a name="zh-cn_topic_0053158693_p174601046239"></a>从marker指定的<span id="zh-cn_topic_0053158693_text71323381731"><a name="zh-cn_topic_0053158693_text71323381731"></a><a name="zh-cn_topic_0053158693_text71323381731"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text613212389311"><a name="zh-cn_topic_0053158693_text613212389311"></a><a name="zh-cn_topic_0053158693_text613212389311"></a></span>ID的下一条数据开始查询。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row14320610478"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p5324615479"><a name="zh-cn_topic_0053158693_p5324615479"></a><a name="zh-cn_topic_0053158693_p5324615479"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p143218664715"><a name="zh-cn_topic_0053158693_p143218664715"></a><a name="zh-cn_topic_0053158693_p143218664715"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p143211619479"><a name="zh-cn_topic_0053158693_p143211619479"></a><a name="zh-cn_topic_0053158693_p143211619479"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p123246194714"><a name="zh-cn_topic_0053158693_p123246194714"></a><a name="zh-cn_topic_0053158693_p123246194714"></a>查询tag字段中包含该值的<span id="zh-cn_topic_0053158693_text142391140333"><a name="zh-cn_topic_0053158693_text142391140333"></a><a name="zh-cn_topic_0053158693_text142391140333"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text162393401630"><a name="zh-cn_topic_0053158693_text162393401630"></a><a name="zh-cn_topic_0053158693_text162393401630"></a></span>。</p>
    <p id="zh-cn_topic_0053158693_p12820165216471"><a name="zh-cn_topic_0053158693_p12820165216471"></a><a name="zh-cn_topic_0053158693_p12820165216471"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row1658884211523"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p203418324539"><a name="zh-cn_topic_0053158693_p203418324539"></a><a name="zh-cn_topic_0053158693_p203418324539"></a>not-tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p173673215532"><a name="zh-cn_topic_0053158693_p173673215532"></a><a name="zh-cn_topic_0053158693_p173673215532"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p238132105317"><a name="zh-cn_topic_0053158693_p238132105317"></a><a name="zh-cn_topic_0053158693_p238132105317"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p154313328536"><a name="zh-cn_topic_0053158693_p154313328536"></a><a name="zh-cn_topic_0053158693_p154313328536"></a>查询tag字段中不包含该值的<span id="zh-cn_topic_0053158693_text179892421232"><a name="zh-cn_topic_0053158693_text179892421232"></a><a name="zh-cn_topic_0053158693_text179892421232"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text149891342231"><a name="zh-cn_topic_0053158693_text149891342231"></a><a name="zh-cn_topic_0053158693_text149891342231"></a></span>，值为标签的Key。</p>
    <div class="note" id="zh-cn_topic_0053158693_note124521913175616"><a name="zh-cn_topic_0053158693_note124521913175616"></a><a name="zh-cn_topic_0053158693_note124521913175616"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0053158693_p1745221311560"><a name="zh-cn_topic_0053158693_p1745221311560"></a><a name="zh-cn_topic_0053158693_p1745221311560"></a>如果之前添加的Tag为“Key.Value”的形式，则查询的时候需要使用“Key”来查询。</p>
    <p id="zh-cn_topic_0053158693_p213418685710"><a name="zh-cn_topic_0053158693_p213418685710"></a><a name="zh-cn_topic_0053158693_p213418685710"></a>例如：之前添加的tag为“a.b”,则升级后，查询时需使用“not-tags=a”。</p>
    </div></div>
    <p id="zh-cn_topic_0053158693_p19441232135317"><a name="zh-cn_topic_0053158693_p19441232135317"></a><a name="zh-cn_topic_0053158693_p19441232135317"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row1158812424528"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p184717323539"><a name="zh-cn_topic_0053158693_p184717323539"></a><a name="zh-cn_topic_0053158693_p184717323539"></a>reservation_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p1650832195311"><a name="zh-cn_topic_0053158693_p1650832195311"></a><a name="zh-cn_topic_0053158693_p1650832195311"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p1453143220535"><a name="zh-cn_topic_0053158693_p1453143220535"></a><a name="zh-cn_topic_0053158693_p1453143220535"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p5551832185311"><a name="zh-cn_topic_0053158693_p5551832185311"></a><a name="zh-cn_topic_0053158693_p5551832185311"></a>批量创建<span id="zh-cn_topic_0053158693_text63205019314"><a name="zh-cn_topic_0053158693_text63205019314"></a><a name="zh-cn_topic_0053158693_text63205019314"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text734501833"><a name="zh-cn_topic_0053158693_text734501833"></a><a name="zh-cn_topic_0053158693_text734501833"></a></span>时，指定该预留ID，可以查询同批次创建的<span id="zh-cn_topic_0053158693_text281110523312"><a name="zh-cn_topic_0053158693_text281110523312"></a><a name="zh-cn_topic_0053158693_text281110523312"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text281195211313"><a name="zh-cn_topic_0053158693_text281195211313"></a><a name="zh-cn_topic_0053158693_text281195211313"></a></span>。</p>
    <p id="zh-cn_topic_0053158693_p45753218534"><a name="zh-cn_topic_0053158693_p45753218534"></a><a name="zh-cn_topic_0053158693_p45753218534"></a>微版本2.26新增</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row1758864217526"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p10633321531"><a name="zh-cn_topic_0053158693_p10633321531"></a><a name="zh-cn_topic_0053158693_p10633321531"></a>sort_key</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p106613212531"><a name="zh-cn_topic_0053158693_p106613212531"></a><a name="zh-cn_topic_0053158693_p106613212531"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p196963275311"><a name="zh-cn_topic_0053158693_p196963275311"></a><a name="zh-cn_topic_0053158693_p196963275311"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p167133212536"><a name="zh-cn_topic_0053158693_p167133212536"></a><a name="zh-cn_topic_0053158693_p167133212536"></a>用于排序的属性，包括uuid（<span id="zh-cn_topic_0053158693_text62627567316"><a name="zh-cn_topic_0053158693_text62627567316"></a><a name="zh-cn_topic_0053158693_text62627567316"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text1726217563313"><a name="zh-cn_topic_0053158693_text1726217563313"></a><a name="zh-cn_topic_0053158693_text1726217563313"></a></span>的uuid）、vm_state（<span id="zh-cn_topic_0053158693_text142381559638"><a name="zh-cn_topic_0053158693_text142381559638"></a><a name="zh-cn_topic_0053158693_text142381559638"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text22392599316"><a name="zh-cn_topic_0053158693_text22392599316"></a><a name="zh-cn_topic_0053158693_text22392599316"></a></span>的状态）、display_name（<span id="zh-cn_topic_0053158693_text135136112411"><a name="zh-cn_topic_0053158693_text135136112411"></a><a name="zh-cn_topic_0053158693_text135136112411"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text6513116415"><a name="zh-cn_topic_0053158693_text6513116415"></a><a name="zh-cn_topic_0053158693_text6513116415"></a></span>名称）、task_state（<span id="zh-cn_topic_0053158693_text1810916516416"><a name="zh-cn_topic_0053158693_text1810916516416"></a><a name="zh-cn_topic_0053158693_text1810916516416"></a>裸金属服务器</span><span id="zh-cn_topic_0053158693_text17109175241"><a name="zh-cn_topic_0053158693_text17109175241"></a><a name="zh-cn_topic_0053158693_text17109175241"></a></span>任务状态）、power_state（电源状态）、created_at（创建时间）、updated_at（更新时间）、availability_zone（可用区）。可以指定多对sort_key和sort_dir。</p>
    <p id="zh-cn_topic_0053158693_p1321581482211"><a name="zh-cn_topic_0053158693_p1321581482211"></a><a name="zh-cn_topic_0053158693_p1321581482211"></a>默认排序顺序为created_at逆序。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0053158693_row135891242165217"><td class="cellrowborder" valign="top" width="19.85%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0053158693_p1327414444539"><a name="zh-cn_topic_0053158693_p1327414444539"></a><a name="zh-cn_topic_0053158693_p1327414444539"></a>sort_dir</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.39%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0053158693_p16275104445317"><a name="zh-cn_topic_0053158693_p16275104445317"></a><a name="zh-cn_topic_0053158693_p16275104445317"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.75%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0053158693_p202804443536"><a name="zh-cn_topic_0053158693_p202804443536"></a><a name="zh-cn_topic_0053158693_p202804443536"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0053158693_p15283154425314"><a name="zh-cn_topic_0053158693_p15283154425314"></a><a name="zh-cn_topic_0053158693_p15283154425314"></a>排序方向。</p>
    <a name="zh-cn_topic_0053158693_ul22858441530"></a><a name="zh-cn_topic_0053158693_ul22858441530"></a><ul id="zh-cn_topic_0053158693_ul22858441530"><li>asc：升序</li><li>desc：降序（默认值）</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例
    -   不带可选参数

        ```
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail
        ```

    -   携带一个可选参数

        ```
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail?tags=__type_baremetal
        ```

    -   携带多个可选参数

        ```
        https://{ECS Endpoint}/v2.1/bbf1946d374b44a0a2a95533562ba954/servers/detail?tags=__type_baremetal&name=bms-test01
        ```



## 响应消息<a name="section17727455"></a>

-   响应参数

    <a name="table61256692"></a>
    <table><thead align="left"><tr id="row16697504"><th class="cellrowborder" valign="top" width="17.86%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="32.97%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.17%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row64050727"><td class="cellrowborder" valign="top" width="17.86%" headers="mcps1.1.4.1.1 "><p id="p20726409"><a name="p20726409"></a><a name="p20726409"></a>servers</p>
    </td>
    <td class="cellrowborder" valign="top" width="32.97%" headers="mcps1.1.4.1.2 "><p id="p491044173818"><a name="p491044173818"></a><a name="p491044173818"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.17%" headers="mcps1.1.4.1.3 "><p id="p24702645"><a name="p24702645"></a><a name="p24702645"></a><span id="text56791793514"><a name="text56791793514"></a><a name="text56791793514"></a>裸金属服务器</span><span id="text06791091752"><a name="text06791091752"></a><a name="text06791091752"></a></span>信息列表详情。内容参见<a href="查询裸金属服务器详情（OpenStack原生）.md#table6149040">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "servers": [
            {
                "tenant_id": "c685484a8cc2416b97260938705deb64",
                "addresses": {
                    "08a7715f-7de6-4ff9-a343-95ba4209f24a": [
                        {
                            "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:0e:c4:77",
                            "OS-EXT-IPS:type": "fixed",
                            "addr": "192.168.0.107",
                            "version": 4
                        }
                    ]
                },
                "metadata": {
                    "op_svc_userid": "1311c433dd9b408886f57d695c229cbe"
                },
                "OS-EXT-STS:task_state": null,
                "OS-DCF:diskConfig": "MANUAL",
                "OS-EXT-AZ:availability_zone": "az-dc-1",
                "links": [
                    {
                        "rel": "self",
                        "href": "https://openstack.example.com/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                    },
                    {
                        "rel": "bookmark",
                        "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                    }
                ],
                "OS-EXT-STS:power_state": 1,
                "id": "95bf2490-5428-432c-ad9b-5e3406f869dd",
                "os-extended-volumes:volumes_attached": [
                    {
                        "id": "dfa375b5-9856-44ad-a937-a4802b6434c3"
                    },
                    {
                        "id": "bb9f1b27-843b-4561-b62e-ca18eeaec417"
                    },
                    {
                        "id": "86e801c3-acc6-465d-890c-d43ba493f553"
                    },
                    {
                        "id": "0994d3ac-3c6a-495c-a439-c597a4f08fa6"
                    }
                ],
                "OS-EXT-SRV-ATTR:host": "bms.az1",
                "image": {
                    "links": [
                        {
                            "rel": "bookmark",
                            "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/images/1a6635d8-afea-4f2b-abb6-27a202bad319"
                        }
                    ],
                    "id": "1a6635d8-afea-4f2b-abb6-27a202bad319"
                },
                "OS-SRV-USG:terminated_at": null,
                "accessIPv4": "",
                "accessIPv6": "",
                "created": "2017-05-24T06:14:05Z",
                "hostId": "e9c3ee0fcc58ab6085cf30df70b5544eab958858fb50d925f023e53e",
                "OS-EXT-SRV-ATTR:hypervisor_hostname": "nova004@2",
                "key_name": "KeyPair-JX",
                "flavor": {
                    "links": [
                        {
                            "rel": "bookmark",
                            "href": "https://openstack.example.com/c685484a8cc2416b97260938705deb65/flavors/physical.83.medium"
                        }
                    ],
                    "id": "physical.83.medium"
                },
                "security_groups": [
                    {
                        "name": "0011b620-4982-42e4-ad12-47c95ca495c4"
                    }
                ],
                "config_drive": "",
                "OS-EXT-STS:vm_state": "active",
                "OS-EXT-SRV-ATTR:instance_name": "instance-0000ebd3",
                "user_id": "1311c433dd9b408886f57d695c229cbe",
                "name": "bms",
                "progress": 0,
                "OS-SRV-USG:launched_at": "2017-05-25T03:40:25.066078",
                "updated": "2017-05-25T03:40:25Z",
                "status": "ACTIVE"
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

