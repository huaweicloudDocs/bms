# Linux操作系统常用命令速查<a name="bms_faq_0073"></a>

## lsblk<a name="section2795194911251"></a>

lsblk命令用于列出所有可用块设备的信息，而且还能显示他们之间的依赖关系，但是不会列出RAM盘的信息。块设备有硬盘、闪存、CD-ROM等等。

lsblk命令默认情况下将以树状列出所有块设备。打开终端，并输入以下命令：

```
lsblk
NAME    MAJ:MIN  RM  SIZE RO TYPE  MOUNTPOINT
sda     202:0    0   40G  0  disk 
├─sda1 202:1   0    4G  0  part  [SWAP]
└─sda2 202:2   0   36G  0  part  /
sdb     202:16   0   10G  0  disk
```

7个栏目名称如下：

-   NAME：块设备名称。
-   MAJ:MIN：表示主要和次要设备号。
-   RM：设备是否为可移动设备。“0”表示否；“1”表示是。
-   SIZE：设备的容量大小信息。
-   RO：设备是否为只读。“0”表示否；“1”表示是。
-   TYPE：表示块设备的类型（磁盘或者磁盘上的一个分区）。
-   MOUNTPOINT：设备挂载的挂载点。

