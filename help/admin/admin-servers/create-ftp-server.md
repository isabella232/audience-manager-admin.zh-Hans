---
description: 使用“Audience Manager管理”工具中的“服务器”页可创建新的FTP服务器或编辑现有服务器。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: 创建或编辑 FTP 服务器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# 创建或编辑 FTP 服务器 {#create-or-edit-an-ftp-server}

使用 [!UICONTROL Servers] “Audience Manager管理”工具中的页面来新建FTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须拥有 [!UICONTROL DEXADMIN] 角色来创建新服务器或编辑现有服务器。

1. 要创建新服务器，请单击 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 要编辑现有服务器，请在 **[!UICONTROL Label]** 列。
1. 为此服务器指定所需的标签。
1. 从 **[!UICONTROL Protocol]** 下拉列表，选择所需的协议： **FTP**.

   >[!NOTE]
   >
   >作为最佳实践，我们建议使用 [!DNL Amazon S3] 作为一种从合作伙伴获取文件并将文件交付给合作伙伴的方法。 [!DNL Amazon S3] 提供了一个简单的web服务界面，可用于随时随地从web上的任何位置存储和检索任意数量的数据。 有关更多信息，请参阅 [关于Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 在 *Audience Manager用户指南*.

1. 填写以下字段：

   * **[!UICONTROL Type]：** 选择所需的加密类型： **[!UICONTROL SFTP]** 或 **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]：** 为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]：** 为此服务器指定所需的端口。 将为每种加密类型显示默认端口。 您可以根据需要更改默认端口。
   * **[!UICONTROL Remote Path]：** 为此服务器指定所需的远程路径。 如果将此字段留空，则Audience Manager会将文件放置在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]：** 启用此选项以重命名 `.tmp` 文件完成。
   * **[!UICONTROL Filename Suffix]：** 指定要附加以传输文件的文本。
   * **[!UICONTROL Moved to When Finished]：** 指定要在完成时移动传输文件的位置的路径。
   * **[!UICONTROL Authentication]：** 指定所需的服务器身份验证方法： **[!UICONTROL Username/Password]** 或 **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >请记住添加出口 [!DNL FTP] [!DNL IP] 添加到允许的IP列表： **52.44.29.204**.

1. 对象 **[!UICONTROL SSH Key]** 身份验证：
   >[!NOTE]
   >
   >在配置SSH密钥身份验证时，请确保始终仅以OpenSSH格式生成公钥和私钥。
   1. 从任何生成公钥/私钥对 [!DNL Linux] 或 [!DNL Mac] 机器。
   1. 授予 **公钥** 以更新其 [!DNL SFTP] 服务器。 它们必须包含其服务器上公钥中的所有文本，包括 `-----BEGIN RSA PRIVATE KEY-----` 和  `-----END RSA PRIVATE KEY-----` . 作为交换，他们必须提供安装密钥的用户名。
   1. 将username字段更新为客户端提供的字段，并将key字段更新为 **私钥**.
1. 单击 **[!UICONTROL Create]** 如果要创建新服务器，请单击 **[!UICONTROL Update]** 如果您正在编辑现有服务器。
