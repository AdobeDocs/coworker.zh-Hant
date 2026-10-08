---
title: 透過同事聊天分析Customer Journey Analytics資料
description: 瞭解如何使用Adobe CX Enterprise Coworker Chat分析Customer Journey Analytics資料、建立漏斗，並找出客戶在歷程中的流失位置。
hold: true
product_v2:
  internal-label: CX Enterprise Coworker
feature_v2:
  internal-label: CX Enterprise Coworker
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 1%
---

# 透過同事聊天分析資料

本頁資訊提供Adobe CX Enterprise Coworker Chat概觀，以及可如何協助您分析組織的資料。

同事聊天可讓團隊使用自然語言自動化Adobe產品工作，透過彈性規劃、可自訂的技能和智慧型執行，快速將想法轉換為動作。 如需有關同事的一般資訊，請參閱[CX Enterprise Coworker概觀](/help/home.md)。

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## 資料分析的運作方式

Co-worker Chat可以執行進階資料分析，而之前僅能在Analysis Workspace中執行。 Co-worker Chat會存取您Customer Journey Analytics資料檢視或Adobe Analytics報告套裝中的資料，讓您透過自然語言提示探索資料並獲得答案。

同事聊天從Customer Journey Analytics或Adobe Analytics繼承許可權。 您只能存取Analysis Workspace中可供您使用的資料檢視、報表套裝、維度、量度和區段。

當您在同事聊天中建立視覺效果時，您可以隨時在Analysis Workspace中開啟視覺效果，以取得更多手動控制。

## 快速解答與深思熟慮的工作

您可以透過兩種方式使用「同事聊天」，視您需要的分析數量而定：

* **快速解答** — 直接詢問簡單語言的問題，並取得立即的答案。 商務使用者經常以這種方式使用同事聊天，而分析師在需要為利害關係人提供快速答案時也會使用聊天。
* **深思熟慮的工作** — 與同事聊天室進行延伸、多回合的交談，以調查業務問題、排除原因，並取得建議。 分析人員通常會在建議前，使用此方法來深入探索資料。

## 開始在「同事聊天」中分析

首先以簡單的語言描述您想知道的事情。 Co-worker Chat會規劃分析、查詢您的資料檢視或報告套裝，並建立視覺效果和摘要。

下列使用案例會依您想要達成的目標分組。 每個群組都列出最適合的角色。

### 測量績效

**最佳對象：**&#x200B;分析師、業務使用者

