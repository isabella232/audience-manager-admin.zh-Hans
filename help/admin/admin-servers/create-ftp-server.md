---
description: 使用Audience Manager管理工具中的“服务器”页面创建新的FTP服务器或编辑现有服务器。
seo-description: 使用Audience Manager管理工具中的“服务器”页面创建新的FTP服务器或编辑现有服务器。
seo-title: ' 创建或编辑FTP服务器'
title: ' 创建或编辑FTP服务器'
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 创建或编辑FTP服务器 {#create-or-edit-an-ftp-server}

使用Audience [!UICONTROL Servers] Manager管理工具中的页面创建新的FTP服务器或编辑现有服务器。

>[!NOTE]
>
>要创建新服务 [!UICONTROL DEXADMIN] 器或编辑现有服务器，您必须具有该角色。

1. 要创建新服务器，请单击 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**。 要编辑现有服务器，请在列中单击所需的服 **[!UICONTROL Label]** 务器。
1. 为此服务器指定所需的标签。
1. 从下 **[!UICONTROL Protocol]** 拉列表中，选择所需的协议： **FTP**。

   >[!NOTE]
   >
   >作为最佳实践，我们建议将 [!DNL Amazon S3] 文件用作从合作伙伴获取文件并将文件交付给合作伙伴的方法。 [!DNL Amazon S3] 提供一个简单的Web服务界面，该界面可用于从Web上的任意位置随时存储和检索任意数量的数据。 有关详细信息，请参 [阅Audience Manager用户指南中的](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) “关于 *Amazon S3”*。

1. 填写以下字段：

   * **[!UICONTROL Type]** :选择所需的加密类型：或 **[!UICONTROL SFTP]** 者 **[!UICONTROL FTPs/TLS]**。
   * **[!UICONTROL Domain]** :为此服务器指定所需的域（主机）。
   * **[!UICONTROL Port]** :为此服务器指定所需的端口。 将显示每个加密类型的默认端口。 如有必要，可以更改默认端口。
   * **[!UICONTROL Remote Path]** :为此服务器指定所需的远程路径。 如果将此字段留空，Audience Manager会将文件放在默认目录中。
   * **[!UICONTROL .tmp File Rename on Completion]** :启用此选项后，将在完成 `.tmp` 时重命名文件。
   * **[!UICONTROL Filename Suffix]** :指定要在传输文件中附加的文本。
   * **[!UICONTROL Moved to When Finished]** :指定完成时要移动传输文件的位置的路径。
   * **[!UICONTROL Authentication]** :指定所需的服务器身份验证方法：或 **[!UICONTROL Username/Password]** 者 **[!UICONTROL SSH Key]**。
   >[!NOTE]
   >
   >请记住将我们的出口列入白名单 [!DNL FTP][!DNL IP]: **52.44.29.204**。

1. 对于身 **[!UICONTROL SSH Key]** 份验证：
   1. 从任何或计算机生成公共／私 [!DNL Linux] 钥 [!DNL Mac] 对。
   1. 将公钥 **给客户端** ，以在其服务器上进行更 [!DNL SFTP] 新。 它们必须包含服务器上公钥中的所有文本，包括 `-----BEGIN RSA PRIVATE KEY-----` 和 `-----END RSA PRIVATE KEY-----` 。 作为交换，他们必须提供安装密钥时所使用的用户名。
   1. 使用客户端提供的用户名字段更新用户名字段，使用私钥更 **新密钥字段**。
1. 如果 **[!UICONTROL Create]** 要创建新服务器，请单击，或者如果要编辑 **[!UICONTROL Update]** 现有服务器，则单击。
