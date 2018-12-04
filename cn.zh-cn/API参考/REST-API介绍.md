# REST API介绍<a name="ZH-CN_TOPIC_0113746487"></a>

公有云API符合RESTful API的设计理论。

REST从资源的角度来观察整个网络，提供创建、查询、更新、删除等方法访问服务的资源。

REST API请求/响应可以分为五个部分：

-   请求URI
-   请求消息头
-   请求消息体
-   响应消息头
-   响应消息体

## 请求URI<a name="section697653216219"></a>

请求URI由如下部分组成：

**\{URI-scheme\}://\{Endpoint\}/\{resource-path\}?\{query-string\}**

尽管请求URI包含在请求消息头中，但大多数语言或框架都要求您从请求消息中单独传递它，所有我们在此单独拿出来强调。

**表 1**  URI中的参数说明

<a name="table4443194632512"></a>
<table><thead align="left"><tr id="row1944414616258"><th class="cellrowborder" valign="top" width="26%" id="mcps1.2.3.1.1"><p id="p1644484692510"><a name="p1644484692510"></a><a name="p1644484692510"></a><strong id="b2015193132620"><a name="b2015193132620"></a><a name="b2015193132620"></a>参数</strong></p>
</th>
<th class="cellrowborder" valign="top" width="74%" id="mcps1.2.3.1.2"><p id="p174441146142511"><a name="p174441146142511"></a><a name="p174441146142511"></a><strong id="b131565362615"><a name="b131565362615"></a><a name="b131565362615"></a>描述</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row10444144620259"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p154446465251"><a name="p154446465251"></a><a name="p154446465251"></a>URI-scheme</p>
</td>
<td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p8444144692517"><a name="p8444144692517"></a><a name="p8444144692517"></a>表示用于传输请求的协议。</p>
</td>
</tr>
<tr id="row444414692513"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p7444194610257"><a name="p7444194610257"></a><a name="p7444194610257"></a>Endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p244474613259"><a name="p244474613259"></a><a name="p244474613259"></a>指定承载REST服务端点的服务器域名或IP，从<a href="http://developer.huaweicloud.com/dev/endpoint" target="_blank" rel="noopener noreferrer">地区和终端节点</a>中获取。</p>
</td>
</tr>
<tr id="row1744454612520"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p14442468257"><a name="p14442468257"></a><a name="p14442468257"></a>resource-path</p>
</td>
<td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p1844412467258"><a name="p1844412467258"></a><a name="p1844412467258"></a>资源路径，也即API访问路径。从具体接口的URI模块获取，例如“v3/auth/tokens”。</p>
</td>
</tr>
<tr id="row184441346152515"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p4444154692516"><a name="p4444154692516"></a><a name="p4444154692516"></a>query-string</p>
</td>
<td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p1444414622514"><a name="p1444414622514"></a><a name="p1444414622514"></a>可选参数，例如API版本或资源选择标准。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息头<a name="section5296154118345"></a>

请求消息头包含如下两部分：

