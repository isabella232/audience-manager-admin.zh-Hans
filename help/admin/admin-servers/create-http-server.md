---
description: 使用“Audience Manager管理工具”中的“服务器”页面创建新的HTTP服务器或编辑现有服务器。
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

使用Audience Manager管理工具中的[!UICONTROL Servers]页面创建新的HTTP服务器或编辑现有服务器。

>[!NOTE]
>
>要创建新服务器或编辑现有服务器，您必须具有[!UICONTROL DEXADMIN]角色。

1. 要创建新服务器，请转到&#x200B;**[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要编辑现有服务器，请在&#x200B;**[!UICONTROL Label]**&#x200B;列中单击所需的服务器。
1. 为此服务器指定所需的标签。
1. 从&#x200B;**[!UICONTROL Protocol]**&#x200B;下拉列表中，选择所需的协议：[!DNL HTTP]。
1. 填写以下字段：

   * **[!UICONTROL Domain]:** 为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]:** 为此服务器指定所需的端口。每种加密类型均显示默认端口。 如有必要，您可以更改默认端口
   * **[!UICONTROL Maximum Users Per Request]:** 指定此服务器允许的每个请求的最大用户数。
   * **[!UICONTROL URL Prefix]:** 指定 [!DNL URL] 此服务器的前缀。
   * **[!UICONTROL Authentication URL]:** 指定此 [!UICONTROL Authentication URL] 服务器 `HTTP` 的。
   * **[!UICONTROL Authentication]:** 指定所需的身份验证方法： **[!UICONTROL None]**、  **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:** 由客户提 [!DNL HTTP] 供的包含签名键的标 [!DNL HTTP] 头名称。默认值为[!UICONTROL X-Signature]，如以下示例所示：

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

   * **[!UICONTROL HTTP Signature Key]:** 客户提供的用于 [!DNL HTTP] 对请求进行签名的键。
   * **[!UICONTROL Show Signature Key]:** 切换是否在浏览器中显示签名。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 指定加密签名的方法。除非客户另有选择，否则请使用[!UICONTROL SHA1]。

   >[!NOTE]
   >
   >如果要为合作伙伴的实时数据传输启用[OAuth 2.0身份验证](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en)，请按照下表中的字段填写。 *斜体*&#x200B;中的字段需要完全按照表中的方式填写。

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

1. 如果要创建新服务器，请单击&#x200B;**[!UICONTROL Create]**；如果要编辑现有服务器，则单击&#x200B;**[!UICONTROL Update]**。
