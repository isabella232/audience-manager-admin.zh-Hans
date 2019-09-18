---
description: 创建、编辑和删除Audience manager目标。
seo-description: 创建、编辑和删除Audience manager目标。
seo-title: ' 管理公司目标'
title: ' 管理公司目标'
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 管理公司目标 {#manage-company-destinations}

创建、编辑和删除Audience manager目标。

<!-- t_company_destinations.xml -->

有关详细信息，请参 [阅Audience](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) *Manager用户指南中的目标*。

## 创建或编辑公司目标 {#create-edit-company-destinations}

滚动查看各节，了解有关如何创建新目标或编辑现有目标 [!DNL Audience Manager] 的分步说明。

<!-- create-edit-company-destinations.xml -->

在设置目 [标之前，请访问Experience cloud合作伙伴集成页面](https://wiki.corp.adobe.com/x/mPIMPw) 。 该页面包含您需要填写的每个合作伙伴集成的特 [!DNL Audience Manager] 定信息。

如果您的客户希望将 [!DNL Adobe Media Optimizer] 其用作中的目 [!DNL Audience Manager] 标，您需要在中设置此设置 [!DNL Adobe Media Optimizer]。

## Navigate to the Destinations Tab {#navigate-destinations}

1. 单 **[!UICONTROL Companies]**&#x200B;击，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。 您可以使用列 [!UICONTROL Search] 表底部的框或分页控件来查找所需的公司。 您可以通过单击所需列的标题，按升序或降序对每列进行排序。
1. Click the **[!UICONTROL Destinations]** tab.
1. 要创建新目标，请单击 **[!UICONTROL Add Destination]**。 To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## 基本设置 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** :（必需）指定此目标的名称。
* **[!UICONTROL Description]** :指定有关此目标的描述性信息。
* **[!UICONTROL Type]** :（必需）选择所需的目标类型：
   * **[!UICONTROL Bulk ID]**:在不同平台之间同步ID。
   * **[!UICONTROL Bulk Trait]**:将特征信息批量发送到不同的平台。
   * **[!UICONTROL Bulk Segment]**:将细分信息批量发送到不同的平台。
   * **[!UICONTROL S2S]**:使用服务器到服务器目标向不同平台发送实时和批量数据。
* **[!UICONTROL Auto-Fill Destination Mapping]** :(仅 [!UICONTROL S2S] 限)选择一个选项：
   * **[!UICONTROL Segment ID]** :如果选择此设置，则目标值映射将填充区段 [!DNL Audience Manager] ID。
   * **[!UICONTROL Integration Code Value]** :如果选择此设置，则目标值映射将填充区段集 [!DNL Audience Manager] 成代码。
* **[!UICONTROL User ID Key]** :（必需）从下拉列表中选择此目标的所需用户ID密钥。

此ID用作主数据源ID。 这决定了文件中的用户ID超出范围。

>[!NOTE]
>
>对于目 [!UICONTROL Bulk ID] 标类型，您不能使用 [!DNL Audience Manager] 或 [!UICONTROL User ID][!DNL Adobe Experience Cloud] ID。

如果数据源ID( [!UICONTROL DPID])未显示在下拉列表中，则必须在“数据源设置”页面的 **[!UICONTROL Outbound]** 数据源级别选中该 [复选框](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)。

* **[!UICONTROL Target Data Source]** :（必需）从下拉列表中选择此目标的所需数据源。 该设置允许标记出界数据，这允许引入到客户端的单独系统中。
* **[!UICONTROL Foreign Account ID]** :指定此目标的外国帐户ID。 这是接收者系统中对这个无界数据的标识值。
* **[!UICONTROL Outbound Sample Rate Denominator]** :当返回的数据总量未知时，使用此设置只返回样本量的数据，而不是完全量的数据。 在此调整数字以表示数据的一部分（例如，值“100”返回常规数据量的1/100，值“10”返回常规数据量的1/10）。 默认值为“1”，它返回所有数据。

## 实时数据（针对S2S目标） {#realtime-s2s}

如果要创建目 [!UICONTROL S2S] 标，请填写以下字段：

**[!UICONTROL Servers]**:为此目标选 `HTTP` 择所需的服务器。
**[!UICONTROL Format]**:从下拉列表中选择此目标的所需格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>仅可 [!DNL S2S] 使用屏幕上的“关闭”/“开 [!UICONTROL Realtime] 启” [!UICONTROL Batch] 滑块启用或禁用目标。 不能同时禁用这两个选项。

## 批量数据 {#batch-data}

对于 [!UICONTROL Bulk ID]或 [!UICONTROL Bulk Trait] 目 [!UICONTROL Bulk Segment] 标，请填写以下字段：

* **[!UICONTROL Protocol]**:（必需）从下拉列表中选择此目标的所需协议：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必需）从下拉列表中为此目标选择所需的服务器。
* **[!UICONTROL Format]**:（必需）从下拉列表中选择此目标的所需格式：或文 [!DNL HTTP] 件类型，具体取决于您选择的上述协议。
* **[!UICONTROL Sync Type]**:（必需）为此目标选择所需的同步类型。 这表示客户端希望包括在出站订单中的用户活动级别。 选择 **[!UICONTROL Customer]** 客户是否只对从其资产分析细分资格感兴趣。 选择 **[!UICONTROL Platform]** 是否要包括来自所有客户的场外活动的细分 [!DNL Audience Manager] 资格。
* **[!UICONTROL Customer]**:文件包含的活动用户，在所选时间段内，这些活动用户仅在客户端的属性(与客户端的属性关联 [!UICONTROL PID])上具有至少1个特征。 客户应使用此选项将实时细 *分资格推向* 目标。
* **[!UICONTROL Platform]**:文件包含在选定时间段内所有客户端属性（与所有客户端PID关联）的任意位置具有至少1个实时交互（无论是ID同步还是特征实现）的活动用户。 [!DNL Audience Manager] 客户应使用此选项将其总细分资格 *推向* 目标。
* **[!UICONTROL Lifetime]**:文件包含自目标创建以来在所有客 [!DNL Audience Manager] 户端属性中的任意位置看到的活动用户。
* **[!UICONTROL Sync Type Lookback Period]**:如果选择或， [!UICONTROL Customer] 请 [!UICONTROL Platform]选择一个时间段。 文件包含选定时间段内的活动用户。
接下来，选择订单类型。 这表示每个与合作伙伴的出站集成的频率和范围。 在增量订单和完整订单之间进行选择。
* **[!UICONTROL Incremental Scheduled Run]**:每次运行时， [!DNL Audience Manager] 将仅将自上一个出站订单起合格的净新用户出站。 选择要执行增量同步进 [!DNL Audience Manager] 程的所需时间段。 例如，您可以每24小时、每7天、每30天或从不进行选择。

>[!NOTE] {importance="high"}
>
>第一个增量订单等同于完整订单，因为之前从未向目标发送过任何用户。

* **[!UICONTROL Full Sync Scheduled Run]**:每次运行时， [!DNL Audience Manager] 都会将目标首次设置后的所有活动用户出站。 选择要用于执行完全同 [!DNL Audience Manager] 步进程的所需计划。 例如，您可以每24小时、每7天、每30天或从不进行选择。

>[!NOTE] {importance="high"}
>
>我们建议使用增量同步比使用完全同步更频繁。 增量同步仅发送包含新特征实现或ID同步的文件。 完全同步发送所有文件，无论这些文件是否包含新实现或ID同步。 仅当客户 [!UICONTROL Full Sync Scheduled Run] 端需要所有用户的完整副本时使用配置，以减少出站数据量。

## 配置数据源 {#configure-data-sources}

对于 [!UICONTROL Bulk ID]或 [!UICONTROL Bulk Trait] 目 [!UICONTROL Bulk Segment] 标，请填写以下字段。 这些设置允许您根据所选的类型发送与数据源关联的所有数据（特征、区段或ID）。

* **[!UICONTROL All Unrestricted First Party Data]**:选择以使用所有第一方数据源。 如果选择此选项，则会 [!UICONTROL Available Data Sources] 禁用这些选项。
* **[!UICONTROL Available Data Sources]**:使用箭头在和框之间移动数 **[!UICONTROL Available Data Sources]** 据 **[!UICONTROL In File Data Sources]** 源。

## 保存并完成 {#save-and-finalize}

在填 **[!UICONTROL Save]** 写所有必填字段后，按钮即被激活。 单击 **[!UICONTROL Save]** 以完成创建目标流程。

## 删除公司目标 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要删除目标，请执行以下操作：

1. 单击 **[!UICONTROL Companies]**、找到并单击所需的公司，然后单击选 **[!UICONTROL Destinations]** 项卡。
1. 单击 ![](assets/icon_delete.png) 所需目 **[!UICONTROL Actions]** 标的列中的。
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>如果目标的区段已映射到该目标，则无法删除该目标。