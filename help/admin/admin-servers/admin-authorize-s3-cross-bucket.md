---
description: 某些客户可能不希望向Adobe提供其Amazon Simple Storage Service(Amazon S3)访问或密钥，以授权将目标数据上传到其存储段。
seo-description: 某些客户可能不希望向Adobe提供其Amazon Simple Storage Service(Amazon S3)访问或密钥，以授权将目标数据上传到其存储段。
seo-title: 如何授权批处理目标的跨帐户Amazon S3存储段访问
title: 如何授权批处理目标的跨帐户Amazon S3存储段访问
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 如何授权批处理目标的跨帐户Amazon S3存储段访问{#authorize-cross-account-bucket-batch}

某些客户可能不希望向Adobe提 [!DNL Amazon S3] 供访问或密钥，以授权将目标数据上传到其存储段。

我们可以为客户提供的另一种选择 [!UICONTROL Cross-Account Bucket Permissions] 是 [!DNL Amazon S3]。 AWS文档中对此过 [程进行了说明](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)。 要在Audience manager中启用此备选项，请执行以下步骤：

1. 转到并 **[!UICONTROL Servers]** 选择 **[!UICONTROL Create Server]**。
1. 在下 **[!UICONTROL S3]** 拉蒙 **[!UICONTROL Protocol/Credentials]** 版中进行选择。
1. 选中该 **[!UICONTROL Use Internal Adobe Key]** 选项。
1. 请在中使用客户的帐户和存储段名称 [!DNL Amazon S3]。
1. 确保您的客户白名单列出客户 [!DNL Amazon S3] 桶中 `975822914085` 的帐 [!DNL S3] 户。

>[!NOTE]
>
>我们的出站发布者确保已上 `bucket-owner-full-control` 传数据的权限级别已设置，以便您的客户拥有该数据。
