---
description: 参与Adobe Experience Cloud设备合作社的公司可以使用设备图形选项。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于公司>公司名称>用户档案>设备图形选项中。
seo-description: 参与Adobe Experience Cloud设备合作社的公司可以使用设备图形选项。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于公司>公司名称>用户档案>设备图形选项中。
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

[!UICONTROL Device Graph Options]适用于参与[!DNL Adobe Experience Cloud Device Co-op]的公司。 如果客户还与与Audience Manager集成的第三方设备图形提供商有合同关系，则本节将显示该设备图形的选项。 这些选项位于[!UICONTROL Companies] >公司名称> [!UICONTROL Profile] > [!UICONTROL Device Graph Options]中。

![](assets/adminUIdataSource.png)

此插图为第三方设备图形选项使用通用名称。 在生产中，这些名称来自设备图形提供商，可能因此处显示的内容而异。 例如，[!DNL LiveRamp]选项通常（但不总是）:

* 从 &quot;[!DNL LiveRamp]&quot;
* 包含中间名称，该名称会有所不同
* 以“[!UICONTROL - Household]”或“[!UICONTROL -Person]”结尾

## 已定义设备图形选项{#device-graph-options-defined}

您在此处选择的设备图选项显示或隐藏[!DNL Audience Manager]客户在创建[!UICONTROL Profile Merge Rule]时可用的[!UICONTROL Device Options]选项。

### 协作设备图{#co-op-graph}

参与[Adobe Experience Cloud设备合作社](https://marketing.adobe.com/resources/help/en_US/mcdc/)的客户使用这些选项创建[!UICONTROL Profile Merge Rule]，其中包含[确定性和概率数据](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)。 [!DNL Corporate Provisioning Team]通过后端[!DNL API]调用激活和取消激活此选项。 不能在[!DNL Admin UI]中选中或清除这些框。 此外，**[!UICONTROL Co-op Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Company Device Graph]**&#x200B;选项互斥。 客户可以要求我们激活一个或另一个，但不能同时激活两个。 选中后，将显示[!UICONTROL Profile Merge Rule]的[!UICONTROL Device Options]设置中的&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;控件。

![](assets/adminUI1.png)

### 公司设备图{#company-graph}

此选项针对在[!DNL Analytics]报表包中使用[!UICONTROL People]度量的[!DNL Analytics]客户。 [!DNL Corporate Provisioning Team]通过后端[!DNL API]调用激活和取消激活此选项。 不能在[!DNL Admin UI]中选中或清除这些框。 此外，**[!UICONTROL Company Device Graph]**&#x200B;和&#x200B;**[!UICONTROL Co-op Device Graph]**&#x200B;选项互斥。 客户可以要求我们激活一个或另一个，但不能同时激活两个。 选中后：

* 此设备图形使用属于您正在配置的公司的确定性数据（无概率数据）。
* [!DNL Audience Manager] 自动创建名 [!UICONTROL Data Source] 为 `*`伙伴名称`*-Company Device Graph-Person`。在[!UICONTROL Data Source]详细信息页中，[!DNL Audience Manager]客户可以更改合作伙伴名称、说明，并将[数据导出控件](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html)应用到此数据源。
* [!DNL Audience Manager] 客 *户* 在部分中看不到 [!UICONTROL Device Options] 新设置 [!UICONTROL Profile Merge Rule]。

### LiveRamp设备图（人或家）{#liveramp-device-graph}

当合作伙伴创建[!UICONTROL Data Source]并选择&#x200B;**[!UICONTROL Use as an Authenticated Profile]**&#x200B;和／或&#x200B;**[!UICONTROL Use as a Device Graph]**&#x200B;时，这些复选框会在[!DNL Admin UI]中启用。 这些设置的名称由第三方设备图形提供程序（如[!DNL LiveRamp]、[!DNL TapAd]等）确定。 选中后，这意味着您正在配置的公司将使用这些设备图形提供的数据。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [定义的配置文件合并规则选项](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [数据源设置和菜单选项](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

