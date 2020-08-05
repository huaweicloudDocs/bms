# 初始化Linux数据盘（fdisk）<a name="bms_01_0019"></a>

## 操作场景<a name="zh-cn_topic_0044524669_section31580524185332"></a>

本文以裸金属服务器的操作系统为“CentOS 7.0 64位”为例，采用fdisk分区工具为数据盘设置分区。

MBR格式分区支持的磁盘最大容量为2 TB，GPT分区表最大支持的磁盘容量为18 EB，因此当为容量大于2 TB的磁盘分区时，请采用GPT分区方式。对于Linux操作系统而言，当磁盘分区形式选用GPT时，fdisk分区工具将无法使用，需要采用parted工具。关于磁盘分区形式的更多介绍，请参见[初始化数据盘场景及磁盘分区形式介绍](初始化数据盘场景及磁盘分区形式介绍.md)。

不同服务器的操作系统的格式化操作可能不同，本文仅供参考，具体操作步骤和差异请参考对应的服务器操作系统的产品文档。

>![](public_sys-resources/icon-caution.gif) **注意：** 
>首次使用云磁盘时，如果您未参考本章节对磁盘执行初始化操作，主要包括创建分区和文件系统等操作，那么当后续扩容磁盘时，新增容量部分的磁盘可能无法正常使用。

## 前提条件<a name="zh-cn_topic_0044524669_section117091356845"></a>

-   已登录裸金属服务器。
-   已挂载数据盘至裸金属服务器，且该数据盘未初始化。

## 划分分区并挂载磁盘<a name="zh-cn_topic_0044524669_section36039836195351"></a>

本操作以该场景为例，当裸金属服务器挂载了一块新的数据盘时，使用fdisk分区工具将该数据盘设为主分区，分区形式默认设置为MBR，文件系统设为ext4格式，挂载在“/mnt/sdc”下，并设置开机启动自动挂载。

1.  执行以下命令，查看新增数据盘。

    **fdisk** **-l**

    回显类似如下信息：

    ```
    [root@bms-b656 test]# fdisk -l
    
    Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
    Units = sectors of 1 * 512 = 512 bytes
    Sector size (logical/physical): 512 bytes / 512 bytes
    I/O size (minimum/optimal): 512 bytes / 512 bytes
    Disk label type: dos
    Disk identifier: 0x000cc4ad
    
       Device Boot      Start         End      Blocks   Id  System
    /dev/xvda1   *        2048     2050047     1024000   83  Linux
    /dev/xvda2         2050048    22530047    10240000   83  Linux
    /dev/xvda3        22530048    24578047     1024000   83  Linux
    /dev/xvda4        24578048    83886079    29654016    5  Extended
    /dev/xvda5        24580096    26628095     1024000   82  Linux swap / Solaris
    
    Disk /dev/sdb: 10.7 GB, 10737418240 bytes, 20971520 sectors
    Units = sectors of 1 * 512 = 512 bytes
    Sector size (logical/physical): 512 bytes / 512 bytes
    I/O size (minimum/optimal): 512 bytes / 512 bytes
    ```

    表示当前的服务器有两块磁盘，“/dev/sda“是系统盘，“/dev/sdb“是新增数据盘。

2.  执行以下命令，进入fdisk分区工具，开始对新增数据盘执行分区操作。

    **fdisk** _新增数据盘_

    以新挂载的数据盘“/dev/sdb”为例：

    **fdisk** **/dev/sdb**

    回显类似如下信息：

    ```
    [root@ecs-b656 test]# fdisk /dev/sdb
    Welcome to fdisk (util-linux 2.23.2).
    Changes will remain in memory only, until you decide to write them.
    Be careful before using the write command.
    Device does not contain a recognized partition table
    Building a new DOS disklabel with disk identifier 0xb00005bd.
    Command (m for help): 
    ```

3.  输入“n”，按“Enter”，开始新建分区。

    回显类似如下信息：

    ```
    Command (m for help): n
    Partition type:
       p   primary (0 primary, 0 extended, 4 free)
       e   extended
    ```

    表示磁盘有两种分区类型：

    -   “p“表示主要分区。
    -   “e“表示延伸分区。

4.  以创建一个主要分区为例，输入“p”，按“Enter”，开始创建一个主分区。

    回显类似如下信息：

    ```
    Select (default p): p
    Partition number (1-4, default 1):
    ```

    “Partition number“表示主分区编号，可以选择1-4。

5.  以分区编号选择“1“为例，输入主分区编号“1“，按“Enter”。

    回显类似如下信息：

    ```
    Partition number (1-4, default 1): 1
    First sector (2048-20971519, default 2048):
    ```

    “First sector“表示初始磁柱区域，可以选择2048-20971519，默认为2048。

6.  以选择默认初始磁柱编号2048为例，按“Enter”。

    回显类似如下信息：

    ```
    First sector (2048-20971519, default 2048):
    Using default value 2048
    Last sector, +sectors or +size{K,M,G} (2048-20971519, default 20971519):
    ```

    “Last sector“表示截止磁柱区域，可以选择2048-20971519，默认为20971519。

7.  以选择默认截止磁柱编号20971519为例，按“Enter”。

    回显类似如下信息：

    ```
    Last sector, +sectors or +size{K,M,G} (2048-20971519, default 20971519):
    Using default value 20971519
    Partition 1 of type Linux and of size 10 GiB is set
    Command (m for help):
    ```

    表示分区完成，即为10GB的数据盘新建了1个分区。

