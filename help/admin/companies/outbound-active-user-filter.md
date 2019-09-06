---
description: 按照这些说明生成一个完全同步文件，其中仅包括最近活动的用户。您可能希望过滤活动用户将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。不能将此过滤器与增量同步一起使用。
seo-description: 按照这些说明生成一个完全同步文件，其中仅包括最近活动的用户。您可能希望过滤活动用户将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。不能将此过滤器与增量同步一起使用。
seo-title: 仅按有效用户过滤出站数据
title: 仅按有效用户过滤出站数据
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 仅按有效用户过滤出站数据 {#filter-outbound-data-by-active-users-only}

按照这些说明生成一个完全同步文件，其中仅包括最近活动的用户。您可能希望过滤活动用户将相关数据推送到现场定位系统，或者限制发送到DSP的文件的大小。不能将此过滤器与增量同步一起使用。

>[!NOTE]
>
>访客不需要在选定的客户网站或广告流量中看到“活动”。任何 [!DNL Audience Manager] 客户或合作伙伴均可看到他们的“活动”。

仅供活动用户过滤：

1. 单击 **[!UICONTROL Companies]**.
1. 选择要处理的公司，然后单击 **[!UICONTROL Destinations]**。
1. [!UICONTROL Batch Data] 在部分中，设置以下选项：

   * **[!UICONTROL Sync Type]**：选择 **[!UICONTROL Customer]****[!UICONTROL Platform]**&#x200B;或.
   * **[!UICONTROL Sync Type Lookback Period]**：此时间间隔定义数据文件的范围。选择包括 **[!UICONTROL 24 hours]**， **[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**
   * **[!UICONTROL Incremental Sync Scheduled Run]**：选择 **[!UICONTROL Never]**。记住，此过滤器仅应用于完全同步文件。
   * **[!UICONTROL Full Sync Scheduled Run]**：这将确定您要接收此文件的频率。选择包括 **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**、或 **[!UICONTROL 30 days]****[!UICONTROL Never]** (禁用)。

1. 单击 **[!UICONTROL Save]**.
