---
description: 使用宏创建出站、FTP文件模板的示例。
seo-description: 使用宏创建出站、FTP文件模板的示例。
seo-title: 文件格式宏示例
title: 文件格式宏示例
uuid: f00d431d-7e43-457a-b633-c79 cbc4 c8 f10
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# 文件格式宏示例 {#file-format-macro-examples}

如何使用宏创建出站、 [!DNL FTP] 文件模板的示例。

>[!NOTE]
>
>在表中 **，粗体** 类型可识别每个宏及其相关输出。对于格式示例，添加了&lt;&gt;符号以帮助可视化地分离每个宏。

## 常见宏 {#common-macros}

这些宏可用于任何格式字段。有关完整的列表和定义，请参阅 [文件格式宏](../formats/file-formats.md) 。

<table id="table_B5073597219B470298EE614902DACAE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 格式和输出示例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>输出： <code>ftp_215_888_ iter_1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; MASTER_ DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>输出： <code>ftp_215_888_20915_ iter_1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>输出： <code>ftp_215_888_ iter_1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步模式 </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>Output（输出）: 
     <ul id="ul_F63D7B78AF1246639D6ED85C1621B17C"> 
      <li id="li_4D0D7B4D047345FE861FCBA2BD0408ED">完全： <code>ftp_215_888_ full_1449756724. sync </code> </li> 
      <li id="li_23F4D1F6B2784E599EDA29AA457327E6">增量： <code>ftp_215_888_ iter_1449756724. sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ TYPE </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>Output（输出）: 
     <ul id="ul_11B14E740E40474F8302BDB809C428FE"> 
      <li id="li_54A3EAA468B44AC8B2528F855E03D04B">FTP： <code>ftp_215_888_ iter_1449756724. sync </code> </li> 
      <li id="li_93468C56B661463CA7F62B1F5D3A53FF">https： <code>http_215_888_ iter_1449756724. sync </code> </li> 
      <li id="li_8A204C7BEDBC41C096FE953B5F827DEC">S3： <code>s3_215_888_ iter_1449756724. sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>时间戳 </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; SYNC_ TYPE&gt;_&lt; ORDER_ ID&gt;_&lt; DPID&gt;_&lt; SYNC_ MODE&gt;_&lt; TIMESTAMP&gt;. sync </code> </p> <p>输出： <code>ftp_215_888_ iter_1449756724. sync </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 标题字段宏 {#header-field-macros}

宏仅在标题字段中使用。有关完整的列表和定义，请参阅 [文件格式宏](../formats/file-formats.md) 。

<table id="table_ABC31B3D660D47969E111EBC734D5BBC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 格式和输出示例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; ORDER_ ID&gt;&lt; TAB&gt;&lt; SYNC_ TYPE&gt; </code> </p> <p>输出： <code>888full. sync </code> </p> <p>在输出中，非打印选项卡字符将分隔每个元素。 </p> </td>
  </tr>
 </tbody>
</table>

## 数据行宏 {#data-row-macros}

宏仅在标题字段中使用。有关完整的列表和定义，请参阅 [文件格式宏](../formats/file-formats.md) 。

<table id="table_408C6DD2B9D54550B003EAC93562E64F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 格式和输出示例 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>输出： <code>123456UUID UUID UUID2UUID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>输出： <code>123456UUID UUID UUID2UUID3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST&amp;&amp; REMOVED_ SERVER_ LIST </code> </p> </td> 
   <td colname="col2"> <p>此示例创建一种格式，可在服务器到服务器源中返回删除的区段。 </p> <p> 
     <code>{“advertiseriID”：“&lt; PIDAAS&gt;”、“dataEnterID”：2，“TID”：“&lt; DP_ UUID&gt;”，
“数据”：[&lt; SUNTENCE_ LIST：{seg||&lt; OPEN_ COLLY_ STAREN&gt;“名称”：“&lt; seg. alias&gt;”&lt; CLOSE_ COURLY_ HOSTER&gt;}；
separator="，"&gt;&lt;(Segment_ LIST&amp;&amp; REMOVED_ SERVER_ LIST)&gt;&lt; COMMMA&gt;&lt; endif&gt;
&lt; REMOVED_ SERVER_ LIST：{seg||&lt; OPEN_ COLLY_ STAREN&gt;“名称”：“&lt; seg. alias&gt;”，
“ttlinMinutes”：&lt; CLOSE_ COLLY_ HOSTER&gt;}；separator="，"&gt;]} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; SERVER_ LIST&gt;；separator="&gt; </code> </p> <p>输出： <code>12345610595510118310118010119 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ TERMATS </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; PID&gt;&lt; TAB&gt;&lt; UUID&gt;&lt; UUID&gt;&lt; TAB&gt;&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; SET_ OUTTIONS&gt;&lt; TAB&gt;&lt; OPTION_ OUT&gt;&lt; TAB&gt;&lt; SUNCTION_ LIST：{seg||&lt; seg. type&gt;、&lt; see. alias&gt;、&lt; OUTPUT_ PROGATIBER_ VALUE&gt;、&lt; Seg. laxDisdateTime&gt;&amp;}&gt; </code> </p> <p>输出： <code>115900080085796796836537415797507373717T0aj01b120p1，1344114661000&amp;5,103713,1,1343250661000 </code> </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <code>TAB </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; DP_ UUID_ LIST；separator= TAB&gt; </code> </p> <p>输出： <code>123456UUID UUID UUID2UUID3 </code> </p> <p>在输出中，非打印选项卡字符将分隔每个元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST </code> </p> </td> 
   <td colname="col2"> <p>格式： <code>&lt; PID&gt;&lt; TAB&gt;&lt; DP_ UUID&gt;&lt; TAB&gt;&lt; SET_ PATIONS&gt;&lt; TAB&gt;&lt; TraIT_ LIST；分隔符=||”&gt; </code> </p> <p>输出： <code>113112345 123||456||789 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>