-   HTTP方法（也称为操作或动词），它告诉服务你正在请求什么类型的操作。

    **表 2**  HTTP方法

    <a name="table1961229113819"></a>
    <table><thead align="left"><tr id="row86141913816"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p186147910387"><a name="p186147910387"></a><a name="p186147910387"></a><strong id="b1093312238395"><a name="b1093312238395"></a><a name="b1093312238395"></a>方法</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p166141293387"><a name="p166141293387"></a><a name="p166141293387"></a><strong id="b169341023133919"><a name="b169341023133919"></a><a name="b169341023133919"></a>说明</strong></p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row146141194381"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p12831539123914"><a name="p12831539123914"></a><a name="p12831539123914"></a>GET</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p2831123916397"><a name="p2831123916397"></a><a name="p2831123916397"></a>请求服务器返回指定资源。</p>
    </td>
    </tr>
    <tr id="row161429103817"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p3831239183912"><a name="p3831239183912"></a><a name="p3831239183912"></a>PUT</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p178311939193911"><a name="p178311939193911"></a><a name="p178311939193911"></a>请求服务器更新指定资源。</p>
    </td>
    </tr>
    <tr id="row56141190384"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p68311239113912"><a name="p68311239113912"></a><a name="p68311239113912"></a>POST</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p1583133918391"><a name="p1583133918391"></a><a name="p1583133918391"></a>请求服务器新增资源或执行特殊操作。</p>
    </td>
    </tr>
    <tr id="row861411903812"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p1183153943916"><a name="p1183153943916"></a><a name="p1183153943916"></a>DELETE</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p6831163914392"><a name="p6831163914392"></a><a name="p6831163914392"></a>请求服务器删除指定资源，如删除对象等。</p>
    </td>
    </tr>
    <tr id="row5614119183810"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p78314395393"><a name="p78314395393"></a><a name="p78314395393"></a>HEAD</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p38311239153920"><a name="p38311239153920"></a><a name="p38311239153920"></a>请求服务器资源头部。</p>
    </td>
    </tr>
    <tr id="row2614199163812"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p1483143915390"><a name="p1483143915390"></a><a name="p1483143915390"></a>PATCH</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p17831173918394"><a name="p17831173918394"></a><a name="p17831173918394"></a>请求服务器更新资源的部分内容。</p>
    <p id="p9831123911390"><a name="p9831123911390"></a><a name="p9831123911390"></a>当资源不存在的时候，PATCH可能会去创建一个新的资源。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   可选的附加请求头字段，如指定的URI和HTTP方法所要求的字段。详细的公共请求消息头字段请参见[表3](#zh-cn_topic_0020536996_table2598811411913)。

    **表 3**  公共请求消息头

    <a name="zh-cn_topic_0020536996_table2598811411913"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0020536996_row3248625511913"><th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0020536996_p6015991611913"><a name="zh-cn_topic_0020536996_p6015991611913"></a><a name="zh-cn_topic_0020536996_p6015991611913"></a><strong id="b16125122010516"><a name="b16125122010516"></a><a name="b16125122010516"></a>名称</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="26.490000000000002%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0020536996_p4111502811913"><a name="zh-cn_topic_0020536996_p4111502811913"></a><a name="zh-cn_topic_0020536996_p4111502811913"></a><strong id="b612662015512"><a name="b612662015512"></a><a name="b612662015512"></a>描述</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="20.119999999999997%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0020536996_p4198298511913"><a name="zh-cn_topic_0020536996_p4198298511913"></a><a name="zh-cn_topic_0020536996_p4198298511913"></a><strong id="b812872012519"><a name="b812872012519"></a><a name="b812872012519"></a>是否必选</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="33.650000000000006%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0020536996_p4517861011913"><a name="zh-cn_topic_0020536996_p4517861011913"></a><a name="zh-cn_topic_0020536996_p4517861011913"></a><strong id="b812932085119"><a name="b812932085119"></a><a name="b812932085119"></a>示例</strong></p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0020536996_row395431011913"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p5186367311913"><a name="zh-cn_topic_0020536996_p5186367311913"></a><a name="zh-cn_topic_0020536996_p5186367311913"></a>X-Sdk-Date</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p4020795611913"><a name="zh-cn_topic_0020536996_p4020795611913"></a><a name="zh-cn_topic_0020536996_p4020795611913"></a>请求的发生时间，格式为YYYYMMDD'T'HHMMSS'Z'。</p>
    <p id="zh-cn_topic_0020536996_p54353155164637"><a name="zh-cn_topic_0020536996_p54353155164637"></a><a name="zh-cn_topic_0020536996_p54353155164637"></a>取值为当前系统的GMT时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p13173142111121"><a name="zh-cn_topic_0020536996_p13173142111121"></a><a name="zh-cn_topic_0020536996_p13173142111121"></a>否</p>
    <p id="zh-cn_topic_0020536996_p4951939165616"><a name="zh-cn_topic_0020536996_p4951939165616"></a><a name="zh-cn_topic_0020536996_p4951939165616"></a>使用AK/SK认证时该字段必选。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p13243898111235"><a name="zh-cn_topic_0020536996_p13243898111235"></a><a name="zh-cn_topic_0020536996_p13243898111235"></a>20150907T101459Z</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row6223565911913"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p792363911913"><a name="zh-cn_topic_0020536996_p792363911913"></a><a name="zh-cn_topic_0020536996_p792363911913"></a>Authorization</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p3783505611913"><a name="zh-cn_topic_0020536996_p3783505611913"></a><a name="zh-cn_topic_0020536996_p3783505611913"></a>签名认证信息。</p>
    <p id="zh-cn_topic_0020536996_p32120799165456"><a name="zh-cn_topic_0020536996_p32120799165456"></a><a name="zh-cn_topic_0020536996_p32120799165456"></a>该值来源于请求签名结果。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p6395216415245"><a name="zh-cn_topic_0020536996_p6395216415245"></a><a name="zh-cn_topic_0020536996_p6395216415245"></a>否</p>
    <p id="zh-cn_topic_0020536996_p27320033165638"><a name="zh-cn_topic_0020536996_p27320033165638"></a><a name="zh-cn_topic_0020536996_p27320033165638"></a>使用AK/SK认证时该字段必选。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p18982550111240"><a name="zh-cn_topic_0020536996_p18982550111240"></a><a name="zh-cn_topic_0020536996_p18982550111240"></a>SDK-HMAC-SHA256 Credential=ZIRRKMTWPTQFQI1WKNKB/20150907//ec2/sdk_request, SignedHeaders=content-type;host;x-sdk-date, Signature=55741b610f3c9fa3ae40b5a8021ebf7ebc2a28a603fc62d25cb3bfe6608e1994</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row106365011913"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p1904681711913"><a name="zh-cn_topic_0020536996_p1904681711913"></a><a name="zh-cn_topic_0020536996_p1904681711913"></a>Host</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p8809216111110"><a name="zh-cn_topic_0020536996_p8809216111110"></a><a name="zh-cn_topic_0020536996_p8809216111110"></a>请求的服务器信息，从服务API的URL中获取。值为hostname[:port]。端口缺省时使用默认的端口，https的默认端口为443。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p2507173515247"><a name="zh-cn_topic_0020536996_p2507173515247"></a><a name="zh-cn_topic_0020536996_p2507173515247"></a>否</p>
    <p id="zh-cn_topic_0020536996_p38175022165640"><a name="zh-cn_topic_0020536996_p38175022165640"></a><a name="zh-cn_topic_0020536996_p38175022165640"></a>使用AK/SK认证时该字段必选。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p14146116111246"><a name="zh-cn_topic_0020536996_p14146116111246"></a><a name="zh-cn_topic_0020536996_p14146116111246"></a>code.test.com</p>
    <p id="zh-cn_topic_0020536996_p2493641117013"><a name="zh-cn_topic_0020536996_p2493641117013"></a><a name="zh-cn_topic_0020536996_p2493641117013"></a>or</p>
    <p id="zh-cn_topic_0020536996_p36288498165821"><a name="zh-cn_topic_0020536996_p36288498165821"></a><a name="zh-cn_topic_0020536996_p36288498165821"></a>code.test.com:443</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row54513894165638"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p53549319165638"><a name="zh-cn_topic_0020536996_p53549319165638"></a><a name="zh-cn_topic_0020536996_p53549319165638"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p42527621165638"><a name="zh-cn_topic_0020536996_p42527621165638"></a><a name="zh-cn_topic_0020536996_p42527621165638"></a>发送的实体的MIME类型。推荐用户默认使用application/json，如果API是对象、镜像上传等接口，媒体类型可按照流类型的不同进行确定。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p22185287165638"><a name="zh-cn_topic_0020536996_p22185287165638"></a><a name="zh-cn_topic_0020536996_p22185287165638"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p52177846165638"><a name="zh-cn_topic_0020536996_p52177846165638"></a><a name="zh-cn_topic_0020536996_p52177846165638"></a>application/json</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row5620044311913"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p5594200711913"><a name="zh-cn_topic_0020536996_p5594200711913"></a><a name="zh-cn_topic_0020536996_p5594200711913"></a>Content-Length</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p3500874411913"><a name="zh-cn_topic_0020536996_p3500874411913"></a><a name="zh-cn_topic_0020536996_p3500874411913"></a>请求body长度，单位为Byte。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p4828723111129"><a name="zh-cn_topic_0020536996_p4828723111129"></a><a name="zh-cn_topic_0020536996_p4828723111129"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p4584314411913"><a name="zh-cn_topic_0020536996_p4584314411913"></a><a name="zh-cn_topic_0020536996_p4584314411913"></a>3495</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row5934929120145"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p4256329220145"><a name="zh-cn_topic_0020536996_p4256329220145"></a><a name="zh-cn_topic_0020536996_p4256329220145"></a>X-Project-Id</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p18851584144919"><a name="zh-cn_topic_0020536996_p18851584144919"></a><a name="zh-cn_topic_0020536996_p18851584144919"></a>project id，项目编号。请参考<a href="获取项目ID.md">获取项目ID</a>章节获取项目编号。</p>
    <p id="zh-cn_topic_0020536996_p2507466620145"><a name="zh-cn_topic_0020536996_p2507466620145"></a><a name="zh-cn_topic_0020536996_p2507466620145"></a>如果是DeC的请求或者多project的请求则必须传入project id。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p1778207620145"><a name="zh-cn_topic_0020536996_p1778207620145"></a><a name="zh-cn_topic_0020536996_p1778207620145"></a>否</p>
    <p id="zh-cn_topic_0020536996_p55232980103957"><a name="zh-cn_topic_0020536996_p55232980103957"></a><a name="zh-cn_topic_0020536996_p55232980103957"></a>如果是专属云场景采用AK/SK 认证方式的接口请求或者多project场景采用AK/SK认证的接口请求则该字段必选。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p3106207520145"><a name="zh-cn_topic_0020536996_p3106207520145"></a><a name="zh-cn_topic_0020536996_p3106207520145"></a>e9993fc787d94b6c886cbaa340f9c0f4</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536996_row60029080165425"><td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0020536996_p30517305165425"><a name="zh-cn_topic_0020536996_p30517305165425"></a><a name="zh-cn_topic_0020536996_p30517305165425"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.490000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020536996_p55982606165425"><a name="zh-cn_topic_0020536996_p55982606165425"></a><a name="zh-cn_topic_0020536996_p55982606165425"></a>用户Token。</p>
    <p id="zh-cn_topic_0020536996_p23288801103741"><a name="zh-cn_topic_0020536996_p23288801103741"></a><a name="zh-cn_topic_0020536996_p23288801103741"></a>获取Token，请参考《统一身份认证服务API参考》的“获取用户Token”章节。请求响应成功后在响应消息头中包含的“X-Subject-Token”的值即为Token值。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020536996_p38297215165425"><a name="zh-cn_topic_0020536996_p38297215165425"></a><a name="zh-cn_topic_0020536996_p38297215165425"></a>否</p>
    <p id="zh-cn_topic_0020536996_p2488420216568"><a name="zh-cn_topic_0020536996_p2488420216568"></a><a name="zh-cn_topic_0020536996_p2488420216568"></a>使用Token认证时该字段必选。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020536996_p3766765110398"><a name="zh-cn_topic_0020536996_p3766765110398"></a><a name="zh-cn_topic_0020536996_p3766765110398"></a>注：以下仅为Token示例片段MIIPAgYJKoZIhvcNAQcCoIIO8zCCDu8CAQExDTALBglghkgBZQMEAgEwgg1QBgkqhkiG9w0BBwGggg1BBIINPXsidG9rZ</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息体<a name="section1437471411"></a>

该部分可选。请求消息体通常以结构化格式（如JSON或XML）发出，与请求消息头中Content-Type对应，传递除请求消息头之外的内容。

若请求消息体中的参数支持中文，则中文字符必须为UTF-8编码。

## 响应消息头<a name="section61333484715"></a>

响应消息头包含如下两部分：

-   一个HTTP状态代码，从2xx成功代码到4xx或5xx错误代码，或者可以返回服务定义的状态码。
-   附加响应头字段，如Content-Type响应消息头。详细的公共响应消息头字段请参考[表4](#zh-cn_topic_0020536997_table3877208613139)。

    **表 4**  公共响应消息头

    <a name="zh-cn_topic_0020536997_table3877208613139"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0020536997_row3771309013139"><th class="cellrowborder" valign="top" width="19.15%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0020536997_p4531764513139"><a name="zh-cn_topic_0020536997_p4531764513139"></a><a name="zh-cn_topic_0020536997_p4531764513139"></a><strong id="b1355613001117"><a name="b1355613001117"></a><a name="b1355613001117"></a>名称</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="49.830000000000005%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0020536997_p4685062813139"><a name="zh-cn_topic_0020536997_p4685062813139"></a><a name="zh-cn_topic_0020536997_p4685062813139"></a><strong id="b555911300112"><a name="b555911300112"></a><a name="b555911300112"></a>描述</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="31.019999999999996%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0020536997_p5162099210429"><a name="zh-cn_topic_0020536997_p5162099210429"></a><a name="zh-cn_topic_0020536997_p5162099210429"></a><strong id="b55591930171112"><a name="b55591930171112"></a><a name="b55591930171112"></a>示例</strong></p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0020536997_row1900247113139"><td class="cellrowborder" valign="top" width="19.15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0020536997_p6280518613139"><a name="zh-cn_topic_0020536997_p6280518613139"></a><a name="zh-cn_topic_0020536997_p6280518613139"></a>Content-Length</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.830000000000005%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0020536997_p4985309313517"><a name="zh-cn_topic_0020536997_p4985309313517"></a><a name="zh-cn_topic_0020536997_p4985309313517"></a>响应消息体的字节长度，单位为Byte。</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.019999999999996%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0020536997_p2055083910429"><a name="zh-cn_topic_0020536997_p2055083910429"></a><a name="zh-cn_topic_0020536997_p2055083910429"></a>--</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536997_row1673548413139"><td class="cellrowborder" valign="top" width="19.15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0020536997_p1339693313139"><a name="zh-cn_topic_0020536997_p1339693313139"></a><a name="zh-cn_topic_0020536997_p1339693313139"></a>Date</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.830000000000005%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0020536997_p1140975013139"><a name="zh-cn_topic_0020536997_p1140975013139"></a><a name="zh-cn_topic_0020536997_p1140975013139"></a>系统响应的GMT时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.019999999999996%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0020536997_p59381193104213"><a name="zh-cn_topic_0020536997_p59381193104213"></a><a name="zh-cn_topic_0020536997_p59381193104213"></a>Wed, 27 Dec 2016 06:49:46 GMT</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0020536997_row2720466144725"><td class="cellrowborder" valign="top" width="19.15%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0020536997_p19031219144725"><a name="zh-cn_topic_0020536997_p19031219144725"></a><a name="zh-cn_topic_0020536997_p19031219144725"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.830000000000005%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0020536997_p65133809144725"><a name="zh-cn_topic_0020536997_p65133809144725"></a><a name="zh-cn_topic_0020536997_p65133809144725"></a>响应消息体的MIME类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.019999999999996%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0020536997_p21477025104246"><a name="zh-cn_topic_0020536997_p21477025104246"></a><a name="zh-cn_topic_0020536997_p21477025104246"></a>application/json</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应消息体<a name="section2045571671419"></a>

该部分可选。响应消息体通常以结构化格式（如JSON或XML）返回，与响应消息头中Content-Type对应，传递除响应消息头之外的内容。

## 发送请求<a name="section162124161515"></a>

共有三种方式可以基于已构建好的请求消息发起请求，分别为：

-   cURL

    cURL是一个命令行工具，用来执行各种URL操作和信息传输。cURL充当的是HTTP客户端，可以发送HTTP请求给服务端，并接收响应消息。cURL适用于接口调试。关于cURL详细信息请参见[https://curl.haxx.se/](https://curl.haxx.se/)。

-   编码

    通过编码调用接口，组装请求消息，并发送处理请求消息。

-   REST客户端

    Mozilla、Google都为REST提供了图形化的浏览器插件，发送处理请求消息。针对Firefox，请参见[Firefox
    REST Client](https://addons.mozilla.org/en-US/firefox/addon/restclient/)；针对Chrome，请参见[Chrome REST Client](https://code.google.com/archive/p/rest-client)。


