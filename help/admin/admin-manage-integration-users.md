---
description: 使用“集成用户”页面可查看Audience Manager配置中的用户列表。您可以根据分配的用户角色编辑或删除现有用户或创建新用户。
seo-description: 使用“集成用户”页面可查看Audience Manager配置中的用户列表。您可以根据分配的用户角色编辑或删除现有用户或创建新用户。
seo-title: 集成用户
title: 集成用户
uuid: 13 dcb3 fb-4561-409c-84da-943d0 d390 cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 集成用户 {#integration-users}

使用 [!UICONTROL Integration Users] 页面可查看Audience Manager配置中的用户列表。您可以根据分配的用户角色编辑或删除现有用户或创建新用户。

<!-- c_integration_users.xml -->

您可以单击所需列的标题，以升序或降序排列每个列。
使用 [!UICONTROL Search] 该框或列表底部的分页控件查找所需的用户。

## 创建或编辑用户 {#create-edit-user}

使用Audience [!UICONTROL Integration Users] Manager [!UICONTROL Admin] 工具中的页面创建新用户或编辑现有用户的帐户。

<!-- t_create_user.xml -->

>[!NOTE]
>
>您必须 [!UICONTROL CREATE_USER] 具有角色才能创建新用户。您必须 [!UICONTROL EDIT_USER] 具有角色才能编辑现有用户。

1. 要创建新用户，请单击 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**。要编辑现有用户，请在 **[!UICONTROL Username]** 列中单击所需的用户。
2. 填写以下字段：
   * **[!UICONTROL First Name]**：(必需)指定用户的名字。
   * **[!UICONTROL Last Name]**：(必需)指定用户的姓氏。
   * **[!UICONTROL Username]**：(必需)指定用户的用户名。
   * **[!UICONTROL Email Address]**：(必需)指定用户的电子邮件地址。
   * **[!UICONTROL Phone Number]**：指定用户的电话号码。
   * **[!UICONTROL IMS ID]**：指定用户 [!UICONTROL Internet Messaging Service ID]的姓名。
   * **[!UICONTROL User Roles]**：选择所需的用户角色：
      * **[!UICONTROL DEXADMIN]**：提供管理员在Audience Manager [!UICONTROL Admin] 工具中执行任务的权限。如果您不选择此选项，则可以选择单独的角色。这些角色允许用户使用 [!DNL API] 调用执行任务，但不能使用管理员工具执行任务。
      * **[!UICONTROL CREATE_USERS]**：允许用户使用 [!DNL API] 呼叫创建新用户。
      * **[!UICONTROL DELETE_USERS]**：允许用户使用 [!DNL API] 呼叫删除现有用户。
      * **[!UICONTROL EDIT_USERS]**：允许用户使用 [!DNL API] 呼叫编辑现有用户。
      * **[!UICONTROL VIEW_USERS]**：允许用户使用 [!DNL API] 呼叫在Audience Manager配置中查看其他用户。
      * **[!UICONTROL CREATE_PARTNERS]**：允许用户使用 [!DNL API] 呼叫创建Audience Manager合作伙伴。
      * **[!UICONTROL DELETE_PARTNERS]**：允许用户使用 [!DNL API] 呼叫删除Audience Manager合作伙伴。
      * **[!UICONTROL EDIT_PARTNERS]**：允许用户使用 [!DNL API] 呼叫编辑Audience Manager合作伙伴。
      * **[!UICONTROL VIEW_PARNTERS]**：允许用户使用 [!DNL API] 呼叫查看Audience Manager合作伙伴。
   * **状态：** 选择 **[!UICONTROL Active]** 此选项可使此用户成为激活的Audience Manager用户。
3. 单击 **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

使用Audience [!UICONTROL Integration Users] Manager [!UICONTROL Admin] 工具中的页面删除现有用户。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>您必须 **[!UICONTROL DELETE_USER]** 具有角色才能创建新用户。

1. 单击 **[!UICONTROL Integration Users]**.
2. 单击 ![](assets/icon_delete.png) 所需用户 **[!UICONTROL Actions]** 的列。
3. Click **[!UICONTROL OK]** to confirm the deletion.