---
description: 参与Adobe Experience Cloud设备合作计划的公司可以使用设备图形选项。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于公司>公司名称>用户档案>设备图形选项中。
seo-description: 参与Adobe Experience Cloud设备合作计划的公司可以使用设备图形选项。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于公司>公司名称>用户档案>设备图形选项中。
seo-title: 适用于公司的设备图选项
title: 适用于公司的设备图选项
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 4%

---


# 适用于公司的设备图选项 {#device-graph-options-for-companies}

参 [!UICONTROL Device Graph Options] 与该活动的公司可以使用 [!DNL Adobe Experience Cloud Device Co-op]。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于 [!UICONTROL Companies] >公司名称> [!UICONTROL Profile] > [!UICONTROL Device Graph Options]。

![](assets/adminUIdataSource.png)

此插图为第三方设备图形选项使用通用名称。 在生产中，这些名称来自设备图形提供商，可能因此处显示的内容而异。 例如，通常 [!DNL LiveRamp] （但不总是）有以下选项：

* 从 &quot;[!DNL LiveRamp]&quot;
* 包含中间名称，该名称会有所不同
* 以“”[!UICONTROL - Household]或“[!UICONTROL -Person]”结尾

## 已定义设备图形选项 {#device-graph-options-defined}

您在此处选择的设备图形选项显示或隐 [!UICONTROL Device Options] 藏客户在创建 [!DNL Audience Manager] 时可用的选项 [!UICONTROL Profile Merge Rule]。

### 协作设备图 {#co-op-graph}

参与Adobe Experience Cloud Device Co- [op的客户可使用这些选项](https://marketing.adobe.com/resources/help/en_US/mcdc/) ，创建包含确定 [!UICONTROL Profile Merge Rule] 性和概 [率性数据的数据](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)。 通 [!DNL Corporate Provisioning Team] 过后端调用激活和停用此选 [!DNL API] 项。 不能在中选中或清除这些框 [!DNL Admin UI]。 此外，这些 **[!UICONTROL Co-op Device Graph]** 选项 **[!UICONTROL Company Device Graph]** 和选项是互斥的。 客户可以要求我们激活一个或另一个，但不能同时激活两个。 选中后，它将显 **[!UICONTROL Co-op Device Graph]** 示设置中 [!UICONTROL Device Options] 的控件 [!UICONTROL Profile Merge Rule]。

![](assets/adminUI1.png)

### 公司设备图 {#company-graph}

此选项针对在 [!DNL Analytics] 其报表包中 [!UICONTROL People] 使用该度 [!DNL Analytics] 量的客户。 通 [!DNL Corporate Provisioning Team] 过后端调用激活和停用此选 [!DNL API] 项。 不能在中选中或清除这些框 [!DNL Admin UI]。 此外，这些 **[!UICONTROL Company Device Graph]** 选项 **[!UICONTROL Co-op Device Graph]** 和选项是互斥的。 客户可以要求我们激活一个或另一个，但不能同时激活两个。 选中后：

* 此设备图形使用属于您正在配置的公司的确定性数据（无概率数据）。
* [!DNL Audience Manager] 自动创建名 [!UICONTROL Data Source] 为“ `*`合作伙伴名称`*-Company Device Graph-Person`”。 在详细 [!UICONTROL Data Source] 信息页面中， [!DNL Audience Manager] 客户可以更改合作伙伴名称、说明，并将数 [据导出控制应](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) 用到此数据源。
* [!DNL Audience Manager] 客户 *在* “”部分中看不到 [!UICONTROL Device Options] 新设置 [!UICONTROL Profile Merge Rule]。

### LiveRamp设备图（人或家） {#liveramp-device-graph}

当合作伙伴创建并选 [!DNL Admin UI] 择和／或时， [!UICONTROL Data Source] 这些复选框 **[!UICONTROL Use as an Authenticated Profile]** 在中启用 **[!UICONTROL Use as a Device Graph]**。 这些设置的名称由第三方设备图形提供者(如 [!DNL LiveRamp], [!DNL TapAd]等)确定。 选中后，这意味着您正在配置的公司将使用这些设备图形提供的数据。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定义的配置文件合并规则选项](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [数据源设置和菜单选项](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

