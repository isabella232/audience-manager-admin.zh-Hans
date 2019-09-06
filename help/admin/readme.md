---
source-git-commit: b76aa4a35a5216aabd60d07352a7c4bd2b3e6e32
translation-type: tm+mt

---
# 说明

**注意：此页面(或任何readme. md页面)不会发布到面向客户的文档**

## 目录

+ `TOC.md` 用户指南的根目录提供了该解决方案指南中包含的主题。
+ 每个用户指南都具有自己的独特功能 `TOC.md`，您可以根据需要对所有页面/主题进行排序。
+ 所有用户指南的第一页都是 `overview.md`。

## 用户指南

+ 用户指南简介称为 `overview.md`
+ 用户指南中的每个主题都有自己的独特目录。
   + 如果在称为 *“实施”*&#x200B;的指南中存在主题，则相应的目录为 `/implementation`
+ 所有图像资源都存储在 `/assets` 用户指南的根目录下。
   + `/assets` 目录中的所有图像都将本地化。
   + `/no-localize` 目录中的任何图像都不会本地化(有一个意外！)。这可用于确保在loc版本中不必要重现特定资产。

## 用户指南级别元数据

+ 用于描述用户指南的元数据存储在此中 `TOC.md`。这包括：
   + 产品-产品/功能的名称。
   + 云-此产品所属的云。
   + 受众-定位指南的受众或类型。
   + 用户指南-用户指南的名称。

## 页面级别元数据

+ 描述文档所需的元数据作为每个单独页面的一部分存储。这包括：
   + 标题-页面标题。
   + 描述-页面描述。
   + seo-title- seo替换标题。
   + seo-description-用于SEO用途的替换标题。
   + short-title-(可选字段)。
   + 索引-是/否-页面将由Adobe的搜索平台索引。
   + translate- yes/no- this page be localized.
   + 版本(主要用于AEM和Campaign)以表示产品版本。
   + private-feature-pack-主要用于AEM。
   + Beta-此产品是Beta版产品吗？
   + 重定向-可用于为新页面创建引用。
   + doc-type：reference(default)/疑难解答/developer/tutorial/kb/白皮书。

## 更多信息

有关更多发布说明、样式指南、示例和其他资源，请访问 [协作文档回购](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
