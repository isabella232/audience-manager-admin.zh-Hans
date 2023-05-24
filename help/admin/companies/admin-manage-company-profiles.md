---
description: 使用“Audience Manager管理”工具中的“公司”页可创建新公司。
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

使用 [!UICONTROL Companies] Audience Manager页面，以创建新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必须拥有 **[!UICONTROL DEXADMIN]** 角色以创建新公司。

1. 单击 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填写以下字段：

   * **[!UICONTROL Name]**：（必需）指定公司的名称。
   * **[!UICONTROL Description]**：（必需）提供公司的描述性信息，如行业或其全名。
   * **[!UICONTROL Subdomain]**：（必需）指定公司的子域。 您输入的文本将显示为事件调用的子域。 无法更改。 它必须是字符串 [!DNL URL] — 有效字符。

      例如，如果贵公司名为 [!DNL AcmeCorp]，则子域将为 [!DNL acmecorp].

      Audience Manager将子域用于 [!UICONTROL Data Collection Server] (DCS)。 在上一个示例中，如果您的公司已满 [!DNL URL] 在 [!UICONTROL DCS] 将为 [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**：为公司指定所需的阶段：
      * **[!UICONTROL Active]**：指定公司将是一个活动的Audience Manager客户端。 An [!UICONTROL Active] account是指付费客户，不仅是为了咨询，也是为了提供Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司仅用于演示目的。 报表数据将被自动伪造。
      * **[!UICONTROL Prospect]**：指定该公司是潜在的Audience Manager客户，例如获得免费服务的公司 [!DNL POC] 或销售演示的帐户设置。
      * **[!UICONTROL Test]**：指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**：指定此公司的完整帐户类型集。 没有帐户类型与任何其他类型互斥。
      * **[!UICONTROL Full AAM]**：指定公司将拥有完整的Adobe Audience Manager帐户，并且用户将拥有登录访问权限。
      * **[!UICONTROL MMP]**：指定已允许公司使用 [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])功能。 此 [!UICONTROL MMP] 允许使用在Experience Cloud间共享受众 [!UICONTROL Experience Cloud ID] ([!DNL MCID])，这些资源会分配给每位访客，然后由Audience Manager使用。 如果选择此帐户类型，则 [!UICONTROL Experience Cloud ID Service] 也会自动选中。

         有关更多信息，请参阅 [Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**：指定该公司是Audience Manager中的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**：指定公司用作Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定已允许公司使用 [!UICONTROL Experience Cloud Visitor ID Service].

      此 [!UICONTROL Experience Cloud Visitor ID Service] 提供了跨Experience Cloud解决方案的通用访客ID。 欲了解更多信息，请参见 [Experience Cloud访客ID服务用户指南](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**：指定公司将拥有 [!UICONTROL Agency] 帐户。



1. 单击 **[!UICONTROL Create]**. 按照中的说明继续操作 [编辑公司配置文件](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![步骤结果](assets/add_company.png)

## 编辑公司配置文件 {#edit-company-profile}

编辑公司的配置文件，包括其名称、描述、子域、生命周期等。

<!-- t_edit_company_profile.xml -->

1. 单击 **[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。

   使用 [!UICONTROL Search] 框或列表底部的分页控件以查找所需的公司。 您可以通过单击所需列的标题，按升序或降序对每个列进行排序。

   ![步骤结果](assets/profile_company.png)

1. 根据需要编辑字段：

   * **[!UICONTROL Name]**：编辑公司的名称。 这是必填字段。
   * **[!UICONTROL Description]**：编辑公司的描述。 这是必填字段。
   * **[!UICONTROL Subdomain]**：（必需）指定公司的子域。 您输入的文本将显示为事件调用的子域。 无法更改。 它必须是字符串 [!DNL URL] — 有效字符。

      例如，如果贵公司名为 [!DNL AcmeCorp]，则子域将为 [!DNL acmecorp].

      Audience Manager将子域用于 [!UICONTROL Data Collection Server] (DCS)。 在上一个示例中，如果您的公司已满 [!DNL URL] 在 [!UICONTROL DCS] 将为 [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**：([!UICONTROL Identity Management System Organization ID])通过此ID，您可以将公司与Adobe Experience Cloud连接。
   * **[!UICONTROL Lifecyle]**：为公司指定所需的阶段：
      * **[!UICONTROL Active]**：指定公司将是一个活动的Audience Manager客户端。 活动帐户是指付费客户，不仅是为了咨询，而且也是为了提供Audience ManagerSKU。
      * **[!UICONTROL Demo]**：指定公司仅用于演示目的。 报表数据将被自动伪造。
      * **[!UICONTROL Prospect]**：指定该公司是潜在的Audience Manager客户，例如获得免费服务的公司 [!DNL POC] 或销售演示的帐户设置。
      * **[!UICONTROL Test]**：指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**：指定此公司的完整帐户类型集。 没有帐户类型与任何其他类型互斥。
      * **[!UICONTROL Full AAM]**：指定公司将拥有完整的Adobe Audience Manager帐户，并且用户将拥有登录访问权限。
      * **[!UICONTROL MMP]**：指定允许公司使用主控的营销配置文件([!UICONTROL MMP])功能。

         如果您选择此帐户类型， **[!UICONTROL Visitor ID Service]** 也会自动选中。
有关更多信息，请参阅 [Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**：指定该公司是Audience Manager中的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**：指定公司用作Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定允许该公司使用Experience Cloud访客ID服务。

      Experience Cloud 访客 ID 服务可以跨多个 Experience Cloud 解决方案提供一个通用的访客 ID。欲了解更多信息，请参见 [Experience CloudID服务用户指南](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**：指定公司将拥有代理帐户。
   * **[!UICONTROL Features]**：选择所需的选项：
      * **[!UICONTROL Password Expiration]**：将该公司内的所有用户密码设置为在90天后过期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**：为此公司启用Audience Manager报表。
      * **[!UICONTROL Role Based Access Controls]**：为此公司启用基于角色的访问控制。 基于角色的访问控制允许您创建具有不同访问权限的用户组。 之后，这些组中的个人用户只能访问Audience Manager中的特定功能。


1. 单击 **[!UICONTROL Submit Updates]**.

## 删除公司配置文件 {#delete-company-profile}

使用 [!UICONTROL Companies] Audience Manager中的页面 [!UICONTROL Admin] 工具，用于删除现有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必须拥有 [!UICONTROL DEXADMIN] 角色以删除现有公司。

1. 要删除现有公司，请单击 **[!UICONTROL Companies]**.

   ![步骤结果](assets/companies.png)

1. 单击  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 所需公司的列。
1. 单击 **[!UICONTROL OK]** 以确认删除。
