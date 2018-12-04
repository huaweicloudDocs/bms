# CentOS 7系列裸金属服务器如何切换内核版本？<a name="bms_faq_0051"></a>

## 问题背景<a name="section053816599522"></a>

对于一些特殊的软件，必须在指定Linux内核版本才能很好地支持，这时就需要切换内核版本了，您可以参考本指导完成切换操作。

## 解决方案<a name="section53364865320"></a>

1.  登录裸金属服务器操作系统。
2.  <a name="li1576484761615"></a>查看当前系统内核版本。

    **uname -r**

    ```
    [root@xxxxxx~]# uname -r
    3.10.0-327.22.2.el7.x86_64
    ```

3.  查看当前系统有几个内核。

    **cat /boot/grub2/grub.cfg | grep menuentry**

    ```
    [root@xxxxxx~]# cat /boot/grub2/grub.cfg | grep menuentry
    if [ x"${feature_menuentry_id}" = xy ]; then
      menuentry_id_option="--id"
      menuentry_id_option=""
    export menuentry_id_option
    menuentry ´CentOS Linux (3.10.0-327.22.2.el7.x86_64) 7 (Core)´ --class centos --class gnu-linux --class gnu --class os --unrestricted $menuentry_id_option ´gnulinux-3.10.0-327.el7.x86_64-advanced-80b9b662-0a1d-4e84-b07b-c1bf19e72d97´ {
    menuentry ´CentOS Linux (3.10.0-327.el7.x86_64) 7 (Core)´ --class centos --class gnu-linux --class gnu --class os --unrestricted $menuentry_id_option ´gnulinux-3.10.0-327.el7.x86_64-advanced-80b9b662-0a1d-4e84-b07b-c1bf19e72d97´ {
    menuentry ´CentOS Linux (0-rescue-7d26c16f128042a684ea474c9e2c240f) 7 (Core)´ --class centos --class gnu-linux --class gnu --class os --unrestricted $menuentry_id_option ´gnulinux-0-rescue-7d26c16f128042a684ea474c9e2c240f-advanced-80b9b662-0a1d-4e84-b07b-c1bf19e72d97´ {
    ```

4.  设置默认的启动内核。

    比如我们选择上一步回显中的“CentOS Linux \(3.10.0-327.el7.x86\_64\) 7 \(Core\)”内核为默认启动。

    **grub2-set-default "CentOS Linux \(3.10.0-327.el7.x86\_64\) 7 \(Core\)"**

5.  查看默认启动的系统内核。

    **grub2-editenv list**

    ```
    [root@xxxxxx~]# grub2-editenv list 
    saved_entry=CentOS Linux (3.10.0-327.el7.x86_64) 7 (Core)
    ```

6.  重启裸金属服务器后，再次进入操作系统，执行[2](#li1576484761615)中的命令观察内核版本是否已成功切换。

    ```
    [root@xxxxxx~]# uname -r
    3.10.0-327.el7.x86_64
    ```


