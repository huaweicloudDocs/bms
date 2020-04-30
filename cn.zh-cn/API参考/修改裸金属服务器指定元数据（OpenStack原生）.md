# 修改裸金属服务器指定元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0053158695"></a>

## 功能介绍<a name="section19950704192629"></a>

修改裸金属服务器指定元数据。

## 约束<a name="section48821040143631"></a>

裸金属服务器状态（OS-EXT-STS:vm\_state属性）必须是active、stopped、paused或者suspended。

## URI<a name="section48549151192629"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table1370626163519)。

**表 1**  参数说明

<a name="table1370626163519"></a>
<table><thead align="left"><tr id="row1708361352"><th class="cellrowborder" valign="top" width="25.662566256625663%" id="mcps1.2.4.1.1"><p id="p11130554192629"><a name="p11130554192629"></a><a name="p11130554192629"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="26.712671267126716%" id="mcps1.2.4.1.2"><p id="p29159654192629"><a name="p29159654192629"></a><a name="p29159654192629"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47.624762476247625%" id="mcps1.2.4.1.3"><p id="p13121799192629"><a name="p13121799192629"></a><a name="p13121799192629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17708565350"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p58565959192629"><a name="p58565959192629"></a><a name="p58565959192629"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="26.712671267126716%" headers="mcps1.2.4.1.2 "><p id="p46222262192629"><a name="p46222262192629"></a><a name="p46222262192629"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.624762476247625%" headers="mcps1.2.4.1.3 "><p id="p53015737192629"><a name="p53015737192629"></a><a name="p53015737192629"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row137081065353"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p60875907192629"><a name="p60875907192629"></a><a name="p60875907192629"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="26.712671267126716%" headers="mcps1.2.4.1.2 "><p id="p32001416192629"><a name="p32001416192629"></a><a name="p32001416192629"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.624762476247625%" headers="mcps1.2.4.1.3 "><p id="p41977918192629"><a name="p41977918192629"></a><a name="p41977918192629"></a><span id="text9174603203"><a name="text9174603203"></a><a name="text9174603203"></a>裸金属服务器</span><span id="text7174209201"><a name="text7174209201"></a><a name="text7174209201"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
<tr id="row570816103517"><td class="cellrowborder" valign="top" width="25.662566256625663%" headers="mcps1.2.4.1.1 "><p id="p2044590819279"><a name="p2044590819279"></a><a name="p2044590819279"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="26.712671267126716%" headers="mcps1.2.4.1.2 "><p id="p4550582719279"><a name="p4550582719279"></a><a name="p4550582719279"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.624762476247625%" headers="mcps1.2.4.1.3 "><p id="p6209335919279"><a name="p6209335919279"></a><a name="p6209335919279"></a>待修改的<span id="text1279921102018"><a name="text1279921102018"></a><a name="text1279921102018"></a>裸金属服务器</span><span id="text11799017207"><a name="text11799017207"></a><a name="text11799017207"></a></span>metadata键值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section42256947192629"></a>

-   请求参数

    <a name="table21113531192629"></a>
    <table><thead align="left"><tr id="row12974012192629"><th class="cellrowborder" valign="top" width="17.2%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.9%" id="mcps1.1.5.1.2"><p id="p87612353016"><a name="p87612353016"></a><a name="p87612353016"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.25%" id="mcps1.1.5.1.3"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="41.65%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8613312192629"><td class="cellrowborder" valign="top" width="17.2%" headers="mcps1.1.5.1.1 "><p id="p26589676192629"><a name="p26589676192629"></a><a name="p26589676192629"></a>meta</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.1.5.1.2 "><p id="p57785097181826"><a name="p57785097181826"></a><a name="p57785097181826"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.1.5.1.3 "><p id="p38929685192629"><a name="p38929685192629"></a><a name="p38929685192629"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.65%" headers="mcps1.1.5.1.4 "><p id="p59800316192629"><a name="p59800316192629"></a><a name="p59800316192629"></a>用户自定义metadata键值对。详情请参见<a href="#table40778039192629">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  meta数据结构说明

    <a name="table40778039192629"></a>
    <table><thead align="left"><tr id="row63796811192629"><th class="cellrowborder" valign="top" width="17.810000000000002%" id="mcps1.2.5.1.1"><p id="p16744351100"><a name="p16744351100"></a><a name="p16744351100"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.39%" id="mcps1.2.5.1.2"><p id="p6539153311416"><a name="p6539153311416"></a><a name="p6539153311416"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.36%" id="mcps1.2.5.1.3"><p id="p14755351010"><a name="p14755351010"></a><a name="p14755351010"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="41.44%" id="mcps1.2.5.1.4"><p id="p47711354019"><a name="p47711354019"></a><a name="p47711354019"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row30326018192629"><td class="cellrowborder" valign="top" width="17.810000000000002%" headers="mcps1.2.5.1.1 "><p id="p40488404192629"><a name="p40488404192629"></a><a name="p40488404192629"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.5.1.2 "><p id="p14539633743"><a name="p14539633743"></a><a name="p14539633743"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.36%" headers="mcps1.2.5.1.3 "><p id="p27540070192629"><a name="p27540070192629"></a><a name="p27540070192629"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="41.44%" headers="mcps1.2.5.1.4 "><p id="p11161128192629"><a name="p11161128192629"></a><a name="p11161128192629"></a>用户自定义metadata键值对。</p>
    <a name="ul687584551016"></a><a name="ul687584551016"></a><ul id="ul687584551016"><li>键、值长度均不大于255字节。</li><li>键名key不支持如下特殊字符：<p id="zh-cn_topic_0053158712_p104281244172319"><a name="zh-cn_topic_0053158712_p104281244172319"></a><a name="zh-cn_topic_0053158712_p104281244172319"></a>:`~!@#$%^&amp;*()=+&lt;,&gt;?/'";{[]}|\</p>
    </li><li>键值value不支持如下特殊字符：<p id="zh-cn_topic_0053158712_p15830162842312"><a name="zh-cn_topic_0053158712_p15830162842312"></a><a name="zh-cn_topic_0053158712_p15830162842312"></a>\"</p>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    PUT https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/metadata/{key}
    ```

    ```
    {
        "meta": {
            "key": "value"
        }
    }
    ```


