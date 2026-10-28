---
title: 透過同事聊天比較受眾和客戶區段
description: 使用同事聊天來比較客戶群組、尋找被忽略的成長機會、追蹤對象趨勢，以及將深入分析轉換為您可建立的對象。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%
---

# 對象和區段分析概觀

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

使用Adobe CX Enterprise Coworker Chat瞭解哪些客戶群組有不同行為以及如何進行，以便您能聚焦於最重要的客戶群組。 並排比較頻道、時段和區段，追蹤對象在一段時間內的變化，並將您找到的內容轉變為您可建立的對象。

對象和區段分析是Co-worker Chat中的數個分析網域之一。 若要檢視所有網域，請參閱「使用同事聊天分析資料」中的[開始在同事聊天中分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最佳對象：**&#x200B;分析師、業務使用者

## 先決條件

<!-- FLAG: Confidence: High for the shared bullets (sourced from the Skills and limitations table and analytics-chat.md). Medium for the "Additional prerequisite" notes on the operational trends rows in the Use cases table: workflows.md lists the operational time-series skill as available for "All Eligible Applications" but doesn't state required permissions. Mapping Track audience size trends to the same requirement is inferred. Low for the "Additional prerequisite" note on the Take an insight into an audience row: inferred from the Audiences section of workflows.md, which lists Real-Time CDP as the application for audience creation. Confirm with the PM. -->

若要使用此頁面上的使用案例，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視或Adobe Analytics報表套裝。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析的資料檢視或報表套裝的存取權。 同事聊天會從Customer Journey Analytics或Adobe Analytics繼承您的許可權。

## 使用案例

| 使用案例 | 函數 |
| --- | --- |
| [比較效能](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 並排比較不同管道、時段或區段的量度。<p>**範例提示：** 「按管道月份比較收入」</p><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [比較客戶群組](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 顯示哪些群組的行為不同，而不需要您編寫區段邏輯。<p>**最佳對象：**&#x200B;商務使用者</p><p>**範例提示：**</p><ul><li>「付費社交訪客的轉換方式是否與電子郵件不同？」</li><li>「比較收入中的新訪客和回訪訪客」</li></ul><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| 尋找被忽略的增長機會 | 探索受眾、歷程和管道，以找出整體效能數字可以隱藏的機會。<p>**範例提示：**</p><ul><li>「哪些受眾轉換率高於平均水準，但只有很少的流量？」</li><li>「哪些管道的轉換率使用率偏低？」</li></ul> |
| [分析營運趨勢與原因](/help/chat/use-cases/workflows.md#data-insights) | 查詢對象、資料集和歷程的歷史時間序列資料，並識別導致變更的原因。<p>**最佳對象：**&#x200B;管理員、分析師</p><p>**範例提示：** 「顯示過去90天的對象人數趨勢」</p><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例也需要存取您要分析的對象、資料集或歷程。</p><p>如需詳細資訊，請參閱同事聊天使用案例中的[資料深入分析](/help/chat/use-cases/workflows.md#data-insights)。</p> |
| 追蹤對象人數趨勢 | 找出人數增加或減少的受眾，並找出原因。<p>**最佳對象：**&#x200B;管理員、分析師</p><p>**範例提示：** 「本季哪些對象成長最快？」</p><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例也需要存取您要追蹤的對象。</p> |
| 將insight帶入受眾 | 從insight進入您可以建立的對象，無需重新開始。<p>**範例提示：**</p><ul><li>「在Analysis Workspace中開啟此比較」</li><li>「協助我建立此群組的對象」</li></ul><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例也需要存取Real-Time Customer Data Platform以及建立對象的許可權。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for Compare performance and Analyze operational trends and causes (skills listed for "Comparative analysis" and "Operational time-series & causal analysis" in workflows.md). Medium for Compare customer groups and Track audience size trends, which are mapped to the same skills based on their descriptions. Low for `audience-creation-flow`: inferred from the Audiences section of workflows.md. No skill is listed for Find overlooked growth opportunities because no source names one. Only `cja`, `aa`, and the root cause analysis skills currently appear in the Skills and limitations table on analytics-overview.md. -->

Co-worker會針對本文所述的使用案例使用下列技能。 如需所有分析技能的清單，包括所需許可權及未涵蓋的內容，請參閱「使用同事聊天分析資料」中的[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用於 |
| --- | --- |
| `cja`, `aa` | 比較績效<br>比較客戶群組 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 比較績效 |
| `operational-stats-causal-analysis` | 分析運作趨勢與原因<br>追蹤對象人數趨勢 |
| `audience-creation-flow` | 將insight帶入受眾 |

## 取得更好結果的秘訣

* 指定您要包含、排除或比較的區段、對象、管道或裝置。
* 依確切名稱參照區段和其他元件。
* 命名您要比較的量度和日期範圍，例如收入月份與月份。
* 如果您想知道為什麼一個群組的行為與另一個群組不同，請詢問貢獻維度。

## 後續步驟

* 如需使用「同事聊天」進行資料分析的概觀，包括其他分析網域和最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要直接在同事聊天中建立對象，請參閱[與同事評估Experience Platform健康狀況，並從自然語言建立對象](/help/chat/use-cases/audiences/create-audience-from-natural-language.md)。
