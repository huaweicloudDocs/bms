# 订单Id的响应<a name="ZH-CN_TOPIC_0131356400"></a>

## 正常响应要素<a name="section5296124617366"></a>

**表 1**  正常响应要素说明

<a name="table757167711151"></a>
<table><thead align="left"><tr id="row5251903911151"><th class="cellrowborder" valign="top" width="19.86%" id="mcps1.2.4.1.1"><p id="p2618376611151"><a name="p2618376611151"></a><a name="p2618376611151"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="23.59%" id="mcps1.2.4.1.2"><p id="p4051029311151"><a name="p4051029311151"></a><a name="p4051029311151"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.55%" id="mcps1.2.4.1.3"><p id="p6010832511151"><a name="p6010832511151"></a><a name="p6010832511151"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3693617411151"><td class="cellrowborder" valign="top" width="19.86%" headers="mcps1.2.4.1.1 "><p id="p3332124712519"><a name="p3332124712519"></a><a name="p3332124712519"></a>order_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.59%" headers="mcps1.2.4.1.2 "><p id="p813044011151"><a name="p813044011151"></a><a name="p813044011151"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.55%" headers="mcps1.2.4.1.3 "><p id="p5458589811151"><a name="p5458589811151"></a><a name="p5458589811151"></a>提交订单成功后返回的订单ID，用户可以使用该ID对订单的处理情况进行查询（在管理控制台的“费用中心 &gt; 我的订单”页面查询）。</p>
</td>
</tr>
</tbody>
</table>

## 异常响应要素<a name="section1651919613712"></a>

**表 2**  异常响应要素说明

<a name="table6467239411151"></a>
<table><thead align="left"><tr id="row2581079811151"><th class="cellrowborder" valign="top" width="19.93%" id="mcps1.2.4.1.1"><p id="p1029990211151"><a name="p1029990211151"></a><a name="p1029990211151"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="23.69%" id="mcps1.2.4.1.2"><p id="p2898571411151"><a name="p2898571411151"></a><a name="p2898571411151"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.379999999999995%" id="mcps1.2.4.1.3"><p id="p6614149111151"><a name="p6614149111151"></a><a name="p6614149111151"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row5586052011151"><td class="cellrowborder" valign="top" width="19.93%" headers="mcps1.2.4.1.1 "><p id="p2840824911151"><a name="p2840824911151"></a><a name="p2840824911151"></a>error</p>
</td>
<td class="cellrowborder" valign="top" width="23.69%" headers="mcps1.2.4.1.2 "><p id="p1936686411151"><a name="p1936686411151"></a><a name="p1936686411151"></a>字典数据结构[1]</p>
</td>
<td class="cellrowborder" valign="top" width="56.379999999999995%" headers="mcps1.2.4.1.3 "><p id="p2558244011151"><a name="p2558244011151"></a><a name="p2558244011151"></a>提交任务异常时返回的异常信息，详情请参见<a href="#table6409189311151">表1 error数据结构</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  error数据结构

<a name="table6409189311151"></a>
<table><thead align="left"><tr id="row2324327311151"><th class="cellrowborder" valign="top" width="20.169999999999998%" id="mcps1.2.4.1.1"><p id="p365693111151"><a name="p365693111151"></a><a name="p365693111151"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="23.369999999999997%" id="mcps1.2.4.1.2"><p id="p2777597711151"><a name="p2777597711151"></a><a name="p2777597711151"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.46%" id="mcps1.2.4.1.3"><p id="p3526170111151"><a name="p3526170111151"></a><a name="p3526170111151"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3762550011151"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p2776668011151"><a name="p2776668011151"></a><a name="p2776668011151"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.4.1.2 "><p id="p3450864111151"><a name="p3450864111151"></a><a name="p3450864111151"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.46%" headers="mcps1.2.4.1.3 "><p id="p4373654211151"><a name="p4373654211151"></a><a name="p4373654211151"></a>任务异常错误信息描述。</p>
</td>
</tr>
<tr id="row5808456411151"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.4.1.1 "><p id="p722924311151"><a name="p722924311151"></a><a name="p722924311151"></a>code</p>
</td>
<td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.4.1.2 "><p id="p4869780211151"><a name="p4869780211151"></a><a name="p4869780211151"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.46%" headers="mcps1.2.4.1.3 "><p id="p5220791411151"><a name="p5220791411151"></a><a name="p5220791411151"></a>任务异常错误信息编码。</p>
</td>
</tr>
</tbody>
</table>

## 响应样例<a name="section1519683320370"></a>

-   正常响应

    ```
    { 
        "order_id": "CS18020810083A4GP"
    } 
    ```

-   异常响应

    ```
    { 
        "error": {"message": "", "code": XXX}
    } 
    ```


