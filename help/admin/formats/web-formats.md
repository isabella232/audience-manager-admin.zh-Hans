---
description: 列出可用于创建HTTP数据文件的宏。HTTP以JSON格式发送数据。
seo-description: 列出可用于创建HTTP数据文件的宏。HTTP以JSON格式发送数据。
seo-title: HTTP格式宏
title: HTTP格式宏
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# HTTP格式宏 {#http-format-macros}

列出可用于创建 [!DNL HTTP] 数据文件的宏。[!DNL HTTP] 以 [!DNL JSON] 格式发送数据。

有关列表和一些常用宏组合的示例，请参阅 [HTTP格式宏示例](../formats/web-format-examples.md) 。

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 方法类型 </th> 
   <th colname="col3" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Audience Manager </span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>数据合作伙伴唯一用户ID。如果用户ID已经与 <span class="keyword"> Audience Manager </span> 设备ID同步，则此宏返回您分配给用户的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>数据提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>EID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>数据提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Generation_ TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>Unix UTC时间戳。内部时间戳表示AAM向我们的合作伙伴发布 <span class="wintitle"> S </span> 2S目标的时间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户的IP地址。 </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (McID代表Marketing Cloud，它是Experience Cloud的旧名称) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ REMOVED_ TERSIONS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户不再属于的区段的数字(整数)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_ SERSIONS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户所属的区段数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>订单或目标ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET，POST</code> </p> </td> 
   <td colname="col3"> <p>合作伙伴ID的别名。也称为外键ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>随机</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>生成随机数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>LOCAL_ ID_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p><a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience Manager DCS所 </a> 在的活动区域。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SERVER_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>返回用户不再符合资格的区段ID(如果有)的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ ENTERSIONS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户不再符合资格的区段列表。您还可以返回特定的区段字段，包括： </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>Tritalias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>legacySegmentiID(之前名为SegmentiID)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>NewSegmentiID</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>DateTime</code> </li> 
     </ul> </p> <p>在数组中指定这些字段，如本示例所示： </p> <p> <code>[&lt; REMOVED_ SERVES：{seg||&lt; Open_ STOLUBER&gt;“映射”：&lt; seg. Tritalias&gt;，“Status：“&lt; seg. status&gt;，“Time”：&lt; seg. dateTime&gt;、“legacySegmentiID”：&lt; seg. legacySegmentiID&gt;，“newSegmentiID”：&lt; seg. newSegmentiID&gt;&lt; CLOSE_ STOLD&gt;}；“separator=”，"&gt;]</code> </p> <p>另请参阅 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式宏示例 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> 用户不再符合资格的区段的上次真实性列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ TraITIRAAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户不再符合资格的区段别名列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>返回区段ID列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segments</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>用户有资格获得的区段列表。您还可以返回特定的区段字段，包括： </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>Tritalias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>legacySegmentiID(之前名为SegmentiID)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>NewSegmentiID</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>DateTime</code> </li> 
     </ul> </p> <p>在数组中指定这些字段，如本示例所示： </p> <p> <code>[&lt;区段：{seg||&lt; Open_ STOLUBER&gt;“映射”：&lt; seg. Tritalias&gt;，“Status：“&lt; seg. status&gt;，“Time”：&lt; seg. dateTime&gt;、“legacySegmentiID”：&lt; seg. legacySegmentiID&gt;，“newSegmentiID”：&lt; seg. newSegmentiID&gt;&lt; CLOSE_ STOLD&gt;}；“separator=”，"&gt;]</code> </p> <p>另请参阅 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式宏示例 </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>上一个真实性的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>时间戳</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix，UTC时间戳。表示区段的最后实现。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TraITIRAAS_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>特定区段的别名名称列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>初始请求的用户代理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_ LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p><span class="keyword"> Audience Manager </span> 用户ID列表。您还可以返回包含以下内容的特定字段： </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user. AamuUID</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user. dpuUID</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user. segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user. removedSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user. userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user. ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user. dpuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user. timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user. random</code> </li>
     <li><code>user. regionID</code></li> 
    </ul> <p>指定这些字段，如以下示例所示： </p> <p> 
     <codeblock>
       “AAM_ UUID”：“&lt; user. aamuUID&gt;”dataAtNer_ UUID”：“&lt; user. dpuUID&gt;” 
     </codeblock> </p> <p>有关完整示例，请参阅 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式宏示例 </a> 。 </p> </td> 
  </tr>
 </tbody>
</table>