---
description: 使用Audience Manager管理工具中的“服务器”页可创建新的HTTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理工具中的“服务器”页可创建新的HTTP服务器或编辑现有服务器。
seo-title: ' 创建或编辑HTTP服务器'
title: ' 创建或编辑HTTP服务器'
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 创建或编辑HTTP服务器 {#create-or-edit-an-http-server}

使用Audience [!UICONTROL Servers] Manager管理工具中的页面创建新的HTTP服务器或编辑现有服务器。

>[!NOTE]
>
>要创建新服务 [!UICONTROL DEXADMIN] 器或编辑现有服务器，您必须具有该角色。

1. 要创建新服务器，请转到 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。 要编辑现有服务器，请在列中单击所需的服 **[!UICONTROL Label]** 务器。
1. 为此服务器指定所需的标签。
1. 从下 **[!UICONTROL Protocol]** 拉列表中，选择所需的协议： [!DNL HTTP].
1. 填写以下字段：

   * **[!UICONTROL Domain]** :为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]** :为此服务器指定所需的端口。 将显示每个加密类型的默认端口。 如有必要，可以更改默认端口
   * **[!UICONTROL Maximum Users Per Request]** :指定此服务器允许的每个请求的最大用户数。
   * **[!UICONTROL URL Prefix]** :指定用 [!DNL URL] 于此服务器的前缀。
   * **[!UICONTROL Authentication URL]** :指定此服 [!UICONTROL Authentication URL] 务器的 `HTTP` 名称。
   * **[!UICONTROL Authentication]** :指定所需的身份验证方法： **[!UICONTROL None]**、 **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]** :包含签名密 [!DNL HTTP] 钥的标题的名称，由客户 [!DNL HTTP] 提供。 默认值 [!UICONTROL X-Signature]为，如下例所示：

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

   * **[!UICONTROL HTTP Signature Key]** :客户提供的用于签署 [!DNL HTTP] 请求的密钥。
   * **[!UICONTROL Show Signature Key]** :切换是否在浏览器中显示签名。
   * **[!UICONTROL HTTP Signature Encryption Method]** :指定用于加密签名的方法。 除非客 [!UICONTROL SHA1] 户喜欢使用其他方式，否则请使用。
   >[!NOTE]
   >
   >如果要为合作伙伴启用 [OAuth 2.0身份验证以实时传输数据](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) ，请填写下表中的字段。 斜体中 *的字段* ，需要像表中一样填写。

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
   | [!UICONTROL Username] | [!UICONTROL *授权&#x200B;*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，或者如果要编辑 **[!UICONTROL Update]** 现有服务器，则单击。