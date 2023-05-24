---
description: 使用“Audience Manager管理”工具中的“服务器”页可创建新的S3服务器或编辑现有服务器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new S3 server or to edit an existing server.
seo-title: Create or Edit an S3 Server
title: 创建或编辑 S3 服务器
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
exl-id: 89310de0-e24e-4d4b-8171-56faf0b441f6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# 创建或编辑 S3 服务器 {#create-or-edit-an-s-server}

使用 [!UICONTROL Servers] 页面以新建Audience Manager [!DNL S3] ，或者编辑现有服务器。

>[!NOTE]
>
>您必须拥有 [!UICONTROL DEXADMIN] 角色来创建新服务器或编辑现有服务器。

1. 要创建新服务器，请单击 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 要编辑现有服务器，请在 **[!UICONTROL Label]** 列。
1. 为此服务器指定所需的标签。
1. 从 **[!UICONTROL Protocol]** 下拉列表，选择所需的协议： **[!UICONTROL S3]**.

   >[!NOTE]
   >
   >我们建议使用 [!DNL Amazon S3] 作为一种从合作伙伴获取文件并将文件交付给合作伙伴的方法。 [!DNL Amazon S3] 提供了一个简单的web服务界面，可用于随时随地从web上的任何位置存储和检索任意数量的数据。 有关更多信息，请参阅 [关于Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 在 *Audience Manager用户指南*.

1. 填写以下字段：

   * **[!UICONTROL Account]：** 指定所需的 [!DNL S3] 帐户。
   * **[!UICONTROL Bucket]：** 指定所需的 [!DNL S3] 桶。
   * **[!UICONTROL Directory]：** 指定所需的 [!DNL S3] 目录。
   * **[!UICONTROL Access Key]：** 指定所需的 [!DNL S3] 访问密钥。
   * **[!UICONTROL Secret Key]：** 指定所需的 [!DNL S3] 密钥。

1. 单击 **[!UICONTROL Create]** 如果要创建新服务器，请单击 **[!UICONTROL Update]** 如果您正在编辑现有服务器。
