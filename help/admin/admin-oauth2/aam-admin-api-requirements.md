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

您应鼓励客户在与Audience Manager合作时了解的事 [!DNL API]情。

## 要求 {#requirements}

使用代码时请注意 [!DNL Audience Manager] 以 [!DNL API] 下事项：

* **请求参数：** 除非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]内容类型：**在`content-type: application/json`代&#x200B;*码*`accept: application/json`中指定。

* **请求和答复：** 将请求作为格式正确的对象 [!DNL JSON] 发送。 [!DNL Audience Manager] 用格式化的 [!DNL JSON] 数据做出响应。 服务器响应可以包含请求的数据、状态代码或两者。

* **访问：** 您 [!DNL Audience Manager] 的顾问将为您提供客户端ID和密钥，以便您进行 [!DNL API] 请求。

* **文档和代码示例：** 斜体 *文本* 表示您在创建或接收数据时提供或传递的 [!DNL API] 变量。 将斜 *体文本* 替换为您自己的代码、参数或其他必需信息。

## 建议： 创建通用API用户 {#recommendations}

我们建议创建单独的技术用户帐户以与Audience Manager [!DNL API]配合。 这是一个通用帐户，它没有绑定到客户组织中的特定用户或与其关联。 此类型的用 [!DNL API] 户帐户有助于完成以下两项任务：

* 确定调用哪项服务( [!DNL API] 例如，来自使用我们的客户端应用程序的调用或 [!DNL API]进行批量更改的调用)。
* 不间断地访问 [!DNL API]s。 与特定员工关联的帐户在他们离开公司时可能会被删除。 这将阻止您的客户使用可用的 [!DNL API] 代码。 未绑定到特定员工的通用帐户有助于避免此问题。

作为此类帐户的示例或用例，假设客户希望使用批量管理工具一次更改大 [量细分](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)。 为此，他们需要访 [!DNL API] 问权。 不要向特定用户添加权限，而是创建一个非特定的 [!DNL API] 用户帐户，该帐户具有相应的凭据、密钥和密码进行 [!DNL API] 呼叫。 如果客户端开发自己的使用s的应用程序，这也很 [!DNL Audience Manager] 有 [!DNL API]用。
