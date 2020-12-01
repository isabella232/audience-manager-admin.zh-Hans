---
description: 按照以下说明生成完整的同步文件，该文件仅包含最近处于活动状态的用户。 您可能希望过滤活动用户以将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。 不能将此筛选器与增量同步一起使用。
seo-description: 按照以下说明生成完整的同步文件，该文件仅包含最近处于活动状态的用户。 您可能希望过滤活动用户以将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。 不能将此筛选器与增量同步一起使用。
seo-title: 仅按活动用户筛选出站数据
title: 仅按活动用户筛选出站数据
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# 仅按活动用户筛选出站数据{#filter-outbound-data-by-active-users-only}

按照以下说明生成完整的同步文件，该文件仅包含最近处于活动状态的用户。 您可能希望过滤活动用户以将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。 不能将此筛选器与增量同步一起使用。

>[!NOTE]
>
>访客无需在选定的客户站点或广告流量中看到，即可获得“有效”资格。 任何[!DNL Audience Manager]客户或合作伙伴都可以看到它们以符合“活动”资格。

要仅按活动用户进行筛选，请执行以下操作：

1. 单击 **[!UICONTROL Companies]**.
1. 选择要处理的公司并单击&#x200B;**[!UICONTROL Destinations]**。
1. 在[!UICONTROL Batch Data]部分，设置以下选项：

   * **[!UICONTROL Sync Type]**:选择 **[!UICONTROL Customer]** 或 **[!UICONTROL Platform]**。
   * **[!UICONTROL Sync Type Lookback Period]**:此时间间隔定义数据文件的范围。选项包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**&#x200B;和&#x200B;**[!UICONTROL 30 days]**。
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 请记住，此过滤器仅适用于完全同步文件。
   * **[!UICONTROL Full Sync Scheduled Run]**:这决定了您希望接收此文件的频率。选择包括&#x200B;**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**&#x200B;或&#x200B;**[!UICONTROL Never]**（禁用）。

1. 单击 **[!UICONTROL Save]**.
