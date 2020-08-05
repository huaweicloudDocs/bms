# 自定义网络ACL配置示例<a name="ZH-CN_TOPIC_0161727556"></a>

## 示例一：拒绝特定端口访问<a name="section968441113166"></a>

在本示例中，假设要防止勒索病毒Wanna Cry的攻击，需要隔离具有漏洞的应用端口，例如TCP 445端口。您可以在子网层级添加自定义网络ACL拒绝规则，拒绝所有对TCP 445端口的入站访问。

需要添加的入方向规则如[表1](#table12372132313177)所示。

**表 1**  自定义网络ACL规则

<a name="table12372132313177"></a>
<table><thead align="left"><tr id="row83726235174"><th class="cellrowborder" valign="top" width="9.46%" id="mcps1.2.9.1.1"><p id="p1437292312171"><a name="p1437292312171"></a><a name="p1437292312171"></a>方向</p>
</th>
<th class="cellrowborder" valign="top" width="9.19%" id="mcps1.2.9.1.2"><p id="p33736237172"><a name="p33736237172"></a><a name="p33736237172"></a>策略</p>
</th>
<th class="cellrowborder" valign="top" width="10.05%" id="mcps1.2.9.1.3"><p id="p1337319234177"><a name="p1337319234177"></a><a name="p1337319234177"></a>协议</p>
</th>
<th class="cellrowborder" valign="top" width="12.2%" id="mcps1.2.9.1.4"><p id="p183731023121717"><a name="p183731023121717"></a><a name="p183731023121717"></a>源地址</p>
</th>
<th class="cellrowborder" valign="top" width="12.379999999999999%" id="mcps1.2.9.1.5"><p id="p11373102315176"><a name="p11373102315176"></a><a name="p11373102315176"></a>源端口范围</p>
</th>
<th class="cellrowborder" valign="top" width="13.459999999999999%" id="mcps1.2.9.1.6"><p id="p17373162318179"><a name="p17373162318179"></a><a name="p17373162318179"></a>目的地址</p>
</th>
<th class="cellrowborder" valign="top" width="12.91%" id="mcps1.2.9.1.7"><p id="p03731323181712"><a name="p03731323181712"></a><a name="p03731323181712"></a>目的端口范围</p>
</th>
<th class="cellrowborder" valign="top" width="20.349999999999998%" id="mcps1.2.9.1.8"><p id="p837342317172"><a name="p837342317172"></a><a name="p837342317172"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9373142313177"><td class="cellrowborder" valign="top" width="9.46%" headers="mcps1.2.9.1.1 "><p id="p16373172310178"><a name="p16373172310178"></a><a name="p16373172310178"></a>入方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.9.1.2 "><p id="p037322321718"><a name="p037322321718"></a><a name="p037322321718"></a>拒绝</p>
</td>
<td class="cellrowborder" valign="top" width="10.05%" headers="mcps1.2.9.1.3 "><p id="p173730232176"><a name="p173730232176"></a><a name="p173730232176"></a>TCP</p>
</td>
<td class="cellrowborder" valign="top" width="12.2%" headers="mcps1.2.9.1.4 "><p id="p6373132317170"><a name="p6373132317170"></a><a name="p6373132317170"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.379999999999999%" headers="mcps1.2.9.1.5 "><p id="p63731623101716"><a name="p63731623101716"></a><a name="p63731623101716"></a>1-65535</p>
</td>
<td class="cellrowborder" valign="top" width="13.459999999999999%" headers="mcps1.2.9.1.6 "><p id="p14373423171710"><a name="p14373423171710"></a><a name="p14373423171710"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.9.1.7 "><p id="p137372391717"><a name="p137372391717"></a><a name="p137372391717"></a>445</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.9.1.8 "><p id="p133731523171712"><a name="p133731523171712"></a><a name="p133731523171712"></a>拒绝所有IP地址通过TCP 445端口入站访问</p>
</td>
</tr>
</tbody>
</table>

## 示例二：允许某些协议端口的访问<a name="section19692296209"></a>

在本示例中，假设自定义子网内的某个裸金属服务器做Web服务器，入方向需要放通HTTP 80和HTTPS 443端口，出方向全部放通。

需要添加的自定义网络ACL入方向、出方向规则如[表2](#table1798617588250)所示。

**表 2**  自定义网络ACL规则

<a name="table1798617588250"></a>
<table><thead align="left"><tr id="row0986658132512"><th class="cellrowborder" valign="top" width="9.46%" id="mcps1.2.9.1.1"><p id="p1398619580258"><a name="p1398619580258"></a><a name="p1398619580258"></a>方向</p>
</th>
<th class="cellrowborder" valign="top" width="9.19%" id="mcps1.2.9.1.2"><p id="p10986185892511"><a name="p10986185892511"></a><a name="p10986185892511"></a>策略</p>
</th>
<th class="cellrowborder" valign="top" width="10.05%" id="mcps1.2.9.1.3"><p id="p29863585250"><a name="p29863585250"></a><a name="p29863585250"></a>协议</p>
</th>
<th class="cellrowborder" valign="top" width="12.2%" id="mcps1.2.9.1.4"><p id="p69861582256"><a name="p69861582256"></a><a name="p69861582256"></a>源地址</p>
</th>
<th class="cellrowborder" valign="top" width="12.379999999999999%" id="mcps1.2.9.1.5"><p id="p13986558122519"><a name="p13986558122519"></a><a name="p13986558122519"></a>源端口范围</p>
</th>
<th class="cellrowborder" valign="top" width="13.459999999999999%" id="mcps1.2.9.1.6"><p id="p198735802514"><a name="p198735802514"></a><a name="p198735802514"></a>目的地址</p>
</th>
<th class="cellrowborder" valign="top" width="12.91%" id="mcps1.2.9.1.7"><p id="p79871558162513"><a name="p79871558162513"></a><a name="p79871558162513"></a>目的端口范围</p>
</th>
<th class="cellrowborder" valign="top" width="20.349999999999998%" id="mcps1.2.9.1.8"><p id="p498795816253"><a name="p498795816253"></a><a name="p498795816253"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row59871558172518"><td class="cellrowborder" valign="top" width="9.46%" headers="mcps1.2.9.1.1 "><p id="p11987185852511"><a name="p11987185852511"></a><a name="p11987185852511"></a>入方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.9.1.2 "><p id="p1498775892511"><a name="p1498775892511"></a><a name="p1498775892511"></a>允许</p>
</td>
<td class="cellrowborder" valign="top" width="10.05%" headers="mcps1.2.9.1.3 "><p id="p298712587258"><a name="p298712587258"></a><a name="p298712587258"></a>TCP</p>
</td>
<td class="cellrowborder" valign="top" width="12.2%" headers="mcps1.2.9.1.4 "><p id="p129879584259"><a name="p129879584259"></a><a name="p129879584259"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.379999999999999%" headers="mcps1.2.9.1.5 "><p id="p49879588252"><a name="p49879588252"></a><a name="p49879588252"></a>1-65535</p>
</td>
<td class="cellrowborder" valign="top" width="13.459999999999999%" headers="mcps1.2.9.1.6 "><p id="p298718586252"><a name="p298718586252"></a><a name="p298718586252"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.9.1.7 "><p id="p1898735819257"><a name="p1898735819257"></a><a name="p1898735819257"></a>80</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.9.1.8 "><p id="p1598765812512"><a name="p1598765812512"></a><a name="p1598765812512"></a>允许所有IP地址通过HTTP协议入站访问自定义子网内的裸金属服务器的80端口</p>
</td>
</tr>
<tr id="row252217255268"><td class="cellrowborder" valign="top" width="9.46%" headers="mcps1.2.9.1.1 "><p id="p2052382542610"><a name="p2052382542610"></a><a name="p2052382542610"></a>入方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.9.1.2 "><p id="p152316259268"><a name="p152316259268"></a><a name="p152316259268"></a>允许</p>
</td>
<td class="cellrowborder" valign="top" width="10.05%" headers="mcps1.2.9.1.3 "><p id="p16523132592620"><a name="p16523132592620"></a><a name="p16523132592620"></a>TCP</p>
</td>
<td class="cellrowborder" valign="top" width="12.2%" headers="mcps1.2.9.1.4 "><p id="p652317257266"><a name="p652317257266"></a><a name="p652317257266"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.379999999999999%" headers="mcps1.2.9.1.5 "><p id="p55237256260"><a name="p55237256260"></a><a name="p55237256260"></a>1-65535</p>
</td>
<td class="cellrowborder" valign="top" width="13.459999999999999%" headers="mcps1.2.9.1.6 "><p id="p65231225132611"><a name="p65231225132611"></a><a name="p65231225132611"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.9.1.7 "><p id="p12523122519269"><a name="p12523122519269"></a><a name="p12523122519269"></a>443</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.9.1.8 "><p id="p185231252265"><a name="p185231252265"></a><a name="p185231252265"></a>允许所有IP地址通过HTTP协议入站访问自定义子网内的裸金属服务器的443端口</p>
</td>
</tr>
<tr id="row2623172910269"><td class="cellrowborder" valign="top" width="9.46%" headers="mcps1.2.9.1.1 "><p id="p20623162917265"><a name="p20623162917265"></a><a name="p20623162917265"></a>出方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.9.1.2 "><p id="p6623129202613"><a name="p6623129202613"></a><a name="p6623129202613"></a>允许</p>
</td>
<td class="cellrowborder" valign="top" width="10.05%" headers="mcps1.2.9.1.3 "><p id="p1762311295265"><a name="p1762311295265"></a><a name="p1762311295265"></a>全部</p>
</td>
<td class="cellrowborder" valign="top" width="12.2%" headers="mcps1.2.9.1.4 "><p id="p76231529132618"><a name="p76231529132618"></a><a name="p76231529132618"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.379999999999999%" headers="mcps1.2.9.1.5 "><p id="p66231129162614"><a name="p66231129162614"></a><a name="p66231129162614"></a>0</p>
</td>
<td class="cellrowborder" valign="top" width="13.459999999999999%" headers="mcps1.2.9.1.6 "><p id="p12623182932613"><a name="p12623182932613"></a><a name="p12623182932613"></a>0.0.0.0/0</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.9.1.7 "><p id="p262382916267"><a name="p262382916267"></a><a name="p262382916267"></a>0</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.9.1.8 "><p id="p106231294268"><a name="p106231294268"></a><a name="p106231294268"></a>允许自定义子网内所有出站流量的数据报文通过</p>
</td>
</tr>
</tbody>
</table>

