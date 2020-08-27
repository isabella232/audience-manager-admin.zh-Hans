---
description: 使用公司管理工具中的Audience Manager页面创建新公司。
seo-description: 使用公司管理工具中的Audience Manager页面创建新公司。
seo-title: 创建公司配置文件
title: 创建公司配置文件
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 69b733ae869b3dded76f0264e395f0157b445148
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 4%

---


# 创建公司配置文件 {#create-a-company-profile}

使用 [!UICONTROL Companies] Audience Manager管理工具中的页面创建新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必须具 **[!UICONTROL DEXADMIN]** 有角色才能创建新公司。

1. 单击 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填写以下字段：

   * **[!UICONTROL Name]**:（必需）指定公司的名称。
   * **[!UICONTROL Description]**:（必需）提供有关公司的描述性信息，如行业或其全名。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。 您输入的文本显示为事件调用的子域。 无法更改。 它必须是一串有效 [!DNL URL]的字符。

      例如，如果您的公司被命 [!DNL AcmeCorp]名，则子域将被命 [!DNL acmecorp]名。

      Audience Manager将子域用 [!UICONTROL Data Collection Server] 于(DCS)。 在上一个示例中，如果公司的 [!DNL URL] 完整 [!UICONTROL DCS] 值为 [!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**:为公司指定所需的舞台：
      * **[!UICONTROL Active]**:指定公司将是活动Audience Manager客户端。 帐 [!UICONTROL Active] 户是指付费客户，不仅是咨询，还是Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司将仅用于演示目的。 报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，如为公司提供免费的或 [!DNL POC] 为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。 任何帐户类型与任何其他类型不相容。
      * **[!UICONTROL Full AAM]**:指定公司将具有完整的Adobe Audience Manager帐户，并且用户将具有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使用( [!UICONTROL Master Marketing Profile] )[!UICONTROL MMP]功能。 The [!UICONTROL MMP] allows audiences to be shared across the Experience Cloud using an [!UICONTROL Experience Cloud ID] ([!DNL MCID]) that is assigned to every visitor and then used by Audience Manager. 如果您选择此帐户类型，则 [!UICONTROL Experience Cloud ID Service] 也会自动选择。

         有关详细信息，请参 [阅受众服务-主控营销用户档案](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager中的第三方数据提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用以使用 [!UICONTROL Experience Cloud Visitor ID Service]。

      它提 [!UICONTROL Experience Cloud Visitor ID Service] 供跨访客解决方案的通用Experience CloudID。 For more information, see the [Experience Cloud Visitor ID Service user guide](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**:指定公司将具有帐 [!UICONTROL Agency] 户。



1. 单击 **[!UICONTROL Create]**. 继续执行编辑 [公司用户档案中的说明](../companies/admin-manage-company-profiles.md#edit-company-profile)。

   ![步骤结果](assets/add_company.png)

## 编辑公司配置文件{#edit-company-profile}

编辑公司的用户档案，包括其名称、描述、子域、生命周期等。

<!-- t_edit_company_profile.xml -->

1. 单 **[!UICONTROL Companies]**&#x200B;击，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。

   使用 [!UICONTROL Search] 列表底部的框或分页控件找到所需的公司。 单击所需列的标题，可以按升序或降序对每列进行排序。

   ![步骤结果](assets/profile_company.png)

1. 根据需要编辑字段：

   * **[!UICONTROL Name]**:编辑公司的名称。 这是必填字段。
   * **[!UICONTROL Description]**:编辑公司的描述。 这是必填字段。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。 您输入的文本显示为事件调用的子域。 无法更改。 它必须是一串有效 [!DNL URL]的字符。

      例如，如果您的公司被命 [!DNL AcmeCorp]名，则子域将被命 [!DNL acmecorp]名。

      Audience Manager将子域用 [!UICONTROL Data Collection Server] 于(DCS)。 在上一个示例中，如果公司的 [!DNL URL] 完整 [!UICONTROL DCS] 值为 [!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])此ID可让您将公司与Adobe Experience Cloud连接。
   * **[!UICONTROL Lifecyle]**:为公司指定所需的舞台：
      * **[!UICONTROL Active]**:指定公司将是活动Audience Manager客户端。 有效帐户是指付费客户，不仅用于咨询，还用于Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司将仅用于演示目的。 报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，如为公司提供免费的或 [!DNL POC] 为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。 任何帐户类型与任何其他类型不相容。
      * **[!UICONTROL Full AAM]**:指定公司将具有完整的Adobe Audience Manager帐户，并且用户将具有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使用主控营销用户档案([!UICONTROL MMP])功能。

         如果您选择此帐户类型， **[!UICONTROL Visitor ID Service]** 则也会自动选择。
有关详细信息，请参 [阅受众服务-主控营销用户档案](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager中的第三方数据提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用Experience Cloud访客ID服务。

      Experience Cloud 访客 ID 服务可以跨多个 Experience Cloud 解决方案提供一个通用的访客 ID。For more information, see the [Experience Cloud Visitor ID Service user guide](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**:指定公司将具有代理帐户。
   * **[!UICONTROL Features]**:选择所需选项：
      * **[!UICONTROL Password Expiration]**:设置此公司内的所有用户密码在90天后过期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**:启用此Audience Manager的报告。
      * **[!UICONTROL Role Based Access Controls]**:为此访问控制启用基于角色的公司。 基于角色的访问控制允许您创建具有不同访问权限的用户组。 然后，这些组中的各个用户只能访问Audience Manager中的特定功能。


1. 单击 **[!UICONTROL Submit Updates]**.

## 删除公司用户档案 {#delete-company-profile}

使用Audience Manager [!UICONTROL Companies] 工具中的页面 [!UICONTROL Admin] 删除现有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必须具有 [!UICONTROL DEXADMIN] 角色才能删除现有公司。

1. 要删除现有公司，请单击 **[!UICONTROL Companies]**。

   ![步骤结果](assets/companies.png)

1. 单 ![](assets/icon_delete.png) 击所 **[!UICONTROL Actions]** 需公司的列。
1. Click **[!UICONTROL OK]** to confirm the deletion.
