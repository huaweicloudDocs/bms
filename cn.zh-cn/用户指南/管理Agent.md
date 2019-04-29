# 管理Agent<a name="ZH-CN_TOPIC_0141766649"></a>

本章节指导用户管理Agent，您可进行查看、启动、停止和卸载Agent。

>![](public_sys-resources/icon-note.gif) **说明：**   
>查看、启动、停止和卸载Agent需使用root用户。  

## 查看Agent状态<a name="zh-cn_topic_0104704867_section1546883019433"></a>

登录裸金属服务器，执行以下命令，查看Agent状态。

**service telescoped status**

当系统返回以下内容，则表示Agent为正常运行状态。

```
"Telescope process is running well."
```

## 启动Agent<a name="zh-cn_topic_0104704867_section18605194154420"></a>

执行以下命令，启动Agent。

**/usr/local/telescope/telescoped start**

## 重启Agent<a name="zh-cn_topic_0104704867_section13659182694517"></a>

执行以下命令，重启Agent。

**/usr/local/telescope/telescoped restart**

## 停止Agent<a name="zh-cn_topic_0104704867_section13521205311454"></a>

执行以下命令，停止Agent。

**service telescoped stop**

>![](public_sys-resources/icon-note.gif) **说明：**   
>如果Telescope安装失败，可能会导致无法正常停止Agent，可通过执行以下命令进一步尝试：  
>**/usr/local/telescope/telescoped stop**  

## 卸载Agent<a name="zh-cn_topic_0104704867_section17673352204613"></a>

用户可手动卸载Agent插件，卸载后将不再监控BMS实例监控数据。如需再次使用，请参考[安装Agent](安装Agent.md#ZH-CN_TOPIC_0141766647)重新安装。

执行以下命令，即可卸载Agent。

**/usr/local/telescope/uninstall.sh**

