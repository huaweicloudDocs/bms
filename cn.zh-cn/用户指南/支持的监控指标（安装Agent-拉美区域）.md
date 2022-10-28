# 支持的监控指标（安装Agent，拉美区域）<a name="bms_01_0053"></a>

## 功能说明<a name="zh-cn_topic_0107606742_section1233112278019"></a>

本节定义了裸金属服务器上报云监控服务的监控指标的命名空间，监控指标列表和维度定义，用户可以通过云监控服务控制台或API接口来检索裸金属服务器产生的监控指标和告警信息。

>![](public_sys-resources/icon-note.gif) **说明：** 
>安装Agent后，您便可以查看裸金属服务器的操作系统监控指标。指标采集周期是1分钟。
>““华东-上海一”、“华东-上海二”、“华北-北京一”、“华北-北京四”、“华南-广州”、“华南-深圳”、“西南-贵阳一”、“中国-香港”、“亚太-曼谷”、“亚太-新加坡”、“非洲-约翰内斯堡”区域主机监控Agent采用最新版本的Agent，监控指标更为简洁，详情请参见[支持的监控指标（安装Agent，简洁版）](支持的监控指标（安装Agent-简洁版）.md)。

## 命名空间<a name="zh-cn_topic_0107606742_section3231114620112"></a>

SERVICE.BMS

## 监控指标<a name="zh-cn_topic_0107606742_section738316451823"></a>

