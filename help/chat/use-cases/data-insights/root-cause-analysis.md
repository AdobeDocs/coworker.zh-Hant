---
title: 使用Adobe Analytics和Customer Journey Analytics分析根本原因
description: 使用Adobe CX Enterprise Coworker來調查量度變更、識別貢獻的維度和區段，以及測試Adobe Analytics和CJA中的假設。
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 186
last-substantial-update: 2026-08-10T00:00:00.000Z
jira: KT-22082
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 7e096fc9cda2157c02501ee909a80bf4df9a2f32
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%
---

# 使用[!DNL Adobe Analytics]和[!DNL Customer Journey Analytics]分析根本原因

使用Adobe CX Enterprise Coworker Chat調查Adobe Analytics或Customer Journey Analytics (CJA)中量度變更的原因。 Co-worker會分析您指定的變更、構成維度和區段的曲面，並協助您使用自然語言測試假設。

## 使用Customer Journey Analytics資料進行根本原因分析

下列影片示範Co-worker如何將對話式AI與Customer Journey Analytics結合。 瞭解如何以自然語言提出問題、視覺化結果、識別有意義的趨勢，並找出無需建立手動查詢即可提升效能的因素。

>[!VIDEO](https://video.tv.adobe.com/v/3496861/?captions=chi_hant&learn=on&enablevpops)

### 先決條件

開始之前：

1. **可以存取同事聊天並連線Customer Journey Analytics。** 確認貴組織已設定必要的整合。
1. **擁有您要分析之CJA資料檢視的檢視存取權。** Co-worker只能使用您可用的資料檢視和元件。
1. **選擇包含相關量度和維度的資料檢視。** 如果您可以存取多個資料檢視，請命名您希望Co-worker使用的檢視。
1. **識別您要調查的變更。** 指定量度、日期範圍和比較期間。 您也可以提供維度、區段或假設，以集中進行分析。

### Customer Journey Analytics的範例提示

從您的資料檢視中，以元件名稱和時段取代括弧內的文字。

* 在&#x200B;**[資料檢視名稱]**&#x200B;資料檢視中，為何&#x200B;**[量度]**&#x200B;在&#x200B;**[日期範圍]**&#x200B;內與&#x200B;**[比較日期範圍]**&#x200B;相比有所變更？ 依&#x200B;**[維度]**&#x200B;劃分變更，並顯示貢獻最大的區段。
* 在&#x200B;**[資料檢視名稱]**&#x200B;資料檢視中，**[維度或區段]**&#x200B;是否造成從&#x200B;**[日期範圍A]**&#x200B;到&#x200B;**[日期範圍B]**&#x200B;的&#x200B;**[量度]**&#x200B;減少？ 比較兩個期間的值並解釋變更內容。
* 在&#x200B;**[資料檢視名稱]**&#x200B;資料檢視中，比較&#x200B;**[日期範圍]**&#x200B;內&#x200B;**[區段A]**&#x200B;與&#x200B;**[區段B]**&#x200B;的&#x200B;**[量度]**。 哪些維度對差異的貢獻最大？
* 在&#x200B;**[資料檢視名稱]**&#x200B;資料檢視中，測試此假設： **[陳述您的假設]**。 分析&#x200B;**[日期範圍]**&#x200B;的&#x200B;**[量度]**，並顯示支援或不支援它的維度或區段。

## 使用Adobe Analytics資料進行根本原因分析

同事可以調查Adobe Analytics報表套裝中量度變更的原因。 它會使用`aa-root-cause-analysis`技能來分析您指定的變更，並識別造成變更的維度和區段。

### 先決條件

開始之前：

1. **可以存取同事聊天並連線Adobe Analytics。** 在Co-worker中，移至&#x200B;**自訂>整合**&#x200B;並確認`aa-mcp`整合已列出且已連線。 如果無法取得，請要求您的管理員檢查組織的設定。 請參閱[開始使用同事聊天](https://experienceleague.adobe.com/zh-hant/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)分析資料，以取得設定指南。
1. **擁有您要分析之Adobe Analytics報表套裝的檢視存取權。** 同事會繼承您的Adobe Analytics許可權，而且只能使用Analysis Workspace中可供您使用的報表套裝和元件。
1. **選擇包含相關資料的報表套裝。** 如果您可以存取多個報表套裝，請為同事要使用的報表套裝命名。
1. **識別您要調查的變更。** 指定量度和時段。 如需更聚焦的分析，請包含比較期間、相關維度或區段，以及您想要同事測試的任何假設。

### Adobe Analytics的範例提示

將報表套裝中的括弧文字取代為元件名稱和時段。

* 在&#x200B;**[報表套裝名稱]**&#x200B;報表套裝中，為何在&#x200B;**[日期範圍]**&#x200B;期間有&#x200B;**[量度]**&#x200B;變更而非&#x200B;**[比較日期範圍]**？ 依&#x200B;**[維度]**&#x200B;劃分變更，並顯示貢獻最大的區段。
* 在&#x200B;**[報表套裝名稱]**&#x200B;報表套裝中，**[維度或區段]**&#x200B;是否造成從&#x200B;**[日期範圍A]**&#x200B;到&#x200B;**[日期範圍B]**&#x200B;的&#x200B;**[量度]**&#x200B;減少？ 比較兩個期間的值並解釋變更內容。
* 在&#x200B;**[報表套裝名稱]**&#x200B;報表套裝中，比較&#x200B;**[日期範圍]**&#x200B;內&#x200B;**[區段A]**&#x200B;與&#x200B;**[區段B]**&#x200B;的&#x200B;**[量度]**。 哪些維度對差異的貢獻最大？

## 相關資源

* [使用Adobe CX Enterprise Coworker Chat分析資料](https://experienceleague.adobe.com/zh-hant/docs/coworker/content/chat/use-cases/data-insights/analytics-overview)
* [開始使用同事聊天分析資料](https://experienceleague.adobe.com/zh-hant/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)
