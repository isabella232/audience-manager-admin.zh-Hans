---
description: 设备图选项适用于参与Adobe Experience Cloud设备协作的公司。 如果客户还与与Audience Manager集成的第三方设备图提供商存在合同关系，本节将显示该设备图的选项。 这些选项位于公司>公司名称>配置文件>设备图选项中。
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: 适用于公司的设备图选项
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# 适用于公司的设备图选项 {#device-graph-options-for-companies}

此 [!UICONTROL Device Graph Options] 适用于参与 [!DNL Adobe Experience Cloud Device Co-op]. 如果客户还与与Audience Manager集成的第三方设备图提供商存在合同关系，本节将显示该设备图的选项。 这些选项位于 [!UICONTROL Companies] >公司名称> [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

此图使用第三方设备图选项的通用名称。 在生产环境中，这些名称来自设备图提供商，可能与此处显示的名称不同。 例如， [!DNL LiveRamp] 选项通常（但不总是如此）：

* 从 &quot;[!DNL LiveRamp]&quot;
* 包含各种不同的中间名
* 结尾为&quot;[!UICONTROL - Household]“或”[!UICONTROL -Person]”

## 定义的设备图选项 {#device-graph-options-defined}

您在此处选择的设备图选项会公开或隐藏 [!UICONTROL Device Options] 可供选择的选项 [!DNL Audience Manager] 客户创建 [!UICONTROL Profile Merge Rule].

### 协作设备图 {#co-op-graph}

参与 [Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en) 使用这些选项创建 [!UICONTROL Profile Merge Rule] 替换为 [确定性数据和概率性数据](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en). 此 [!DNL Corporate Provisioning Team] 通过后端激活和停用此选项 [!DNL API] 呼叫。 您无法选中或清除 [!DNL Admin UI]. 此外， **[!UICONTROL Co-op Device Graph]** 和 **[!UICONTROL Company Device Graph]** 选项相互排斥。 客户可以要求我们激活其中一个，但不能同时激活两者。 选中后，将会公开 **[!UICONTROL Co-op Device Graph]** 中的控件 [!UICONTROL Device Options] 设置 [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### 公司设备图 {#company-graph}

此选项用于 [!DNL Analytics] 使用 [!UICONTROL People] 量度 [!DNL Analytics] 报表包。 此 [!DNL Corporate Provisioning Team] 通过后端激活和停用此选项 [!DNL API] 呼叫。 您无法选中或清除 [!DNL Admin UI]. 此外， **[!UICONTROL Company Device Graph]** 和 **[!UICONTROL Co-op Device Graph]** 选项相互排斥。 客户可以要求我们激活其中一个，但不能同时激活两者。 选中后：

* 此设备图使用属于您配置的公司的确定性数据（无概率数据）。
* [!DNL Audience Manager] 自动创建 [!UICONTROL Data Source] 已调用 `*`合作伙伴名称`*-Company Device Graph-Person`. 在 [!UICONTROL Data Source] 详细信息页面， [!DNL Audience Manager] 客户可以更改合作伙伴名称、描述和应用 [数据导出控制](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en) 至此数据源。
* [!DNL Audience Manager] 客户 *不要* 在中查看新设置 [!UICONTROL Device Options] 部分 [!UICONTROL Profile Merge Rule].

### LiveRamp设备图（人员或家庭） {#liveramp-device-graph}

这些复选框在 [!DNL Admin UI] 当合作伙伴创建 [!UICONTROL Data Source] 并选择 **[!UICONTROL Use as an Authenticated Profile]** 和/或 **[!UICONTROL Use as a Device Graph]**. 这些设置的名称由第三方设备图提供商确定(例如， [!DNL LiveRamp]， [!DNL TapAd]、等)。 选中后，这意味着您配置的公司将使用这些设备图提供的数据。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定义的配置文件合并规则选项](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [数据源设置和菜单选项](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)

