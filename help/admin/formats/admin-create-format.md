---
description: 使用Audience Manager管理工具中的格式页面创建新格式或编辑现有格式。
seo-description: 使用Audience Manager管理工具中的格式页面创建新格式或编辑现有格式。
seo-title: 创建或编辑格式
title: 创建或编辑格式
uuid: ca1b1cb-bcd3-4a41-b1 e8-80565f6 c23 ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 创建或编辑格式 {#create-or-edit-a-format}

使用Audience Manager管理工具中的 [!UICONTROL Formats] 页面创建新格式或编辑现有格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>为有限制的数据选择格式时，最好尽可能使用现有格式。使用已经验证过的格式可确保成功生成出站数据。要准确查看现有格式的格式，请单击菜单栏中的 [!UICONTROL Formats] 选项，并按名称或ID编号搜索您的格式。格式格式不正确的格式或宏将提供格式不正确的输出或阻止信息完全输出。

1. 要创建新格式，请单击 **[!UICONTROL Formats]** &gt; **[!UICONTROL Add Format]**。要编辑现有格式，请在 **[!UICONTROL Name]** 列中单击所需的格式。

   ![](assets/create_format.png)

1. 填写以下字段：
   * **名称：** (必需)为该格式提供一个描述性名称。
   * **类型：** (必需)选择所需格式：
      * **[!UICONTROL File]**：通过 [!DNL FTP] 文件发送数据。
      * **[!UICONTROL HTTP]**：在 [!DNL JSON] 包装器中封闭数据。

1. (视情况而定)如果选择 **[!UICONTROL File]**，请填写字段：

   >[!NOTE]
   >
   >有关可用宏的列表，请参阅 [文件格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 和 [HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)。

   * **[!UICONTROL File Name]：** 指定数据传输文件的文件名。
   * **标题：** 指定显示在数据传输文件的第一行中的文本。
   * **[!UICONTROL Data Row]：** 指定在文件的每个出站行中显示的文本。
   * **[!UICONTROL Maximum File Size (In MB)]：** 为数据传输文件指定最大文件大小。压缩的文件必须小于100MB。未压缩文件大小没有限制。
   * **[!UICONTROL Compression]：** 选择所需的压缩类型：gz或zip，用于您的数据文件。要分发到 [!UICONTROL AWS S3]，您必须使用.gz或未压缩的文件。
   * **[!UICONTROL .info Receipt]：** 指定生成transfer-control([!DNL .info])文件。[!DNL .info] 该文件提供有关文件传输的元数据信息，以便合作伙伴能够验证Audience Manager是否正确处理了文件传输。有关详细信息，请参阅 [传输控制文件以进行日志文件传输](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html)。
   * **[!UICONTROL MD5 Checksum Receipt]：** 指定生成 [!DNL MD5] 校验和收据。[!DNL MD5] 校验和收据，以便合作伙伴能够确认Audience Manager正确处理完整转让。

1. (视情况而定)如果选择 **[!UICONTROL HTTP]**，请填写字段：

   * **[!UICONTROL Method]：** 选择要用于传输流程的 [!DNL API] 方法：
      * **[!UICONTROL POST]：** 如果选择 [!DNL POST]，请选择内容类型([!DNL XML] 或 [!DNL JSON])，然后指定请求正文。
      * **[!UICONTROL GET]：** 如果选择 [!DNL GET]，则指定查询参数。

1. 如果 **[!UICONTROL Create]** 要创建新格式，请单击，如果 **[!UICONTROL Save Updates]** 您正在编辑现有格式，则单击。

## 删除格式 {#delete-format}

1. 单击 **[!UICONTROL Formats]**.
2. 单击 ![](assets/icon_delete.png) 所需格式的 **[!UICONTROL Actions]** 列。
3. Click **[!UICONTROL OK]** to confirm the deletion.
