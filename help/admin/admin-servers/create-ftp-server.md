---
description: 使用Audience Manager管理工具中的“服务器”页面创建新的FTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理工具中的“服务器”页面创建新的FTP服务器或编辑现有服务器。
seo-title: 创建或编辑 FTP 服务器
title: 创建或编辑 FTP 服务器
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 78d694670e7abdc18938c5be729ad499e2647825
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 5%

---


# 创建或编辑 FTP 服务器 {#create-or-edit-an-ftp-server}

使用 [!UICONTROL Servers] Audience Manager管理工具中的页面创建新的FTP服务器或编辑现有服务器。

>[!NOTE]
>
>您必须具有角 [!UICONTROL DEXADMIN] 色才能创建新服务器或编辑现有服务器。

1. 要创建新服务器，请单击 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**。 要编辑现有服务器，请在列中单击所需的服 **[!UICONTROL Label]** 务器。
1. 为此服务器指定所需的标签。
1. 从下 **[!UICONTROL Protocol]** 拉列表中，选择所需的协议： **FTP**。

   >[!NOTE]
   >
   >作为最佳实践，我们建 [!DNL Amazon S3] 议将文件用作从合作伙伴获取文件并将文件交付给合作伙伴的方法。 [!DNL Amazon S3] 提供简单的web服务界面，可随时从Web上的任何位置存储和检索任意数量的数据。 有关详细信息，请 [参阅Audience Manager用户指南](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) 中 *的“关于Amazon S3”*。

1. 填写以下字段：

   * **[!UICONTROL Type]:**选择所需的加密类型：**[!UICONTROL SFTP]**或&#x200B;**[!UICONTROL FTPs/TLS]**者
   * **[!UICONTROL Domain]:**为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]:**指定此服务器的所需端口。 将显示每个加密类型的默认端口。 如有必要，可以更改默认端口。
   * **[!UICONTROL Remote Path]:**为此服务器指定所需的远程路径。 如果将此字段留空，Audience Manager会将文件放在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]:**启用此选项后，将在完成`.tmp`时重命名文件。
   * **[!UICONTROL Filename Suffix]:**指定要在传输文件时附加的文本。
   * **[!UICONTROL Moved to When Finished]:**指定完成时要将传输文件移动到的位置的路径。
   * **[!UICONTROL Authentication]:**指定所需的服务器身份验证方法：**[!UICONTROL Username/Password]**或&#x200B;**[!UICONTROL SSH Key]**者
   >[!NOTE]
   >
   >请记住将我们的出 [!DNL FTP] 口添 [!DNL IP] 加到允许的IP列表中： **52.44.29.204**。

1. 对于身 **[!UICONTROL SSH Key]** 份验证：
   >[!NOTE]
   >
   >配置SSH密钥身份验证时，请确保始终仅以OpenSSH格式生成公钥和私钥。
   1. 从任何或计算机生成公共／私 [!DNL Linux] 有密 [!DNL Mac] 钥对。
   1. 为客户端 **提供公钥** ，以便在其服务器上进行更 [!DNL SFTP] 新。 它们必须包含服务器上公钥中的所有文本，包括 `-----BEGIN RSA PRIVATE KEY-----` 和 `-----END RSA PRIVATE KEY-----` 。 作为交换，他们必须提供安装密钥时所使用的用户名。
   1. 使用客户端提供的用户名字段更新用户名字段，使用私钥更 **新密钥字段**。
1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，如 **[!UICONTROL Update]** 果要编辑现有服务器，则单击。
