---
description: In order to prevent accidental file and data onboarding into target data sources owned by other partners or customers, Audience Manager has added a mapping requirement between partner ID (PID) and the data sources owned by other partners.
title: 管理第二方数据的载入访问
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 管理第二方数据的入门访问 {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> The audience for this page is Adobe-internal employees. 如果您是Audience Manager客户，请求按照本页所述进行第二方数据源映射，请联系客户关怀团队或您的技术客户经理。
> 请注意，请求现有数据共享关系的映射时不需要使用。 将数据载入属于您的PID的目标数据源时，也不需要进行映射。

为了防止意外将文件和数据载入到其他合作伙伴拥有的目标数据源中，Audience Manager在合作伙伴ID(PID)和其他合作伙伴拥有的数据源(DPID)之间添加了映射要求。 有关PID和DPID的更多信息，请参阅 [Audience ManagerID索引](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

出于第二方数据共享目的，如果Audience Manager合作伙伴或客户希望将文件摄取到他们不拥有的目标数据源中，则他们需要请求其合作伙伴ID(PID)与该特定数据源(DPID)之间的映射。 如果缺少映射，则集客数据作业将不会处理文件，并且数据不会载入到Audience Manager中。

要创建该映射，请向Audience Manager工程团队提交Jira票证。 查看示例Jira票证 [此处](https://jira.corp.adobe.com/browse/AAM-60353). 您无需请求为任何现有数据共享关系创建映射。
