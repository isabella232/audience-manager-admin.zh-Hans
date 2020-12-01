---
description: 使用“OAuth2客户端”页可在视图配置中Audience ManagerOAuth2客户端的列表。 您可以编辑或删除现有客户端或创建新客户端，前提是您已分配了相应的用户角色。
seo-description: 使用“OAuth2客户端”页可在视图配置中Audience ManagerOAuth2客户端的列表。 您可以编辑或删除现有客户端或创建新客户端，前提是您已分配了相应的用户角色。
seo-title: OAuth2 客户端
title: OAuth2 客户端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# OAuth2 客户端 {#oauth-clients}

使用[!UICONTROL OAuth2 Clients]页可视图[!DNL Audience Manager]配置中[!UICONTROL OAuth2]客户机的列表。 您可以编辑或删除现有客户端或创建新客户端，前提是您已分配了相应的用户角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>确保您的客户阅读《Audience Manager用户指南》中的[OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth)文档。

[!DNL OAuth2] 是一个开放的授权标准，用于代表资源所有者 [!DNL Audience Manager] 提供对资源的安全委托访问。

![](assets/oauth.png)

单击所需列的标题，可以按升序或降序对每列进行排序。

使用[!UICONTROL Search]框或列表底部的分页控件找到所需的客户端。

## 创建或编辑OAuth2客户端{#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL OAuth2 Clients]页面创建新的[!UICONTROL Oauth2]客户端或编辑现有客户端。

1. 要创建新的[!UICONTROL OAuth2]客户端，请单击&#x200B;**[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**。 要编辑现有的[!UICONTROL OAuth2]客户端，请在&#x200B;**[!UICONTROL Client ID]**&#x200B;列中单击所需的客户端。
1. 为此[!UICONTROL OAuth2]客户端指定所需的名称。 请注意，这是仅记录的名称。
1. 指定[!UICONTROL OAuth2]客户端的电子邮件地址。 电子邮件地址限制为一个。
1. 从&#x200B;**[!UICONTROL Partner]**&#x200B;下拉列表中，选择所需的合作伙伴。
1. 在&#x200B;**[!UICONTROL Client ID]**&#x200B;框中，指定所需的ID。 这是提交[!DNL API]请求时使用的值。 在您从上一步的下拉开始中选择[!UICONTROL Partner]后，列表键入时，前缀会自动填充。 正确的格式为&lt;*`partner subdomain`*> - &lt;*`Audience Manager username`*>。
1. 根据需要选择或取消选中&#x200B;**[!UICONTROL Restrict to Partner Users]**&#x200B;复选框。 如果选中此复选框，则用户必须是所选合作伙伴的[!DNL Audience Manager]用户。 作为最佳实践，我们建议您选择此选项。
1. 在&#x200B;**[!UICONTROL Scope]**&#x200B;部分，根据需要选择或取消选择&#x200B;**[!UICONTROL Read]**&#x200B;和&#x200B;**[!UICONTROL Write]**&#x200B;复选框。
1. 在&#x200B;**[!UICONTROL Grant Type]**&#x200B;部分，选择所需的授权方式。 我们建议您使用[!UICONTROL Password]和[!UICONTROL Refresh-token]选项的默认设置。

   * **[!UICONTROL Implicit]**:如果选择此选项，则 [!UICONTROL Redirect URI] 将启用框。通过身份验证后，用户将获得自动访问令牌，并立即发送到重定向[!DNL URI]。
   * **[!UICONTROL Authorization Code]**:如果选择此选项，则 [!UICONTROL Redirect URI] 将启用框。通过身份验证后，用户将返回到客户端，然后发送到重定向[!DNL URI]。
   * **[!UICONTROL Password]**:使用用户输入的口令而不是通过授权服务器进行自动式校验尝试来验证用户。
   * **[!UICONTROL Refresh_token]**:用于刷新已过期访问令牌的较长时间。

1. 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;框中，指定所需的[!DNL URI]。 仅当您选择&#x200B;**[!UICONTROL Implicit]**&#x200B;和&#x200B;**[!UICONTROL Authorization_code]**&#x200B;授权类型时，才启用此选项。 在&#x200B;**[!UICONTROL Redirect URI]**&#x200B;框中，可以指定可接受值[!DNL URI]的以逗号分隔的值。 这是在批准客户端访问[!DNL API]后，将客户端的[!DNL URI]用户重定向到的。
1. 指定访问和刷新令牌到期所需的到期时间（以秒为单位）。

   * **[!UICONTROL Access Token Expiration Time]**:发出访问令牌后有效的秒数。使用平台默认值（12小时）可为null。 也可以是-1，表示访问令牌未过期。
   * **[!UICONTROL Refresh Token Expiration Time]**:发出刷新令牌后有效的秒数。使用平台默认值（30天）可为null。

1. 单击 **[!UICONTROL Save]**.

要删除[!UICONTROL OAuth2]客户端，请单击&#x200B;**[!UICONTROL OAuth2 Clients]**，然后单击所需客户端的&#x200B;**[!UICONTROL Actions]**&#x200B;列中的![](assets/icon_delete.png)。

>[!MORELIKETHIS]
>
>* [API 要求和建议](../admin-oauth2/aam-admin-api-requirements.md)

