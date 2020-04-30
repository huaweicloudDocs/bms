# Windows裸金属服务器获取密码<a name="ZH-CN_TOPIC_0131629816"></a>

## 功能介绍<a name="section57769674"></a>

获取Windows裸金属服务器初始安装时系统生成的管理员帐户（Administrator帐户或Cloudbase-init设置的帐户）随机密码。

如果裸金属服务器是通过私有镜像创建的，请确保已安装Cloudbase-init。公共镜像默认已安装该软件。

## URI<a name="section50165025"></a>

GET /v1/\{project\_id\}/baremetalservers/\{server\_id\}/os-server-password

参数说明请参见[表1](#table23262209)。

**表 1**  参数说明

<a name="table23262209"></a>
<table><thead align="left"><tr id="row32406826"><th class="cellrowborder" valign="top" width="24.112411241124114%" id="mcps1.2.4.1.1"><p id="p7707213"><a name="p7707213"></a><a name="p7707213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.7022702270227%" id="mcps1.2.4.1.2"><p id="p20304554"><a name="p20304554"></a><a name="p20304554"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="53.185318531853184%" id="mcps1.2.4.1.3"><p id="p34056167"><a name="p34056167"></a><a name="p34056167"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row7086124"><td class="cellrowborder" valign="top" width="24.112411241124114%" headers="mcps1.2.4.1.1 "><p id="p37105186"><a name="p37105186"></a><a name="p37105186"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.7022702270227%" headers="mcps1.2.4.1.2 "><p id="p52730096"><a name="p52730096"></a><a name="p52730096"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.185318531853184%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row1829803718504"><td class="cellrowborder" valign="top" width="24.112411241124114%" headers="mcps1.2.4.1.1 "><p id="p183003372507"><a name="p183003372507"></a><a name="p183003372507"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.7022702270227%" headers="mcps1.2.4.1.2 "><p id="p5300113705012"><a name="p5300113705012"></a><a name="p5300113705012"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.185318531853184%" headers="mcps1.2.4.1.3 "><p id="p830083715506"><a name="p830083715506"></a><a name="p830083715506"></a>裸金属服务器ID。</p>
<p id="p29791113277"><a name="p29791113277"></a><a name="p29791113277"></a>可以从<span id="zh-cn_topic_0113746489_text013014803615"><a name="zh-cn_topic_0113746489_text013014803615"></a><a name="zh-cn_topic_0113746489_text013014803615"></a>裸金属服务器</span><span id="zh-cn_topic_0113746489_text10131448133612"><a name="zh-cn_topic_0113746489_text10131448133612"></a><a name="zh-cn_topic_0113746489_text10131448133612"></a></span>控制台查询，或者通过调用<a href="查询裸金属服务器列表（OpenStack原生）.md">查询裸金属服务器列表（OpenStack原生）</a>API获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section12542250184015"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/v1/bbf1946d374b44a0a2a95533562ba954/baremetalservers/cf2a8b97-b5c6-47ef-9714-eb27adf26e5b/os-server-password
    ```


## 响应消息<a name="section36835188"></a>

-   响应参数

    <a name="table23477058"></a>
    <table><thead align="left"><tr id="row2792905"><th class="cellrowborder" valign="top" width="28.532853285328528%" id="mcps1.1.4.1.1"><p id="p24898733"><a name="p24898733"></a><a name="p24898733"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.722572257225725%" id="mcps1.1.4.1.2"><p id="p17614915"><a name="p17614915"></a><a name="p17614915"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.744574457445744%" id="mcps1.1.4.1.3"><p id="p17521988"><a name="p17521988"></a><a name="p17521988"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row9994955"><td class="cellrowborder" valign="top" width="28.532853285328528%" headers="mcps1.1.4.1.1 "><p id="p4284989"><a name="p4284989"></a><a name="p4284989"></a>password</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.722572257225725%" headers="mcps1.1.4.1.2 "><p id="p62312200"><a name="p62312200"></a><a name="p62312200"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.744574457445744%" headers="mcps1.1.4.1.3 "><p id="p60002101"><a name="p60002101"></a><a name="p60002101"></a>加密后的密码。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "password": "UHC9+YW1xDC1Yu8Mg9n+tnOp7euEO/cW//9KgdJKWhr5w=="
    }
    ```


## 返回值<a name="section868814916514"></a>

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

