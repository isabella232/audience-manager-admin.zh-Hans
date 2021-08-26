---
description: 使用“Audience Manager管理工具”中的“格式”页面创建新格式或编辑现有格式。
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

使用“Audience Manager管理工具”中的[!UICONTROL Formats]页面创建新格式或编辑现有格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>在为出站数据选择格式时，最好（如果可能）重新使用现有格式。 使用已验证的格式可确保成功生成出站数据。 要确切了解现有格式的格式，请单击菜单栏中的[!UICONTROL Formats]选项，然后按名称或ID号搜索格式。 格式中使用的格式不正确或宏将提供格式不正确的输出，或将阻止完全输出信息。

1. 要创建新格式，请单击&#x200B;**[!UICONTROL Formats]** > **[!UICONTROL Add Format]**。 要编辑现有格式，请在&#x200B;**[!UICONTROL Name]**&#x200B;列中单击所需的格式。

   ![](assets/create_format.png)

1. 填写以下字段：
   * **名称：** （必需）为格式提供一个描述性名称。
   * **类型：** （必需）选择所需的格式：
      * **[!UICONTROL File]**:通过文件发送 [!DNL FTP] 数据。
      * **[!UICONTROL HTTP]**:将数据封装在包装 [!DNL JSON] 器中。

1. （视情况而定）如果您选择&#x200B;**[!UICONTROL File]**，请填写以下字段：

   >[!NOTE]
   >
   >有关可用宏的列表，请参阅[文件格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089)和[HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)。

   * **[!UICONTROL File Name]:** 指定数据传输文件的文件名。
   * **标题：** 指定在数据传输文件的第一行中显示的文本。
   * **[!UICONTROL Data Row]:** 指定文件中每个外界行中显示的文本。
   * **[!UICONTROL Maximum File Size (In MB)]:** 指定数据传输文件的最大文件大小。压缩文件必须小于100 MB。 未压缩文件大小没有限制。
   * **[!UICONTROL Compression]:** 选择所需的压缩类型：gz或zip。要传送到[!UICONTROL AWS S3]，必须使用.gz或未压缩文件。
   * **[!UICONTROL .info Receipt]:** 指定生成传输控制([!DNL .info])文件。[!DNL .info]文件提供有关文件传输的元数据信息，以便合作伙伴能够验证Audience Manager是否正确处理了文件传输。 有关更多信息，请参阅[用于日志文件传输的传输控制文件](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en)。
   * **[!UICONTROL MD5 Checksum Receipt]:** 指定生成 [!DNL MD5] 校验和接收。[!DNL MD5]校验和接收，以便合作伙伴能够验证Audience Manager是否正确处理了完整传输。

1. （视情况而定）如果您选择&#x200B;**[!UICONTROL HTTP]**，请填写以下字段：

   * **[!UICONTROL Method]:** 选择 [!DNL API] 要用于传输流程的方法：
      * **[!UICONTROL POST]:** 如果选择 [!DNL POST]，请选择内容类型([!DNL XML] 或 [!DNL JSON])，然后指定请求正文。
      * **[!UICONTROL GET]:** 如果选择 [!DNL GET]，请指定查询参数。

1. 如果要创建新格式，请单击&#x200B;**[!UICONTROL Create]**；如果要编辑现有格式，则单击&#x200B;**[!UICONTROL Save Updates]**。

## 删除格式 {#delete-format}

1. 单击 **[!UICONTROL Formats]**.
2. 在所需格式的&#x200B;**[!UICONTROL Actions]**&#x200B;列中单击![](assets/icon_delete.png)。
3. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以确认删除。
