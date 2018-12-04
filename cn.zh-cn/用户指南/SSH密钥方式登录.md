# SSH密钥方式登录<a name="zh-cn_topic_0027575694"></a>

## 前提条件<a name="section33044631113942"></a>

-   裸金属服务器已经绑定弹性公网IP地址。
-   已在本地获取登录裸金属服务器的私钥文件。
-   已配置安全组入方向的访问规则，配置方式请参见[配置安全组](https://support.huaweicloud.com/usermanual-bms/zh-cn_topic_0028313245.html)。
-   使用的登录工具（如PuTTY）与待登录的裸金属服务器之间网络连通。例如，默认的22端口没有被防火墙屏蔽。

## 本地使用Windows操作系统<a name="section62238598113942"></a>

如果您本地使用Windows操作系统登录Linux裸金属服务器，可以按照下面方式登录。

我们以PuTTY工具为例介绍如何登录Linux裸金属服务器。使用PuTTY登录裸金属服务器前，需要先将私钥文件转化为.ppk格式。

1.  判断私钥文件是否为.ppk格式。
    -   是，执行步骤[7](#li693703913264)。
    -   否，执行步骤[2](#li11816141811202)。

2.  <a name="li11816141811202"></a>在以下路径中下载PuTTY和PuTTYgen。

    [http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >PuTTYgen是密钥生成器，用于创建密钥对，生成一对公钥和私钥供PuTTY使用。  

3.  运行PuTTYgen。
4.  在“Actions”区域，单击“Load”，并导入创建裸金属服务器时保存的私钥文件。

    导入时注意确保导入的格式要求为“All files \(\*.\*\)”。

5.  单击“Save private key”。
6.  <a name="li194442401260"></a>保存转化后的私钥到本地。例如：kp-123.ppk
7.  <a name="li693703913264"></a>双击“PUTTY.EXE”，打开“PuTTY Configuration”。

    **图 1**  PuTTY Configuration<a name="fig14750143592717"></a>  
    ![](figures/PuTTY-Configuration.png "PuTTY-Configuration")

8.  选择“Connection \> Data”，在Auto-login username处输入镜像的用户名。
9.  选择“Connection \> SSH \> Auth”，在最下面一个配置项“Private key file for authentication”中，单击“Browse”，选择步骤[6](#li194442401260)转化的密钥。
10. 单击“Session”，在“Host Name \(or IP address\)”下的输入框中输入裸金属服务器的弹性公网IP地址。
11. 单击“Open”。

    登录裸金属服务器。


## 本地使用Linux操作系统<a name="section3666784111724"></a>

如果您本地使用Linux操作系统登录Linux裸金属服务器，可以按照下面方式登录。下面步骤以私钥文件是“KeyPair-ee55”为例进行介绍。

1.  在您的linux计算机的命令行中执行如下命令，变更权限。

    **chmod 600 /**_path_/_KeyPair-ee55_

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >上述命令的path为密钥文件的存放路径。  

2.  执行如下命令登录裸金属服务器。

    **ssh -i /**_path_/_KeyPair-ee55_ _xxx_**@** _裸金属服务器__弹性公网IP地址_

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   path为密钥文件的存放路径。  
    >-   xxx为裸金属服务器下发过程中默认创建的，如果创建裸金属服务器时使用Red Hat操作系统，则用户名为rhel。  


