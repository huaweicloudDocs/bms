# 查询API版本信息列表<a name="ZH-CN_TOPIC_0132973804"></a>

## 功能介绍<a name="section54478915181842"></a>

查询裸金属服务器当前所有可用的API版本。

## URI<a name="section53791107181842"></a>

GET /

## 请求消息<a name="section39878380181842"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/
    ```


## 响应消息<a name="section201868180299"></a>

-   响应参数

    <a name="table59665636"></a>
    <table><thead align="left"><tr id="row28755990"><th class="cellrowborder" valign="top" width="23.71%" id="mcps1.1.4.1.1"><p id="p47533853"><a name="p47533853"></a><a name="p47533853"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.52%" id="mcps1.1.4.1.2"><p id="p25036876"><a name="p25036876"></a><a name="p25036876"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.769999999999996%" id="mcps1.1.4.1.3"><p id="p14721100"><a name="p14721100"></a><a name="p14721100"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34736162"><td class="cellrowborder" valign="top" width="23.71%" headers="mcps1.1.4.1.1 "><p id="p1654215818362"><a name="p1654215818362"></a><a name="p1654215818362"></a>versions</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.52%" headers="mcps1.1.4.1.2 "><p id="p2257160"><a name="p2257160"></a><a name="p2257160"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.769999999999996%" headers="mcps1.1.4.1.3 "><p id="p48612303"><a name="p48612303"></a><a name="p48612303"></a>描述裸金属服务器API版本信息列表。详情请参见<a href="#table5036780310489">表1</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 1**  versions字段数据结构说明

    <a name="table5036780310489"></a>
    <table><thead align="left"><tr id="r1f3f90a6acc94015acc80b9d6b53f072"><th class="cellrowborder" valign="top" width="24.14%" id="mcps1.2.4.1.1"><p id="ad0d15c1370cb450fb7e6011b8baff160"><a name="ad0d15c1370cb450fb7e6011b8baff160"></a><a name="ad0d15c1370cb450fb7e6011b8baff160"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.31%" id="mcps1.2.4.1.2"><p id="a2273dfb9dd3341b0b5cbf801a0aa70fc"><a name="a2273dfb9dd3341b0b5cbf801a0aa70fc"></a><a name="a2273dfb9dd3341b0b5cbf801a0aa70fc"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.55%" id="mcps1.2.4.1.3"><p id="a479b45e1fbfc44118151c43b5ecb82f1"><a name="a479b45e1fbfc44118151c43b5ecb82f1"></a><a name="a479b45e1fbfc44118151c43b5ecb82f1"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rdd24623b54f94a86b0f655ec659180e9"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="ab9c8eb8b964943509fca83cc70a4e489"><a name="ab9c8eb8b964943509fca83cc70a4e489"></a><a name="ab9c8eb8b964943509fca83cc70a4e489"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="a43cc5f338c7e429c861f7dbb2dcb3229"><a name="a43cc5f338c7e429c861f7dbb2dcb3229"></a><a name="a43cc5f338c7e429c861f7dbb2dcb3229"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="a5c153a8f0b8d4f26af1405cdcbcec1cc"><a name="a5c153a8f0b8d4f26af1405cdcbcec1cc"></a><a name="a5c153a8f0b8d4f26af1405cdcbcec1cc"></a>API版本ID。</p>
    </td>
    </tr>
    <tr id="r784e679e20ef42c7b5f0d9caebb3d506"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="af5650be6710143e49d288b78f41a9c9d"><a name="af5650be6710143e49d288b78f41a9c9d"></a><a name="af5650be6710143e49d288b78f41a9c9d"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="aa41878c3fbc74f52be50c47e0dd26a46"><a name="aa41878c3fbc74f52be50c47e0dd26a46"></a><a name="aa41878c3fbc74f52be50c47e0dd26a46"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="a37d79d061a9f47c5beee1f98f4c4611b"><a name="a37d79d061a9f47c5beee1f98f4c4611b"></a><a name="a37d79d061a9f47c5beee1f98f4c4611b"></a>API的url地址。详情请参见<a href="#t759e6d15d244474e8f286185ede143fb">表2</a>。</p>
    </td>
    </tr>
    <tr id="r06fe5129bbc1493289f623afe4a4f1a2"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="p9107111411399"><a name="p9107111411399"></a><a name="p9107111411399"></a>min_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="a89734c8a12d44d69ab229cf5857bdf05"><a name="a89734c8a12d44d69ab229cf5857bdf05"></a><a name="a89734c8a12d44d69ab229cf5857bdf05"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="p19907734114018"><a name="p19907734114018"></a><a name="p19907734114018"></a>API支持的最小微版本号。</p>
    </td>
    </tr>
    <tr id="rac189e8b65c5430eb4503bf1d1bbb4d7"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="ab5c5c2b93a134f18a2455224014556e9"><a name="ab5c5c2b93a134f18a2455224014556e9"></a><a name="ab5c5c2b93a134f18a2455224014556e9"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="a2de7247f99c143e09e698f0ef82f62bc"><a name="a2de7247f99c143e09e698f0ef82f62bc"></a><a name="a2de7247f99c143e09e698f0ef82f62bc"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="a65ce06cd4813480498062e1de2541bd3"><a name="a65ce06cd4813480498062e1de2541bd3"></a><a name="a65ce06cd4813480498062e1de2541bd3"></a>API版本状态：</p>
    <a name="ud3dc362d60f54fc08039ec57e921e5a6"></a><a name="ud3dc362d60f54fc08039ec57e921e5a6"></a><ul id="ud3dc362d60f54fc08039ec57e921e5a6"><li>CURRENT：表示该版本为主推版本。</li><li>SUPPORTED：表示为老版本，但是现在还在继续支持。</li><li>DEPRECATED：表示为废弃版本，存在后续删除的可能。</li></ul>
    </td>
    </tr>
    <tr id="r4dfedc0bd4ff45f2ac05364f99f01708"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="a306f2c2ef05e47f78c5e0fc5440cea3c"><a name="a306f2c2ef05e47f78c5e0fc5440cea3c"></a><a name="a306f2c2ef05e47f78c5e0fc5440cea3c"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="a979f525a997c4d1e8808195ca9d7f53e"><a name="a979f525a997c4d1e8808195ca9d7f53e"></a><a name="a979f525a997c4d1e8808195ca9d7f53e"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="p1255911034615"><a name="p1255911034615"></a><a name="p1255911034615"></a>API版本发布时间。</p>
    <p id="p9711133519711"><a name="p9711133519711"></a><a name="p9711133519711"></a>时间戳格式为ISO 8601：YYYY-MM-DDTHH:MM:SSZ，例如：2018-09-30T00:00:00Z</p>
    </td>
    </tr>
    <tr id="r45a3cc4c3f6943639ac3843c688f6865"><td class="cellrowborder" valign="top" width="24.14%" headers="mcps1.2.4.1.1 "><p id="a52a9f640ec724f40a4829ddf066e0837"><a name="a52a9f640ec724f40a4829ddf066e0837"></a><a name="a52a9f640ec724f40a4829ddf066e0837"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.31%" headers="mcps1.2.4.1.2 "><p id="a015154a0e4094475a717b23650fa6cf1"><a name="a015154a0e4094475a717b23650fa6cf1"></a><a name="a015154a0e4094475a717b23650fa6cf1"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.55%" headers="mcps1.2.4.1.3 "><p id="adefe07f521ca4e0aab9007ea28bebc7d"><a name="adefe07f521ca4e0aab9007ea28bebc7d"></a><a name="adefe07f521ca4e0aab9007ea28bebc7d"></a>API支持的最大微版本号。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  links字段数据结构说明

    <a name="t759e6d15d244474e8f286185ede143fb"></a>
    <table><thead align="left"><tr id="rce98b9668cd747c88039421afe5ce935"><th class="cellrowborder" valign="top" width="24.25%" id="mcps1.2.4.1.1"><p id="ad9ac3007570a4752b2b2dbc0fb04dadc"><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a><a name="ad9ac3007570a4752b2b2dbc0fb04dadc"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.63%" id="mcps1.2.4.1.2"><p id="a602246198adf4a79a13bc4317d4c0d4f"><a name="a602246198adf4a79a13bc4317d4c0d4f"></a><a name="a602246198adf4a79a13bc4317d4c0d4f"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.12%" id="mcps1.2.4.1.3"><p id="a8cbfa8dcb0b943ff8e789755123fec83"><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a><a name="a8cbfa8dcb0b943ff8e789755123fec83"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r43de461181294c56b28da56a1f604b09"><td class="cellrowborder" valign="top" width="24.25%" headers="mcps1.2.4.1.1 "><p id="abc19a41a8f594f1ba6701e10da50a078"><a name="abc19a41a8f594f1ba6701e10da50a078"></a><a name="abc19a41a8f594f1ba6701e10da50a078"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.2 "><p id="a15ae7b8585d24e48abc6b9bf45636fda"><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a><a name="a15ae7b8585d24e48abc6b9bf45636fda"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.12%" headers="mcps1.2.4.1.3 "><p id="p139393206480"><a name="p139393206480"></a><a name="p139393206480"></a>API的url地址。</p>
    </td>
    </tr>
    <tr id="rbd5ec7242fef4c03b21636ac14160d9e"><td class="cellrowborder" valign="top" width="24.25%" headers="mcps1.2.4.1.1 "><p id="a18479f6b70b34f29b2b90d754f59282a"><a name="a18479f6b70b34f29b2b90d754f59282a"></a><a name="a18479f6b70b34f29b2b90d754f59282a"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.2.4.1.2 "><p id="ae1f14fa2e6a54531aeffd26874fea267"><a name="ae1f14fa2e6a54531aeffd26874fea267"></a><a name="ae1f14fa2e6a54531aeffd26874fea267"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.12%" headers="mcps1.2.4.1.3 "><p id="p115877381483"><a name="p115877381483"></a><a name="p115877381483"></a>API的url地址依赖。取值为：</p>
    <a name="ul207311644172510"></a><a name="ul207311644172510"></a><ul id="ul207311644172510"><li>self：包含版本号的资源链接，需要立即跟踪时使用此类链接。</li><li>bookmark：提供了适合长期存储的资源链接。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "versions": [
            {
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
        ]
    }
    ```


## 返回值<a name="section12571834"></a>

正常返回值：

<a name="table753804619176"></a>
<table><thead align="left"><tr id="row10735134615172"><th class="cellrowborder" valign="top" width="42.42%" id="mcps1.1.3.1.1"><p id="p19735204616177"><a name="p19735204616177"></a><a name="p19735204616177"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="57.58%" id="mcps1.1.3.1.2"><p id="p207355465176"><a name="p207355465176"></a><a name="p207355465176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1473514621713"><td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.1.3.1.1 "><p id="p13735144611178"><a name="p13735144611178"></a><a name="p13735144611178"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="57.58%" headers="mcps1.1.3.1.2 "><p id="p207351246161711"><a name="p207351246161711"></a><a name="p207351246161711"></a>服务器已成功处理了请求。</p>
</td>
</tr>
</tbody>
</table>

其他返回值请参考[状态码](状态码.md)。

## 错误码<a name="section12157147171520"></a>

请参考[错误码](错误码.md)。

