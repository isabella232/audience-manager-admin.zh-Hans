---
description: 某些客户可能不想提供其Amazon Simple Storage Service (Amazon S3)访问或密钥以Adobe授权将目标数据上传到他们的存储桶。
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 如何授权跨帐户Amazon S3存储段访问以实现批处理目标
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 如何授权跨帐户Amazon S3存储段访问以实现批处理目标{#authorize-cross-account-bucket-batch}

某些客户可能不想提供其 [!DNL Amazon S3] Adobe的访问密钥或机密密钥，用于授权将目标数据上传到其存储桶。

我们可以为客户提供的替代方案是 [!UICONTROL Cross-Account Bucket Permissions] 在 [!DNL Amazon S3]. 此过程的说明请参见 [AWS文档](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). 要在Audience Manager中启用此替代方法，请执行以下步骤：

1. 转到 **[!UICONTROL Servers]** 并选择 **[!UICONTROL Create Server]**.
1. 选择 **[!UICONTROL S3]** 在 **[!UICONTROL Protocol/Credentials]** 下拉蒙版。
1. 查看 **[!UICONTROL Use Internal Adobe Key]** 选项。
1. 在中使用客户的帐户和分段名称 [!DNL Amazon S3].
1. 确保您的客户白名单中列出了 [!DNL Amazon S3] 帐户 `975822914085` 关于 [!DNL S3] 桶。

>[!NOTE]
>
>我们的出站发布者可确保权限级别 `bucket-owner-full-control` 对上传的数据进行了设置，以便您的客户可以拥有该数据。
