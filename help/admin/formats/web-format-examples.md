---
description: 一些常用HTTP宏组合的示例。
seo-description: 一些常用HTTP宏组合的示例。
seo-title: ' HTTP格式宏示例'
title: ' HTTP格式宏示例'
uuid: a81a2e2a-de7e-4b6a-8771-fcfa0dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP格式宏示例 {#http-format-macro-examples}

一些常用宏组合 [!DNL HTTP] 的示例。

有关宏 [及其定义的列表](../formats/web-formats.md) ，请参阅HTTP格式宏。

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏示例 </th> 
   <th colname="col2" class="entry"> Output Format（输出格式） </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST;separa=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|users:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;};separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>“Firefox|255.255.255.255|1395758143|42341”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;};separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>“Firefox|255.255.255.255|1395758143|42341”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UUIDS.1&gt;和&lt;DP_UUIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1和dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>users:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; AND &lt;user.dpUids.2&gt;};separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>用户：[dpuuid1和dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAITALIAS_LIST;separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS。(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST;separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST;separa=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users": [&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; "AAM_UUID": "&lt;user.aamUuid&gt;", "DataPartner_UUID": "&lt;user.dpUuuid&gt;", "Segments": [&lt;user.seg|&lt;OPEN_BRACKET&gt;":"&lt;seg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] "Removed_Segments": [&lt;user.removedSegments:{resg|&lt;OPEN_BRACKET&gt;"Segment":"&lt;resg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;}; separ=",",",",",",",","]bracket&gt;}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Users":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segments":[ { "Segment":"alias1" }, { "Segment":"alias2" }], " Removed_Segment" }, { "" alias4" } ] } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users": [&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; "AAM_UUID": "&lt;user.aamUuid&gt;", "DataPartner_UUID": "&lt;user.dpUuuid&gt;", "Segments": [&lt;user.seg|&lt;OPEN_BRACKET&gt;":"&lt;seg.traitAlias&gt;","Status":"&lt;seg.status&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] &lt;CLOSE_BRACKET&gt;}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Users":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segments":[ { "Segment":"alias1" "Status":"1" }, { "Segment":" 0" } } } } } } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;SEGMENTS:{seg|&lt;seg.traitAlias&gt;};separator=\",\"&gt;|&lt;REMOVED_SEGMENTS:{seg|&lt;seg.traitAlias&gt;};separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removedSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>如果字段segments和removedSegments <code>不为空</code> , <code>则打印逗号</code> 。 当连接段和删除的段的列表时，此条件可用于POST请求。 </p> </td> 
  </tr> 
 </tbody> 
</table>
