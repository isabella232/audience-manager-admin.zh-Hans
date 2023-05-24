---
description: 您应鼓励客户在使用Audience ManagerAPI时注意的事项。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API 要求和建议
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# API 要求和建议 {#api-requirements-and-recommendations}

您应鼓励客户在与Audience Manager合作时注意的事项 [!DNL API]s.

## 要求 {#requirements}

使用时，请注意以下事项 [!DNL Audience Manager] [!DNL API] 代码：

* **请求参数：** 除非另有指定，否则需要所有请求参数。
* **[!DNL JSON]内容类型：** 指定 `content-type: application/json` *和* `accept: application/json` 在您的代码中。

* **请求和响应：** 以正确格式化的方式发送请求 [!DNL JSON] 对象。 [!DNL Audience Manager] 响应方式 [!DNL JSON] 格式化数据。 服务器响应可以包含请求的数据、状态代码或同时包含这两者。

* **访问：** 您的 [!DNL Audience Manager] 顾问将为您提供客户端ID和密钥，以便您制作 [!DNL API] 请求。

* **文档和代码示例：** 文本输入 *斜体* 表示在制作或接收时提供或传入的变量 [!DNL API] 数据。 Replace *斜体* 包含您自己的代码、参数或其他必需信息的文本。

## Recommendations：创建通用API用户 {#recommendations}

我们建议创建一个单独的技术用户帐户来使用该Audience Manager [!DNL API]s.这是一个通用帐户，与您客户组织中的特定用户不绑定或不关联。 此类型 [!DNL API] 用户帐户可帮助完成以下两件事：

* 识别什么服务在调用 [!DNL API] (例如，从使用我们的 [!DNL API]或进行批量更改)。
* 提供对的不间断访问 [!DNL API]s.与特定员工关联的帐户可能会在员工离开公司时删除。 这会阻止您的客户使用可用的 [!DNL API] 代码。 不绑定到特定员工的通用帐户有助于避免此问题。

作为此类帐户的示例或用例，假设您的客户希望使用 [批量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). 要做到这一点，他们需要 [!DNL API] 访问权限。 不要向特定用户添加权限，请创建非特定、 [!DNL API] 具有要生成的相应凭据、密钥和密钥的用户帐户 [!DNL API] 呼叫。 如果客户端开发自己的应用程序，而这些应用程序又使用 [!DNL Audience Manager] [!DNL API]s.
