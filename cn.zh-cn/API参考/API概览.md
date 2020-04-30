# API概览<a name="ZH-CN_TOPIC_0113746486"></a>

## 接口介绍<a name="section1852025323614"></a>

裸金属服务器所提供的接口分为BMS接口与OpenStack原生接口。

通过配合使用BMS服务提供的接口和OpenStack原生接口，您可以完整地使用裸金属服务器的所有功能。例如创建裸金属服务器实例，可以使用OpenStack原生接口，也可以使用BMS接口进行创建。

**表 1**  接口说明

<a name="table9334665555"></a>
<table><thead align="left"><tr id="row153368665516"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.4.1.1"><p id="p1133713655517"><a name="p1133713655517"></a><a name="p1133713655517"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.2"><p id="p19339862553"><a name="p19339862553"></a><a name="p19339862553"></a>子类型</p>
</th>
<th class="cellrowborder" valign="top" width="64%" id="mcps1.2.4.1.3"><p id="p1034013665517"><a name="p1034013665517"></a><a name="p1034013665517"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row153421662553"><td class="cellrowborder" rowspan="10" valign="top" width="17%" headers="mcps1.2.4.1.1 "><p id="p13344767552"><a name="p13344767552"></a><a name="p13344767552"></a>BMS接口</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.2 "><p id="p134513665511"><a name="p134513665511"></a><a name="p134513665511"></a><a href="查询API版本信息.md">查询API版本信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="64%" headers="mcps1.2.4.1.3 "><p id="p934556145517"><a name="p934556145517"></a><a name="p934556145517"></a>查询裸金属服务当前所用的API版本。</p>
</td>
</tr>
<tr id="row2345166115515"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p73469616550"><a name="p73469616550"></a><a name="p73469616550"></a><a href="裸金属服务器生命周期管理.md">生命周期管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p123461564553"><a name="p123461564553"></a><a name="p123461564553"></a>可以实现包周期<span id="text49901016638"><a name="text49901016638"></a><a name="text49901016638"></a>裸金属服务器</span><span id="text109901116731"><a name="text109901116731"></a><a name="text109901116731"></a></span>的创建、<span id="text109869383714"><a name="text109869383714"></a><a name="text109869383714"></a>裸金属服务器</span><span id="text29868313715"><a name="text29868313715"></a><a name="text29868313715"></a></span>详情查询等操作。</p>
</td>
</tr>
<tr id="row71441405579"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p13144170195717"><a name="p13144170195717"></a><a name="p13144170195717"></a><a href="裸金属服务器状态管理.md">状态管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p191441902579"><a name="p191441902579"></a><a name="p191441902579"></a><span id="text56814195314"><a name="text56814195314"></a><a name="text56814195314"></a>裸金属服务器</span><span id="text13681119239"><a name="text13681119239"></a><a name="text13681119239"></a></span>修改名称、重装系统、启动、重启、关闭等功能。</p>
</td>
</tr>
<tr id="row14577541105614"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p157734185612"><a name="p157734185612"></a><a name="p157734185612"></a><a href="裸金属服务器规格管理.md">规格管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p3577641145617"><a name="p3577641145617"></a><a name="p3577641145617"></a>用于查询<span id="text251919214313"><a name="text251919214313"></a><a name="text251919214313"></a>裸金属服务器</span><span id="text105198211734"><a name="text105198211734"></a><a name="text105198211734"></a></span>的规格详情和规格扩展信息，比如规格ID、规格名称、CPU核数、启动源。</p>
</td>
</tr>
<tr id="row103464620555"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1346564551"><a name="p1346564551"></a><a name="p1346564551"></a><a href="裸金属服务器网卡管理.md">网卡管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p222805111129"><a name="p222805111129"></a><a name="p222805111129"></a>可以查询<span id="text672810237319"><a name="text672810237319"></a><a name="text672810237319"></a>裸金属服务器</span><span id="text12728102317311"><a name="text12728102317311"></a><a name="text12728102317311"></a></span>网卡信息，比如网卡的IP地址、MAC地址。</p>
</td>
</tr>
<tr id="row146421313171420"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p166421813121411"><a name="p166421813121411"></a><a name="p166421813121411"></a><a href="裸金属服务器云硬盘管理.md">云硬盘管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p2642213111418"><a name="p2642213111418"></a><a name="p2642213111418"></a><span id="text5209152515315"><a name="text5209152515315"></a><a name="text5209152515315"></a>裸金属服务器</span><span id="text52091525937"><a name="text52091525937"></a><a name="text52091525937"></a></span>云硬盘挂载、卸载，以及挂载的磁盘信息查询。</p>
</td>
</tr>
<tr id="row1080851571413"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p122893414147"><a name="p122893414147"></a><a name="p122893414147"></a><a href="裸金属服务器元数据管理.md">元数据管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p540515534142"><a name="p540515534142"></a><a name="p540515534142"></a><span id="text1879010339328"><a name="text1879010339328"></a><a name="text1879010339328"></a>裸金属服务器</span><span id="text187901330328"><a name="text187901330328"></a><a name="text187901330328"></a></span>元数据包含了<span id="text15790173313218"><a name="text15790173313218"></a><a name="text15790173313218"></a>裸金属服务器</span><span id="text2790833193211"><a name="text2790833193211"></a><a name="text2790833193211"></a></span>在云平台的基本信息，例如服务器ID、主机名、网络信息等。您可以更新<span id="text47021291039"><a name="text47021291039"></a><a name="text47021291039"></a>裸金属服务器</span><span id="text1470272919311"><a name="text1470272919311"></a><a name="text1470272919311"></a></span>的元数据。</p>
</td>
</tr>
<tr id="row842719131413"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p13428192145"><a name="p13428192145"></a><a name="p13428192145"></a><a href="裸金属服务器租户配额管理.md">租户配额管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p9420199148"><a name="p9420199148"></a><a name="p9420199148"></a>查询某租户名下，所有资源的配额信息，包括已使用配额。</p>
</td>
</tr>
<tr id="row151478231164"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p0147172331616"><a name="p0147172331616"></a><a name="p0147172331616"></a><a href="裸金属服务器密码管理.md">密码管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p16147823201620"><a name="p16147823201620"></a><a name="p16147823201620"></a>查询是否支持一键重置密码，如果支持，您可以对<span id="text17420635364"><a name="text17420635364"></a><a name="text17420635364"></a>裸金属服务器</span><span id="text1442016311360"><a name="text1442016311360"></a><a name="text1442016311360"></a></span>重置密码。还包括Windows<span id="text18259159193414"><a name="text18259159193414"></a><a name="text18259159193414"></a>裸金属服务器</span><span id="text172591359173417"><a name="text172591359173417"></a><a name="text172591359173417"></a></span>的密码获取与清除。</p>
</td>
</tr>
<tr id="row1134814625515"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p034812625510"><a name="p034812625510"></a><a name="p034812625510"></a><a href="Job管理.md">查询Job状态</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p11361165261112"><a name="p11361165261112"></a><a name="p11361165261112"></a>对于创建<span id="zh-cn_topic_0118696596_text11602822115310"><a name="zh-cn_topic_0118696596_text11602822115310"></a><a name="zh-cn_topic_0118696596_text11602822115310"></a>裸金属服务器</span><span id="zh-cn_topic_0118696596_text1060218229533"><a name="zh-cn_topic_0118696596_text1060218229533"></a><a name="zh-cn_topic_0118696596_text1060218229533"></a></span>、挂卸卷等异步API，命令下发后，会返回“job_id”，通过“job_id”可以查询任务的执行状态。</p>
</td>
</tr>
<tr id="row723410891820"><td class="cellrowborder" rowspan="9" valign="top" width="17%" headers="mcps1.2.4.1.1 "><p id="p593922418413"><a name="p593922418413"></a><a name="p593922418413"></a>OpenStack原生接口（v2.1版本）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.2 "><p id="p1268143210442"><a name="p1268143210442"></a><a name="p1268143210442"></a><a href="裸金属服务器生命周期管理-0.md">生命周期管理</a></p>
</td>
<td class="cellrowborder" valign="top" width="64%" headers="mcps1.2.4.1.3 "><p id="p132344820187"><a name="p132344820187"></a><a name="p132344820187"></a>查询类接口，包括查询<span id="text5418544472"><a name="text5418544472"></a><a name="text5418544472"></a>裸金属服务器</span><span id="text11418544672"><a name="text11418544672"></a><a name="text11418544672"></a></span>详情、查询<span id="text124182446719"><a name="text124182446719"></a><a name="text124182446719"></a>裸金属服务器</span><span id="text54188446718"><a name="text54188446718"></a><a name="text54188446718"></a></span>列表、查询<span id="text4418944878"><a name="text4418944878"></a><a name="text4418944878"></a>裸金属服务器</span><span id="text54183441575"><a name="text54183441575"></a><a name="text54183441575"></a></span>详情信息列表。</p>
</td>
</tr>
<tr id="row9353566558"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p36811832124410"><a name="p36811832124410"></a><a name="p36811832124410"></a><a href="裸金属服务器状态管理-1.md">状态管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p153576685510"><a name="p153576685510"></a><a name="p153576685510"></a>状态管理接口，包括对<span id="text183732721119"><a name="text183732721119"></a><a name="text183732721119"></a>裸金属服务器</span><span id="text1883702713116"><a name="text1883702713116"></a><a name="text1883702713116"></a></span>的启动、重启、关闭等接口。</p>
</td>
</tr>
<tr id="row77791614337"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1582719815330"><a name="p1582719815330"></a><a name="p1582719815330"></a><a href="裸金属服务器元数据管理-2.md">元数据管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p182798113316"><a name="p182798113316"></a><a name="p182798113316"></a><span id="text4751115023314"><a name="text4751115023314"></a><a name="text4751115023314"></a>裸金属服务器</span><span id="text20751185013336"><a name="text20751185013336"></a><a name="text20751185013336"></a></span>元数据包含了<span id="text1820815593317"><a name="text1820815593317"></a><a name="text1820815593317"></a>裸金属服务器</span><span id="text420825519334"><a name="text420825519334"></a><a name="text420825519334"></a></span>在云平台的基本信息，例如服务器ID、主机名、网络信息等。您可以查询、更新、删除<span id="text2827381336"><a name="text2827381336"></a><a name="text2827381336"></a>裸金属服务器</span><span id="text282714813333"><a name="text282714813333"></a><a name="text282714813333"></a></span>的元数据。</p>
</td>
</tr>
<tr id="row1135816125517"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p18682183213443"><a name="p18682183213443"></a><a name="p18682183213443"></a><a href="裸金属服务器IP地址查询.md">IP信息查询</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p7360560559"><a name="p7360560559"></a><a name="p7360560559"></a>查询<span id="text1883323118273"><a name="text1883323118273"></a><a name="text1883323118273"></a>裸金属服务器</span><span id="text1083363120275"><a name="text1083363120275"></a><a name="text1083363120275"></a></span>的私有IP地址信息，包括IP地址版本（IPv4或者IPv6）和具体的IP地址。</p>
</td>
</tr>
<tr id="row2360262554"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1682153211444"><a name="p1682153211444"></a><a name="p1682153211444"></a><a href="裸金属服务器规格查询.md">裸金属服务器规格查询</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><a name="ul142971456162316"></a><a name="ul142971456162316"></a><ul id="ul142971456162316"><li><a href="查询裸金属服务器规格信息列表（OpenStack原生）.md">查询裸金属服务器规格信息列表</a>：查询系统中的所有规格，或者指定过滤条件检索需要的规格。</li><li><a href="查询裸金属服务器规格详情（OpenStack原生）.md">查询裸金属服务器规格详情</a>：根据<span id="text229795611239"><a name="text229795611239"></a><a name="text229795611239"></a>裸金属服务器</span><span id="text1729705612237"><a name="text1729705612237"></a><a name="text1729705612237"></a></span>的规格ID，查询规格的详细信息，比如规格名称、CPU核数、内存大小等。</li><li><a href="查询裸金属服务器规格extra_specs参数的详情（OpenStack原生）.md">查询裸金属服务器规格extra_specs参数的详情</a>：“extra_specs”参数用于描述<span id="text029718569236"><a name="text029718569236"></a><a name="text029718569236"></a>裸金属服务器</span><span id="text3297105672319"><a name="text3297105672319"></a><a name="text3297105672319"></a></span>规格的键值对，如果您想确认某个规格是否支持快速发放，可以调用该接口进行查询。</li></ul>
</td>
</tr>
<tr id="row736386195512"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1368293214419"><a name="p1368293214419"></a><a name="p1368293214419"></a><a href="裸金属服务器网卡管理-3.md">裸金属服务器网卡查询</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p21001243131316"><a name="p21001243131316"></a><a name="p21001243131316"></a>您可以查询<span id="text182401259121312"><a name="text182401259121312"></a><a name="text182401259121312"></a>裸金属服务器</span><span id="text13240459121311"><a name="text13240459121311"></a><a name="text13240459121311"></a></span>的所有网卡；或者根据网卡ID，查询某一个网卡的详细信息，比如网卡的IP地址、MAC地址。</p>
</td>
</tr>
<tr id="row93661067558"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p5682153244415"><a name="p5682153244415"></a><a name="p5682153244415"></a><a href="裸金属服务器云硬盘管理-4.md">云硬盘管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p20367136135519"><a name="p20367136135519"></a><a name="p20367136135519"></a>您可以查询<span id="text2567161771713"><a name="text2567161771713"></a><a name="text2567161771713"></a>裸金属服务器</span><span id="text1256721711713"><a name="text1256721711713"></a><a name="text1256721711713"></a></span>所挂载的云硬盘信息；或者根据磁盘ID，查询<span id="text181941623101710"><a name="text181941623101710"></a><a name="text181941623101710"></a>裸金属服务器</span><span id="text71941023141716"><a name="text71941023141716"></a><a name="text71941023141716"></a></span>挂载的某个云硬盘信息，比如挂载目录。</p>
</td>
</tr>
<tr id="row1536716165511"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1768212329441"><a name="p1768212329441"></a><a name="p1768212329441"></a><a href="裸金属服务器SSH密钥管理.md">SSH密钥管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p6367366557"><a name="p6367366557"></a><a name="p6367366557"></a>查询SSH密钥信息列表、详情，创建、删除SSH密钥等功能。</p>
</td>
</tr>
<tr id="row136718614556"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1368211325448"><a name="p1368211325448"></a><a name="p1368211325448"></a><a href="裸金属服务器一维标签管理.md">一维标签管理</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p33694616557"><a name="p33694616557"></a><a name="p33694616557"></a><span id="text284320511410"><a name="text284320511410"></a><a name="text284320511410"></a>裸金属服务器</span><span id="text1184465149"><a name="text1184465149"></a><a name="text1184465149"></a></span>一维标签的增删改查。</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   使用BMS提供的接口时，您需要使用BMS服务自身的Endpoint。  
>-   使用OpenStack原生接口时，您需要使用ECS服务注册的Endpoint。  
>-   当前版本调用OpenStack接口不支持HTTP长连接。  

