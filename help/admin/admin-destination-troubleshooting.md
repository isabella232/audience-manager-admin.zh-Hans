---
description: 帮助您在Audience manager中设置目标并避免常见问题的信息。
seo-description: 帮助您在Audience manager中设置目标并避免常见问题的信息。
seo-title: ' 目标设置疑难解答'
title: ' 目标设置疑难解答'
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# 目标设置疑难解答 {#destination-setup-troubleshooting}

帮助您在Audience manager中设置目标并避免常见问题的信息。

## 我设置了目标，但我看不到任何文件。 他们在哪？ {#destination-no-files}

<!-- c_dest_tshooting.xml -->

常见的目标配置问题包括以下问题：

### 目标配置错误

* **[!UICONTROL UserID]不正** 确的键：键 [!UICONTROL UserID] 是此目 [!UICONTROL MasterDPID] 标的值，它是将超出界的ID值的基础。 即使密钥 [!UICONTROL UserID] 可以通过下拉列表进行选择，也不一定表示存在映射到此值的ID/特征／区段。 如果进 [!UICONTROL Outbound] 程（在创建目标后运行）找不到映射到此键的任何用户，则不会有 [!UICONTROL UserID] 任何数据超出界限。
* **** 未在文件数据源中选择：当选择除外的任何目标类 [!UICONTROL S2S]型时，屏幕底部将显示一个标记为的部分 [!UICONTROL Configure Data Sources]。 首次显示此部分时，不会选择任何值。 如果您忘记单击该复选框或 [!UICONTROL All First Party] 从窗口中单独选择数据源， [!UICONTROL Available Data Sources] 则不会有任何数据超出界限。

### 格式配置错误

在为您的无界数据选择格式时，最好（如果可能）重新使用现有格式。 使用已经过验证的格式可确保成功生成出站数据。 要准确了解现有格式的格式，请单击菜 [!UICONTROL Formats] 单栏中的选项，然后按名称或ID编号搜索格式。 格式中使用的格式或宏的格式不正确将提供格式不正确的输出，或将阻止完全输出信息。

