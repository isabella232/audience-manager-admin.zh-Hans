---
description: 默认情况下，所有公司都与Adobe Media Optimizer (AMO)同步数据。 在管理员UI中，每个公司容器都有一个用于管理此流程的数据源。 此数据源Adobe于AMO (ID 411)。 单击选定公司的容器行（在“容器”选项卡下）以禁用此默认同步，或向AMO同步过程添加和删除其他数据源。
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: ID 与 Media Optimizer 同步
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 6%

---

# ID 与 Media Optimizer 同步 {#id-syncing-with-media-optimizer}

默认情况下，所有公司都与同步数据 [!DNL Adobe Media Optimizer] ([!DNL AMO])。 在 [!UICONTROL Admin UI]，每个公司容器都有一个数据源来管理此过程。 此数据源为 [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411)。 单击容器行(在 [!UICONTROL Containers] 选项卡)，以禁用此默认同步或者向中添加和删除其他数据源 [!DNL AMO] 同步过程。

![](assets/id-sync.png)

## ID同步状态 {#id-sync-status}

下表描述了数据源的同步状态。

| 状态 | 描述 |
|------ | -------- |
| 关 | 从删除所有数据源 [!UICONTROL Selected Data Sources] ，以禁用ID同步 [!DNL AMO] |
| 开启（不论ID服务版本如何） | 数据源与同步 [!DNL AMO] 无论ID服务版本如何，当： <ul><li>数据源显示在 [!UICONTROL Selected Data Sources] 列表。</li><li>此 [!DNL AMO] 复选框 *不是* 已选中。</li></ul> |
| 开启（不论ID服务版本如何） | 数据源将与 [!DNL AMO] 使用ID服务版本2.0（或更高版本）的情况： <ul><li>数据源显示在 [!UICONTROL Selected Data Sources] 列表。</li><li>此 [!DNL AMO] 复选框 *是* 已选中。</li></ul> |

>[!MORELIKETHIS]
>
>* [管理容器](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

