---
description: 为了防止意外将文件和数据载入其他合作伙伴或客户拥有的目标数据源，Audience Manager在合作伙伴ID(PID)和其他合作伙伴拥有的数据源之间添加了映射要求。
title: 管理第二方数据的载入访问
source-git-commit: 6c88979f876909bc32b5238605cb4a352e327a00
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 管理第二方数据的入门访问 {#manage-onboarding-access-for-second-party-data}

为了防止意外将文件和数据载入到其他合作伙伴拥有的目标数据源中，Audience Manager在合作伙伴ID(PID)和其他合作伙伴拥有的数据源(DPID)之间添加了映射要求。 有关PID和DPID的更多信息，请参阅 [Audience ManagerID索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

出于第二方数据共享目的，如果Audience Manager合作伙伴或客户希望将文件摄取到他们不拥有的目标数据源中，则他们需要请求其合作伙伴ID(PID)与该特定数据源(DPID)之间的映射。 如果缺少映射，则集客数据作业将不会处理文件，并且数据不会载入到Audience Manager中。

要创建该映射，请向Audience Manager工程团队提交Jira票证。 查看示例Jira票证 [此处](https://jira.corp.adobe.com/browse/AAM-60353). 您无需请求为任何现有数据共享关系创建映射。
