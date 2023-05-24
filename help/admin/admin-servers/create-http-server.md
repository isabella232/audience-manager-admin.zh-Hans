---
description: 使用“Audience Manager管理”工具中的“服务器”页可创建新的HTTP服务器或编辑现有服务器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: 创建或编辑 HTTP 服务器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 6%

---

# 创建或编辑 HTTP 服务器 {#create-or-edit-an-http-server}

使用 [!UICONTROL Servers] 页面，用于创建新的HTTP服务器或编辑现有Audience Manager。

>[!NOTE]
>
>您必须拥有 [!UICONTROL DEXADMIN] 角色来创建新服务器或编辑现有服务器。

1. 要创建新服务器，请转到 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 要编辑现有服务器，请在 **[!UICONTROL Label]** 列。
1. 为此服务器指定所需的标签。
1. 从 **[!UICONTROL Protocol]** 下拉列表，选择所需的协议： [!DNL HTTP].
1. 填写以下字段：

   * **[!UICONTROL Domain]：** 为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]：** 为此服务器指定所需的端口。 将为每种加密类型显示默认端口。 您可以根据需要更改默认端口
   * **[!UICONTROL Maximum Users Per Request]：** 指定此服务器允许的每个请求的最大用户数。
   * **[!UICONTROL URL Prefix]：** 指定 [!DNL URL] 用于此服务器的前缀。
   * **[!UICONTROL Authentication URL]：** 指定 [!UICONTROL Authentication URL] 对于此 `HTTP` 服务器。
   * **[!UICONTROL Authentication]：** 指定所需的身份验证方法： **[!UICONTROL None]**， **[!UICONTROL Username/Password]**，或 **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]：** 的名称 [!DNL HTTP] 标头，由客户提供，其中包含 [!DNL HTTP] 签名密钥。 默认值为 [!UICONTROL X-Signature]，如以下示例所示：

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]：** 用于签署 [!DNL HTTP] 请求，由客户提供。
   * **[!UICONTROL Show Signature Key]：** 切换是否在浏览器中显示签名。
   * **[!UICONTROL HTTP Signature Encryption Method]：** 指定我们用于加密签名的方法。 使用 [!UICONTROL SHA1] 除非客户另有选择。

   >[!NOTE]
   >
   >如果要启用 [用于实时数据传输的OAuth 2.0身份验证](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) 对于合作伙伴，请填写下表中的字段。 中的字段 *斜体* 需要完全按照表中的方式填写。

   | 名称 | 值 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *授权*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 单击 **[!UICONTROL Create]** 如果要创建新服务器，请单击 **[!UICONTROL Update]** 如果您正在编辑现有服务器。
