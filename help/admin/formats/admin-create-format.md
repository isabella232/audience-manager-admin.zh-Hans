---
description: 使用Audience Manager管理工具中的“格式”页可创建新格式或编辑现有格式。
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: 创建或编辑格式
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# 创建或编辑格式 {#create-or-edit-a-format}

使用 [!UICONTROL Formats] 页面，以创建新格式或编辑现有Audience Manager。

<!-- t_create_format.xml -->

>[!TIP]
>
>在为出站数据选择格式时，如果可能，最好重复使用现有格式。 使用已验证的格式可确保成功生成出站数据。 要准确地查看现有格式的格式，请单击 [!UICONTROL Formats] 选项，并按名称或ID号搜索您的格式。 格式中使用的格式不正确或宏将提供格式不正确的输出或阻止完全输出信息。

1. 要创建新格式，请单击 **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. 要编辑现有格式，请在 **[!UICONTROL Name]** 列。

   ![](assets/create_format.png)

1. 填写以下字段：
   * **名称：** （必需）为格式提供描述性名称。
   * **类型：** （必需）选择所需的格式：
      * **[!UICONTROL File]**：通过发送数据 [!DNL FTP] 文件。
      * **[!UICONTROL HTTP]**：将数据封装在 [!DNL JSON] 包装纸。

1. （视情况而定）如果您选择 **[!UICONTROL File]**，填写以下字段：

   >[!NOTE]
   >
   >有关可用宏的列表，请参见 [文件格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 和 [HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]：** 指定数据传输文件的文件名。
   * **标头：** 指定在数据传输文件第一行中显示的文本。
   * **[!UICONTROL Data Row]：** 指定在文件的每个出站行中显示的文本。
   * **[!UICONTROL Maximum File Size (In MB)]：** 指定数据传输文件的最大文件大小。 压缩文件必须小于100 MB。 未压缩文件大小没有限制。
   * **[!UICONTROL Compression]：** 为数据文件选择所需的压缩类型：gz或zip。 用于投放到 [!UICONTROL AWS S3]中，您必须使用.gz或未压缩的文件。
   * **[!UICONTROL .info Receipt]：** 指定传输控制([!DNL .info])文件生成。 此 [!DNL .info] file提供了有关文件传输的元数据信息，以便合作伙伴能够验证Audience Manager是否正确处理了文件传输。 有关更多信息，请参阅 [用于日志文件传输的传输控制文件](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]：** 指定 [!DNL MD5] 生成校验和回执。 此 [!DNL MD5] 校验和接收，以便合作伙伴能够验证Audience Manager是否正确处理了完全传输。

1. （视情况而定）如果您选择 **[!UICONTROL HTTP]**，填写以下字段：

   * **[!UICONTROL Method]：** 选择 [!DNL API] 要用于传输过程的方法：
      * **[!UICONTROL POST]：** 如果您选择 [!DNL POST]，选择内容类型([!DNL XML] 或 [!DNL JSON])，然后指定请求正文。
      * **[!UICONTROL GET]：** 如果您选择 [!DNL GET]，指定查询参数。

1. 单击 **[!UICONTROL Create]** 如果要创建新格式，请单击 **[!UICONTROL Save Updates]** 如果您正在编辑现有格式。

## 删除格式 {#delete-format}

1. 单击 **[!UICONTROL Formats]**.
2. 单击  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 列指定所需的格式。
3. 单击 **[!UICONTROL OK]** 以确认删除。
