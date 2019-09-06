---
description: 使用Audience Manager管理工具中的公司页面创建一个新公司。
seo-description: 使用Audience Manager管理工具中的公司页面创建一个新公司。
seo-title: 创建公司简介
title: 创建公司简介
uuid: 55de18f8-883d-43fe-b37 f-e8805 bb92 f7 a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 创建公司简介 {#create-a-company-profile}

使用Audience Manager管理工具中的 [!UICONTROL Companies] 页面创建一个新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>要创建新公司 **[!UICONTROL DEXADMIN]** ，您必须持有角色。

1. Click **[!UICONTROL Companies]** &gt; **[!UICONTROL Add Company]**.
1. 填写以下字段：

   * **[!UICONTROL Name]**：(必需)指定公司的名称。
   * **[!UICONTROL Description]**：(必需)提供有关公司的描述性信息，如行业或其全名。
   * **[!UICONTROL Subdomain]**：(必需)指定公司的子域。您输入的文本将显示为事件调用的子域。无法更改。它必须是一串 [!DNL URL]有效字符。

      例如，如果您的公司被命名 [!DNL AcmeCorp]，则子域将为 [!DNL acmecorp]。

      Audience Manager使用 [!UICONTROL Data Collection Server]([!UICONTROL DCS])的子域。在上一个示例中，如果您的公司已满 [!DNL URL][!UICONTROL DCS][!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**：为公司指定所需的舞台：
      * **[!UICONTROL Active]**：指定该公司将成为活跃的Audience Manager客户端。[!UICONTROL Active] 帐户是指付费客户，不仅是用于咨询，而且是用于Audience Manager SKU。
      * **[!UICONTROL Demo]**：指定该公司仅用于演示目的。报告数据将自动被隐藏。
      * **[!UICONTROL Prospect]**：指定该公司是潜在Audience Manager客户端，如获得免费 [!DNL POC] 或帐户销售演示的公司。
      * **[!UICONTROL Test]**：指定公司仅用于内部测试目的。
   * **[!UICONTROL Account Types]**：指定此公司的完整帐户类型。没有任何帐户类型与任何其他类型都是互斥的。
      * **[!UICONTROL Full AAM]**：指定公司将拥有完整的Adobe Audience Manager帐户，用户将具有登录访问权限。
      * **[!UICONTROL MMP]**：指定已启用( [!UICONTROL Master Marketing Profile][!UICONTROL MMP])功能的公司。The [!UICONTROL MMP] allows audiences to be shared across the Experience Cloud using an [!UICONTROL Experience Cloud ID] ([!DNL MCID]) that is assigned to every visitor and then used by Audience Manager. 如果您选择此帐户类型，也会自动选择该 [!UICONTROL Experience Cloud ID Service] 帐户类型。

         有关更多信息，请参阅 [受众服务-主营销配置文件](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**：指定该公司是Audience Manager中的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**：指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定已启用该公司 [!UICONTROL Experience Cloud Visitor ID Service]使用。

      提供 [!UICONTROL Experience Cloud Visitor ID Service] 跨Experience Cloud解决方案的通用访客ID。For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**：指定该公司将具有一个 [!UICONTROL Agency] 帐户。



1. 单击 **[!UICONTROL Create]**. 继续使用编辑公司配置文件中 [的说明](../companies/admin-manage-company-profiles.md#edit-company-profile)。

   ![步骤结果](assets/add_company.png)

## 编辑公司简介 {#edit-company-profile}

编辑公司的配置文件，包括其名称、描述、子域、生命周期等。

<!-- t_edit_company_profile.xml -->

1. 单击 **[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。

   使用 [!UICONTROL Search] 列表底部的分页控件或分页控件查找所需的公司。您可以单击所需列的标题，以升序或降序排列每个列。

   ![步骤结果](assets/profile_company.png)

1. 根据需要编辑字段：

   * **[!UICONTROL Name]**：编辑公司名称。这是必填字段。
   * **[!UICONTROL Description]**：编辑公司描述。这是必填字段。
   * **[!UICONTROL Subdomain]**：(必需)指定公司的子域。您输入的文本将显示为事件调用的子域。无法更改。它必须是一串 [!DNL URL]有效字符。

      例如，如果您的公司被命名 [!DNL AcmeCorp]，则子域将为 [!DNL acmecorp]。

      Audience Manager使用 [!UICONTROL Data Collection Server] ([!UICONTROL DCS])的子域。在上一个示例中，如果您的公司已满 [!DNL URL][!UICONTROL DCS][!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**：([!UICONTROL Identity Management System Organization ID])此ID允许您与Adobe Experience Cloud连接您的公司。
   * **[!UICONTROL Lifecyle]**：为公司指定所需的舞台：
      * **[!UICONTROL Active]**：指定该公司将成为活跃的Audience Manager客户端。有效帐户是指付费客户，不仅仅是用于咨询，还包括Audience Manager SKU。
      * **[!UICONTROL Demo]**：指定该公司仅用于演示目的。报告数据将自动被隐藏。
      * **[!UICONTROL Prospect]**：指定该公司是潜在Audience Manager客户端，如获得免费 [!DNL POC] 或帐户销售演示的公司。
      * **[!UICONTROL Test]**：指定公司仅用于内部测试目的。
   * **[!UICONTROL Account Types]**：指定此公司的完整帐户类型。没有任何帐户类型与任何其他类型都是互斥的。
      * **[!UICONTROL Full AAM]**：指定公司将拥有完整的Adobe Audience Manager帐户，用户将具有登录访问权限。
      * **[!UICONTROL MMP]**：指定已启用公司使用主营销配置文件([!UICONTROL MMP])功能。

         如果选择此帐户类型 **[!UICONTROL Visitor ID Service]** ，也会自动选择此类型。
有关更多信息，请参阅 [受众服务-主营销配置文件](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**：指定该公司是Audience Manager中的第三方数据提供商。
   * **[!UICONTROL Targeting Partner]**：指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**：指定已启用该公司以使用Experience Cloud访问者ID服务。

      Experience Cloud 访客 ID 服务可以跨多个 Experience Cloud 解决方案提供一个通用的访客 ID。For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**：指定公司将拥有代理帐户。
   * **[!UICONTROL Features]**：选择所需的选项：
      * **[!UICONTROL Password Expiration]**：设置该公司内的所有用户密码，以在90天后过期以增加Audience Manager安全性。
      * **[!UICONTROL Reporting]**：为此公司启用Audience Manager报告。
      * **[!UICONTROL Role Based Access Controls]**：为此公司启用基于角色的访问控制。基于角色的访问控制允许您创建具有不同访问权限的用户组。这些组中的各个用户随后只能访问Audience Manager中的特定功能。


1. 单击 **[!UICONTROL Submit Updates]**.

## 删除公司配置文件 {#delete-company-profile}

使用Audience [!UICONTROL Companies] Manager [!UICONTROL Admin] 工具中的页面删除现有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必须具有相应的 [!UICONTROL DEXADMIN] 角色才能删除现有的公司。

1. 要删除现有公司，请单击 **[!UICONTROL Companies]**。

   ![步骤结果](assets/companies.png)

1. 单击 ![](assets/icon_delete.png) 所需公司的 **[!UICONTROL Actions]** 列。
1. Click **[!UICONTROL OK]** to confirm the deletion.
