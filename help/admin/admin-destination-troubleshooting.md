---
description: 帮助您在Audience Manager中设置目标并避免常见问题的信息。
seo-description: 帮助您在Audience Manager中设置目标并避免常见问题的信息。
seo-title: 目标设置疑难解答
title: 目标设置疑难解答
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# 目标设置疑难解答 {#destination-setup-troubleshooting}

帮助您在Audience Manager中设置目标并避免常见问题的信息。

## 我设置了目标，但看不到任何文件。他们在哪里？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常见目标配置问题包括以下问题：

### 未配置的目标

* **密钥不正确[!UICONTROL UserID]：**[!UICONTROL UserID] 关键在于此目标， [!UICONTROL MasterDPID] 它是将超出的ID值的基础。即使 [!UICONTROL UserID] 通过下拉列表可选择键，但它并不一定意味着存在映射到此值的ID/特征/区段。如果 [!UICONTROL Outbound] 该过程(在创建目标后运行)找不到映射到此 [!UICONTROL UserID] 键的任何用户，则不会超出任何数据。
* **未选择文件数据源中的否：** 选择除其他目的以外的任何目标 [!UICONTROL S2S]类型时，屏幕底部会显示一个部分 [!UICONTROL Configure Data Sources]。第一次出现此部分时，不会选择任何值。如果忘记单击 [!UICONTROL All First Party] 复选框或从 [!UICONTROL Available Data Sources] 窗口单独选择数据源，则不会超出任何数据。

### 格式错误

为有限制的数据选择格式时，最好尽可能使用现有格式。使用已经验证过的格式可确保成功生成出站数据。要准确查看现有格式的格式，请单击菜单栏中的 [!UICONTROL Formats] 选项，并按名称或ID编号搜索您的格式。格式格式不正确的格式或宏将提供格式不正确的输出或阻止信息完全输出。

