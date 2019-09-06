---
description: 一些客户可能不想向Adobe提供Amazon Simple Storage Service(Amazon S3)访问或秘密密钥，以授权将目标数据上传至其buckets。
seo-description: 一些客户可能不想向Adobe提供Amazon Simple Storage Service(Amazon S3)访问或秘密密钥，以授权将目标数据上传至其buckets。
seo-title: 如何对跨帐户Amazon S Bucket Access进行批量目标授权
title: 如何对跨帐户Amazon S Bucket Access进行批量目标授权
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 如何对跨帐户Amazon S Bucket Access进行批量目标授权{#authorize-cross-account-bucket-batch}

某些客户可能不想向Adobe [!DNL Amazon S3] 提供访问目标数据的访问权或秘密密钥。

我们为客户提供的一种替代 [!UICONTROL Cross-Account Bucket Permissions][!DNL Amazon S3]方式。[AWS文档](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)中介绍了此过程。要在Audience Manager中启用此备选方案，请按照以下步骤操作：

1. 转到 **[!UICONTROL Servers]** 并选择 **[!UICONTROL Create Server]**。
1. 在 **[!UICONTROL S3]****[!UICONTROL Protocol/Credentials]** 下拉掩码中选择。
1. 选中 **[!UICONTROL Use Internal Adobe Key]** 此选项。
1. 使用客户的帐户和桶名称 [!DNL Amazon S3]。
1. 确保您的客户白名单在其 [!DNL Amazon S3]`975822914085`[!DNL S3] 桶上列出帐户。

>[!NOTE]
>
>我们的出站publisher可确保对上传的数据设置权限级别 `bucket-owner-full-control` ，以便您的客户拥有该数据。
