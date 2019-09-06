---
description: 一些常用的HTTP宏组合的示例。
seo-description: 一些常用的HTTP宏组合的示例。
seo-title: HTTP格式宏示例
title: HTTP格式宏示例
uuid: a81a2e2a-de7 e-4b6 a-8771-fcfa0 dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP格式宏示例 {#http-format-macro-examples}

一些常用 [!DNL HTTP] 宏组合的示例。

有关宏及其定义的列表，请参阅 [HTTP格式宏](../formats/web-formats.md) 。

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏示例 </th> 
   <th colname="col2" class="entry"> Output Format（输出格式） </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;||&lt; DP_ UUID&gt;||&lt; TraITIRAAS_ LIST；separator="，"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| tratentity_1，traentity_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;|计数：&lt; NUM_ USERS&gt;|用户：[&lt; USER_ LIST：{user||&lt; user. aamuUID&gt;：&lt; user. dpuUID&gt;}；separator="，"&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>“pid_ alias| count：|用户：[uuid1：dpuid1，uuid2：dpuid2]”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ AGENT&gt;||&lt; IP&gt;||&lt; TIMESTAMP&gt;||&lt; ANDUMERY&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>“Firefox|255.255.255.255|1395758143|42341”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; USER_ LIST：{u||&lt; u. userAgent&gt;||&lt; u. ip&gt;||&lt; u. timestamp&gt;||&lt; u random&gt;}；separator="，"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>“Firefox|255.255.255.255|1395758143|42341”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; DP_ UUID.1&gt;和&lt; DP_ UUID.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuid1AND dpuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>用户：[&lt; USER_ LIST：{user||&lt; user. dpuID.1&gt; AND&lt; user. dPuID.2&gt;}；separator="，"&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>用户：[dpuuid1AND dpuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ known_ string= loamemlipsum&amp; segid=&lt; TraITARIAS_ LIST；separator="，"&gt;&amp; test_ dpuid_1000=&lt; DP_ UUID.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ known_ string= loememlipsum&amp; segid= traentifetch&amp; segid_2，traical_2&amp; test_ dpuid_1000= dpuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ dpuids=&lt; DP_ UUID。(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ dpuids= dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>“&lt; PID_ ALIAS&gt;||&lt; DP_ UUID&gt;||&lt; TraITIRAAS_ LIST；separator="，"&gt;||&lt; REMOVED_ TRAITALIAS_ LIST；separator="，"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| tratentity_1，traentity_2| traentity_3，traentity_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{“用户”：[&lt; USER_ LIST：{user||&lt; Open_ STOLUBER&gt;
“AAM_ UUID”：“&lt; user. AamuUID&gt;”，
“DataAtner_ UUID”：“&lt; user. dpuUID&gt;”，
“区段”：[&lt; user. segments：{seg||&lt; OPEN_ STOLMESTER&gt;“区段”：”&lt; sg. Tritalias&gt;”&lt; CLOSE_ STOLD&gt;}；separator="，"&gt;]
“删除的_区段”：[&lt; user. removedSegments：{rseg||&lt; OPEN_ STOLMESTER&gt;“区段”：“&lt; rseg. traialias&gt;”&lt; CLOSE_ STOLD&gt;}；separator="，"&gt;]
&lt; CLOSE_ HOSTER&gt;}；separator="，"&gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“用户”：[[[
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“AAM_ UUID”：“uuid1”，
“DataAtner_ UUID”：“dpuuid1”，
“区段”：[[[
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名1”
}
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名2”
}}
]，
“删除的_区段”：[[[
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名3”
}
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名4”
}}
]
}}
]
}} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{“用户”：[&lt; USER_ LIST：{user||&lt; Open_ STOLUBER&gt;
“AAM_ UUID”：“&lt; user. AamuUID&gt;”，
“DataAtner_ UUID”：“&lt; user. dpuUID&gt;”，
“区段”：[&lt; user. segments：{seg||&lt; OPEN_ STOLMESTER&gt;“区段”：“&lt; sg. traialias&gt;”，“Status”：“&lt; seg. status&gt;”&lt; CLOSE_ STOLD&gt;}；separator="，"&gt;]
&lt; CLOSE_ HOSTER&gt;}；separator="，"&gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“用户”：[[[
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“AAM_ UUID”：“uuid1”，
“DataAtner_ UUID”：“dpuuid1”，
“区段”：[[[
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名1”
“状态”：“1”
}
{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{{
“区段”：“别名2”
“状态”：“0”
}}
]
}}
]
}} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; PID_ ALIAS&gt;||&lt; DP_ UUID&gt;||&lt;区段：{seg||&lt; seg. Tritalias&gt;}；separator=\"，\"&gt;||&lt; REMOVED_ SERVES：{seg||&lt; seg. Tritalias&gt;}；separator=\"，\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias| dp_ uuid| tratentity_1，traentity_2| traentity_3，traentity_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; if(user. segments&amp;&amp; user. removedSegments)&gt;&lt; COMMMA&gt;&lt; endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>如果字段 <code>区段</code> 和 <code>removed区段</code> 不是空，则打印逗号。此条件可用于在连接区段和删除区段列表时用于POST请求。 </p> </td> 
  </tr> 
 </tbody> 
</table>
