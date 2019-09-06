---
description: '在调试客户问题时，请使用审核日志作为第一个位置。 '
seo-description: '在调试客户问题时，请使用审核日志作为第一个位置。 '
seo-title: 审核日志
title: 审核日志
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 审核日志 {#audit-logging}

作为 [!UICONTROL  Audit Logging] 调试客户问题的第一个位置。

> [!NOTE]
>
>[!UICONTROL Audit Logging] 当前正在开发并受到更改。请记录您遇到的任何问题 [!DNL JIRA] ([!DNL UI] 团队)

![审核日志视图](assets/audit-logging-img.png)

在 **“审核类型”** 下拉选择器中，选择以下各项：

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

**对象ID** 是您正在研究的项目的ID。请参阅下面的表格，其中对应于每个情况中的对象ID对应的ID：

| 审核类型 | 对象ID |
---------|----------|
| [!UICONTROL Partner] | 合作伙伴ID- PID |
| [!UICONTROL User] | 用户 ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | 数据源ID |
| [!UICONTROL General Datasource] | 数据源ID |
| [!UICONTROL Merge Rule Datasource] | 数据源ID |
| [!UICONTROL Data Feed] | 数据源ID |
| [!UICONTROL Data Feed Subscription] | 数据源ID |
| [!UICONTROL Trait Summary] | SID(特征) |
| [!UICONTROL Trait Rule] | SID(特征) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | 不适用 |
| [!UICONTROL Derived Signal] | 不适用 |
| [!UICONTROL Model] | 不适用 |
| [!UICONTROL Segment Test Group] | 不适用 |

使用 [!UICONTROL Start Date] ([!DNL UTC])和 [!UICONTROL End Date] ([!DNL UTC])可缩小日志的时间间隔。