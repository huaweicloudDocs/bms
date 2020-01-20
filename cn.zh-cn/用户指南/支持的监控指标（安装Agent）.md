# 支持的监控指标（安装Agent）<a name="bms_01_0053"></a>

## 功能说明<a name="zh-cn_topic_0107606742_section1233112278019"></a>

本节定义了裸金属服务器上报云监控服务的监控指标的命名空间，监控指标列表和维度定义，用户可以通过云监控服务提供管理控制台或API接口来检索裸金属服务器产生的监控指标和告警信息。

>![](public_sys-resources/icon-note.gif) **说明：**   
>安装Agent后，您便可以查看裸金属服务器的操作系统监控指标。指标采集周期是1分钟。  
>“华东-上海一”区域主机监控Agent采用最新版本的Agent，监控指标更为简洁，详情请参见[支持的监控指标（安装Agent，华东-上海一）](支持的监控指标（安装Agent-华东-上海一）.md)。  

## 命名空间<a name="zh-cn_topic_0107606742_section3231114620112"></a>

SERVICE.BMS

## 监控指标<a name="zh-cn_topic_0107606742_section738316451823"></a>

裸金属服务器（操作系统监控）支持的监控指标有：CPU相关监控指标（[表1](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1274172674913)）、CPU负载类相关监控指标（[表2](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table341241110501)）、内存相关监控指标（[表3](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table844220384507)）、磁盘相关监控指标（[表4](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1067218184514)）、磁盘I/O类（[表5](#zh-cn_topic_0107606742_table1559955415558)）、文件系统类（[表6](#zh-cn_topic_0107606742_table296913551343)）、网卡类（[表7](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table19476249105111)）、软RAID相关监控指标（[表8](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table17716191314220)）和进程相关监控指标（[表9](#zh-cn_topic_0107606742_table2080718432177)）。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   如果要监控软RAID相关指标，Agent版本必须为1.0.5及以上。  
>-   Windows系统的裸金属服务器暂不支持监控。  

**表 1**  CPU相关监控指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1274172674913"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row0274142619497"><th class="cellrowborder" valign="top" width="10.93%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p16698359842"><a name="zh-cn_topic_0107606742_p16698359842"></a><a name="zh-cn_topic_0107606742_p16698359842"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.2%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p179771946114914"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.660000000000004%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697704684912"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.120000000000001%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1097713469495"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.06%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11977946144917"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="17.03%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4977194644918"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row13274112613493"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p969820597415"><a name="zh-cn_topic_0107606742_p969820597415"></a><a name="zh-cn_topic_0107606742_p969820597415"></a>cpu_usage_idle</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897744614498"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897744614498"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897744614498"></a>（Agent）CPU空闲时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1977174644912"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1977174644912"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1977174644912"></a>该指标用于统计测量对象当前CPU空闲时间占比。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199778464495"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199778464495"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199778464495"></a>通过计算采集周期内“/proc/stat”文件中的变化得出CPU空闲时间占比。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12977746144919"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12977746144919"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12977746144919"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b58832064164253"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b58832064164253"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b58832064164253"></a>top</strong>命令查看“%Cpu(s) id”值。</p>
<p id="zh-cn_topic_0107606742_p1349816063411"><a name="zh-cn_topic_0107606742_p1349816063411"></a><a name="zh-cn_topic_0107606742_p1349816063411"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6977184674918"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6977184674918"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6977184674918"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697710469493"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697710469493"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p697710469493"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1927494213519"><a name="zh-cn_topic_0107606742_p1927494213519"></a><a name="zh-cn_topic_0107606742_p1927494213519"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row12274152613492"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p169875920411"><a name="zh-cn_topic_0107606742_p169875920411"></a><a name="zh-cn_topic_0107606742_p169875920411"></a>cpu_usage_other</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897719462498"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897719462498"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p897719462498"></a>（Agent）其他CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p159771846194911"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p159771846194911"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p159771846194911"></a>该指标用于统计测量对象其他占用CPU使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p830102016019"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p830102016019"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p830102016019"></a>计算公式：</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1797710466496"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1797710466496"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1797710466496"></a>1 - 空闲CPU使用率（%） - 内核空间CPU使用率 - 用户空间CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p1014117574349"><a name="zh-cn_topic_0107606742_p1014117574349"></a><a name="zh-cn_topic_0107606742_p1014117574349"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1297764614490"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1297764614490"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1297764614490"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1397784620499"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1397784620499"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1397784620499"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p19721181441613"><a name="zh-cn_topic_0107606742_p19721181441613"></a><a name="zh-cn_topic_0107606742_p19721181441613"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row9275162654918"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p206988594412"><a name="zh-cn_topic_0107606742_p206988594412"></a><a name="zh-cn_topic_0107606742_p206988594412"></a>cpu_usage_system</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p109771846174917"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p109771846174917"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p109771846174917"></a>（Agent）内核空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p19781246114915"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p19781246114915"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p19781246114915"></a>该指标用于统计测量对象当前内核空间占用CPU使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0978134644916"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0978134644916"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0978134644916"></a>通过计算采集周期内“/proc/stat”文件中的变化得出内核空间CPU使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9978184613492"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9978184613492"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9978184613492"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b65111313628"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b65111313628"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b65111313628"></a>top</strong>命令查看“%Cpu(s) sy”值。</p>
<p id="zh-cn_topic_0107606742_p1259919133513"><a name="zh-cn_topic_0107606742_p1259919133513"></a><a name="zh-cn_topic_0107606742_p1259919133513"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1758603923418"><a name="zh-cn_topic_0107606742_p1758603923418"></a><a name="zh-cn_topic_0107606742_p1758603923418"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15978134684917"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15978134684917"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15978134684917"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p176761120181613"><a name="zh-cn_topic_0107606742_p176761120181613"></a><a name="zh-cn_topic_0107606742_p176761120181613"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row142751526184919"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p13698135913414"><a name="zh-cn_topic_0107606742_p13698135913414"></a><a name="zh-cn_topic_0107606742_p13698135913414"></a>cpu_usage_user</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978184613491"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978184613491"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978184613491"></a>（Agent）用户空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978146134918"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978146134918"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6978146134918"></a>该指标用于统计测量对象当前用户空间占用CPU使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997812467499"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997812467499"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997812467499"></a>通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p7127428111612"><a name="zh-cn_topic_0107606742_p7127428111612"></a><a name="zh-cn_topic_0107606742_p7127428111612"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1099915261931"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1099915261931"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1099915261931"></a>top</strong>命令查看“%Cpu(s) us”值。</p>
<p id="zh-cn_topic_0107606742_p63851171350"><a name="zh-cn_topic_0107606742_p63851171350"></a><a name="zh-cn_topic_0107606742_p63851171350"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p165928392347"><a name="zh-cn_topic_0107606742_p165928392347"></a><a name="zh-cn_topic_0107606742_p165928392347"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1497844624916"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1497844624916"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1497844624916"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997815461493"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997815461493"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p997815461493"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1161417109567"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1969965915417"><a name="zh-cn_topic_0107606742_p1969965915417"></a><a name="zh-cn_topic_0107606742_p1969965915417"></a>cpu_usage</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p092415835715"><a name="zh-cn_topic_0107606742_p092415835715"></a><a name="zh-cn_topic_0107606742_p092415835715"></a>（Agent）CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p11924165815571"><a name="zh-cn_topic_0107606742_p11924165815571"></a><a name="zh-cn_topic_0107606742_p11924165815571"></a>该指标用于统计测量对象当前CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p728854765611"><a name="zh-cn_topic_0107606742_p728854765611"></a><a name="zh-cn_topic_0107606742_p728854765611"></a>通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p2310193561618"><a name="zh-cn_topic_0107606742_p2310193561618"></a><a name="zh-cn_topic_0107606742_p2310193561618"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b9294154711566"><a name="zh-cn_topic_0107606742_b9294154711566"></a><a name="zh-cn_topic_0107606742_b9294154711566"></a>top</strong>命令查看“%Cpu(s)”值。</p>
<p id="zh-cn_topic_0107606742_p18756472598"><a name="zh-cn_topic_0107606742_p18756472598"></a><a name="zh-cn_topic_0107606742_p18756472598"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p8924205815579"><a name="zh-cn_topic_0107606742_p8924205815579"></a><a name="zh-cn_topic_0107606742_p8924205815579"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p2369141815610"><a name="zh-cn_topic_0107606742_p2369141815610"></a><a name="zh-cn_topic_0107606742_p2369141815610"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p6291134715618"><a name="zh-cn_topic_0107606742_p6291134715618"></a><a name="zh-cn_topic_0107606742_p6291134715618"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row22865476406"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p569913598411"><a name="zh-cn_topic_0107606742_p569913598411"></a><a name="zh-cn_topic_0107606742_p569913598411"></a>cpu_usage_nice</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p18338192592712"><a name="zh-cn_topic_0107606742_p18338192592712"></a><a name="zh-cn_topic_0107606742_p18338192592712"></a>（Agent）Nice进程CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p14357142313313"><a name="zh-cn_topic_0107606742_p14357142313313"></a><a name="zh-cn_topic_0107606742_p14357142313313"></a>该指标用于统计测量对象当前Nice进程CPU使用率。</p>
<p id="zh-cn_topic_0107606742_p182861747104013"><a name="zh-cn_topic_0107606742_p182861747104013"></a><a name="zh-cn_topic_0107606742_p182861747104013"></a>通过计算采集周期内/proc/stat中的变化得出Nice进程CPU使用率。用户可以通过<strong id="zh-cn_topic_0107606742_b1295818112591"><a name="zh-cn_topic_0107606742_b1295818112591"></a><a name="zh-cn_topic_0107606742_b1295818112591"></a>top</strong>命令查看 %Cpu(s) ni值。</p>
<p id="zh-cn_topic_0107606742_p628018138353"><a name="zh-cn_topic_0107606742_p628018138353"></a><a name="zh-cn_topic_0107606742_p628018138353"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p2038612436341"><a name="zh-cn_topic_0107606742_p2038612436341"></a><a name="zh-cn_topic_0107606742_p2038612436341"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p13390114094912"><a name="zh-cn_topic_0107606742_p13390114094912"></a><a name="zh-cn_topic_0107606742_p13390114094912"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p20898203910163"><a name="zh-cn_topic_0107606742_p20898203910163"></a><a name="zh-cn_topic_0107606742_p20898203910163"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row142725794013"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p166991594414"><a name="zh-cn_topic_0107606742_p166991594414"></a><a name="zh-cn_topic_0107606742_p166991594414"></a>cpu_usage_iowait</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p12309132815275"><a name="zh-cn_topic_0107606742_p12309132815275"></a><a name="zh-cn_topic_0107606742_p12309132815275"></a>（Agent）iowait状态占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p5358182363312"><a name="zh-cn_topic_0107606742_p5358182363312"></a><a name="zh-cn_topic_0107606742_p5358182363312"></a>该指标用于统计测量对象当前iowait状态占用CPU的比率。</p>
<p id="zh-cn_topic_0107606742_p663920448413"><a name="zh-cn_topic_0107606742_p663920448413"></a><a name="zh-cn_topic_0107606742_p663920448413"></a>通过计算采集周期内/proc/stat中的变化得出iowait状态占比。</p>
<p id="zh-cn_topic_0107606742_p15303649101612"><a name="zh-cn_topic_0107606742_p15303649101612"></a><a name="zh-cn_topic_0107606742_p15303649101612"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b1457611515594"><a name="zh-cn_topic_0107606742_b1457611515594"></a><a name="zh-cn_topic_0107606742_b1457611515594"></a>top</strong>命令查看 %Cpu(s) wa值。</p>
<p id="zh-cn_topic_0107606742_p20874101814352"><a name="zh-cn_topic_0107606742_p20874101814352"></a><a name="zh-cn_topic_0107606742_p20874101814352"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p103931843173414"><a name="zh-cn_topic_0107606742_p103931843173414"></a><a name="zh-cn_topic_0107606742_p103931843173414"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p5260555124015"><a name="zh-cn_topic_0107606742_p5260555124015"></a><a name="zh-cn_topic_0107606742_p5260555124015"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p342785718405"><a name="zh-cn_topic_0107606742_p342785718405"></a><a name="zh-cn_topic_0107606742_p342785718405"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row20565515408"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p156991459344"><a name="zh-cn_topic_0107606742_p156991459344"></a><a name="zh-cn_topic_0107606742_p156991459344"></a>cpu_usage_irq</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p0789035152712"><a name="zh-cn_topic_0107606742_p0789035152712"></a><a name="zh-cn_topic_0107606742_p0789035152712"></a>（Agent）CPU中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p1358182311339"><a name="zh-cn_topic_0107606742_p1358182311339"></a><a name="zh-cn_topic_0107606742_p1358182311339"></a>该指标用于统计测量对象当前CPU处理中断用时占用CPU时间的比率，以百分比为单位。</p>
<p id="zh-cn_topic_0107606742_p9141124715417"><a name="zh-cn_topic_0107606742_p9141124715417"></a><a name="zh-cn_topic_0107606742_p9141124715417"></a>通过计算采集周期内/proc/stat中的变化得出CPU中断时间占比。</p>
<p id="zh-cn_topic_0107606742_p7187156151615"><a name="zh-cn_topic_0107606742_p7187156151615"></a><a name="zh-cn_topic_0107606742_p7187156151615"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b12259497594"><a name="zh-cn_topic_0107606742_b12259497594"></a><a name="zh-cn_topic_0107606742_b12259497594"></a>top</strong>命令查看 %Cpu(s) hi值。</p>
<p id="zh-cn_topic_0107606742_p19199108135311"><a name="zh-cn_topic_0107606742_p19199108135311"></a><a name="zh-cn_topic_0107606742_p19199108135311"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p144241746123419"><a name="zh-cn_topic_0107606742_p144241746123419"></a><a name="zh-cn_topic_0107606742_p144241746123419"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p1698212556400"><a name="zh-cn_topic_0107606742_p1698212556400"></a><a name="zh-cn_topic_0107606742_p1698212556400"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p145785119401"><a name="zh-cn_topic_0107606742_p145785119401"></a><a name="zh-cn_topic_0107606742_p145785119401"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row617334524011"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p369915596420"><a name="zh-cn_topic_0107606742_p369915596420"></a><a name="zh-cn_topic_0107606742_p369915596420"></a>cpu_usage_softirq</p>
</td>
<td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p103301332413"><a name="zh-cn_topic_0107606742_p103301332413"></a><a name="zh-cn_topic_0107606742_p103301332413"></a>（Agent）CPU软中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.660000000000004%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p335819233334"><a name="zh-cn_topic_0107606742_p335819233334"></a><a name="zh-cn_topic_0107606742_p335819233334"></a>该指标用于统计测量对象当前CPU处理软中断时间占用CPU时间的比率。</p>
<p id="zh-cn_topic_0107606742_p131853510412"><a name="zh-cn_topic_0107606742_p131853510412"></a><a name="zh-cn_topic_0107606742_p131853510412"></a>通过计算采集周期内/proc/stat中的变化得出CPU软中断时间占比。</p>
<p id="zh-cn_topic_0107606742_p20174114514406"><a name="zh-cn_topic_0107606742_p20174114514406"></a><a name="zh-cn_topic_0107606742_p20174114514406"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b1338551295912"><a name="zh-cn_topic_0107606742_b1338551295912"></a><a name="zh-cn_topic_0107606742_b1338551295912"></a>top</strong>命令查看 %Cpu(s) si值。</p>
<p id="zh-cn_topic_0107606742_p162243251359"><a name="zh-cn_topic_0107606742_p162243251359"></a><a name="zh-cn_topic_0107606742_p162243251359"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.120000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p14431194616341"><a name="zh-cn_topic_0107606742_p14431194616341"></a><a name="zh-cn_topic_0107606742_p14431194616341"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p151557174020"><a name="zh-cn_topic_0107606742_p151557174020"></a><a name="zh-cn_topic_0107606742_p151557174020"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.03%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p14331613173"><a name="zh-cn_topic_0107606742_p14331613173"></a><a name="zh-cn_topic_0107606742_p14331613173"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 2**  CPU负载指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table341241110501"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row04121111185015"><th class="cellrowborder" valign="top" width="10.93%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p1390722513619"><a name="zh-cn_topic_0107606742_p1390722513619"></a><a name="zh-cn_topic_0107606742_p1390722513619"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.23%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1155321135012"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1155321135012"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1155321135012"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.75%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4155152175018"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4155152175018"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4155152175018"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.85%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p315532115017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p315532115017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p315532115017"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.33%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1815522175014"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1815522175014"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1815522175014"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.91%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p8758203511818"><a name="zh-cn_topic_0107606742_p8758203511818"></a><a name="zh-cn_topic_0107606742_p8758203511818"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row16413811105014"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1390717256610"><a name="zh-cn_topic_0107606742_p1390717256610"></a><a name="zh-cn_topic_0107606742_p1390717256610"></a>load_average1</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p415572125013"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p415572125013"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p415572125013"></a>（Agent）1分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="34.75%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1215572115019"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1215572115019"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1215572115019"></a>该指标用于统计测量对象在过去1分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155112135016"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155112135016"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155112135016"></a>通过“/proc/loadavg”文件中load1/逻辑CPU个数得到。</p>
<p id="zh-cn_topic_0107606742_p143187110186"><a name="zh-cn_topic_0107606742_p143187110186"></a><a name="zh-cn_topic_0107606742_p143187110186"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b13696142816511"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b13696142816511"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b13696142816511"></a>top</strong>命令查看“load1”值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.85%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17155821115010"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17155821115010"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17155821115010"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="11.33%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7155112145020"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7155112145020"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7155112145020"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12155192116500"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12155192116500"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12155192116500"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row34131011155017"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p49077251062"><a name="zh-cn_topic_0107606742_p49077251062"></a><a name="zh-cn_topic_0107606742_p49077251062"></a>load_average5</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1515562117503"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1515562117503"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1515562117503"></a>（Agent）5分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="34.75%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p6155221105019"></a>该指标用于统计测量对象在过去5分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p715511219509"></a>通过“/proc/loadavg”文件中load5/逻辑CPU个数得到。</p>
<p id="zh-cn_topic_0107606742_p98941691813"><a name="zh-cn_topic_0107606742_p98941691813"></a><a name="zh-cn_topic_0107606742_p98941691813"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b28441821263"></a>top</strong>命令查看“load5”值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.85%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15155192115011"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15155192115011"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p15155192115011"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="11.33%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155202114505"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155202114505"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p8155202114505"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p91551621105013"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p91551621105013"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p91551621105013"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row19413181125020"><td class="cellrowborder" valign="top" width="10.93%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p4907132517616"><a name="zh-cn_topic_0107606742_p4907132517616"></a><a name="zh-cn_topic_0107606742_p4907132517616"></a>load_average15</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p36631706418"><a name="zh-cn_topic_0107606742_p36631706418"></a><a name="zh-cn_topic_0107606742_p36631706418"></a>（Agent）15分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="34.75%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p51551021115010"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p51551021115010"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p51551021115010"></a>该指标用于统计测量对象在过去15分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p20156112115503"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p20156112115503"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p20156112115503"></a>通过“/proc/loadavg”中load15/逻辑CPU个数得到。</p>
<p id="zh-cn_topic_0107606742_p19366201331810"><a name="zh-cn_topic_0107606742_p19366201331810"></a><a name="zh-cn_topic_0107606742_p19366201331810"></a>用户可以通过<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b0142440265"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b0142440265"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b0142440265"></a>top</strong>命令查看“load15”值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.85%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p161557217508"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p161557217508"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p161557217508"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="11.33%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2156421105012"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2156421105012"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2156421105012"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11561221195018"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11561221195018"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11561221195018"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 3**  内存相关监控指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table844220384507"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row6442153818506"><th class="cellrowborder" valign="top" width="10.74%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p18774183711"><a name="zh-cn_topic_0107606742_p18774183711"></a><a name="zh-cn_topic_0107606742_p18774183711"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.44%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p751312468504"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p751312468504"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p751312468504"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.699999999999996%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p135131046165017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p135131046165017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p135131046165017"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.08%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p351319467501"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p351319467501"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p351319467501"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.14%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p175131146125015"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p175131146125015"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p175131146125015"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.900000000000002%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p2081818792116"><a name="zh-cn_topic_0107606742_p2081818792116"></a><a name="zh-cn_topic_0107606742_p2081818792116"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row1744223825017"><td class="cellrowborder" valign="top" width="10.74%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p147741581073"><a name="zh-cn_topic_0107606742_p147741581073"></a><a name="zh-cn_topic_0107606742_p147741581073"></a>mem_available</p>
</td>
<td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351394675019"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351394675019"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351394675019"></a>（Agent）可用内存</p>
</td>
<td class="cellrowborder" valign="top" width="34.699999999999996%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7513144620504"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7513144620504"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p7513144620504"></a>该指标用于统计测量对象的可用内存。</p>
<p id="zh-cn_topic_0107606742_p68441420162011"><a name="zh-cn_topic_0107606742_p68441420162011"></a><a name="zh-cn_topic_0107606742_p68441420162011"></a>通过“/proc/meminfo”文件得到MemAvailable。若“/proc/meminfo”中不显示MemAvailable，则MemAvailable=MemFree+Buffers+Cached。</p>
<p id="zh-cn_topic_0107606742_p0974102253715"><a name="zh-cn_topic_0107606742_p0974102253715"></a><a name="zh-cn_topic_0107606742_p0974102253715"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.08%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351534645020"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351534645020"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1351534645020"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4515154685010"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4515154685010"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4515154685010"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p151513466505"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p151513466505"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p151513466505"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row64421238175015"><td class="cellrowborder" valign="top" width="10.74%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p3774138379"><a name="zh-cn_topic_0107606742_p3774138379"></a><a name="zh-cn_topic_0107606742_p3774138379"></a>mem_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1951544645010"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1951544645010"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1951544645010"></a>（Agent）内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.699999999999996%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p145151046205017"></a>该指标用于统计测量对象的内存使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p55151946185013"></a>通过“/proc/meminfo”文件获取。计算公式：(MemTotal-MemAvailable)/MemTotal。</p>
<p id="zh-cn_topic_0107606742_p1728710269372"><a name="zh-cn_topic_0107606742_p1728710269372"></a><a name="zh-cn_topic_0107606742_p1728710269372"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.08%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17515114695018"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17515114695018"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17515114695018"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11515144665011"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11515144665011"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11515144665011"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p787173514200"><a name="zh-cn_topic_0107606742_p787173514200"></a><a name="zh-cn_topic_0107606742_p787173514200"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row9998183034219"><td class="cellrowborder" valign="top" width="10.74%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1277417814711"><a name="zh-cn_topic_0107606742_p1277417814711"></a><a name="zh-cn_topic_0107606742_p1277417814711"></a>mem_free</p>
</td>
<td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p13461198162815"><a name="zh-cn_topic_0107606742_p13461198162815"></a><a name="zh-cn_topic_0107606742_p13461198162815"></a>（Agent）空闲内存量</p>
</td>
<td class="cellrowborder" valign="top" width="34.699999999999996%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p446198172813"><a name="zh-cn_topic_0107606742_p446198172813"></a><a name="zh-cn_topic_0107606742_p446198172813"></a>该指标用于统计测量对象的空闲内存量。</p>
<p id="zh-cn_topic_0107606742_p11841446192013"><a name="zh-cn_topic_0107606742_p11841446192013"></a><a name="zh-cn_topic_0107606742_p11841446192013"></a>通过/proc/meminfo获取。</p>
<p id="zh-cn_topic_0107606742_p854054214372"><a name="zh-cn_topic_0107606742_p854054214372"></a><a name="zh-cn_topic_0107606742_p854054214372"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.08%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1646188112819"><a name="zh-cn_topic_0107606742_p1646188112819"></a><a name="zh-cn_topic_0107606742_p1646188112819"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p20461168132819"><a name="zh-cn_topic_0107606742_p20461168132819"></a><a name="zh-cn_topic_0107606742_p20461168132819"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1998130164211"><a name="zh-cn_topic_0107606742_p1998130164211"></a><a name="zh-cn_topic_0107606742_p1998130164211"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row105051636144210"><td class="cellrowborder" valign="top" width="10.74%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1977412817712"><a name="zh-cn_topic_0107606742_p1977412817712"></a><a name="zh-cn_topic_0107606742_p1977412817712"></a>mem_buffers</p>
</td>
<td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p1097541222813"><a name="zh-cn_topic_0107606742_p1097541222813"></a><a name="zh-cn_topic_0107606742_p1097541222813"></a>（Agent）Buffers占用量</p>
</td>
<td class="cellrowborder" valign="top" width="34.699999999999996%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p1491524514516"><a name="zh-cn_topic_0107606742_p1491524514516"></a><a name="zh-cn_topic_0107606742_p1491524514516"></a>该指标用于统计测量对象的Buffers内存量。</p>
<p id="zh-cn_topic_0107606742_p20825412143613"><a name="zh-cn_topic_0107606742_p20825412143613"></a><a name="zh-cn_topic_0107606742_p20825412143613"></a>通过/proc/meminfo获取。</p>
<p id="zh-cn_topic_0107606742_p1965710529208"><a name="zh-cn_topic_0107606742_p1965710529208"></a><a name="zh-cn_topic_0107606742_p1965710529208"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b161722665912"><a name="zh-cn_topic_0107606742_b161722665912"></a><a name="zh-cn_topic_0107606742_b161722665912"></a>top</strong>命令查看 KiB Mem:buffers值。</p>
<p id="zh-cn_topic_0107606742_p1072511511372"><a name="zh-cn_topic_0107606742_p1072511511372"></a><a name="zh-cn_topic_0107606742_p1072511511372"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.08%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1975131212815"><a name="zh-cn_topic_0107606742_p1975131212815"></a><a name="zh-cn_topic_0107606742_p1975131212815"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p397571215283"><a name="zh-cn_topic_0107606742_p397571215283"></a><a name="zh-cn_topic_0107606742_p397571215283"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p288693644310"><a name="zh-cn_topic_0107606742_p288693644310"></a><a name="zh-cn_topic_0107606742_p288693644310"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row153632028144210"><td class="cellrowborder" valign="top" width="10.74%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p97741281374"><a name="zh-cn_topic_0107606742_p97741281374"></a><a name="zh-cn_topic_0107606742_p97741281374"></a>mem_cached</p>
</td>
<td class="cellrowborder" valign="top" width="17.44%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p1996519532814"><a name="zh-cn_topic_0107606742_p1996519532814"></a><a name="zh-cn_topic_0107606742_p1996519532814"></a>（Agent）Cache占用量</p>
</td>
<td class="cellrowborder" valign="top" width="34.699999999999996%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p15966946124515"><a name="zh-cn_topic_0107606742_p15966946124515"></a><a name="zh-cn_topic_0107606742_p15966946124515"></a>该指标用于统计测量对象Cache内存量。</p>
<p id="zh-cn_topic_0107606742_p196571126183613"><a name="zh-cn_topic_0107606742_p196571126183613"></a><a name="zh-cn_topic_0107606742_p196571126183613"></a>通过/proc/meminfo获取。</p>
<p id="zh-cn_topic_0107606742_p245516282434"><a name="zh-cn_topic_0107606742_p245516282434"></a><a name="zh-cn_topic_0107606742_p245516282434"></a>用户可以通过<strong id="zh-cn_topic_0107606742_b12251192311594"><a name="zh-cn_topic_0107606742_b12251192311594"></a><a name="zh-cn_topic_0107606742_b12251192311594"></a>top</strong>命令查看 KiB Swap:cached Mem值。</p>
<p id="zh-cn_topic_0107606742_p820055743717"><a name="zh-cn_topic_0107606742_p820055743717"></a><a name="zh-cn_topic_0107606742_p820055743717"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.08%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p296519522819"><a name="zh-cn_topic_0107606742_p296519522819"></a><a name="zh-cn_topic_0107606742_p296519522819"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.14%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p89657513281"><a name="zh-cn_topic_0107606742_p89657513281"></a><a name="zh-cn_topic_0107606742_p89657513281"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1948045614207"><a name="zh-cn_topic_0107606742_p1948045614207"></a><a name="zh-cn_topic_0107606742_p1948045614207"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 4**  磁盘相关监控指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1067218184514"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row1673171813517"><th class="cellrowborder" valign="top" width="10.741074107410741%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p117713919819"><a name="zh-cn_topic_0107606742_p117713919819"></a><a name="zh-cn_topic_0107606742_p117713919819"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.331733173317332%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1938953325118"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1938953325118"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1938953325118"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.713471347134714%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3389163316514"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3389163316514"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3389163316514"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.520952095209521%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p138963317515"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p138963317515"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p138963317515"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.03110311031103%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1389183312512"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1389183312512"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1389183312512"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.661666166616662%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p4225141812217"><a name="zh-cn_topic_0107606742_p4225141812217"></a><a name="zh-cn_topic_0107606742_p4225141812217"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row7673318135112"><td class="cellrowborder" valign="top" width="10.741074107410741%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p377112919816"><a name="zh-cn_topic_0107606742_p377112919816"></a><a name="zh-cn_topic_0107606742_p377112919816"></a>mountPointPrefix_disk_free</p>
</td>
<td class="cellrowborder" valign="top" width="17.331733173317332%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113891733165111"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113891733165111"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113891733165111"></a>（Agent）磁盘剩余存储量</p>
</td>
<td class="cellrowborder" valign="top" width="34.713471347134714%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238993314518"></a>该指标用于统计测量对象磁盘的剩余存储空间。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1338903314517"></a>执行<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b17687744586"></a>df -h</strong>命令，查看Avail列数据。</p>
<p id="zh-cn_topic_0107606742_p6772134582115"><a name="zh-cn_topic_0107606742_p6772134582115"></a><a name="zh-cn_topic_0107606742_p6772134582115"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p1961921713810"><a name="zh-cn_topic_0107606742_p1961921713810"></a><a name="zh-cn_topic_0107606742_p1961921713810"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.520952095209521%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0389163365115"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0389163365115"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p0389163365115"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.03110311031103%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1538913355110"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1538913355110"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1538913355110"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.661666166616662%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p18727185919557"><a name="zh-cn_topic_0107606742_p18727185919557"></a><a name="zh-cn_topic_0107606742_p18727185919557"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row1667341845112"><td class="cellrowborder" valign="top" width="10.741074107410741%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p19771892085"><a name="zh-cn_topic_0107606742_p19771892085"></a><a name="zh-cn_topic_0107606742_p19771892085"></a>mountPointPrefix_disk_total</p>
</td>
<td class="cellrowborder" valign="top" width="17.331733173317332%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p18389533165112"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p18389533165112"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p18389533165112"></a>（Agent）磁盘存储总量</p>
</td>
<td class="cellrowborder" valign="top" width="34.713471347134714%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2038910335511"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2038910335511"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2038910335511"></a>该指标用于统计测量对象磁盘存储总量。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139010332517"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139010332517"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139010332517"></a>执行<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1924915481981"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1924915481981"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1924915481981"></a>df -h</strong>命令，查看Size列数据。</p>
<p id="zh-cn_topic_0107606742_p19373543219"><a name="zh-cn_topic_0107606742_p19373543219"></a><a name="zh-cn_topic_0107606742_p19373543219"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p851524123818"><a name="zh-cn_topic_0107606742_p851524123818"></a><a name="zh-cn_topic_0107606742_p851524123818"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.520952095209521%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238917334512"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238917334512"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1238917334512"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.03110311031103%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17390163310513"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17390163310513"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p17390163310513"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.661666166616662%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p148682267225"><a name="zh-cn_topic_0107606742_p148682267225"></a><a name="zh-cn_topic_0107606742_p148682267225"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row0673191815515"><td class="cellrowborder" valign="top" width="10.741074107410741%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p17711491183"><a name="zh-cn_topic_0107606742_p17711491183"></a><a name="zh-cn_topic_0107606742_p17711491183"></a>mountPointPrefix_disk_used</p>
</td>
<td class="cellrowborder" valign="top" width="17.331733173317332%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p839018338516"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p839018338516"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p839018338516"></a>（Agent）磁盘已用存储量</p>
</td>
<td class="cellrowborder" valign="top" width="34.713471347134714%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13390113385119"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13390113385119"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13390113385119"></a>该指标用于统计测量对象磁盘的已用存储空间。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1839083310512"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1839083310512"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1839083310512"></a>执行<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1793412910"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1793412910"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1793412910"></a>df -h</strong>命令，查看Used列数据。</p>
<p id="zh-cn_topic_0107606742_p13875212218"><a name="zh-cn_topic_0107606742_p13875212218"></a><a name="zh-cn_topic_0107606742_p13875212218"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p8711162973819"><a name="zh-cn_topic_0107606742_p8711162973819"></a><a name="zh-cn_topic_0107606742_p8711162973819"></a>单位：GB</p>
</td>
<td class="cellrowborder" valign="top" width="9.520952095209521%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2039017331518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2039017331518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2039017331518"></a>≥ 0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="11.03110311031103%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139015335513"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139015335513"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139015335513"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.661666166616662%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p15916162718225"><a name="zh-cn_topic_0107606742_p15916162718225"></a><a name="zh-cn_topic_0107606742_p15916162718225"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row11673618205115"><td class="cellrowborder" valign="top" width="10.741074107410741%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p17721291380"><a name="zh-cn_topic_0107606742_p17721291380"></a><a name="zh-cn_topic_0107606742_p17721291380"></a>mountPointPrefix_disk_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="17.331733173317332%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139013355117"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139013355117"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1139013355117"></a>（Agent）磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.713471347134714%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2390203318518"></a>该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为：磁盘已用存储量/磁盘存储总量。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p103901733125117"></a>通过计算Used/Size得出。</p>
<p id="zh-cn_topic_0107606742_p464848112210"><a name="zh-cn_topic_0107606742_p464848112210"></a><a name="zh-cn_topic_0107606742_p464848112210"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p196724114386"><a name="zh-cn_topic_0107606742_p196724114386"></a><a name="zh-cn_topic_0107606742_p196724114386"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.520952095209521%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113901533155112"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113901533155112"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p113901533155112"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.03110311031103%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1939073335116"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1939073335116"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1939073335116"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.661666166616662%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p17691628112210"><a name="zh-cn_topic_0107606742_p17691628112210"></a><a name="zh-cn_topic_0107606742_p17691628112210"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 5**  磁盘I/O相关监控指标说明

<a name="zh-cn_topic_0107606742_table1559955415558"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_row20615854145518"><th class="cellrowborder" valign="top" width="10.63893610638936%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p81971210596"><a name="zh-cn_topic_0107606742_p81971210596"></a><a name="zh-cn_topic_0107606742_p81971210596"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.228277172282773%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_p1462035465515"><a name="zh-cn_topic_0107606742_p1462035465515"></a><a name="zh-cn_topic_0107606742_p1462035465515"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="35.03649635036496%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_p1962255445518"><a name="zh-cn_topic_0107606742_p1962255445518"></a><a name="zh-cn_topic_0107606742_p1962255445518"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.24907509249075%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_p862618540554"><a name="zh-cn_topic_0107606742_p862618540554"></a><a name="zh-cn_topic_0107606742_p862618540554"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.048895110488951%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_p106288542554"><a name="zh-cn_topic_0107606742_p106288542554"></a><a name="zh-cn_topic_0107606742_p106288542554"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.798320167983203%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p971315116293"><a name="zh-cn_topic_0107606742_p971315116293"></a><a name="zh-cn_topic_0107606742_p971315116293"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_row187021054125517"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1919710101693"><a name="zh-cn_topic_0107606742_p1919710101693"></a><a name="zh-cn_topic_0107606742_p1919710101693"></a>mountPointPrefix_disk_agt_read_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p18704954115515"><a name="zh-cn_topic_0107606742_p18704954115515"></a><a name="zh-cn_topic_0107606742_p18704954115515"></a>（Agent）磁盘读速率</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p47061754115520"><a name="zh-cn_topic_0107606742_p47061754115520"></a><a name="zh-cn_topic_0107606742_p47061754115520"></a>该指标用于统计每秒从测量对象磁盘读出的数据量。</p>
<p id="zh-cn_topic_0107606742_p107156545559"><a name="zh-cn_topic_0107606742_p107156545559"></a><a name="zh-cn_topic_0107606742_p107156545559"></a>通过计算采集周期内“/proc/diskstats”文件中对应设备第六列数据的变化得出磁盘读速率。</p>
<p id="zh-cn_topic_0107606742_p13404181214236"><a name="zh-cn_topic_0107606742_p13404181214236"></a><a name="zh-cn_topic_0107606742_p13404181214236"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p148356163915"><a name="zh-cn_topic_0107606742_p148356163915"></a><a name="zh-cn_topic_0107606742_p148356163915"></a>单位：byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p17081454175517"><a name="zh-cn_topic_0107606742_p17081454175517"></a><a name="zh-cn_topic_0107606742_p17081454175517"></a>≥ 0 byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p8712754155516"><a name="zh-cn_topic_0107606742_p8712754155516"></a><a name="zh-cn_topic_0107606742_p8712754155516"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p2058314532918"><a name="zh-cn_topic_0107606742_p2058314532918"></a><a name="zh-cn_topic_0107606742_p2058314532918"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row187171154145512"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1519731016916"><a name="zh-cn_topic_0107606742_p1519731016916"></a><a name="zh-cn_topic_0107606742_p1519731016916"></a>mountPointPrefix_disk_agt_read_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p1272025495519"><a name="zh-cn_topic_0107606742_p1272025495519"></a><a name="zh-cn_topic_0107606742_p1272025495519"></a>（Agent）磁盘读操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p8723154175514"><a name="zh-cn_topic_0107606742_p8723154175514"></a><a name="zh-cn_topic_0107606742_p8723154175514"></a>该指标用于统计每秒从测量对象磁盘读取数据的请求次数。</p>
<p id="zh-cn_topic_0107606742_p17332054145515"><a name="zh-cn_topic_0107606742_p17332054145515"></a><a name="zh-cn_topic_0107606742_p17332054145515"></a>通过计算采集周期内“/proc/diskstats”文件中对应设备第四列数据的变化得出磁盘读操作速率。</p>
<p id="zh-cn_topic_0107606742_p7646163514279"><a name="zh-cn_topic_0107606742_p7646163514279"></a><a name="zh-cn_topic_0107606742_p7646163514279"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p179753333915"><a name="zh-cn_topic_0107606742_p179753333915"></a><a name="zh-cn_topic_0107606742_p179753333915"></a>单位：请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p172715415516"><a name="zh-cn_topic_0107606742_p172715415516"></a><a name="zh-cn_topic_0107606742_p172715415516"></a>≥ 0 请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p27303545559"><a name="zh-cn_topic_0107606742_p27303545559"></a><a name="zh-cn_topic_0107606742_p27303545559"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1451914662911"><a name="zh-cn_topic_0107606742_p1451914662911"></a><a name="zh-cn_topic_0107606742_p1451914662911"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row17341854175518"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1919712105912"><a name="zh-cn_topic_0107606742_p1919712105912"></a><a name="zh-cn_topic_0107606742_p1919712105912"></a>mountPointPrefix_disk_agt_write_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p117361554115512"><a name="zh-cn_topic_0107606742_p117361554115512"></a><a name="zh-cn_topic_0107606742_p117361554115512"></a>（Agent）磁盘写速率</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p0739954115518"><a name="zh-cn_topic_0107606742_p0739954115518"></a><a name="zh-cn_topic_0107606742_p0739954115518"></a>该指标用于统计每秒写到测量对象磁盘的数据量。</p>
<p id="zh-cn_topic_0107606742_p14750175416553"><a name="zh-cn_topic_0107606742_p14750175416553"></a><a name="zh-cn_topic_0107606742_p14750175416553"></a>通过计算采集周期内“/proc/diskstats”文件中对应设备第十列数据的变化得出磁盘写速率。</p>
<p id="zh-cn_topic_0107606742_p1394334212717"><a name="zh-cn_topic_0107606742_p1394334212717"></a><a name="zh-cn_topic_0107606742_p1394334212717"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p7497720123911"><a name="zh-cn_topic_0107606742_p7497720123911"></a><a name="zh-cn_topic_0107606742_p7497720123911"></a>单位：byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1574475475512"><a name="zh-cn_topic_0107606742_p1574475475512"></a><a name="zh-cn_topic_0107606742_p1574475475512"></a>≥ 0 byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p1674635465519"><a name="zh-cn_topic_0107606742_p1674635465519"></a><a name="zh-cn_topic_0107606742_p1674635465519"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p68469102920"><a name="zh-cn_topic_0107606742_p68469102920"></a><a name="zh-cn_topic_0107606742_p68469102920"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1775125416551"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p15197110599"><a name="zh-cn_topic_0107606742_p15197110599"></a><a name="zh-cn_topic_0107606742_p15197110599"></a>mountPointPrefix_disk_agt_write_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p575325417553"><a name="zh-cn_topic_0107606742_p575325417553"></a><a name="zh-cn_topic_0107606742_p575325417553"></a>（Agent）磁盘写操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p4755195416554"><a name="zh-cn_topic_0107606742_p4755195416554"></a><a name="zh-cn_topic_0107606742_p4755195416554"></a>该指标用于统计每秒向测量对象磁盘写数据的请求次数。</p>
<p id="zh-cn_topic_0107606742_p15764125418557"><a name="zh-cn_topic_0107606742_p15764125418557"></a><a name="zh-cn_topic_0107606742_p15764125418557"></a>通过计算采集周期内“/proc/diskstats”文件中对应设备第八列数据的变化得出磁盘写操作速率。</p>
<p id="zh-cn_topic_0107606742_p156580521272"><a name="zh-cn_topic_0107606742_p156580521272"></a><a name="zh-cn_topic_0107606742_p156580521272"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p444414443393"><a name="zh-cn_topic_0107606742_p444414443393"></a><a name="zh-cn_topic_0107606742_p444414443393"></a>单位：请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p875985415559"><a name="zh-cn_topic_0107606742_p875985415559"></a><a name="zh-cn_topic_0107606742_p875985415559"></a>≥ 0 请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p67628546556"><a name="zh-cn_topic_0107606742_p67628546556"></a><a name="zh-cn_topic_0107606742_p67628546556"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p16168171042915"><a name="zh-cn_topic_0107606742_p16168171042915"></a><a name="zh-cn_topic_0107606742_p16168171042915"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row138761052155714"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p019716101894"><a name="zh-cn_topic_0107606742_p019716101894"></a><a name="zh-cn_topic_0107606742_p019716101894"></a>disk_readTime</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1888124844819"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1888124844819"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1888124844819"></a>（Agent）读操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p15890164812481"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p15890164812481"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p15890164812481"></a>该指标用于统计测量对象磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0107606742_p487810529578"><a name="zh-cn_topic_0107606742_p487810529578"></a><a name="zh-cn_topic_0107606742_p487810529578"></a>通过计算采集周期内/proc/diskstats中对应设备第七列数据的变化得出磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0107606742_p71451732125"><a name="zh-cn_topic_0107606742_p71451732125"></a><a name="zh-cn_topic_0107606742_p71451732125"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p123431514403"><a name="zh-cn_topic_0107606742_p123431514403"></a><a name="zh-cn_topic_0107606742_p123431514403"></a>单位：ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p761943410503"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p761943410503"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p761943410503"></a>≥ 0 ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p942165217407"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p942165217407"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p942165217407"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p12741131122918"><a name="zh-cn_topic_0107606742_p12741131122918"></a><a name="zh-cn_topic_0107606742_p12741131122918"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row782895555718"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p61970105914"><a name="zh-cn_topic_0107606742_p61970105914"></a><a name="zh-cn_topic_0107606742_p61970105914"></a>disk_writeTime</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p48901848154819"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p48901848154819"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p48901848154819"></a>（Agent）写操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p2890104810484"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p2890104810484"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p2890104810484"></a>该指标用于统计测量对象磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0107606742_p182885514571"><a name="zh-cn_topic_0107606742_p182885514571"></a><a name="zh-cn_topic_0107606742_p182885514571"></a>通过计算采集周期内/proc/diskstats中对应设备第十一列数据的变化得出磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0107606742_p163011351529"><a name="zh-cn_topic_0107606742_p163011351529"></a><a name="zh-cn_topic_0107606742_p163011351529"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p1139961424013"><a name="zh-cn_topic_0107606742_p1139961424013"></a><a name="zh-cn_topic_0107606742_p1139961424013"></a>单位：ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p166190349509"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p166190349509"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p166190349509"></a>≥ 0 ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p423815418405"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p423815418405"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p423815418405"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p414611312912"><a name="zh-cn_topic_0107606742_p414611312912"></a><a name="zh-cn_topic_0107606742_p414611312912"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1555285865716"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p171978101196"><a name="zh-cn_topic_0107606742_p171978101196"></a><a name="zh-cn_topic_0107606742_p171978101196"></a>disk_ioUtils</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p198904485488"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p198904485488"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p198904485488"></a>（Agent）磁盘I/O使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p6204818503"></a>该指标用于统计测量对象磁盘I/O使用率。</p>
<p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p990615654016"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。</p>
<p id="zh-cn_topic_0107606742_p1090014381522"><a name="zh-cn_topic_0107606742_p1090014381522"></a><a name="zh-cn_topic_0107606742_p1090014381522"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p5387192112400"><a name="zh-cn_topic_0107606742_p5387192112400"></a><a name="zh-cn_topic_0107606742_p5387192112400"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1761915344507"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1761915344507"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1761915344507"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p19897165664017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p19897165664017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p19897165664017"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p78241018192911"><a name="zh-cn_topic_0107606742_p78241018192911"></a><a name="zh-cn_topic_0107606742_p78241018192911"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row10579194514424"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p019751018917"><a name="zh-cn_topic_0107606742_p019751018917"></a><a name="zh-cn_topic_0107606742_p019751018917"></a>disk_queue_length</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p713715519426"><a name="zh-cn_topic_0107606742_p713715519426"></a><a name="zh-cn_topic_0107606742_p713715519426"></a>（Agent）平均队列长度</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p1314212554429"><a name="zh-cn_topic_0107606742_p1314212554429"></a><a name="zh-cn_topic_0107606742_p1314212554429"></a>该指标用于统计指定时间段内，平均等待完成的读取或写入操作请求的数量。</p>
<p id="zh-cn_topic_0107606742_p11809211915"><a name="zh-cn_topic_0107606742_p11809211915"></a><a name="zh-cn_topic_0107606742_p11809211915"></a>通过计算采集周期内/proc/diskstats中对应设备第十四列数据的变化得出磁盘平均队列长度。</p>
<p id="zh-cn_topic_0107606742_p1813151012"><a name="zh-cn_topic_0107606742_p1813151012"></a><a name="zh-cn_topic_0107606742_p1813151012"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p514635511420"><a name="zh-cn_topic_0107606742_p514635511420"></a><a name="zh-cn_topic_0107606742_p514635511420"></a>单位：个</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p5152355184210"><a name="zh-cn_topic_0107606742_p5152355184210"></a><a name="zh-cn_topic_0107606742_p5152355184210"></a>≥ 0 个</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p2015512557427"><a name="zh-cn_topic_0107606742_p2015512557427"></a><a name="zh-cn_topic_0107606742_p2015512557427"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p20512202072913"><a name="zh-cn_topic_0107606742_p20512202072913"></a><a name="zh-cn_topic_0107606742_p20512202072913"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row95818494421"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p9197121014916"><a name="zh-cn_topic_0107606742_p9197121014916"></a><a name="zh-cn_topic_0107606742_p9197121014916"></a>disk_write_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p3172175574210"><a name="zh-cn_topic_0107606742_p3172175574210"></a><a name="zh-cn_topic_0107606742_p3172175574210"></a>（Agent）平均写操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p13177755184215"><a name="zh-cn_topic_0107606742_p13177755184215"></a><a name="zh-cn_topic_0107606742_p13177755184215"></a>该指标用于统计指定时间段内，平均每个写I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0107606742_p161522251118"><a name="zh-cn_topic_0107606742_p161522251118"></a><a name="zh-cn_topic_0107606742_p161522251118"></a>通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化与第八列数据的变化相除得出磁盘平均写操作大小。</p>
<p id="zh-cn_topic_0107606742_p127948355281"><a name="zh-cn_topic_0107606742_p127948355281"></a><a name="zh-cn_topic_0107606742_p127948355281"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p318012553426"><a name="zh-cn_topic_0107606742_p318012553426"></a><a name="zh-cn_topic_0107606742_p318012553426"></a>单位：KB/op</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p8186135574216"><a name="zh-cn_topic_0107606742_p8186135574216"></a><a name="zh-cn_topic_0107606742_p8186135574216"></a>≥ 0 KB/op</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p819113557425"><a name="zh-cn_topic_0107606742_p819113557425"></a><a name="zh-cn_topic_0107606742_p819113557425"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1831052317294"><a name="zh-cn_topic_0107606742_p1831052317294"></a><a name="zh-cn_topic_0107606742_p1831052317294"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row12607155119421"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p21971210698"><a name="zh-cn_topic_0107606742_p21971210698"></a><a name="zh-cn_topic_0107606742_p21971210698"></a>disk_read_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p92061755184217"><a name="zh-cn_topic_0107606742_p92061755184217"></a><a name="zh-cn_topic_0107606742_p92061755184217"></a>（Agent）平均读操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p521217557424"><a name="zh-cn_topic_0107606742_p521217557424"></a><a name="zh-cn_topic_0107606742_p521217557424"></a>该指标用于统计指定时间段内，平均每个读I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0107606742_p19145105520218"><a name="zh-cn_topic_0107606742_p19145105520218"></a><a name="zh-cn_topic_0107606742_p19145105520218"></a>通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化与第四列数据的变化相除得出磁盘平均读操作大小。</p>
<p id="zh-cn_topic_0107606742_p114817551628"><a name="zh-cn_topic_0107606742_p114817551628"></a><a name="zh-cn_topic_0107606742_p114817551628"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p10214135515421"><a name="zh-cn_topic_0107606742_p10214135515421"></a><a name="zh-cn_topic_0107606742_p10214135515421"></a>单位：KB/op</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p152207559426"><a name="zh-cn_topic_0107606742_p152207559426"></a><a name="zh-cn_topic_0107606742_p152207559426"></a>≥ 0 KB/op</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p722625515424"><a name="zh-cn_topic_0107606742_p722625515424"></a><a name="zh-cn_topic_0107606742_p722625515424"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p82292026192920"><a name="zh-cn_topic_0107606742_p82292026192920"></a><a name="zh-cn_topic_0107606742_p82292026192920"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row15805135318425"><td class="cellrowborder" valign="top" width="10.63893610638936%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p131976106910"><a name="zh-cn_topic_0107606742_p131976106910"></a><a name="zh-cn_topic_0107606742_p131976106910"></a>disk_io_svctm</p>
</td>
<td class="cellrowborder" valign="top" width="17.228277172282773%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p823855511428"><a name="zh-cn_topic_0107606742_p823855511428"></a><a name="zh-cn_topic_0107606742_p823855511428"></a>（Agent）平均I/O服务时长</p>
</td>
<td class="cellrowborder" valign="top" width="35.03649635036496%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p18245755124217"><a name="zh-cn_topic_0107606742_p18245755124217"></a><a name="zh-cn_topic_0107606742_p18245755124217"></a>该指标用于统计指定时间段内，平均每个读或写I/O的操作时长。</p>
<p id="zh-cn_topic_0107606742_p185331914314"><a name="zh-cn_topic_0107606742_p185331914314"></a><a name="zh-cn_topic_0107606742_p185331914314"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化与第四列数据与第八列数据和的变化相除得出磁盘平均I/O时长。</p>
<p id="zh-cn_topic_0107606742_p205464502286"><a name="zh-cn_topic_0107606742_p205464502286"></a><a name="zh-cn_topic_0107606742_p205464502286"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p152501855124215"><a name="zh-cn_topic_0107606742_p152501855124215"></a><a name="zh-cn_topic_0107606742_p152501855124215"></a>单位：ms/op</p>
</td>
<td class="cellrowborder" valign="top" width="9.24907509249075%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1125675517425"><a name="zh-cn_topic_0107606742_p1125675517425"></a><a name="zh-cn_topic_0107606742_p1125675517425"></a>≥ 0 ms/op</p>
</td>
<td class="cellrowborder" valign="top" width="11.048895110488951%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p326214556428"><a name="zh-cn_topic_0107606742_p326214556428"></a><a name="zh-cn_topic_0107606742_p326214556428"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.798320167983203%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p198871927182919"><a name="zh-cn_topic_0107606742_p198871927182919"></a><a name="zh-cn_topic_0107606742_p198871927182919"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 6**  文件系统类监控指标说明

<a name="zh-cn_topic_0107606742_table296913551343"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_row49905557345"><th class="cellrowborder" valign="top" width="10.438956104389561%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p468174911017"><a name="zh-cn_topic_0107606742_p468174911017"></a><a name="zh-cn_topic_0107606742_p468174911017"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.418258174182583%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_p2994055123412"><a name="zh-cn_topic_0107606742_p2994055123412"></a><a name="zh-cn_topic_0107606742_p2994055123412"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.876512348765125%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_p1599916553345"><a name="zh-cn_topic_0107606742_p1599916553345"></a><a name="zh-cn_topic_0107606742_p1599916553345"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.649035096490351%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_p93135623412"><a name="zh-cn_topic_0107606742_p93135623412"></a><a name="zh-cn_topic_0107606742_p93135623412"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.998900109989002%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_p10766173818117"><a name="zh-cn_topic_0107606742_p10766173818117"></a><a name="zh-cn_topic_0107606742_p10766173818117"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.61833816618338%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p1132563345"><a name="zh-cn_topic_0107606742_p1132563345"></a><a name="zh-cn_topic_0107606742_p1132563345"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_row146411425432"><td class="cellrowborder" valign="top" width="10.438956104389561%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p76815490107"><a name="zh-cn_topic_0107606742_p76815490107"></a><a name="zh-cn_topic_0107606742_p76815490107"></a>disk_fs_rwstate</p>
</td>
<td class="cellrowborder" valign="top" width="17.418258174182583%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p06744107437"><a name="zh-cn_topic_0107606742_p06744107437"></a><a name="zh-cn_topic_0107606742_p06744107437"></a>（Agent）文件系统读写状态</p>
</td>
<td class="cellrowborder" valign="top" width="34.876512348765125%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p186795108438"><a name="zh-cn_topic_0107606742_p186795108438"></a><a name="zh-cn_topic_0107606742_p186795108438"></a>该指标用于统计测量对象挂载文件系统的读写状态。状态分为：可读写（0）/只读（1）。</p>
<p id="zh-cn_topic_0107606742_p68391649142916"><a name="zh-cn_topic_0107606742_p68391649142916"></a><a name="zh-cn_topic_0107606742_p68391649142916"></a>通过读取/proc/mounts中第四列文件系统挂载参数获得。</p>
</td>
<td class="cellrowborder" valign="top" width="9.649035096490351%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1268416108435"><a name="zh-cn_topic_0107606742_p1268416108435"></a><a name="zh-cn_topic_0107606742_p1268416108435"></a>0，1</p>
</td>
<td class="cellrowborder" valign="top" width="10.998900109989002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p16690161011435"><a name="zh-cn_topic_0107606742_p16690161011435"></a><a name="zh-cn_topic_0107606742_p16690161011435"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.61833816618338%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p106921103436"><a name="zh-cn_topic_0107606742_p106921103436"></a><a name="zh-cn_topic_0107606742_p106921103436"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row4161756163419"><td class="cellrowborder" valign="top" width="10.438956104389561%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p16814913106"><a name="zh-cn_topic_0107606742_p16814913106"></a><a name="zh-cn_topic_0107606742_p16814913106"></a>disk_inodesTotal</p>
</td>
<td class="cellrowborder" valign="top" width="17.418258174182583%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_a3cf28f4ba8c34be683cf7c28eb36028e"><a name="zh-cn_topic_0107606742_a3cf28f4ba8c34be683cf7c28eb36028e"></a><a name="zh-cn_topic_0107606742_a3cf28f4ba8c34be683cf7c28eb36028e"></a>（Agent）inode空间大小</p>
</td>
<td class="cellrowborder" valign="top" width="34.876512348765125%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p6853181323"><a name="zh-cn_topic_0107606742_p6853181323"></a><a name="zh-cn_topic_0107606742_p6853181323"></a>该指标用于统计测量对象当前磁盘的inode空间量。执行<strong id="zh-cn_topic_0107606742_b177554231309"><a name="zh-cn_topic_0107606742_b177554231309"></a><a name="zh-cn_topic_0107606742_b177554231309"></a>df -i</strong>命令，查看Inodes列数据。</p>
<p id="zh-cn_topic_0107606742_p443104153012"><a name="zh-cn_topic_0107606742_p443104153012"></a><a name="zh-cn_topic_0107606742_p443104153012"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="9.649035096490351%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_a667a6062f5434cb381b861e3a52526f8"><a name="zh-cn_topic_0107606742_a667a6062f5434cb381b861e3a52526f8"></a><a name="zh-cn_topic_0107606742_a667a6062f5434cb381b861e3a52526f8"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.998900109989002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_abc87e5d61cf04150b58dfb974ce13aed"><a name="zh-cn_topic_0107606742_abc87e5d61cf04150b58dfb974ce13aed"></a><a name="zh-cn_topic_0107606742_abc87e5d61cf04150b58dfb974ce13aed"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.61833816618338%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p4933304312"><a name="zh-cn_topic_0107606742_p4933304312"></a><a name="zh-cn_topic_0107606742_p4933304312"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row7421756203419"><td class="cellrowborder" valign="top" width="10.438956104389561%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p176854921010"><a name="zh-cn_topic_0107606742_p176854921010"></a><a name="zh-cn_topic_0107606742_p176854921010"></a>disk_inodesUsed</p>
</td>
<td class="cellrowborder" valign="top" width="17.418258174182583%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_ada107ec63c5e48fc872d433a6d6431fa"><a name="zh-cn_topic_0107606742_ada107ec63c5e48fc872d433a6d6431fa"></a><a name="zh-cn_topic_0107606742_ada107ec63c5e48fc872d433a6d6431fa"></a>（Agent）inode已使用空间</p>
</td>
<td class="cellrowborder" valign="top" width="34.876512348765125%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_a964a48c0ba3c4f3cbeff333aa5dd7d6f"><a name="zh-cn_topic_0107606742_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a><a name="zh-cn_topic_0107606742_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a>该指标用于统计测量对象当前磁盘已使用的inode空间量。</p>
<p id="zh-cn_topic_0107606742_p18752745516"><a name="zh-cn_topic_0107606742_p18752745516"></a><a name="zh-cn_topic_0107606742_p18752745516"></a>执行<strong id="zh-cn_topic_0107606742_b1742744214588"><a name="zh-cn_topic_0107606742_b1742744214588"></a><a name="zh-cn_topic_0107606742_b1742744214588"></a>df -i</strong>命令，查看IUsed列数据。</p>
<p id="zh-cn_topic_0107606742_p179910344317"><a name="zh-cn_topic_0107606742_p179910344317"></a><a name="zh-cn_topic_0107606742_p179910344317"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="9.649035096490351%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_ac21f06dacf11428da8ad15257903cc2f"><a name="zh-cn_topic_0107606742_ac21f06dacf11428da8ad15257903cc2f"></a><a name="zh-cn_topic_0107606742_ac21f06dacf11428da8ad15257903cc2f"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.998900109989002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p189006115213"><a name="zh-cn_topic_0107606742_p189006115213"></a><a name="zh-cn_topic_0107606742_p189006115213"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.61833816618338%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p681611210308"><a name="zh-cn_topic_0107606742_p681611210308"></a><a name="zh-cn_topic_0107606742_p681611210308"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1362175683411"><td class="cellrowborder" valign="top" width="10.438956104389561%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1368949161014"><a name="zh-cn_topic_0107606742_p1368949161014"></a><a name="zh-cn_topic_0107606742_p1368949161014"></a>disk_inodesUsedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="17.418258174182583%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_aecb1139b3e694480b09dcb590ce395ed"><a name="zh-cn_topic_0107606742_aecb1139b3e694480b09dcb590ce395ed"></a><a name="zh-cn_topic_0107606742_aecb1139b3e694480b09dcb590ce395ed"></a>（Agent）inode已使用占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.876512348765125%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"><a name="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"></a><a name="zh-cn_topic_0107606742_af7d7bf90b33c4ab8a734dca22a9b0803"></a>该指标用于统计测量对象当前磁盘已使用的inode占比。</p>
<p id="zh-cn_topic_0107606742_p11890521116"><a name="zh-cn_topic_0107606742_p11890521116"></a><a name="zh-cn_topic_0107606742_p11890521116"></a>执行<strong id="zh-cn_topic_0107606742_b17532345115811"><a name="zh-cn_topic_0107606742_b17532345115811"></a><a name="zh-cn_topic_0107606742_b17532345115811"></a>df -i</strong>命令，查看IUse%列数据。</p>
<p id="zh-cn_topic_0107606742_p20144348934"><a name="zh-cn_topic_0107606742_p20144348934"></a><a name="zh-cn_topic_0107606742_p20144348934"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
<p id="zh-cn_topic_0107606742_p11782138145615"><a name="zh-cn_topic_0107606742_p11782138145615"></a><a name="zh-cn_topic_0107606742_p11782138145615"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.649035096490351%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_a976d888f07a94317952cbd3259ba9a2d"><a name="zh-cn_topic_0107606742_a976d888f07a94317952cbd3259ba9a2d"></a><a name="zh-cn_topic_0107606742_a976d888f07a94317952cbd3259ba9a2d"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.998900109989002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p6942317212"><a name="zh-cn_topic_0107606742_p6942317212"></a><a name="zh-cn_topic_0107606742_p6942317212"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.61833816618338%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p3139181873016"><a name="zh-cn_topic_0107606742_p3139181873016"></a><a name="zh-cn_topic_0107606742_p3139181873016"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 7**  网卡相关监控指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table19476249105111"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row20476849145110"><th class="cellrowborder" valign="top" width="10.35%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p3741131816125"><a name="zh-cn_topic_0107606742_p3741131816125"></a><a name="zh-cn_topic_0107606742_p3741131816125"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.630000000000003%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1392391135213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1392391135213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1392391135213"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.69%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p992381165212"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p992381165212"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p992381165212"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.77%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923911125218"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923911125218"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923911125218"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.200000000000001%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923121113524"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923121113524"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923121113524"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.36%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p15840154617214"><a name="zh-cn_topic_0107606742_p15840154617214"></a><a name="zh-cn_topic_0107606742_p15840154617214"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row154771649185115"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p6741618111217"><a name="zh-cn_topic_0107606742_p6741618111217"></a><a name="zh-cn_topic_0107606742_p6741618111217"></a>net_bitSent</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3923411195213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3923411195213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3923411195213"></a>（Agent）入网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p99231311175211"></a>该指标用于统计测量对象网卡每秒发送的比特数。</p>
<p id="zh-cn_topic_0107606742_p9414151572118"><a name="zh-cn_topic_0107606742_p9414151572118"></a><a name="zh-cn_topic_0107606742_p9414151572118"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p0780145612408"><a name="zh-cn_topic_0107606742_p0780145612408"></a><a name="zh-cn_topic_0107606742_p0780145612408"></a>单位：bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923911195217"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923711115215"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p118402467212"><a name="zh-cn_topic_0107606742_p118402467212"></a><a name="zh-cn_topic_0107606742_p118402467212"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row047714490517"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1874131821217"><a name="zh-cn_topic_0107606742_p1874131821217"></a><a name="zh-cn_topic_0107606742_p1874131821217"></a>net_bitRecv</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923191120526"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923191120526"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p12923191120526"></a>（Agent）出网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p692381185210"></a>该指标用于统计测量对象网卡每秒接收的比特数。</p>
<p id="zh-cn_topic_0107606742_p109105171214"><a name="zh-cn_topic_0107606742_p109105171214"></a><a name="zh-cn_topic_0107606742_p109105171214"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p1857448154112"><a name="zh-cn_topic_0107606742_p1857448154112"></a><a name="zh-cn_topic_0107606742_p1857448154112"></a>单位：bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1692341113526"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p9923811185213"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p369617410228"><a name="zh-cn_topic_0107606742_p369617410228"></a><a name="zh-cn_topic_0107606742_p369617410228"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row54771049175118"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p8741151811211"><a name="zh-cn_topic_0107606742_p8741151811211"></a><a name="zh-cn_topic_0107606742_p8741151811211"></a>net_packetRecv</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923201110528"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923201110528"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2923201110528"></a>（Agent）网卡包接收速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p10923171135217"></a>该指标用于统计测量对象网卡每秒接收的数据包数。</p>
<p id="zh-cn_topic_0107606742_p1653912017215"><a name="zh-cn_topic_0107606742_p1653912017215"></a><a name="zh-cn_topic_0107606742_p1653912017215"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p34321561417"><a name="zh-cn_topic_0107606742_p34321561417"></a><a name="zh-cn_topic_0107606742_p34321561417"></a>单位：Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199231611135216"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199231611135216"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p199231611135216"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139231011205218"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139231011205218"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p139231011205218"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p6504155142212"><a name="zh-cn_topic_0107606742_p6504155142212"></a><a name="zh-cn_topic_0107606742_p6504155142212"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row16477164995117"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p47411218151211"><a name="zh-cn_topic_0107606742_p47411218151211"></a><a name="zh-cn_topic_0107606742_p47411218151211"></a>net_packetSent</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p792311110528"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p792311110528"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p792311110528"></a>（Agent）网卡包发送速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16923151110524"></a>该指标用于统计测量对象网卡每秒发送的数据包数。</p>
<p id="zh-cn_topic_0107606742_p1557942352114"><a name="zh-cn_topic_0107606742_p1557942352114"></a><a name="zh-cn_topic_0107606742_p1557942352114"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p673911116424"><a name="zh-cn_topic_0107606742_p673911116424"></a><a name="zh-cn_topic_0107606742_p673911116424"></a>单位：Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p39231511205216"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p13923161165215"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p421119642214"><a name="zh-cn_topic_0107606742_p421119642214"></a><a name="zh-cn_topic_0107606742_p421119642214"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row154221167209"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p274110186120"><a name="zh-cn_topic_0107606742_p274110186120"></a><a name="zh-cn_topic_0107606742_p274110186120"></a>net_errin</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p73131027132512"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p73131027132512"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p73131027132512"></a>（Agent）接收误包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p9313172719250"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p9313172719250"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p9313172719250"></a>该指标用于统计测量对象网卡每秒接收的错误数据包数量占所接收的数据包的比率。</p>
<p id="zh-cn_topic_0107606742_p1210213716411"><a name="zh-cn_topic_0107606742_p1210213716411"></a><a name="zh-cn_topic_0107606742_p1210213716411"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p3369579281"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p3369579281"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p3369579281"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p766584013202"><a name="zh-cn_topic_0107606742_p766584013202"></a><a name="zh-cn_topic_0107606742_p766584013202"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p126449812219"><a name="zh-cn_topic_0107606742_p126449812219"></a><a name="zh-cn_topic_0107606742_p126449812219"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row17243722162020"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1274121811120"><a name="zh-cn_topic_0107606742_p1274121811120"></a><a name="zh-cn_topic_0107606742_p1274121811120"></a>net_errout</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p155501224102512"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p155501224102512"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p155501224102512"></a>（Agent）发送误包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p125501924112513"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p125501924112513"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p125501924112513"></a>该指标用于统计测量对象网卡每秒发送的错误数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0107606742_p736292692115"><a name="zh-cn_topic_0107606742_p736292692115"></a><a name="zh-cn_topic_0107606742_p736292692115"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p6703191284110"><a name="zh-cn_topic_0107606742_p6703191284110"></a><a name="zh-cn_topic_0107606742_p6703191284110"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p204221754161213"><a name="zh-cn_topic_0107606742_p204221754161213"></a><a name="zh-cn_topic_0107606742_p204221754161213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p166741440192011"><a name="zh-cn_topic_0107606742_p166741440192011"></a><a name="zh-cn_topic_0107606742_p166741440192011"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p8344996224"><a name="zh-cn_topic_0107606742_p8344996224"></a><a name="zh-cn_topic_0107606742_p8344996224"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1558171912206"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p10741518121212"><a name="zh-cn_topic_0107606742_p10741518121212"></a><a name="zh-cn_topic_0107606742_p10741518121212"></a>net_dropin</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1216444673017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1216444673017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p1216444673017"></a>（Agent）接收丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p216474618302"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p216474618302"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p216474618302"></a>该指标用于统计测量对象网卡每秒接收并已丢弃的数据包数量占所接收的数据包的比率。</p>
<p id="zh-cn_topic_0107606742_p146971928122113"><a name="zh-cn_topic_0107606742_p146971928122113"></a><a name="zh-cn_topic_0107606742_p146971928122113"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p180611817419"><a name="zh-cn_topic_0107606742_p180611817419"></a><a name="zh-cn_topic_0107606742_p180611817419"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p10992115701213"><a name="zh-cn_topic_0107606742_p10992115701213"></a><a name="zh-cn_topic_0107606742_p10992115701213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p1968334016208"><a name="zh-cn_topic_0107606742_p1968334016208"></a><a name="zh-cn_topic_0107606742_p1968334016208"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1180051082217"><a name="zh-cn_topic_0107606742_p1180051082217"></a><a name="zh-cn_topic_0107606742_p1180051082217"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1727210289208"><td class="cellrowborder" valign="top" width="10.35%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p074121820124"><a name="zh-cn_topic_0107606742_p074121820124"></a><a name="zh-cn_topic_0107606742_p074121820124"></a>net_dropout</p>
</td>
<td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p16466149153017"><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p16466149153017"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0083516942_p16466149153017"></a>（Agent）发送丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.69%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p3266135619131"><a name="zh-cn_topic_0107606742_p3266135619131"></a><a name="zh-cn_topic_0107606742_p3266135619131"></a>该指标用于统计测量对象网卡每秒发送并已丢弃的数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0107606742_p9433215219"><a name="zh-cn_topic_0107606742_p9433215219"></a><a name="zh-cn_topic_0107606742_p9433215219"></a>通过计算采集周期内“/proc/net/dev”文件中的变化得出。</p>
<p id="zh-cn_topic_0107606742_p38071223104116"><a name="zh-cn_topic_0107606742_p38071223104116"></a><a name="zh-cn_topic_0107606742_p38071223104116"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="9.77%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p139272012134"><a name="zh-cn_topic_0107606742_p139272012134"></a><a name="zh-cn_topic_0107606742_p139272012134"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p769020403202"><a name="zh-cn_topic_0107606742_p769020403202"></a><a name="zh-cn_topic_0107606742_p769020403202"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.36%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p15712511122210"><a name="zh-cn_topic_0107606742_p15712511122210"></a><a name="zh-cn_topic_0107606742_p15712511122210"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 8**  软RAID相关监控指标说明

<a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_table17716191314220"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row17730171316215"><th class="cellrowborder" valign="top" width="10.238976102389762%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p1771151717148"><a name="zh-cn_topic_0107606742_p1771151717148"></a><a name="zh-cn_topic_0107606742_p1771151717148"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.638236176382364%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p473016131024"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p473016131024"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p473016131024"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.44655534446555%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p67468133219"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p67468133219"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p67468133219"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="10.218978102189782%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p27466130211"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p27466130211"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p27466130211"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.38886111388861%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11746121317219"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11746121317219"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p11746121317219"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.068393160683932%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p878002110237"><a name="zh-cn_topic_0107606742_p878002110237"></a><a name="zh-cn_topic_0107606742_p878002110237"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_row12507192717120"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p10711151761417"><a name="zh-cn_topic_0107606742_p10711151761417"></a><a name="zh-cn_topic_0107606742_p10711151761417"></a>md1_status_device:1</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2026419151240"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2026419151240"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p2026419151240"></a>（Agent）软RAID状态</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p192646151149"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p192646151149"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p192646151149"></a>该指标用于统计测量对象软RAID设备的状态，RAID异常情况下值为0。</p>
<p id="zh-cn_topic_0107606742_p13507102713125"><a name="zh-cn_topic_0107606742_p13507102713125"></a><a name="zh-cn_topic_0107606742_p13507102713125"></a>通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行<strong id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1446918321628"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1446918321628"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_b1446918321628"></a>mdadm -D /dev/</strong><em id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_i12685835421"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_i12685835421"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_i12685835421"></a>md0</em>（RAID名称）得出。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p152644157411"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p152644157411"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p152644157411"></a>0，1</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1326412151414"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1326412151414"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1326412151414"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p2078062110238"><a name="zh-cn_topic_0107606742_p2078062110238"></a><a name="zh-cn_topic_0107606742_p2078062110238"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row1974611311213"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p071151791412"><a name="zh-cn_topic_0107606742_p071151791412"></a><a name="zh-cn_topic_0107606742_p071151791412"></a>md1_active_device:2</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3746613921"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3746613921"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p3746613921"></a>（Agent）软RAID活跃设备数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1026318374420"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1026318374420"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1026318374420"></a>该指标用于统计测量对象软RAID设备的活跃盘数，RAID异常情况下值为-1。</p>
<p id="zh-cn_topic_0107606742_p3737205582216"><a name="zh-cn_topic_0107606742_p3737205582216"></a><a name="zh-cn_topic_0107606742_p3737205582216"></a>通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行<strong id="zh-cn_topic_0107606742_b57371655182216"><a name="zh-cn_topic_0107606742_b57371655182216"></a><a name="zh-cn_topic_0107606742_b57371655182216"></a>mdadm -D /dev/</strong><em id="zh-cn_topic_0107606742_i07371655112218"><a name="zh-cn_topic_0107606742_i07371655112218"></a><a name="zh-cn_topic_0107606742_i07371655112218"></a>md0</em>（RAID名称）得出。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16746171311213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16746171311213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p16746171311213"></a>≥0，-1</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1774612139213"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1774612139213"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1774612139213"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p96863882320"><a name="zh-cn_topic_0107606742_p96863882320"></a><a name="zh-cn_topic_0107606742_p96863882320"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row17762181311219"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p167111817201410"><a name="zh-cn_topic_0107606742_p167111817201410"></a><a name="zh-cn_topic_0107606742_p167111817201410"></a>md1_working_device:2</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p117629138220"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p117629138220"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p117629138220"></a>（Agent）软RAID工作设备数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p181395565412"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p181395565412"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p181395565412"></a>该指标用于统计测量对象软RAID设备的工作设备数，RAID异常情况下值为-1。</p>
<p id="zh-cn_topic_0107606742_p1557259122211"><a name="zh-cn_topic_0107606742_p1557259122211"></a><a name="zh-cn_topic_0107606742_p1557259122211"></a>通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行<strong id="zh-cn_topic_0107606742_b1857135932216"><a name="zh-cn_topic_0107606742_b1857135932216"></a><a name="zh-cn_topic_0107606742_b1857135932216"></a>mdadm -D /dev/</strong><em id="zh-cn_topic_0107606742_i15710590221"><a name="zh-cn_topic_0107606742_i15710590221"></a><a name="zh-cn_topic_0107606742_i15710590221"></a>md0</em>（RAID名称）得出。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p576220132210"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p576220132210"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p576220132210"></a>≥0，-1</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p127625131328"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p127625131328"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p127625131328"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p9345163917235"><a name="zh-cn_topic_0107606742_p9345163917235"></a><a name="zh-cn_topic_0107606742_p9345163917235"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row1762171316214"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p871131721415"><a name="zh-cn_topic_0107606742_p871131721415"></a><a name="zh-cn_topic_0107606742_p871131721415"></a>md1_failed_device:0</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4762131319217"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4762131319217"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p4762131319217"></a>（Agent）软RAID失败设备数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p79208714518"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p79208714518"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p79208714518"></a>该指标用于统计测量对象软RAID设备的失败设备数，RAID异常情况下值为-1。</p>
<p id="zh-cn_topic_0107606742_p12396252320"><a name="zh-cn_topic_0107606742_p12396252320"></a><a name="zh-cn_topic_0107606742_p12396252320"></a>通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行<strong id="zh-cn_topic_0107606742_b423972172314"><a name="zh-cn_topic_0107606742_b423972172314"></a><a name="zh-cn_topic_0107606742_b423972172314"></a>mdadm -D /dev/</strong><em id="zh-cn_topic_0107606742_i1123910292316"><a name="zh-cn_topic_0107606742_i1123910292316"></a><a name="zh-cn_topic_0107606742_i1123910292316"></a>md0</em>（RAID名称）得出。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p37787131220"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p37787131220"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p37787131220"></a>≥0，-1</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p977820136211"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p977820136211"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p977820136211"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p2549240132316"><a name="zh-cn_topic_0107606742_p2549240132316"></a><a name="zh-cn_topic_0107606742_p2549240132316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_row177861317214"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1171115177144"><a name="zh-cn_topic_0107606742_p1171115177144"></a><a name="zh-cn_topic_0107606742_p1171115177144"></a>md1_spare_device:0</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p187785134219"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p187785134219"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p187785134219"></a>（Agent）软RAID备用设备数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p146215199519"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p146215199519"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p146215199519"></a>该指标用于统计测量对象软RAID设备的备用设备数，RAID异常情况下值为-1。</p>
<p id="zh-cn_topic_0107606742_p106571655236"><a name="zh-cn_topic_0107606742_p106571655236"></a><a name="zh-cn_topic_0107606742_p106571655236"></a>通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行<strong id="zh-cn_topic_0107606742_b66587542312"><a name="zh-cn_topic_0107606742_b66587542312"></a><a name="zh-cn_topic_0107606742_b66587542312"></a>mdadm -D /dev/</strong><em id="zh-cn_topic_0107606742_i46581151233"><a name="zh-cn_topic_0107606742_i46581151233"></a><a name="zh-cn_topic_0107606742_i46581151233"></a>md0</em>（RAID名称）得出。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1277861311219"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1277861311219"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p1277861311219"></a>≥0，-1</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p5778201316214"><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p5778201316214"></a><a name="zh-cn_topic_0107606742_zh-cn_topic_0104704449_p5778201316214"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p125754212238"><a name="zh-cn_topic_0107606742_p125754212238"></a><a name="zh-cn_topic_0107606742_p125754212238"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 9**  进程相关监控指标说明

<a name="zh-cn_topic_0107606742_table2080718432177"></a>
<table><thead align="left"><tr id="zh-cn_topic_0107606742_row1808184381716"><th class="cellrowborder" valign="top" width="10.238976102389762%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0107606742_p1680874351710"><a name="zh-cn_topic_0107606742_p1680874351710"></a><a name="zh-cn_topic_0107606742_p1680874351710"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="17.638236176382364%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0107606742_p1808243101711"><a name="zh-cn_topic_0107606742_p1808243101711"></a><a name="zh-cn_topic_0107606742_p1808243101711"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.44655534446555%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0107606742_p48085438172"><a name="zh-cn_topic_0107606742_p48085438172"></a><a name="zh-cn_topic_0107606742_p48085438172"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="10.218978102189782%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0107606742_p11808194361711"><a name="zh-cn_topic_0107606742_p11808194361711"></a><a name="zh-cn_topic_0107606742_p11808194361711"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.38886111388861%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0107606742_p1880884311713"><a name="zh-cn_topic_0107606742_p1880884311713"></a><a name="zh-cn_topic_0107606742_p1880884311713"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.068393160683932%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0107606742_p1580812439175"><a name="zh-cn_topic_0107606742_p1580812439175"></a><a name="zh-cn_topic_0107606742_p1580812439175"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0107606742_row680884312173"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p7809443101715"><a name="zh-cn_topic_0107606742_p7809443101715"></a><a name="zh-cn_topic_0107606742_p7809443101715"></a>proc_pHashId_cpu</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p19146121813512"><a name="zh-cn_topic_0107606742_p19146121813512"></a><a name="zh-cn_topic_0107606742_p19146121813512"></a>进程CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p0809164316178"><a name="zh-cn_topic_0107606742_p0809164316178"></a><a name="zh-cn_topic_0107606742_p0809164316178"></a>进程消耗的CPU百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0107606742_p158099432171"><a name="zh-cn_topic_0107606742_p158099432171"></a><a name="zh-cn_topic_0107606742_p158099432171"></a>通过计算/proc/pid/stat的变化得出。</p>
<p id="zh-cn_topic_0107606742_p9815165917223"><a name="zh-cn_topic_0107606742_p9815165917223"></a><a name="zh-cn_topic_0107606742_p9815165917223"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p9815231124"><a name="zh-cn_topic_0107606742_p9815231124"></a><a name="zh-cn_topic_0107606742_p9815231124"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p48091143151719"><a name="zh-cn_topic_0107606742_p48091143151719"></a><a name="zh-cn_topic_0107606742_p48091143151719"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p5809154351713"><a name="zh-cn_topic_0107606742_p5809154351713"></a><a name="zh-cn_topic_0107606742_p5809154351713"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row680934313172"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p1280964361711"><a name="zh-cn_topic_0107606742_p1280964361711"></a><a name="zh-cn_topic_0107606742_p1280964361711"></a>proc_pHashId_mem</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p8724192617519"><a name="zh-cn_topic_0107606742_p8724192617519"></a><a name="zh-cn_topic_0107606742_p8724192617519"></a>进程内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p282220584518"><a name="zh-cn_topic_0107606742_p282220584518"></a><a name="zh-cn_topic_0107606742_p282220584518"></a>进程消耗的内存百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0107606742_p811262715197"><a name="zh-cn_topic_0107606742_p811262715197"></a><a name="zh-cn_topic_0107606742_p811262715197"></a>计算方式：RSS*PAGESIZE/MemTotal</p>
<a name="zh-cn_topic_0107606742_ul841435982311"></a><a name="zh-cn_topic_0107606742_ul841435982311"></a><ul id="zh-cn_topic_0107606742_ul841435982311"><li>RSS：通过获取/proc/pid/statm第二列得到</li><li>PAGESIZE：通过命令getconf PAGESIZE获取</li><li>MemTotal：通过/proc/meminfo获取</li></ul>
<p id="zh-cn_topic_0107606742_p571147113714"><a name="zh-cn_topic_0107606742_p571147113714"></a><a name="zh-cn_topic_0107606742_p571147113714"></a>单位：百分比</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p12665715182320"><a name="zh-cn_topic_0107606742_p12665715182320"></a><a name="zh-cn_topic_0107606742_p12665715182320"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p16810134301710"><a name="zh-cn_topic_0107606742_p16810134301710"></a><a name="zh-cn_topic_0107606742_p16810134301710"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p281064311177"><a name="zh-cn_topic_0107606742_p281064311177"></a><a name="zh-cn_topic_0107606742_p281064311177"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row58100431174"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p17810144391711"><a name="zh-cn_topic_0107606742_p17810144391711"></a><a name="zh-cn_topic_0107606742_p17810144391711"></a>proc_pHashId_file</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p135156347514"><a name="zh-cn_topic_0107606742_p135156347514"></a><a name="zh-cn_topic_0107606742_p135156347514"></a>进程打开文件数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p881044311171"><a name="zh-cn_topic_0107606742_p881044311171"></a><a name="zh-cn_topic_0107606742_p881044311171"></a>进程打开文件数，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0107606742_p178102432172"><a name="zh-cn_topic_0107606742_p178102432172"></a><a name="zh-cn_topic_0107606742_p178102432172"></a>通过执行<strong id="zh-cn_topic_0107606742_b331910275242"><a name="zh-cn_topic_0107606742_b331910275242"></a><a name="zh-cn_topic_0107606742_b331910275242"></a>ls -l /proc/pid/fd</strong>可以查看数量。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p381011430177"><a name="zh-cn_topic_0107606742_p381011430177"></a><a name="zh-cn_topic_0107606742_p381011430177"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p17810114318177"><a name="zh-cn_topic_0107606742_p17810114318177"></a><a name="zh-cn_topic_0107606742_p17810114318177"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p11810743171718"><a name="zh-cn_topic_0107606742_p11810743171718"></a><a name="zh-cn_topic_0107606742_p11810743171718"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row18810164316173"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p18111432178"><a name="zh-cn_topic_0107606742_p18111432178"></a><a name="zh-cn_topic_0107606742_p18111432178"></a>proc_running_count</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p6740185510386"><a name="zh-cn_topic_0107606742_p6740185510386"></a><a name="zh-cn_topic_0107606742_p6740185510386"></a>（Agent）运行中进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p072111023915"><a name="zh-cn_topic_0107606742_p072111023915"></a><a name="zh-cn_topic_0107606742_p072111023915"></a>该指标用于统计测量对象处于运行状态的进程数。</p>
<p id="zh-cn_topic_0107606742_p133158173255"><a name="zh-cn_topic_0107606742_p133158173255"></a><a name="zh-cn_topic_0107606742_p133158173255"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p17811204315170"><a name="zh-cn_topic_0107606742_p17811204315170"></a><a name="zh-cn_topic_0107606742_p17811204315170"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p1281110439171"><a name="zh-cn_topic_0107606742_p1281110439171"></a><a name="zh-cn_topic_0107606742_p1281110439171"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p881124351715"><a name="zh-cn_topic_0107606742_p881124351715"></a><a name="zh-cn_topic_0107606742_p881124351715"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row4811204321713"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p381144301715"><a name="zh-cn_topic_0107606742_p381144301715"></a><a name="zh-cn_topic_0107606742_p381144301715"></a>proc_idle_count</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p3740125514380"><a name="zh-cn_topic_0107606742_p3740125514380"></a><a name="zh-cn_topic_0107606742_p3740125514380"></a>（Agent）空闲进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p872120113911"><a name="zh-cn_topic_0107606742_p872120113911"></a><a name="zh-cn_topic_0107606742_p872120113911"></a>该指标用于统计测量对象处于空闲状态的进程数。</p>
<p id="zh-cn_topic_0107606742_p37931527132514"><a name="zh-cn_topic_0107606742_p37931527132514"></a><a name="zh-cn_topic_0107606742_p37931527132514"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p15812114314179"><a name="zh-cn_topic_0107606742_p15812114314179"></a><a name="zh-cn_topic_0107606742_p15812114314179"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p68121243181718"><a name="zh-cn_topic_0107606742_p68121243181718"></a><a name="zh-cn_topic_0107606742_p68121243181718"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p28121143191715"><a name="zh-cn_topic_0107606742_p28121143191715"></a><a name="zh-cn_topic_0107606742_p28121143191715"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row13908141871814"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p190912180182"><a name="zh-cn_topic_0107606742_p190912180182"></a><a name="zh-cn_topic_0107606742_p190912180182"></a>proc_zombie_count</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p274010553387"><a name="zh-cn_topic_0107606742_p274010553387"></a><a name="zh-cn_topic_0107606742_p274010553387"></a>（Agent）僵死进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p07216015392"><a name="zh-cn_topic_0107606742_p07216015392"></a><a name="zh-cn_topic_0107606742_p07216015392"></a>该指标用于统计测量对象处于僵死状态的进程数。</p>
<p id="zh-cn_topic_0107606742_p1529093016253"><a name="zh-cn_topic_0107606742_p1529093016253"></a><a name="zh-cn_topic_0107606742_p1529093016253"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p1590911181181"><a name="zh-cn_topic_0107606742_p1590911181181"></a><a name="zh-cn_topic_0107606742_p1590911181181"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p16910018161819"><a name="zh-cn_topic_0107606742_p16910018161819"></a><a name="zh-cn_topic_0107606742_p16910018161819"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p8910101810189"><a name="zh-cn_topic_0107606742_p8910101810189"></a><a name="zh-cn_topic_0107606742_p8910101810189"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row1191021811815"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p5910181812187"><a name="zh-cn_topic_0107606742_p5910181812187"></a><a name="zh-cn_topic_0107606742_p5910181812187"></a>proc_blocked_count</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p2740755103817"><a name="zh-cn_topic_0107606742_p2740755103817"></a><a name="zh-cn_topic_0107606742_p2740755103817"></a>（Agent）阻塞进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p1972120103917"><a name="zh-cn_topic_0107606742_p1972120103917"></a><a name="zh-cn_topic_0107606742_p1972120103917"></a>该指标用于统计测量对象被阻塞的进程数。</p>
<p id="zh-cn_topic_0107606742_p1663019323257"><a name="zh-cn_topic_0107606742_p1663019323257"></a><a name="zh-cn_topic_0107606742_p1663019323257"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p2910318141818"><a name="zh-cn_topic_0107606742_p2910318141818"></a><a name="zh-cn_topic_0107606742_p2910318141818"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p0910121851811"><a name="zh-cn_topic_0107606742_p0910121851811"></a><a name="zh-cn_topic_0107606742_p0910121851811"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p1491091811812"><a name="zh-cn_topic_0107606742_p1491091811812"></a><a name="zh-cn_topic_0107606742_p1491091811812"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row18864722151810"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p178641722101818"><a name="zh-cn_topic_0107606742_p178641722101818"></a><a name="zh-cn_topic_0107606742_p178641722101818"></a>proc_sleeping_count</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p1741105513811"><a name="zh-cn_topic_0107606742_p1741105513811"></a><a name="zh-cn_topic_0107606742_p1741105513811"></a>（Agent）睡眠进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p17215017397"><a name="zh-cn_topic_0107606742_p17215017397"></a><a name="zh-cn_topic_0107606742_p17215017397"></a>该指标用于统计测量对象处于睡眠状态的进程数。</p>
<p id="zh-cn_topic_0107606742_p0740173432513"><a name="zh-cn_topic_0107606742_p0740173432513"></a><a name="zh-cn_topic_0107606742_p0740173432513"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p2864182231811"><a name="zh-cn_topic_0107606742_p2864182231811"></a><a name="zh-cn_topic_0107606742_p2864182231811"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p686482214181"><a name="zh-cn_topic_0107606742_p686482214181"></a><a name="zh-cn_topic_0107606742_p686482214181"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p9864122141813"><a name="zh-cn_topic_0107606742_p9864122141813"></a><a name="zh-cn_topic_0107606742_p9864122141813"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0107606742_row2864622201813"><td class="cellrowborder" valign="top" width="10.238976102389762%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0107606742_p198644223181"><a name="zh-cn_topic_0107606742_p198644223181"></a><a name="zh-cn_topic_0107606742_p198644223181"></a>proc_total_coun</p>
</td>
<td class="cellrowborder" valign="top" width="17.638236176382364%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0107606742_p137416556389"><a name="zh-cn_topic_0107606742_p137416556389"></a><a name="zh-cn_topic_0107606742_p137416556389"></a>（Agent）系统进程数</p>
</td>
<td class="cellrowborder" valign="top" width="34.44655534446555%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0107606742_p157213019397"><a name="zh-cn_topic_0107606742_p157213019397"></a><a name="zh-cn_topic_0107606742_p157213019397"></a>该指标用于统计测量对象的总进程数。</p>
<p id="zh-cn_topic_0107606742_p15923163612259"><a name="zh-cn_topic_0107606742_p15923163612259"></a><a name="zh-cn_topic_0107606742_p15923163612259"></a>通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。</p>
</td>
<td class="cellrowborder" valign="top" width="10.218978102189782%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0107606742_p13864132214189"><a name="zh-cn_topic_0107606742_p13864132214189"></a><a name="zh-cn_topic_0107606742_p13864132214189"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="11.38886111388861%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0107606742_p1586482241814"><a name="zh-cn_topic_0107606742_p1586482241814"></a><a name="zh-cn_topic_0107606742_p1586482241814"></a>裸金属服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.068393160683932%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0107606742_p186472217187"><a name="zh-cn_topic_0107606742_p186472217187"></a><a name="zh-cn_topic_0107606742_p186472217187"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

