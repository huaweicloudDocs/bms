# 启动裸金属服务器（OpenStack原生）<a name="ZH-CN_TOPIC_0053158659"></a>

## 功能介绍<a name="section5894231"></a>

启动单台裸金属服务器。

## URI<a name="section53048087"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table15103162717019)。

**表 1**  参数说明

<a name="table15103162717019"></a>
<table><thead align="left"><tr id="row6103127604"><th class="cellrowborder" valign="top" width="26.182618261826185%" id="mcps1.2.4.1.1"><p id="p53294272"><a name="p53294272"></a><a name="p53294272"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.302530253025306%" id="mcps1.2.4.1.2"><p id="p21868813"><a name="p21868813"></a><a name="p21868813"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.51485148514852%" id="mcps1.2.4.1.3"><p id="p26543418"><a name="p26543418"></a><a name="p26543418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row201031271407"><td class="cellrowborder" valign="top" width="26.182618261826185%" headers="mcps1.2.4.1.1 "><p id="p3865173"><a name="p3865173"></a><a name="p3865173"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.302530253025306%" headers="mcps1.2.4.1.2 "><p id="p44643603"><a name="p44643603"></a><a name="p44643603"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.51485148514852%" headers="mcps1.2.4.1.3 "><p id="p59362130"><a name="p59362130"></a><a name="p59362130"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row111036271506"><td class="cellrowborder" valign="top" width="26.182618261826185%" headers="mcps1.2.4.1.1 "><p id="p56885004"><a name="p56885004"></a><a name="p56885004"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.302530253025306%" headers="mcps1.2.4.1.2 "><p id="p44282627"><a name="p44282627"></a><a name="p44282627"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.51485148514852%" headers="mcps1.2.4.1.3 "><p id="p30123063"><a name="p30123063"></a><a name="p30123063"></a><span id="text1001475119"><a name="text1001475119"></a><a name="text1001475119"></a>裸金属服务器</span><span id="text9024761115"><a name="text9024761115"></a><a name="text9024761115"></a></span>ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section7670737"></a>

-   请求参数

    <a name="table48180537"></a>
    <table><thead align="left"><tr id="row15499871"><th class="cellrowborder" valign="top" width="19.2%" id="mcps1.1.5.1.1"><p id="p59978491115233"><a name="p59978491115233"></a><a name="p59978491115233"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.41%" id="mcps1.1.5.1.2"><p id="p17403183919111"><a name="p17403183919111"></a><a name="p17403183919111"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.340000000000002%" id="mcps1.1.5.1.3"><p id="p26419641115233"><a name="p26419641115233"></a><a name="p26419641115233"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.05%" id="mcps1.1.5.1.4"><p id="p64181866115233"><a name="p64181866115233"></a><a name="p64181866115233"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54897010"><td class="cellrowborder" valign="top" width="19.2%" headers="mcps1.1.5.1.1 "><p id="p17472816"><a name="p17472816"></a><a name="p17472816"></a>os-start</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.41%" headers="mcps1.1.5.1.2 "><p id="p74009391212"><a name="p74009391212"></a><a name="p74009391212"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.340000000000002%" headers="mcps1.1.5.1.3 "><p id="p17209562"><a name="p17209562"></a><a name="p17209562"></a>null</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.05%" headers="mcps1.1.5.1.4 "><p id="p63522246"><a name="p63522246"></a><a name="p63522246"></a>标记为启动<span id="text5483653171111"><a name="text5483653171111"></a><a name="text5483653171111"></a>裸金属服务器</span><span id="text1348315319117"><a name="text1348315319117"></a><a name="text1348315319117"></a></span>操作，数据结构为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    ```
    POST https://{ECS Endpoint}/v2.1/c685484a8cc2416b97260938705deb65/servers/95bf2490-5428-432c-ad9b-5e3406f869dd/action
    ```

    ```
    {
        "os-start": {}
    }
    ```


## 响应消息<a name="section1927776"></a>

不涉及。

## 返回值<a name="section17349988"></a>

正常返回值：

<a name="table753804619176"></a>
<table><thead align="left"><tr id="row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="p19735204616177"><a name="p19735204616177"></a><a name="p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="p207355465176"><a name="p207355465176"></a><a name="p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="p13735144611178"><a name="p13735144611178"></a><a name="p13735144611178"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="p81516575011"><a name="p81516575011"></a><a name="p81516575011"></a>服务器成功处理了请求，但没有返回任何内容。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section14752650154917"></a>

请参考[错误码](错误码.md)。

