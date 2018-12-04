# SSH密码方式登录<a name="zh-cn_topic_0053537015"></a>

## 前提条件<a name="section33044631113942"></a>

-   裸金属服务器已经绑定弹性公网IP地址。
-   已配置安全组入方向的访问规则，配置方式请参见[配置安全组](https://support.huaweicloud.com/usermanual-bms/zh-cn_topic_0028313245.html)。
-   使用的登录工具（如PuTTY）与待登录的裸金属服务器之间网络连通。例如，默认的22端口没有被防火墙屏蔽。

>![](public_sys-resources/icon-note.gif) **说明：**   
>密码登录方式创建的Linux裸金属服务器，如需使用SSH密码方式登录，请先使用裸金属服务器页面的远程登录功能登录裸金属服务器，开启SSH密码登录方式，具体操作请参见[如何设置SSH服务配置项](http://support.huaweicloud.com/faq-bms/bms_faq_0040.html)。  

## Windows系统<a name="section62238598113942"></a>

如果您用于登录BMS的服务器的系统是Windows，以PuTTY为例，可以按照下面方式登录裸金属服务器。

1.  运行PuTTY。
2.  单击“Session”，在“Host Name \(or IP address\)”下的输入框中输入裸金属服务器的弹性公网IP地址，连接方式选择SSH。
3.  单击“Open”。
4.  输入用户名“root”和密码，登录裸金属服务器。

## Linux系统<a name="section6934158113942"></a>

如果您登录BMS的服务器的系统是Linux，您可以在服务器的命令行中运行如下命令登录裸金属服务器。

**ssh** _裸金属服务器__的弹性公网IP地址_

