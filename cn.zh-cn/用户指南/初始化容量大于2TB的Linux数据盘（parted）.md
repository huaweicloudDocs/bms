# 初始化容量大于2TB的Linux数据盘（parted）<a name="bms_umn_0028"></a>

## 操作场景<a name="zh-cn_topic_0117871092_section29374781163839"></a>

本文以裸金属服务器的操作系统为“CentOS 7.4 64位”、云硬盘容量为3 TB举例，采用Parted分区工具为容量大于2 TB的数据盘设置分区。

MBR格式分区支持的磁盘最大容量为2 TB，GPT分区表最大支持的磁盘容量为18 EB，因此当为容量大于2 TB的磁盘分区时，请采用GPT分区方式。对于Linux操作系统而言，当磁盘分区形式选用GPT时，fdisk分区工具将无法使用，需要采用parted工具。关于磁盘分区形式的更多介绍，请参见[初始化数据盘场景及磁盘分区形式介绍](初始化数据盘场景及磁盘分区形式介绍.md)。

不同服务器的操作系统的格式化操作可能不同，本文仅供参考，具体操作步骤和差异请参考对应的服务器操作系统的产品文档。

>![](public_sys-resources/icon-notice.gif) **须知：**   
>首次使用云磁盘时，如果您未参考本章节对磁盘执行初始化操作，主要包括创建分区和文件系统等操作，那么当后续扩容磁盘时，新增容量部分的磁盘可能无法正常使用。  

## 前提条件<a name="zh-cn_topic_0084935709_section36737034185332"></a>

-   已登录裸金属服务器。
-   已挂载数据盘至裸金属服务器，且该数据盘未初始化。

## 划分分区并挂载磁盘<a name="zh-cn_topic_0117871092_section36039836195351"></a>

本操作以该场景为例，当裸金属服务器挂载了一块新的数据盘时，采用parted分区工具为数据盘设置分区，分区形式设置为GPT，文件系统设为ext4格式，挂载在“/mnt/sdc”下，并设置开机启动自动挂载。

1.  执行以下命令，查看新增数据盘。

    **lsblk**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# lsblk
    NAME   MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
    vda    253:0    0  40G  0 disk
    ├─vda1 253:1    0   1G  0 part /boot
    └─vda2 253:2    0  39G  0 part /
    vdb    253:16   0   3T  0 disk
    ```

    表示当前的服务器有两块磁盘，“/dev/vda“是系统盘，“/dev/vdb“是新增数据盘。

2.  执行以下命令，进入parted分区工具，开始对新增数据盘执行分区操作。

    **parted** _新增数据盘_

    以新挂载的数据盘“/dev/vdb”为例：

    **parted** **/dev/vdb**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# parted /dev/vdb
    GNU Parted 3.1
    Using /dev/vdb
    Welcome to GNU Parted! Type 'help' to view a list of commands.
    (parted)
    ```

3.  输入“p”，按“Enter”，查看当前磁盘分区形式。

    回显类似如下信息：

    ```
    (parted) p
    Error: /dev/vdb: unrecognised disk label
    Model: Virtio Block Device (virtblk)
    Disk /dev/vdb: 3299GB
    Sector size (logical/physical): 512B/512B
    Partition Table: unknown
    Disk Flags:
    (parted)
    ```

    “Partition Table”为“unknown”表示磁盘分区形式未知。

4.  输入以下命令，设置磁盘分区形式。

    **mklabel** _磁盘分区方式_

    磁盘分区形式有MBR和GPT两种，大于2 TB的磁盘容量，请采用GPT分区方式：

    **mklabel** **gpt**

    >![](public_sys-resources/icon-notice.gif) **须知：**   
    >MBR支持的磁盘最大容量为2 TB，GPT最大支持的磁盘容量为18 EB，当前数据盘支持的最大容量为32 TB，如果您需要使用大于2 TB的磁盘容量，分区形式请采用GPT。  
    >当磁盘已经投入使用后，此时切换磁盘分区形式时，磁盘上的原有数据将会清除，因此请在磁盘初始化时谨慎选择磁盘分区形式。  

5.  输入“p”，按“Enter”，设置分区形式后查看磁盘分区形式。

    回显类似如下信息：

    ```
    (parted) mklabel gpt
    (parted) p
    Model: Virtio Block Device (virtblk)
    Disk /dev/vdb: 3299GB
    Sector size (logical/physical): 512B/512B
    Partition Table: gpt
    Disk Flags:
     
    Number  Start  End  Size  File system  Name  Flags
     
    (parted)
    ```

6.  输入“unit s”，按“Enter”，设置磁盘的计量单位为磁柱。
7.  以为整个磁盘创建一个分区为例，输入“mkpart opt 2048s  _100%_”，按“Enter”。

    “2048s”表示磁盘起始容量，“100%”表示磁盘截止容量，此处仅供参考，您可以根据业务需要自行规划磁盘分区数量及容量。

    回显类似如下信息：

    ```
    (parted) mkpart opt 2048s 100%
    Warning: The resulting partition is not properly aligned for best performance.
    Ignore/Cancel? Cancel 
    ```

    若出现以上性能优化提示，请先输入“Cancel”，停止分区。然后找出对应磁盘最优性能的初始磁柱值，再使用该值进行分区即可。本示例中性能最优的初始磁柱值即为2048s，因此系统没有该提示。

