---
description: Beta环境用于测试Audience Manager实施。测试版中所做的更改不会影响生产数据。Audience Manager beta环境是一个规模较小、独立版本的生产环境。必须在此环境中输入和收集要测试的所有数据。
seo-description: Beta环境用于测试Audience Manager实施。测试版中所做的更改不会影响生产数据。Audience Manager beta环境是一个规模较小、独立版本的生产环境。必须在此环境中输入和收集要测试的所有数据。
seo-title: 测试版环境
solution: Audience Manager
title: 测试版环境
uuid: 6a253f4e-96e7-4395-a783-a8 eb213 b7 af
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# 测试版环境 {#beta-environment}

Beta环境用于测试Audience Manager实施。测试版中所做的更改不会影响生产数据。Audience Manager beta环境是一个规模较小、独立版本的生产环境。必须在此环境中输入和收集要测试的所有数据。

## 概述 {#overview}

<!-- beta_environment_admin.xml -->

| 服务 | URL/主机名 | 设置步骤 |
|--- |--- |--- |
| S3 |  | 请参阅 [设置Amazon S Buckets](admin-beta-environment.md#provision-s3-buckets)。 |
| DCS | https&amp; amp；冒号；/dcs-beta.demdex.net/.。 | 无需任何其他步骤。请参阅 [访问测试版环境中的DCS](admin-beta-environment.md#access-dcs-beta-environment)。 |
| 用户界面 | https&amp; amp；冒号；//bank-beta.demdex.com | 数据将按月从制作复制到测试环境。生产凭据适用于测试版。 |
| API | https&amp; amp；冒号；/api-beta.demdex.com/.。 | 数据将按月从制作复制到测试环境。生产凭据适用于测试版。 |

## 规定Amazon S Buckets {#provision-s3-buckets}

>[!NOTE]
>
>我们正在放弃使用 [!DNL FTP/SFTP]。另外，请注意，出站数据传输不适用于测试版环境。

为入站数据设置 [!DNL S3] 套接字：

1. 使用 [**SKMS请求TechPs帮助**](https://skms.adobe.com/) 功能。
1. 转到 **[!UICONTROL Request TechOps Help]** 左侧导航边栏。
1. In **[!UICONTROL Request Search]**，in the Search field in the search field.
1. 向下滚动搜索结果并单击 **Audience Manager- S3入站/出站帐户供应**。
1. 填写供应窗口中的字段，并在字段中指定 **Sandbox环境****[!UICONTROL Environment]** 。

>[!NOTE]
>
>我们同意使用 [!DNL FTP/SFTP] 并鼓励 [!UICONTROL Amazon S3]使用。我们鼓励使用Amazon [!UICONTROL Amazon S3][S中列出的原因：](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)关于。

## 访问Beta环境中的DCS {#access-dcs-beta-environment}

要访问测试环境 [!UICONTROL DCS] 中的内容，请执行以下操作：

1. 使用该命令进行 [!UICONTROL DCS][!DNL curl][通话](https://curl.haxx.se/docs/manpage.html)。[!DNL Curl] 是一种使用受支持的协议之一从服务器或服务器传输数据的工具。

   例如：`curl -v https://dcs-beta.demdex.net/event`

1. 验证您的请求是否通过“ [!UICONTROL DCS] 响应头[!DNL sandbox]”进行 [!UICONTROL DCS] 了测试。

   例如：

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->