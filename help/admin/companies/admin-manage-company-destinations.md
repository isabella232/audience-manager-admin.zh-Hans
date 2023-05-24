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

有关详细信息，请参阅 [目标](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) 在 *Audience Manager用户指南*.

## 创建或编辑公司目标 {#create-edit-company-destinations}

浏览各部分，获取有关如何创建新的分步说明 [!DNL Audience Manager] 目标或编辑现有目标。

<!-- create-edit-company-destinations.xml -->

访问 [“Experience Cloud合作伙伴集成”页](https://wiki.corp.adobe.com/x/mPIMPw) ，然后再设置目标。 该页面包含您需要为每个页面填写的特定信息 [!DNL Audience Manager] 合作伙伴集成。

如果您的客户希望使用 [!DNL Adobe Media Optimizer] 作为中的目标 [!DNL Audience Manager] ，您需要在 [!DNL Adobe Media Optimizer].

## 导航到目标选项卡 {#navigate-destinations}

1. 单击 **[!UICONTROL Companies]**，然后找到并单击所需的公司以显示其 [!UICONTROL Profile] 页面。 您可以使用 [!UICONTROL Search] 框或列表底部的分页控件以查找所需的公司。 您可以通过单击所需列的标题，按升序或降序对每个列进行排序。
1. 单击 **[!UICONTROL Destinations]** 选项卡。
1. 要创建新目标，请单击 **[!UICONTROL Add Destination]**. 要编辑现有目标，请在 **[!UICONTROL Name]** 列。

## 基本设置 {#basic-settings}

填写 **[!UICONTROL Basic Settings]** 窗口。

* **[!UICONTROL Name]：** （必需）指定此目标的名称。
* **[!UICONTROL Description]：** 指定有关此目标的描述性信息。
* **[!UICONTROL Type]：** （必需）选择所需的目标类型：
   * **[!UICONTROL Bulk ID]**：在不同平台之间同步ID。
   * **[!UICONTROL Bulk Trait]**：将特征信息批量发送到不同的平台。
   * **[!UICONTROL Bulk Segment]**：将区段信息批量发送到不同的平台。
   * **[!UICONTROL S2S]**：使用服务器到服务器目标将实时和批量数据发送到不同的平台。
* **[!UICONTROL Auto-Fill Destination Mapping]：** ( [!UICONTROL S2S] （仅限）选择一个选项：
   * **[!UICONTROL Segment ID]：** 如果选择此设置，则目标值映射将使用 [!DNL Audience Manager] 区段ID。
   * **[!UICONTROL Integration Code Value]：** 如果选择此设置，则目标值映射将使用 [!DNL Audience Manager] 区段集成代码。
* **[!UICONTROL User ID Key]：** （必需）从下拉列表中选择此目标所需的用户ID密钥。

此ID用作主控数据源ID。 这会确定文件中要退出的用户ID。

>[!NOTE]
>
>对于 [!UICONTROL Bulk ID] 目标类型，则不能使用 [!DNL Audience Manager] [!UICONTROL User ID] 或 [!DNL Adobe Experience Cloud] ID。

如果您的数据源ID ( [!UICONTROL DPID])不会显示在下拉列表中，您必须选择 **[!UICONTROL Outbound]** 上的数据源级别的复选框 [“数据源设置”页](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]：** （必需）从下拉列表中选择此目标所需的数据源。 此设置允许标记出站数据，允许将出站数据摄取到客户端的单独系统中。
* **[!UICONTROL Foreign Account ID]：** 指定此目标的外部帐户ID。 这是收件人系统中此出站数据的标识值。
* **[!UICONTROL Outbound Sample Rate Denominator]：** 如果返回的数据总量未知，则使用此设置可仅返回数据样本量，而不是返回数据总量。 调整此处的数字以表示数据的一部分（例如，值“100”返回常规数据量的1/100，值“10”返回常规数据量的1/10）。 默认值为“1”，这将返回所有数据。

## 实时数据（用于S2S目标） {#realtime-s2s}

如果您要创建 [!UICONTROL S2S] 目标，请填写以下字段：

**[!UICONTROL Servers]**：选择所需的 `HTTP` 服务器作为目标服务器。
**[!UICONTROL Format]**：从下拉列表中选择此目标的所需格式： [!UICONTROL HTTP only].

>[!NOTE]
>
>对象 [!DNL S2S] 只有这样，您才能启用或禁用 [!UICONTROL Realtime] 或 [!UICONTROL Batch] 目标使用屏幕关闭/打开滑块。 不能同时禁用这两个选项。

## 批量数据 {#batch-data}

对象 [!UICONTROL Bulk ID]， [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目标，请填写以下字段：

* **[!UICONTROL Protocol]**：（必需）从下拉列表中选择此目标所需的协议：
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：（必需）从下拉列表中选择此目标所需的服务器。
* **[!UICONTROL Format]**：（必需）从下拉列表中选择此目标所需的格式： [!DNL HTTP] 或文件类型，具体取决于您在上面选择的协议。
* **[!UICONTROL Sync Type]**：（必需）为此目标选择所需的同步类型。 这表示客户希望包含在出站订单中的用户活动级别。 选择 **[!UICONTROL Customer]** 客户只对根据彼等之物业分析分部资格感兴趣。 选择 **[!UICONTROL Platform]** 如果客户希望将所有场外活动的区段资格纳入其中 [!DNL Audience Manager] 客户。
* **[!UICONTROL Customer]**：文件包含的活动用户，这些用户仅在客户端的属性上实现至少1个特征（与客户端的属性关联） [!UICONTROL PID])。 您的客户应使用此选项来出站 *实时* 区段资格到目标。
* **[!UICONTROL Platform]**：文件包含的活动用户具有至少1个实时交互（无论是ID同步还是特征实现），并且可在所有位置随时交互 [!DNL Audience Manager] 选定时间段的客户端属性（与所有客户端PID关联）。 您的客户应使用此选项来出站 *总计* 区段资格到目标。
* **[!UICONTROL Lifetime]**：文件包含可在所有位置看到的活动用户 [!DNL Audience Manager] 自创建目标以来客户端的属性。
* **[!UICONTROL Sync Type Lookback Period]**：如果您选择 [!UICONTROL Customer] 或 [!UICONTROL Platform]，选择一个时间段。 文件包含选定时间段的活动用户。
接下来，选择订单类型。 这指示与合作伙伴的每次出站集成的频率和范围。 选择增量订单和完整订单。
* **[!UICONTROL Incremental Scheduled Run]**：每次运行时， [!DNL Audience Manager] 将仅出站自上次出站订单以来符合条件的净新用户。 选择所需的时间段 [!DNL Audience Manager] 执行增量同步过程。 例如，您可以选择每24小时、每7天、每30天或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>第一个增量订单等于完整订单，因为以前没有任何用户被发送到目标。

* **[!UICONTROL Full Sync Scheduled Run]**：每次运行时， [!DNL Audience Manager] 将出站自首次设置目标以来的所有活动用户。 选择所需的计划 [!DNL Audience Manager] 用于执行完整的同步过程。 例如，您可以选择每24小时、每7天、每30天或从不。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>我们建议使用增量同步的频率高于完全同步。 增量同步仅发送包含新特征实现或ID同步的文件。 完全同步会发送所有文件，无论它们是否包括新的实现或ID同步。 仅使用 [!UICONTROL Full Sync Scheduled Run] 在客户端需要其所有用户的完整副本时进行配置，以减少出站数据量。

## 配置数据源 {#configure-data-sources}

对象 [!UICONTROL Bulk ID]， [!UICONTROL Bulk Trait] 或 [!UICONTROL Bulk Segment] 目标，请填写以下字段。 这些设置允许您发送与数据源关联的所有数据（特征、区段或ID，基于选定的类型）。

* **[!UICONTROL All Unrestricted First Party Data]**：选择以使用所有第一方数据源。 如果选择此选项， [!UICONTROL Available Data Sources] 选项被禁用。
* **[!UICONTROL Available Data Sources]**：使用箭头在 **[!UICONTROL Available Data Sources]** 和 **[!UICONTROL In File Data Sources]** 盒子。

## 保存并完成 {#save-and-finalize}

此 **[!UICONTROL Save]** 填写完所有必填字段后按钮处于激活状态。 单击 **[!UICONTROL Save]** 以完成创建目标过程。

## 删除公司目标 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

要删除目标，请执行以下操作：

1. 单击 **[!UICONTROL Companies]**，找到并单击所需的公司，然后单击 **[!UICONTROL Destinations]** 选项卡。
1. 单击  ![](assets/icon_delete.png) 在 **[!UICONTROL Actions]** 所需目标的列。
1. 单击 **[!UICONTROL OK]** 以确认删除。

>[!NOTE]
>
>如果目标具有映射到它的区段，则无法删除该目标。
