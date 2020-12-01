---
description: 一些客户可能不想提供其Amazon简单存储服务(AmazonS3)访问或密钥，以便Adobe授权将目标数据上传到其存储段。
seo-description: 一些客户可能不想提供其Amazon简单存储服务(AmazonS3)访问或密钥，以便Adobe授权将目标数据上传到其存储段。
seo-title: 如何授权批目标的跨帐户AmazonS3存储段访问
title: 如何授权批目标的跨帐户AmazonS3存储段访问
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# 如何授权批目标的跨帐户AmazonS3存储段访问{#authorize-cross-account-bucket-batch}

某些客户可能不想提供其[!DNL Amazon S3]访问或密钥，以便Adobe授权将目标数据上传到其存储段。

我们可以优惠客户的替代方法是[!DNL Amazon S3]中的[!UICONTROL Cross-Account Bucket Permissions]。 此过程在[AWS文档](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)中有介绍。 要在Audience Manager中启用此备选项，请执行以下步骤：

1. 转至&#x200B;**[!UICONTROL Servers]**&#x200B;并选择&#x200B;**[!UICONTROL Create Server]**。
1. 在&#x200B;**[!UICONTROL Protocol/Credentials]**&#x200B;下拉掩码中选择&#x200B;**[!UICONTROL S3]**。
1. 选中&#x200B;**[!UICONTROL Use Internal Adobe Key]**&#x200B;选项。
1. 在[!DNL Amazon S3]中使用客户的帐户和存储段名称。
1. 确保您的客户白名单在其[!DNL S3]存储桶中列出[!DNL Amazon S3]帐户`975822914085`。

>[!NOTE]
>
>我们的出站发布者确保已对已上载数据设置权限级别`bucket-owner-full-control`，以便您的客户可以拥有该数据。
