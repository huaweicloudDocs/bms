# 查询Job状态<a name="ZH-CN_TOPIC_0118696596"></a>

## 功能介绍<a name="section1145624712615"></a>

查询Job的执行状态。

对于创建裸金属服务器、挂卸卷等异步API，命令下发后，会返回“job\_id”，通过“job\_id”可以查询任务的执行状态。

## URI<a name="section12499172418819"></a>

GET /v1/\{project\_id\}/jobs/\{job\_id\}

参数说明请参见[表1](#table108782505134)。

**表 1**  参数说明

<a name="table108782505134"></a>
<table><thead align="left"><tr id="row087915031315"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p2450228144"><a name="p2450228144"></a><a name="p2450228144"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p164531028144"><a name="p164531028144"></a><a name="p164531028144"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p845682121415"><a name="p845682121415"></a><a name="p845682121415"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row198791550121313"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1646042151413"><a name="p1646042151413"></a><a name="p1646042151413"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6463182161412"><a name="p6463182161412"></a><a name="p6463182161412"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p64651423146"><a name="p64651423146"></a><a name="p64651423146"></a>项目ID。</p>
<p id="p652825144113"><a name="p652825144113"></a><a name="p652825144113"></a>获取方式请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row18879175019131"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p194675214146"><a name="p194675214146"></a><a name="p194675214146"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1747012171413"><a name="p1747012171413"></a><a name="p1747012171413"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p04739215149"><a name="p04739215149"></a><a name="p04739215149"></a>Job ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1707915201018"></a>

-   请求参数

    无

-   请求样例

    ```
    GET https://{BMS Endpoint}/v1/bbf1946d374b44a0a2a95533562ba954/jobs/2c9eb2c5544cbf6101544f0635672b60
    ```


## 响应消息<a name="section32178181210"></a>

-   响应参数

    <a name="table63003337163851"></a>
    <table><thead align="left"><tr id="row65296242163851"><th class="cellrowborder" valign="top" width="22.67%" id="mcps1.1.4.1.1"><p id="p54504213163851"><a name="p54504213163851"></a><a name="p54504213163851"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.59%" id="mcps1.1.4.1.2"><p id="p52765170163851"><a name="p52765170163851"></a><a name="p52765170163851"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.74%" id="mcps1.1.4.1.3"><p id="p46120367163851"><a name="p46120367163851"></a><a name="p46120367163851"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row44762228163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p20905868102821"><a name="p20905868102821"></a><a name="p20905868102821"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p15653760102821"><a name="p15653760102821"></a><a name="p15653760102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p3084195102821"><a name="p3084195102821"></a><a name="p3084195102821"></a>Job的状态。</p>
    <a name="ul27757760102821"></a><a name="ul27757760102821"></a><ul id="ul27757760102821"><li>SUCCESS：成功</li><li>RUNNING：运行中</li><li>FAIL：失败</li><li>INIT：正在初始化</li></ul>
    </td>
    </tr>
    <tr id="row17040455163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p21767581102821"><a name="p21767581102821"></a><a name="p21767581102821"></a>entities</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p18343614102821"><a name="p18343614102821"></a><a name="p18343614102821"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p78921950203711"><a name="p78921950203711"></a><a name="p78921950203711"></a>Job操作的对象。请参见<a href="#table63816992163249">表2</a>。</p>
    <p id="p17831309102821"><a name="p17831309102821"></a><a name="p17831309102821"></a>根据不同Job类型，显示不同的内容。<span id="text1027592519399"><a name="text1027592519399"></a><a name="text1027592519399"></a>裸金属服务器</span><span id="text1968164914717"><a name="text1968164914717"></a><a name="text1968164914717"></a></span>相关操作显示server_id；网卡相关操作显示nic_id；有子Job时为子Job的详情。</p>
    </td>
    </tr>
    <tr id="row51515112163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p47013726102821"><a name="p47013726102821"></a><a name="p47013726102821"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p50015490102821"><a name="p50015490102821"></a><a name="p50015490102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p21179423102821"><a name="p21179423102821"></a><a name="p21179423102821"></a>Job ID。</p>
    </td>
    </tr>
    <tr id="row25971152163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p4761320102821"><a name="p4761320102821"></a><a name="p4761320102821"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p50122638102821"><a name="p50122638102821"></a><a name="p50122638102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p32181178102821"><a name="p32181178102821"></a><a name="p32181178102821"></a>Job的类型，包含以下类型：</p>
    <a name="ul1381913613363"></a><a name="ul1381913613363"></a><ul id="ul1381913613363"><li>baremetalBatchCreate：批量创建<span id="text355864965317"><a name="text355864965317"></a><a name="text355864965317"></a>裸金属服务器</span><span id="text9558114975316"><a name="text9558114975316"></a><a name="text9558114975316"></a></span></li><li>baremetalBatchOperate：批量修改<span id="text1836716524531"><a name="text1836716524531"></a><a name="text1836716524531"></a>裸金属服务器</span><span id="text1836755215534"><a name="text1836755215534"></a><a name="text1836755215534"></a></span>电源状态</li><li>baremetalVolumeBootReinstallOs：重装快速发放裸金属服务器操作系统</li><li>baremetalReinstallOs：重装本地盘裸金属服务器操作系统</li><li>baremetalAttachVolume：挂载单个磁盘</li><li>baremetalDetachVolume：卸载单个磁盘</li></ul>
    </td>
    </tr>
    <tr id="row37164860163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p39085626102821"><a name="p39085626102821"></a><a name="p39085626102821"></a>begin_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p11819105102821"><a name="p11819105102821"></a><a name="p11819105102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p26193501102821"><a name="p26193501102821"></a><a name="p26193501102821"></a>开始时间。</p>
    <p id="p8261133915368"><a name="p8261133915368"></a><a name="p8261133915368"></a>时间戳格式为ISO 8601，例如：2019-04-25T20:04:47.591Z</p>
    </td>
    </tr>
    <tr id="row15772661163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p36144979102821"><a name="p36144979102821"></a><a name="p36144979102821"></a>end_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p42062205102821"><a name="p42062205102821"></a><a name="p42062205102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p61705735102821"><a name="p61705735102821"></a><a name="p61705735102821"></a>结束时间。</p>
    <p id="p4767114253718"><a name="p4767114253718"></a><a name="p4767114253718"></a>时间戳格式为ISO 8601，例如：2019-04-26T20:04:47.591Z</p>
    </td>
    </tr>
    <tr id="row58136329163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p20542517102821"><a name="p20542517102821"></a><a name="p20542517102821"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p53331169102821"><a name="p53331169102821"></a><a name="p53331169102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p22389946102821"><a name="p22389946102821"></a><a name="p22389946102821"></a>Job执行失败时的错误码。</p>
    </td>
    </tr>
    <tr id="row26946447163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p14816990102821"><a name="p14816990102821"></a><a name="p14816990102821"></a>fail_reason</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p59325580102821"><a name="p59325580102821"></a><a name="p59325580102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p30239861102821"><a name="p30239861102821"></a><a name="p30239861102821"></a>Job执行失败时的错误原因。</p>
    </td>
    </tr>
    <tr id="row41958503163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p33151312102821"><a name="p33151312102821"></a><a name="p33151312102821"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p901760102821"><a name="p901760102821"></a><a name="p901760102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p53403447102821"><a name="p53403447102821"></a><a name="p53403447102821"></a>出现错误时，返回的错误消息。</p>
    </td>
    </tr>
    <tr id="row47258102163851"><td class="cellrowborder" valign="top" width="22.67%" headers="mcps1.1.4.1.1 "><p id="p7972234102821"><a name="p7972234102821"></a><a name="p7972234102821"></a>code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.59%" headers="mcps1.1.4.1.2 "><p id="p41771195102821"><a name="p41771195102821"></a><a name="p41771195102821"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.74%" headers="mcps1.1.4.1.3 "><p id="p50886402102821"><a name="p50886402102821"></a><a name="p50886402102821"></a>出现错误时，返回的错误码。</p>
    <p id="p55324436102821"><a name="p55324436102821"></a><a name="p55324436102821"></a>错误码和其对应的含义请参考<a href="状态码.md">状态码</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  entities字段数据结构说明

    <a name="table63816992163249"></a>
    <table><thead align="left"><tr id="row25378569163249"><th class="cellrowborder" valign="top" width="22.752275227522752%" id="mcps1.2.4.1.1"><p id="p38741046114219"><a name="p38741046114219"></a><a name="p38741046114219"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.75207520752075%" id="mcps1.2.4.1.2"><p id="p687612460429"><a name="p687612460429"></a><a name="p687612460429"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.495649564956494%" id="mcps1.2.4.1.3"><p id="p20879104611427"><a name="p20879104611427"></a><a name="p20879104611427"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row21068325163249"><td class="cellrowborder" valign="top" width="22.752275227522752%" headers="mcps1.2.4.1.1 "><p id="p1987866102840"><a name="p1987866102840"></a><a name="p1987866102840"></a>sub_jobs_total</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.75207520752075%" headers="mcps1.2.4.1.2 "><p id="p26799477102840"><a name="p26799477102840"></a><a name="p26799477102840"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.495649564956494%" headers="mcps1.2.4.1.3 "><p id="p23274041102840"><a name="p23274041102840"></a><a name="p23274041102840"></a>子任务数量。没有子任务时为0。</p>
    </td>
    </tr>
    <tr id="row1957164017643"><td class="cellrowborder" valign="top" width="22.752275227522752%" headers="mcps1.2.4.1.1 "><p id="p55342196102840"><a name="p55342196102840"></a><a name="p55342196102840"></a>sub_jobs</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.75207520752075%" headers="mcps1.2.4.1.2 "><p id="p53532900102840"><a name="p53532900102840"></a><a name="p53532900102840"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.495649564956494%" headers="mcps1.2.4.1.3 "><p id="p35234299102840"><a name="p35234299102840"></a><a name="p35234299102840"></a>每个子任务的执行信息。没有子任务时为空列表。请参见<a href="#table1500801817135">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  sub\_jobs字段数据结构说明

    <a name="table1500801817135"></a>
    <table><thead align="left"><tr id="row5502467917135"><th class="cellrowborder" valign="top" width="22.78%" id="mcps1.2.4.1.1"><p id="p14352122417435"><a name="p14352122417435"></a><a name="p14352122417435"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.7%" id="mcps1.2.4.1.2"><p id="p153558241436"><a name="p153558241436"></a><a name="p153558241436"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.52%" id="mcps1.2.4.1.3"><p id="p8357122474310"><a name="p8357122474310"></a><a name="p8357122474310"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row3836327417140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p5596555610290"><a name="p5596555610290"></a><a name="p5596555610290"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p3691618110290"><a name="p3691618110290"></a><a name="p3691618110290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p124153110290"><a name="p124153110290"></a><a name="p124153110290"></a>Job的状态。</p>
    <a name="ul1117378710290"></a><a name="ul1117378710290"></a><ul id="ul1117378710290"><li>SUCCESS：成功</li><li>RUNNING：运行中</li><li>FAIL：失败</li><li>INIT：正在初始化</li></ul>
    </td>
    </tr>
    <tr id="row1171912617140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p5946004210290"><a name="p5946004210290"></a><a name="p5946004210290"></a>entities</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p5153410710290"><a name="p5153410710290"></a><a name="p5153410710290"></a>Array of objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p5450940410290"><a name="p5450940410290"></a><a name="p5450940410290"></a>Job操作的对象。根据不同Job类型，显示不同的内容。<span id="text17249209105512"><a name="text17249209105512"></a><a name="text17249209105512"></a>裸金属服务器</span><span id="text142491299553"><a name="text142491299553"></a><a name="text142491299553"></a></span>相关操作显示server_id；网卡相关操作显示nic_id。</p>
    <p id="p1645004534016"><a name="p1645004534016"></a><a name="p1645004534016"></a>请参见<a href="#table2577901102930">表4</a>。</p>
    </td>
    </tr>
    <tr id="row875866517140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p890825710290"><a name="p890825710290"></a><a name="p890825710290"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p5048019610290"><a name="p5048019610290"></a><a name="p5048019610290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p2440551510290"><a name="p2440551510290"></a><a name="p2440551510290"></a>Job ID。</p>
    </td>
    </tr>
    <tr id="row3079934617140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p777215910290"><a name="p777215910290"></a><a name="p777215910290"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p2556517210290"><a name="p2556517210290"></a><a name="p2556517210290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p4785561910290"><a name="p4785561910290"></a><a name="p4785561910290"></a>Job的类型，包含以下类型：</p>
    <a name="ul767111320272"></a><a name="ul767111320272"></a><ul id="ul767111320272"><li>baremetalSingleCreate：创建单个<span id="text1825012125551"><a name="text1825012125551"></a><a name="text1825012125551"></a>裸金属服务器</span><span id="text8250131217551"><a name="text8250131217551"></a><a name="text8250131217551"></a></span></li><li>baremetalSingleOperate：修改单个<span id="text14253141475512"><a name="text14253141475512"></a><a name="text14253141475512"></a>裸金属服务器</span><span id="text182531614125517"><a name="text182531614125517"></a><a name="text182531614125517"></a></span>电源状态</li></ul>
    </td>
    </tr>
    <tr id="row6307447317140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p5724624610290"><a name="p5724624610290"></a><a name="p5724624610290"></a>begin_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p643434910290"><a name="p643434910290"></a><a name="p643434910290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p6012909110290"><a name="p6012909110290"></a><a name="p6012909110290"></a>开始时间。</p>
    <p id="p196331548193717"><a name="p196331548193717"></a><a name="p196331548193717"></a>时间戳格式为ISO 8601，例如：2019-04-25T20:04:47.591Z</p>
    </td>
    </tr>
    <tr id="row2192135517140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p1201928510290"><a name="p1201928510290"></a><a name="p1201928510290"></a>end_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p3403799810290"><a name="p3403799810290"></a><a name="p3403799810290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p5052973810290"><a name="p5052973810290"></a><a name="p5052973810290"></a>结束时间。</p>
    <p id="p970018924217"><a name="p970018924217"></a><a name="p970018924217"></a>时间戳格式为ISO 8601，例如：2019-04-26T20:04:47.591Z</p>
    </td>
    </tr>
    <tr id="row5463148917140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p6052212310290"><a name="p6052212310290"></a><a name="p6052212310290"></a>error_code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p334495010290"><a name="p334495010290"></a><a name="p334495010290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p2254991410290"><a name="p2254991410290"></a><a name="p2254991410290"></a>Job执行失败时的错误码。</p>
    </td>
    </tr>
    <tr id="row6572248917140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p6432481010290"><a name="p6432481010290"></a><a name="p6432481010290"></a>fail_reason</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p4292711110290"><a name="p4292711110290"></a><a name="p4292711110290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p2113349010290"><a name="p2113349010290"></a><a name="p2113349010290"></a>Job执行失败时的错误原因。</p>
    </td>
    </tr>
    <tr id="row5949828117140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p3838440010290"><a name="p3838440010290"></a><a name="p3838440010290"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p2212873510290"><a name="p2212873510290"></a><a name="p2212873510290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p2572110510290"><a name="p2572110510290"></a><a name="p2572110510290"></a>出现错误时，返回的错误消息。</p>
    </td>
    </tr>
    <tr id="row5135016217140"><td class="cellrowborder" valign="top" width="22.78%" headers="mcps1.2.4.1.1 "><p id="p2731299110290"><a name="p2731299110290"></a><a name="p2731299110290"></a>code</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.4.1.2 "><p id="p6486867210290"><a name="p6486867210290"></a><a name="p6486867210290"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.52%" headers="mcps1.2.4.1.3 "><p id="p4462200910290"><a name="p4462200910290"></a><a name="p4462200910290"></a>出现错误时，返回的错误码。</p>
    <p id="p6605376310290"><a name="p6605376310290"></a><a name="p6605376310290"></a>错误码和其对应的含义请参考<a href="状态码.md">状态码</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  entities字段数据结构说明

    <a name="table2577901102930"></a>
    <table><thead align="left"><tr id="row41961594102930"><th class="cellrowborder" valign="top" width="24.82%" id="mcps1.2.4.1.1"><p id="p14673171924310"><a name="p14673171924310"></a><a name="p14673171924310"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.6%" id="mcps1.2.4.1.2"><p id="p1767515196438"><a name="p1767515196438"></a><a name="p1767515196438"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.58%" id="mcps1.2.4.1.3"><p id="p1967812199432"><a name="p1967812199432"></a><a name="p1967812199432"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row12623506102930"><td class="cellrowborder" valign="top" width="24.82%" headers="mcps1.2.4.1.1 "><p id="p15871098102930"><a name="p15871098102930"></a><a name="p15871098102930"></a>server_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.6%" headers="mcps1.2.4.1.2 "><p id="p10490546102930"><a name="p10490546102930"></a><a name="p10490546102930"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.58%" headers="mcps1.2.4.1.3 "><p id="p64306551102930"><a name="p64306551102930"></a><a name="p64306551102930"></a><span id="text4200019145516"><a name="text4200019145516"></a><a name="text4200019145516"></a>裸金属服务器</span><span id="text0200141925511"><a name="text0200141925511"></a><a name="text0200141925511"></a></span>相关操作显示server_id。</p>
    </td>
    </tr>
    <tr id="row41888051102930"><td class="cellrowborder" valign="top" width="24.82%" headers="mcps1.2.4.1.1 "><p id="p37488972102930"><a name="p37488972102930"></a><a name="p37488972102930"></a>nic_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.6%" headers="mcps1.2.4.1.2 "><p id="p16707926102930"><a name="p16707926102930"></a><a name="p16707926102930"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.58%" headers="mcps1.2.4.1.3 "><p id="p33374275102930"><a name="p33374275102930"></a><a name="p33374275102930"></a>网卡相关操作显示nic_id。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "status": "SUCCESS",
        "entities": {
            "sub_jobs_total": 1,
            "sub_jobs": [
                {
                    "status": "SUCCESS",
                    "entities": {
                        "server_id": "bae51750-0089-41a1-9b18-5c777978ff6d"
                    },
                    "job_id": "2c9eb2c5544cbf6101544f0635672b60",
                    "job_type": "baremetalSingleCreate",
                    "begin_time": "2019-04-25T20:04:47.591Z",
                    "end_time": "2019-04-25T20:08:21.328Z",
                    "error_code": null,
                    "fail_reason": null
                }
            ]
        },
        "job_id": "2c9eb2c5544cbf6101544f0602af2b4f",
        "job_type": "baremetalBatchCreate",
        "begin_time": "2019-04-25T20:04:34.604Z",
        "end_time": "2019-04-25T20:08:41.593Z",
        "error_code": null,
        "fail_reason": null
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

