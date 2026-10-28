---
title: 透過同事聊天詢問有關您內容的問題
description: 透過簡單的語言向同事詢問您的內容（從一般到具體），且無需分析人員專業知識即可獲得準確的Content Analytics答案。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 2%
---

# 提出有關您內容的問題

<!-- FLAG: Confirm with the PM: (1) availability (GA, beta, or experimental) and whether this page needs an AVAILABILITY note or `hide: true` until launch, and (2) any required Coworker entitlement. Content Analytics itself has no separate permission: users get access through data views that are configured for Content Analytics (Access control section of analytics-platform.en/help/content-analytics/config/configuration.md). -->

>[!AVAILABILITY]
>
>本文所述的功能處於發行的有限測試階段，可能尚未在您的環境中提供。 當功能正式可用時，將移除此附註。

使用Adobe CX Enterprise Coworker Chat從Adobe Content Analytics取得有關您內容的正確答案。 提出特定問題，例如「哪些影像吸引上季最多營收？」，或一般問題，例如「我應該將哪種內容列為優先順序？」 同事會將您的問題轉換為可靠的分析。

同事瞭解Content Analytics資料的架構，並套用經驗豐富的分析師所適用的報表規則，因此行銷人員和其他業務使用者不需深入瞭解Content Analytics專業知識，便可取得可靠的結果。

如需其他內容效能使用案例，請參閱[內容效能概觀](/help/chat/use-cases/data-insights/content-performance.md)。

**最佳對象：**&#x200B;業務使用者、分析人員

## 先決條件

<!-- FLAG: Confidence: High. The first two bullets match the other data insights pages. The third bullet follows the Content Analytics docs in analytics-platform.en: Content Analytics components are available only in data views that are configured for Content Analytics (report/report.md), and there's no separate Content Analytics permission (config/configuration.md). -->

若要就您的內容提出問題，您需要：

