---
description: 在使用Audience Manager API时应鼓励客户了解的事项。
seo-description: 在使用Audience Manager API时应鼓励客户了解的事项。
seo-title: API要求和推荐
title: API要求和推荐
uuid: eba9cf92-f0 c8-4394-8532-0de9 e7 b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API要求和推荐 {#api-requirements-and-recommendations}

您应鼓励客户在使用Audience Manager [!DNL API]时应注意的事项。

## 要求 {#requirements}

使用 [!DNL Audience Manager][!DNL API] 代码时请注意以下事项：

* **请求参数：** 除非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]内容类型：** 指定 `content-type: application/json`*并*`accept: application/json` 在代码中。

* **请求和答复：** 将请求发送为格式正确的 [!DNL JSON] 对象。[!DNL Audience Manager] 响应 [!DNL JSON] 格式数据。服务器响应可以包含请求的数据、状态代码或两者。

* **访问：**[!DNL Audience Manager] 您的顾问将为您提供一个客户ID和允许您 [!DNL API] 提出请求的密钥。

* **文档和代码示例：***斜体文本* 表示您在制作或接收 [!DNL API] 数据时提供或传入的变量。将 *斜体* 文本替换为您自己的代码、参数或其他必需信息。

## 推荐：创建通用API用户 {#recommendations}

我们建议创建一个单独的技术用户帐户，用于Audience Manager [!DNL API]的使用。这是一个通用帐户，不绑定到客户组织中的特定用户或与其关联。这类 [!DNL API] 用户帐户有助于完成以下两件事：

* 确定哪些服务正在调用( [!DNL API] 例如，来自使用我们 [!DNL API]的s或进行批量更改的客户端应用程序的调用)。
* 提供不间断的s访问权限 [!DNL API]。与特定员工关联的帐户在离开公司时可能会被删除。这将阻止您的客户使用可用 [!DNL API] 代码。不与特定员工绑定的通用帐户可帮助避免此问题。

作为此类帐户的示例或用例，假设您的客户希望通过 [批量管理工具同时更改大量细分](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)。为此，他们需要 [!DNL API] 访问。不是向特定用户添加权限，而是创建一个非特定的用户帐户， [!DNL API] 该帐户具有适当的凭据、密钥和用于 [!DNL API] 拨打调用的机密。如果客户端开发自己的应用程序，则此功能也很有用 [!DNL Audience Manager][!DNL API]。
