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

使用Audience Manager管理工具中的[!UICONTROL Companies]页面创建新公司。

<!-- t_create_company.xml -->

>[!NOTE]
>
>您必须具有&#x200B;**[!UICONTROL DEXADMIN]**&#x200B;角色才能创建新公司。

1. 单击 **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. 填写以下字段：

   * **[!UICONTROL Name]**:（必需）指定公司的名称。
   * **[!UICONTROL Description]**:（必需）提供有关公司的描述性信息，如行业或其全名。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。您输入的文本显示为事件调用的子域。 无法更改。 它必须是[!DNL URL]-valid字符的字符串。

      例如，如果您的公司名为[!DNL AcmeCorp]，则子域将为[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子域。 在上一个示例中，如果您的公司在[!UICONTROL DCS]中的完整[!DNL URL]将为[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL Lifecyle]**:为公司指定所需的舞台：
      * **[!UICONTROL Active]**:指定公司将是活动Audience Manager客户端。[!UICONTROL Active]帐户是指付费客户，不仅是咨询客户，还包括Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司将仅用于演示目的。报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，如向公司提供免费的 [!DNL POC] 或为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。任何帐户类型与任何其他类型不相容。
      * **[!UICONTROL Full AAM]**:指定公司将具有完整的Adobe Audience Manager帐户，并且用户将具有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使用 [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])功能。[!UICONTROL MMP]允许使用[!UICONTROL Experience Cloud ID]([!DNL MCID])在Experience Cloud之间共享受众，该&lt;a1/>(&lt;a2/>)分配给每个访客，然后由Audience Manager使用。 如果选择此帐户类型，[!UICONTROL Experience Cloud ID Service]也会自动选中。

         有关详细信息，请参阅[受众服务-主控营销用户档案](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager中的第三方数据提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用以使用 [!UICONTROL Experience Cloud Visitor ID Service]。

      [!UICONTROL Experience Cloud Visitor ID Service]提供跨访客解决方案的通用Experience CloudID。 有关详细信息，请参阅[Experience Cloud访客ID服务用户指南](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html)。

   * **[!UICONTROL Agency]**:指定公司将具有帐 [!UICONTROL Agency] 户。



1. 单击 **[!UICONTROL Create]**. 继续使用[编辑公司用户档案](../companies/admin-manage-company-profiles.md#edit-company-profile)中的说明。

   ![步骤结果](assets/add_company.png)

## 编辑公司配置文件{#edit-company-profile}

编辑公司的用户档案，包括其名称、描述、子域、生命周期等。

<!-- t_edit_company_profile.xml -->

1. 单击&#x200B;**[!UICONTROL Companies]**，找到并单击所需的公司以显示其[!UICONTROL Profile]页。

   使用[!UICONTROL Search]框或列表底部的分页控件找到所需的公司。 单击所需列的标题，可以按升序或降序对每列进行排序。

   ![步骤结果](assets/profile_company.png)

1. 根据需要编辑字段：

   * **[!UICONTROL Name]**:编辑公司的名称。这是必填字段。
   * **[!UICONTROL Description]**:编辑公司的描述。这是必填字段。
   * **[!UICONTROL Subdomain]**:（必需）指定公司的子域。您输入的文本显示为事件调用的子域。 无法更改。 它必须是[!DNL URL]-valid字符的字符串。

      例如，如果您的公司名为[!DNL AcmeCorp]，则子域将为[!DNL acmecorp]。

      Audience Manager使用[!UICONTROL Data Collection Server](DCS)的子域。 在上一个示例中，如果您的公司在[!UICONTROL DCS]中的完整[!DNL URL]将为[!DNL acmecorp.demdex.net]。

   * **[!UICONTROL imsOrgld]**:([!UICONTROL Identity Management System Organization ID])此ID可让您将公司与Adobe Experience Cloud连接。
   * **[!UICONTROL Lifecyle]**:为公司指定所需的舞台：
      * **[!UICONTROL Active]**:指定公司将是活动Audience Manager客户端。有效帐户是指付费客户，不仅用于咨询，还用于Audience ManagerSKU。
      * **[!UICONTROL Demo]**:指定公司将仅用于演示目的。报告数据将自动伪造。
      * **[!UICONTROL Prospect]**:指定公司是潜在的Audience Manager客户，如向公司提供免费的 [!DNL POC] 或为销售演示设置帐户。
      * **[!UICONTROL Test]**:指定公司仅用于内部测试。
   * **[!UICONTROL Account Types]**:为此公司指定完整的帐户类型集。任何帐户类型与任何其他类型不相容。
      * **[!UICONTROL Full AAM]**:指定公司将具有完整的Adobe Audience Manager帐户，并且用户将具有登录访问权限。
      * **[!UICONTROL MMP]**:指定公司已启用以使用主控营销用户档案([!UICONTROL MMP])功能。

         如果选择此帐户类型，**[!UICONTROL Visitor ID Service]**也会自动选中。
有关详细信息，请参阅[受众服务-主控营销用户档案](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)。
   * **[!UICONTROL Data Source]**:指定公司是Audience Manager中的第三方数据提供者。
   * **[!UICONTROL Targeting Partner]**:指定公司充当Audience Manager客户的定位平台。
   * **[!UICONTROL Visitor ID Service]**:指定公司已启用Experience Cloud访客ID服务。

      Experience Cloud 访客 ID 服务可以跨多个 Experience Cloud 解决方案提供一个通用的访客 ID。有关详细信息，请参阅[Experience Cloud访客ID服务用户指南](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html)。

   * **[!UICONTROL Agency]**:指定公司将具有代理帐户。
   * **[!UICONTROL Features]**:选择所需选项：
      * **[!UICONTROL Password Expiration]**:设置此公司内的所有用户密码在90天后过期，以提高Audience Manager安全性。
      * **[!UICONTROL Reporting]**:启用此Audience Manager的报告。
      * **[!UICONTROL Role Based Access Controls]**:为此访问控制启用基于角色的公司。基于角色的访问控制允许您创建具有不同访问权限的用户组。 然后，这些组中的各个用户只能访问Audience Manager中的特定功能。


1. 单击 **[!UICONTROL Submit Updates]**.

## 删除公司用户档案{#delete-company-profile}

使用Audience Manager[!UICONTROL Admin]工具中的[!UICONTROL Companies]页可删除现有公司。

<!-- t_delete_company.xml -->

>[!NOTE]
>
>您必须具有[!UICONTROL DEXADMIN]角色才能删除现有公司。

1. 要删除现有公司，请单击&#x200B;**[!UICONTROL Companies]**。

   ![步骤结果](assets/companies.png)

1. 单击所需公司的&#x200B;**[!UICONTROL Actions]**&#x200B;列中的![](assets/icon_delete.png)。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以确认删除。
