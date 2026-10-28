---
title: 透過同事聊天分析業務績效和KPI
description: 使用「同事聊天」來說明量度移動的原因、預測其前往何處、準備績效審查，以及將重複分析轉換為可重複使用的技能。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%
---

# 業務績效概觀

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

使用Adobe CX Enterprise Coworker Chat瞭解業務狀況、量度移動的原因、前往的位置，以及下一步該做什麼。 調查關鍵量度的變更，將其向前投影，並將您的發現轉變為適用於利害關係人的摘要和可重複使用的技能。

業務績效是Co-worker Chat中的數個分析網域之一。 若要檢視所有網域，請參閱「使用同事聊天分析資料」中的[開始在同事聊天中分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最佳對象：**&#x200B;分析師、業務使用者

## 先決條件

若要使用此頁面上的使用案例，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視或Adobe Analytics報表套裝。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析的資料檢視或報表套裝的存取權。 同事聊天會從Customer Journey Analytics或Adobe Analytics繼承您的許可權。

## 使用案例

| 使用案例 | 函數 |
| --- | --- |
| [探索趨勢和根本原因](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![探索趨勢和根本原因](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | 識別Customer Journey Analytics和Adobe Analytics資料中的趨勢，以及推動效能變更的因素，無需手動查詢。<p>**範例提示：** 「為什麼上週轉換率下降？」</p><p>如需詳細資訊，請參閱[Customer Journey Analytics與同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。</p> |
| [說明量度移動的原因](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 執行根本原因分析，該分析顯示變更後的尺寸與區段，並排除其餘的尺寸與區段。<p>**範例提示：**</p><ul><li>「為什麼週二收入會激增？」</li><li>「是什麼原因導致這個月的工作階段發生變更？」</li></ul><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [準備業務績效評論](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 將受信任的量度轉換為已說明的效能故事，其中包含發現的專案和建議的後續步驟。<p>**範例提示：**</p><ul><li>「給我上個月的執行摘要」</li><li>「領導團隊的績效摘要」</li></ul><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [量度標題的預測](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 從歷史資料中專案量度，以便您檢視即將到來的遺漏。<p>**範例提示：**</p><ul><li>「未來30天的預測工作階段」</li><li>「我們是否可望達成收入目標？」</li></ul><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [建立自訂Customer Journey Analytics技能](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 將您重複的分析轉換為可重複使用的技能，並持續存在於各個工作階段。<p>**範例提示：** 「將此每週收入分析變成可重複使用的技能」</p><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例也需要「管理技能」許可權。</p><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [跨市場重複成功的分析](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 跨品牌、地區或業務單位套用實證分析方法。<p>**最適合：**&#x200B;分析人員</p><p>**範例提示：** 「針對EMEA資料檢視執行我的每週funnel技能」</p><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for the root cause analysis skills, `cja-executive-summary`, forecasting with `cja` and `aa`, and `cja-skill-creator` for creating skills. All are listed in the Skills and limitations table and in workflows.md. Medium for mapping Repeat successful analysis across markets to `cja-skill-creator`: the row describes running a saved skill, which is inferred. workflows.md also lists `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, and `cja-reporting` for executive summaries. They're left out because they look org-specific. Confirm with the PM. -->

Co-worker會針對本文所述的使用案例使用下列技能。 如需所有分析技能的清單，包括所需許可權及未涵蓋的內容，請參閱「使用同事聊天分析資料」中的[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用於 |
| --- | --- |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 探索趨勢和根本原因<br>說明量度移動的原因 |
| `cja-executive-summary` | 準備業務績效審查 |
| `cja`, `aa` | 量度標題的預測 |
| `cja-skill-creator` | 建立自訂Customer Journey Analytics技能<br>跨市場重複成功的分析 |

## 取得更好結果的秘訣

* 為要調查的變更的度量和期間命名。 根本原因分析適用於已知期間內的已知量度。
* 如果您想要劃分量度變更，請詢問貢獻維度。
* 在預測量度時要求預測總時程，例如「未來30天」。
* 指定摘要的對象，例如領導或行銷團隊，如果您打算展示發現，請要求投影片投影片大綱。
* 請先完成分析，然後要求「同事聊天」將其儲存為技能。 為技能提供一個清楚的描述性名稱，並記下您計畫重複使用它的頻率。

## 後續步驟

* 如需使用「同事聊天」進行資料分析的概觀，包括其他分析網域和最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要檢視進行中的根本原因分析，請參閱[Customer Journey Analytics與同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。