| 使用案例 | 函數 |
| --- | --- |
| [分析Customer Journey Analytics和Adobe Analytics資料](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![分析Customer Journey Analytics和Adobe Analytics資料](../../assets/coworker-funnel-response-card.png)</p> | 回答有關資料檢視或報表套裝的自然語言問題、建置漏斗和其他視覺效果，並找出客戶流失的位置。 您可以在Analysis Workspace中開啟任何視覺效果以供進一步分析。<p>**範例提示：** 「顯示過去30天的頁面檢視」</p><p>如需詳細資訊，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。</p> |
| [比較效能](#skills-and-limitations) | 並排比較不同管道、時段或區段的量度。<p>**範例提示：** 「按管道月份比較收入」</p><p>如需詳細資訊，請參閱[技能與限制](#skills-and-limitations)。</p> |
| [測量行銷活動績效](/help/chat/use-cases/overview.md#data-insights) | 瞭解特定期間內的行銷活動、管道和Web屬性的執行方式。<p>**範例提示：** 「上個月我們的Acrobat網路行銷活動的表現如何？」</p><p>如需詳細資訊，請參閱同事聊天使用案例中的[資料深入分析](/help/chat/use-cases/overview.md#data-insights)。</p> |
| [分析漏斗](#skills-and-limitations) | 逐步瞭解多步驟轉換漏斗，並檢視每個階段的流失情況。<p>**最適合：**&#x200B;分析人員</p><p>**範例提示：** 「引導我完成結帳funnel」</p><p>如需詳細資訊，請參閱[技能與限制](#skills-and-limitations)。</p> |

### 瞭解量度變更的原因

**最適合：**&#x200B;分析人員

| 使用案例 | 函數 |
| --- | --- |
| [探索趨勢和根本原因](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![探索趨勢和根本原因](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | 識別Customer Journey Analytics和Adobe Analytics資料中的趨勢，以及推動效能變更的因素，無需手動查詢。<p>**範例提示：** 「為什麼上週轉換率下降？」</p><p>如需詳細資訊，請參閱[Customer Journey Analytics與同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。</p> |
| [分析營運趨勢與原因](/help/chat/use-cases/overview.md#data-insights) | 查詢對象、資料集和歷程的歷史時間序列資料，並識別導致變更的原因。<p>**最佳對象：**&#x200B;管理員、分析師</p><p>**範例提示：** 「顯示過去90天的對象人數趨勢」</p><p>如需詳細資訊，請參閱同事聊天使用案例中的[資料深入分析](/help/chat/use-cases/overview.md#data-insights)。</p> |

### 預測未來的效能

**最適合：**&#x200B;分析人員

| 使用案例 | 函數 |
| --- | --- |
| [預測量度](#skills-and-limitations) | 從歷史Customer Journey Analytics或Adobe Analytics資料中專案未來的量度值，例如您是否有望達到收入目標。<p>**範例提示：** 「未來30天的預測工作階段」</p><p>如需詳細資訊，請參閱[技能與限制](#skills-and-limitations)。</p> |

### 與利害關係人分享見解

**最佳對象：**&#x200B;分析師、業務使用者

| 使用案例 | 函數 |
| --- | --- |
| [建立執行摘要和KPI摘要](#skills-and-limitations) | 製作適合利害關係人的效能摘要、建議和投影片組大綱。<p>**範例提示：** 「給我上個月的執行摘要」</p><p>如需詳細資訊，請參閱[技能與限制](#skills-and-limitations)。</p> |

### 規劃您的實作或升級

**最佳對象：**&#x200B;管理員

| 使用案例 | 函數 |
| --- | --- |
| [規劃您的實作](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![規劃您的實作](../../assets/ui-guide-6.png)</p> | 建立實施Customer Journey Analytics、從Adobe Analytics升級，或在Edge上設定Content Analytics、Marketing Campaign Analytics或串流媒體集合的個人化逐步計畫。 計畫包含如擁有者、工作量估算、相依性和驗證步驟等詳細資訊。<p>**範例提示：** 「協助我規劃Customer Journey Analytics的實作」</p><p>如需詳細資訊，請參閱[與同事一起規劃實作](/help/chat/use-cases/data-insights/implementation-guide.md)。</p> |
| [產生實作檢查清單](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![產生實作檢查清單](../../assets/data-validation-aa-cja/date-detail.png)</p> | 將您的Customer Journey Analytics實作計畫轉換為同事專案中的檢查清單，您的團隊可以在其中指派步驟、追蹤狀態和新增核准閘門。<p>如需詳細資訊，請參閱[與同事專案產生實作檢查清單](/help/chat/use-cases/data-insights/intelligent-checklist.md)。</p> |

### 確認您的資料準確

**最佳對象：**&#x200B;管理員

| 使用案例 | 函數 |
| --- | --- |
| [從Adobe Analytics升級至Customer Journey Analytics時驗證資料](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![從Adobe Analytics升級至Customer Journey Analytics時驗證資料](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | 比較Adobe Analytics報表套裝與Customer Journey Analytics資料檢視之間的維度、量度和趨勢，然後建議修正以支援您的升級。<p>**最佳對象：**&#x200B;管理員、分析師</p><p>**範例提示：** 「將我的AA報告套裝與我的CJA資料檢視進行比較」</p><p>如需詳細資訊，請參閱[從Adobe Analytics升級至Customer Journey Analytics時，與同事驗證資料](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)。</p> |
| [驗證您的串流媒體實作](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![驗證您的串流媒體實作](../../assets/ui-guide-8.png)</p> | 檢查您的資料流、結構、資料集、資料檢視和工作階段資料，確認已正確設定串流媒體追蹤並收集資料。<p>**範例提示：** 「我的串流媒體實施整體狀況如何？」</p><p>如需詳細資訊，請參閱[與同事驗證您的串流媒體實作](/help/chat/use-cases/data-insights/streaming-media-validation.md)。</p> |
| [驗證Customer Journey Analytics的資料集品質](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![驗證Customer Journey Analytics的資料集品質](../../assets/data-validation-aep/dataset-validation.png)</p> | 識別摘要提供Customer Journey Analytics報告的資料集，然後檢查結構描述、身分品質和欄位品質，以便在建立儀表板之前解決問題。<p>如需詳細資訊，請參閱[在同事中使用資料驗證技能驗證Customer Journey Analytics資料](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)。</p> |
| [擷取到Experience Platform後驗證資料](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![擷取到Experience Platform後驗證資料](../../assets/data-validation-aep/null-values.png)</p> | 對Experience Platform資料集和欄位執行統計和語意檢查，以尋找資料品質問題，例如無效值或對應問題。<p>**範例提示：** 「驗證資料集Electronics Sample 1000」</p><p>如需詳細資訊，請參閱[與同事驗證您的Experience Platform資料](/help/chat/use-cases/data-insights/data-validation-aep.md)。</p> |

### 自動化您重複的分析

**最適合：**&#x200B;分析人員

| 使用案例 | 函數 |
| --- | --- |
| [建立自訂Customer Journey Analytics技能](#skills-and-limitations) | 將您重複的分析轉換為可重複使用的技能，並持續存在於各個工作階段。<p>**範例提示：** 「將此每週收入分析變成可重複使用的技能」</p><p>如需詳細資訊，請參閱[技能與限制](#skills-and-limitations)。</p> |

如需關於這些使用案例的詳細資訊，包括他們使用的技巧和更多範例提示，請參閱[資料深入分析使用案例](/help/chat/use-cases/overview.md#data-insights)。

## 技能和限制

下列技能適用於分析Customer Journey Analytics或Adobe Analytics資料。

| 技能 | 使用它可以 | 必要權限 | 超出範圍 |
| --- | --- | --- | --- |
| `cja`, `aa` | 即時查詢Customer Journey Analytics資料檢視(`cja`)或Adobe Analytics報表套裝(`aa`)：<ul><li>提取量度、維度、區段、資料檢視和報告套裝</li><li>並排比較頻道、時段或區段</li><li>執行多步驟funnel和流失分析</li><li>根據歷史趨勢的預測量度</li></ul> | 檢視對您要查詢之資料檢視或報表套裝的存取權 | <ul><li>建立或編輯資料檢視或報表套裝元件</li><li>資料檢視或您有權存取的報告套裝之外的資料</li><li>超越量度預測的預測性模型</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 調查量度變更的原因，而不僅僅是報告其已變更：<ul><li>調查已知時段內已知量度的變更</li><li>對造成變更的尺寸與區段進行曲面處理</li></ul> | 檢視對所分析資料檢視或報表套裝的存取權 | <ul><li>偵測您未詢問的異常（無自動或即時警報）</li><li>針對您有權存取的資料檢視或報表套裝外部量度的根本原因分析</li></ul> |
| `cja-executive-summary` | 製作利害關係人就緒的資料摘要：<ul><li>摘要指定期間的效能</li><li>根據資料產生規範性建議</li><li>投影片投影片或利害關係人閱讀的概要內容</li></ul> | 檢視摘要中涵蓋的資料檢視或報表套裝存取權 | <ul><li>建立最後的投影片單元或簡報檔案</li><li>跨越您無權存取的資料檢視或報表套裝的摘要</li></ul> |
| `aa-cja-validation` | 比較、稽核及調解[!DNL Adobe Analytics]與Customer Journey Analytics之間的資料：<ul><li>比較報表套裝和資料檢視之間的量度值</li><li>標示兩個資料來源之間的差異</li></ul> | 檢視對正在比較的[!DNL Adobe Analytics]報表套裝和Customer Journey Analytics資料檢視的存取權 | <ul><li>解決資料差異的根本原因</li><li>驗證[!DNL Adobe Analytics]和Customer Journey Analytics以外的資料來源</li></ul> |
| `cja-skill-creator` | 將您已掌握的分析變成可重複使用的技能：<ul><li>將完成的分析轉換為已命名且可重複使用的技能</li><li>讓儲存的技能可用於未來的聊天工作階段</li></ul> | 管理技能 | <ul><li>自動與其他使用者共用已儲存的技能（組織層級技能庫需要管理員設定）</li><li>編輯技能參照的資料檢視或報告套裝元件</li></ul> |

## 使用同事聊天分析資料的最佳實務

### 組織層級最佳實務

* 指定貴組織的分析人員為同事達人。

* 建立與使用者可用的資料和元件相關的已稽核提示和技能資料庫。

* 建立一或多個技能，指示「同事聊天」只使用您要在分析中使用的元件。 這可幫助「同事聊天」為您組織中的使用者提供最相關的資料。

* 教育使用者何時向同事聊天詢問快速解答，以及何時將其用於深入思考工作。

### 使用者層級最佳實務

* 使用計畫模式。

  此模式在複雜任務中特別有用，但也可以為簡單任務產生更好的結果，因為它允許同事在採取行動之前提出後續問題。 如需詳細資訊，請參閱[計畫模式](/help/chat/ui-guide.md#plan-mode)。

* 建立提示時，請儘可能具體一些：

  * 命名您要分析的維度、量度和日期範圍。
  * 依元件的確切名稱參照元件。
  * 指定您要包含、排除或比較的任何區段、對象、管道或裝置。
  * 指出您想要特定的視覺效果型別，例如funnel、趨勢或同類群組表格。
  * 如果您希望「同事聊天」提供後續問題的建議，請詢問建議的後續步驟。
  * 在預測量度時要求預測總時程，例如「未來30天」。
  * 提及您已擁有的任何假設，以便「同事聊天」可驗證或排除該假設。
  * 如果您想要劃分量度變更，請詢問貢獻維度。
  * 指定摘要的對象，例如領導或行銷團隊，如果您打算展示發現，請要求投影片投影片大綱。
  * 為驗證資料時您想要比較的特定報表套裝和資料檢視命名。
  * 先完成分析，然後要求「同事聊天」將其儲存為技能，提供清楚的描述性名稱，並記下您計畫重複使用分析的頻率。

* 將標準方向新增至Co-worker Chat記憶體。 例如，如果您一律使用相同資料檢視或報表套裝的資料，請將其新增至記憶體。 如需詳細資訊，請參閱「開始使用同事聊天分析資料」中的[在記憶體](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)中新增資料檢視或報告套裝偏好設定。

## 後續步驟

若要設定同事聊天並逐步瀏覽工作範例，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。


