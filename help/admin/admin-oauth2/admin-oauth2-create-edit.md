---
description: 使用“OAuth2客户端”页可查看Audience Manager配置中的OAuth2客户端列表。 只要分配了相应的用户角色，就可以编辑或删除现有客户机或创建新客户机。
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2 客户端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# OAuth2 客户端 {#oauth-clients}

使用 [!UICONTROL OAuth2 Clients] 页面查看列表 [!UICONTROL OAuth2] 您的中的客户 [!DNL Audience Manager] 配置。 只要分配了相应的用户角色，就可以编辑或删除现有客户机或创建新客户机。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>确保您的客户阅读 [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 文档(位于《Audience Manager用户指南》中)。

[!DNL OAuth2] 是一个开放标准，用于授权提供对的安全委派访问 [!DNL Audience Manager] 代表资源所有者的资源。

![](assets/oauth.png)

您可以通过单击所需列的标题，按升序或降序对每个列进行排序。

使用 [!UICONTROL Search] 框或列表底部的分页控件以查找所需的客户端。

## 创建或编辑OAuth2客户端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用 [!UICONTROL OAuth2 Clients] Audience Manager中的页面 [!UICONTROL Admin] 用于创建新工具的工具 [!UICONTROL Oauth2] 客户端或编辑现有客户端。

1. 新建 [!UICONTROL OAuth2] 客户端，单击 **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. 编辑现有 [!UICONTROL OAuth2] 客户端，在 **[!UICONTROL Client ID]** 列。
1. 为此指定所需的名称 [!UICONTROL OAuth2] 客户。 请注意，这是仅记录的名称。
1. 指定 [!UICONTROL OAuth2] 客户的电子邮件地址。 电子邮件地址数量有限。
1. 从 **[!UICONTROL Partner]** 从下拉列表中，选择所需的合作伙伴。
1. 在 **[!UICONTROL Client ID]** 框中，指定所需的ID。 这是提交时使用的值 [!DNL API] 请求。 选择后开始键入时会自动填充前缀 [!UICONTROL Partner] 从上一步骤的下拉列表中。 正确的格式为&lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. 选择或取消选择 **[!UICONTROL Restrict to Partner Users]** 复选框。 如果选中此复选框，则用户必须是 [!DNL Audience Manager] 为所选合作伙伴列出的用户。 作为最佳实践，我们建议您选择此选项。
1. 在 **[!UICONTROL Scope]** 部分，选择或取消选择 **[!UICONTROL Read]** 和 **[!UICONTROL Write]** 复选框。
1. 在 **[!UICONTROL Grant Type]** 部分，选择所需的授权方式。 我们建议您使用 [!UICONTROL Password] 和 [!UICONTROL Refresh-token] 选项。

   * **[!UICONTROL Implicit]**：如果选择此选项，则 [!UICONTROL Redirect URI] 框已启用。 用户经过身份验证后会获得自动访问令牌，并会立即发送到重定向 [!DNL URI].
   * **[!UICONTROL Authorization Code]**：如果选择此选项，则 [!UICONTROL Redirect URI] 框已启用。 用户经过身份验证后返回到客户端，然后发送到重定向 [!DNL URI].
   * **[!UICONTROL Password]**：用户使用用户输入的密码进行身份验证，而不是通过授权服务器进行自动验证尝试。
   * **[!UICONTROL Refresh_token]**：用于长时间刷新过期的访问令牌。

1. 在 **[!UICONTROL Redirect URI]** 框中，指定所需的 [!DNL URI]. 仅当您选择 **[!UICONTROL Implicit]** 和 **[!UICONTROL Authorization_code]** 授予类型。 此 **[!UICONTROL Redirect URI]** 框可让您指定可接受的逗号分隔值 [!DNL URI] 值。 这是 [!DNL URI] 在批准客户端之后，客户端的用户将被重定向到 [!DNL API] 访问权限。
1. 为访问和刷新令牌过期指定所需的过期时间（以秒为单位）。

   * **[!UICONTROL Access Token Expiration Time]**：颁发访问令牌后其有效的秒数。 可以为空以使用平台默认值（12小时）。 也可以为–1，表示访问令牌未过期。
   * **[!UICONTROL Refresh Token Expiration Time]**：刷新令牌发出后有效的秒数。 可以为空以使用平台默认值（30天）。

1. 单击 **[!UICONTROL Save]**.

删除 [!UICONTROL OAuth2] 客户端，单击 **[!UICONTROL OAuth2 Clients]**，然后单击  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 列。

>[!MORELIKETHIS]
>
>* [API 要求和建议](../admin-oauth2/aam-admin-api-requirements.md)

