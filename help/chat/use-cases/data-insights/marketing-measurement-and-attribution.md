---
title: 透過同事聊天來衡量行銷影響和歸因
description: 使用「同事聊天」來評估每個管道的遞增影響、尋找支出飽和之處、建立假設預算案例，以及檢查行銷模型品質。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 2%
---

# 行銷測量與歸因概觀

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat瞭解每個行銷管道和行銷活動的累加影響，以便您可以分配支出以最佳化ROI。 瞭解管道如何共同運作、額外支出停止支付的地方，以及在確認前不同的預算分配比較方式。

行銷測量和歸因是Co-worker Chat中的幾個分析網域之一。 若要檢視所有網域，請參閱「使用同事聊天分析資料」中的[開始在同事聊天中分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最佳對象：**&#x200B;分析師、業務使用者

## 先決條件

<!-- FLAG: Confidence: High for the shared bullets (sourced from analytics-chat.md and the Skills and limitations table). They're confirmed for Measure campaign performance only; whether the marketing mix modeling use cases also need a data view or report suite connection is unknown. Low for the "Additional prerequisite" notes on the four marketing mix modeling rows in the Use cases table: incremental impact, response curves, budget scenarios, and model retraining describe a marketing mix model, but no source names the product or data that these use cases need. It could be Adobe Mix Modeler or Marketing Campaign Analytics (listed as an implementation path in implementation-guide.md). Confirm with the PM before publishing. -->

若要使用此頁面上的使用案例，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視或Adobe Analytics報表套裝。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析的資料檢視或報表套裝的存取權。 同事聊天會從Customer Journey Analytics或Adobe Analytics繼承您的許可權。

## 使用案例

| 使用案例 | 函數 |
| --- | --- |
| 探索每個管道的遞增影響 | 顯示每個管道的增量值、管道相互擴增的方式，以及外部因素的作用。<p>**範例提示：**</p><ul><li>「哪些頻道帶來最多遞增的轉換？」</li><li>「付費搜尋與顯示如何互相放大？」</li></ul><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例還需要經過訓練的行銷測量模型。 *[需要確認的產品和安裝程式需求。]*</p> |
| 找出支出開始飽和的位置<p>![尋找支出開始飽和的位置](assets/marketing-measurement.png)</p> | 顯示可顯示額外支出停止支付情形的回應曲線。<p>**範例提示：**</p><ul><li>「付費搜尋花費從哪裡開始飽和？」</li><li>「顯示每個頻道的回應曲線」</li></ul><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例還需要經過訓練的行銷測量模型。 *[需要確認的產品和安裝程式需求。]*</p> |
| 建立假設預算案例 | 並排比較配置選項以支援計畫決策。<p>**最佳對象：**&#x200B;商務使用者</p><p>**範例提示：**</p><ul><li>「建立下一季的預算案例」</li><li>「如果我將10%的支出從顯示區轉移到搜尋區，該怎麼辦？」</li></ul><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例還需要經過訓練的行銷測量模型。 *[需要確認的產品和安裝程式需求。]*</p> |
| 檢查模型品質以及何時重新訓練 | 檢查模型品質、訓練詳細資料和評分量度，讓您瞭解該信任某個答案的程度。<p>**最適合：**&#x200B;分析人員</p><p>**範例提示：**</p><ul><li>「這個模式是否需要其他因素？」</li><li>「這個模型需要重新訓練嗎？」</li></ul><p>**其他先決條件：**&#x200B;除了[一般先決條件](#prerequisites)之外，此使用案例還需要經過訓練的行銷測量模型。 *[需要確認的產品和安裝程式需求。]*</p> |
| [測量行銷活動績效](/help/chat/use-cases/workflows.md#data-insights) | 瞭解特定期間內的行銷活動、管道和Web屬性的執行方式。<p>**範例提示：** 「上個月我們的Acrobat網路行銷活動的表現如何？」</p><p>如需詳細資訊，請參閱同事聊天使用案例中的[資料深入分析](/help/chat/use-cases/workflows.md#data-insights)。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for Measure campaign performance (workflows.md lists `cja`, `aa`, `dx-api`, and `knowledge-graph` for "Campaign performance"). `dx-api` and `knowledge-graph` aren't in the Skills and limitations table on analytics-overview.md. Low for the other four use cases: no source names their skills. Get the skill IDs from the PM, replace the placeholder row, and add the skills to the Skills and limitations table. -->

Co-worker會針對本文所述的使用案例使用下列技能。 如需所有分析技能的清單，包括所需許可權及未涵蓋的內容，請參閱「使用同事聊天分析資料」中的[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用於 |
| --- | --- |
| `cja`, `aa`, `dx-api`, `knowledge-graph` | 衡量行銷活動績效 |
| *[要確認的技能]* | 探索每個管道的遞增影響<br>尋找支出開始飽和的領域<br>建立假設預算案例<br>檢查模型品質及何時重新訓練 |

## 取得更好結果的秘訣

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the sample prompts. -->

* 命名您要分析的管道、行銷活動和日期範圍。
* 提及您已擁有的任何假設，例如兩個管道同時合作，讓「同事聊天」可以驗證或排除該假設。
* 說明在建置假設情景時，您想要測試的特定預算轉移，例如將10%的支出從一個管道移至另一個管道。

## 後續步驟

* 如需使用「同事聊天」進行資料分析的概觀，包括其他分析網域和最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要設定同事聊天並逐步瀏覽工作範例，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。
