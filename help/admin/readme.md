---
source-git-commit: b76aa4a35a5216aabd60d07352a7c4bd2b3e6e32
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---
# 说明

**注意：此页面（或任何readme.md页面）不会发布到面向客户的文档**

## 目录

+ `TOC.md` 位于用户指南根目录的提供了此解决方案指南中包含的主题的组织。
+ 每个用户指南都有其自身的独特之处 `TOC.md`，您可以在其中根据需要对所有页面/主题进行排序。
+ 所有用户指南的第一页都是 `overview.md`.

## 用户指南

+ 用户指南的简介称为 `overview.md`
+ 用户指南中的每个主题都有自己的独特目录。
   + 如果指南中有一个名为的主题 *实现*，相应的目录为 `/implementation`
+ 所有图像资源都存储在 `/assets` 位于用户指南的根目录。
   + 中的所有图像 `/assets` 目录将进行本地化。
   + 中的任何图像 `/no-localize` 目录将不会进行本地化（令人惊讶！）。 这可用于确保在loc版本中特定资产不会被不必要地复制。

## 用户指南级别元数据

+ 描述用户指南的元数据存储在中 `TOC.md`. 这包括：
   + product — 产品/功能的名称。
   + cloud — 此产品所属的云。
   + 受众 — 指南所针对的受众或原型。
   + user-guide — 用户指南的名称。

## 页面级别元数据

+ 描述文档所需的元数据将作为每个单独页面的一部分存储。 这包括：
   + title — 页面的标题。
   + description — 页面的描述。
   + seo-title - seo替代标题。
   + seo-description — 用于SEO的替代标题。
   + short-title — （可选字段）。
   + index - yes / no — 页面是否会按Adobe的搜索平台编入索引。
   + translate - yes / no — 此页面是否会进行本地化。
   + 版本 — 主要用于AEM和Campaign，表示产品的版本。
   + private-feature-pack — 主要用于AEM。
   + beta — 此产品是否为beta版？
   + 重定向 — 必要时可用于为新页面创建引用。
   + doc-type：引用（默认）/疑难解答/开发人员/教程/ kb/白皮书。

## 更多信息

如需更多发布说明、风格指南、示例和其他资源，请访问 [协作文档存储库](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
