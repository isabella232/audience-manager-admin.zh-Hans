---
description: 此信息可帮助您在Audience Manager中设置目标和避免常见问题。
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 目标设置疑难解答
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# 目标设置疑难解答 {#destination-setup-troubleshooting}

此信息可帮助您在Audience Manager中设置目标和避免常见问题。

## 我设置了一个目标，但看不到任何文件。 这些区段在何处？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常见的目标配置问题包括以下问题：

### 目标配置错误

* **不正确 [!UICONTROL UserID] 密钥：** 此 [!UICONTROL UserID] 键是 [!UICONTROL MasterDPID] 作为此目标的组成部分，并且是将被出库的ID值的基础。 即使 [!UICONTROL UserID] 键可通过下拉列表进行选择，但这并不一定意味着存在ID/特征/区段映射到此值。 如果 [!UICONTROL Outbound] 进程（在创建目标后运行）未找到映射到此进程的任何用户 [!UICONTROL UserID] 键，不会返回任何数据。
* **未选中文件数据源中的：** 选择目标类型以外的任何目标类型时 [!UICONTROL S2S]，则屏幕底部会显示一个部分，其标签为 [!UICONTROL Configure Data Sources]. 首次显示此部分时，未选择任何值。 如果您忘记单击 [!UICONTROL All First Party] 复选框，或分别从以下位置选择数据源： [!UICONTROL Available Data Sources] 窗口，不会返回任何数据。

### 格式配置错误

在为出站数据选择格式时，如果可能，最好重复使用现有格式。 使用已验证的格式可确保成功生成出站数据。 要准确地查看现有格式的格式，请单击 [!UICONTROL Formats] 选项，并按名称或ID号搜索您的格式。 格式中使用的格式不正确或宏将提供格式不正确的输出或阻止完全输出信息。

