---
title: 使用CX Enterprise Coworker分析Adobe Experience Platform對象變更
description: 瞭解CX Enterprise Coworker如何使用Operational Stats和Causal Analysis技能來說明對象變更、識別可能的原因、評估下游影響以及建議後續步驟。
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 216
last-substantial-update: 20261105
jira: KT-22454
autotag-review: '2026-11-05T15:16:40.881Z'
TQID: 'https://experienceleague.adobe.com/mj3rSj7AxRsmhxipLJLR69bzfujK-eCVaXQMFlgg-NA'
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 41216c2254d4c98f05c608f02bc6da31da3dd3c6
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%
---

# 為什麼我的Experience Platform對象人數激增/下降？

瞭解[!DNL CX Enterprise Coworker]如何使用「操作統計資料」和「因果分析」技能，協助調查索引鍵[!DNL Adobe Experience Platform]物件的非預期變更。

## 您將瞭解的內容

在此影片中，您將會瞭解如何在同事中使用純語言提示，以在行銷活動啟動前調查Adobe Experience Platform對象中意外的增加。 逐步解說會顯示因果分析如何將受眾規模變更與營運資料連結、排除設定變更，以及提供可能的解釋，而不需要等待工程部門調查。

>[!VIDEO](https://video.tv.adobe.com/v/3507342/?learn=on&enablevpops)

您將學習如何：

- 使用作業統計和因果分析技能執行原因分析。
- 比較受眾規模變更與沙箱設定檔總數中的變更。
- 瞭解對象資格規則如何導致新擷取的設定檔自動進入對象。
- 檢查管道和設定活動，以判斷對象設定是否已變更。
- 使用同事建議的後續步驟來調整對象條件，並繼續調查設定檔增長的來源。
- 識別相依對象、行銷活動、目的地和未發佈的歷程，以評估下游影響。
- 當上游對象變更影響鎖定目標時，在啟動之前識別要驗證的內容。

## 分析如何運作

此範例追蹤在數天內人數意外變化的對象。 Co-worker會分析選取的時間範圍，並比較可能的原因。 分析發現，受眾的每日變化與沙箱中總設定檔母體的成長相符。

由於對象包含沒有忠誠度ID的設定檔，因此新擷取的符合該條件的設定檔可自動符合資格。 Co-worker也會檢查管道和設定歷史記錄，協助區分傳入資料變更與對象設定的變更。

## 評估下游影響

尋找原因只是調查的一部分。 影片也會示範如何詢問Co-worker對象變更對下游的影響。 同事會檢視相依物件，並著重說明較大對象可能會對未來目標定位造成影響的位置，包括相關對象和歷程。

這可讓行銷營運團隊更快速地偵測未預期的對象變更，以瞭解其可能的原因、潛在影響，以及在啟動前進行的檢查。

## 主要外賣

CX Enterprise Coworker可結合營運統計資料、因果分析、相依性資訊，以及在對話式工作流程中建議的後續動作，協助說明重要的Adobe Experience Platform物件為何會隨著時間變更。
