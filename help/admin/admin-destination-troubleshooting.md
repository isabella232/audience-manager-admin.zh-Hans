---
description: 帮助您以Audience Manager设置目标并避免常见问题的信息。
seo-description: 帮助您以Audience Manager设置目标并避免常见问题的信息。
seo-title: 目标设置疑难解答
title: 目标设置疑难解答
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 4%

---


# 目标设置疑难解答{#destination-setup-troubleshooting}

帮助您以Audience Manager设置目标并避免常见问题的信息。

## 我设置了目标，但没看到任何文件。 这些区段在何处？{#destination-no-files}

<!-- c_dest_tshooting.xml -->

常见目标配置问题包括以下问题：

### 目标配置错误

* **错 [!UICONTROL UserID] 误** 键 [!UICONTROL UserID] ：键是 [!UICONTROL MasterDPID] 此目标的基础，是将超出界限的ID值的基础。即使[!UICONTROL UserID]键可通过下拉列表进行选择，也不一定表示存在映射到此值的ID/traits/segments。 如果[!UICONTROL Outbound]进程（在创建目标后运行）找不到映射到此[!UICONTROL UserID]键的任何用户，则不会有任何数据超出界限。
* **未在文件数据源中选** 择：选择除 [!UICONTROL S2S]外的任何目标类型时，标记的屏幕底部会显示一个部分 [!UICONTROL Configure Data Sources]。首次显示此部分时，不选择任何值。 如果您忘记单击[!UICONTROL All First Party]复选框或从[!UICONTROL Available Data Sources]窗口单独选择数据源，则不会有任何数据超出界限。

### 格式错误

在为您的无界数据选择格式时，最好（如果可能）重新使用现有格式。 使用已经过验证的格式，可确保成功生成您的出站数据。 要确切了解现有格式的格式，请单击菜单栏中的[!UICONTROL Formats]选项，然后按名称或ID编号搜索格式。 格式中使用的格式不正确或宏将提供格式不正确的输出，或将阻止完全输出信息。

