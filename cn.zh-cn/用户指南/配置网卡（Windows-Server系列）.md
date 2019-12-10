# 配置网卡（Windows Server系列）<a name="bms_01_0063"></a>

下面以Windows Server 2012 R2 Standard操作系统为例，举例介绍裸金属服务器增删VPC网卡的配置方法。

>![](public_sys-resources/icon-note.gif) **说明：**   
>Windows Server系列其他操作系统的配置方法与Windows Server 2012 R2 Standard类似。  

## 增加网卡<a name="section208961921154819"></a>

1.  <a name="li1558174719483"></a>获取新增网卡的信息，如[表1](#table1669415379510)所示。

    **表 1**  信息收集

    <a name="table1669415379510"></a>
    <table><thead align="left"><tr id="row1669543725112"><th class="cellrowborder" valign="top" width="18.181818181818183%" id="mcps1.2.4.1.1"><p id="p369643735111"><a name="p369643735111"></a><a name="p369643735111"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.63636363636363%" id="mcps1.2.4.1.2"><p id="p18696537135118"><a name="p18696537135118"></a><a name="p18696537135118"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.181818181818183%" id="mcps1.2.4.1.3"><p id="p1969613379517"><a name="p1969613379517"></a><a name="p1969613379517"></a>样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15696143715112"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.4.1.1 "><p id="p4696193725113"><a name="p4696193725113"></a><a name="p4696193725113"></a>VLAN、MAC地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.63636363636363%" headers="mcps1.2.4.1.2 "><p id="p2696143775114"><a name="p2696143775114"></a><a name="p2696143775114"></a>VPC网卡的VLAN信息和MAC地址，获取方式如下：</p>
    <a name="ol14133135462114"></a><a name="ol14133135462114"></a><ol id="ol14133135462114"><li>在裸金属服务器页面，单击待配置网卡的裸金属服务器名称。</li><li id="li58541779231"><a name="li58541779231"></a><a name="li58541779231"></a>选择“网卡”页签，在新增的VPC网卡所在行，单击<a name="image733261764518"></a><a name="image733261764518"></a><span><img id="image733261764518" src="figures/7-5.png"></span>，展开网卡详情。</li><li>获取“VLAN”信息、“MAC地址”。</li></ol>
    </td>
    <td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.4.1.3 "><p id="p1569683715512"><a name="p1569683715512"></a><a name="p1569683715512"></a>2812</p>
    <p id="p2086519914612"><a name="p2086519914612"></a><a name="p2086519914612"></a>fa:16:3e:15:38:07</p>
    </td>
    </tr>
    <tr id="row1269673714515"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.4.1.1 "><p id="p13696183735110"><a name="p13696183735110"></a><a name="p13696183735110"></a>网关</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.63636363636363%" headers="mcps1.2.4.1.2 "><p id="p4696103719515"><a name="p4696103719515"></a><a name="p4696103719515"></a>VPC网卡的网关地址，获取方式如下：</p>
    <a name="ol1433103653118"></a><a name="ol1433103653118"></a><ol id="ol1433103653118"><li id="li32431027104614"><a name="li32431027104614"></a><a name="li32431027104614"></a>在<a href="#li58541779231">2</a>中的网卡详情页面，获取“子网”信息。</li><li>在裸金属服务器详情页面，单击虚拟私有云后的链接，跳转至VPC列表。</li><li>单击裸金属服务器所属VPC的名称，进入VPC详情页面。</li><li>单击“子网”页签，找到<a href="#li32431027104614">1</a>中的子网所对应的网关地址。</li></ol>
    </td>
    <td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.4.1.3 "><p id="p9696173714518"><a name="p9696173714518"></a><a name="p9696173714518"></a>192.168.1.1</p>
    </td>
    </tr>
    </tbody>
    </table>

2.  登录Windows裸金属服务器。
3.  进入裸金属服务器的Windows PowerShell命令行界面，执行以下命令，查询网卡信息是否有Team1（VPC网络的端口组名称）。

    **Get-NetAdapter**

    -   若有，执行[4](#li27700107517)。
    -   若没有，请联系客服。

    返回信息示例如下：

    ![](figures/20.png)

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其中，“eth0”和“eth1”为承载VPC网络的网络设备。  

4.  <a name="li27700107517"></a>执行以下命令，添加VPC网卡。

    **Add-NetLbfoTeamNIC** **-Team** **"Team1"** **-VlanID** _vlan\_id_ **-Name** **"Team1-vlan-**_vlan\_id_**"** **-Confirm:$false**

    **Set-NetAdapter** **-Name** **"Team1-vlan-**_vlan\_id_**"** **-MacAddress** **"mac\_addr"** **-Confirm:$false**

    其中，“Team1”为VPC网络的端口组名称， vlan\_id为[1](#li1558174719483)中获取的VLAN信息，如2812，mac\_addr为[1](#li1558174719483)中获取的MAC地址，如fa:16:3e:15:38:07。

    ![](figures/21.png)

5.  执行以下命令，查看VPC网卡设备的状态。

    **Get-NetAdapter**

    返回信息示例如下：

    ![](figures/23.png)

6.  通过指定新增的网络设备ping其网关，验证网络是否正常。

    其中，新增网络设备Team1-vlan-2812的IPv4地址为：

    ![](figures/24.png)

    网关为[1](#li1558174719483)中获取的网关地址。

    返回信息示例如下：

    ![](figures/25.png)


## 删除网卡<a name="section5744173334810"></a>

1.  <a name="li960312341080"></a>获取待删除VPC网卡的VLAN和MAC地址。
2.  登录Windows裸金属服务器。
3.  进入裸金属服务器的Windows PowerShell命令行界面，执行以下命令，查询需要删除的VPC网卡信息。

    **Get-NetLbfoTeamNIC** **-Team** **Team1**

    ![](figures/26.png)

4.  执行以下命令，删除VPC网卡。

    **Remove-NetLbfoTeamNIC** **-Team** **"Team1"** **-VlanID** _vlan\_id_

    其中，vlan\_id为[1](#li960312341080)中获取的VLAN信息。

    ![](figures/27.png)

5.  执行如下命令，查询网络信息，确认VPC网卡已被删除。

    **Get-NetLbfoTeamNIC** **-Team** **Team1**

    **Get-NetAdapter**

    ![](figures/28.png)


