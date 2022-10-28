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

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|cpu_usage|（Agent）CPU使用率|该指标用于统计测量对象当前CPU使用率。通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。用户可以通过**top**命令查看“%Cpu(s)”值。单位：百分比|0-100%|裸金属服务器|1分钟|
|load_average5|（Agent）5分钟平均负载|该指标用于统计测量对象在过去5分钟的CPU平均负载。通过“/proc/loadavg”文件中load5/逻辑CPU个数得到。用户可以通过**top**命令查看“load5”值。|≥ 0|裸金属服务器|1分钟|
|mem_usedPercent|（Agent）内存使用率|该指标用于统计测量对象的内存使用率。通过“/proc/meminfo”文件获取。计算公式：(MemTotal-MemAvailable)/MemTotal。单位：百分比|0-100%|裸金属服务器|1分钟|
|mountPointPrefix_disk_free|（Agent）磁盘剩余存储量|该指标用于统计测量对象磁盘的剩余存储空间。执行**df -h**命令，查看Avail列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mountPointPrefix_disk_usedPercent|（Agent）磁盘使用率|该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为：磁盘已用存储量/磁盘存储总量。通过计算Used/Size得出。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|
|mountPointPrefix_disk_ioUtils 和volumePrefix_disk_ioUtils|（Agent）磁盘I/O使用率|该指标用于统计测量对象磁盘I/O使用率。通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|
|mountPointPrefix_disk_inodesUsedPercent|（Agent）inode已使用占比|该指标用于统计测量对象当前磁盘已使用的inode占比。执行**df -i**命令，查看IUse%列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|
|net_bitRecv|（Agent）入网带宽|该指标用于统计测量对象网卡每秒接收的比特数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：bit/s|≥ 0 bit/s|裸金属服务器|1分钟|
|net_bitSent|（Agent）出网带宽|该指标用于统计测量对象网卡每秒发送的比特数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：bit/s|≥ 0 bit/s|裸金属服务器|1分钟|
|net_packetRecv|（Agent）网卡包接收速率|该指标用于统计测量对象网卡每秒接收的数据包数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：Counts/s|≥ 0 Counts/s|裸金属服务器|1分钟|
|net_packetSent|（Agent）网卡包发送速率|该指标用于统计测量对象网卡每秒发送的数据包数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：Counts/s|≥ 0 Counts/s|裸金属服务器|1分钟|
|net_tcp_total|（Agent）所有状态的TCP连接数总和|该指标用于统计测量对象网卡所有状态的TCP连接数总和。|≥0|裸金属服务器|1分钟|
|net_tcp_established|（Agent）处于ESTABLISHED状态的TCP连接数量|该指标用于统计测量对象网卡处于ESTABLISHED状态的TCP连接数量。|≥0|裸金属服务器|1分钟|


