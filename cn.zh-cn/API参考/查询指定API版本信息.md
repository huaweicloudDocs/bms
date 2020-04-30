# 查询指定API版本信息<a name="ZH-CN_TOPIC_0132973805"></a>

## 功能介绍<a name="section553655182144"></a>

查询裸金属服务指定API版本的信息。

## URI<a name="section961608182144"></a>

GET /\{api\_version\}

参数说明请参见[表1](#table46110007)。

**表 1**  参数说明

<a name="table46110007"></a>
<table><thead align="left"><tr id="row14148614"><th class="cellrowborder" valign="top" width="27.650000000000002%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.339999999999996%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="45.01%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17201924"><td class="cellrowborder" valign="top" width="27.650000000000002%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>api_version</p>
</td>
<td class="cellrowborder" valign="top" width="27.339999999999996%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="45.01%" headers="mcps1.2.4.1.3 "><p id="p37195178"><a name="p37195178"></a><a name="p37195178"></a>API版本号。例如：v1</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section19667838182144"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/v1
    ```


## 响应消息<a name="section43666554182144"></a>

-   响应参数

    <a name="table59665636"></a>
    <table><thead align="left"><tr id="row28755990"><th class="cellrowborder" valign="top" width="26.72267226722672%" id="mcps1.1.4.1.1"><p id="p47533853"><a name="p47533853"></a><a name="p47533853"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.802780278027804%" id="mcps1.1.4.1.2"><p id="p25036876"><a name="p25036876"></a><a name="p25036876"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.474547454745476%" id="mcps1.1.4.1.3"><p id="p14721100"><a name="p14721100"></a><a name="p14721100"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34736162"><td class="cellrowborder" valign="top" width="26.72267226722672%" headers="mcps1.1.4.1.1 "><p id="p1654215818362"><a name="p1654215818362"></a><a name="p1654215818362"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.802780278027804%" headers="mcps1.1.4.1.2 "><p id="p2257160"><a name="p2257160"></a><a name="p2257160"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.474547454745476%" headers="mcps1.1.4.1.3 "><p id="p48612303"><a name="p48612303"></a><a name="p48612303"></a>描述裸金属服务器API指定版本信息。详情请参见<a href="#table786171513527">表2</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  version字段数据结构说明

    <a name="table786171513527"></a>
    <table><thead align="left"><tr id="row16870715205219"><th class="cellrowborder" valign="top" width="26.619999999999997%" id="mcps1.2.4.1.1"><p id="p787314157521"><a name="p787314157521"></a><a name="p787314157521"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.13%" id="mcps1.2.4.1.2"><p id="p15875415185216"><a name="p15875415185216"></a><a name="p15875415185216"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.25%" id="mcps1.2.4.1.3"><p id="p1487831516528"><a name="p1487831516528"></a><a name="p1487831516528"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1288051545213"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p198824151526"><a name="p198824151526"></a><a name="p198824151526"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p4884915105217"><a name="p4884915105217"></a><a name="p4884915105217"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p088519150526"><a name="p088519150526"></a><a name="p088519150526"></a>API版本ID。</p>
    </td>
    </tr>
    <tr id="row8887191525212"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p9888151505213"><a name="p9888151505213"></a><a name="p9888151505213"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p1489112150526"><a name="p1489112150526"></a><a name="p1489112150526"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p1894161514527"><a name="p1894161514527"></a><a name="p1894161514527"></a>API的url地址。详情请参见<a href="#t759e6d15d244474e8f286185ede143fb">表3</a>。</p>
    </td>
    </tr>
    <tr id="row20895111565214"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p9107111411399"><a name="p9107111411399"></a><a name="p9107111411399"></a>min_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p58981015115218"><a name="p58981015115218"></a><a name="p58981015115218"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p19907734114018"><a name="p19907734114018"></a><a name="p19907734114018"></a>API支持的最小微版本号。</p>
    </td>
    </tr>
    <tr id="row9901141525214"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p3903415185215"><a name="p3903415185215"></a><a name="p3903415185215"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p390610159525"><a name="p390610159525"></a><a name="p390610159525"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p4907191535213"><a name="p4907191535213"></a><a name="p4907191535213"></a>API版本状态：</p>
    <a name="ul19909615185218"></a><a name="ul19909615185218"></a><ul id="ul19909615185218"><li>CURRENT：表示该版本为主推版本。</li><li>SUPPORTED：表示为老版本，但是现在还在继续支持。</li><li>DEPRECATED：表示为废弃版本，存在后续删除的可能。</li></ul>
    </td>
    </tr>
    <tr id="row149151915105212"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p4918715155215"><a name="p4918715155215"></a><a name="p4918715155215"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p892011518520"><a name="p892011518520"></a><a name="p892011518520"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p1255911034615"><a name="p1255911034615"></a><a name="p1255911034615"></a>API版本发布时间。</p>
    <p id="p19899173431114"><a name="p19899173431114"></a><a name="p19899173431114"></a>时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2018-09-30T00:00:00Z</p>
    </td>
    </tr>
    <tr id="row17923151519525"><td class="cellrowborder" valign="top" width="26.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p1892416155523"><a name="p1892416155523"></a><a name="p1892416155523"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.13%" headers="mcps1.2.4.1.2 "><p id="p16926191511523"><a name="p16926191511523"></a><a name="p16926191511523"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.25%" headers="mcps1.2.4.1.3 "><p id="p12928215185216"><a name="p12928215185216"></a><a name="p12928215185216"></a>API支持的最大微版本号。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  links字段数据结构说明

    <a name="t759e6d15d244474e8f286185ede143fb"></a>
    <table><thead align="left"><tr id="rce98b9668cd747c88039421afe5ce935"><th class="cellrowborder" valign="top" width="26.51%" id="mcps1.2.4.1.1"><p id="ad9ac3007570a4752b2b2dbc0fb04dadc"><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.660000000000004%" id="mcps1.2.4.1.2"><p id="a602246198adf4a79a13bc4317d4c0d4f"><a name="a602246198adf4a79a13bc4317d4c0d4f"></a><a name="a602246198adf4a79a13bc4317d4c0d4f"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.83%" id="mcps1.2.4.1.3"><p id="a8cbfa8dcb0b943ff8e789755123fec83"><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r43de461181294c56b28da56a1f604b09"><td class="cellrowborder" valign="top" width="26.51%" headers="mcps1.2.4.1.1 "><p id="abc19a41a8f594f1ba6701e10da50a078"><a name="abc19a41a8f594f1ba6701e10da50a078"></a><a name="abc19a41a8f594f1ba6701e10da50a078"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.660000000000004%" headers="mcps1.2.4.1.2 "><p id="a15ae7b8585d24e48abc6b9bf45636fda"><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.83%" headers="mcps1.2.4.1.3 "><p id="p139393206480"><a name="p139393206480"></a><a name="p139393206480"></a>API的url地址。</p>
    </td>
    </tr>
    <tr id="rbd5ec7242fef4c03b21636ac14160d9e"><td class="cellrowborder" valign="top" width="26.51%" headers="mcps1.2.4.1.1 "><p id="a18479f6b70b34f29b2b90d754f59282a"><a name="a18479f6b70b34f29b2b90d754f59282a"></a><a name="a18479f6b70b34f29b2b90d754f59282a"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.660000000000004%" headers="mcps1.2.4.1.2 "><p id="ae1f14fa2e6a54531aeffd26874fea267"><a name="ae1f14fa2e6a54531aeffd26874fea267"></a><a name="ae1f14fa2e6a54531aeffd26874fea267"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.83%" headers="mcps1.2.4.1.3 "><p id="p115877381483"><a name="p115877381483"></a><a name="p115877381483"></a>API的url地址依赖。取值为：</p>
    <a name="ul207311644172510"></a><a name="ul207311644172510"></a><ul id="ul207311644172510"><li>self：包含版本号的资源链接，需要立即跟踪时使用此类链接。</li><li>bookmark：提供了适合长期存储的资源链接。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "version": {
            "id": "v1",
            "links": [
                {
                    "href": "http://bms.xxx.com/v1/",
                    "rel": "self"
                }
            ],
            "min_version": "",
            "status": "CURRENT",
            "updated": "2018-09-30T00:00:00Z",
            "version": ""
        }
    }
    ```


## 返回值<a name="section12571834"></a>

正常返回值：

<a name="zh-cn_topic_0132973804_table753804619176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0132973804_row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0132973804_p19735204616177"><a name="zh-cn_topic_0132973804_p19735204616177"></a><a name="zh-cn_topic_0132973804_p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0132973804_p207355465176"><a name="zh-cn_topic_0132973804_p207355465176"></a><a name="zh-cn_topic_0132973804_p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0132973804_row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0132973804_p13735144611178"><a name="zh-cn_topic_0132973804_p13735144611178"></a><a name="zh-cn_topic_0132973804_p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0132973804_p207351246161711"><a name="zh-cn_topic_0132973804_p207351246161711"></a><a name="zh-cn_topic_0132973804_p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section12157147171520"></a>

请参考[错误码](错误码.md)。

