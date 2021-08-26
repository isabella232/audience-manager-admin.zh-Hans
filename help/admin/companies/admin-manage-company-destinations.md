---
description: 创建、编辑和删除Audience Manager目标。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 管理公司目标
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# 管理公司目标 {#manage-company-destinations}

创建、编辑和删除Audience Manager目标。

<!-- t_company_destinations.xml -->

有关详细信息，请参阅&#x200B;*Audience Manager用户指南*&#x200B;中的[目标](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html)。

## 创建或编辑公司目标 {#create-edit-company-destinations}

滚动浏览有关如何创建新[!DNL Audience Manager]目标或编辑现有目标的分步说明部分。

<!-- create-edit-company-destinations.xml -->

在设置目标之前，请访问[Experience Cloud合作伙伴集成页面](https://wiki.corp.adobe.com/x/mPIMPw)。 该页面包含您需要填写的每个[!DNL Audience Manager]合作伙伴集成的特定信息。

如果您的客户端希望将[!DNL Adobe Media Optimizer]用作[!DNL Audience Manager]中的目标，则需要在[!DNL Adobe Media Optimizer]中进行设置。

## 导航到目标选项卡 {#navigate-destinations}

1. 单击&#x200B;**[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其[!UICONTROL Profile]页面。 您可以使用[!UICONTROL Search]框或列表底部的分页控件来查找所需的公司。 您可以通过单击所需列的标题，按升序或降序对每列进行排序。
1. 单击&#x200B;**[!UICONTROL Destinations]**&#x200B;选项卡。
1. 要创建新目标，请单击&#x200B;**[!UICONTROL Add Destination]**。 要编辑现有目标，请在&#x200B;**[!UICONTROL Name]**&#x200B;列中单击目标的名称。

## 基本设置 {#basic-settings}

填写&#x200B;**[!UICONTROL Basic Settings]**&#x200B;窗口中的字段。

* **[!UICONTROL Name]:** （必需）指定此目标的名称。
* **[!UICONTROL Description]:** 指定有关此目标的描述性信息。
* **[!UICONTROL Type]:** （必需）选择所需的目标类型：
   * **[!UICONTROL Bulk ID]**:在不同平台之间同步ID。
   * **[!UICONTROL Bulk Trait]**:将特征信息批量发送到不同的平台。
   * **[!UICONTROL Bulk Segment]**:将区段信息批量发送到不同的平台。
   * **[!UICONTROL S2S]**:使用服务器到服务器目标将实时数据和批量数据发送到不同的平台。
* **[!UICONTROL Auto-Fill Destination Mapping]:** (仅 [!UICONTROL S2S] 限)选择一个选项：
   * **[!UICONTROL Segment ID]:** 如果选择此设置，则目标值映射将填充区 [!DNL Audience Manager] 段ID。
   * **[!UICONTROL Integration Code Value]:** 如果选择此设置，则目标值映射将填充区段 [!DNL Audience Manager] 集成代码。
* **[!UICONTROL User ID Key]:** （必需）从下拉列表中为此目标选择所需的用户ID键。

此ID用作主控数据源ID。 这可确定文件中要超出界限的用户ID。

>[!NOTE]
>
>对于[!UICONTROL Bulk ID]目标类型，不能使用[!DNL Audience Manager] [!UICONTROL User ID]或[!DNL Adobe Experience Cloud] ID。

如果您的数据源ID([!UICONTROL DPID])未显示在下拉列表中，则必须在[“数据源设置”页面](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)的数据源级别选中&#x200B;**[!UICONTROL Outbound]**&#x200B;复选框。

* **[!UICONTROL Target Data Source]:** （必需）从下拉列表中为此目标选择所需的数据源。此设置允许标记出界数据，以便将摄取到客户端上的单独系统中。
* **[!UICONTROL Foreign Account ID]:** 指定此目标的外来帐户ID。这是收件人系统中此外界数据的标识值。
* **[!UICONTROL Outbound Sample Rate Denominator]:** 当返回的数据总量未知时，使用此设置只返回一个数据样本量，而不是全部数据量。在此处调整数字以表示数据的一小部分(例如，值“100”返回1/100常规数据量，值“10”返回1/10常规数据量)。 默认值为“1”，返回所有数据。

## 实时数据（用于S2S目标） {#realtime-s2s}

如果要创建[!UICONTROL S2S]目标，请填写以下字段：

**[!UICONTROL Servers]**:为此目标选 `HTTP` 择所需的服务器。**[!UICONTROL Format]**:从下拉列表中为此目标选择所需的格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>仅对于[!DNL S2S]，您可以使用屏幕上的“关闭/打开”滑块启用或禁用[!UICONTROL Realtime]或[!UICONTROL Batch]目标。 不能同时禁用这两个选项。

## 批量数据 {#batch-data}

对于[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目标，请填写以下字段：

* **[!UICONTROL Protocol]**:（必需）从下拉列表中为此目标选择所需的协议：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:（必需）从下拉列表中为此目标选择所需的服务器。
* **[!UICONTROL Format]**:（必需）从下拉列表中为此目标选择所需的格式： [!DNL HTTP] 或文件类型，具体取决于您选择的上述协议。
* **[!UICONTROL Sync Type]**:（必需）为此目标选择所需的同步类型。这表示客户希望在出站订单中包含的用户活动级别。 如果客户只希望分析其属性中的区段资格，请选择&#x200B;**[!UICONTROL Customer]**。 如果希望包含来自所有[!DNL Audience Manager]客户的站外活动的区段资格，请选择&#x200B;**[!UICONTROL Platform]**。
* **[!UICONTROL Customer]**:文件包含的活动用户，在选定时间段内，他们至少仅在客户端属性（与客户端关联）上 [!UICONTROL PID]具有1个特征实现。您的客户应使用此选项将其&#x200B;*实时*&#x200B;区段资格要求发送到目标。
* **[!UICONTROL Platform]**:文件包含在选定时间段内所有客户端属性（与所有客户端PID关联）的任意位置具有至少1次实时交互(无论是ID [!DNL Audience Manager] 同步还是特征实现)的活动用户。您的客户应使用此选项将其&#x200B;*total*&#x200B;区段资格数据发送到目标。
* **[!UICONTROL Lifetime]**:文件包含自目标创建以来在所有客 [!DNL Audience Manager] 户端属性中的任意位置看到的活动用户。
* **[!UICONTROL Sync Type Lookback Period]**:如果选择 [!UICONTROL Customer] 或 [!UICONTROL Platform]，请选择时间段。文件包含选定时间段内的活动用户。
接下来，选择订单类型。 这表示每个与合作伙伴的出站集成的频率和范围。 在增量订单和完整订单之间进行选择。
* **[!UICONTROL Incremental Scheduled Run]**:每次运行时， [!DNL Audience Manager] 将仅将上一个出站订单后符合条件的净新用户叫出。选择您希望[!DNL Audience Manager]执行增量同步过程的所需时间段。 例如，您可以选择每24小时、每7天、每30天，或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一个增量订单等同于完整订单，因为之前从未向目标发送过任何用户。

* **[!UICONTROL Full Sync Scheduled Run]**:每次运行时， [!DNL Audience Manager] 都会将自目标首次设置以来的所有活动用户叫出。选择您希望[!DNL Audience Manager]用来执行完全同步进程的所需计划。 例如，您可以选择每24小时、每7天、每30天，或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我们建议使用增量同步比使用完整同步更频繁。 增量同步仅发送包含新特征实现或ID同步的文件。 完全同步会发送所有文件，无论它们是否包含新实现或ID同步。 仅当客户端需要其所有用户的完整副本时，才使用[!UICONTROL Full Sync Scheduled Run]配置来减少出站数据卷。

## 配置数据源 {#configure-data-sources}

对于[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]或[!UICONTROL Bulk Segment]目标，填写以下字段。 通过这些设置，您可以发送与数据源关联的所有数据（特征、区段或ID，基于所选类型）。

* **[!UICONTROL All Unrestricted First Party Data]**:选择以使用所有第一方数据源。如果选择此选项，则[!UICONTROL Available Data Sources]选项将被禁用。
* **[!UICONTROL Available Data Sources]**:使用箭头在和框之间移 **[!UICONTROL Available Data Sources]** 动数 **[!UICONTROL In File Data Sources]** 据源。

## 保存并完成 {#save-and-finalize}

填写所有必填字段后，将激活&#x200B;**[!UICONTROL Save]**&#x200B;按钮。 单击&#x200B;**[!UICONTROL Save]**&#x200B;以完成创建目标流程。

## 删除公司目标 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要删除目标，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Companies]**，找到并单击所需的公司，然后单击&#x200B;**[!UICONTROL Destinations]**&#x200B;选项卡。
1. 在所需目标的&#x200B;**[!UICONTROL Actions]**&#x200B;列中单击![](assets/icon_delete.png)。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以确认删除。

>[!NOTE]
>
>如果目标具有映射到该目标的区段，则无法删除该目标。
