---
description: 使用Audience Manager管理工具中的“格式”页面创建新格式或编辑现有格式。
seo-description: 使用Audience Manager管理工具中的“格式”页面创建新格式或编辑现有格式。
seo-title: 创建或编辑格式
title: 创建或编辑格式
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 4%

---


# 创建或编辑格式{#create-or-edit-a-format}

使用 [!UICONTROL Formats] Audience Manager管理工具中的页面创建新格式或编辑现有格式。

<!-- t_create_format.xml -->

>[!TIP]
>
>在为您的无界数据选择格式时，最好（如果可能）重新使用现有格式。 使用已经过验证的格式，可确保成功生成您的出站数据。 要确切了解现有格式的格式，请单击 [!UICONTROL Formats] 菜单栏中的选项，然后按名称或ID编号搜索格式。 格式中使用的格式不正确或宏将提供格式不正确的输出，或将阻止完全输出信息。

1. 要创建新格式，请单击 **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**。 要编辑现有格式，请单击列中所需的 **[!UICONTROL Name]** 格式。

   ![](assets/create_format.png)

1. 填写以下字段：
   * **名称：** （必需）为格式提供描述性名称。
   * **类型：** （必需）选择所需格式：
      * **[!UICONTROL File]**: 通过文件发 [!DNL FTP] 送数据。
      * **[!UICONTROL HTTP]**: 将数据封入包装 [!DNL JSON] 器中。

1. （视情况而定）如果 **[!UICONTROL File]**&#x200B;您选择，请填写以下字段：

   >[!NOTE]
   >
   >有关可用宏的列表，请参 [阅文件格式宏](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089)[和HTTP格式宏](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)。

   * **[!UICONTROL File Name]:**指定数据传输文件的文件名。
   * **标题：** 指定在数据传输文件的第一行中显示的文本。
   * **[!UICONTROL Data Row]:**指定在文件的每个外界行中显示的文本。
   * **[!UICONTROL Maximum File Size (In MB)]:**指定数据传输文件的最大文件大小。 压缩文件必须小于100 MB。 未压缩文件大小没有限制。
   * **[!UICONTROL Compression]:**选择所需的压缩类型： gz或zip。 要投放,[!UICONTROL AWS S3]必须使用。gz或未压缩文件。
   * **[!UICONTROL .info Receipt]:**指定生成转移控制([!DNL .info])文件。 该文[!DNL .info]件提供有关文件传输的元数据信息，以便合作伙伴可以验证Audience Manager处理的文件传输是否正确。 有关详细信息，请[参阅日志文件传输的传输控制文件](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html)。
   * **[!UICONTROL MD5 Checksum Receipt]:**指定生成[!DNL MD5]校验和接收。 校验[!DNL MD5]和接收，以便合作伙伴可以验证Audience Manager是否正确处理了完全传输。

1. （视情况而定）如果 **[!UICONTROL HTTP]**&#x200B;您选择，请填写以下字段：

   * **[!UICONTROL Method]:**选择[!DNL API]要用于传送流程的方法：
      * **[!UICONTROL POST]:**如果您选[!DNL POST]择，请选择内容类型([!DNL XML]或[!DNL JSON])，然后指定请求正文。
      * **[!UICONTROL GET]:**如果您选[!DNL GET]择，请指定查询参数。

1. 如 **[!UICONTROL Create]** 果要创建新格式，请单击，如 **[!UICONTROL Save Updates]** 果要编辑现有格式，则单击。

## 删除格式 {#delete-format}

1. 单击 **[!UICONTROL Formats]**.
2. 单击 ![](assets/icon_delete.png) 所需 **[!UICONTROL Actions]** 格式的列中。
3. Click **[!UICONTROL OK]** to confirm the deletion.
