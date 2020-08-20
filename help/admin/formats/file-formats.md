---
description: 列表可用于创建基于FTP的数据文件的宏。 某些宏可用于所有数据文件字段和行。 其他宏仅特定于标题和数据行。
seo-description: 列表可用于创建基于FTP的数据文件的宏。 某些宏可用于所有数据文件字段和行。 其他宏仅特定于标题和数据行。
seo-title: 文件格式宏
title: 文件格式宏
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---


# 文件格式宏 {#file-format-macros}

列表可用于创建基于数据文 [!DNL FTP]件的宏。 某些宏可用于所有数据文件字段和行。 其他宏仅特定于标题和数据行。

## 常见宏 {#common-macros}

这些宏可用于任何格式字段。 有关示例，请参 [阅文件格式宏示例](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>非打印ASCII字符。 它指示行或内容部分的开始。 它还可以用于在文件中分隔数据列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目标数据提供程序ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>用户ID密钥数据提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>订单／目标ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>订单／目标ID的别名。 </p> <p>此别名的值在目标的外 <span class="wintitle"> 来帐户ID </span> 字段中设置(在“基本设 <span class="wintitle"> 置”部分 </span> )。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>指示同步类型。 接受以下可选变量： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>:完全同步。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>:增量同步。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>指示数据传输方法。 接受以下可选变量： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>一个10位的UTC Unix时间戳。 </p> <p>也可以按照Java日期／时 <code>YYYYMMDDhhmmss</code> 间戳格式化规则设置格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 标题字段宏 {#header-field-macros}

宏仅用于标题字段。 有关示例，请参 [阅文件格式宏示例](../formats/file-format-examples.md)。

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>此宏用作分隔符，在字段之间插入一个选项卡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 数据行宏 {#data-row-macros}

仅用于数据行的宏。 有关示例，请参 [阅文件格式宏示例](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入一个右大括号 <code>}</code> 字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 数据合作伙伴唯一用户标识 </span>符。 返回您分配给用户／站点访客的ID(如果该ID已与Audience Manager设备ID同 <span class="keyword"> 步 </span> )。 </p> <p>如果DPID为0，则此宏将返回 <span class="keyword"> Audience Manager </span> ID而不是用户的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回一个列表，其中包含数据合作伙伴的多个ID。 如果您有一个大型组织，并且有多个子组织或允许您与其共享数据的其他组织组，则此功能很有用。 此宏返回这些下属组的ID列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>此宏的输出将数据提供者ID(DPID)映射到相关的唯一用户ID(DPUUID)。 此宏必须具有格式字符串才能控制其输出。 示例输出将类似于： </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>设 <code>maxMappings</code> 置确定希望宏返回的映射数。 当 <code>maxMappings=0</code>时，此宏返回每个指定DPID的所有映射。 数据按时间戳（最新的前一个）排序，并首先返回具有最大时间戳的结果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>使用条件和 <code>if</code> 宏时 <code>SEGMENT_LIST</code> 需 <code>REMOVED_SEGMENT_LIST</code> 要。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>此宏组合会创建一个条件语句，该语句列表用户所属的 <i>区段</i> ，并已从中删除这些区段。 如果两个条件都不满足或没有数据，则返回空字符串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>插入一个左大括号 <code>{</code> 字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>已弃用。不要使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>已弃用。不要使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 为静态的硬编码值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作伙伴ID(PID)。 该PID显示在管理 <span class="wintitle"> 员 </span> UI的“用户档案”选项卡下。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回已删除的区段列表（如果有）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回列表中的区段。 接受以下可选变量： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>:旧ID。 已弃用。使 <code>sid</code> 用（仅小写）。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>:旧ID。 已弃用。使 <code>sid</code> 用（仅小写）。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>:区段ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>:返回 <code>5</code>一个静态的硬编码值，它将数据标识为段数据。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>:区段的映射。 已弃用。使 <code>sid</code> 用（仅小写）。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>:一个Unix时间戳，指示上次实现段的时间。 </li> 
    </ul> <p>将这些变量放在宏后面的大括号中。 例如，此代码用管道“|”字符分隔结果： <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 为静态的硬编码值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入制表符分隔符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>返回特征列表。 接受以下可选参数： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>:由数字ID标识的特征类型。 此变量返回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> 它标识DPM特征（脱机，由入站作业载入）。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> 识别基于规则的特征(实时、;已载入DCS <span class="wintitle"> 中 </span>)。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>:特征ID。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>:上次这个特质被发现。 Unix时间戳。 </li> 
    </ul> <p>将这些变量放在宏后面的大括号中。 例如，此代码用管道“|”字符分隔结果： <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> 用户ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>