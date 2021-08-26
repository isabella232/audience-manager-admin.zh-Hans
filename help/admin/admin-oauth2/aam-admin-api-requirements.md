---
description: 您应当鼓励客户在使用Audience ManagerAPI时注意的事项。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API 要求和建议
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 2%

---

# API 要求和建议 {#api-requirements-and-recommendations}

您应当鼓励客户在使用Audience Manager[!DNL API]时注意的事项。

## 要求 {#requirements}

使用[!DNL Audience Manager] [!DNL API]代码时，请注意以下事项：

* **请求参数：** 除非另有指定，否则所有请求参数都是必需的。
* **[!DNL JSON]内容类型：** 在代 `content-type: application/json` ** `accept: application/json` 码中指定和。

* **请求和响应：** 将请求作为格式正确的对象 [!DNL JSON] 发送。[!DNL Audience Manager] 以格式化的数 [!DNL JSON] 据做出响应。服务器响应可以包含请求的数据、状态代码或两者。

* **访问：** 您的 [!DNL Audience Manager] 顾问将为您提供客户端ID和用于发出请求的 [!DNL API] 密钥。

* **文档和代码示例：** 斜体 ** 文本表示您在制作或接收数据时提供或传递的 [!DNL API] 变量。将&#x200B;*斜体*&#x200B;文本替换为您自己的代码、参数或其他必需信息。

## Recommendations:创建通用API用户 {#recommendations}

我们建议创建一个单独的技术用户帐户，以便与Audience Manager[!DNL API]s一起使用。这是一个通用帐户，它未绑定到客户组织中的特定用户或与其关联。 此类型的[!DNL API]用户帐户有助于完成以下两项任务：

* 识别正在调用[!DNL API]的服务（例如，来自使用我们的[!DNL API]的客户端应用程序的调用或进行批量更改的调用）。
* 提供对[!DNL API]s的无中断访问。与特定员工关联的帐户在离开公司时可能会被删除。 这将阻止您的客户使用可用的[!DNL API]代码。 未与特定员工绑定的通用帐户有助于避免此问题。

例如，对于此类帐户，假设您的客户希望使用[批量管理工具](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)一次更改多个区段。 要实现此目的，他们需要[!DNL API]访问权限。 创建一个非特定的[!DNL API]用户帐户，该帐户具有适当的凭据、密钥和密钥，以便进行[!DNL API]调用，而不是向特定用户添加权限。 如果客户端自行开发使用[!DNL Audience Manager] [!DNL API]的应用程序，则此功能也非常有用。
