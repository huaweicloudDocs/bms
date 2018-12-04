# 创建和导入SSH密钥（OpenStack原生）<a name="ZH-CN_TOPIC_0060384660"></a>

## 功能介绍<a name="section46928615105534"></a>

创建SSH密钥，或把公钥导入系统，生成密钥对。

创建SSH密钥成功后，请把响应数据中的私钥内容保存到本地文件，用户使用该私钥登录裸金属服务器。为保证裸金属服务器安全，私钥数据只能读取一次，请妥善保管。

## URI<a name="section3181044105534"></a>

POST /v2.1/\{project\_id\}/os-keypairs

参数说明请参见[表1](#table137043339568)。

**表 1**  参数说明

<a name="table137043339568"></a>
<table><thead align="left"><tr id="row6707133385614"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p16860355105534"><a name="p16860355105534"></a><a name="p16860355105534"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p23511481105534"><a name="p23511481105534"></a><a name="p23511481105534"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p25381808105534"><a name="p25381808105534"></a><a name="p25381808105534"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1170718332563"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p32953279105534"><a name="p32953279105534"></a><a name="p32953279105534"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p51969960105534"><a name="p51969960105534"></a><a name="p51969960105534"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p48817201105534"><a name="p48817201105534"></a><a name="p48817201105534"></a>项目ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section61879170105534"></a>

-   请求参数

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >创建SSH密钥时，只需要提交SSH密钥的name属性。导入SSH密钥时，才需要提交public\_key属性。  

    <a name="table40018745105534"></a>
    <table><thead align="left"><tr id="row48164488105534"><th class="cellrowborder" valign="top" width="16.831683168316832%" id="mcps1.1.5.1.1"><p id="p19987085"><a name="p19987085"></a><a name="p19987085"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.1.5.1.2"><p id="p4546697"><a name="p4546697"></a><a name="p4546697"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.1.5.1.3"><p id="p23972980183956"><a name="p23972980183956"></a><a name="p23972980183956"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.59405940594059%" id="mcps1.1.5.1.4"><p id="p32738149"><a name="p32738149"></a><a name="p32738149"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6972410105534"><td class="cellrowborder" valign="top" width="16.831683168316832%" headers="mcps1.1.5.1.1 "><p id="p27894300105534"><a name="p27894300105534"></a><a name="p27894300105534"></a>keypair</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.1.5.1.2 "><p id="p8634695105534"><a name="p8634695105534"></a><a name="p8634695105534"></a>字典数据结构，参见“[1] keypair字段数据结构说明”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.3 "><p id="p64946643185338"><a name="p64946643185338"></a><a name="p64946643185338"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.59405940594059%" headers="mcps1.1.5.1.4 "><p id="p28321695105534"><a name="p28321695105534"></a><a name="p28321695105534"></a>创建或导入的SSH密钥信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] keypair字段数据结构说明

    <a name="table44094886105534"></a>
    <table><thead align="left"><tr id="row40587827105534"><th class="cellrowborder" valign="top" width="17%" id="mcps1.1.5.1.1"><p id="p16104135417242"><a name="p16104135417242"></a><a name="p16104135417242"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23%" id="mcps1.1.5.1.2"><p id="p1110685412246"><a name="p1110685412246"></a><a name="p1110685412246"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.3"><p id="p410875402410"><a name="p410875402410"></a><a name="p410875402410"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="41%" id="mcps1.1.5.1.4"><p id="p41093543243"><a name="p41093543243"></a><a name="p41093543243"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49263560105534"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.1 "><p id="p30925442105534"><a name="p30925442105534"></a><a name="p30925442105534"></a>public_key</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p31731563105534"><a name="p31731563105534"></a><a name="p31731563105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><p id="p33313320185412"><a name="p33313320185412"></a><a name="p33313320185412"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.5.1.4 "><p id="p20119786105534"><a name="p20119786105534"></a><a name="p20119786105534"></a>导入的公钥信息。导入公钥最大长度为1024字节。</p>
    <p id="p46860349105534"><a name="p46860349105534"></a><a name="p46860349105534"></a>注：长度超过1024字节会导致裸金属服务器注入该密钥失败。</p>
    </td>
    </tr>
    <tr id="row19089958105534"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.1 "><p id="p2782726105534"><a name="p2782726105534"></a><a name="p2782726105534"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p3855315105534"><a name="p3855315105534"></a><a name="p3855315105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><p id="p59110514185412"><a name="p59110514185412"></a><a name="p59110514185412"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="41%" headers="mcps1.1.5.1.4 "><p id="p43845137105534"><a name="p43845137105534"></a><a name="p43845137105534"></a>密钥名称。</p>
    <p id="p59061918105534"><a name="p59061918105534"></a><a name="p59061918105534"></a>新创建的密钥名称不能和已有密钥名称相同。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    {
        "keypair": {
            "name": "keypair-7d7c3650-dabe-4eb0-b904-5c464453c043",
            "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC9mC3WZN9UGLxgPBpP7H5jZMc6pKwOoSgre8yun6REFktn/Kz7DUt9jaR1UJyRzHxITfCfAIgSxPdGqB/oF1suMyWgu5i0625vavLB5z5kC8Hq3qZJ9zJO1poE1kyD+htiTtPWJ88e12xuH2XB/CZN9OpEiF98hAagiOE0EnOS5Q== Generated by Nova\n"
        }
    }
    ```


## 响应消息<a name="section33789573105534"></a>

-   响应参数

    <a name="table32814569105534"></a>
    <table><thead align="left"><tr id="row31072960105534"><th class="cellrowborder" valign="top" width="24.39%" id="mcps1.1.4.1.1"><p id="p104001675252"><a name="p104001675252"></a><a name="p104001675252"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.270000000000003%" id="mcps1.1.4.1.2"><p id="p840215762519"><a name="p840215762519"></a><a name="p840215762519"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.339999999999996%" id="mcps1.1.4.1.3"><p id="p1040516718253"><a name="p1040516718253"></a><a name="p1040516718253"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row30545796105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p58290412105534"><a name="p58290412105534"></a><a name="p58290412105534"></a>keypair</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p23902945105534"><a name="p23902945105534"></a><a name="p23902945105534"></a>字典数据结构[1]</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p57090378105534"><a name="p57090378105534"></a><a name="p57090378105534"></a>SSH密钥信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    \[1\] keypair字段数据结构说明

    <a name="table11390225105534"></a>
    <table><thead align="left"><tr id="row13107196105534"><th class="cellrowborder" valign="top" width="24.39%" id="mcps1.1.4.1.1"><p id="p4172201014255"><a name="p4172201014255"></a><a name="p4172201014255"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.270000000000003%" id="mcps1.1.4.1.2"><p id="p10173141011254"><a name="p10173141011254"></a><a name="p10173141011254"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.339999999999996%" id="mcps1.1.4.1.3"><p id="p817617100257"><a name="p817617100257"></a><a name="p817617100257"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row45769827105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p16368506105534"><a name="p16368506105534"></a><a name="p16368506105534"></a>fingerprint</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p50780601105534"><a name="p50780601105534"></a><a name="p50780601105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p19588041105534"><a name="p19588041105534"></a><a name="p19588041105534"></a>密钥对应指纹信息。</p>
    </td>
    </tr>
    <tr id="row42074647105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p52603235105534"><a name="p52603235105534"></a><a name="p52603235105534"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p33003603105534"><a name="p33003603105534"></a><a name="p33003603105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p56046159105534"><a name="p56046159105534"></a><a name="p56046159105534"></a>密钥名称。</p>
    </td>
    </tr>
    <tr id="row34653390105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p55461192105534"><a name="p55461192105534"></a><a name="p55461192105534"></a>public_key</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p63171587105534"><a name="p63171587105534"></a><a name="p63171587105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p16624935105534"><a name="p16624935105534"></a><a name="p16624935105534"></a>密钥对应publicKey信息。</p>
    </td>
    </tr>
    <tr id="row15406687105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p39982130105534"><a name="p39982130105534"></a><a name="p39982130105534"></a>private_key</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p17327106105534"><a name="p17327106105534"></a><a name="p17327106105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p61318326105534"><a name="p61318326105534"></a><a name="p61318326105534"></a>密钥对应privateKey信息。</p>
    </td>
    </tr>
    <tr id="row14994025105534"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.1.4.1.1 "><p id="p6556527105534"><a name="p6556527105534"></a><a name="p6556527105534"></a>user_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.270000000000003%" headers="mcps1.1.4.1.2 "><p id="p61316685105534"><a name="p61316685105534"></a><a name="p61316685105534"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.339999999999996%" headers="mcps1.1.4.1.3 "><p id="p595628105534"><a name="p595628105534"></a><a name="p595628105534"></a>密钥所属用户ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "keypair": {
            "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC9mC3WZN9UGLxgPBpP7H5jZMc6pKwOoSgre8yun6REFktn/Kz7DUt9jaR1UJyRzHxITfCfAIgSxPdGqB/oF1suMyWgu5i0625vavLB5z5kC8Hq3qZJ9zJO1poE1kyD+htiTtPWJ88e12xuH2XB/CZN9OpEiF98hAagiOE0EnOS5Q== Generated by Nova\n",
            "user_id": "f882feb345064e7d9392440a0f397c25",
            "name": "keypair-7d7c3650-dabe-4eb0-b904-5c464453c043",
            "fingerprint": "35:9d:d0:c3:4a:80:d3:d8:86:f1:ca:f7:df:c4:f9:d8"
        }
    }
    ```


## 返回值<a name="section6245741105534"></a>

请参考[通用返回值](通用返回值.md)。