裸金属服务器（操作系统监控）支持的监控指标有：CPU相关监控指标（[表1](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1274172674913)）、CPU负载类相关监控指标（[表2](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table341241110501)）、内存相关监控指标（[表3](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table844220384507)）、磁盘相关监控指标（[表4](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table1067218184514)）、磁盘I/O类（[表5](#zh-cn_topic_0107606742_table1559955415558)）、文件系统类（[表6](#zh-cn_topic_0107606742_table296913551343)）、网卡类（[表7](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table19476249105111)）、软RAID相关监控指标（[表8](#zh-cn_topic_0107606742_zh-cn_topic_0104704449_table17716191314220)）和进程相关监控指标（[表9](#zh-cn_topic_0107606742_table2080718432177)）。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果要监控软RAID相关指标，Agent版本必须为1.0.5及以上。
>Windows系统的裸金属服务器暂不支持监控。

**表 1**  CPU相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|cpu_usage_idle|（Agent）CPU空闲时间占比|该指标用于统计测量对象当前CPU空闲时间占比。通过计算采集周期内“/proc/stat”文件中的变化得出CPU空闲时间占比。用户可以通过**top**命令查看“%Cpu(s) id”值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_other|（Agent）其他CPU使用率|该指标用于统计测量对象其他占用CPU使用率。计算公式：1 - 空闲CPU使用率（%） - 内核空间CPU使用率 - 用户空间CPU使用率。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_system|（Agent）内核空间CPU使用率|该指标用于统计测量对象当前内核空间占用CPU使用率。通过计算采集周期内“/proc/stat”文件中的变化得出内核空间CPU使用率。用户可以通过**top**命令查看“%Cpu(s) sy”值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_user|（Agent）用户空间CPU使用率|该指标用于统计测量对象当前用户空间占用CPU使用率。通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。用户可以通过**top**命令查看“%Cpu(s) us”值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage|（Agent）CPU使用率|该指标用于统计测量对象当前CPU使用率。通过计算采集周期内“/proc/stat”中的变化得出用户空间CPU使用率。用户可以通过**top**命令查看“%Cpu(s)”值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_nice|（Agent）Nice进程CPU使用率|该指标用于统计测量对象当前Nice进程CPU使用率。通过计算采集周期内/proc/stat中的变化得出Nice进程CPU使用率。用户可以通过**top**命令查看 %Cpu(s) ni值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_iowait|（Agent）iowait状态占比|该指标用于统计测量对象当前iowait状态占用CPU的比率。通过计算采集周期内/proc/stat中的变化得出iowait状态占比。用户可以通过**top**命令查看 %Cpu(s) wa值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_irq|（Agent）CPU中断时间占比|该指标用于统计测量对象当前CPU处理中断用时占用CPU时间的比率，以百分比为单位。通过计算采集周期内/proc/stat中的变化得出CPU中断时间占比。用户可以通过**top**命令查看 %Cpu(s) hi值。单位：百分比|0-100%|裸金属服务器|1分钟|
|cpu_usage_softirq|（Agent）CPU软中断时间占比|该指标用于统计测量对象当前CPU处理软中断时间占用CPU时间的比率。通过计算采集周期内/proc/stat中的变化得出CPU软中断时间占比。用户可以通过**top**命令查看 %Cpu(s) si值。单位：百分比|0-100%|裸金属服务器|1分钟|


**表 2**  CPU负载指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|load_average1|（Agent）1分钟平均负载|该指标用于统计测量对象在过去1分钟的CPU平均负载。通过“/proc/loadavg”文件中load1/逻辑CPU个数得到。用户可以通过**top**命令查看“load1”值。|≥ 0|裸金属服务器|1分钟|
|load_average5|（Agent）5分钟平均负载|该指标用于统计测量对象在过去5分钟的CPU平均负载。通过“/proc/loadavg”文件中load5/逻辑CPU个数得到。用户可以通过**top**命令查看“load5”值。|≥ 0|裸金属服务器|1分钟|
|load_average15|（Agent）15分钟平均负载|该指标用于统计测量对象在过去15分钟的CPU平均负载。通过“/proc/loadavg”中load15/逻辑CPU个数得到。用户可以通过**top**命令查看“load15”值。|≥ 0|裸金属服务器|1分钟|


**表 3**  内存相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|mem_available|（Agent）可用内存|该指标用于统计测量对象的可用内存。通过“/proc/meminfo”文件得到MemAvailable。若“/proc/meminfo”中不显示MemAvailable，则MemAvailable=MemFree+Buffers+Cached。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mem_usedPercent|（Agent）内存使用率|该指标用于统计测量对象的内存使用率。通过“/proc/meminfo”文件获取。计算公式：(MemTotal-MemAvailable)/MemTotal。单位：百分比|0-100%|裸金属服务器|1分钟|
|mem_free|（Agent）空闲内存量|该指标用于统计测量对象的空闲内存量。通过/proc/meminfo获取。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mem_buffers|（Agent）Buffers占用量|该指标用于统计测量对象的Buffers内存量。通过/proc/meminfo获取。用户可以通过**top**命令查看 KiB Mem:buffers值。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mem_cached|（Agent）Cache占用量|该指标用于统计测量对象Cache内存量。通过/proc/meminfo获取。用户可以通过**top**命令查看 KiB Swap:cached Mem值。单位：GB|≥ 0 GB|裸金属服务器|1分钟|


**表 4**  磁盘相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|mountPointPrefix_disk_free|（Agent）磁盘剩余存储量|该指标用于统计测量对象磁盘的剩余存储空间。执行**df -h**命令，查看Avail列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mountPointPrefix_disk_total|（Agent）磁盘存储总量|该指标用于统计测量对象磁盘存储总量。执行**df -h**命令，查看Size列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mountPointPrefix_disk_used|（Agent）磁盘已用存储量|该指标用于统计测量对象磁盘的已用存储空间。执行**df -h**命令，查看Used列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：GB|≥ 0 GB|裸金属服务器|1分钟|
|mountPointPrefix_disk_usedPercent|（Agent）磁盘使用率|该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为：磁盘已用存储量/磁盘存储总量。通过计算Used/Size得出。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|


**表 5**  磁盘I/O相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|mountPointPrefix_disk_agt_read_bytes_rate|（Agent）磁盘读速率|该指标用于统计每秒从测量对象磁盘读出的数据量。通过计算采集周期内“/proc/diskstats”文件中对应设备第六列数据的变化得出磁盘读速率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：byte/s|≥ 0 byte/s|裸金属服务器|1分钟|
|mountPointPrefix_disk_agt_read_requests_rate|（Agent）磁盘读操作速率|该指标用于统计每秒从测量对象磁盘读取数据的请求次数。通过计算采集周期内“/proc/diskstats”文件中对应设备第四列数据的变化得出磁盘读操作速率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：请求/秒|≥ 0 请求/秒|裸金属服务器|1分钟|
|mountPointPrefix_disk_agt_write_bytes_rate|（Agent）磁盘写速率|该指标用于统计每秒写到测量对象磁盘的数据量。通过计算采集周期内“/proc/diskstats”文件中对应设备第十列数据的变化得出磁盘写速率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：byte/s|≥ 0 byte/s|裸金属服务器|1分钟|
|mountPointPrefix_disk_agt_write_requests_rate|（Agent）磁盘写操作速率|该指标用于统计每秒向测量对象磁盘写数据的请求次数。通过计算采集周期内“/proc/diskstats”文件中对应设备第八列数据的变化得出磁盘写操作速率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：请求/秒|≥ 0 请求/秒|裸金属服务器|1分钟|
|disk_readTime|（Agent）读操作平均耗时|该指标用于统计测量对象磁盘读操作平均耗时。通过计算采集周期内/proc/diskstats中对应设备第七列数据的变化得出磁盘读操作平均耗时。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：ms/Count|≥ 0 ms/Count|裸金属服务器|1分钟|
|disk_writeTime|（Agent）写操作平均耗时|该指标用于统计测量对象磁盘写操作平均耗时。通过计算采集周期内/proc/diskstats中对应设备第十一列数据的变化得出磁盘写操作平均耗时。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：ms/Count|≥ 0 ms/Count|裸金属服务器|1分钟|
|disk_ioUtils|（Agent）磁盘I/O使用率|该指标用于统计测量对象磁盘I/O使用率。通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|
|disk_queue_length|（Agent）平均队列长度|该指标用于统计指定时间段内，平均等待完成的读取或写入操作请求的数量。通过计算采集周期内/proc/diskstats中对应设备第十四列数据的变化得出磁盘平均队列长度。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：个|≥ 0 个|裸金属服务器|1分钟|
|disk_write_bytes_per_operation|（Agent）平均写操作大小|该指标用于统计指定时间段内，平均每个写I/O操作传输的字节数。通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化与第八列数据的变化相除得出磁盘平均写操作大小。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：KB/op|≥ 0 KB/op|裸金属服务器|1分钟|
|disk_read_bytes_per_operation|（Agent）平均读操作大小|该指标用于统计指定时间段内，平均每个读I/O操作传输的字节数。通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化与第四列数据的变化相除得出磁盘平均读操作大小。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：KB/op|≥ 0 KB/op|裸金属服务器|1分钟|
|disk_io_svctm|（Agent）平均I/O服务时长|该指标用于统计指定时间段内，平均每个读或写I/O的操作时长。通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化与第四列数据与第八列数据和的变化相除得出磁盘平均I/O时长。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：ms/op|≥ 0 ms/op|裸金属服务器|1分钟|


**表 6**  文件系统类监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|disk_fs_rwstate|（Agent）文件系统读写状态|该指标用于统计测量对象挂载文件系统的读写状态。状态分为：可读写（0）/只读（1）。通过读取/proc/mounts中第四列文件系统挂载参数获得。|0，1|裸金属服务器|1分钟|
|disk_inodesTotal|（Agent）inode空间大小|该指标用于统计测量对象当前磁盘的inode空间量。执行**df -i**命令，查看Inodes列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。|≥ 0|裸金属服务器|1分钟|
|disk_inodesUsed|（Agent）inode已使用空间|该指标用于统计测量对象当前磁盘已使用的inode空间量。执行**df -i**命令，查看IUsed列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。|≥ 0|裸金属服务器|1分钟|
|disk_inodesUsedPercent|（Agent）inode已使用占比|该指标用于统计测量对象当前磁盘已使用的inode占比。执行**df -i**命令，查看IUse%列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。单位：百分比|0-100%|裸金属服务器|1分钟|


**表 7**  网卡相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|net_bitRecv|（Agent）入网带宽|该指标用于统计测量对象网卡每秒接收的比特数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：bit/s|≥ 0 bit/s|裸金属服务器|1分钟|
|net_bitSent|（Agent）出网带宽|该指标用于统计测量对象网卡每秒发送的比特数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：bit/s|≥ 0 bit/s|裸金属服务器|1分钟|
|net_packetRecv|（Agent）网卡包接收速率|该指标用于统计测量对象网卡每秒接收的数据包数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：Counts/s|≥ 0 Counts/s|裸金属服务器|1分钟|
|net_packetSent|（Agent）网卡包发送速率|该指标用于统计测量对象网卡每秒发送的数据包数。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：Counts/s|≥ 0 Counts/s|裸金属服务器|1分钟|
|net_errin|（Agent）接收误包率|该指标用于统计测量对象网卡每秒接收的错误数据包数量占所接收的数据包的比率。单位：百分比|0-100%|裸金属服务器|1分钟|
|net_errout|（Agent）发送误包率|该指标用于统计测量对象网卡每秒发送的错误数据包数量占所发送的数据包的比率。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：百分比|0-100%|裸金属服务器|1分钟|
|net_dropin|（Agent）接收丢包率|该指标用于统计测量对象网卡每秒接收并已丢弃的数据包数量占所接收的数据包的比率。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：百分比|0-100%|裸金属服务器|1分钟|
|net_dropout|（Agent）发送丢包率|该指标用于统计测量对象网卡每秒发送并已丢弃的数据包数量占所发送的数据包的比率。通过计算采集周期内“/proc/net/dev”文件中的变化得出。单位：百分比|0-100%|裸金属服务器|1分钟|


**表 8**  软RAID相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|md1_status_device:1|（Agent）软RAID状态|该指标用于统计测量对象软RAID设备的状态，RAID异常情况下值为0。通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行**mdadm -D /dev/***md0*（RAID名称）得出。|0，1|裸金属服务器|1分钟|
|md1_active_device:2|（Agent）软RAID活跃设备数|该指标用于统计测量对象软RAID设备的活跃盘数，RAID异常情况下值为-1。通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行**mdadm -D /dev/***md0*（RAID名称）得出。|≥0，-1|裸金属服务器|1分钟|
|md1_working_device:2|（Agent）软RAID工作设备数|该指标用于统计测量对象软RAID设备的工作设备数，RAID异常情况下值为-1。通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行**mdadm -D /dev/***md0*（RAID名称）得出。|≥0，-1|裸金属服务器|1分钟|
|md1_failed_device:0|（Agent）软RAID失败设备数|该指标用于统计测量对象软RAID设备的失败设备数，RAID异常情况下值为-1。通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行**mdadm -D /dev/***md0*（RAID名称）得出。|≥0，-1|裸金属服务器|1分钟|
|md1_spare_device:0|（Agent）软RAID备用设备数|该指标用于统计测量对象软RAID设备的备用设备数，RAID异常情况下值为-1。通过采集周期内执行插件脚本“/usr/local/telescope/plugins/raid-monitor.sh”，脚本中计算“/proc/mdstat”文件中的变化并执行**mdadm -D /dev/***md0*（RAID名称）得出。|≥0，-1|裸金属服务器|1分钟|


**表 9**  进程相关监控指标说明

|指标ID|指标名称|指标含义|取值范围|测量对象|监控周期（原始指标）|
|--|--|--|--|--|--|
|proc_pHashId_cpu|进程CPU使用率|进程消耗的CPU百分比，pHashId是（进程名+进程ID）的md5值。通过计算/proc/pid/stat的变化得出。单位：百分比|0-100%|裸金属服务器|1分钟|
|proc_pHashId_mem|进程内存使用率|进程消耗的内存百分比，pHashId是（进程名+进程ID）的md5值。计算方式：RSS*PAGESIZE/MemTotalRSS：通过获取/proc/pid/statm第二列得到PAGESIZE：通过命令getconf PAGESIZE获取MemTotal：通过/proc/meminfo获取单位：百分比|0-100%|裸金属服务器|1分钟|
|proc_pHashId_file|进程打开文件数|进程打开文件数，pHashId是（进程名+进程ID）的md5值。通过执行**ls -l /proc/pid/fd**可以查看数量。|≥0|裸金属服务器|1分钟|
|proc_running_count|（Agent）运行中进程数|该指标用于统计测量对象处于运行状态的进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|
|proc_idle_count|（Agent）空闲进程数|该指标用于统计测量对象处于空闲状态的进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|
|proc_zombie_count|（Agent）僵死进程数|该指标用于统计测量对象处于僵死状态的进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|
|proc_blocked_count|（Agent）阻塞进程数|该指标用于统计测量对象被阻塞的进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|
|proc_sleeping_count|（Agent）睡眠进程数|该指标用于统计测量对象处于睡眠状态的进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|
|proc_total_count|（Agent）系统进程数|该指标用于统计测量对象的总进程数。通过统计/proc/pid/status中Status值获取每个进程的状态，进而统计各个状态进程总数。|≥0|裸金属服务器|1分钟|


