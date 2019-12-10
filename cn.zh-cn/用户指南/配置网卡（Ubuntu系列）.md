# 配置网卡（Ubuntu系列）<a name="bms_01_0062"></a>

下面以Ubuntu 16.04 LTS \(Xenial Xerus x86\_64\)操作系统为例，举例介绍裸金属服务器增删VPC网卡的配置方法。

>![](public_sys-resources/icon-note.gif) **说明：**   
>Ubuntu系列其他操作系统的配置方法与Ubuntu 16.04 LTS \(Xenial Xerus x86\_64\)类似。  

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
    <a name="ol14133135462114"></a><a name="ol14133135462114"></a><ol id="ol14133135462114"><li>在裸金属服务器页面，单击待配置网卡的裸金属服务器名称。</li><li id="li58541779231"><a name="li58541779231"></a><a name="li58541779231"></a>选择“网卡”页签，在新增的VPC网卡所在行，单击<a name="image733261764518"></a><a name="image733261764518"></a><span><img id="image733261764518" src="figures/7-4.png"></span>，展开网卡详情。</li><li>获取“VLAN”信息、“MAC地址”。</li></ol>
    </td>
    <td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.4.1.3 "><p id="p1569683715512"><a name="p1569683715512"></a><a name="p1569683715512"></a>2847</p>
    <p id="p2086519914612"><a name="p2086519914612"></a><a name="p2086519914612"></a>fa:16:3e:a2:aa:65</p>
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

2.  以“root”用户，使用密钥或密码登录裸金属服务器。
3.  在“/etc/network/interfaces.d/”目录中查看是否含有“/etc/network/interfaces.d/70-cloud-init.cfg”文件。
    -   若含有，执行[5](#li27700107517)。
    -   若没有，执行[4](#li05281426185416)。

4.  <a name="li05281426185416"></a>执行以下命令，生成“/etc/network/interfaces.d/70-cloud-init.cfg”文件并设置文件权限。

    **touch** **/etc/network/interfaces.d/70-cloud-init.cfg**

    **chmod** **644** **/etc/network/interfaces.d/70-cloud-init.cfg**

5.  <a name="li27700107517"></a>执行以下命令，编辑“/etc/network/interfaces.d/70-cloud-init.cfg”，在文件后面配置新增的网卡信息。

    **vim** ****/etc/network/interfaces.d/70-cloud-init.cfg****

    按以下格式编辑：

    ```
    auto bond0.2847
    iface bond0.2847 inet dhcp
    mtu 8888
    hwaddress fa:16:3e:a2:aa:65
    vlan-raw-device bond0
    ```

    其中所需的信息在[1](#li1558174719483)中已经获取。

    -   _bond0.2847_为新增VPC网卡的名称，bond0为固定值，后面的数字为新增网卡的VLAN信息。
    -   hwaddress为新增网卡的的MAC地址。
    -   vlan-raw-device取值当前默认为bond0。

    修改完成后，按“Esc”，输入**:wq**保存并退出。

6.  执行以下命令，启动新增的VPC网卡。

    ****ifup**** ****bond0**.**_vlan_

    例如，启动“bond0.2847”，执行****ifup**** ****bond0**.2847**。

7.  执行以下命令，查看网卡设备的状态。

    **ip** **link**

    ![](figures/17.png)

8.  通过指定新增的网络设备ping其网关，验证网络是否正常。

    其中，网关为[1](#li1558174719483)中获取的网关地址。

    ![](figures/18.png)


## 删除网卡<a name="section5744173334810"></a>

1.  <a name="li960312341080"></a>获取待删除VPC网卡的VLAN和MAC地址。
2.  以“root”用户，使用密钥或密码登录裸金属服务器。
3.  根据VLAN信息找到网络设备，然后执行命令关闭并删除网络设备。

    ```
    root@ubuntu:~# ip link | grep 2847
    9: bond0.2847@bond0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8888 qdisc noqueue state UP mode DEFAULT group default qlen 1000
    root@ubuntu:~# ifconfig bond0.2847 down
    root@ubuntu:~# ip link delete bond0.2847
    ```

4.  裸金属服务器添加VPC网卡后是否进行过重装OS操作。
    -   若无，执行[5](#li4483427910)。
    -   否则执行[9](#li9305111119230)。

5.  <a name="li4483427910"></a>执行以下命令，将网卡配置文件“/etc/network/interfaces.d/70-cloud-init.cfg”拷贝为“/etc/network/interfaces.d/70-cloud-init.cfg.bak”, 进行网络配置备份。

    **cp** **-p** **/etc/network/interfaces.d/70-cloud-init.cfg** **/etc/network/interfaces.d/70-cloud-init.cfg.bak**

6.  执行以下命令，编辑“/etc/network/interfaces.d/70-cloud-init.cfg”，根据[1](#li960312341080)中获取的VLAN和MAC地址找到需要删除的网卡，然后在文件中删除相关的网卡信息。

    **vim** **/etc/network/interfaces.d/70-cloud-init.cfg**

    ```
    # 以下为需要删除的内容
    auto bond0.2847
    iface bond0.2847 inet dhcp
    mtu 8888
    hwaddress fa:16:3e:a2:aa:65
    vlan-raw-device bond0
    ```

    修改完成后，按“Esc”，输入**:wq**保存并退出。

7.  删除网卡后，若“/etc/network/interfaces.d/70-cloud-init.cfg”中无其他网卡信息，可以执行如下命令删除“/etc/network/interfaces.d/70-cloud-init.cfg”文件。

    **rm** **/etc/network/interfaces.d/70-cloud-init.cfg**

8.  验证其他网卡是否正常。若正常，删除“/etc/network/interfaces.d/70-cloud-init.cfg.bak”备份文件，执行结束。

    **rm** **/etc/network/interfaces.d/70-cloud-init.cfg.bak**

9.  <a name="li9305111119230"></a>执行以下命令，将网卡配置文件“/etc/network/interfaces.d/50-cloud-init.cfg”拷贝为“/etc/network/interfaces.d/50-cloud-init.cfg.bak”, 进行网络配置备份。

    **cp** **-p** **/etc/network/interfaces.d/50-cloud-init.cfg** **/etc/network/interfaces.d/50-cloud-init.cfg.bak**

10. 执行以下命令，编辑“/etc/network/interfaces.d/50-cloud-init.cfg”，根据[1](#li960312341080)中获取的VLAN和MAC地址找到需要删除的网卡，然后在文件中删除相关的网卡信息。

    **vim** **/etc/network/interfaces.d/50-cloud-init.cfg**

    ```
    # 以下为需要删除的内容
    auto bond0.2847
    iface bond0.2847 inet dhcp
    mtu 8888
    hwaddress fa:16:3e:a2:aa:65
    vlan-raw-device bond0
    ```

    修改完成后，按“Esc”，输入**:wq**保存并退出。

11. 验证其他VPC网卡是否正常。若正常，删除“/etc/network/interfaces.d/50-cloud-init.cfg.bak”备份文件，执行结束。

    **rm** **/etc/network/interfaces.d/50-cloud-init.cfg.bak**