有关设置格式和使用宏的详细信息，请参 [阅文件格式宏](formats/file-formats.md#) 和 [HTTP格式宏](formats/web-formats.md)。

### 服务器配置错误

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 请勿为主机名输入任何前缀。 如果您有帐户，只 [!DNL ftp://hello.com]需在此字 [!DNL hello.com] 段中输入。
   * **[!UICONTROL Port/Type Combination]**
      * 对于转 [!DNL FTP] 让，优选的转让类型是 [!DNL SFTP]。
      * 选择类型 [!DNL SFTP] 时，端口几乎始终为22。
      * 选择类型 [!DNL FTPs/TLS] 时，端口几乎始终为21。
      * 类 [!DNL FTPs/TLS] 型与常规传输不同 [!DNL FTP] 。 我们不支持定期（无担保）转 [!DNL FTP] 让。
   * **[!UICONTROL Remote Path]**
      * 选择远程子路径时，应输入该路径时不带前导斜杠。
      * 如果传输的文件应放在子文件夹中，只 [!DNL (root)/inbound] 需为远程路径添 [!DNL inbound] 加，而不是添加 [!DNL /inbound]。
      * 如果向路径下发送多个目录，请在每个目录之间输入斜杠。 如果您获得的位置 [!DNL /inbound/subdirectory1/subdirectory2]，则应在此字 [!DNL inbound/subdirectory1/subdirectory2] 段中输入。
      * 如果文件应放在外部服务器自动路由到的目录中，则可以将此空格留空。 请勿输入句点(. )、斜杠(/)或其他任何内容。

* **[!DNL S3]**
   * [!DNL S3] 是首选传输协议(在或之 [!DNL FTP] 上 [!DNL HTTP])。
      * **[!UICONTROL Bucket]**
         * 存储段名称应当不带斜杠、前缀、后缀等。 如果给了您地址， [!DNL s3://your-bucket] 您只需添加 [!DNL your-bucket] 到此字段。
      * **[!UICONTROL Directory]**
         * 将此字段留空，除非您专门为应将数据放置到其中的子目录。 如果给了您地址， [!DNL s3://your-bucket/your-subdirectory]请在字 [!DNL your-bucket] 段中 [!UICONTROL Bucket] 输入，并 [!DNL your-subdirectory] 应将其添加到字 [!UICONTROL Directory] 段。 请勿添加前面的斜杠。
         * 如果必须沿路径向下移动多个目录，则仅应使用斜杠作为分隔符。 因此，某个位 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 置会在 [!DNL your-bucket] 字段中 [!UICONTROL Bucket] 进入 [!DNL your-subdirectory1/your-subdirectory2] 该字段 [!UICONTROL Directory] 中。
      * **[!UICONTROL Access / Secret Keys]**
         * 当创 [!DNL TechOps] 建存储段并向顾问提供访问／密钥时，这些凭据通常是要移交给 `READ-ONLY` 客户端的凭据。 不应将这些凭据输入到字 [!UICONTROL Access / Secret Key] 段中，因为这将导致传输失败（因为这些凭据是只读的，不可写的）。 在创建存储 [!DNL TechOps] 段并提供凭据的情况下，顾问还应请求一个Adobe密钥对（不要给予客户端），以便将文件写入此存储段。 该键应添加到这些字段中。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 输入条目的前缀 [!DNL HTTP] 信息。 如果您有帐户，请 [!DNL https://superduper.com]在此 [!DNL https://superduper.com] 字段中输入。
      * **[!UICONTROL URL Prefix]**
         * 添加前缀 [!DNL URL] 时，请将前面的斜杠保留为关闭。 应已在字 [!DNL https://hello.com/r/x/y/z] 段中输 [!DNL https://hello.com] 入地址， [!UICONTROL Domain] 并在 [!DNL r/x/y/z] 此字段中输入 [!UICONTROL URL Prefix] 地址。
         * 如果不 [!UICONTROL URL Prefix] 需要，请将此值留空。
      * **[!UICONTROL Authentication - SSH Key]**
         * 在此框中输 `SSH PRIVATE` 入完整的键值，包括页眉、页脚和换行符，以确保准确的加密／密钥存储。

### 外发生成时间不足

外部边界进程每天运行两次，并且多个进程（外部边界、发布、推送到外部位置等）必须在将文件推送到其最终目标之前运行。 一个不错的经验法则是，目标应至少在24小时后才能完全配置好，这样您就可以预期数据会被推送到外部位置。

### 文件拆分大小过大

将文件外移到目标时，您可以按文件块拆分较大的外移文件。 确保单个文件块不超过10 GB。 另请参阅 [出站数据文件名：语法和示例](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html)。


## 如何设置目标以在出站数据文件中导出Experience Cloud ID、客户ID或Audience Manager ID {#set-up-destinations-export}

本页向您介绍如何设置目标以导出所需ID类型的已键入数据 [!UICONTROL Outbound Data Files]。

<!-- set-up-destinations-mcid-aamid.xml -->

目标允许我们的客户跨任意数量的数字渠道激活其数据。 例如，他们可以将受众数据导出到其 [!DNL Adobe Experience Cloud] 他解决方[!DNL Target]案( [!DNL Campaign]、等等)。 或者，他们可以将数据发 [!UICONTROL DSP]送到s [!UICONTROL SSP]、s或任何与Audience manager集成的平台。 我们在集成维客页面上保留我们与之合作 [的合作伙伴列表](https://wiki.corp.adobe.com/display/MCPI)。

>[!NOTE]
>
>有关在管理员UI中创建目标的详细演练，请参阅创建或编 [辑公司目标文章](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 。

客户希望导出不同的ID类型，具体取决于目标。 以下配置图显示了您应选择的选项，以导出与不同ID类型相关的配置文件信息。 我们建议您参阅Audience manager中 [的ID索引](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)。 有三个重要的设置要考虑， [!UICONTROL User ID Key]分别是 [!UICONTROL Data Source Type] 、和 [!UICONTROL Format]。 我们在下面详细描述了所有这些内容。

* [!UICONTROL User ID Key]。在中 [!UICONTROL Admin UI]，转到 **[!UICONTROL Companies]**。 搜索客户的公司并单击它。 查找选 **[!UICONTROL Destinations]** 项卡并按 **[!UICONTROL Add Destination]**。 在工作 **[!UICONTROL Add Destination]** 流中，选择 [!UICONTROL User ID Key]。 将 [!UICONTROL User ID Key] 过滤目标数据源中的传入ID，并仅允许ID通过。

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]。在Audience Manager UI中创建目标时选择此选项。 首先，选择 [!UICONTROL Inbound]，然后选择所需的ID类型。 选项包括：

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]。此选项决定要导出的文件格式。 在工作 **[!UICONTROL Add Destination]** 流的下方， **[!UICONTROL Batch Data]**&#x200B;选择格式。

要检查格式，请转 **[!UICONTROL Admin UI > Formats]** 到并查找元 [!UICONTROL Data Row] 素。 此元素包含文件格式的宏，在以下示例中为&lt;MCID&gt;。

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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
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
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>客户ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（公司有权访问的任何数据源） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 用例

假设您使用Audience Manager和 [!DNL Campaign]。 为了使客户数据在中具有可操作性， [!DNL Campaign]您需要导出该数据 [!UICONTROL Experience Cloud IDs]。 在这种情况下，应使用配置编号3。