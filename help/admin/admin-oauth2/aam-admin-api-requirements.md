---
description: 您应鼓励客户在使用Audience ManagerAPI时了解的事情。
seo-description: 您应鼓励客户在使用Audience ManagerAPI时了解的事情。
seo-title: API 要求和建议
title: API 要求和建议
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# API 要求和建议 {#api-requirements-and-recommendations}

您应鼓励客户在使用Audience Manager[!DNL API]时注意的事项。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]代码时，请注意以下事项：

* **请求参数：除** 非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]内容类型：** 指 `content-type: application/json` ** `accept: application/json` 定和在代码中。

* **请求和响应：以格式** 正确的对象形式发送 [!DNL JSON] 请求。[!DNL Audience Manager] 用格式化 [!DNL JSON] 的数据做出响应。服务器响应可以包含请求的数据、状态代码或两者。

* **访问：** 顾 [!DNL Audience Manager] 问将为您提供一个客户端ID和用于发出请求的 [!DNL API] 密钥。

* **文档和代码示例：** 斜 ** 体文本表示您在创建或接收数据时提供或传递的 [!DNL API] 变量。将斜体&#x200B;*文本替换为您自己的代码、参数或其他必需信息。*

## Recommendations:创建通用API用户{#recommendations}

我们建议创建单独的技术用户帐户以使用Audience Manager[!DNL API]。这是一个通用帐户，它没有绑定到客户组织中的特定用户或与其关联。 此类型的[!DNL API]用户帐户有助于完成以下两项任务：

* 确定调用[!DNL API]的服务（例如，来自使用我们的[!DNL API]的客户端应用程序的调用或进行批量更改的调用）。
* 提供对[!DNL API]s的不间断访问。与特定员工关联的帐户在他们离开公司时可能会被删除。 这将阻止您的客户使用可用的[!DNL API]代码。 未绑定到特定员工的通用帐户有助于避免此问题。

作为此类帐户的示例或用例，假设您的客户希望使用[批量管理工具](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)一次更改大量细分。 为此，他们需要[!DNL API]访问。 不要向特定用户添加权限，而是创建一个非特定的[!DNL API]用户帐户，该帐户具有进行[!DNL API]调用所需的相应凭据、密钥和机密。 如果客户端开发自己的使用[!DNL Audience Manager] [!DNL API]的应用程序，这也很有用。
