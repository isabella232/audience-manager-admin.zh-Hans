---
description: 您应鼓励客户在使用Audience Manager API时了解的事情。
seo-description: 您应鼓励客户在使用Audience Manager API时了解的事情。
seo-title: ' API要求和建议'
title: ' API要求和建议'
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API要求和建议 {#api-requirements-and-recommendations}

您应该鼓励客户在使用Audience Manager时了解的事 [!DNL API]情。

## 要求 {#requirements}

使用代码时请注意以 [!DNL Audience Manager] 下事 [!DNL API] 项：

* **** 请求参数：除非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]** 内容类型：在 `content-type: application/json` 代 *码中*`accept: application/json` 指定和指定。

* **** 请求和答复：将请求作为格式正确的对象 [!DNL JSON] 发送。 [!DNL Audience Manager] 对格式化的数 [!DNL JSON] 据做出响应。 服务器响应可以包含请求的数据、状态代码或两者。

* **** 访问：您 [!DNL Audience Manager] 的顾问将为您提供客户端ID和密钥，以便您提出 [!DNL API] 请求。

* **** 文档和代码示例：斜体 *文本* ，表示您在创建或接收数据时提供或传入的变 [!DNL API] 量。 将斜 *体文本替换* ，替换为您自己的代码、参数或其他必需信息。

## 建议：创建通用API用户 {#recommendations}

我们建议创建单独的技术用户帐户以与Audience Manager一起 [!DNL API]使用。这是一个通用帐户，它不绑定到客户组织中的特定用户或与其关联。 此类用户帐 [!DNL API] 户有助于完成以下两项任务：

* 识别调用哪项服务( [!DNL API] 例如，来自使用我们的客户端应用程序的调用或进行 [!DNL API]批量更改的调用)。
* 提供对s的不间断 [!DNL API]访问。与特定员工关联的帐户在离开公司时可能会被删除。 这将阻止您的客户使用可用的代 [!DNL API] 码。 未绑定到特定员工的通用帐户有助于避免此问题。

例如，作为此类帐户的示例或用例，假设客户希望使用批量管理工具同时更改大量 [细分](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)。 为此，他们需要访问 [!DNL API] 权限。 不要向特定用户添加权限，而是创建一个非特定的用户帐户，该帐户具有相应的凭据、密钥和机密进行 [!DNL API][!DNL API] 调用。 如果客户开发自己使用s的应用程序，这也很有 [!DNL Audience Manager][!DNL API]用。
