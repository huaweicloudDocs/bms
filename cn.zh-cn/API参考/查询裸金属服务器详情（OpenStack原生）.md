# 查询裸金属服务器详情（OpenStack原生）<a name="ZH-CN_TOPIC_0053158707"></a>

## 功能介绍<a name="section11242227"></a>

根据裸金属服务器ID，查询裸金属服务器的详细信息，接口版本为v2.1，支持带微版本号查询。在请求Header中增加一组Key-Value值， Key固定为“X-OpenStack-Nova-API-Version” ，Value为可选的微版本号，例如“2.26”。表示使用微版本号为2.26进行查询。

## URI<a name="section34071180"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}

参数说明请参见[表1](#table17908225144614)。

**表 1**  参数说明

<a name="table17908225144614"></a>
<table><thead align="left"><tr id="row169095255463"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p16058544"><a name="p16058544"></a><a name="p16058544"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p25673664"><a name="p25673664"></a><a name="p25673664"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p66300913"><a name="p66300913"></a><a name="p66300913"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19097252465"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p637140"><a name="p637140"></a><a name="p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p51608407"><a name="p51608407"></a><a name="p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p19531418"><a name="p19531418"></a><a name="p19531418"></a>项目ID。</p>
</td>
</tr>
<tr id="row1790915256462"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p11324657"><a name="p11324657"></a><a name="p11324657"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p44882061"><a name="p44882061"></a><a name="p44882061"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p11568292"><a name="p11568292"></a><a name="p11568292"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section38205169"></a>

不涉及。

## 响应消息<a name="section8302201"></a>

-   响应参数

    <a name="table44736746"></a>
    <table><thead align="left"><tr id="row8242429"><th class="cellrowborder" valign="top" width="22.84228422842284%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.872587258725872%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.28512851285129%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row18745119"><td class="cellrowborder" valign="top" width="22.84228422842284%" headers="mcps1.1.4.1.1 "><p id="p41959665"><a name="p41959665"></a><a name="p41959665"></a>server</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.872587258725872%" headers="mcps1.1.4.1.2 "><p id="p17222571164727"><a name="p17222571164727"></a><a name="p17222571164727"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.28512851285129%" headers="mcps1.1.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a>裸金属服务器信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] server字段数据结构说明

    <a name="table6149040"></a>
    <table><thead align="left"><tr id="row9499663"><th class="cellrowborder" valign="top" width="22.99%" id="mcps1.1.4.1.1"><p id="p937538164712"><a name="p937538164712"></a><a name="p937538164712"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.94%" id="mcps1.1.4.1.2"><p id="p1643193811475"><a name="p1643193811475"></a><a name="p1643193811475"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.07000000000001%" id="mcps1.1.4.1.3"><p id="p15393816472"><a name="p15393816472"></a><a name="p15393816472"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row30856945"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p16384644"><a name="p16384644"></a><a name="p16384644"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p58359570"><a name="p58359570"></a><a name="p58359570"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p29504734"><a name="p29504734"></a><a name="p29504734"></a>裸金属服务器名称。</p>
    </td>
    </tr>
    <tr id="row64216018"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p34114937"><a name="p34114937"></a><a name="p34114937"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p20045150"><a name="p20045150"></a><a name="p20045150"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p13044459"><a name="p13044459"></a><a name="p13044459"></a>裸金属服务器唯一标识ID。</p>
    </td>
    </tr>
    <tr id="row50291273"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p47061312"><a name="p47061312"></a><a name="p47061312"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p1387343"><a name="p1387343"></a><a name="p1387343"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p45265976"><a name="p45265976"></a><a name="p45265976"></a>裸金属服务器当前状态信息。</p>
    </td>
    </tr>
    <tr id="row4740601"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p48444361"><a name="p48444361"></a><a name="p48444361"></a>created</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p15873654"><a name="p15873654"></a><a name="p15873654"></a>String:DateTime</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p10697636"><a name="p10697636"></a><a name="p10697636"></a>裸金属服务器创建时间。</p>
    </td>
    </tr>
    <tr id="row29169865"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p13948877"><a name="p13948877"></a><a name="p13948877"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p49200685"><a name="p49200685"></a><a name="p49200685"></a>String:DateTime</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p25832538"><a name="p25832538"></a><a name="p25832538"></a>裸金属服务器上一次更新时间。</p>
    </td>
    </tr>
    <tr id="row31166252"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p41438477"><a name="p41438477"></a><a name="p41438477"></a>flavor</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p19839955"><a name="p19839955"></a><a name="p19839955"></a>字典数据结构[2]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p34922074"><a name="p34922074"></a><a name="p34922074"></a>裸金属服务器对应裸金属服务器规格信息。</p>
    </td>
    </tr>
    <tr id="row45863212"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p23932707"><a name="p23932707"></a><a name="p23932707"></a>image</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p54863279"><a name="p54863279"></a><a name="p54863279"></a>字典数据结构[3]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p65556790"><a name="p65556790"></a><a name="p65556790"></a>裸金属服务器镜像信息。</p>
    </td>
    </tr>
    <tr id="row53140205"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p9389347"><a name="p9389347"></a><a name="p9389347"></a>tenant_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p64678211"><a name="p64678211"></a><a name="p64678211"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p4443775"><a name="p4443775"></a><a name="p4443775"></a>裸金属服务器所属租户ID。</p>
    </td>
    </tr>
    <tr id="row15792483165644"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p4122771165644"><a name="p4122771165644"></a><a name="p4122771165644"></a>key_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p65509052165644"><a name="p65509052165644"></a><a name="p65509052165644"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p4632965165644"><a name="p4632965165644"></a><a name="p4632965165644"></a>SSH密钥名称。</p>
    </td>
    </tr>
    <tr id="row39993975"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p18286572"><a name="p18286572"></a><a name="p18286572"></a>user_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p54663960"><a name="p54663960"></a><a name="p54663960"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p65704606"><a name="p65704606"></a><a name="p65704606"></a>裸金属服务器所属用户ID。</p>
    </td>
    </tr>
    <tr id="row54470546"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p50038096"><a name="p50038096"></a><a name="p50038096"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p3388666"><a name="p3388666"></a><a name="p3388666"></a>字典数据结构[5]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p54418662"><a name="p54418662"></a><a name="p54418662"></a>裸金属服务器元数据。</p>
    </td>
    </tr>
    <tr id="row20005910"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p9865986"><a name="p9865986"></a><a name="p9865986"></a>hostId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p37794593"><a name="p37794593"></a><a name="p37794593"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p41463203"><a name="p41463203"></a><a name="p41463203"></a>裸金属服务器对应的主机ID。</p>
    </td>
    </tr>
    <tr id="row37624514"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p27686757"><a name="p27686757"></a><a name="p27686757"></a>addresses</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p56232959"><a name="p56232959"></a><a name="p56232959"></a>字典数据结构[6]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p57420266"><a name="p57420266"></a><a name="p57420266"></a>裸金属服务器对应的网络地址信息。</p>
    </td>
    </tr>
    <tr id="row61793156165818"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p39189735165818"><a name="p39189735165818"></a><a name="p39189735165818"></a>security_groups</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p20251975165818"><a name="p20251975165818"></a><a name="p20251975165818"></a>列表数据结构[8]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p29797259165818"><a name="p29797259165818"></a><a name="p29797259165818"></a>裸金属服务器所属安全组列表。</p>
    </td>
    </tr>
    <tr id="row47020346"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p50551688"><a name="p50551688"></a><a name="p50551688"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p17625551"><a name="p17625551"></a><a name="p17625551"></a>列表数据结构[4]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p31233872"><a name="p31233872"></a><a name="p31233872"></a>裸金属服务器相关快捷链接信息。</p>
    </td>
    </tr>
    <tr id="row707018122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p38394472122520"><a name="p38394472122520"></a><a name="p38394472122520"></a>OS-DCF:diskConfig</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p22944523122520"><a name="p22944523122520"></a><a name="p22944523122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p46567083122520"><a name="p46567083122520"></a><a name="p46567083122520"></a>扩展属性，磁盘配置方式。</p>
    </td>
    </tr>
    <tr id="row44817800122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p57427370122520"><a name="p57427370122520"></a><a name="p57427370122520"></a>OS-EXT-AZ:availability_zone</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p21105408122520"><a name="p21105408122520"></a><a name="p21105408122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p31816494122520"><a name="p31816494122520"></a><a name="p31816494122520"></a>扩展属性，可用分区编码。</p>
    </td>
    </tr>
    <tr id="row49718998122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p41666765122520"><a name="p41666765122520"></a><a name="p41666765122520"></a>OS-EXT-SERVICE:service_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p19564767122520"><a name="p19564767122520"></a><a name="p19564767122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p41242310122520"><a name="p41242310122520"></a><a name="p41242310122520"></a>扩展属性，裸金属服务器服务状态。</p>
    </td>
    </tr>
    <tr id="row42807035122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p873534122520"><a name="p873534122520"></a><a name="p873534122520"></a>OS-EXT-SRV-ATTR:host</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p3647431122520"><a name="p3647431122520"></a><a name="p3647431122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p27006529122520"><a name="p27006529122520"></a><a name="p27006529122520"></a>扩展属性，裸金属服务器宿主名称。</p>
    </td>
    </tr>
    <tr id="row27125958122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p24863094122520"><a name="p24863094122520"></a><a name="p24863094122520"></a>OS-EXT-SRV-ATTR:hypervisor_hostname</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p644704122520"><a name="p644704122520"></a><a name="p644704122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p52221046122520"><a name="p52221046122520"></a><a name="p52221046122520"></a>扩展属性，hypervisor主机名称，由Nova  virt驱动提供。</p>
    </td>
    </tr>
    <tr id="row62666318122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p18417330122520"><a name="p18417330122520"></a><a name="p18417330122520"></a>OS-EXT-SRV-ATTR:instance_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p15408791122520"><a name="p15408791122520"></a><a name="p15408791122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p40152581122520"><a name="p40152581122520"></a><a name="p40152581122520"></a>扩展属性，裸金属服务器实例ID。</p>
    </td>
    </tr>
    <tr id="row59158707122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p11766971122520"><a name="p11766971122520"></a><a name="p11766971122520"></a>OS-EXT-STS:power_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p13600613122520"><a name="p13600613122520"></a><a name="p13600613122520"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p27907859122520"><a name="p27907859122520"></a><a name="p27907859122520"></a>扩展属性，裸金属服务器电源状态。</p>
    </td>
    </tr>
    <tr id="row28942811122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p10843807122520"><a name="p10843807122520"></a><a name="p10843807122520"></a>OS-EXT-STS:task_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p5933192122520"><a name="p5933192122520"></a><a name="p5933192122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p10826513122520"><a name="p10826513122520"></a><a name="p10826513122520"></a>扩展属性，裸金属服务器任务状态。</p>
    </td>
    </tr>
    <tr id="row18128948122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p40790901122520"><a name="p40790901122520"></a><a name="p40790901122520"></a>OS-EXT-STS:vm_state</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p15728710122520"><a name="p15728710122520"></a><a name="p15728710122520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p66066036122520"><a name="p66066036122520"></a><a name="p66066036122520"></a>扩展属性，裸金属服务器状态。</p>
    </td>
    </tr>
    <tr id="row2014327122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p45085213122520"><a name="p45085213122520"></a><a name="p45085213122520"></a>OS-SRV-USG:launched_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p28023600122520"><a name="p28023600122520"></a><a name="p28023600122520"></a>String:DateTime</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p55319165122520"><a name="p55319165122520"></a><a name="p55319165122520"></a>扩展属性，裸金属服务器启动时间。</p>
    </td>
    </tr>
    <tr id="row7680354122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p62353148122520"><a name="p62353148122520"></a><a name="p62353148122520"></a>OS-SRV-USG:terminated_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p17440221122520"><a name="p17440221122520"></a><a name="p17440221122520"></a>String:DateTime</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p3371762122520"><a name="p3371762122520"></a><a name="p3371762122520"></a>扩展属性，裸金属服务器关闭时间。</p>
    </td>
    </tr>
    <tr id="row853372122520"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p42095554122520"><a name="p42095554122520"></a><a name="p42095554122520"></a>os-extended-volumes:volumes_attached</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p54296746122520"><a name="p54296746122520"></a><a name="p54296746122520"></a>列表数据结构[9]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p35960290122520"><a name="p35960290122520"></a><a name="p35960290122520"></a>裸金属服务器挂载的云磁盘信息。</p>
    </td>
    </tr>
    <tr id="row58203854165114"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p16891701165114"><a name="p16891701165114"></a><a name="p16891701165114"></a>accessIPv4</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p26050561165114"><a name="p26050561165114"></a><a name="p26050561165114"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p29720730165114"><a name="p29720730165114"></a><a name="p29720730165114"></a>预留属性。</p>
    </td>
    </tr>
    <tr id="row32395720165115"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p6807678165115"><a name="p6807678165115"></a><a name="p6807678165115"></a>accessIPv6</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p14551052165115"><a name="p14551052165115"></a><a name="p14551052165115"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p37784603165115"><a name="p37784603165115"></a><a name="p37784603165115"></a>预留属性。</p>
    </td>
    </tr>
    <tr id="row45481526194558"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p6680555194558"><a name="p6680555194558"></a><a name="p6680555194558"></a>fault</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p4254049194558"><a name="p4254049194558"></a><a name="p4254049194558"></a>字典数据结构[10]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p9033688194558"><a name="p9033688194558"></a><a name="p9033688194558"></a>可选返回的属性，故障原因</p>
    </td>
    </tr>
    <tr id="row43202810165116"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p9766688165116"><a name="p9766688165116"></a><a name="p9766688165116"></a>config_drive</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p52904263165116"><a name="p52904263165116"></a><a name="p52904263165116"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p57386902165116"><a name="p57386902165116"></a><a name="p57386902165116"></a>预留属性。</p>
    </td>
    </tr>
    <tr id="row63072391165255"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p8590013165255"><a name="p8590013165255"></a><a name="p8590013165255"></a>progress</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p24702452165255"><a name="p24702452165255"></a><a name="p24702452165255"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p54741587165255"><a name="p54741587165255"></a><a name="p54741587165255"></a>预留属性。</p>
    </td>
    </tr>
    <tr id="row62339472192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p4168431192944"><a name="p4168431192944"></a><a name="p4168431192944"></a>description</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p2098640192944"><a name="p2098640192944"></a><a name="p2098640192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p35772153192944"><a name="p35772153192944"></a><a name="p35772153192944"></a>描述信息。</p>
    <p id="p39660978192944"><a name="p39660978192944"></a><a name="p39660978192944"></a>微版本 2.19新增</p>
    </td>
    </tr>
    <tr id="row36752769192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p56041785192944"><a name="p56041785192944"></a><a name="p56041785192944"></a>host_status</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p43090708192944"><a name="p43090708192944"></a><a name="p43090708192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p55603620192944"><a name="p55603620192944"></a><a name="p55603620192944"></a>nova-compute状态。</p>
    <a name="ul30670539192944"></a><a name="ul30670539192944"></a><ul id="ul30670539192944"><li>UP：服务正常</li><li>UNKNOWN：状态未知</li><li>DOWN：服务异常</li><li>MAINTENANCE：维护状态</li><li>空字符串：裸金属服务器无主机信息</li></ul>
    <p id="p47210269192944"><a name="p47210269192944"></a><a name="p47210269192944"></a>微版本2.16新增</p>
    </td>
    </tr>
    <tr id="row18996721192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p56548258192944"><a name="p56548258192944"></a><a name="p56548258192944"></a>OS-EXT-SRV-ATTR:hostname</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p17006177192944"><a name="p17006177192944"></a><a name="p17006177192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p42600570192944"><a name="p42600570192944"></a><a name="p42600570192944"></a>裸金属服务器的主机名。</p>
    <p id="p47860811192944"><a name="p47860811192944"></a><a name="p47860811192944"></a>微版本2.3新增</p>
    </td>
    </tr>
    <tr id="row24480368192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p61030804192944"><a name="p61030804192944"></a><a name="p61030804192944"></a>OS-EXT-SRV-ATTR:reservation_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p44548086192944"><a name="p44548086192944"></a><a name="p44548086192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p20891691192944"><a name="p20891691192944"></a><a name="p20891691192944"></a>批量创建场景，裸金属服务器的预留id。</p>
    <p id="p53807496192944"><a name="p53807496192944"></a><a name="p53807496192944"></a>微版本2.3新增</p>
    <p id="p14505423192944"><a name="p14505423192944"></a><a name="p14505423192944"></a>（当前公有云场景不支持）</p>
    </td>
    </tr>
    <tr id="row47459283192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p38361754192944"><a name="p38361754192944"></a><a name="p38361754192944"></a>OS-EXT-SRV-ATTR:launch_index</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p20294378192944"><a name="p20294378192944"></a><a name="p20294378192944"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p7429535192944"><a name="p7429535192944"></a><a name="p7429535192944"></a>批量创建场景，裸金属服务器的启动顺序。</p>
    <p id="p66865815192944"><a name="p66865815192944"></a><a name="p66865815192944"></a>微版本2.3新增</p>
    <p id="p64921428192944"><a name="p64921428192944"></a><a name="p64921428192944"></a>（当前公有云场景不支持）</p>
    </td>
    </tr>
    <tr id="row27642875192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p15972052192944"><a name="p15972052192944"></a><a name="p15972052192944"></a>OS-EXT-SRV-ATTR:kernel_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p18667868192944"><a name="p18667868192944"></a><a name="p18667868192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p6207108192944"><a name="p6207108192944"></a><a name="p6207108192944"></a>若使用AMI格式的镜像，则表示kernel image的UUID；否则，留空。</p>
    <p id="p55863977192944"><a name="p55863977192944"></a><a name="p55863977192944"></a>微版本2.3新增</p>
    <p id="p33013749192944"><a name="p33013749192944"></a><a name="p33013749192944"></a>（当前公有云场景不支持）</p>
    </td>
    </tr>
    <tr id="row55267213192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p42050086192944"><a name="p42050086192944"></a><a name="p42050086192944"></a>OS-EXT-SRV-ATTR:ramdisk_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p50613791192944"><a name="p50613791192944"></a><a name="p50613791192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p22426767192944"><a name="p22426767192944"></a><a name="p22426767192944"></a>若使用AMI格式镜像，则表示ramdisk image的UUID；否则，留空。</p>
    <p id="p514313192944"><a name="p514313192944"></a><a name="p514313192944"></a>微版本2.3新增</p>
    <p id="p4628821192944"><a name="p4628821192944"></a><a name="p4628821192944"></a>（当前公有云场景不支持）</p>
    </td>
    </tr>
    <tr id="row21053882192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p18967993192944"><a name="p18967993192944"></a><a name="p18967993192944"></a>OS-EXT-SRV-ATTR:root_device_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p60012494192944"><a name="p60012494192944"></a><a name="p60012494192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p14273082192944"><a name="p14273082192944"></a><a name="p14273082192944"></a>裸金属服务器系统盘的设备名称。</p>
    <p id="p61348874192944"><a name="p61348874192944"></a><a name="p61348874192944"></a>微版本2.3新增</p>
    </td>
    </tr>
    <tr id="row2339320192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p28826247192944"><a name="p28826247192944"></a><a name="p28826247192944"></a>OS-EXT-SRV-ATTR:user_data</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p53224662192944"><a name="p53224662192944"></a><a name="p53224662192944"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p39593231192944"><a name="p39593231192944"></a><a name="p39593231192944"></a>创建裸金属服务器时指定的user_data。</p>
    </td>
    </tr>
    <tr id="row30086086192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p6653960192944"><a name="p6653960192944"></a><a name="p6653960192944"></a>locked</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p2099860192944"><a name="p2099860192944"></a><a name="p2099860192944"></a>boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p19869683192944"><a name="p19869683192944"></a><a name="p19869683192944"></a>裸金属服务器实例是否为锁定状态。</p>
    <a name="ul44609424192944"></a><a name="ul44609424192944"></a><ul id="ul44609424192944"><li>true：锁定</li><li>false：未锁定</li></ul>
    <p id="p39580388192944"><a name="p39580388192944"></a><a name="p39580388192944"></a>微版本2.9新增</p>
    </td>
    </tr>
    <tr id="row18255979192944"><td class="cellrowborder" valign="top" width="22.99%" headers="mcps1.1.4.1.1 "><p id="p64400516192944"><a name="p64400516192944"></a><a name="p64400516192944"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.94%" headers="mcps1.1.4.1.2 "><p id="p49059297192944"><a name="p49059297192944"></a><a name="p49059297192944"></a>List &lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.07000000000001%" headers="mcps1.1.4.1.3 "><p id="p23937628192944"><a name="p23937628192944"></a><a name="p23937628192944"></a>裸金属服务器标签。</p>
    <p id="p14112065192944"><a name="p14112065192944"></a><a name="p14112065192944"></a>微版本2.26新增</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] flavor字段数据结构说明

    <a name="table19588408"></a>
    <table><thead align="left"><tr id="row65668512"><th class="cellrowborder" valign="top" width="23.32233223322332%" id="mcps1.1.4.1.1"><p id="p185203139482"><a name="p185203139482"></a><a name="p185203139482"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.192619261926193%" id="mcps1.1.4.1.2"><p id="p952581311482"><a name="p952581311482"></a><a name="p952581311482"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.48504850485048%" id="mcps1.1.4.1.3"><p id="p55371313144813"><a name="p55371313144813"></a><a name="p55371313144813"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54114449"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.1.4.1.1 "><p id="p21194271"><a name="p21194271"></a><a name="p21194271"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.192619261926193%" headers="mcps1.1.4.1.2 "><p id="p6046963"><a name="p6046963"></a><a name="p6046963"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.48504850485048%" headers="mcps1.1.4.1.3 "><p id="p20041994"><a name="p20041994"></a><a name="p20041994"></a>裸金属服务器类型ID。</p>
    </td>
    </tr>
    <tr id="row46160221"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.1.4.1.1 "><p id="p47990424"><a name="p47990424"></a><a name="p47990424"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.192619261926193%" headers="mcps1.1.4.1.2 "><p id="p57492083"><a name="p57492083"></a><a name="p57492083"></a>列表数据结构[4]</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.48504850485048%" headers="mcps1.1.4.1.3 "><p id="p35797372"><a name="p35797372"></a><a name="p35797372"></a>裸金属服务器类型相关快捷链接信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[3\] image字段数据结构说明

    <a name="table1258047620856"></a>
    <table><thead align="left"><tr id="row6041176320856"><th class="cellrowborder" valign="top" width="23.43%" id="mcps1.1.4.1.1"><p id="p1927472664813"><a name="p1927472664813"></a><a name="p1927472664813"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.169999999999998%" id="mcps1.1.4.1.2"><p id="p7278192614818"><a name="p7278192614818"></a><a name="p7278192614818"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.4%" id="mcps1.1.4.1.3"><p id="p122885267488"><a name="p122885267488"></a><a name="p122885267488"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4046402920856"><td class="cellrowborder" valign="top" width="23.43%" headers="mcps1.1.4.1.1 "><p id="p5636094120856"><a name="p5636094120856"></a><a name="p5636094120856"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.1.4.1.2 "><p id="p183352620856"><a name="p183352620856"></a><a name="p183352620856"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.4%" headers="mcps1.1.4.1.3 "><p id="p1429788720856"><a name="p1429788720856"></a><a name="p1429788720856"></a>裸金属服务器镜像ID。</p>
    </td>
    </tr>
    <tr id="row6157211920856"><td class="cellrowborder" valign="top" width="23.43%" headers="mcps1.1.4.1.1 "><p id="p2128571520856"><a name="p2128571520856"></a><a name="p2128571520856"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.169999999999998%" headers="mcps1.1.4.1.2 "><p id="p4642138020856"><a name="p4642138020856"></a><a name="p4642138020856"></a>列表数据结构[4]</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.4%" headers="mcps1.1.4.1.3 "><p id="p203547420856"><a name="p203547420856"></a><a name="p203547420856"></a>裸金属服务器镜像相关快捷链接信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[4\] links字段数据结构说明

    <a name="table16539321"></a>
    <table><thead align="left"><tr id="row4585366"><th class="cellrowborder" valign="top" width="23.86761323867613%" id="mcps1.1.4.1.1"><p id="p5927193513484"><a name="p5927193513484"></a><a name="p5927193513484"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.17738226177382%" id="mcps1.1.4.1.2"><p id="p189301935184812"><a name="p189301935184812"></a><a name="p189301935184812"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.95500449955004%" id="mcps1.1.4.1.3"><p id="p12940123554816"><a name="p12940123554816"></a><a name="p12940123554816"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row14455526"><td class="cellrowborder" valign="top" width="23.86761323867613%" headers="mcps1.1.4.1.1 "><p id="p30046962"><a name="p30046962"></a><a name="p30046962"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.17738226177382%" headers="mcps1.1.4.1.2 "><p id="p39387099"><a name="p39387099"></a><a name="p39387099"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.95500449955004%" headers="mcps1.1.4.1.3 "><p id="p36238473"><a name="p36238473"></a><a name="p36238473"></a>快捷链接标记名称。</p>
    </td>
    </tr>
    <tr id="row57710802"><td class="cellrowborder" valign="top" width="23.86761323867613%" headers="mcps1.1.4.1.1 "><p id="p44063391"><a name="p44063391"></a><a name="p44063391"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.17738226177382%" headers="mcps1.1.4.1.2 "><p id="p62035831"><a name="p62035831"></a><a name="p62035831"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.95500449955004%" headers="mcps1.1.4.1.3 "><p id="p58846418"><a name="p58846418"></a><a name="p58846418"></a>对应快捷链接。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[5\] metadata字段数据结构说明

    <a name="table2549048917552"></a>
    <table><thead align="left"><tr id="row5894027817552"><th class="cellrowborder" valign="top" width="24.467553244675532%" id="mcps1.1.4.1.1"><p id="p91023447486"><a name="p91023447486"></a><a name="p91023447486"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.76742325767423%" id="mcps1.1.4.1.2"><p id="p7108104414810"><a name="p7108104414810"></a><a name="p7108104414810"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.76502349765023%" id="mcps1.1.4.1.3"><p id="p211774424818"><a name="p211774424818"></a><a name="p211774424818"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2346131617552"><td class="cellrowborder" valign="top" width="24.467553244675532%" headers="mcps1.1.4.1.1 "><p id="p2131841817552"><a name="p2131841817552"></a><a name="p2131841817552"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.76742325767423%" headers="mcps1.1.4.1.2 "><p id="p4907026417552"><a name="p4907026417552"></a><a name="p4907026417552"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.76502349765023%" headers="mcps1.1.4.1.3 "><p id="p5719410617654"><a name="p5719410617654"></a><a name="p5719410617654"></a>metadata键、值。</p>
    <p id="p4498490617654"><a name="p4498490617654"></a><a name="p4498490617654"></a>键、值长度均不大于255字节。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[6\] addresses字段数据结构说明

    <a name="table3730161"></a>
    <table><thead align="left"><tr id="row20014316"><th class="cellrowborder" valign="top" width="24.587541245875414%" id="mcps1.1.4.1.1"><p id="p10546933"><a name="p10546933"></a><a name="p10546933"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.23737626237376%" id="mcps1.1.4.1.2"><p id="p9192332"><a name="p9192332"></a><a name="p9192332"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.17508249175083%" id="mcps1.1.4.1.3"><p id="p6381418"><a name="p6381418"></a><a name="p6381418"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row57432766"><td class="cellrowborder" valign="top" width="24.587541245875414%" headers="mcps1.1.4.1.1 "><p id="p25045336115623"><a name="p25045336115623"></a><a name="p25045336115623"></a>虚拟私有云ID</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.23737626237376%" headers="mcps1.1.4.1.2 "><p id="p4439518115623"><a name="p4439518115623"></a><a name="p4439518115623"></a>列表数据结构[7]</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.17508249175083%" headers="mcps1.1.4.1.3 "><p id="p2639016112816"><a name="p2639016112816"></a><a name="p2639016112816"></a>名称是变量，表示裸金属服务器使用的虚拟私有云的ID。</p>
    <p id="p3618485912816"><a name="p3618485912816"></a><a name="p3618485912816"></a>数据结构中是该虚拟私有云下分配的私有IP地址列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[7\]  _虚拟私有云ID_字段数据结构说明

    <a name="table1656029015527"></a>
    <table><thead align="left"><tr id="row2645284715527"><th class="cellrowborder" valign="top" width="24.702470247024706%" id="mcps1.1.4.1.1"><p id="p1040324134912"><a name="p1040324134912"></a><a name="p1040324134912"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.19271927192719%" id="mcps1.1.4.1.2"><p id="p184063416497"><a name="p184063416497"></a><a name="p184063416497"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.10481048104811%" id="mcps1.1.4.1.3"><p id="p1941717419491"><a name="p1941717419491"></a><a name="p1941717419491"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5009697415527"><td class="cellrowborder" valign="top" width="24.702470247024706%" headers="mcps1.1.4.1.1 "><p id="p3132311415527"><a name="p3132311415527"></a><a name="p3132311415527"></a>addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.19271927192719%" headers="mcps1.1.4.1.2 "><p id="p5414433915527"><a name="p5414433915527"></a><a name="p5414433915527"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.10481048104811%" headers="mcps1.1.4.1.3 "><p id="p2361534415527"><a name="p2361534415527"></a><a name="p2361534415527"></a>IP地址信息。</p>
    </td>
    </tr>
    <tr id="row1121151015527"><td class="cellrowborder" valign="top" width="24.702470247024706%" headers="mcps1.1.4.1.1 "><p id="p3571711715527"><a name="p3571711715527"></a><a name="p3571711715527"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.19271927192719%" headers="mcps1.1.4.1.2 "><p id="p740535615527"><a name="p740535615527"></a><a name="p740535615527"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.10481048104811%" headers="mcps1.1.4.1.3 "><p id="p6296298815527"><a name="p6296298815527"></a><a name="p6296298815527"></a>IP地址类型，值为4或6。</p>
    <a name="ul2979598615527"></a><a name="ul2979598615527"></a><ul id="ul2979598615527"><li>4：IP地址类型是IPv4</li><li>6：IP地址类型是IPv6</li></ul>
    </td>
    </tr>
    <tr id="row3913338616494"><td class="cellrowborder" valign="top" width="24.702470247024706%" headers="mcps1.1.4.1.1 "><p id="p37919028165012"><a name="p37919028165012"></a><a name="p37919028165012"></a>OS-EXT-IPS-MAC:mac_addr</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.19271927192719%" headers="mcps1.1.4.1.2 "><p id="p51542402165012"><a name="p51542402165012"></a><a name="p51542402165012"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.10481048104811%" headers="mcps1.1.4.1.3 "><p id="p14185000165012"><a name="p14185000165012"></a><a name="p14185000165012"></a>扩展属性，MAC地址。</p>
    </td>
    </tr>
    <tr id="row5993434716495"><td class="cellrowborder" valign="top" width="24.702470247024706%" headers="mcps1.1.4.1.1 "><p id="p6100298165012"><a name="p6100298165012"></a><a name="p6100298165012"></a>OS-EXT-IPS:type</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.19271927192719%" headers="mcps1.1.4.1.2 "><p id="p24362133165012"><a name="p24362133165012"></a><a name="p24362133165012"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.10481048104811%" headers="mcps1.1.4.1.3 "><p id="p27175732165012"><a name="p27175732165012"></a><a name="p27175732165012"></a>扩展属性，分配IP地址方式。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[8\] security\_groups字段数据结构说明

    <a name="table761507165933"></a>
    <table><thead align="left"><tr id="row29958070165933"><th class="cellrowborder" valign="top" width="24.6975302469753%" id="mcps1.1.4.1.1"><p id="p8701420144919"><a name="p8701420144919"></a><a name="p8701420144919"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.107289271072894%" id="mcps1.1.4.1.2"><p id="p574420174917"><a name="p574420174917"></a><a name="p574420174917"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.1951804819518%" id="mcps1.1.4.1.3"><p id="p108542064912"><a name="p108542064912"></a><a name="p108542064912"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row29572324165933"><td class="cellrowborder" valign="top" width="24.6975302469753%" headers="mcps1.1.4.1.1 "><p id="p46548026165933"><a name="p46548026165933"></a><a name="p46548026165933"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.107289271072894%" headers="mcps1.1.4.1.2 "><p id="p12293798165933"><a name="p12293798165933"></a><a name="p12293798165933"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.1951804819518%" headers="mcps1.1.4.1.3 "><a name="ul1907127295026"></a><a name="ul1907127295026"></a><ul id="ul1907127295026"><li>创建裸金属服务器时未指定安全组，该值为default。</li><li>创建裸金属服务器时指定了安全组，该值为裸金属服务器所在虚拟私有云ID。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    \[9\] os-extended-volumes:volumes\_attached字段数据结构说明

    <a name="table20591095122442"></a>
    <table><thead align="left"><tr id="row46969160122442"><th class="cellrowborder" valign="top" width="24.532453245324533%" id="mcps1.1.4.1.1"><p id="p10156836154910"><a name="p10156836154910"></a><a name="p10156836154910"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.302730273027304%" id="mcps1.1.4.1.2"><p id="p161669368492"><a name="p161669368492"></a><a name="p161669368492"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.16481648164816%" id="mcps1.1.4.1.3"><p id="p2178236184915"><a name="p2178236184915"></a><a name="p2178236184915"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row22997982122442"><td class="cellrowborder" valign="top" width="24.532453245324533%" headers="mcps1.1.4.1.1 "><p id="p50897247122442"><a name="p50897247122442"></a><a name="p50897247122442"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.302730273027304%" headers="mcps1.1.4.1.2 "><p id="p29036308122442"><a name="p29036308122442"></a><a name="p29036308122442"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.16481648164816%" headers="mcps1.1.4.1.3 "><p id="p3130725122442"><a name="p3130725122442"></a><a name="p3130725122442"></a>云磁盘ID。</p>
    </td>
    </tr>
    <tr id="row30980296195037"><td class="cellrowborder" valign="top" width="24.532453245324533%" headers="mcps1.1.4.1.1 "><p id="p50956008195037"><a name="p50956008195037"></a><a name="p50956008195037"></a>delete_on_termination</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.302730273027304%" headers="mcps1.1.4.1.2 "><p id="p33796012195037"><a name="p33796012195037"></a><a name="p33796012195037"></a>boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.16481648164816%" headers="mcps1.1.4.1.3 "><p id="p7951369195037"><a name="p7951369195037"></a><a name="p7951369195037"></a>删裸金属服务器时是否一并删除该卷。</p>
    <a name="ul4453459195037"></a><a name="ul4453459195037"></a><ul id="ul4453459195037"><li>true：是</li><li>false：否</li></ul>
    <p id="p25346744195037"><a name="p25346744195037"></a><a name="p25346744195037"></a>微版本2.3新增</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[10\] fault字段数据结构说明

    <a name="table48872702194825"></a>
    <table><thead align="left"><tr id="row7333744194825"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.4.1.1"><p id="p4296115020494"><a name="p4296115020494"></a><a name="p4296115020494"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.189999999999998%" id="mcps1.1.4.1.2"><p id="p2030275074910"><a name="p2030275074910"></a><a name="p2030275074910"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.81%" id="mcps1.1.4.1.3"><p id="p431725004912"><a name="p431725004912"></a><a name="p431725004912"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row22593755194825"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p18154898194825"><a name="p18154898194825"></a><a name="p18154898194825"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.1.4.1.2 "><p id="p61260596194825"><a name="p61260596194825"></a><a name="p61260596194825"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.81%" headers="mcps1.1.4.1.3 "><p id="p15788383194825"><a name="p15788383194825"></a><a name="p15788383194825"></a>故障信息。</p>
    </td>
    </tr>
    <tr id="row7877723194825"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p34115828194825"><a name="p34115828194825"></a><a name="p34115828194825"></a>code</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.1.4.1.2 "><p id="p11918718194825"><a name="p11918718194825"></a><a name="p11918718194825"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.81%" headers="mcps1.1.4.1.3 "><p id="p16887684194825"><a name="p16887684194825"></a><a name="p16887684194825"></a>故障code。</p>
    </td>
    </tr>
    <tr id="row17771429194825"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p30199627194825"><a name="p30199627194825"></a><a name="p30199627194825"></a>details</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.1.4.1.2 "><p id="p30250759194825"><a name="p30250759194825"></a><a name="p30250759194825"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.81%" headers="mcps1.1.4.1.3 "><p id="p34319578194825"><a name="p34319578194825"></a><a name="p34319578194825"></a>故障详情。</p>
    </td>
    </tr>
    <tr id="row40440754194825"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.4.1.1 "><p id="p54475616194825"><a name="p54475616194825"></a><a name="p54475616194825"></a>created</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.1.4.1.2 "><p id="p50448742194825"><a name="p50448742194825"></a><a name="p50448742194825"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.81%" headers="mcps1.1.4.1.3 "><p id="p13282204194825"><a name="p13282204194825"></a><a name="p13282204194825"></a>故障时间，ISO8601格式。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "server": {
            "tenant_id": "c685484a8cc2416b97260938705deb65",
            "addresses": {
                "08a7715f-7de6-4ff9-a343-95ba4209f24a": [
                    {
                        "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:0e:c3:77",
                        "OS-EXT-IPS:type": "fixed",
                        "addr": "192.168.0.107",
                        "version": 4
                    }
                ]
            },
            "metadata": {
                "op_svc_userid": "1311c433dd9b408886f57d695c229cbe"
            },
            "OS-EXT-STS:task_state": null,
            "OS-DCF:diskConfig": "MANUAL",
            "OS-EXT-AZ:availability_zone": "eu-de-01",
            "links": [
                {
                    "rel": "self",
                    "href": "https://ecs-api.eu-de.otc-tsi.de/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                },
                {
                    "rel": "bookmark",
                    "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd"
                }
            ],
            "OS-EXT-STS:power_state": 1,
            "id": "95bf2490-5428-432c-ad9b-5e3406f869dd",
            "os-extended-volumes:volumes_attached": [
                {
                    "id": "dfa375b5-9856-44ad-a937-a4802b6434c3"
                },
                {
                    "id": "bb9f1b27-843b-4561-b62e-ca18eeaec417"
                },
                {
                    "id": "86e801c3-acc6-465d-890c-d43ba493f553"
                },
                {
                    "id": "0994d3ac-3c6a-495c-a439-c597a4f08fa6"
                }
            ],
            "OS-EXT-SRV-ATTR:host": "bms.eu-de-01",
            "image": {
                "links": [
                    {
                        "rel": "bookmark",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/images/1a6635d8-afea-4f2b-abb6-27a202bad319"
                    }
                ],
                "id": "1a6635d8-afea-4f2b-abb6-27a202bad319"
            },
            "OS-SRV-USG:terminated_at": null,
            "accessIPv4": "",
            "accessIPv6": "",
            "created": "2017-05-24T06:14:05Z",
            "hostId": "e9c3ee0fcc58ab6085cf30df70b5544eab958858fb50d925f023e53e",
            "OS-EXT-SRV-ATTR:hypervisor_hostname": "nova004@2",
            "key_name": "KeyPair-JX",
            "flavor": {
                "links": [
                    {
                        "rel": "bookmark",
                        "href": "https://ecs-api.eu-de.otc-tsi.de/c685484a8cc2416b97260938705deb65/flavors/physical.83.medium"
                    }
                ],
                "id": "physical.83.medium"
            },
            "security_groups": [
                {
                    "name": "0011b620-4982-42e4-ad12-47c95ca495c4"
                }
            ],
            "config_drive": "",
            "OS-EXT-STS:vm_state": "active",
            "OS-EXT-SRV-ATTR:instance_name": "instance-0000ebd3",
            "user_id": "1311c433dd9b408886f57d695c229cbe",
            "name": "bms-83",
            "progress": 0,
            "OS-SRV-USG:launched_at": "2017-05-25T03:40:25.066078",
            "updated": "2017-05-25T03:40:25Z",
            "status": "ACTIVE"
        }
    }
    ```


## 返回值<a name="section7610951"></a>

请参考[通用返回值](通用返回值.md)。

