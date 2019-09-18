---
description: Audience Manager管理指南的所有更新（添加、删除和更正）（按日期）。
seo-description: Audience Manager管理指南的所有更新（添加、删除和更正）（按日期）。
seo-title: 文档更新
title: 文档更新
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
translation-type: tm+mt
source-git-commit: e60aa0ac341d74454bfe00a4f56add3a9f9e281b

---


# 文档更新 {#documentation-updates}

Audience Manager管理指南的所有更新（添加、删除和更正）（按日期）。

有关功能发布、增强和错误修复的信息，请参阅 [Experience cloud发行说明](https://marketing.adobe.com/resources/help/en_US/whatsnew/)。 有关 Experience Cloud 的早期公告，请参阅[之前的发行说明](https://marketing.adobe.com/resources/help/en_US/whatsnew/c_legacy_releases.html)。有关文 [!DNL Audience Manager documentation changes, see] 档 [更新](https://docs.adobe.com/content/help/en/audience-manager/user-guide/documentation-updates/docs-2019.html)。

## AAM 2019文档更新 {#aam-2019-docs-updates}


| 主题 | 描述 |
---------|----------|
| HTTP格式宏 | 我们为宏加了一个 `REGION_ID_LIST`新的宏，`sda``sda`，加了三个新的 `sda``USER_LIST` 字段。 |
| HTTP格式宏 | 我们添加了两个新宏： `ECID` 和 `MCID`。 |


## AAM 2018文档更新 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> 创建或编辑FTP服务器</a> </p> </td> 
   <td colname="col2"> <p>我们添加了有关SFTP服务器的SSH密钥身份验证的更多信息（步骤5）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> 如何设置目标以导出Experience Cloud...</a> </p> </td> 
   <td colname="col2"> <p>本页向您介绍如何设置目标，以导出在“出站数据文件”中要导出的ID类型所键入的数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> 操作方法：授权批处理目标的跨帐户Amazon S3存储段访问</a> </p> </td> 
   <td colname="col2"> <p>如果客户不希望共享Amazon S3访问密钥和密钥，则可以使用Amazon S3中的跨帐户存储段权限来传送出站数据文件。 本文档向您介绍如何在Audience Manager管理员UI中设置此替代方法。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017文档更新 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP格式宏</a> </td> 
   <td colname="col2">用legacySegmentId <code>替换了segmentId</code> 宏，并添加了 <code>newSegmentId</code> 宏 <code></code> 。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> 管理公司限制</a> </td> 
   <td colname="col2"> 为限制文档添加了最大特征文件夹编号和特征结构深度。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> 启用Hadoop序列文件传输以进行出站</a> </td> 
   <td colname="col2"> 阅读如何使客户能够将Outbound SEQ文件发送到其自己的Hadoop实例。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> 管理容器</a> </td> 
   <td colname="col2"> 添加了有关如何创建容器的简短说明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> 创建或编辑公司目标</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">添加了有关平衡使用完全同步和增量同步的说明。 </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7">将 <span class="keyword"> Adobe Media Optimizer</span> (Audience Manager)设置为 <span class="keyword"> Audience Manager</span> 目标是在 <span class="keyword"> Adobe Media Optimizer中完成的</span>。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>次要修订。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> ID与Media Optimizer同步</a> </p> </td> 
   <td colname="col2"> <p>描述每个公司容器中AMO同步复选框的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> 公司的设备图选项</a> </p> </td> 
   <td colname="col2"> <p>介绍如何配置设备图形选项的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API要求和建议</a> </p> </td> 
   <td colname="col2"> <p>新文档描述了需要了解和传递给客户的一些要求和建议。 在公共文档中，此字段会重复，其标题和更改与其他阅读受众相同。 请参 <a href="https://marketing.adobe.com/resources/help/en_US/aam/aam-api-requirements.html" format="https" scope="external"> 阅公共文档中的</a> API要求和建议。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016文档更新 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> 创建或编辑FTP服务器</a> </td> 
   <td colname="col2">添加了出口FTP IP <b>52.44.29.204</b>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>次要修订。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> 创建或编辑HTTP服务器</a> </p> </td> 
   <td colname="col2"> <p>向“ <b>创建服务器配置</b> ”向导添加了HTTP签名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> 测试版环境</a> </p> </td> 
   <td colname="col2"> <p>测试版环境中更新的URL和主机名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> 仅按活动用户过滤出站数据</a> </p> </td> 
   <td colname="col2"> <p>生成仅包含活动用户的完全同步文件的说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP格式宏</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>列出HTTP宏和常见示例的新文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP格式宏示例</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015文档更新 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015年12月 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>修改了宏部分并添加了示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014文档更新 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日期和主题 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014年11月12日 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>添加了有关&lt;MCID&gt;宏的信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月23日 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> 创建或编辑格式</a> </p> </td> 
   <td colname="col2"> <p>添加了有关“.info收 <span class="wintitle"> 据”选项的 </span>信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月23日 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 格式</a> </p> </td> 
   <td colname="col2"> <p>新页面。 请注意，此页面是进行中的工作，将在未来几天内进行更新。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年10月22日 </p> <p><a href="admin-destination-troubleshooting.md#"> 目标设置疑难解答</a> </p> </td> 
   <td colname="col2"> <p>新主题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 21 日 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 管理公司目标</a> </p> </td> 
   <td colname="col2"> <p>重写了整个主题。添加了其他信息和其他设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年9月25日 </p> <p><a href="companies/admin-manage-company-profiles.md"> 创建公司</a> </p> </td> 
   <td colname="col2"> <p>向“生命周期”和“帐户类 <span class="wintitle"> 型</span> ”部分添加 <span class="wintitle"> 了其他信息</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014年9月25日 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> 编辑公司配置文件</a> </p> </td> 
   <td colname="col2"> <p>向“生命周期”和“帐户类 <span class="wintitle"> 型</span> ”部分添加 <span class="wintitle"> 了其他信息</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>