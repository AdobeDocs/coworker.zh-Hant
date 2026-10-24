---
title: 使用Adobe CX Enterprise Coworker Chat分析Analytics資料
description: 使用Adobe CX Enterprise Coworker Chat分析Customer Journey Analytics和Adobe Analytics資料，尋找根本原因，並在Analysis Workspace中開啟結果。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f1ffc050071fc0ca48ae36c7aea8bc66eff2a147
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 1%
---

# 透過同事聊天分析資料

本頁資訊提供Adobe CX Enterprise Coworker Chat概觀，以及可如何協助您分析組織的資料。

同事聊天可讓團隊使用自然語言自動化Adobe產品工作，透過彈性規劃、可自訂的技能和智慧型執行，快速將想法轉換為動作。 如需有關同事的一般資訊，請參閱[CX Enterprise Coworker概觀](/help/home.md)。

## 資料分析的運作方式

Co-worker Chat可以執行進階資料分析，而之前僅能在Analysis Workspace中執行。 Co-worker Chat會存取您Customer Journey Analytics資料檢視或Adobe Analytics報告套裝中的資料，讓您透過自然語言提示探索資料並獲得答案。

同事聊天從Customer Journey Analytics或Adobe Analytics繼承許可權。 您只能存取Analysis Workspace中可供您使用的資料檢視、報表套裝、維度、量度和區段。

當您在同事聊天中建立視覺效果時，您可以隨時在Analysis Workspace中開啟視覺效果，以取得更多手動控制。 請參閱[在Analysis Workspace中開啟視覺效果](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)。

## 快速解答與深思熟慮的工作

您可以透過兩種方式使用「同事聊天」，視您需要的分析數量而定：

* **快速解答** — 直接詢問簡單語言的問題，並取得立即的答案。 商務使用者經常以這種方式使用同事聊天，而分析師在需要為利害關係人提供快速答案時也會使用聊天。
* **深思熟慮的工作** — 與同事聊天室進行延伸、多回合的交談，以調查業務問題、排除原因，並取得建議。 分析人員通常會在建議前，使用此方法來深入探索資料。

## 開始在「同事聊天」中分析

首先以簡單的語言描述您想知道的事情。 Co-worker Chat會規劃分析、查詢您的資料檢視或報告套裝，並建立視覺效果和摘要。

以下使用案例依分析網域分組。 每個網域都有自己的頁面，其中包含使用案例、範例提示、必要條件及其使用的技能。

| 網域 | 您可以做什麼 | 最適合 |
| --- | --- | --- |
| [智慧型實作與管理](/help/chat/use-cases/data-insights/data-governance-and-validation.md) | 設定、移轉及管理您的實作，並確定您可以信任每個答案背後的資料。 | 管理 |
| [歷程分析](/help/chat/use-cases/data-insights/journey-analysis.md) | 瞭解客戶從何處退出轉換歷程，以及為何跨管道、裝置和區段。 | 分析師、業務使用者 |
| [對象和區段分析](/help/chat/use-cases/data-insights/audience-and-segment-analysis.md) | 瞭解哪些客戶群組有不同的行為方式，以便您可以聚焦於最重要的客戶群組。 | 分析師、業務使用者 |
| [企業績效](/help/chat/use-cases/data-insights/business-performance.md) | 瞭解業務狀況、量度移動的原因、前往的位置，以及下一步該做什麼。 | 分析師、業務使用者 |
| [內容效能](/help/chat/use-cases/data-insights/content-performance.md) | 瞭解哪些內容獲勝，以及原因（包括每個資產的屬性），讓您能夠投資於有效內容。 | 業務使用者 |
| [行銷測量和歸因](/help/chat/use-cases/data-insights/marketing-measurement-and-attribution.md) | 瞭解每個行銷管道和行銷活動的累加影響，以便分配支出以最佳化ROI。 | 分析師、業務使用者 |

## 技能和限制

下列技能適用於分析Customer Journey Analytics或Adobe Analytics資料。

| 技能 | 使用它可以 | 必要權限 | 超出範圍 |
| --- | --- | --- | --- |
| `cja`, `aa` | 即時查詢Customer Journey Analytics資料檢視(`cja`)或Adobe Analytics報表套裝(`aa`)：<ul><li>提取量度、維度、區段、資料檢視和報告套裝</li><li>並排比較頻道、時段或區段</li><li>執行多步驟funnel和流失分析</li><li>根據歷史趨勢的預測量度</li></ul> | 檢視對您要查詢之資料檢視或報表套裝的存取權 | <ul><li>建立或編輯資料檢視或報表套裝元件</li><li>資料檢視或您有權存取的報告套裝之外的資料</li><li>超越量度預測的預測性模型</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 調查量度變更的原因，而不僅僅是報告其已變更：<ul><li>調查已知時段內已知量度的變更</li><li>對造成變更的尺寸與區段進行曲面處理</li></ul> | 檢視對所分析資料檢視或報表套裝的存取權 | <ul><li>偵測您未詢問的異常（無自動或即時警報）</li><li>針對您有權存取的資料檢視或報表套裝外部量度的根本原因分析</li></ul> |
| `cja-executive-summary` | 製作利害關係人就緒的資料摘要：<ul><li>摘要指定期間的效能</li><li>根據資料產生規範性建議</li><li>投影片投影片或利害關係人閱讀的概要內容</li></ul> | 檢視摘要中涵蓋的資料檢視或報表套裝存取權 | <ul><li>建立最後的投影片單元或簡報檔案</li><li>跨越您無權存取的資料檢視或報表套裝的摘要</li></ul> |
| `analyze-content`<!-- FLAG: Confirm the Out of scope items with the PM. --> | 在Customer Journey Analytics中使用Content Analytics資料來回答有關您內容的一般或特定問題：<ul><li>找出哪些表現最佳的資產和體驗的共同點</li><li>將內容曝光與轉換和收入聯絡起來</li><li>比較不同管道和受眾的內容</li></ul>如需詳細資訊，請參閱[提出有關您內容的問題](/help/chat/use-cases/data-insights/ask-content-questions.md)。 | 檢視對針對Content Analytics設定的資料檢視的存取權 | <ul><li>設定或設定Content Analytics</li><li>Content Analytics未收集的內容</li></ul> |
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

* 若要設定同事聊天並逐步瀏覽工作範例，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。
* 若要檢視每個同事聊天工作流程及其背後的技能，請參閱[同事聊天工作流程](/help/chat/use-cases/workflows.md)。


