---
title: 透過同事聊天分析內容和Creative效能
description: 使用「同事聊天」來尋找共同的成功內容、將收入歸因於客戶看到的影像，以及比較不同管道和受眾的創意。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: b54085a497ca4bbf0003d5837d816206a4d40396
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 2%
---

# 內容效能概觀

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

透過Adobe CX Enterprise Coworker Chat瞭解哪些內容入選以及入選原因（具體到每個資產的屬性），讓您投資於有效內容。 超越哪些檔案點按以檢視哪些影像、傳送訊息和主題促進跨頻道和受眾的參與和收入。

內容效能是Co-worker Chat中的數個分析網域之一。 若要檢視所有網域，請參閱「使用同事聊天分析資料」中的[開始在同事聊天中分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最佳對象：**&#x200B;商務使用者

## 先決條件

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). High for the third bullet: attribute-level and asset analysis needs Content Analytics components, which are available only in data views that are configured for Content Analytics (report/report.md in analytics-platform.en). This applies whichever skill runs the analysis. It's a shared bullet rather than a table row because it applies to every use case on this page. The paid channel row ("Compare Meta ad creative to our web banners") also needs the Paid Media channel enabled in Content Analytics through an Experience Platform paid media source connector, such as Meta Ads or Google Ads. Comparing paid creative with on-site revenue needs custom tracking-key mapping, because enabling paid media doesn't connect paid media data to site orders or revenue (config/paid-media.md). Add an "Additional prerequisite" note on that row after the PM confirms. -->

若要使用此頁面上的使用案例，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視或Adobe Analytics報表套裝。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析的資料檢視或報表套裝的存取權。 同事聊天會從Customer Journey Analytics或Adobe Analytics繼承您的許可權。
* 為Content Analytics設定的資料檢視。 請參閱Customer Journey Analytics指南中的[設定Content Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/content-analytics/configuration/configuration)。

## 使用案例

| 使用案例 | 函數 |
| --- | --- |
| 找出成功內容的共同點<p>![尋找共同成功內容](assets/content-performance.png)</p> | 顯示哪些影像和傳訊功能在屬性層級運作，而不只是哪些檔案被點按。<p>**範例提示：**</p><ul><li>「我們表現最佳的影像有哪些共同點？」</li><li>「哪些內容屬性吸引最多人參與？」</li></ul> |
| 將收入歸因於客戶看到的內容 | 將影像曝光度與收入、轉換及與演演算法歸因的參與度聯絡起來。<p>**最佳對象：**&#x200B;分析師、業務使用者</p><p>**範例提示：**</p><ul><li>「哪些主圖影像吸引的營收為上一季最多？」</li><li>「此橫幅涉及多少收入？」</li></ul> |
| 比較不同付費和擁有的管道中的創意內容 | 以單一檢視顯示哪些視覺效果和主題在網路、行動和付費頻道中勝出。<p>**範例提示：**</p><ul><li>「哪些創意主題在付費和我們的網站上會勝出？」</li><li>「比較Meta廣告創意與網頁橫幅」</li></ul> |
| 瞭解哪些視覺效果可移動每個受眾 | 顯示哪些視覺效果適合每個對象，以引導個人化和創意簡介。<p>**範例提示：**</p><ul><li>「哪些視覺效果最適合每個區段？」</li><li>「哪些影像適用於首次瀏覽的訪客？」</li></ul> |

## 使用的技能

<!-- FLAG: Confidence: Medium. The `analyze-content` skill is a foundational skill for content questions, so it's listed for every use case on this page. Confirm with the PM that it covers all four. -->

Co-worker會針對本文所述的使用案例使用下列技能。 如需所有分析技能的清單，包括所需許可權及未涵蓋的內容，請參閱「使用同事聊天分析資料」中的[技能與限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用於 |
| --- | --- |
| `analyze-content`, `cja` | 找出成功的內容有哪些共同之處<br>將收入歸因於客戶看到的內容<br>比較不同付費和擁有的管道中的創意<br>瞭解哪些視覺效果會移動每個受眾<p>如需詳細資訊，請參閱[提出有關您內容的問題](/help/chat/use-cases/data-insights/ask-content-questions.md)。</p> |

## 取得更好結果的秘訣

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the row descriptions. -->

* 命名您要分析的量度和日期範圍，例如上一季的收入。
* 指定您要比較的區段、對象或管道。
* 當您想知道內容表現為何時，請詢問內容屬性，例如影像、主題或訊息，而不是個別檔案。

## 後續步驟

* 若要瞭解同事如何回答內容問題，請參閱[提出有關您內容的問題](/help/chat/use-cases/data-insights/ask-content-questions.md)。
* 如需使用「同事聊天」進行資料分析的概觀，包括其他分析網域和最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要設定同事聊天並逐步瀏覽工作範例，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。
