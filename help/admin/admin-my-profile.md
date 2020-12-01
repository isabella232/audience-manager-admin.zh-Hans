---
description: 编辑Audience Manager管理工具用户档案的详细信息或更改密码。
seo-description: 编辑Audience Manager管理工具用户档案的详细信息或更改密码。
seo-title: 我的配置文件
title: 我的配置文件
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 4%

---


# 我的配置文件 {#my-profile}

编辑Audience Manager管理工具用户档案的详细信息或更改密码。

<!-- c_my_profile.xml -->

## 编辑用户档案{#edit-profile}

视图并编辑Audience Manager管理工具用户档案，包括名和姓、用户名、电子邮件地址、电话号码、[!UICONTROL IMS ID]、用户角色和状态。

<!-- t_edit_profile.xml -->

1. 单击 **[!UICONTROL My Profile]**.

   ![步骤结果](assets/profile.png)

2. 填写以下字段：
   * **[!UICONTROL First Name]:** （必需）指定您的名字。
   * **[!UICONTROL Last Name]:(** 必需)指定您的姓氏。
   * **[!UICONTROL Username]:(** 必需)指定您的第一个用户名。
   * **[!UICONTROL Email Address]:(** 必需)指定您的电子邮件地址。
   * **[!UICONTROL Phone Number]:** 指定电话号码。
   * **[!UICONTROL IMS ID]:** 指定Internet消息服务ID。
   * **[!UICONTROL User Roles]：选** 择所需的用户角色：
      * **[!UICONTROL DEXADMIN]：提** 供管理员在Audience Manager管理工具中执行任务的权限。如果不选择此选项，则可以选择单个角色。 这些角色允许用户使用[!DNL API]调用执行任务，但不能在“管理”工具中执行。
      * **[!UICONTROL CREATE_USERS]:** 允许用户使用调用创建新 [!DNL API] 用户。
      * **[!UICONTROL DELETE_USERS]：允** 许用户使用调用删除现有 [!DNL API] 用户。
      * **[!UICONTROL EDIT_USERS]：允** 许用户使用调用编辑现 [!DNL API] 有用户。
      * **[!UICONTROL VIEW_USERS]：允** 许用户使用调用视图Audience Manager配置中的其他 [!DNL API] 用户。
      * **[!UICONTROL CREATE_PARTNERS]：允** 许用户使用调用创建Audience Manager [!DNL API] 合作伙伴。
      * **[!UICONTROL DELETE_PARTNERS]：允** 许用户使用调用删除Audience Manager [!DNL API] 合作伙伴。
      * **[!UICONTROL EDIT_PARTNERS]：允** 许用户使用调用编辑Audience Manager [!DNL API] 合作伙伴。
      * **[!UICONTROL VIEW_PARNTERS]：允** 许用户使用呼叫视图Audience Manager [!DNL API] 合作伙伴。
   * **[!UICONTROL Status]：选** 择所需的状态：
      * **[!UICONTROL Active]：指** 定此用户在活动Audience Manager用户中。
      * **[!UICONTROL Deactivated]：指** 定此用户是受众管理中已停用的用户。
      * **[!UICONTROL Expired]:** 指定此用户在Audience Manager中的帐户已过期。
      * **[!UICONTROL Locked Out]:** 指定锁定Audience Manager中此用户的帐户。
3. 单击 **[!UICONTROL Submit]**.

## 更改密码{#change-password}

更改您的Audience Manager管理工具密码。

<!-- t_change_password.xml -->

1. 单击 **[!UICONTROL My Profile]**.
1. 单击 **[!UICONTROL Change Password]**.

   ![](assets/change_password.png)

   您的Audience Manager密码必须为：

   * 长度至少为8个字符；
   * 至少包含一个大写字符；
   * 至少包含一个小写字符；
   * 至少包含一个数字；
   * 至少包含一个特殊字符；
   * 以字母数字字符开头和结尾；
   * 以字母数字字符开始和结束。

1. 指定旧密码。
1. 指定新密码，然后确认新密码。
1. 单击 **[!UICONTROL OK]**.