* 同事聊天已連線至您的Customer Journey Analytics資料檢視。 請參閱[開始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析資料。
* 檢視對您要分析之資料檢視的存取權。 同事聊天會從Customer Journey Analytics繼承您的許可權。
* 為Content Analytics設定的資料檢視。 請參閱Customer Journey Analytics指南中的[設定Content Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/content-analytics/configuration/configuration)。

## 提出內容問題

1. 登入同事。

1. 選取&#x200B;**[!UICONTROL 新增聊天]**。

1. 在文字欄位中，提出有關您內容的問題。 例如：

   **提示**

   > 我應該優先處理哪些內容？

   <!-- FLAG: The skill includes activation words and phrases, but they weren't provided. Confirm with the PM whether customers need to use specific words to trigger the skill, or whether any content question routes to it automatically. If specific words are needed, list them here. -->

   同事使用`analyze-content`技能來回答內容問題。

1. （視條件而定）如果您的問題可由多種解釋所接受，請回答Co-worker詢問的澄清問題，例如您指的是哪些內容型別、頻道或日期範圍。

1. 檢閱結果。

1. （可選）在同一次交談中詢問後續問題以更深入瞭解，或在Analysis Workspace中開啟視覺效果以取得更多手動控制。 請參閱[在Analysis Workspace中開啟視覺效果](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)。

## 提示範例

下表顯示不同型別的內容問題的範例提示。 以這些區段為起點，並根據您自己的內容進行調整。

| 問題的類型 | 提示範例 |
| --- | --- |
| 廣泛或探索 | <ul><li>「我應該將哪些內容排定優先順序？」</li><li>「我們的內容表現如何？」</li></ul> |
| 屬性層級 | <ul><li>「我們表現最佳的影像有哪些共同點？」</li><li>「哪些內容屬性吸引最多人參與？」</li></ul> |
| 收入與轉換 | <ul><li>「哪些影像帶來的上一季收入最多？」</li><li>「https://www.example.com/images/spring-sale.jpg的影像帶來多少收入？」</li></ul> |
| 管道和受眾 | <ul><li>「在行動應用程式和網站上，哪些創意主題會勝出？」</li><li>「哪些影像適用於首次瀏覽的訪客？」</li></ul> |

## 同事如何回答內容問題

<!-- FLAG: Confidence: High for the list of what the skill includes, metric matching, filtering pages by Experience ID, and choosing an attribution model per question (sourced from the PM's skill description and feature summary). Medium for the remaining details, which combine the skill description with the Content Analytics component reference in the Customer Journey Analytics guide. The skill's specific query defaults, attribution models, and visualization rules weren't provided. Confirm with the PM before adding them. -->

同事會以`analyze-content`技能回答內容問題，其中包括下列內容與護欄。 技能會與`cja`技能配對，並透過相同的Customer Journey Analytics工具對您的Customer Journey Analytics資料檢視執行所有查詢。

### 查詢預設值和澄清問題

如果您的問題遺漏了詳細資訊，則該技能會套用合理的預設值。 如果技能不確定您的意思，它會詢問澄清的問題，而不是猜測。

### 資產和體驗的量度比對

<!-- FLAG: The SME confirmed (October 2026) that the skill doesn't support paid media yet. Support is planned, either in this skill or in a separate add-on skill (not decided). When it ships, add paid media here: paid media content uses separate summary metrics, such as Impressions, Clicks, and Spend with a reporting-level suffix (for example, Clicks | Asset Summary), that can't be combined with event metrics such as Asset Views (config/paid-media.md in analytics-platform.en). -->

Content Analytics追蹤兩種內容：資產和體驗。 每個報表都有各自的量度。 技能一律會將量度與您詢問的內容型別配對。

| 內容類型 | 簡介 | 技能使用的量度 |
| --- | --- | --- |
| 資產 | 個別內容片段，例如影像 | 資產檢視、資產點按、資產點進率(CTR) |
| 體驗 | 在網頁或行動應用程式中包含文字和資產的內容容器 | 體驗檢視、體驗點按、體驗點進率(CTR) |

### Content Analytics資料架構

此技能瞭解Content Analytics資料的結構。 例如：

* **體驗ID：**&#x200B;當您詢問特定頁面時，會依識別該頁面的內容體驗ID來篩選技能。
* **AI產生的屬性：**&#x200B;每個資產和體驗都由屬性描述，例如攝影風格、色彩、色調和說服策略。 此技能會使用這些屬性來解釋內容表現良好的原因，而不只是哪些內容表現良好。

如需完整的元件清單，請參閱Customer Journey Analytics指南中的[Content Analytics元件](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/content-analytics/report/components)。

### 歸因

此技能會選擇適合您問題的歸因模型。 例如，有關影像點選的問題與有關該影像貢獻了多少收入的問題有不同的回答。 如需詳細資訊，請參閱Customer Journey Analytics指南中的[歸因模型](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/attribution/models#attribution-models)。

### 常見分析和工作流程

此技能包括常見內容分析的指示，例如：

* 尋找表現最好的資產或體驗的共同屬性。
* 將內容曝光率與轉換次數和收入掛鉤。
* 比較網路和行動裝置頻道中的內容。
* 比較哪些內容適用於不同的受眾和區段。
* 識別過度使用或使用不足的內容。

### 視覺效果

此技能會選取符合您問題和資料的視覺效果，以便輕鬆閱讀和分享結果。

## 取得更好結果的秘訣

* 如果您不確定要問什麼，請開始廣泛討論。 同事可以將一般問題轉換為重點分析，而您可以從中進行細分。
* 說明您是否知道想要個別資產（例如影像）或整個體驗（例如頁面）。
* 當您詢問特定影像時，請包含其URL或資產ID。 同事無法透過其在頁面上的角色識別影像，例如主圖影像或橫幅。
* 命名您要分析的量度和日期範圍，例如上一季的收入。
* 指定您要比較的區段、對象或管道。
* 當您想知道內容表現為何時，請詢問內容屬性，例如影像、主題或訊息，而不是個別檔案。
* 如果您一律分析相同的資料檢視，請將您偏好的資料檢視新增至「同事聊天」記憶體。 請參閱[在記憶體](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)中新增資料檢視或報表套裝偏好設定。

## 後續步驟

* 如需更多內容效能使用案例，請參閱[內容效能概觀](/help/chat/use-cases/data-insights/content-performance.md)。
* 若要深入瞭解Content Analytics，請參閱Customer Journey Analytics指南中的[Content Analytics概觀](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/content-analytics/content-analytics)。
* 如需使用同事聊天進行資料分析的概觀，包括最佳實務，請參閱[使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-overview.md)。
