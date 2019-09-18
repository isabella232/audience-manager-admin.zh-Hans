---
description: 使用“集成用户”页可查看Audience manager配置中的用户列表。 您可以编辑或删除现有用户或创建新用户，前提是您分配了相应的用户角色。
seo-description: 使用“集成用户”页可查看Audience manager配置中的用户列表。 您可以编辑或删除现有用户或创建新用户，前提是您分配了相应的用户角色。
seo-title: 集成用户
title: 集成用户
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 集成用户 {#integration-users}

使用该 [!UICONTROL Integration Users] 页面可查看Audience manager配置中的用户列表。 您可以编辑或删除现有用户或创建新用户，前提是您分配了相应的用户角色。

<!-- c_integration_users.xml -->

您可以通过单击所需列的标题，按升序或降序对每列进行排序。
使用列 [!UICONTROL Search] 表底部的框或分页控件查找所需用户。

## 创建或编辑用户 {#create-edit-user}

使用Audience manager [!UICONTROL Integration Users] 工具中的页 [!UICONTROL Admin] 面创建新用户或编辑现有用户的帐户。

<!-- t_create_user.xml -->

>[!NOTE]
>
>要创建新用 [!UICONTROL CREATE_USER] 户，您必须具有角色。 要编辑现有用 [!UICONTROL EDIT_USER] 户，您必须具有角色。

1. 要创建新用户，请单击 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**。 要编辑现有用户，请在列中单击所需的用 **[!UICONTROL Username]** 户。
2. 填写以下字段：
   * **[!UICONTROL First Name]**:（必需）指定用户的名。
   * **[!UICONTROL Last Name]**:（必需）指定用户的姓氏。
   * **[!UICONTROL Username]**:（必需）指定用户的用户名。
   * **[!UICONTROL Email Address]**:（必需）指定用户的电子邮件地址。
   * **[!UICONTROL Phone Number]**:指定用户的电话号码。
   * **[!UICONTROL IMS ID]**:指定用户的 [!UICONTROL Internet Messaging Service ID]。
   * **[!UICONTROL User Roles]**:选择所需的用户角色：
      * **[!UICONTROL DEXADMIN]**:为管理员提供在Audience Manager工具中执行任务的 [!UICONTROL Admin] 权限。 如果不选择此选项，则可以选择单个角色。 这些角色允许用户使用调用执行任 [!DNL API] 务，但不能在“管理”工具中执行。
      * **[!UICONTROL CREATE_USERS]**:允许用户使用呼叫创建新 [!DNL API] 用户。
      * **[!UICONTROL DELETE_USERS]**:允许用户使用呼叫删除现有 [!DNL API] 用户。
      * **[!UICONTROL EDIT_USERS]**:允许用户使用呼叫编辑现有 [!DNL API] 用户。
      * **[!UICONTROL VIEW_USERS]**:允许用户使用呼叫查看Audience Manager配置中的其他 [!DNL API] 用户。
      * **[!UICONTROL CREATE_PARTNERS]**:允许用户使用呼叫创建Audience manager合 [!DNL API] 作伙伴。
      * **[!UICONTROL DELETE_PARTNERS]**:允许用户使用呼叫删除Audience manager合作 [!DNL API] 伙伴。
      * **[!UICONTROL EDIT_PARTNERS]**:允许用户使用呼叫编辑Audience manager合作 [!DNL API] 伙伴。
      * **[!UICONTROL VIEW_PARNTERS]**:允许用户使用呼叫查看Audience manager合作 [!DNL API] 伙伴。
   * **** 状态：选择 **[!UICONTROL Active]** 此选项可使此用户成为已激活的Audience manager用户。
3. 单击 **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

使用Audience Manager [!UICONTROL Integration Users] 工具中的页 [!UICONTROL Admin] 面删除现有用户。

<!-- t_delete_user.xml -->

>[!NOTE]
>
>要创建新用 **[!UICONTROL DELETE_USER]** 户，您必须具有角色。

1. 单击 **[!UICONTROL Integration Users]**.
2. 单击 ![](assets/icon_delete.png) 所需 **[!UICONTROL Actions]** 用户的列。
3. Click **[!UICONTROL OK]** to confirm the deletion.