## BMS接口使用限制<a name="section1016613793716"></a>

**表 2**  BMS接口使用限制

<a name="table1613518385619"></a>
<table><thead align="left"><tr id="row131354381261"><th class="cellrowborder" valign="top" width="15.14%" id="mcps1.2.5.1.1"><p id="p1573014512620"><a name="p1573014512620"></a><a name="p1573014512620"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="22.400000000000002%" id="mcps1.2.5.1.2"><p id="p177331245262"><a name="p177331245262"></a><a name="p177331245262"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="31.630000000000003%" id="mcps1.2.5.1.3"><p id="p11735193693511"><a name="p11735193693511"></a><a name="p11735193693511"></a>URI</p>
</th>
<th class="cellrowborder" valign="top" width="30.830000000000002%" id="mcps1.2.5.1.4"><p id="p127381245567"><a name="p127381245567"></a><a name="p127381245567"></a>使用限制</p>
</th>
</tr>
</thead>
<tbody><tr id="row1913533810613"><td class="cellrowborder" rowspan="2" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p833617536610"><a name="p833617536610"></a><a name="p833617536610"></a>查询API版本信息</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p934214532615"><a name="p934214532615"></a><a name="p934214532615"></a><a href="查询API版本信息列表.md">查询API版本信息列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p1815213923615"><a name="p1815213923615"></a><a name="p1815213923615"></a>GET /</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p4347125319619"><a name="p4347125319619"></a><a name="p4347125319619"></a>每分钟2000次</p>
</td>
</tr>
<tr id="row1313518389611"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p12359953669"><a name="p12359953669"></a><a name="p12359953669"></a><a href="查询指定API版本信息.md">查询指定API版本信息</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p121521339173620"><a name="p121521339173620"></a><a name="p121521339173620"></a>GET /{api_version}</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p53608531167"><a name="p53608531167"></a><a name="p53608531167"></a>每分钟2000次</p>
</td>
</tr>
<tr id="row181355382617"><td class="cellrowborder" rowspan="3" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p12365553968"><a name="p12365553968"></a><a name="p12365553968"></a>生命周期管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p1773195117576"><a name="p1773195117576"></a><a name="p1773195117576"></a><a href="创建裸金属服务器.md">创建裸金属服务器</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p8153143973618"><a name="p8153143973618"></a><a name="p8153143973618"></a>POST /v1/{project_id}/baremetalservers</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p1037117534619"><a name="p1037117534619"></a><a name="p1037117534619"></a>每分钟50次</p>
</td>
</tr>
<tr id="row13135163817619"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p187741051165716"><a name="p187741051165716"></a><a name="p187741051165716"></a><a href="查询裸金属服务器详情.md">查询裸金属服务器详情</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p171531739193620"><a name="p171531739193620"></a><a name="p171531739193620"></a>GET /v1/{project_id}/baremetalservers/detail</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p238519531464"><a name="p238519531464"></a><a name="p238519531464"></a>每分钟500次</p>
</td>
</tr>
<tr id="row201371838265"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p20395185313611"><a name="p20395185313611"></a><a name="p20395185313611"></a><a href="查询裸金属服务器详情列表.md">查询裸金属服务器详情列表</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p19153203913369"><a name="p19153203913369"></a><a name="p19153203913369"></a>GET /v1/{project_id}/baremetalservers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p23991532615"><a name="p23991532615"></a><a name="p23991532615"></a>每分钟1000次</p>
</td>
</tr>
<tr id="row1513710382611"><td class="cellrowborder" rowspan="5" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p34200531766"><a name="p34200531766"></a><a name="p34200531766"></a>状态管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p144090531361"><a name="p144090531361"></a><a name="p144090531361"></a><a href="修改裸金属服务器名称.md">修改裸金属服务器名称</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p1515323963613"><a name="p1515323963613"></a><a name="p1515323963613"></a>PUT /v1/{project_id}/baremetalservers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p1141211531767"><a name="p1141211531767"></a><a name="p1141211531767"></a>每分钟100次</p>
</td>
</tr>
<tr id="row1613716384620"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1842213531962"><a name="p1842213531962"></a><a name="p1842213531962"></a><a href="重装裸金属服务器操作系统.md">重装裸金属服务器操作系统</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p16153173920366"><a name="p16153173920366"></a><a name="p16153173920366"></a>POST /v1/{project_id}/baremetalservers/{server_id}/reinstallos</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p144269538616"><a name="p144269538616"></a><a name="p144269538616"></a>每分钟50次</p>
</td>
</tr>
<tr id="row101371381865"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p14323532062"><a name="p14323532062"></a><a name="p14323532062"></a><a href="启动裸金属服务器.md">启动裸金属服务器</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1415343953618"><a name="p1415343953618"></a><a name="p1415343953618"></a>POST /v1/{project_id}/baremetalservers/action</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p343515531767"><a name="p343515531767"></a><a name="p343515531767"></a>每分钟50次</p>
</td>
</tr>
<tr id="row21377381566"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1744310531966"><a name="p1744310531966"></a><a name="p1744310531966"></a><a href="重启裸金属服务器.md">重启裸金属服务器</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p10153133911366"><a name="p10153133911366"></a><a name="p10153133911366"></a>POST /v1/{project_id}/baremetalservers/action</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1744615318613"><a name="p1744615318613"></a><a name="p1744615318613"></a>每分钟50次</p>
</td>
</tr>
<tr id="row1913723817620"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5453353162"><a name="p5453353162"></a><a name="p5453353162"></a><a href="关闭裸金属服务器.md">关闭裸金属服务器</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p7153113913611"><a name="p7153113913611"></a><a name="p7153113913611"></a>POST /v1/{project_id}/baremetalservers/action</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p11455105317612"><a name="p11455105317612"></a><a name="p11455105317612"></a>每分钟50次</p>
</td>
</tr>
<tr id="row16681171320557"><td class="cellrowborder" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p152312531369"><a name="p152312531369"></a><a name="p152312531369"></a>规格管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p8527453266"><a name="p8527453266"></a><a name="p8527453266"></a><a href="查询规格详情和规格扩展信息列表.md">查询规格详情和规格扩展信息列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p61541139183619"><a name="p61541139183619"></a><a name="p61541139183619"></a>GET /v1/{project_id}/baremetalservers/flavors</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p165301453866"><a name="p165301453866"></a><a name="p165301453866"></a>每分钟500次</p>
</td>
</tr>
<tr id="row11441112210551"><td class="cellrowborder" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p11536115316612"><a name="p11536115316612"></a><a name="p11536115316612"></a>网卡管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p35417532620"><a name="p35417532620"></a><a name="p35417532620"></a><a href="查询裸金属服务器网卡信息.md">查询裸金属服务器网卡信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p1115417392369"><a name="p1115417392369"></a><a name="p1115417392369"></a>GET /v1/{project_id}/baremetalservers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p115451553865"><a name="p115451553865"></a><a name="p115451553865"></a>每分钟500次</p>
</td>
</tr>
<tr id="row204331526125519"><td class="cellrowborder" rowspan="3" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p843319264555"><a name="p843319264555"></a><a name="p843319264555"></a>云硬盘管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p1974015383516"><a name="p1974015383516"></a><a name="p1974015383516"></a><a href="裸金属服务器挂载云硬盘.md">裸金属服务器挂载云硬盘</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p515453918364"><a name="p515453918364"></a><a name="p515453918364"></a>POST /v1/{project_id}/baremetalservers/{server_id}/attachvolume</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p75620536610"><a name="p75620536610"></a><a name="p75620536610"></a>每分钟100次</p>
</td>
</tr>
<tr id="row143472615552"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p207409381359"><a name="p207409381359"></a><a name="p207409381359"></a><a href="裸金属服务器卸载云硬盘.md">裸金属服务器卸载云硬盘</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p18154203913615"><a name="p18154203913615"></a><a name="p18154203913615"></a>DELETE /v1/{project_id}/baremetalservers/{server_id}/detachvolume/{attachment_id}</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p5574353867"><a name="p5574353867"></a><a name="p5574353867"></a>每分钟100次</p>
</td>
</tr>
<tr id="row8522631214"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p75222038215"><a name="p75222038215"></a><a name="p75222038215"></a><a href="查询裸金属服务器挂载的云硬盘信息.md">查询裸金属服务器挂载的磁盘信息</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p161541539123617"><a name="p161541539123617"></a><a name="p161541539123617"></a>GET /v1/{project_id}/baremetalservers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p5604185313611"><a name="p5604185313611"></a><a name="p5604185313611"></a>每分钟500次</p>
</td>
</tr>
<tr id="row6506976220"><td class="cellrowborder" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p20612185315618"><a name="p20612185315618"></a><a name="p20612185315618"></a>元数据管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p361765320613"><a name="p361765320613"></a><a name="p361765320613"></a><a href="更新裸金属服务器元数据.md">更新裸金属服务器元数据</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p101542391369"><a name="p101542391369"></a><a name="p101542391369"></a>POST /v1/{project_id}/baremetalservers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p2062114531169"><a name="p2062114531169"></a><a name="p2062114531169"></a>每分钟100次</p>
</td>
</tr>
<tr id="row1518616391143"><td class="cellrowborder" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p462616531467"><a name="p462616531467"></a><a name="p462616531467"></a>租户配额管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p86311553268"><a name="p86311553268"></a><a name="p86311553268"></a><a href="查询租户配额.md">查询租户配额</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p13154539143611"><a name="p13154539143611"></a><a name="p13154539143611"></a>GET /v1/{project_id}/baremetalservers/limits</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p1363516538618"><a name="p1363516538618"></a><a name="p1363516538618"></a>每分钟500次</p>
</td>
</tr>
<tr id="row2013713819619"><td class="cellrowborder" rowspan="4" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p124755535616"><a name="p124755535616"></a><a name="p124755535616"></a>密码管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p24779536618"><a name="p24779536618"></a><a name="p24779536618"></a><a href="查询是否支持一键重置密码.md">查询是否支持一键重置密码</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p1515393917362"><a name="p1515393917362"></a><a name="p1515393917362"></a>GET /v1/{project_id}/baremetalservers/{server_id}/os-resetpwd-flag</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p94811253268"><a name="p94811253268"></a><a name="p94811253268"></a>每分钟500次</p>
</td>
</tr>
<tr id="row1613733813612"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1249017534620"><a name="p1249017534620"></a><a name="p1249017534620"></a><a href="一键重置裸金属服务器密码.md">一键重置裸金属服务器密码</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p115383963620"><a name="p115383963620"></a><a name="p115383963620"></a>PUT /v1/{project_id}/baremetalservers/{server_id}/os-reset-password</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p0491125310619"><a name="p0491125310619"></a><a name="p0491125310619"></a>每分钟50次</p>
</td>
</tr>
<tr id="row101371538561"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p17499253066"><a name="p17499253066"></a><a name="p17499253066"></a><a href="Windows裸金属服务器获取密码.md">Windows裸金属服务器获取密码</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1315310396361"><a name="p1315310396361"></a><a name="p1315310396361"></a>GET /v1/{project_id}/baremetalservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p5504953464"><a name="p5504953464"></a><a name="p5504953464"></a>每分钟50次</p>
</td>
</tr>
<tr id="row111389381965"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p251325313610"><a name="p251325313610"></a><a name="p251325313610"></a><a href="Windows裸金属服务器清除密码.md">Windows裸金属服务器清除密码</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1215413963610"><a name="p1215413963610"></a><a name="p1215413963610"></a>DELETE /v1/{project_id}/baremetalservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1151517531661"><a name="p1151517531661"></a><a name="p1151517531661"></a>每分钟50次</p>
</td>
</tr>
<tr id="row074016811106"><td class="cellrowborder" valign="top" width="15.14%" headers="mcps1.2.5.1.1 "><p id="p242261751020"><a name="p242261751020"></a><a name="p242261751020"></a>Job管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.400000000000002%" headers="mcps1.2.5.1.2 "><p id="p1274048141011"><a name="p1274048141011"></a><a name="p1274048141011"></a><a href="查询Job状态.md">查询Job状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.630000000000003%" headers="mcps1.2.5.1.3 "><p id="p17154839113617"><a name="p17154839113617"></a><a name="p17154839113617"></a>GET /v1/{project_id}/jobs/{jobId}</p>
</td>
<td class="cellrowborder" valign="top" width="30.830000000000002%" headers="mcps1.2.5.1.4 "><p id="p198921343171019"><a name="p198921343171019"></a><a name="p198921343171019"></a>每分钟2000次</p>
</td>
</tr>
</tbody>
</table>

