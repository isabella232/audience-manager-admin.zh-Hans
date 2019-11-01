---
description: 参与Adobe Experience Cloud Device Co-op的公司可以使用设备图形选项。 如果客户还与第三方设备图形提供商建立了合同关系，并与Audience manager集成，则此部分将显示该设备图形的选项。 这些选项位于公司>公司名称>配置文件>设备图形选项中。
seo-description: 参与Adobe Experience Cloud Device Co-op的公司可以使用设备图形选项。 如果客户还与第三方设备图形提供商建立了合同关系，并与Audience manager集成，则此部分将显示该设备图形的选项。 这些选项位于公司>公司名称>配置文件>设备图形选项中。
seo-title: 公司的设备图选项
title: 公司的设备图选项
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92

---


# 公司的设备图选项 {#device-graph-options-for-companies}

参 [!UICONTROL Device Graph Options] 与该计划的公司可使用 [!DNL Adobe Experience Cloud Device Co-op]。 如果客户还与第三方设备图形提供商建立了合同关系，并与Audience manager集成，则此部分将显示该设备图形的选项。 这些选项位于 [!UICONTROL Companies] &gt;公司名称&gt; [!UICONTROL Profile] &gt; [!UICONTROL Device Graph Options]。

![](assets/adminUIdataSource.png)

此插图为第三方设备图形选项使用通用名称。 在生产中，这些名称来自设备图形提供商，并且可能与此处显示的不同。 例如，选项通 [!DNL LiveRamp] 常（但并不总是）:

* 从 "[!DNL LiveRamp]"
* 包含中间名称(因
* 以“”[!UICONTROL - Household]或“[!UICONTROL -Person]”结尾

## 已定义设备图形选项 {#device-graph-options-defined}

在此处选择的设备图选项显示或隐藏 [!UICONTROL Device Options] 客户在创建 [!DNL Audience Manager] 时可用的选择 [!UICONTROL Profile Merge Rule]。

### 协作设备图 {#co-op-graph}

参与 [Adobe Experience Cloud Device Co-op的客户使用这些选项创建](https://marketing.adobe.com/resources/help/en_US/mcdc/) 含确定 [!UICONTROL Profile Merge Rule] 性和概率数据 [](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)。 通 [!DNL Corporate Provisioning Team] 过后端调用激活和禁用此选 [!DNL API] 项。 不能在中选中或清除这些框 [!DNL Admin UI]。 此外，该等 **[!UICONTROL Co-op Device Graph]** 选项 **[!UICONTROL Company Device Graph]** 与该等选项互斥。 客户可以要求我们激活一个或另一个，但不能同时激活两者。 选中此选项后，将显 **[!UICONTROL Co-op Device Graph]** 示设置中 [!UICONTROL Device Options] 的控件 [!UICONTROL Profile Merge Rule]。

![](assets/adminUI1.png)

### 公司设备图 {#company-graph}

此选项适用于在 [!DNL Analytics] 其报表包中使用 [!UICONTROL People] 该量度的 [!DNL Analytics] 客户。 通 [!DNL Corporate Provisioning Team] 过后端调用激活和禁用此选 [!DNL API] 项。 不能在中选中或清除这些框 [!DNL Admin UI]。 此外，该等 **[!UICONTROL Company Device Graph]** 选项 **[!UICONTROL Co-op Device Graph]** 与该等选项互斥。 客户可以要求我们激活一个或另一个，但不能同时激活两者。 选中后：

* 此设备图形使用属于您所配置公司的确定性数据（无概率数据）。
* [!DNL Audience Manager] 自动创建名 [!UICONTROL Data Source] 为合作 `*`伙伴名称`*-Company Device Graph-Person`。 在详细 [!UICONTROL Data Source] 信息页面中， [!DNL Audience Manager] 客户可以更改合作伙伴名称、说明，并将“数据导 [](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) 出控件”应用到此数据源。
* [!DNL Audience Manager] 客 *户在* “”部分中看不到 [!UICONTROL Device Options] 新设置 [!UICONTROL Profile Merge Rule]。

### LiveRamp设备图（个人或家庭） {#liveramp-device-graph}

当合作伙伴创建并选 [!DNL Admin UI] 择和／或时，这些复 [!UICONTROL Data Source] 选框在 **[!UICONTROL Use as an Authenticated Profile]** 中启用 **[!UICONTROL Use as a Device Graph]**。 这些设置的名称由第三方设备图形提供者(例如， [!DNL LiveRamp]、 [!DNL TapAd]等)确定。 如果选中此项，则表示您所配置的公司将使用这些设备图形提供的数据。

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [已定义配置文件合并规则选项](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [数据源设置和菜单选项](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