有关设置格式和使用宏的更多信息，请参阅 [文件格式宏](formats/file-formats.md#) 和 [HTTP格式宏](formats/web-formats.md).

### 服务器配置错误

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 请勿为主机名输入任何前缀。 如果您有一个帐户 [!DNL ftp://hello.com]，只需输入 [!DNL hello.com] 在此字段中。
   * **[!UICONTROL Port/Type Combination]**
      * 对于 [!DNL FTP] 转移，首选转移类型为 [!DNL SFTP].
      * 选择 [!DNL SFTP] 类型，端口几乎始终为22。
      * 选择 [!DNL FTPs/TLS] 类型，端口几乎始终为21。
      * 此 [!DNL FTPs/TLS] 类型与常规类型不同 [!DNL FTP] 转移。 我们不支持定期（无抵押） [!DNL FTP] 转移。
   * **[!UICONTROL Remote Path]**
      * 选择远程子路径时，输入该路径时不应使用前导斜杠。
      * 如果您传输的文件应放在 [!DNL (root)/inbound] 子文件夹，只需添加 [!DNL inbound] 对于远程路径，而不是 [!DNL /inbound].
      * 如果沿路径将文件发送到多个目录，请在每个目录之间输入斜杠。 如果您被指定了 [!DNL /inbound/subdirectory1/subdirectory2]，您应输入 [!DNL inbound/subdirectory1/subdirectory2] 在此字段中。
      * 如果文件应放置在外部服务器自动路由到的目录中，可将此空间留空。 请勿输入句点( 。 )、斜杠( / )或任何其他内容。

* **[!DNL S3]**
   * [!DNL S3] 是首选传输协议(超过 [!DNL FTP] 或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 存储段名称应不带斜杠、前缀、后缀等标记。 如果你有地址 [!DNL s3://your-bucket] 您只需添加 [!DNL your-bucket] 至此字段。
      * **[!UICONTROL Directory]**
         * 将此字段留空，除非为您专门指定要将数据放置到的子目录。 如果你有地址 [!DNL s3://your-bucket/your-subdirectory]，输入 [!DNL your-bucket] 在 [!UICONTROL Bucket] 字段和 [!DNL your-subdirectory] 应添加到 [!UICONTROL Directory] 字段。 请勿添加前面的斜杠。
         * 如果必须沿路径浏览多个目录，则仅当使用斜杠作为分隔符时。 所以 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 会有 [!DNL your-bucket] 在 [!UICONTROL Bucket] 字段和 [!DNL your-subdirectory1/your-subdirectory2] 已输入 [!UICONTROL Directory] 字段。
      * **[!UICONTROL Access / Secret Keys]**
         * 时间 [!DNL TechOps] 创建一个存储段并向顾问提供访问/密钥，这些凭据通常是 `READ-ONLY` 本该传递给客户的凭据。 不应将这些凭据输入到 [!UICONTROL Access / Secret Key] 字段，因为这将导致传输失败（因为这些凭据是只读的，不可写入）。 在 [!DNL TechOps] 创建一个存储段并提供凭据，顾问还应请求一个Adobe密钥对（不提供给客户端），以允许将文件写入此存储段。 应将该键添加到这些字段中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 请输入 [!DNL HTTP] 个条目。 如果您有一个帐户 [!DNL https://superduper.com]，输入 [!DNL https://superduper.com] 在此字段中。
      * **[!UICONTROL URL Prefix]**
         * 添加 [!DNL URL] 前缀，将前面的斜杠保留为关闭。 地址 [!DNL https://hello.com/r/x/y/z] 应该具有 [!DNL https://hello.com] 输入于 [!UICONTROL Domain] 字段和 [!DNL r/x/y/z] 在此输入的 [!UICONTROL URL Prefix] 字段。
         * 如果 [!UICONTROL URL Prefix] 不需要，请将此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 输入完整的 `SSH PRIVATE` 此框中的密钥值（包括页眉、页脚和换行符）可确保精确的加密/密钥存储。

### 出站生成时间不足

扩展流程每天运行两次，并运行多个流程（扩展、发布、推送到外部位置等） 必须先运行，然后才能将文件推送到其最终目标。 一个好的经验法则是，至少应在24小时内完全配置目标，之后才能将数据推送到外部位置。

### 文件拆分大小太大

将文件出站到目标时，可以将较大的出站文件分割为文件块。 确保各个文件块不超过10 GB。 另请参阅， [出站数据文件名：语法和示例](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## 如何设置目标以导出出站数据文件中的Experience CloudID、客户ID或Audience ManagerID {#set-up-destinations-export}

本页向您说明如何设置目标以导出与您要输入的ID类型无关的数据 [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

目标允许我们的客户在任意数量的数字渠道中激活其数据。 例如，他们可以将受众数据导出到其他 [!DNL Adobe Experience Cloud] 解决方案([!DNL Target]， [!DNL Campaign]、等)。 或者，他们可以将数据发送到 [!UICONTROL DSP]s， [!UICONTROL SSP]或任何与Audience Manager集成的平台。 我们有一份合作伙伴名单 [集成维客页面](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>有关在管理员UI中创建目标的详细演练，请查看 [创建或编辑公司目标](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 文章。

您的客户希望导出不同的ID类型，具体取决于目标。 下面的配置图显示了导出与不同ID类型相关的配置文件信息时应选择的选项。 我们建议您同时参阅 [Audience Manager中的ID索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). 需要考虑三个重要设置： [!UICONTROL User ID Key]，则 [!UICONTROL Data Source Type] 和 [!UICONTROL Format]. 我们将在下面详细介绍所有这些功能。

* [!UICONTROL User ID Key]。在 [!UICONTROL Admin UI]，转到 **[!UICONTROL Companies]**. 搜索客户的公司并单击它。 查找 **[!UICONTROL Destinations]** Tab键并按 **[!UICONTROL Add Destination]**. 在 **[!UICONTROL Add Destination]** 工作流，选择 [!UICONTROL User ID Key]. 此 [!UICONTROL User ID Key] 将筛选来自目标数据源的传入ID，并仅允许ID通过。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience ManagerUI中创建目标时选择此选项。 首先，选择 [!UICONTROL Inbound]，然后选择所需的ID类型。 选项包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此选项决定要导出的文件格式。 在 **[!UICONTROL Add Destination]** 工作流，在 **[!UICONTROL Batch Data]**，选择格式。

要检查格式，请转到 **[!UICONTROL Admin UI > Formats]** 并查找 [!UICONTROL Data Row] 元素。 此元素包含文件格式的宏， &lt;mcid> 在以下示例中。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 配置编号 </th> 
   <th colname="col1" class="entry"> <p>用户密钥 </p> </th> 
   <th colname="col2" class="entry"> <p>数据源类型 </p> </th> 
   <th colname="col3" class="entry"> <p>格式 </p> </th> 
   <th colname="col4" class="entry"> <p>导出的ID类型 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>客户ID (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGERID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGERUUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 用例

假设您使用Audience Manager和 [!DNL Campaign]. 为了使客户数据可在以下位置操作 [!DNL Campaign]，您希望导出 [!UICONTROL Experience Cloud IDs]. 在这种情况下，您应该使用配置编号3。
