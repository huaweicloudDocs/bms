# 更新裸金属服务器元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0053158712"></a>

## 功能介绍<a name="section61558535185333"></a>

更新裸金属服务器元数据。

-   如果元数据中没有待更新字段，则自动添加该字段。
-   如果元数据中已存在待更新字段，则直接更新字段值。

## 约束<a name="section57278039123222"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section47451206185333"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table560512381338)。

**表 1**  参数说明

<a name="table560512381338"></a>
<table><thead align="left"><tr id="row960883873311"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p55073076202321"><a name="p55073076202321"></a><a name="p55073076202321"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p4027920716375"><a name="p4027920716375"></a><a name="p4027920716375"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p19427838185333"><a name="p19427838185333"></a><a name="p19427838185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row96081838143310"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p26317623185333"><a name="p26317623185333"></a><a name="p26317623185333"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p51352688185333"><a name="p51352688185333"></a><a name="p51352688185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p65927025185333"><a name="p65927025185333"></a><a name="p65927025185333"></a>项目ID。</p>
</td>
</tr>
<tr id="row86081438153310"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p10854909185333"><a name="p10854909185333"></a><a name="p10854909185333"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6832475185333"><a name="p6832475185333"></a><a name="p6832475185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p16559613185333"><a name="p16559613185333"></a><a name="p16559613185333"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section14818796185333"></a>

-   请求参数

    <a name="table52485804185333"></a>
    <table><thead align="left"><tr id="row22430249185333"><th class="cellrowborder" valign="top" width="17.2017201720172%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.052005200520053%" id="mcps1.1.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.131913191319132%" id="mcps1.1.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.61436143614361%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row27794510185333"><td class="cellrowborder" valign="top" width="17.2017201720172%" headers="mcps1.1.5.1.1 "><p id="p36762838185333"><a name="p36762838185333"></a><a name="p36762838185333"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.052005200520053%" headers="mcps1.1.5.1.2 "><p id="p11727220185333"><a name="p11727220185333"></a><a name="p11727220185333"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.131913191319132%" headers="mcps1.1.5.1.3 "><p id="p977790181624"><a name="p977790181624"></a><a name="p977790181624"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.61436143614361%" headers="mcps1.1.5.1.4 "><p id="p26317995185333"><a name="p26317995185333"></a><a name="p26317995185333"></a>用户自定义metadata键值对。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] metadata数据结构说明

    <a name="table59792218185333"></a>
    <table><thead align="left"><tr id="row39910345185333"><th class="cellrowborder" valign="top" width="17.53%" id="mcps1.1.5.1.1"><p id="p0999194316596"><a name="p0999194316596"></a><a name="p0999194316596"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.82%" id="mcps1.1.5.1.2"><p id="p150244165912"><a name="p150244165912"></a><a name="p150244165912"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.13%" id="mcps1.1.5.1.3"><p id="p101184475910"><a name="p101184475910"></a><a name="p101184475910"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.519999999999996%" id="mcps1.1.5.1.4"><p id="p17344419599"><a name="p17344419599"></a><a name="p17344419599"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17903267185333"><td class="cellrowborder" valign="top" width="17.53%" headers="mcps1.1.5.1.1 "><p id="p40878540185333"><a name="p40878540185333"></a><a name="p40878540185333"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.1.5.1.2 "><p id="p37081126185333"><a name="p37081126185333"></a><a name="p37081126185333"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.13%" headers="mcps1.1.5.1.3 "><p id="p59522419181648"><a name="p59522419181648"></a><a name="p59522419181648"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p54377834185333"><a name="p54377834185333"></a><a name="p54377834185333"></a>用户自定义metadata键值对。</p>
    <a name="ul12187816141520"></a><a name="ul12187816141520"></a><ul id="ul12187816141520"><li>键、值长度均不大于255字节。</li><li>键名key不支持如下特殊字符：<p id="p104281244172319"><a name="p104281244172319"></a><a name="p104281244172319"></a>:`~!@#$%^&amp;*()=+&lt;,&gt;?/'";{[]}|\</p>
    </li><li>键值value不支持如下特殊字符：<p id="p15830162842312"><a name="p15830162842312"></a><a name="p15830162842312"></a>\"</p>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    {
        "metadata": {
            "key": "value"
        }
    }
    ```


## 响应消息<a name="section22254218185333"></a>

-   响应参数

    <a name="table48150236185333"></a>
    <table><thead align="left"><tr id="row64499137185333"><th class="cellrowborder" valign="top" width="23.82238223822382%" id="mcps1.1.4.1.1"><p id="p1697956135910"><a name="p1697956135910"></a><a name="p1697956135910"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.562456245624563%" id="mcps1.1.4.1.2"><p id="p598956135910"><a name="p598956135910"></a><a name="p598956135910"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.615161516151616%" id="mcps1.1.4.1.3"><p id="p1610045625911"><a name="p1610045625911"></a><a name="p1610045625911"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row51055328185333"><td class="cellrowborder" valign="top" width="23.82238223822382%" headers="mcps1.1.4.1.1 "><p id="p41840919185333"><a name="p41840919185333"></a><a name="p41840919185333"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.562456245624563%" headers="mcps1.1.4.1.2 "><p id="p33671307185333"><a name="p33671307185333"></a><a name="p33671307185333"></a>字典数据结构[2]</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.615161516151616%" headers="mcps1.1.4.1.3 "><p id="p51647808185333"><a name="p51647808185333"></a><a name="p51647808185333"></a>用户自定义metadata键值对。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[2\] metadata字段数据结构说明

    <a name="table22722954185333"></a>
    <table><thead align="left"><tr id="row5305371185333"><th class="cellrowborder" valign="top" width="23.82%" id="mcps1.1.4.1.1"><p id="p893525865912"><a name="p893525865912"></a><a name="p893525865912"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.43%" id="mcps1.1.4.1.2"><p id="p99361858125912"><a name="p99361858125912"></a><a name="p99361858125912"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.74999999999999%" id="mcps1.1.4.1.3"><p id="p693905855910"><a name="p693905855910"></a><a name="p693905855910"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2696702185333"><td class="cellrowborder" valign="top" width="23.82%" headers="mcps1.1.4.1.1 "><p id="p17106284185333"><a name="p17106284185333"></a><a name="p17106284185333"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.43%" headers="mcps1.1.4.1.2 "><p id="p43431730185333"><a name="p43431730185333"></a><a name="p43431730185333"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.74999999999999%" headers="mcps1.1.4.1.3 "><p id="p5719410617654"><a name="p5719410617654"></a><a name="p5719410617654"></a>metadata键、值。</p>
    <a name="ul1049861817191"></a><a name="ul1049861817191"></a><ul id="ul1049861817191"><li>键、值长度大于0字节且小于255字节。</li><li>键值value不支持如下特殊字符：<p id="p1821315403243"><a name="p1821315403243"></a><a name="p1821315403243"></a>\"</p>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "metadata": {
            "key": "value"
        }
    }
    ```


## 返回值<a name="section46706088185333"></a>

请参考[通用返回值](通用返回值.md)。

