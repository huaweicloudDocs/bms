# 配置Agent<a name="ZH-CN_TOPIC_0141766648"></a>

用户成功安装Agent插件后，需要修改相关配置文件，用于上报监控指标和心跳数据。

## 前提条件<a name="zh-cn_topic_0104704866_section143239915348"></a>

已成功安装Agent插件。

## 操作步骤<a name="zh-cn_topic_0104704866_section19203299344"></a>

1.  使用root帐号，登录裸金属服务器。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果使用非root帐号登录，可通过**su - root**命令切换至root帐号。  

2.  执行以下命令，切换至Agent安装路径的bin目录下。

    **cd /usr/local/telescope/bin**

3.  修改公共配置文件conf.json。
    1.  执行以下命令，打开公共配置文件conf.json。

        **vi conf.json**

    2.  修改文件中的参数。

        ```
        { 
             "InstanceId":"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", 
             "ProjectId": "b5b92ee0xxxxxxxxxxxxxxxxcab92396", 
             "AccessKey": "QZ0XGJXFxxxxxxxxT65R", 
             "SecretKey": "lEv2aXAGwxxxxxxxxxxxxxxxxxxxxF8t0Bf18Tn2", 
             "RegionId": "cn-north-1"
             "ClientPort": 0,
             "PortNum": 200
         }
        ```

        其中，InstanceId参数如[表1](#zh-cn_topic_0104704866_table10683125111371)所示，其他参数请参见[表2](自动安装配置Agent（新创建裸金属服务器）.md#zh-cn_topic_0104704446_table1083355454411)。

        **表 1**  参数说明

        <a name="zh-cn_topic_0104704866_table10683125111371"></a>
        <table><thead align="left"><tr id="zh-cn_topic_0104704866_row1268575113718"><th class="cellrowborder" valign="top" width="31%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0104704866_p2157141213810"><a name="zh-cn_topic_0104704866_p2157141213810"></a><a name="zh-cn_topic_0104704866_p2157141213810"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="69%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0104704866_p7157201215382"><a name="zh-cn_topic_0104704866_p7157201215382"></a><a name="zh-cn_topic_0104704866_p7157201215382"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="zh-cn_topic_0104704866_row14685175119375"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0104704866_p1368545120370"><a name="zh-cn_topic_0104704866_p1368545120370"></a><a name="zh-cn_topic_0104704866_p1368545120370"></a>InstanceId</p>
        </td>
        <td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704866_p3807112516385"><a name="zh-cn_topic_0104704866_p3807112516385"></a><a name="zh-cn_topic_0104704866_p3807112516385"></a>BMS实例ID，可通过登录管理控制台，在裸金属服务器实例列表中查看。</p>
        <div class="note" id="zh-cn_topic_0104704866_note37911725103816"><a name="zh-cn_topic_0104704866_note37911725103816"></a><a name="zh-cn_topic_0104704866_note37911725103816"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0104704866_ul1080816256383"></a><a name="zh-cn_topic_0104704866_ul1080816256383"></a><ul id="zh-cn_topic_0104704866_ul1080816256383"><li>该实例ID需保证全局唯一性，即同一个RegionId下Agent使用的InstanceId不能相同，否则系统可能会出现异常。</li><li>InstanceId必须与实际的BMS实例ID一致，否则云监控界面将看不到对应BMS实例监控数据。</li></ul>
        </div></div>
        </td>
        </tr>
        <tr id="zh-cn_topic_0104704866_row09353413020"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0104704866_p149351241403"><a name="zh-cn_topic_0104704866_p149351241403"></a><a name="zh-cn_topic_0104704866_p149351241403"></a>ClientPort</p>
        </td>
        <td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704866_p79351943016"><a name="zh-cn_topic_0104704866_p79351943016"></a><a name="zh-cn_topic_0104704866_p79351943016"></a>Agent占用的起始端口号。</p>
        <p id="zh-cn_topic_0104704866_p436355411525"><a name="zh-cn_topic_0104704866_p436355411525"></a><a name="zh-cn_topic_0104704866_p436355411525"></a>默认为0，表示随机占用。1~1023为系统保留端口，建议不要配置。</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0104704866_row1458317128113"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0104704866_p11583712218"><a name="zh-cn_topic_0104704866_p11583712218"></a><a name="zh-cn_topic_0104704866_p11583712218"></a>PortNum</p>
        </td>
        <td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704866_p1583181217117"><a name="zh-cn_topic_0104704866_p1583181217117"></a><a name="zh-cn_topic_0104704866_p1583181217117"></a>Agent占用的端口数量。</p>
        <p id="zh-cn_topic_0104704866_p119271159105217"><a name="zh-cn_topic_0104704866_p119271159105217"></a><a name="zh-cn_topic_0104704866_p119271159105217"></a>默认为200，若ClientPort配置5000，则表示在5000~5199端口中随机占用。</p>
        </td>
        </tr>
        </tbody>
        </table>


4.  修改云监控指标采集模块的配置文件conf\_ces.json。
    1.  执行以下命令，打开公共配置文件conf\_ces.json。

        **vi conf\_ces.json**

    2.  修改文件中的参数，具体参数请参见[表2](#zh-cn_topic_0104704866_table1746442112492)。

        ```
        {
           "Endpoint": "https://ces.cn-north-1.myhwclouds.com"
        }
        ```

        **表 2**  参数说明

        <a name="zh-cn_topic_0104704866_table1746442112492"></a>
        <table><thead align="left"><tr id="zh-cn_topic_0104704866_row1246422164919"><th class="cellrowborder" valign="top" width="34%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0104704866_p74641021114916"><a name="zh-cn_topic_0104704866_p74641021114916"></a><a name="zh-cn_topic_0104704866_p74641021114916"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="66%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0104704866_p1146442113496"><a name="zh-cn_topic_0104704866_p1146442113496"></a><a name="zh-cn_topic_0104704866_p1146442113496"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="zh-cn_topic_0104704866_row1246410215494"><td class="cellrowborder" valign="top" width="34%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0104704866_p8464122154910"><a name="zh-cn_topic_0104704866_p8464122154910"></a><a name="zh-cn_topic_0104704866_p8464122154910"></a>Endpoint</p>
        </td>
        <td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704866_p246432116499"><a name="zh-cn_topic_0104704866_p246432116499"></a><a name="zh-cn_topic_0104704866_p246432116499"></a>BMS实例所属区域的云监控Endpoint URL。例如：BMS实例所属区域为“华北-北京一”，则URL中使用“ces.cn-north-1.myhwclouds.com”，其他区域的Endpoint取值详见<a href="http://developer.huaweicloud.com/endpoint.html" target="_blank" rel="noopener noreferrer">http://developer.huaweicloud.com/endpoint.html</a>。</p>
        </td>
        </tr>
        </tbody>
        </table>


5.  （可选）配置软RAID监控插件。

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >软RAID名称必须以md开头，否则监控页面无法显示监控项名称。  

    1.  新建文件夹。

        **mkdir /usr/local/telescope/plugins/**

    2.  进入文件夹。

        **cd /usr/local/telescope/plugins/**

    3.  获取监控插件脚本。

        **wget** _http://obs.myhwclouds.com/obs-bms-agent/_**raid\_monitor.sh**

    4.  修改文件权限。

        **chmod 755 raid\_monitor.sh**

    5.  新建配置文件。

        **vi /usr/local/telescope/plugins/conf.json**，内容如下：

        ```
        {
          "plugins": [
            {
              "path": "/usr/local/telescope/plugins/raid_monitor.sh",
              "crontime": 10
            }
          ]
        }
        ```

        其中，“path”为插件路径，“crontime”为指标采集周期（单位：秒）。

        完成配置文件编辑后，执行**service telescoped restart**命令重启服务。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   插件采集周期必须是不小于10的整数。对于小于10秒的配置，插件采用默认值10秒；若采集周期配置非整数，软RAID指标采集异常。  
        >-   插件路径path请勿私自修改，否则软RAID指标采集异常。  