有关设置格式和使用宏的更多信息，请参阅 [文件格式宏](formats/file-formats.md#) 和 [HTTP格式宏](formats/web-formats.md)。

### 未配置的服务器

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 请勿为主机名输入任何前缀。如果您已获得帐户 [!DNL ftp://hello.com]，只需在 [!DNL hello.com] 此字段中输入。
   * **[!UICONTROL Port/Type Combination]**
      * [!DNL FTP] 对于传输，首选传输类型为 [!DNL SFTP]。
      * 选择 [!DNL SFTP] 类型时，端口几乎始终为22。
      * 选择 [!DNL FTPs/TLS] 类型时，端口几乎始终为21。
      * [!DNL FTPs/TLS] 类型与常规 [!DNL FTP] 传输相同。我们不支持定期(不安全) [!DNL FTP] 转让。
   * **[!UICONTROL Remote Path]**
      * 选择远程子路径时，应输入无前导斜杠。
      * 如果您的传输文件应放在 [!DNL (root)/inbound] 子文件夹中，只需为远程路径添加， [!DNL inbound] 而 [!DNL /inbound]不是只添加。
      * 如果向路径发送多个目录，则在每个目录之间输入斜杠。如果您已经获得了位置 [!DNL /inbound/subdirectory1/subdirectory2]，则应在 [!DNL inbound/subdirectory1/subdirectory2] 此字段中输入。
      * 如果文件应放在外部服务器自动路由到的目录中，则可以将此空间留空。请勿输入句点(.)、斜杠(/)或其他任何内容。

* **[!DNL S3]**
   * [!DNL S3] 是首选传输协议(over [!DNL FTP] 或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 桶名称应没有斜杠、前缀、后缀等。如果向您提供了地址 [!DNL s3://your-bucket] ，则只需添加 [!DNL your-bucket] 到此字段。
      * **[!UICONTROL Directory]**
         * 除非您专门为要放置数据的子目录提供了一个子目录，否则将此字段留空。如果您为地址提供了地址 [!DNL s3://your-bucket/your-subdirectory]，请在 [!DNL your-bucket][!UICONTROL Bucket] 字段中 [!DNL your-subdirectory] 输入并添加到 [!UICONTROL Directory] 字段中。请勿添加以前的斜杠。
         * 如果必须向下旅行多个目录，则只有当您使用斜杠作为分隔符时才会使用斜杠。因此，在 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 字段中输入 [!DNL your-bucket] 的 [!UICONTROL Bucket] 位置并 [!DNL your-subdirectory1/your-subdirectory2] 输入 [!UICONTROL Directory] 字段。
      * **[!UICONTROL Access / Secret Keys]**
         * [!DNL TechOps] 创建一个桶并向顾问提供访问/密钥时，这些凭据通常 `READ-ONLY` 是要交给客户端的凭据。这些凭据不应输入 [!UICONTROL Access / Secret Key] 字段，因为这会导致传输失败(因为这些凭据是只读的，不可写)。[!DNL TechOps] 如果创建一个桶并提供凭据，则顾问还应请求Adobe密钥对(不要被授予客户端)，这将允许将文件写入此桶。应将该键添加到这些字段中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 请为 [!DNL HTTP] 条目输入前缀信息。如果您已获得帐户 [!DNL https://superduper.com]，请在 [!DNL https://superduper.com] 此字段中输入。
      * **[!UICONTROL URL Prefix]**
         * 添加 [!DNL URL] 前缀时，请关闭前面的斜杠。应在字段 [!DNL https://hello.com/r/x/y/z] 中 [!DNL https://hello.com] 输入地址并 [!UICONTROL Domain][!DNL r/x/y/z] 在 [!UICONTROL URL Prefix] 字段中输入此地址。
         * 如果不 [!UICONTROL URL Prefix] 需要，请将此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此框中输入 `SSH PRIVATE` 全密键值，包括页眉、页脚和换行，以确保准确的加密/密钥存储。

### 没有足够的出站生成时间

出界流程每天运行两次以及多个流程(出界、发布、转至外部位置等)必须在文件被推送到其最终目标之前运行。一个好规则是，目标应至少完全配置24小时，才有望将数据推送到外部位置。

### 文件拆分大小过大

将文件出站到目标时，您可以将较大的出站文件拆分为文件块。确保单个文件块不超过10GB。另请参阅 [出站数据文件名：语法和示例](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html)。


## 如何设置目标以在出站数据文件中导出Experience Cloud ID、客户ID或Audience Manager ID {#set-up-destinations-export}

本页将向您显示如何设置目标 [!UICONTROL Outbound Data Files]，以关闭您需要的ID类型的数据。

<!-- set-up-destinations-mcid-aamid.xml -->

目标允许我们的客户在任意数量的数字渠道中激活其数据。例如，他们可以将受众数据导出到其他 [!DNL Adobe Experience Cloud] 解决方案([!DNL Target]等 [!DNL Campaign])。或者，他们可以将数据发送到 [!UICONTROL DSP]s、 [!UICONTROL SSP]s或与Audience Manager集成的任何平台。我们会保留我们在 [集成Wiki页面上合作的合作伙伴列表](https://wiki.corp.adobe.com/display/MCPI)。

>[!NOTE]
>
>有关在管理员UI中创建目标的详细演练，请参阅 [“创建”或“编辑公司目标](companies/admin-manage-company-destinations.md#create-edit-company-destinations) ”文章。

客户希望导出不同的ID类型，具体取决于目标。下表显示了您应选择用于导出与不同ID类型相关的配置文件信息的选项。我们建议您还参考Audience Manager中的ID [索引](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)。有三个重要的设置要考虑，即 [!UICONTROL User ID Key][!UICONTROL Data Source Type] 和 [!UICONTROL Format]和。我们详细介绍下面的全部内容。

* [!UICONTROL User ID Key]。[!UICONTROL Admin UI]**[!UICONTROL Companies]**&#x200B;在中，转到。搜索客户的公司并单击它。查找 **[!UICONTROL Destinations]** 选项卡并按。**[!UICONTROL Add Destination]**&#x200B;在 **[!UICONTROL Add Destination]** 工作流中，选择 [!UICONTROL User ID Key]该选项卡。它 [!UICONTROL User ID Key] 将从目标数据源过滤传入的ID，只允许ID传递。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience Manager UI中创建目标时，请选择此选项。首先，选择 [!UICONTROL Inbound]，然后选择所需的ID类型。选项有：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此选项决定您将导出的文件格式。在 **[!UICONTROL Add Destination]** 工作流中 **[!UICONTROL Batch Data]**，选择该格式。

要检查格式，请转到 **[!UICONTROL Admin UI > Formats]** 并查找 [!UICONTROL Data Row] 元素。此元素包含以下示例中的文件格式的宏：&lt; MCID&gt;。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 配置否。 </th> 
   <th colname="col1" class="entry"> <p>用户密钥 </p> </th> 
   <th colname="col2" class="entry"> <p>数据源类型 </p> </th> 
   <th colname="col3" class="entry"> <p>格式 </p> </th> 
   <th colname="col4" class="entry"> <p>导出的ID类型 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>客户ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt; DP_ UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 用例

假设您使用Audience Manager和[!DNL Campaign]为了使客户数据可 [!DNL Campaign]操作，您需要导出 [!UICONTROL Experience Cloud IDs]。在这种情况下，您应使用配置号3。