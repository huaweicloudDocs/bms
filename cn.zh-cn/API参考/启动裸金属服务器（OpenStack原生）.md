# 启动裸金属服务器（OpenStack原生）<a name="ZH-CN_TOPIC_0053158659"></a>

## 功能介绍<a name="section5894231"></a>

启动单台裸金属服务器。

## URI<a name="section53048087"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table15103162717019)。

**表 1**  参数说明

<a name="table15103162717019"></a>
<table><thead align="left"><tr id="row6103127604"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p53294272"><a name="p53294272"></a><a name="p53294272"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p21868813"><a name="p21868813"></a><a name="p21868813"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p26543418"><a name="p26543418"></a><a name="p26543418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row201031271407"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p3865173"><a name="p3865173"></a><a name="p3865173"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p44643603"><a name="p44643603"></a><a name="p44643603"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p59362130"><a name="p59362130"></a><a name="p59362130"></a>项目ID。</p>
</td>
</tr>
<tr id="row111036271506"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p56885004"><a name="p56885004"></a><a name="p56885004"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p44282627"><a name="p44282627"></a><a name="p44282627"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p30123063"><a name="p30123063"></a><a name="p30123063"></a>裸金属服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section7670737"></a>

-   请求参数

    <a name="table48180537"></a>
    <table><thead align="left"><tr id="row15499871"><th class="cellrowborder" valign="top" width="15.83%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.06%" id="mcps1.1.5.1.2"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.260000000000002%" id="mcps1.1.5.1.3"><p id="p59616187115233"><a name="p59616187115233"></a><a name="p59616187115233"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.849999999999994%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54897010"><td class="cellrowborder" valign="top" width="15.83%" headers="mcps1.1.5.1.1 "><p id="p17472816"><a name="p17472816"></a><a name="p17472816"></a>os-start</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.06%" headers="mcps1.1.5.1.2 "><p id="p17209562"><a name="p17209562"></a><a name="p17209562"></a>空结构体</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.260000000000002%" headers="mcps1.1.5.1.3 "><p id="p2419366181021"><a name="p2419366181021"></a><a name="p2419366181021"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.849999999999994%" headers="mcps1.1.5.1.4 "><p id="p63522246"><a name="p63522246"></a><a name="p63522246"></a>标记为启动裸金属服务器操作，数据结构为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    ```
    {
        "os-start": {}
    }
    ```


## 响应消息<a name="section1927776"></a>

不涉及。

## 返回值<a name="section17349988"></a>

请参考[通用返回值](通用返回值.md)。

