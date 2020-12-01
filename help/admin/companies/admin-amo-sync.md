---
description: 默认情况下，所有公司都与Adobe Media Optimizer(AMO)同步数据。 在管理员UI中，每个公司容器都有一个管理此流程的数据源。 此数据源为AdobeAMO(ID 411)。 单击选定容器的容器行(在公司选项卡下)，以禁用此默认同步，或向AMO同步过程添加和删除其他数据源。
seo-description: 默认情况下，所有公司都与Adobe Media Optimizer(AMO)同步数据。 在管理员UI中，每个公司容器都有一个管理此流程的数据源。 此数据源为AdobeAMO(ID 411)。 单击选定容器的容器行(在公司选项卡下)，以禁用此默认同步，或向AMO同步过程添加和删除其他数据源。
seo-title: ID 与 Media Optimizer 同步
title: ID 与 Media Optimizer 同步
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 6%

---


# ID 与 Media Optimizer 同步{#id-syncing-with-media-optimizer}

默认情况下，所有公司都与[!DNL Adobe Media Optimizer]([!DNL AMO])同步数据。 在[!UICONTROL Admin UI]中，每个公司容器都有一个管理此进程的数据源。 此数据源为[!UICONTROL Adobe AMO]([!UICONTROL ID] 411)。 单击选定公司的容器行（位于[!UICONTROL Containers]选项卡下），以禁用此默认同步，或向[!DNL AMO]同步过程添加和删除其他数据源。

![](assets/id-sync.png)

## ID同步状态{#id-sync-status}

下表描述了数据源的同步状态。

| 状态 | 描述 |
|------ | -------- |
| 关 | 从此容器的[!UICONTROL Selected Data Sources]中删除所有数据源以禁用与[!DNL AMO]的ID同步 |
| 开启（无论ID服务版本如何） | 在以下情况下，无论ID服务版本如何，数据源都与[!DNL AMO]同步： <ul><li>数据源显示在[!UICONTROL Selected Data Sources]列表中。</li><li>[!DNL AMO]复选框&#x200B;*未选中。*</li></ul> |
| 开启（无论ID服务版本如何） | 在以下情况下，数据源将与ID服务版本2.0（或更高版本）的[!DNL AMO]同步： <ul><li>数据源显示在[!UICONTROL Selected Data Sources]列表中。</li><li>选中[!DNL AMO]复选框&#x200B;**。</li></ul> |

>[!MORELIKETHIS]
>
>* [管理容器](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

