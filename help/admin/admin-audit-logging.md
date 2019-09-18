---
description: '在调试客户问题时，首先使用审核记录。 '
seo-description: '在调试客户问题时，首先使用审核记录。 '
seo-title: 审核记录
title: 审核记录
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 审核记录 {#audit-logging}

在调 [!UICONTROL  Audit Logging] 试客户问题时首先使用它。

> [!NOTE]
>
>[!UICONTROL Audit Logging] 正在开发中，并可能发生更改。 请记录您在（团队）中遇到的 [!DNL JIRA] 任何[!DNL UI] 问题

![“审核日志记录”视图](assets/audit-logging-img.png)

在“审 **核类型** ”下拉选择器中，选择以下选项：

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

对 **象ID** 是您正在研究的项目的ID。 请参阅下表，每种情况下，其ID对应于对象ID:

| 审核类型 | 对象ID |
---------|----------|
| [!UICONTROL Partner] | 合作伙伴ID - PID |
| [!UICONTROL User] | 用户 ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | 数据源ID |
| [!UICONTROL General Datasource] | 数据源ID |
| [!UICONTROL Merge Rule Datasource] | 数据源ID |
| [!UICONTROL Data Feed] | 数据源ID |
| [!UICONTROL Data Feed Subscription] | 数据源ID |
| [!UICONTROL Trait Summary] | SID（特征） |
| [!UICONTROL Trait Rule] | SID（特征） |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | 不适用 |
| [!UICONTROL Derived Signal] | 不适用 |
| [!UICONTROL Model] | 不适用 |
| [!UICONTROL Segment Test Group] | 不适用 |

使 [!UICONTROL Start Date] 用([!DNL UTC])和 [!UICONTROL End Date] ([!DNL UTC])缩小日志的时间间隔。