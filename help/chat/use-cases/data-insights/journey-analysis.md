---
title: 透過同事聊天分析客戶歷程和還車
description: 使用「同事聊天」建立漏斗、尋找客戶流失的位置、診斷轉換下降，以及在分析資料中比較不同期間的歷程。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f1ffc050071fc0ca48ae36c7aea8bc66eff2a147
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 2%
---

# 歷程分析概觀

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat來瞭解客戶從何處退出歷程以進行轉換，以及為何跨管道、裝置和區段。 以簡單的語言描述歷程，Co-worker Chat會建置funnel、顯示每個步驟的流失情況，並幫助您調查原因。

歷程分析是同事聊天中的數個分析網域之一。 若要檢視所有網域，請參閱「使用同事聊天分析資料」中的[開始在同事聊天中分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最佳對象：**&#x200B;分析師、業務使用者

## 先決條件

若要使用此頁面上的使用案例，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視或Adobe Analytics報表套裝。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析的資料檢視或報表套裝的存取權。 同事聊天會從Customer Journey Analytics或Adobe Analytics繼承您的許可權。

## 使用案例

| 使用案例 | 函數 |
| --- | --- |
| [分析Customer Journey Analytics和Adobe Analytics資料](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![分析Customer Journey Analytics和Adobe Analytics資料](../../assets/coworker-funnel-response-card.png)</p> | 回答有關資料檢視或報表套裝的自然語言問題、建置漏斗和其他視覺效果，並找出客戶流失的位置。 您可以在Analysis Workspace中開啟任何視覺效果以供進一步分析。<p>**範例提示：** 「顯示過去30天的頁面檢視」</p><p>如需詳細資訊，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。</p> |
| [尋找客戶流失的地方](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 從簡單明瞭的問題建立funnel，對最大的漏洞進行排名，並提出後續步驟。<p>**最佳對象：**&#x200B;商務使用者</p><p>**範例提示：**</p><ul><li>「在購買的過程中，我們在哪裡失去客戶？」</li><li>「帶我瀏覽funnel結帳」</li></ul><p>如需詳細資訊，請參閱[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| 診斷轉換拒絕 | 調查客戶在哪裡退出，並評估促成變更的原因。<p>**範例提示：**</p><ul><li>「為什麼上週轉換率下降？」</li><li>「網站變更後，客戶從哪裡退出？」</li></ul> |
| 找出流失的原因 | 排除會導致一次一個隔離問題背後的通道、裝置或區段。<p>**範例提示：**</p><ul><li>「在行動裝置或桌上型電腦上放棄購物車的情況更糟糕嗎？」</li><li>「哪些管道在購物車和購買之間洩漏最多？」</li></ul> |
| 比較不同期間的歷程 | 逐步顯示您傳送的變更是否移動了funnel。<p>**最佳對象：**&#x200B;商務使用者</p><p>**範例提示：**</p><ul><li>「比較本季與上季的結帳轉換」</li><li>「重新設計後，我的funnel有什麼改變？」</li></ul> |

## 範例：尋找客戶流失的位置

如需從第一個問題到建議的完整範例交談，請參閱[範例：尋找客戶流失之處](/help/chat/use-cases/data-insights/analytics-chat.md#example-find-where-customers-drop-off) （在「開始使用同事聊天分析資料」中）。

## 使用的技能

<!-- FLAG: Confidence: High for `cja` and `aa` (the Skills and limitations table lists funnel and fallout analysis and side-by-side comparison of time periods). Medium for the root cause analysis skills: workflows.md maps the prompt "Why did conversions drop last week?" to them, but the mapping to the slide rows "Diagnose conversion declines" and "Isolate the cause of a drop-off" is inferred. Confirm with the PM. -->

Co-worker會針對本文所述的使用案例使用下列技能。 如需所有分析技能的清單，包括所需許可權及未涵蓋的內容，請參閱「使用同事聊天分析資料」中的[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用於 |
| --- | --- |
| `cja`, `aa` | 分析Customer Journey Analytics和Adobe Analytics資料<br>找出客戶流失的位置<br>比較不同期間的歷程 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 診斷轉換下降<br>找出下降的原因 |

## 取得更好結果的秘訣

<!-- FLAG: Confidence: High, except the first bullet (Medium), which moved here from Prerequisites and is inferred from how funnel prompts work. The rest are adapted from the best practices in analytics-overview.md. -->

* 命名您要分析的歷程步驟，例如產品頁面、購物車、結帳和購買。
* 為要分析的維度、量度和日期範圍命名，並按其確切名稱參照元件。
* 如果這是您想要看到的內容，請要求funnel或流失視覺效果。
* 指定要包含、排除或比較的區段、頻道或裝置。
* 提及您已擁有的任何假設（例如最近的網站變更），讓「同事聊天」可以驗證或排除該假設。
* 如果您希望「同事聊天」提供後續問題的建議，請詢問建議的後續步驟。
* 需要更多手動控制時，可在Analysis Workspace中開啟任何視覺效果。 請參閱[在Analysis Workspace中開啟視覺效果](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)。

## 後續步驟

* 如需使用「同事聊天」進行資料分析的概觀，包括其他分析網域和最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要設定同事聊天並逐步瀏覽工作範例，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。