8.  输入“p”，按“Enter”，查看新建分区的详细信息。

    回显类似如下信息：

    ```
    Command (m for help): p
    
    Disk /dev/sdb: 10.7 GB, 10737418240 bytes, 20971520 sectors
    Units = sectors of 1 * 512 = 512 bytes
    Sector size (logical/physical): 512 bytes / 512 bytes
    I/O size (minimum/optimal): 512 bytes / 512 bytes
    Disk label type: dos
    Disk identifier: 0xb00005bd
    
       Device Boot      Start         End      Blocks   Id  System
    /dev/sdb1            2048    20971519    10484736   83  Linux
    
    Command (m for help): 
    ```

    表示新建分区“/dev/sdb1“的详细信息。

9.  输入“w”，按“Enter”，将分区结果写入分区表中。

    回显类似如下信息：。

    ```
    Command (m for help): w
    The partition table has been altered!
    
    Calling ioctl() to re-read partition table.
    Syncing disks.
    ```

    表示分区创建完成。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果之前分区操作有误，请输入“q”，则会退出fdisk分区工具，之前的分区结果将不会被保留。

10. 执行以下命令，将新的分区表变更同步至操作系统。

    **partprobe**

11. 执行以下命令，将新建分区文件系统设为系统所需格式。

    **mkfs** **-t** _文件系统格式_ **/dev/sdb1**

    以设置文件系统为“ext4“为例：

    **mkfs** **-t** **ext4** **/dev/sdb1**

    回显类似如下信息：

    ```
    [root@bms-b656 test]# mkfs -t ext4 /dev/sdb1
    mke2fs 1.42.9 (28-Dec-2013)
    Filesystem label=
    OS type: Linux
    Block size=4096 (log=2)
    Fragment size=4096 (log=2)
    Stride=0 blocks, Stripe width=0 blocks
    655360 inodes, 2621184 blocks
    131059 blocks (5.00%) reserved for the super user
    First data block=0
    Maximum filesystem blocks=2151677952
    80 block groups
    32768 blocks per group, 32768 fragments per group
    8192 inodes per group
    Superblock backups stored on blocks:
            32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632
    
    Allocating group tables: done
    Writing inode tables: done
    Creating journal (32768 blocks): done
    Writing superblocks and filesystem accounting information: done
    ```

    格式化需要等待一段时间，请观察系统运行状态，不要退出。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >不同文件系统支持的分区大小不同，请根据您的业务需求选择合适的文件系统。

12. <a name="zh-cn_topic_0044524669_li1758111811323"></a>执行以下命令，新建挂载点。

    **mkdir** _挂载点_

    以新建挂载点“/mnt/sdc“为例：

    **mkdir** **/mnt/sdc**

13. 执行以下命令，将新建分区挂载到[12](#zh-cn_topic_0044524669_li1758111811323)中新建的挂载点下。

    **mount** **/dev/sdb1** _挂载点_

    以挂载新建分区至“/mnt/sdc“为例：

    **mount** **/dev/sdb1** **/mnt/sdc**

14. 执行以下命令，查看挂载结果。

    **df** **-TH**

    回显类似如下信息：

    ```
    [root@bms-b656 test]# df -TH
    Filesystem     Type      Size  Used Avail Use% Mounted on
    /dev/xvda2     xfs        11G  7.4G  3.2G  71% /
    devtmpfs       devtmpfs  4.1G     0  4.1G   0% /dev
    tmpfs          tmpfs     4.1G   82k  4.1G   1% /dev/shm
    tmpfs          tmpfs     4.1G  9.2M  4.1G   1% /run
    tmpfs          tmpfs     4.1G     0  4.1G   0% /sys/fs/cgroup
    /dev/sda3     xfs       1.1G   39M  1.1G   4% /home
    /dev/sda1     xfs       1.1G  131M  915M  13% /boot
    /dev/sdb1     ext4       11G   38M  9.9G   1% /mnt/sdc
    ```

    表示新建分区“/dev/sdb1“已挂载至“/mnt/sdc“。


## 设置开机自动挂载磁盘<a name="zh-cn_topic_0044524669_section15839912195453"></a>

如果您需要在服务器系统启动时自动挂载磁盘，不能采用在 /etc/fstab直接指定 /dev/sdb1的方法，因为云中设备的顺序编码在关闭或者开启服务器过程中可能发生改变，例如/dev/sdb可能会变成/dev/sdc。推荐使用UUID来配置自动挂载数据盘。

>![](public_sys-resources/icon-note.gif) **说明：** 
>磁盘的UUID（Universally Unique Identifier）是Linux系统为磁盘分区提供的唯一的标识字符串。

1.  执行如下命令，查询磁盘分区的UUID。

    **blkid** _磁盘分区_

    以查询磁盘分区“/dev/sdb1“的UUID为例：

    **blkid** **/dev/sdb1**

    回显类似如下信息：

    ```
    [root@bms-b656 test]# blkid /dev/sdb1
    /dev/sdb1: UUID="1851e23f-1c57-40ab-86bb-5fc5fc606ffa" TYPE="ext4"
    ```

    表示“/dev/sdb1“的UUID。

2.  执行以下命令，使用vi编辑器打开“fstab”文件。

    **vi** **/etc/fstab**

3.  按“i”，进入编辑模式。
4.  将光标移至文件末尾，按“Enter”，添加如下内容。

    ```
    UUID=1851e23f-1c57-40ab-86bb-5fc5fc606ffa /mnt/sdc      ext4 defaults     0   2
    ```

5.  按“ESC”后，输入**:wq**，按“Enter”。

    保存设置并退出编辑器。


