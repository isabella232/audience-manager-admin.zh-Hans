---
description: 使用Audience Manager管理工具中的“服务器”页可创建新的HTTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理工具中的“服务器”页可创建新的HTTP服务器或编辑现有服务器。
seo-title: 创建或编辑 HTTP 服务器
title: 创建或编辑 HTTP 服务器
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: d518ba4011f203a7d450ce76d8c1924f7d73a815
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 7%

---


# 创建或编辑 HTTP 服务器{#create-or-edit-an-http-server}

使用Audience Manager [!UICONTROL Servers] 管理工具中的页面创建新的HTTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须具有角 [!UICONTROL DEXADMIN] 色才能创建新服务器或编辑现有服务器。

1. 要创建新服务器，请转到 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要编辑现有服务器，请在列中单击所需的服 **[!UICONTROL Label]** 务器。
1. 为此服务器指定所需的标签。
1. 从下 **[!UICONTROL Protocol]** 拉列表中，选择所需的协议： [!DNL HTTP].
1. 填写以下字段：

   * **[!UICONTROL Domain]:** 为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]:** 指定此服务器的所需端口。 将显示每个加密类型的默认端口。 如有必要，可更改默认端口
   * **[!UICONTROL Maximum Users Per Request]:** 指定此服务器允许的每个请求的最大用户数。
   * **[!UICONTROL URL Prefix]:** 指定要 [!DNL URL] 用于此服务器的前缀。
   * **[!UICONTROL Authentication URL]:** 指定此 [!UICONTROL Authentication URL] 服务器 `HTTP` 的。
   * **[!UICONTROL Authentication]:** 指定所需的身份验证方法： **[!UICONTROL None]**、 **[!UICONTROL Username/Password]**&#x200B;或 **[!UICONTROL SSH Key]**。
   * **[!UICONTROL HTTP Signature Header]:** 由客户提 [!DNL HTTP] 供的包含签名密钥的头 [!DNL HTTP] 的名称。 默认值 [!UICONTROL X-Signature]为，如下例所示：

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

   * **[!UICONTROL HTTP Signature Key]:** 客户提供的用 [!DNL HTTP] 于签署请求的密钥。
   * **[!UICONTROL Show Signature Key]:** 切换是否在浏览器中显示签名。
   * **[!UICONTROL HTTP Signature Encryption Method]:** 指定用于加密签名的方法。 除非 [!UICONTROL SHA1] 客户另有选择，否则使用。

   >[!NOTE]
   >
   >如果要为合 [作伙伴启用OAuth 2.0身份验证实时数据传输](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) ，请填写下表中的字段。 斜体中 *的字段* ，需要完全按表中的方式填写。

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

1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，如 **[!UICONTROL Update]** 果要编辑现有服务器，则单击。
