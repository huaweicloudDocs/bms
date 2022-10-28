# 如何设置SSH服务配置项？<a name="bms_faq_0040"></a>

您可以根据需要选择登录裸金属服务器的登录方式或帐户类型，如果需要特殊配置，可执行以下操作：

1.  如果要禁用密码远程登录，仅支持证书登录的方式，以提高裸金属服务器的安全性，可设置如下参数：
    -   查看文件“/etc/cloud/cloud.cfg”中是否存在参数“ssh\_pwauth”且值是否为“false”，若不是则修改或添加该参数且值为“false”，使其在使用Xshell登录时，拒绝通过password方式输入密码登录。
    -   查看文件“/etc/ssh/sshd\_config”中参数“ChallengeResponseAuthentication ”的值是否为“no”，若不是则修改为“no”。使其在使用Xshell登录时，拒绝通过keyboard inactive方式输入密码登录。

2.  如果开放root密码远程登录并开启root用户的SSH权限，需要执行以下操作：

    >![](public_sys-resources/icon-caution.gif) **注意：** 
    >允许root用户登录有一定的安全隐患，请谨慎操作。

    1.  修改cloud-init配置文件。

        以CentOS 6.7系列操作系统为例，修改如下参数：

        ```
        users: 
          - name: root 
            lock_passwd: false 
          
        disable_root: 0 
        ssh_pwauth: 1
        ```

        其中，

        -   lock\_passwd字段设置为false，表示不锁住用户密码。
        -   disable\_root字段用于是否禁用远程ssh root登录，此处设置为0，表示不禁用（部分操作系统的cloud-init配置使用true表示禁用，false表示不禁用）。
        -   ssh\_pwauth字段用于是否支持ssh密码登录，此处设置为1，表示支持。

    2.  执行以下命令，在vi编辑器中打开“/etc/ssh/sshd\_config”。

        **vi /etc/ssh/sshd\_config**

        将“sshd\_config”中的“PasswordAuthentication”的值修改为“yes”。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >-   如果是SUSE和OpenSUSE系列操作系统，需要将“sshd\_config”中的“PasswordAuthentication”和“ChallengeResponseAuthentication”参数同时配置为“yes”。
        >-   如果是Ubuntu系列操作系统，需要将“PermitRootLogin”参数配置为“yes”。

    3.  修改shadow文件配置，将镜像模板中的初始root帐户密码锁定，避免安全风险。
        1.  使用vim编辑器打开“/etc/shadow”配置文件。

            **vim /etc/shadow**

            在root帐户的密码hash值中添加“!!”。修改后的配置文件如下：

            ```
            # cat /etc/shadow | grep root 
             root:!!$6$SphQRPXu$Nvg6izXbhDPrcY3j1vRiHaQFVRpNiV3HD/bjDgnZrACOWPXwJahx78iaut1IigIUrwavVGSYQ1JOIw.rDlVh7.:17376:0:99999:7::
            ```

        2.  修改完成后，按“Esc”，输入**:wq**保存并退出文件编辑。

            >![](public_sys-resources/icon-note.gif) **说明：** 
            >如果是Ubuntu系列操作系统，需要将安装操作系统过程中新创建的用户删除。例如创建的用户为“ubuntu”，删除命令：**userdel -rf ubuntu**  。




