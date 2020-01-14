# 安装Agent<a name="ZH-CN_TOPIC_0141766647"></a>

本章节主要介绍如何在已有裸金属服务器实例中手动安装Agent，实现主机监控。您需要完成以下步骤：

1.  [添加域名解析地址](#zh-cn_topic_0104704865_section20336159191311)：在裸金属服务器“/etc/resolv.conf”文件中添加各区域域名解析地址。
2.  [修改子网DNS地址](#zh-cn_topic_0104704865_section24544395145)：按裸金属服务器所在区域修改子网的DNS服务器地址。
3.  [配置安全组](#zh-cn_topic_0104704865_section49331415141516)：用于下载Telescope包、发送指标数据、采集日志等。
4.  [安装Agent](#zh-cn_topic_0104704865_section2500354141513)：手动为裸金属服务器安装Agent，实现主机监控。

## 添加域名解析地址<a name="zh-cn_topic_0104704865_section20336159191311"></a>

1.  使用root帐号，登录裸金属服务器。
2.  输入**vi /etc/resolv.conf**，打开“/etc/resolv.conf”文件。
3.  在文件中添加“nameserver 100.125.1.250”，如[图1](#zh-cn_topic_0104704865_fig185163506199)所示。

    **图 1**  添加域名解析地址<a name="zh-cn_topic_0104704865_fig185163506199"></a>  
    ![](figures/添加域名解析地址.png "添加域名解析地址")

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >不同区域nameserver不同，如下所示：  
    >华北-北京一：100.125.1.250,100.125.21.250  
    >华东-上海二：100.125.17.29,100.125.135.29  
    >华南-广州：100.125.1.250,100.125.136.29  
    >亚太-香港：100.125.1.250,100.125.3.250  
    >亚太-曼谷：100.125.1.250,100.125.3.250  

4.  按“Esc”，输入**:wq**保存设置。

## 修改子网DNS地址<a name="zh-cn_topic_0104704865_section24544395145"></a>

参考[修改子网DNS地址](自动安装配置Agent（新创建裸金属服务器）.md#zh-cn_topic_0104704446_section99035364202)进行操作。

## 配置安全组<a name="zh-cn_topic_0104704865_section49331415141516"></a>

参考[配置安全组](自动安装配置Agent（新创建裸金属服务器）.md#zh-cn_topic_0104704446_section199181037202414)进行操作。

## 安装Agent<a name="zh-cn_topic_0104704865_section2500354141513"></a>

1.  执行以下命令，安装Agent。

    华北-北京一：

    ```
    cd /usr/local && wget https://telescope.obs.cn-north-1.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    华北-北京四：

    ```
    cd /usr/local && wget https://telescope-cn-north-4.obs.cn-north-4.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    arm通用计算型：

    ```
    cd /usr/local && wget https://telescope-cn-north-4.obs.myhuaweicloud.com/scripts/agentInstallARM.sh && chmod 755 agentInstallARM.sh && ./agentInstallARM.sh
    ```

    华南-广州：

    ```
    cd /usr/local && wget https://telescope-cn-south-1.obs.cn-south-1.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    华东-上海二：

    ```
    cd /usr/local && wget https://telescope-cn-east-2.obs.cn-east-2.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    华东-上海一：

    ```
    cd /usr/local && wget --no-check-certificate https://obs.cn-east-3.myhuaweicloud.com/uniagent-cn-east-3/script/uniagent_install_amd64.sh && bash uniagent_install_amd64.sh
    ```

    亚太-香港：

    ```
    cd /usr/local && wget https://telescope-ap-southeast-1.obs.ap-southeast-1.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    亚太-曼谷：

    ```
    cd /usr/local && wget https://telescope-ap-southeast-2.obs.ap-southeast-2.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    亚太-新加坡：

    ```
    cd /usr/local && wget https://telescope-ap-southeast-3.obs.ap-southeast-3.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    非洲-约翰内斯堡：

    ```
    cd /usr/local && wget https://telescope-af-south-1.obs.af-south-1.myhuaweicloud.com/scripts/agentInstall.sh && chmod 755 agentInstall.sh && ./agentInstall.sh
    ```

    当回显如[图2](#zh-cn_topic_0104704865_zh-cn_topic_0127535833_fig1948103311810)所示时，说明Agent安装成功。

    **图 2**  Agent安装成功<a name="zh-cn_topic_0104704865_zh-cn_topic_0127535833_fig1948103311810"></a>  
    ![](figures/Agent安装成功.png "Agent安装成功")

2.  安装完成后，请参考“[手动配置Agent（Linux）](https://support.huaweicloud.com/usermanual-ces/zh-cn_topic_0085245601.html)”完成Agent的配置。