## 响应消息<a name="section12391939192629"></a>

-   响应参数

    <a name="table34681280192629"></a>
    <table><thead align="left"><tr id="row7754416192629"><th class="cellrowborder" valign="top" width="23.912391239123913%" id="mcps1.1.4.1.1"><p id="p053124814019"><a name="p053124814019"></a><a name="p053124814019"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.7023702370237%" id="mcps1.1.4.1.2"><p id="p165594820018"><a name="p165594820018"></a><a name="p165594820018"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.38523852385239%" id="mcps1.1.4.1.3"><p id="p958124812019"><a name="p958124812019"></a><a name="p958124812019"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34495047192629"><td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.4.1.1 "><p id="p42635402192629"><a name="p42635402192629"></a><a name="p42635402192629"></a>meta</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.7023702370237%" headers="mcps1.1.4.1.2 "><p id="p30915509192629"><a name="p30915509192629"></a><a name="p30915509192629"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38523852385239%" headers="mcps1.1.4.1.3 "><p id="p55937021192629"><a name="p55937021192629"></a><a name="p55937021192629"></a>用户自定义metadata键值对。详情请参见<a href="#table34604820192629">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  meta字段数据结构说明

    <a name="table34604820192629"></a>
    <table><thead align="left"><tr id="row41672406192629"><th class="cellrowborder" valign="top" width="24.26%" id="mcps1.2.4.1.1"><p id="p168451154608"><a name="p168451154608"></a><a name="p168451154608"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.26%" id="mcps1.2.4.1.2"><p id="p158471654902"><a name="p158471654902"></a><a name="p158471654902"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.480000000000004%" id="mcps1.2.4.1.3"><p id="p6848125412010"><a name="p6848125412010"></a><a name="p6848125412010"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row64139640192629"><td class="cellrowborder" valign="top" width="24.26%" headers="mcps1.2.4.1.1 "><p id="p27928340192629"><a name="p27928340192629"></a><a name="p27928340192629"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.26%" headers="mcps1.2.4.1.2 "><p id="p47603028192629"><a name="p47603028192629"></a><a name="p47603028192629"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.480000000000004%" headers="mcps1.2.4.1.3 "><p id="p30640032192629"><a name="p30640032192629"></a><a name="p30640032192629"></a>用户自定义metadata键值对。</p>
    <p id="p16870474174442"><a name="p16870474174442"></a><a name="p16870474174442"></a>键、值长度均不大于255字节。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "meta": {
            "key": "value"
        }
    } 
    ```


## 返回值<a name="section7610951"></a>

正常返回值：

<a name="zh-cn_topic_0106040941_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0106040941_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0106040941_p19735204616177"><a name="zh-cn_topic_0106040941_p19735204616177"></a><a name="zh-cn_topic_0106040941_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0106040941_p207355465176"><a name="zh-cn_topic_0106040941_p207355465176"></a><a name="zh-cn_topic_0106040941_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0106040941_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0106040941_p13735144611178"><a name="zh-cn_topic_0106040941_p13735144611178"></a><a name="zh-cn_topic_0106040941_p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0106040941_p207351246161711"><a name="zh-cn_topic_0106040941_p207351246161711"></a><a name="zh-cn_topic_0106040941_p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

