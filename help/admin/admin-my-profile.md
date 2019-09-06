---
description: 编辑Audience Manager管理员工具配置文件的详细信息或更改密码。
seo-description: 编辑Audience Manager管理员工具配置文件的详细信息或更改密码。
seo-title: 我的个人资料
title: 我的个人资料
uuid: cCaa611d-c855-484e-9696-081d9 b4 e0935
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 我的个人资料 {#my-profile}

编辑Audience Manager管理员工具配置文件的详细信息或更改密码。

<!-- c_my_profile.xml -->

## 编辑配置文件 {#edit-profile}

查看和编辑Audience Manager管理员工具配置文件，包括名字、姓氏、用户名、电话号码、 [!UICONTROL IMS ID]用户角色、用户角色和状态。

<!-- t_edit_profile.xml -->

1. 单击 **[!UICONTROL My Profile]**.

   ![步骤结果](assets/profile.png)

2. 填写以下字段：
   * **[!UICONTROL First Name]：** (必需)指定您的名字。
   * **[!UICONTROL Last Name]：** (必需)指定姓氏。
   * **[!UICONTROL Username]：** (必需)指定您的第一个用户名。
   * **[!UICONTROL Email Address]：** (必需)指定电子邮件地址。
   * **[!UICONTROL Phone Number]：** 指定电话号码。
   * **[!UICONTROL IMS ID]：** 指定Internet Messaging Service ID。
   * **[!UICONTROL User Roles]：** 选择所需的用户角色：
      * **[!UICONTROL DEXADMIN]：** 提供管理员访问Audience Manager管理员工具中的任务的权限。如果您不选择此选项，则可以选择单独的角色。这些角色允许用户使用 [!DNL API] 调用执行任务，但不能使用管理员工具执行任务。
      * **[!UICONTROL CREATE_USERS]：** 允许用户使用 [!DNL API] 呼叫创建新用户。
      * **[!UICONTROL DELETE_USERS]：** 允许用户使用 [!DNL API] 呼叫删除现有用户。
      * **[!UICONTROL EDIT_USERS]：** 允许用户使用 [!DNL API] 呼叫编辑现有用户。
      * **[!UICONTROL VIEW_USERS]：** 允许用户使用 [!DNL API] 呼叫在Audience Manager配置中查看其他用户。
      * **[!UICONTROL CREATE_PARTNERS]：** 允许用户使用 [!DNL API] 呼叫创建Audience Manager合作伙伴。
      * **[!UICONTROL DELETE_PARTNERS]：** 允许用户使用 [!DNL API] 呼叫删除Audience Manager合作伙伴。
      * **[!UICONTROL EDIT_PARTNERS]：** 允许用户使用 [!DNL API] 呼叫编辑Audience Manager合作伙伴。
      * **[!UICONTROL VIEW_PARNTERS]：** 允许用户使用 [!DNL API] 呼叫查看Audience Manager合作伙伴。
   * **[!UICONTROL Status]：** 选择所需状态：
      * **[!UICONTROL Active]：** 指定此用户在活动Audience Manager用户中。
      * **[!UICONTROL Deactivated]：** 指定此用户是Audience Management中已停用的用户。
      * **[!UICONTROL Expired]：** 指定此用户在Audience Manager中的帐户已过期。
      * **[!UICONTROL Locked Out]：** 指定此用户在Audience Manager中的帐户已锁定。
3. 单击 **[!UICONTROL Submit]**.

## 更改密码 {#change-password}

更改Audience Manager管理员工具密码。

<!-- t_change_password.xml -->

1. 单击 **[!UICONTROL My Profile]**.
1. 单击 **[!UICONTROL Change Password]**.

   ![](assets/change_password.png)

   Audience Manager密码必须为：

   * 长度至少有八个字符；
   * 包含一个大写字符；
   * 至少包含一个小写字符；
   * 包含至少一个数字；
   * 至少包含一个特殊字符；
   * 以字母数字字符开始和结束；
   * 以字母数字字符开头并结束。

1. 指定旧密码。
1. 指定新密码，然后确认新密码。
1. 单击 **[!UICONTROL OK]**.