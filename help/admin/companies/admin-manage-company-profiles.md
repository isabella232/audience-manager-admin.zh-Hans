---
description: 使用Audience Manager管理工具中的公司页面创建新公司。
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: 创建公司配置文件
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 4%

---

# 创建公司配置文件 {#create-a-company-profile}

使用Audience Manager管理工具中的[!UICONTROL Companies]页面创建新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>要创建新公司，您必须具有&#x200B;**[!UICONTROL DEXADMIN]**&#x200B;角色。

1. 单击 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填写以下字段：

   * **[!UICONTROL Name]**:（必需）指定公司名称。
   * **[!UICONTROL Description]**:（必需）提供有关公司的描述性信息，如行业或其全名。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。您输入的文本将显示为事件调用的子域。 无法更改。 它必须是包含[!DNL URL]有效字符的字符串。

      例如，如果您的公司名为[!DNL AcmeCorp]，则子域将为[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子域。 在上一个示例中，如果您公司[!UICONTROL DCS]中的[!DNL URL]全部内容为[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**:为公司指定所需的阶段：
      * **[!UICONTROL Active]**:指定公司将是活动的Audience Manager客户端。[!UICONTROL Active]帐户是指付费客户，不仅是咨询客户，还包括Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司仅用于演示目的。报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，例如向公司提供免费或 [!DNL POC] 为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。没有帐户类型与任何其他类型互斥。
      * **[!UICONTROL Full AAM]**:指定公司将拥有完整的Adobe Audience Manager帐户，用户将拥有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使 [!UICONTROL Master Marketing Profile] 用([!UICONTROL MMP])功能。[!UICONTROL MMP]允许使用分配给每位访客并供Experience Cloud使用的[!UICONTROL Experience Cloud ID]([!DNL MCID])在Audience Manager之间共享受众。 如果选择此帐户类型，则[!UICONTROL Experience Cloud ID Service]也会自动选择。

         有关更多信息，请参阅[Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager内的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用以使用 [!UICONTROL Experience Cloud Visitor ID Service]。

      [!UICONTROL Experience Cloud Visitor ID Service]可跨多个Experience Cloud解决方案提供通用访客ID。 有关更多信息，请参阅[Experience Cloud访客ID服务用户指南](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司将拥有帐 [!UICONTROL Agency] 户。



1. 单击 **[!UICONTROL Create]**. 按照[编辑公司配置文件](../companies/admin-manage-company-profiles.md#edit-company-profile)中的说明继续操作。

   ![步骤结果](assets/add_company.png)

## 编辑公司配置文件 {#edit-company-profile}

编辑公司的配置文件，包括其名称、描述、子域、生命周期等。

<!-- t_edit_company_profile.xml -->

1. 单击&#x200B;**[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其[!UICONTROL Profile]页面。

   使用[!UICONTROL Search]框或列表底部的分页控件找到所需的公司。 您可以通过单击所需列的标题，按升序或降序对每列进行排序。

   ![步骤结果](assets/profile_company.png)

1. 根据需要编辑字段：

   * **[!UICONTROL Name]**:编辑公司名称。这是必填字段。
   * **[!UICONTROL Description]**:编辑公司的描述。这是必填字段。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。您输入的文本将显示为事件调用的子域。 无法更改。 它必须是包含[!DNL URL]有效字符的字符串。

      例如，如果您的公司名为[!DNL AcmeCorp]，则子域将为[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子域。 在上一个示例中，如果您公司[!UICONTROL DCS]中的[!DNL URL]全部内容为[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])此ID用于将您的公司与Adobe Experience Cloud连接。
   * **[!UICONTROL Lifecyle]**:为公司指定所需的阶段：
      * **[!UICONTROL Active]**:指定公司将是活动的Audience Manager客户端。有效帐户是指付费客户，这不仅是咨询客户，还包括Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司仅用于演示目的。报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，例如向公司提供免费或 [!DNL POC] 为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。没有帐户类型与任何其他类型互斥。
      * **[!UICONTROL Full AAM]**:指定公司将拥有完整的Adobe Audience Manager帐户，用户将拥有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使用主控营销配置文件([!UICONTROL MMP])功能。

         如果选择此帐户类型，则也会自动选择&#x200B;**[!UICONTROL Visitor ID Service]**。
有关更多信息，请参阅[Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager内的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用以使用Experience Cloud访客ID服务。

      Experience Cloud 访客 ID 服务可以跨多个 Experience Cloud 解决方案提供一个通用的访客 ID。有关更多信息，请参阅[Experience CloudID服务用户指南](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)。

   * **[!UICONTROL Agency]**:指定公司将具有代理帐户。
   * **[!UICONTROL Features]**:选择所需的选项：
      * **[!UICONTROL Password Expiration]**:将此公司内的所有用户密码设置为在90天后过期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**:为此公司启用Audience Manager报表。
      * **[!UICONTROL Role Based Access Controls]**:为此公司启用基于角色的访问控制。基于角色的访问控制允许您创建具有不同访问权限的用户组。 然后，这些群组中的个人用户只能访问Audience Manager中的特定功能。


1. 单击 **[!UICONTROL Submit Updates]**.

## 删除公司配置文件 {#delete-company-profile}

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL Companies]页面删除现有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>要删除现有公司，您必须具有[!UICONTROL DEXADMIN]角色。

1. 要删除现有公司，请单击&#x200B;**[!UICONTROL Companies]**。

   ![步骤结果](assets/companies.png)

1. 单击所需公司&#x200B;**[!UICONTROL Actions]**&#x200B;列中的![](assets/icon_delete.png)。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以确认删除。
