---
description: 使用Audience Manager管理员工具中的服务器页面创建新的HTTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理员工具中的服务器页面创建新的HTTP服务器或编辑现有服务器。
seo-title: 创建或编辑HTTP服务器
title: 创建或编辑HTTP服务器
uuid: ef0e751-e239-4dc6-a4 f6-73cc05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 创建或编辑HTTP服务器 {#create-or-edit-an-http-server}

使用Audience Manager管理工具中的 [!UICONTROL Servers] 页面创建新的HTTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须 [!UICONTROL DEXADMIN] 具有角色才能创建新服务器或编辑现有服务器。

1. 要创建新服务器，请转至 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。要编辑现有服务器，请在 **[!UICONTROL Label]** 列中单击所需的服务器。
1. 指定此服务器所需的标签。
1. 从 **[!UICONTROL Protocol]** 下拉列表中，选择所需的协议： [!DNL HTTP]。
1. 填写以下字段：

   * **[!UICONTROL Domain]：** 为此服务器指定所需的域(主机)。
   * **[!UICONTROL Port]：** 为此服务器指定所需端口。将为每个加密类型显示默认端口。如有必要，可更改默认端口
   * **[!UICONTROL Maximum Users Per Request]：** 指定此服务器允许的每个请求的最大用户数。
   * **[!UICONTROL URL Prefix]：** 指定用于此服务器的 [!DNL URL] 前缀。
   * **[!UICONTROL Authentication URL]：** 指定此 [!UICONTROL Authentication URL]`HTTP` 服务器的名称。
   * **[!UICONTROL Authentication]：** 指定所需的身份验证方法： **[!UICONTROL None]****[!UICONTROL Username/Password]****[!UICONTROL SSH Key]**&#x200B;或.
   * **[!UICONTROL HTTP Signature Header]：** 客户提供 [!DNL HTTP] 的标题的名称，其中包含 [!DNL HTTP] 签名密钥。默认值为 [!UICONTROL X-Signature]，如下面的示例所示：

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

   * **[!UICONTROL HTTP Signature Key]：** 客户提供 [!DNL HTTP] 的请求用于签署请求的密钥。
   * **[!UICONTROL Show Signature Key]：** 切换是否在浏览器中显示签名。
   * **[!UICONTROL HTTP Signature Encryption Method]：** 指定用于加密签名的方法。除非 [!UICONTROL SHA1] 客户更倾向于使用。
   >[!NOTE]
   >
   >如果您希望为合作伙伴启用 [OAuth2.0身份验证，](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) 请填写字段，如下表所示。*斜体中的字段* 需要完全像表一样填充。

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
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，或者在 **[!UICONTROL Update]** 编辑现有服务器时单击。