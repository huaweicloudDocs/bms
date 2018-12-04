# 查询裸金属服务器元数据（OpenStack原生）<a name="ZH-CN_TOPIC_0060402469"></a>

## 功能介绍<a name="section61558535185333"></a>

查询裸金属服务器元数据。

## 约束<a name="section57278039123222"></a>

不支持分页查询。

## URI<a name="section47451206185333"></a>

GET  /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table3831319143216)。

**表 1**  参数说明

<a name="table3831319143216"></a>
<table><thead align="left"><tr id="row38322019153219"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p49662088185333"><a name="p49662088185333"></a><a name="p49662088185333"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p63206191185333"><a name="p63206191185333"></a><a name="p63206191185333"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p19427838185333"><a name="p19427838185333"></a><a name="p19427838185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15832181913211"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p26317623185333"><a name="p26317623185333"></a><a name="p26317623185333"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p51352688185333"><a name="p51352688185333"></a><a name="p51352688185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p65927025185333"><a name="p65927025185333"></a><a name="p65927025185333"></a>项目ID。</p>
</td>
</tr>
<tr id="row78321619103218"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p10854909185333"><a name="p10854909185333"></a><a name="p10854909185333"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6832475185333"><a name="p6832475185333"></a><a name="p6832475185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p16559613185333"><a name="p16559613185333"></a><a name="p16559613185333"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section14818796185333"></a>

不涉及。

## 响应消息<a name="section22254218185333"></a>

-   响应参数

    <a name="table48150236185333"></a>
    <table><thead align="left"><tr id="row64499137185333"><th class="cellrowborder" valign="top" width="22.259999999999998%" id="mcps1.1.4.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.24%" id="mcps1.1.4.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.50000000000001%" id="mcps1.1.4.1.3"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row51055328185333"><td class="cellrowborder" valign="top" width="22.259999999999998%" headers="mcps1.1.4.1.1 "><p id="p41840919185333"><a name="p41840919185333"></a><a name="p41840919185333"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.1.4.1.2 "><p id="p33671307185333"><a name="p33671307185333"></a><a name="p33671307185333"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.50000000000001%" headers="mcps1.1.4.1.3 "><p id="p51647808185333"><a name="p51647808185333"></a><a name="p51647808185333"></a>用户自定义metadata键值对。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] metadata字段数据结构说明

    <a name="table22722954185333"></a>
    <table><thead align="left"><tr id="row5305371185333"><th class="cellrowborder" valign="top" width="22.957704229577043%" id="mcps1.1.4.1.1"><p id="p1640481205915"><a name="p1640481205915"></a><a name="p1640481205915"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.467853214678534%" id="mcps1.1.4.1.2"><p id="p1440581220594"><a name="p1440581220594"></a><a name="p1440581220594"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.57444255574442%" id="mcps1.1.4.1.3"><p id="p1340841217596"><a name="p1340841217596"></a><a name="p1340841217596"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2696702185333"><td class="cellrowborder" valign="top" width="22.957704229577043%" headers="mcps1.1.4.1.1 "><p id="p17106284185333"><a name="p17106284185333"></a><a name="p17106284185333"></a>用户自定义字段键值对</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.467853214678534%" headers="mcps1.1.4.1.2 "><p id="p43431730185333"><a name="p43431730185333"></a><a name="p43431730185333"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57444255574442%" headers="mcps1.1.4.1.3 "><p id="p5719410617654"><a name="p5719410617654"></a><a name="p5719410617654"></a>metadata键、值。</p>
    <p id="p4498490617654"><a name="p4498490617654"></a><a name="p4498490617654"></a>键、值长度均不大于255字节。</p>
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

