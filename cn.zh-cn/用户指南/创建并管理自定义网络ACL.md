# 创建并管理自定义网络ACL<a name="ZH-CN_TOPIC_0161727557"></a>

## 创建自定义网络ACL<a name="section6127738485"></a>

每个用户默认可以创建200个自定义网络ACL。

1.  登录管理控制台。
2.  选择“计算 \> 裸金属服务器”。

    进入裸金属服务器页面。

3.  在“自定义网络”页签中，选择“自定义网络ACL”并单击“创建自定义网络ACL”。
4.  输入名称、描述，单击“确定”。
5.  创建成功后，自定义网络ACL列表中增加一条记录。

## 添加入/出方向规则<a name="section128685618819"></a>

您可根据自身网络需求，在出方向和入方向添加相应规则。

1.  在裸金属服务器页面，单击“自定义网络”页签，选择“自定义网络ACL”。
2.  单击待添加规则的自定义网络ACL名称，进入自定义网络ACL详情页面。
3.  在入方向规则或出方向规则页签，单击“添加规则”，添加入方向或出方向规则。

    单击“+”可以依次增加多条规则。

    **表 1**  参数说明

    <a name="table53776177585"></a>
    <table><thead align="left"><tr id="row237820178581"><th class="cellrowborder" valign="top" width="18.61186118611861%" id="mcps1.2.4.1.1"><p id="p037821765815"><a name="p037821765815"></a><a name="p037821765815"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="54.88548854885489%" id="mcps1.2.4.1.2"><p id="p7378131710589"><a name="p7378131710589"></a><a name="p7378131710589"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.502650265026507%" id="mcps1.2.4.1.3"><p id="p18378317155811"><a name="p18378317155811"></a><a name="p18378317155811"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5378141755817"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p9378141711587"><a name="p9378141711587"></a><a name="p9378141711587"></a>策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p153781317195820"><a name="p153781317195820"></a><a name="p153781317195820"></a>自定义网络ACL策略。必选项，单击下拉按钮可选择。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p20378131715582"><a name="p20378131715582"></a><a name="p20378131715582"></a>允许</p>
    </td>
    </tr>
    <tr id="row113781117155817"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p43781617175815"><a name="p43781617175815"></a><a name="p43781617175815"></a>协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p1378161785817"><a name="p1378161785817"></a><a name="p1378161785817"></a>自定义网络ACL支持的协议。必选项，单击下拉按钮可选择。目前只支持选择TCP、UDP、ICMP、全部协议。当选择ICMP或者全部时，端口信息不可填写。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p1137851713589"><a name="p1137851713589"></a><a name="p1137851713589"></a>TCP</p>
    </td>
    </tr>
    <tr id="row2037913177582"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p33796174585"><a name="p33796174585"></a><a name="p33796174585"></a>源地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p73791117165811"><a name="p73791117165811"></a><a name="p73791117165811"></a>此方向允许的源地址。</p>
    <p id="p18556334549"><a name="p18556334549"></a><a name="p18556334549"></a>默认值为0.0.0.0/0，代表支持所有的IP地址。</p>
    <p id="p1219645618419"><a name="p1219645618419"></a><a name="p1219645618419"></a>例如：</p>
    <p id="p25741611556"><a name="p25741611556"></a><a name="p25741611556"></a>xxx.xxx.xxx.xxx/32（IP地址）</p>
    <p id="p66883501454"><a name="p66883501454"></a><a name="p66883501454"></a>xxx.xxx.xxx.0/24（子网）</p>
    <p id="p18163114966"><a name="p18163114966"></a><a name="p18163114966"></a>0.0.0.0/0（任意地址）</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p18379617125816"><a name="p18379617125816"></a><a name="p18379617125816"></a>0.0.0.0/0</p>
    </td>
    </tr>
    <tr id="row937971705818"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p837918178581"><a name="p837918178581"></a><a name="p837918178581"></a>源端口范围</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p8379201712583"><a name="p8379201712583"></a><a name="p8379201712583"></a>源端口范围，取值范围是1~65535的数字。表示某一范围时，两个数字必须以短中划线分隔，例如：1-100。</p>
    <p id="p2193381275"><a name="p2193381275"></a><a name="p2193381275"></a>选择TCP或UDP协议时必须填写。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p19379101712588"><a name="p19379101712588"></a><a name="p19379101712588"></a>22或22-30</p>
    </td>
    </tr>
    <tr id="row737931711588"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p193791017185818"><a name="p193791017185818"></a><a name="p193791017185818"></a>目的地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p937916175584"><a name="p937916175584"></a><a name="p937916175584"></a>此方向允许的目的地址。</p>
    <p id="p12504122815917"><a name="p12504122815917"></a><a name="p12504122815917"></a>默认值为0.0.0.0/0，代表支持所有的IP地址。</p>
    <p id="p9504162811915"><a name="p9504162811915"></a><a name="p9504162811915"></a>例如：</p>
    <p id="p13504128394"><a name="p13504128394"></a><a name="p13504128394"></a>xxx.xxx.xxx.xxx/32（IP地址）</p>
    <p id="p85043281491"><a name="p85043281491"></a><a name="p85043281491"></a>xxx.xxx.xxx.0/24（子网）</p>
    <p id="p75047281491"><a name="p75047281491"></a><a name="p75047281491"></a>0.0.0.0/0（任意地址）</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p18379917135812"><a name="p18379917135812"></a><a name="p18379917135812"></a>0.0.0.0/0</p>
    </td>
    </tr>
    <tr id="row20379171714584"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p10379117195819"><a name="p10379117195819"></a><a name="p10379117195819"></a>目的端口范围</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p1166811291122"><a name="p1166811291122"></a><a name="p1166811291122"></a>目的端口范围，取值范围是1~65535的数字。表示某一范围时，两个数字必须以短中划线分隔，例如：1-100。</p>
    <p id="p1766811294124"><a name="p1766811294124"></a><a name="p1766811294124"></a>选择TCP或UDP协议时必须填写。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p23791117145819"><a name="p23791117145819"></a><a name="p23791117145819"></a>22或22-30</p>
    </td>
    </tr>
    <tr id="row173434529593"><td class="cellrowborder" valign="top" width="18.61186118611861%" headers="mcps1.2.4.1.1 "><p id="p143437520593"><a name="p143437520593"></a><a name="p143437520593"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.88548854885489%" headers="mcps1.2.4.1.2 "><p id="p23432052145916"><a name="p23432052145916"></a><a name="p23432052145916"></a>自定义网络ACL规则的描述信息，非必填项。</p>
    <p id="p1157715115137"><a name="p1157715115137"></a><a name="p1157715115137"></a>描述信息内容不能超过255个字符，且不能包含<span>&lt;</span><span>、</span><span>&gt;</span><span>符号。</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="26.502650265026507%" headers="mcps1.2.4.1.3 "><p id="p4343652185912"><a name="p4343652185912"></a><a name="p4343652185912"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

4.  单击“确定”完成自定义网络ACL规则的添加。

## 关联自定义子网<a name="section113777104910"></a>

当用户需进行子网关联时，可进入该自定义网络ACL详情页面的“关联自定义子网”页签。关联子网后，自定义网络ACL默认拒绝裸金属服务器所有出入子网的流量，直至添加放通规则。

1.  在裸金属服务器页面，单击“自定义网络”页签，选择“自定义网络ACL”。
2.  单击待关联自定义子网的自定义网络ACL名称，进入自定义网络ACL详情页面。
3.  在“关联子网”页签，单击“关联”，弹出“关联子网”窗口。

    **图 1**  关联子网<a name="fig424103515311"></a>  
    ![](figures/关联子网.png "关联子网")

4.  勾选需要进行关联的自定义子网，单击“确定”，完成自定义子网关联。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >已关联自定义网络ACL的自定义子网将不会展示在关联自定义子网页面的列表中，即暂不支持一键式解绑自定义子网与关联自定义子网操作，若用户需要关联已绑定自定义网络ACL的自定义子网，需要先解除绑定再进行关联。


