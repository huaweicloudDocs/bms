# 查询裸金属服务器标签（OpenStack原生）<a name="ZH-CN_TOPIC_0060410926"></a>

## 功能介绍<a name="section17769131"></a>

查询裸金属服务器的所有标签。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="section40393097103718"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#table0142163245812)。

**表 1**  参数说明

<a name="table0142163245812"></a>
<table><thead align="left"><tr id="row51434323581"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p67050730103718"><a name="p67050730103718"></a><a name="p67050730103718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p62400032103718"><a name="p62400032103718"></a><a name="p62400032103718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p21237868103718"><a name="p21237868103718"></a><a name="p21237868103718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row01430322585"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p23650911103718"><a name="p23650911103718"></a><a name="p23650911103718"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p36675672103718"><a name="p36675672103718"></a><a name="p36675672103718"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p17939461103718"><a name="p17939461103718"></a><a name="p17939461103718"></a>项目ID。</p>
</td>
</tr>
<tr id="row1114316327585"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p18738546141829"><a name="p18738546141829"></a><a name="p18738546141829"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p41427238141829"><a name="p41427238141829"></a><a name="p41427238141829"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p163111141829"><a name="p163111141829"></a><a name="p163111141829"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section43810255103718"></a>

不涉及。

## 响应消息<a name="section60965769103718"></a>

-   响应参数

    <a name="table48150236185333"></a>
    <table><thead align="left"><tr id="row64499137185333"><th class="cellrowborder" valign="top" width="23.169999999999998%" id="mcps1.1.4.1.1"><p id="p19987085"><a name="p19987085"></a><a name="p19987085"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.169999999999998%" id="mcps1.1.4.1.2"><p id="p4546697"><a name="p4546697"></a><a name="p4546697"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.66%" id="mcps1.1.4.1.3"><p id="p32738149"><a name="p32738149"></a><a name="p32738149"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row51055328185333"><td class="cellrowborder" valign="top" width="23.169999999999998%" headers="mcps1.1.4.1.1 "><p id="p41840919185333"><a name="p41840919185333"></a><a name="p41840919185333"></a>tags</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.169999999999998%" headers="mcps1.1.4.1.2 "><p id="p33671307185333"><a name="p33671307185333"></a><a name="p33671307185333"></a>list &lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.66%" headers="mcps1.1.4.1.3 "><p id="p51647808185333"><a name="p51647808185333"></a><a name="p51647808185333"></a>用户自定义标签列表。</p>
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


## 返回值<a name="section29598436103718"></a>

请参考[通用返回值](通用返回值.md)。

