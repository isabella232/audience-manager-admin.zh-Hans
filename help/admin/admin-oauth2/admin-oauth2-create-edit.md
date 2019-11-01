---
description: 使用“OAuth2客户端”页可以在Audience manager配置中查看OAuth2客户端列表。 您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。
seo-description: 使用“OAuth2客户端”页可以在Audience manager配置中查看OAuth2客户端列表。 您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。
seo-title: OAuth2客户端
title: OAuth2客户端
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaa
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92

---


# OAuth2客户端 {#oauth-clients}

使用该页 [!UICONTROL OAuth2 Clients] 面可查看配置中的 [!UICONTROL OAuth2] 客户端列 [!DNL Audience Manager] 表。 您可以编辑或删除现有客户端或创建新客户端，前提是您分配了相应的用户角色。

## 概述 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>确保您的客户阅读《 [[!DNL Audience Manager用户指南](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 》中的OAuth2文档。

[!DNL OAuth2] 是一个开放的授权标准，用于代表资源所有者提供对 [!DNL Audience Manager] 资源的安全授权访问。

![](assets/oauth.png)

您可以通过单击所需列的标题，按升序或降序对每列进行排序。

使用列 [!UICONTROL Search] 表底部的框或分页控件查找所需的客户端。

## 创建或编辑OAuth2客户端 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

使用Audience Manager [!UICONTROL OAuth2 Clients] 工具中的页面 [!UICONTROL Admin] 创建新客户端或编 [!UICONTROL Oauth2] 辑现有客户端。

1. 要创建新客户 [!UICONTROL OAuth2] 端，请单击 **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**。 要编辑现有客 [!UICONTROL OAuth2] 户端，请在列中单击所需的客 **[!UICONTROL Client ID]** 户端。
1. 为此客户端指定所需的 [!UICONTROL OAuth2] 名称。 请注意，这仅是记录的名称。
1. 指定客 [!UICONTROL OAuth2] 户端的电子邮件地址。 电子邮件地址的限制为一个。
1. 从下 **[!UICONTROL Partner]** 拉列表中，选择所需的合作伙伴。
1. 在框 **[!UICONTROL Client ID]** 中，指定所需的ID。 这是提交请求时使用的 [!DNL API] 值。 从上一步的下拉列表中选择一个后，开始键 [!UICONTROL Partner] 入时，前缀会自动填充。 正确的格式为&lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt;。
1. 根据需要选 **[!UICONTROL Restrict to Partner Users]** 中或取消选中复选框。 如果选中此复选框，则用户必须是选定 [!DNL Audience Manager] 合作伙伴的列出用户。 作为最佳实践，我们建议您选择此选项。
1. 在部分 **[!UICONTROL Scope]** 中，根据需要选择或取消选 **[!UICONTROL Read]** 中 **[!UICONTROL Write]** 相应的和复选框。
1. 在部分 **[!UICONTROL Grant Type]** 中，选择所需的授权方式。 我们建议您使用默认设置和 [!UICONTROL Password] 选项 [!UICONTROL Refresh-token] 。

   * **[!UICONTROL Implicit]**:如果选择此选项，则 [!UICONTROL Redirect URI] 将启用该框。 用户在经过身份验证后将获得一个自动访问令牌，并立即被发送到重定向 [!DNL URI]。
   * **[!UICONTROL Authorization Code]**:如果选择此选项，则 [!UICONTROL Redirect URI] 将启用该框。 用户在经过身份验证后返回到客户端，然后被发送到重定向 [!DNL URI]。
   * **[!UICONTROL Password]**:使用用户输入的口令而不是通过授权服务器自动验证尝试来验证用户。
   * **[!UICONTROL Refresh_token]**:用于刷新已过期的访问令牌一段时间。

1. 在框 **[!UICONTROL Redirect URI]** 中，指定所需的 [!DNL URI]。 仅当您选择类型并授予类型时，才 **[!UICONTROL Implicit]** 启用 **[!UICONTROL Authorization_code]** 此选项。 该 **[!UICONTROL Redirect URI]** 框允许您指定可接受值的逗号分隔 [!DNL URI] 值。 这是在批准 [!DNL URI] 客户端进行访问后，将客户端的用户重定向到的 [!DNL API] 用户。
1. 指定访问和刷新令牌过期所需的过期时间（以秒为单位）。

   * **[!UICONTROL Access Token Expiration Time]**:发出访问令牌后有效的秒数。 使用平台默认值（12小时）可为null。 也可以是-1以指示访问令牌不过期。
   * **[!UICONTROL Refresh Token Expiration Time]**:发出刷新令牌后有效的秒数。 使用平台默认值（30天）时可为null。

1. 单击 **[!UICONTROL Save]**.

要删除客 [!UICONTROL OAuth2] 户端，请单 **[!UICONTROL OAuth2 Clients]**&#x200B;击，然后单击 ![](assets/icon_delete.png) 所需客 **[!UICONTROL Actions]** 户端的列。

>[!MORELIKETHIS]
>
>* [API要求和建议](../admin-oauth2/aam-admin-api-requirements.md)

