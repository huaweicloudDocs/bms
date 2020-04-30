# Windows裸金属服务器挂载云硬盘后提示脱机，如何解决？<a name="bms_faq_0047"></a>

## 问题描述<a name="section123870357116"></a>

Windows裸金属服务器挂载云硬盘后，打开“控制面板”，选择其中的“系统和安全”，选择“管理工具”，双击“计算机管理”。在“计算机管理”页面选择“存储 \> 磁盘管理”，查看挂载的云硬盘显示脱机状态。

## 解决方案<a name="section4448543152417"></a>

1.  登录Windows裸金属服务器操作系统。
2.  单击“开始”菜单，在“搜索程序和文件”中输入**cmd**并按“Enter”，打开命令提示符窗口。
3.  输入命令**diskpart**。

    ```
    C:\Users\Administrator>diskpart
    ```

4.  输入命令**san**。

    ```
    DISKPART> san
    SAN 策略： 全部联机
    ```

5.  输入命令**san policy=onlineall**。

    ```
    DISKPART> san policy=onlineall
    DiskPart 已成功更改用于当前操作系统的SAN策略。
    ```

6.  输入命令list disk，将显示裸金属服务器所有磁盘信息。

    ```
    DISKPART> list disk
    磁盘 ### 状态    大小    可用     Dyn    Gpt
    磁盘 0   联机   838 GB    0B
    磁盘 1   脱机   838 GB    838 GB
    磁盘 2   脱机   838 GB    838 GB
    磁盘 3   脱机   838 GB    838 GB
    ...
    ```

7.  输入命令**select disk** _num_。其中，num表示磁盘号，执行命令时要替换为具体的磁盘号。

    ```
    DISKPART> select disk 4
    ```

8.  输入命令**attributes disk clear readonly**。

    ```
    DISKPART> attributes disk clear readonly
    已成功清除磁盘属性。
    ```

9.  输入命令**online disk**。

    ```
    DISKPART> online disk
    DiskPart 成功使所选磁盘联机。
    ```

10. 修改完成后即可进行格式化云硬盘。