有关设置格式和使用宏的详细信息，请参阅[文件格式宏](formats/file-formats.md#)和[HTTP格式宏](formats/web-formats.md)。

### 服务器配置错误

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 请勿为主机名输入任何前缀。 如果您有帐户[!DNL ftp://hello.com]，只需在此字段中输入[!DNL hello.com]。
   * **[!UICONTROL Port/Type Combination]**
      * 对于[!DNL FTP]传输，首选传输类型为[!DNL SFTP]。
      * 选择[!DNL SFTP]类型时，端口几乎始终为22。
      * 选择[!DNL FTPs/TLS]类型时，端口几乎始终为21。
      * [!DNL FTPs/TLS]类型与常规[!DNL FTP]传输不同。 我们不支持常规（无担保）[!DNL FTP]转让。
   * **[!UICONTROL Remote Path]**
      * 选择远程子路径时，应输入不带前导斜杠的子路径。
      * 如果传输的文件应放在[!DNL (root)/inbound]子文件夹中，只需为远程路径添加[!DNL inbound]，而不是[!DNL /inbound]。
      * 如果向路径下发送多个文件，请在每个目录之间输入斜杠。 如果您获得位置为[!DNL /inbound/subdirectory1/subdirectory2]，则应在此字段中输入[!DNL inbound/subdirectory1/subdirectory2]。
      * 如果文件应该放在外部服务器自动路由到的目录中，则可以将此空格留空。 请勿输入期间(. )、斜杠(/)或其他任何内容。

* **[!DNL S3]**
   * [!DNL S3] 是首选的传输协议( [!DNL FTP] over或 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 存储段名称应当没有斜杠、前缀、后缀等。 如果给了地址[!DNL s3://your-bucket]，您只需将[!DNL your-bucket]添加到此字段。
      * **[!UICONTROL Directory]**
         * 此字段留空，除非您被特别指定了数据应放入的子目录。 如果您获得地址[!DNL s3://your-bucket/your-subdirectory]，请在[!UICONTROL Bucket]字段中输入[!DNL your-bucket],[!DNL your-subdirectory]应添加到[!UICONTROL Directory]字段。 请勿添加前面的斜杠。
         * 如果必须沿路径下行多个目录，则只应使用斜杠作为分隔符。 因此，[!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2]的位置在[!UICONTROL Bucket]字段中具有[!DNL your-bucket]，在[!UICONTROL Directory]字段中输入[!DNL your-subdirectory1/your-subdirectory2]。
      * **[!UICONTROL Access / Secret Keys]**
         * 当[!DNL TechOps]创建存储段并向顾问提供访问／密钥时，这些凭据通常是`READ-ONLY`要移交给客户端的凭据。 这些凭据不应输入到[!UICONTROL Access / Secret Key]字段中，因为这将导致传输失败（因为这些凭据是只读的，不可写的）。 在[!DNL TechOps]创建存储段并提供凭据的情况下，顾问还应请求一个Adobe密钥对- NOT TO BE GIVED TO THE CLIENT —— 这将允许将文件写入此存储段。 该键应添加到这些字段中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 输入[!DNL HTTP]条目的前缀信息。 如果您有帐户[!DNL https://superduper.com]，请在此字段中输入[!DNL https://superduper.com]。
      * **[!UICONTROL URL Prefix]**
         * 添加[!DNL URL]前缀时，请将前面的斜杠保留为关闭。 [!DNL https://hello.com/r/x/y/z]的地址应在[!UICONTROL Domain]字段中输入[!DNL https://hello.com]，在[!UICONTROL URL Prefix]字段中输入[!DNL r/x/y/z]。
         * 如果不需要[!UICONTROL URL Prefix]，请将此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此框中输入完整的`SSH PRIVATE`键值，包括页眉、页脚和换行符，以确保准确的加密／密钥存储。

### 外发生成时间不足

外界流程每天运行两次，并且多个流程（外界、发布、推送到外部位置等） 必须运行，才能将文件推送到其最终目标。 一个不错的经验法则是，目标应至少在24小时之前完全配置，然后您才能预期数据会推送到外部位置。

### 文件拆分大小过大

将文件外移到目标时，您可以以文件块拆分较大的出站文件。 确保单个文件块不超过10 GB。 另请参阅[出站数据文件名：语法和示例](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html)。


## 如何设置目标以导出出站Experience Cloud文件{#set-up-destinations-export}中的Audience ManagerID、客户ID或客户ID

本页向您介绍如何设置目标以导出[!UICONTROL Outbound Data Files]中所需ID类型的已键入数据。

<!-- set-up-destinations-mcid-aamid.xml -->

目标允许我们的客户在任意数量的数字渠道中激活其数据。 例如，他们可以将受众数据导出到其他[!DNL Adobe Experience Cloud]解决方案（[!DNL Target]、[!DNL Campaign]等）。 或者，他们可以将数据发送到[!UICONTROL DSP]s、[!UICONTROL SSP]s或任何与Audience Manager集成的平台。 我们在[集成Wiki页面](https://wiki.corp.adobe.com/display/MCPI)上保留一列表与我们合作的合作伙伴。

>[!NOTE]
>
>有关在管理员UI中创建目标的详细演练，请参阅[创建或编辑公司目标](companies/admin-manage-company-destinations.md#create-edit-company-destinations)文章。

客户需要导出不同的ID类型，具体取决于目标。 以下配置图显示了您应选择的选项，以导出与不同ID类型相关的用户档案信息。 我们还建议您参考Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)中ID的[索引。 有三个重要设置需要考虑：[!UICONTROL User ID Key]、[!UICONTROL Data Source Type]和[!UICONTROL Format]。 下面我们详细讲述了所有这些。

* [!UICONTROL User ID Key]。在[!UICONTROL Admin UI]中，转到&#x200B;**[!UICONTROL Companies]**。 搜索客户的公司并单击它。 查找&#x200B;**[!UICONTROL Destinations]**&#x200B;选项卡并按&#x200B;**[!UICONTROL Add Destination]**。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流中，选择[!UICONTROL User ID Key]。 [!UICONTROL User ID Key]将过滤来自目标数据源的传入ID，并仅允许ID通过。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience ManagerUI中创建目标时选择此选项。 首先，选择[!UICONTROL Inbound]，然后选择所需的ID类型。 选项有：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此选项确定要导出的文件格式。 在&#x200B;**[!UICONTROL Add Destination]**&#x200B;工作流的&#x200B;**[!UICONTROL Batch Data]**&#x200B;下，选择格式。

要检查格式，请转到&#x200B;**[!UICONTROL Admin UI > Formats]**&#x200B;并查找[!UICONTROL Data Row]元素。 此元素包含文件格式的宏，在以下示例中为&lt;MCID>。

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
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience CloudID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience CloudID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>客户ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>客户 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience CloudID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(公司有权访问的任何数据源) </p> </td> 
   <td colname="col2"> <p>Audience ManagerID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience ManagerUUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 用例

假设您使用Audience Manager和[!DNL Campaign]。 为了使客户数据在[!DNL Campaign]中具有可操作性，您需要导出[!UICONTROL Experience Cloud IDs]。 在这种情况下，应使用配置编号3。