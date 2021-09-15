# 支持的监控指标（安装Agent，简洁版）<a name="bms_01_0130"></a>

## 功能说明<a name="zh-cn_topic_0107606742_section1233112278019"></a>

本节内容介绍裸金属服务器支持上报云监控的操作系统监控指标。以下区域主机监控Agent采用最新版本的Agent，监控指标更为简洁。

当前支持的区域：

“华东-上海一”、“华东-上海二”、“华北-北京一”、“华北-北京四”、“华南-广州”、“华南-深圳”、“西南-贵阳一”、“中国-香港”、“亚太-曼谷”、“亚太-新加坡”、“非洲-约翰内斯堡”。

>![](public_sys-resources/icon-note.gif) **说明：** 
>安装Agent后，您便可以查看裸金属服务器的操作系统监控指标。指标采集周期是1分钟。

## 命名空间<a name="zh-cn_topic_0107606742_section3231114620112"></a>

SERVICE.BMS

## 监控指标<a name="section1291762275415"></a>

裸金属服务器（操作系统监控）支持的监控指标如[表1](#table18122035141217)所示。

**表 1**  监控指标

<a name="table18122035141217"></a>
<table><thead align="left"><tr id="row11123153511214"><th class="cellrowborder" valign="top" width="10.347930413917217%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p16698359842"><a name="zh-cn_topic_0107606742_p16698359842"></a><a name="zh-cn_topic_0107606742_p16698359842"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="16.77664467106579%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="36.822635472905425%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="10.757848430313938%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="12.05758848230354%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="13.237352529494101%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row1112373514129"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p5123335101213"><a name="p5123335101213"></a><a name="p5123335101213"></a>cpu_usage</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p91231135201214"><a name="p91231135201214"></a><a name="p91231135201214"></a>（Agent）CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p11924165815571"><a name="zh-cn_topic_0107606742_p11924165815571"></a><a name="zh-cn_topic_0107606742_p11924165815571"></a>该指标用于统计测量对象当前CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p728854765611"><a name="zh-cn_topic_0107606742_p728854765611"></a><a name="zh-cn_topic_0107606742_p728854765611"></a>通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p2310193561618"><a name="zh-cn_topic_0107606742_p2310193561618"></a><a name="zh-cn_topic_0107606742_p2310193561618"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b9294154711566"><a name="zh-cn_topic_0107606742_b9294154711566"></a><a name="zh-cn_topic_0107606742_b9294154711566"></a>top</strong>命令查看“%Cpu(s)”值。</p>
<p id="zh-cn_topic_0107606742_p18756472598"><a name="zh-cn_topic_0107606742_p18756472598"></a><a name="zh-cn_topic_0107606742_p18756472598"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p1612353510123"><a name="p1612353510123"></a><a name="p1612353510123"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p111237358127"><a name="p111237358127"></a><a name="p111237358127"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p13123203561216"><a name="p13123203561216"></a><a name="p13123203561216"></a>1分钟</p>
</td>
</tr>
<tr id="row1612393513128"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p9123535191211"><a name="p9123535191211"></a><a name="p9123535191211"></a>load_average5</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p41231035181219"><a name="p41231035181219"></a><a name="p41231035181219"></a>（Agent）5分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"></a>该指标用于统计测量对象在过去5分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"></a>通过“/proc/loadavg”文件中load5/逻辑CPU个数得到。</p>
<p id="zh-cn_topic_0107606742_p98941691813"><a name="zh-cn_topic_0107606742_p98941691813"></a><a name="zh-cn_topic_0107606742_p98941691813"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"></a>top</strong>命令查看“load5”值。</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p612323512127"><a name="p612323512127"></a><a name="p612323512127"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p612353512125"><a name="p612353512125"></a><a name="p612353512125"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p1012323510123"><a name="p1012323510123"></a><a name="p1012323510123"></a>1分钟</p>
</td>
</tr>
<tr id="row212314352127"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p0123173531216"><a name="p0123173531216"></a><a name="p0123173531216"></a>mem_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p121231935131216"><a name="p121231935131216"></a><a name="p121231935131216"></a>（Agent）内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"></a>该指标用于统计测量对象的内存使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"></a>通过“/proc/meminfo”文件获取。计算公式：(MemTotal-MemAvailable)/MemTotal。</p>
<p id="zh-cn_topic_0107606742_p1728710269372"><a name="zh-cn_topic_0107606742_p1728710269372"></a><a name="zh-cn_topic_0107606742_p1728710269372"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p51238355124"><a name="p51238355124"></a><a name="p51238355124"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p1412393591218"><a name="p1412393591218"></a><a name="p1412393591218"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p151231235161218"><a name="p151231235161218"></a><a name="p151231235161218"></a>1分钟</p>
</td>
</tr>
<tr id="row61247355125"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p11241735151219"><a name="p11241735151219"></a><a name="p11241735151219"></a>mountPointPrefix_disk_free</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p61241535101212"><a name="p61241535101212"></a><a name="p61241535101212"></a>（Agent）磁盘剩余存储量</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"></a>该指标用于统计测量对象磁盘的剩余存储空间。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"></a>执行<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"></a>df -h</strong>命令，查看Avail列数据。</p>
<p id="zh-cn_topic_0107606742_p6772134582115"><a name="zh-cn_topic_0107606742_p6772134582115"></a><a name="zh-cn_topic_0107606742_p6772134582115"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p1961921713810"><a name="zh-cn_topic_0107606742_p1961921713810"></a><a name="zh-cn_topic_0107606742_p1961921713810"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p12124335151210"><a name="p12124335151210"></a><a name="p12124335151210"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p1412415353129"><a name="p1412415353129"></a><a name="p1412415353129"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p1112412353129"><a name="p1112412353129"></a><a name="p1112412353129"></a>1分钟</p>
</td>
</tr>
<tr id="row1312423591215"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p1912413359124"><a name="p1912413359124"></a><a name="p1912413359124"></a>mountPointPrefix_disk_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p191245352128"><a name="p191245352128"></a><a name="p191245352128"></a>（Agent）磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"></a>该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为：磁盘已用存储量/磁盘存储总量。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"></a>通过计算Used/Size得出。</p>
<p id="zh-cn_topic_0107606742_p464848112210"><a name="zh-cn_topic_0107606742_p464848112210"></a><a name="zh-cn_topic_0107606742_p464848112210"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p196724114386"><a name="zh-cn_topic_0107606742_p196724114386"></a><a name="zh-cn_topic_0107606742_p196724114386"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p21240356129"><a name="p21240356129"></a><a name="p21240356129"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p8124173541220"><a name="p8124173541220"></a><a name="p8124173541220"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p412417359129"><a name="p412417359129"></a><a name="p412417359129"></a>1分钟</p>
</td>
</tr>
<tr id="row112410356126"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p1581223517560"><a name="p1581223517560"></a><a name="p1581223517560"></a>mountPointPrefix_disk_ioUtils 和volumePrefix_disk_ioUtils</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p131241035131210"><a name="p131241035131210"></a><a name="p131241035131210"></a>（Agent）磁盘I/O使用率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"></a>该指标用于统计测量对象磁盘I/O使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。</p>
<p id="zh-cn_topic_0107606742_p1090014381522"><a name="zh-cn_topic_0107606742_p1090014381522"></a><a name="zh-cn_topic_0107606742_p1090014381522"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p5387192112400"><a name="zh-cn_topic_0107606742_p5387192112400"></a><a name="zh-cn_topic_0107606742_p5387192112400"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p13124153518129"><a name="p13124153518129"></a><a name="p13124153518129"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p112413561212"><a name="p112413561212"></a><a name="p112413561212"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p7124113571213"><a name="p7124113571213"></a><a name="p7124113571213"></a>1分钟</p>
</td>
</tr>
<tr id="row1312443516122"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p14586144185715"><a name="p14586144185715"></a><a name="p14586144185715"></a>mountPointPrefix_disk_inodesUsedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p15124133521213"><a name="p15124133521213"></a><a name="p15124133521213"></a>（Agent）inode已使用占比</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"><a name="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"></a><a name="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"></a>该指标用于统计测量对象当前磁盘已使用的inode占比。</p>
<p id="zh-cn_topic_0107606742_p11890521116"><a name="zh-cn_topic_0107606742_p11890521116"></a><a name="zh-cn_topic_0107606742_p11890521116"></a>执行<strong id="zh-cn_topic_0107606742_b17532345115811"><a name="zh-cn_topic_0107606742_b17532345115811"></a><a name="zh-cn_topic_0107606742_b17532345115811"></a>df -i</strong>命令，查看IUse%列数据。</p>
<p id="zh-cn_topic_0107606742_p20144348934"><a name="zh-cn_topic_0107606742_p20144348934"></a><a name="zh-cn_topic_0107606742_p20144348934"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p11782138145615"><a name="zh-cn_topic_0107606742_p11782138145615"></a><a name="zh-cn_topic_0107606742_p11782138145615"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p6124135121210"><a name="p6124135121210"></a><a name="p6124135121210"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p161243357120"><a name="p161243357120"></a><a name="p161243357120"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p5124113511211"><a name="p5124113511211"></a><a name="p5124113511211"></a>1分钟</p>
</td>
</tr>
<tr id="row171246355128"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p1712403521219"><a name="p1712403521219"></a><a name="p1712403521219"></a>net_bitRecv</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p112463541217"><a name="p112463541217"></a><a name="p112463541217"></a>（Agent）入网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"></a>该指标用于统计测量对象网卡每秒接收的比特数。</p>
<p id="zh-cn_topic_0107606742_p9414151572118"><a name="zh-cn_topic_0107606742_p9414151572118"></a><a name="zh-cn_topic_0107606742_p9414151572118"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p0780145612408"><a name="zh-cn_topic_0107606742_p0780145612408"></a><a name="zh-cn_topic_0107606742_p0780145612408"></a>单位：bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p118402467212"><a name="zh-cn_topic_0107606742_p118402467212"></a><a name="zh-cn_topic_0107606742_p118402467212"></a>1分钟</p>
</td>
</tr>
<tr id="row1124235161214"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p14124153516126"><a name="p14124153516126"></a><a name="p14124153516126"></a>net_bitSent</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p191248356123"><a name="p191248356123"></a><a name="p191248356123"></a>（Agent）出网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"></a>该指标用于统计测量对象网卡每秒发送的比特数。</p>
<p id="zh-cn_topic_0107606742_p109105171214"><a name="zh-cn_topic_0107606742_p109105171214"></a><a name="zh-cn_topic_0107606742_p109105171214"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p1857448154112"><a name="zh-cn_topic_0107606742_p1857448154112"></a><a name="zh-cn_topic_0107606742_p1857448154112"></a>单位：bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p369617410228"><a name="zh-cn_topic_0107606742_p369617410228"></a><a name="zh-cn_topic_0107606742_p369617410228"></a>1分钟</p>
</td>
</tr>
<tr id="row101242354121"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p1612413355127"><a name="p1612413355127"></a><a name="p1612413355127"></a>net_packetRecv</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p512443581212"><a name="p512443581212"></a><a name="p512443581212"></a>（Agent）网卡包接收速率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"></a>该指标用于统计测量对象网卡每秒接收的数据包数。</p>
<p id="zh-cn_topic_0107606742_p1653912017215"><a name="zh-cn_topic_0107606742_p1653912017215"></a><a name="zh-cn_topic_0107606742_p1653912017215"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p34321561417"><a name="zh-cn_topic_0107606742_p34321561417"></a><a name="zh-cn_topic_0107606742_p34321561417"></a>单位：Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p12124103517122"><a name="p12124103517122"></a><a name="p12124103517122"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p17125435201220"><a name="p17125435201220"></a><a name="p17125435201220"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p4125183571210"><a name="p4125183571210"></a><a name="p4125183571210"></a>1分钟</p>
</td>
</tr>
<tr id="row412573516129"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p1212593581218"><a name="p1212593581218"></a><a name="p1212593581218"></a>net_packetSent</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p12125835141211"><a name="p12125835141211"></a><a name="p12125835141211"></a>（Agent）网卡包发送速率</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"></a>该指标用于统计测量对象网卡每秒发送的数据包数。</p>
<p id="zh-cn_topic_0107606742_p1557942352114"><a name="zh-cn_topic_0107606742_p1557942352114"></a><a name="zh-cn_topic_0107606742_p1557942352114"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p673911116424"><a name="zh-cn_topic_0107606742_p673911116424"></a><a name="zh-cn_topic_0107606742_p673911116424"></a>单位：Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p421119642214"><a name="zh-cn_topic_0107606742_p421119642214"></a><a name="zh-cn_topic_0107606742_p421119642214"></a>1分钟</p>
</td>
</tr>
<tr id="row171252355123"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p012563521212"><a name="p012563521212"></a><a name="p012563521212"></a>net_tcp_total</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p912513352126"><a name="p912513352126"></a><a name="p912513352126"></a>（Agent）所有状态的TCP连接数总和</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="p176415443212"><a name="p176415443212"></a><a name="p176415443212"></a>该指标用于统计测量对象网卡所有状态的TCP连接数总和。</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p196411044192113"><a name="p196411044192113"></a><a name="p196411044192113"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p151254355120"><a name="p151254355120"></a><a name="p151254355120"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p13125735161212"><a name="p13125735161212"></a><a name="p13125735161212"></a>1分钟</p>
</td>
</tr>
<tr id="row181835279144"><td class="cellrowborder" valign="top" width="10.347930413917217%" headers="mcps1.2.7.1.1 "><p id="p5183132791416"><a name="p5183132791416"></a><a name="p5183132791416"></a>net_tcp_established</p>
</td>
<td class="cellrowborder" valign="top" width="16.77664467106579%" headers="mcps1.2.7.1.2 "><p id="p2183192710144"><a name="p2183192710144"></a><a name="p2183192710144"></a>（Agent）处于ESTABLISHED状态的TCP连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="36.822635472905425%" headers="mcps1.2.7.1.3 "><p id="p464214444219"><a name="p464214444219"></a><a name="p464214444219"></a>该指标用于统计测量对象网卡处于ESTABLISHED状态的TCP连接数量。</p>
</td>
<td class="cellrowborder" valign="top" width="10.757848430313938%" headers="mcps1.2.7.1.4 "><p id="p1764254413215"><a name="p1764254413215"></a><a name="p1764254413215"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="12.05758848230354%" headers="mcps1.2.7.1.5 "><p id="p1183172751411"><a name="p1183172751411"></a><a name="p1183172751411"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="13.237352529494101%" headers="mcps1.2.7.1.6 "><p id="p181831727111420"><a name="p181831727111420"></a><a name="p181831727111420"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

