# 为裸金属服务器添加标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060410927"></a>

## 功能介绍<a name="section59539732104217"></a>

为裸金属服务器添加标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## 约束<a name="section12956040151655"></a>

标签个数不超过50个。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   建议为裸金属服务器添加“\_\_type\_baremetal”标签，标识是一台裸金属服务器。否则，裸金属服务器将仅在ECS控制台可见，而不在BMS控制台中。  
>-   新增标签时，会覆盖原有标签。如需保留原有标签，请在添加时，将原有标签加入到新增标签的列表中。建议每次添加标签时，将“\_\_type\_baremetal”放在请求新增的tags列表中。  

## URI<a name="section52138884104217"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#table7714219185912)。

**表 1**  参数说明

<a name="table7714219185912"></a>
<table><thead align="left"><tr id="row1271511905917"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p17653616104217"><a name="p17653616104217"></a><a name="p17653616104217"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p20656767104217"><a name="p20656767104217"></a><a name="p20656767104217"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p62585419104217"><a name="p62585419104217"></a><a name="p62585419104217"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row12715101918599"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p50904119104217"><a name="p50904119104217"></a><a name="p50904119104217"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p29593000104217"><a name="p29593000104217"></a><a name="p29593000104217"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p48222838104217"><a name="p48222838104217"></a><a name="p48222838104217"></a>项目ID。</p>
</td>
</tr>
<tr id="row107151219135910"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p56513487104217"><a name="p56513487104217"></a><a name="p56513487104217"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p14189698104217"><a name="p14189698104217"></a><a name="p14189698104217"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p8514927104217"><a name="p8514927104217"></a><a name="p8514927104217"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section18620476104217"></a>

-   请求参数

    <a name="table40018745105534"></a>
    <table><thead align="left"><tr id="row48164488105534"><th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.1"><p id="p19987085"><a name="p19987085"></a><a name="p19987085"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.1.5.1.2"><p id="p4546697"><a name="p4546697"></a><a name="p4546697"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.3"><p id="p23972980183956"><a name="p23972980183956"></a><a name="p23972980183956"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="42%" id="mcps1.1.5.1.4"><p id="p32738149"><a name="p32738149"></a><a name="p32738149"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6972410105534"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.1 "><p id="p27894300105534"><a name="p27894300105534"></a><a name="p27894300105534"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.2 "><p id="p8634695105534"><a name="p8634695105534"></a><a name="p8634695105534"></a>list &lt;string&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><p id="p33309670185828"><a name="p33309670185828"></a><a name="p33309670185828"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="42%" headers="mcps1.1.5.1.4 "><a name="ul1785812112408"></a><a name="ul1785812112408"></a><ul id="ul1785812112408"><li>标签列表，每个标签不超过80个字符。</li><li>标签不能以“.”开头。</li><li>标签个数不超过50个。</li><li>不支持创建空标签（空串）。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    ```
    {
        "tags": [
            "baz",
            "foo",
            "qux"
        ]
    }
    ```


## 响应消息<a name="section6196486814321"></a>

-   响应参数

    <a name="table600597414321"></a>
    <table><thead align="left"><tr id="row5646441114321"><th class="cellrowborder" valign="top" width="23.169999999999998%" id="mcps1.1.4.1.1"><p id="p2639349142614"><a name="p2639349142614"></a><a name="p2639349142614"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.61%" id="mcps1.1.4.1.2"><p id="p13639114902610"><a name="p13639114902610"></a><a name="p13639114902610"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.22%" id="mcps1.1.4.1.3"><p id="p1864164972614"><a name="p1864164972614"></a><a name="p1864164972614"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4038057614321"><td class="cellrowborder" valign="top" width="23.169999999999998%" headers="mcps1.1.4.1.1 "><p id="p4960123314321"><a name="p4960123314321"></a><a name="p4960123314321"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.61%" headers="mcps1.1.4.1.2 "><p id="p5827693814321"><a name="p5827693814321"></a><a name="p5827693814321"></a>list &lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.22%" headers="mcps1.1.4.1.3 "><p id="p2281157214321"><a name="p2281157214321"></a><a name="p2281157214321"></a>用户自定义标签列表。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "tags": [
            "baz",
            "foo",
            "qux"
        ]
    }
    ```


## 返回值<a name="section57884614"></a>

请参考[通用返回值](通用返回值.md)。

