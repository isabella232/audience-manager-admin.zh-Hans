---
description: 使用Audience Manager管理员工具中的服务器页面创建新的FTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理员工具中的服务器页面创建新的FTP服务器或编辑现有服务器。
seo-title: 创建或编辑FTP服务器
title: 创建或编辑FTP服务器
uuid: 9273abb2-963d-4d83-bf5 a-b3817 f0 b90 e6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 创建或编辑FTP服务器 {#create-or-edit-an-ftp-server}

使用Audience Manager管理工具中的 [!UICONTROL Servers] 页面创建新的FTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须 [!UICONTROL DEXADMIN] 具有角色才能创建新服务器或编辑现有服务器。

1. 要创建新服务器，请单击 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。要编辑现有服务器，请在 **[!UICONTROL Label]** 列中单击所需的服务器。
1. 指定此服务器所需的标签。
1. 从 **[!UICONTROL Protocol]** 下拉列表中，选择所需的协议： **FTP**。

   >[!NOTE]
   >
   >作为最佳实践，我们建议用作 [!DNL Amazon S3] 一种从中获取文件并向合作伙伴交付文件的方法。[!DNL Amazon S3] 提供一个简单的Web服务界面，可用于随时从Web上的任意位置存储和检索任何数据。有关更多信息，请参阅 [Amazon](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) Manager用户指南中的关于 *Amazon S3*。

1. 填写以下字段：

   * **[!UICONTROL Type]：** 选择所需的加密类型： **[!UICONTROL SFTP]****[!UICONTROL FTPs/TLS]**&#x200B;或.
   * **[!UICONTROL Domain]：** 为此服务器指定所需的域(主机)。
   * **[!UICONTROL Port]：** 为此服务器指定所需端口。将为每个加密类型显示默认端口。如有必要，可更改默认端口。
   * **[!UICONTROL Remote Path]：** 为此服务器指定所需的远程路径。如果将此字段留空，Audience Manager将把文件放在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]：** 启用此选项可在完成时重命名 `.tmp` 文件。
   * **[!UICONTROL Filename Suffix]：** 指定要附加到传输文件的文本。
   * **[!UICONTROL Moved to When Finished]：** 指定要在完成时移动传输文件的位置。
   * **[!UICONTROL Authentication]：** 指定所需的服务器身份验证方法： **[!UICONTROL Username/Password]****[!UICONTROL SSH Key]**&#x200B;或.
   >[!NOTE]
   >
   >记得将我们 [!DNL FTP][!DNL IP]的电子邮件地址列入白名单： **52.44.29.204**。

1. **[!UICONTROL SSH Key]** 用于身份验证：
   1. 从任何 [!DNL Linux] 或 [!DNL Mac] 计算机生成公共/私钥对。
   1. 将 **公钥提供** 给客户端，在 [!DNL SFTP] 其服务器上更新。它们必须包括服务器上的公钥中的所有文本，包括 `-----BEGIN RSA PRIVATE KEY-----` 和 `-----END RSA PRIVATE KEY-----` 。交换后，他们必须提供安装密钥的用户名。
   1. 使用客户端提供的用户名字段和 **私钥的密钥字段更新用户名字段**。
1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，或者在 **[!UICONTROL Update]** 编辑现有服务器时单击。
