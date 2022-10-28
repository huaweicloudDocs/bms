# 如何修改“fstab”文件中的磁盘标识方式为UUID？<a name="bms_faq_0058"></a>

## 问题背景<a name="section8777165815715"></a>

对于Linux裸金属服务器，挂载磁盘后需要将“fstab”文件中的磁盘标识方式修改为UUID，否则，裸金属服务器关机再开机，或者重启后会因为挂载点乱序而无法进入操作系统或者业务不可用。

>![](public_sys-resources/icon-note.gif) **说明：** 
>UUID：Universally Unique Identifier，通用唯一识别码，是用于计算机体系中以识别信息数目的一个128位标识符。

## 操作步骤<a name="section19667181242113"></a>

以CentOS 7操作系统为例，介绍如何修改“fstab”文件中的磁盘标识方式为UUID。

1.  使用root用户登录裸金属服务器，执行**blkid**命令，列出当前系统中所有已挂载文件系统的类型以及对应设备的UUID。

    ```
    /dev/sda2: UUID="4eb40294-4c6f-4384-bbb6-b8795bbb1130" TYPE="xfs"
    /dev/sda1: UUID="2de37c6b-2648-43b4-a4f5-40162154e135" TYPE="swap"
    ```

2.  执行**cat /etc/fstab**命令，查看“fstab”文件。

    ```
    /dev/sda2  /       xfs     defaults    0 0
    /dev/sda1  swap    swap    defaults    0 0
    ```

3.  查看“fstab”文件中的磁盘的标识方式。
    -   若为UUID的标识方式，无需修改。
    -   若为设备名称的标识方式，执行[4](#li784575352211)进行修改。

4.  <a name="li784575352211"></a>执行**vi /etc/fstab**命令，打开“fstab”文件，按“i”进入编辑模式，将“fstab”中的磁盘标识方式修改为UUID的形式。

    ```
    UUID=4eb40294-4c6f-4384-bbb6-b8795bbb1130 /       xfs     defaults    0 0
    UUID=2de37c6b-2648-43b4-a4f5-40162154e135 swap    swap    defaults    0 0
    ```

    修改完成后，按“Esc”，输入**:wq**保存并退出文件。