8.  输入“p”，按“Enter”，查看新建分区的详细信息。

    回显类似如下信息：

    ```
    (parted) p
    Model: Virtio Block Device (virtblk)
    Disk /dev/vdb: 6442450944s
    Sector size (logical/physical): 512B/512B
    Partition Table: gpt
    Disk Flags:
     
    Number  Start  End          Size         File system  Name  Flags
     1      2048s  6442448895s  6442446848s               opt
    ```

    表示新建分区“dev/vdb1”的详细信息。

9.  输入“q”，按“Enter”，退出parted分区工具。
10. 执行以下命令，查看磁盘分区信息。

    **lsblk**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# lsblk
    NAME   MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
    vda    253:0    0  40G  0 disk
    ├─vda1 253:1    0   1G  0 part /boot
    └─vda2 253:2    0  39G  0 part /
    vdb    253:16   0   3T  0 disk
    └─vdb1 253:17   0   3T  0 part
    ```

    此时可以查看到新建分区“/dev/vdb1”。

11. 执行以下命令，将新建分区文件系统设为系统所需格式。

    **mkfs** **-t** _文件系统格式_ **/dev/vdb1**

    以设置文件系统为“ext4“为例：

    **mkfs** **-t** **ext4** **/dev/vdb1**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# mkfs -t ext4 /dev/vdb1
    mke2fs 1.42.9 (28-Dec-2013)
    Filesystem label=
    OS type: Linux
    Block size=4096 (log=2)
    Fragment size=4096 (log=2)
    Stride=0 blocks, Stripe width=0 blocks
    201326592 inodes, 805305856 blocks
    40265292 blocks (5.00%) reserved for the super user
    First data block=0
    Maximum filesystem blocks=2952790016
    24576 block groups
    32768 blocks per group, 32768 fragments per group
    8192 inodes per group
    Superblock backups stored on blocks:
            32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208,
            4096000, 7962624, 11239424, 20480000, 23887872, 71663616, 78675968,
            102400000, 214990848, 512000000, 550731776, 644972544
     
    Allocating group tables: done
    Writing inode tables: done
    Creating journal (32768 blocks): done
    Writing superblocks and filesystem accounting information: done
    ```

    格式化需要等待一段时间，请观察系统运行状态，不要退出。

    >![](public_sys-resources/icon-notice.gif) **须知：**   
    >不同文件系统支持的分区大小不同，请根据您的业务需求选择合适的文件系统。  

12. <a name="zh-cn_topic_0117871092_li1758111811323"></a>执行以下命令，新建挂载点。

    **mkdir** _挂载点_

    以新建挂载点“/mnt/sdc“为例：

    **mkdir** **/mnt/sdc**

13. 执行以下命令，将新建分区挂载到[12](#zh-cn_topic_0117871092_li1758111811323)中新建的挂载点下。

    **mount** **/dev/vdb1** _挂载点_

    以挂载新建分区至“/mnt/sdc“为例：

    **mount** **/dev/vdb1** **/mnt/sdc**

14. 执行以下命令，查看挂载结果。

    **df** **-TH**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# df -TH
    Filesystem     Type      Size  Used Avail Use% Mounted on
    /dev/vda2      ext4       42G  1.5G   38G   4% /
    devtmpfs       devtmpfs  2.0G     0  2.0G   0% /dev
    tmpfs          tmpfs     2.0G     0  2.0G   0% /dev/shm
    tmpfs          tmpfs     2.0G  8.9M  2.0G   1% /run
    tmpfs          tmpfs     2.0G     0  2.0G   0% /sys/fs/cgroup
    /dev/vda1      ext4      1.1G  153M  801M  17% /boot
    tmpfs          tmpfs     398M     0  398M   0% /run/user/0
    /dev/vdb1      ext4      3.3T   93M  3.1T   1% /mnt/sdc
    ```

    表示新建分区“dev/vdb1”已挂载至“/mnt/sdc“。


## 设置开机自动挂载磁盘<a name="zh-cn_topic_0117871092_section0312944173714"></a>

如果您需要在裸金属服务器系统启动时自动挂载磁盘，不能采用在/etc/fstab直接指定 /dev/vdb1的方法，因为云中设备的顺序编码在关闭或者开启服务器过程中可能发生改变，例如/dev/vdb1可能会变成/dev/vdb2。推荐使用UUID来配置自动挂载数据盘。

>![](public_sys-resources/icon-note.gif) **说明：**   
>磁盘的UUID（Universally Unique Identifier）是Linux系统为磁盘分区提供的唯一的标识字符串。  

1.  执行如下命令，查询磁盘分区的UUID。

    **blkid** _磁盘分区_

    以查询磁盘分区“/dev/vdb1“的UUID为例：

    **blkid** **/dev/vdb1**

    回显类似如下信息：

    ```
    [root@bms-centos74 ~]# blkid /dev/vdb1
    /dev/vdb1: UUID="bdd29fe6-9cee-4d4f-a553-9faad281f89b" TYPE="ext4" PARTLABEL="opt" PARTUUID="c7122c92-ed14-430b-9ece-259920d5ee74"
    ```

    表示“/dev/vdb1“的UUID。

2.  执行以下命令，使用VI编辑器打开“fstab”文件。

    **vi** **/etc/fstab**

3.  按“i”，进入编辑模式。
4.  将光标移至文件末尾，按“Enter”，添加如下内容。

    ```
    UUID=bdd29fe6-9cee-4d4f-a553-9faad281f89b /mnt/sdc      ext4 defaults     0   2
    ```

5.  按“ESC”后，输入“:wq”，按“Enter”。

    保存设置并退出编辑器。


