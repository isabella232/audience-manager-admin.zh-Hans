---
description: 某些客户可能不想向Adobe提供其Amazon Simple存储服务(Amazon S3)访问或密钥，以授权将目标数据上传到其存储段。
seo-description: 某些客户可能不想向Adobe提供其Amazon Simple存储服务(Amazon S3)访问或密钥，以授权将目标数据上传到其存储段。
seo-title: 如何授权批处理目标的跨帐户Amazon S3存储段访问
title: 如何授权批处理目标的跨帐户Amazon S3存储段访问
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

某些客户可能不希望向Adobe提 [!DNL Amazon S3] 供访问或密钥，以授权将目标数据上传到其存储段。

我们可以优惠客户的另一种方 [!UICONTROL Cross-Account Bucket Permissions] 法 [!DNL Amazon S3]是。 AWS文档中对此过 [程进行了说明](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)。 要在Audience Manager中启用此备选项，请执行以下步骤：

1. 转到并 **[!UICONTROL Servers]** 选择 **[!UICONTROL Create Server]**。
1. 在 **[!UICONTROL S3]** 下拉 **[!UICONTROL Protocol/Credentials]** 蒙版中选择。
1. 选中该 **[!UICONTROL Use Internal Adobe Key]** 选项。
1. 在中使用客户的帐户和存储段名称 [!DNL Amazon S3]。
1. 确保客户白色列表客户桶 [!DNL Amazon S3] 上 `975822914085` 的帐 [!DNL S3] 户。

>[!NOTE]
>
>我们的出站发布者确保对已上 `bucket-owner-full-control` 传的数据设置权限级别，以便您的客户可以拥有该数据。
