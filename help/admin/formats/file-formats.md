---
description: 列出可用于创建基于FTP的数据文件的宏。一些宏可用于所有数据文件字段和行。其他宏仅特定于标题和数据行。
seo-description: 列出可用于创建基于FTP的数据文件的宏。一些宏可用于所有数据文件字段和行。其他宏仅特定于标题和数据行。
seo-title: 文件格式宏
title: 文件格式宏
uuid: f91c91b6-6581-4ed7-3d7f-f8532 bd41 df9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# 文件格式宏 {#file-format-macros}

列出可用于创建基于创建 [!DNL FTP]的数据文件的宏。一些宏可用于所有数据文件字段和行。其他宏仅特定于标题和数据行。

## 常见宏 {#common-macros}

这些宏可用于任何格式字段。有关示例，请参阅 [文件格式宏示例](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>非打印ASCII字符。它指示一行的开始或内容的一部分。它还可用于在文件中分隔数据列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>目标数据提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_ DPID</code> </p> </td> 
   <td colname="col2"> <p>用户ID密钥数据提供者ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ ID</code> </p> </td> 
   <td colname="col2"> <p>订单/目标ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>订单/目标ID的别名。 </p> <p>此别名的值在目标的 <span class="wintitle"> 外键ID </span> 字段中设置(在 <span class="wintitle"> “基本设置 </span> ”部分中)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>同步模式</code> </p> </td> 
   <td colname="col2"> <p>指示同步类型。接受以下可选变量： </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>：完全同步。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>：增量同步。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>指示数据传输方法。接受以下可选变量： </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>时间戳</code> </p> </td> 
   <td colname="col2"> <p>A10-digital，UTC，Unix时间戳。 </p> <p>它还可以作为 <code>yyyyMMddDHMS格式设置</code> 为以下Java日期/时间戳格式规则。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 标题字段宏 {#header-field-macros}

宏仅在标题字段中使用。有关示例，请参阅 [文件格式宏示例](../formats/file-format-examples.md)。

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

宏仅在数据行中使用。有关示例，请参阅 [文件格式宏示例](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_ COLLY_ STOLUSTER</code> </p> </td> 
   <td colname="col2"> <p>插入隐藏的大括号}字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMA</code> </p> </td> 
   <td colname="col2"> <p>插入逗号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 数据合作伙伴唯一用户标识符 </span>。返回您已分配给用户/站点访问者的ID，如果该ID已经与 <span class="keyword"> Audience Manager </span> 设备ID同步。 </p> <p>如果DPID为0，则此宏将返回 <span class="keyword"> Audience Manager </span> ID而不是用户ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_ UUID_ LIST</code> </p> </td> 
   <td colname="col2"> <p>返回一个列表，其中包含数据合作伙伴的多个ID。如果您拥有多个子部门或允许您共享数据的其他组织组，则此功能很有用。此宏返回这些下级用户组的ID列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUDS</code> </p> </td> 
   <td colname="col2"> <p>此宏的输出将数据提供者ID(DPID)映射到相关的唯一用户ID(DPUUID)。此宏必须具有格式字符串才能控制其输出。示例输出类似于以下内容： </p> <p> <code>“dpds= dpid1，dpid2，… dpid n| maxMapTypes= n| format= json”</code> </p> <p><code>maxMapTypes</code> 设置确定您希望宏返回的映射数。<code>当maxMapTypes=时</code>，此宏返回每个指定DPID的所有映射。数据由时间戳(最近一次)排序，并首先返回最大时间戳的结果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>在使用条件 <code>时(如果</code><code>与SERVER_ LIST</code> 和 <code>REMOVED_ SERVER_ LIST</code> 宏)时需要。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(Segment_ LIST&amp;&amp; REMOVED_ SERVER_ LIST) endif</code> </p> </td> 
   <td colname="col2"> <p>这种宏组合创建了一个条件语句，它列出了用户属于 <i>并且</i> 已从中删除的区段。如果这两种条件均未达到或没有数据，则它会返回一个空字符串。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_ CURLY_ STOLUCK</code> </p> </td> 
   <td colname="col2"> <p>插入一个左大括号{字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>已弃用。不要使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ TERMATY_ TYPE</code> </p> </td> 
   <td colname="col2"> <p>已弃用。不要使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ TERMATY_ VALUE</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 作为静态硬编码值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>合作伙伴ID(PID)。PID会显示在管理UI的 <span class="wintitle"> “配置文件 </span> ”选项卡下。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_ SERVER_ LIST</code> </p> </td> 
   <td colname="col2"> <p>返回已删除的区段列表(如果有)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Segment_ LIST</code> </p> </td> 
   <td colname="col2"> <p>返回列表中区段的列表。接受以下可选变量： </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>SegmentiID</code>：旧版ID。已弃用。使用 <code>sid</code> (仅小写)。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>：旧版ID。已弃用。使用 <code>sid</code> (仅小写)。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>：区段ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>类型</code>：返回 <code>5</code>，一个静态硬编码值，它将数据标识为区段数据。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>别名</code>：区段映射。已弃用。使用 <code>sid</code> (仅小写)。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>laxDisdateTime</code>：指示上次区段被识别时间的Unix时间戳。 </li> 
    </ul> <p>将这些变量放在宏之后大括号中。例如，此代码将结果与管道分开”||“字符： <code>&lt; SUNTERGE_ LIST：{seg||&lt; seg. type&gt;，&lt; seg. sid&gt;}；separator=”||“&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ TERMATS</code> </p> </td> 
   <td colname="col2"> <p>返回 <code>1</code> 作为静态硬编码值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>插入选项卡分隔线。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_ LIST</code> </p> </td> 
   <td colname="col2"> <p>返回特征列表。接受以下可选参数： </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>类型</code>：由数字ID标识的特征类型。此变量返回： 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>标识DPM特征(脱机，由入站作业载入)的10</code> 。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3确定</code> 基于规则的特征(实时、以 <span class="wintitle"> DCS </span>格式提供)。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>陷印ID</code>：特征ID。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastEnabled</code>：上次识别特征的时间。Unix时间戳。 </li> 
    </ul> <p>将这些变量放在宏之后大括号中。例如，此代码将结果与管道分开”||“字符： <code>TRAIT_ LIST{type| TraviID}；separator=”||”</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> 用户ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>