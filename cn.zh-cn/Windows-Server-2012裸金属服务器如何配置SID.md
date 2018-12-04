# Windows Server 2012裸金属服务器如何配置SID？<a name="bms_faq_0049"></a>

SID也就是安全标识符（Security Identifiers），是标识用户、组和计算机帐户的唯一号码。

1.  修改cloudbase-init的配置文件。
    1.  分别打开“cloudbase-init.conf”和“cloudbase-init-unattend.con”文件。

        文件所在目录：C:\\Program Files\\Cloudbase Solutions\\Cloudbase-Init\\conf

    2.  为两个配置文件都增加一行“first\_logon\_behaviour=no”。

        ```
        [DEFAULT]
        username=Administrator
        groups=Administrators
        first_logon_behaviour=no
        netbios_host_name_compatibility=false
        metadata_services=cloudbaseinit.metadata.services.httpser
        inject_user_password=true
        ...
        ```

    3.  删除“cloudbase-init-unattend.conf”配置文件中的“cloudbaseinit.plugins.common.sethostname.SetHostNamePlugin”。

        ![](figures/配置文件修改示例.png)


2.  打开命令提示符，输入如下命令打开Sysprep窗口。

    ```
    C:\Program Files\Cloudbase Solutions\Cloudbase-Init\conf>C:\Windows\System32\Sysprep\sysprep.exe /unattend:Unattend.xml
    ```

3.  按照下图进行设置。

    ![](figures/System Preparation Tool设置.png)


