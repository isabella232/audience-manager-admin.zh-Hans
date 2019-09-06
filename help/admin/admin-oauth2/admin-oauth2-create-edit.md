---
description: 使用OAuth客户端页面在Audience Manager配置中查看OAuth客户端列表。您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。
seo-description: 使用OAuth客户端页面在Audience Manager配置中查看OAuth客户端列表。您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。
seo-title: OAuth客户端
title: OAuth客户端
uuid: 3e654053-fb2 f-4d8 f-a53 c-b5 c3 b8 ddaaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# OAuth客户端 {#oauth-clients}

使用 [!UICONTROL OAuth2 Clients] 页面查看配置中 [!UICONTROL OAuth2] 的客户端 [!DNL Audience Manager] 列表。您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>确保您的客户 [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 阅读[！DNL Audience Manager用户指南。

[!DNL OAuth2] 是一个开放标准，用于代表资源所有者提供安全委托访问 [!DNL Audience Manager] 资源。

![](assets/oauth.png)

您可以单击所需列的标题，以升序或降序排列每个列。

使用 [!UICONTROL Search] 列表底部的分页控件或分页控件查找所需的客户端。

## 创建或编辑OAuth客户端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience [!UICONTROL OAuth2 Clients] Manager [!UICONTROL Admin] 工具中的页面创建新 [!UICONTROL Oauth2] 客户端或编辑现有客户端。

1. 要创建新 [!UICONTROL OAuth2] 客户端，请单击 **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**。要编辑现有 [!UICONTROL OAuth2] 客户端，请在 **[!UICONTROL Client ID]** 列中单击所需的客户端。
1. 指定此 [!UICONTROL OAuth2] 客户端所需的名称。请注意，这只是记录的名称。
1. 指定 [!UICONTROL OAuth2] 客户端的电子邮件地址。只有一个电子邮件地址限制。
1. 从 **[!UICONTROL Partner]** 下拉列表中，选择所需的合作伙伴。
1. **[!UICONTROL Client ID]** 在框中，指定所需的ID。这是提交 [!DNL API] 请求时使用的值。从上一步中的下拉列表中选择一个 [!UICONTROL Partner] 下拉列表后，前缀会自动填充。正确的格式为&lt; *`partner subdomain`*&gt;-&lt; *`Audience Manager username`*&gt;。
1. 根据需要选中或取消选中复选 **[!UICONTROL Restrict to Partner Users]** 框。如果选中此复选框，则用户必须为选定合作伙伴列出的 [!DNL Audience Manager] 用户。作为最佳实践，建议您选择此选项。
1. 在 **[!UICONTROL Scope]** 部分中，根据需要选择或 **[!UICONTROL Read]****[!UICONTROL Write]** 取消选择复选框。
1. 在 **[!UICONTROL Grant Type]** 部分中，选择所需的授权方式。建议您使用默认设置 [!UICONTROL Password] 和 [!UICONTROL Refresh-token] 选项。

   * **[!UICONTROL Implicit]**：如果选择此选项，则启用 [!UICONTROL Redirect URI] 该框。经过验证后，用户获得了自动访问令牌，并立即发送到重定向 [!DNL URI]。
   * **[!UICONTROL Authorization Code]**：如果选择此选项，则启用 [!UICONTROL Redirect URI] 该框。用户在经过身份验证后返回到客户端，然后发送到重定向 [!DNL URI]。
   * **[!UICONTROL Password]**：用户使用用户输入的密码进行身份验证，而不是通过授权服务器进行自动验证尝试。
   * **[!UICONTROL Refresh_token]**：用于刷新长期到期的访问令牌。

1. 在 **[!UICONTROL Redirect URI]** 框中，指定所需 [!DNL URI]的。仅当您选择 **[!UICONTROL Implicit]** 和 **[!UICONTROL Authorization_code]** 授予类型时，才启用此选项。该 **[!UICONTROL Redirect URI]** 框允许您指定以逗号分隔的 [!DNL URI] 值值。这是批准 [!DNL URI] 客户端以 [!DNL API] 供访问后重定向到客户端的客户端。
1. 指定用于访问和刷新令牌过期的所需的过期时间(以秒为单位)。

   * **[!UICONTROL Access Token Expiration Time]**：访问令牌在发布后有效的秒数。可为null，使用平台默认值(12小时)。也可以为-1，表示访问令牌未过期。
   * **[!UICONTROL Refresh Token Expiration Time]**：刷新令牌在发布后有效的秒数。使用平台默认值(30天)时可为null。

1. 单击 **[!UICONTROL Save]**.

要删除 [!UICONTROL OAuth2] 客户端，请单击 **[!UICONTROL OAuth2 Clients]**，然后单击 ![](assets/icon_delete.png) 所需客户端的 **[!UICONTROL Actions]** 列。

>[!MORE_ LIKE_ This]
>
>* [API要求和推荐](../admin-oauth2/aam-admin-api-requirements.md)

