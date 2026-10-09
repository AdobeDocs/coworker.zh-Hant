---
description: 瀏覽同事聊天使用案例和範例提示，依資料深入分析、受眾、歷程和平台操作的區域進行整理。
title: 同事聊天使用案例
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 1071cb1d9d08d89592f14f05ec9e32087ad937f3
workflow-type: tm+mt
source-wordcount: '7196'
ht-degree: 6%
---
# 同事聊天使用案例 {#use-cases}

Co-worker Chat可讓您使用自然語言來查詢、分析和處理您的[!DNL Experience Platform]資料，而不需手動導覽多個UI或撰寫查詢。 此頁面提供從業人員最仰賴的使用案例目錄，並按工作區域整理：資料深入分析、對象、歷程、忠誠度、基本元素和沙箱工具。 每個專案都包含它叫用的技能、它使用的應用程式，以及範例提示，您可以複製、調整您自己的資料，並透過對話調整內容。

>[!NOTE]
>
>即將推出：
>
>透過CX Enterprise Coworker的全新AEM代理功能，可協助您更快完成更多工作。
>
>所有符合資格的客戶將可輪流在Co-worker中存取Adobe Experience Manager代理功能。
>
>另請參閱AEM中的[AI - AEM代理功能概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/overview)。

## 品牌體驗

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [更新AEM頁面](brand-visibility/author-web-pages.md) | 執行更新、移除、取代或新增內容元素等動作，讓體驗保持精確且最新。 輸入內容可以是自然語言或視覺化註解，例如PDF或熒幕擷圖。 | `aem-sites-pages-update` | Adobe Experience Manager (AEM) - AEM Sites | 在&lt;URL>將標題更新為Hello World<br><br>在&lt;URL>上將「參加我們的咖啡測驗」按鈕變更為更吸引人的版本<br><br>根據附加的<br><br>在&lt;URL>上更新&lt;URL>我想在頁面底部新增新的Teaser區段，說明我們在8月份進行的促銷活動，購買咖啡機並免費取得2袋咖啡。 同時尋找喝咖啡的朋友的影像，並在Teaser中使用 |
| 大量更新AEM | 同時跨多個頁面執行大量動作，例如移除、取代或新增內容元素，以保持體驗正確且最新。 | `aem-sites-pages-bulkreplace` | Adobe Experience Manager (AEM) - AEM Sites | 在&lt;aem path>上，將包含複製「MyBarista\」的所有頁面更新為「BrewPass」 |
| 從圖表移至視覺內容片段 | 使用自然語言，直接從Figma將設計匯入Adobe Experience Manager。 此技能會自動建立所需的內容模型、內容片段、資產和視覺效果範本，讓業務使用者在數分鐘內從設計移至網頁就緒內容，無需手動設定。 | `aem-sites-visualcontentfragments-create` | Adobe Experience Manager (AEM) - AEM Sites | 從&lt;Figma_URL>匯入 |

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 建立表單 | 從純語言說明、附加的簡報、影像或PDF產生新的調適型表單 | `aem-forms-adaptiveform-create` | Adobe Experience Manager (AEM) - AEM Forms | 「建立員工入門表單」<br><br>「使用附加的簡報（影像或pdf）建立表單」<br><br>「建立&lt;form type>最適化表單」 |
| 編輯/更新表單 | 修改現有表單 — 新增/編輯欄位、調整簡單版面、設定提交動作，或套用附加准則檔案的變更 | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM) - AEM Forms | 「在名字欄位下方新增中間名欄位」<br><br>「將名字和姓氏欄位放在2欄佈局中，50/50」<br><br>「設定表單以傳送資料到REST端點」<br><br>「更新此表單以符合附加的准則檔案」<br><br>「在&lt;現有欄位>欄位下方新增&lt;欄位名稱>欄位」 |
| 新增商業邏輯 | 建立簡單規則，例如根據其他欄位的值顯示或隱藏欄位 | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM) - AEM Forms | 「僅在員工型別為承包商時顯示公司欄位」<br><br>「僅在&lt;其他欄位>為&lt;值>時顯示&lt;欄位>欄位」 |
| 內嵌表單 | 將現有或新建立的表單放置在指定的AEM Sites頁面上（僅支援Edge Delivery Services頁面） | `aem-forms-adaptiveform-embed` | Adobe Experience Manager (AEM) - AEM Forms | &quot;將此表單內嵌到我們網站的首頁上&quot;<br><br>&quot;將此表單內嵌到&lt;page path>&quot; |

**相關資訊**

* [AEM中的代理程式功能：品牌體驗 — 體驗生產 — 網站](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-sites)

* [AEM的代理程式功能：品牌體驗 — 體驗生產 — Forms](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-forms)

### 開發

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 管理Cloud Manager管道 | 建立、執行和監視AEM Cloud Manager管道，包括記錄、成品、變數和設定 | `cloud-manager-pipeline-management` | Adobe Experience Manager (AEM) | 「列出方案12345的管道」<br><br>「我最近管道的狀態如何？」 |
| 管理Cloud Manager環境 | 建立、設定和維護AEM Cloud Manager環境，包括RDE、環境變數、記錄檔和備份 | `cloud-manager-environment-management` | Adobe Experience Manager (AEM) | 列出我的計畫12345環境&quot;<br><br>&quot;重設我的RDE&quot; |
| 管理Cloud Manager計畫 | 列出、檢查和刪除AEM Cloud Manager程式，包括其管道和環境 | `cloud-manager-program-management` | Adobe Experience Manager (AEM) | 「列出我的Cloud Manager程式」<br><br>「取得程式12345的詳細資料」 |
| 管理AEM版本更新排程 | 設定每日無訊息時間和無更新期間以進行自動維護，並檢視Adobe的全域程式碼凍結視窗 | `cloud-manager-release-management` | Adobe Experience Manager (AEM) | 「我目前的無訊息時間視窗是多少？」<br><br>「排程從12月20日至1月2日的無更新期間」 |

**相關資訊**

* [AEM的代理程式功能：品牌體驗 — 開發](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/development/use-cases)

### 上線

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 引導式端對端上線 | 協調完整的入門生命週期、存放庫選擇、委派到資料夾、標籤、中繼資料、匯入和搜尋子技能（如果您不知道您需要的特定入門任務）。 | `aem-onboarding-workflow` | Adobe Experience Manager (AEM) - AEM Assets | 「將我們的團隊加入AEM Assets」<br><br>「帶我瞭解AEM DAM加入」 |
| 設計和建立資料夾階層 | 根據業務需求或CSV輸入，在AEM Assets （在`/content/dam`下）中建議並建立可擴充的資料夾結構。 | `aem-folder-management` | Adobe Experience Manager (AEM) - AEM Assets | 「建議我們生活方式行銷資產的資料夾結構」<br><br>「根據此CSV檔案建立資料夾」 |
| 設計和建立標籤 | 在`/content/cq:tags`下設計和建立控制標籤辭彙 — 名稱空間、階層標籤和批次標籤作業。 | `aem-tag-taxonomy` | Adobe Experience Manager (AEM) - AEM Assets | 「使用我們產品類別的名稱空間設計標籤分類法」<br><br>「從此CSV匯入標籤」<br><br>「在AEM中建立這些階層式標籤」 |
| 建立及指派中繼資料表單 | 從CSV、表格、需求檔案或說明設計並建立作者使用的自訂中繼資料表單（製作UI內容），然後選擇性地將其指派給資料夾。 | `aem-metadata-form` | Adobe Experience Manager (AEM) - AEM Assets | 「從這個欄位清單建立中繼資料表單」<br><br>「將此表單指派到`campaigns`資料夾」 |

**相關資訊**

* [AEM的代理功能：品牌體驗 — 入門](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/onboarding/use-cases)

## 內容顧問

### 內容探索

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 依語意主題搜尋 | 使用AI支援的語意比對功能，依概念、心情或視覺主題尋找資產。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | 「尋找我晨間咖啡生活方式影像」 |
| 依自訂中繼資料搜尋 | 依自訂中繼資料欄位篩選資產（例如Coffee Blend、Brand、Roast Level）。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | 「尋找`Coffee Blend`為`Morning Muse`的資產」<br><br>「取得授權未過期的資產」<br><br>「尋找未設定行銷活動名稱的資產（屬性必須針對適當結果編制索引）。」 |
| 依核准狀態搜尋 | 根據核准狀態篩選資產。 例如，已核准、稽核中、已拒絕或缺少狀態。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | 「顯示`Campaign`資料夾中所有已核准的資產」 |
| 依資料夾/路徑搜尋 | 透過解譯參考AEM中資料夾名稱的自然語言提示來識別資產。 您只需在提示中提及資料夾，無需手動導覽存放庫，即可顯著減少尋找正確內容所需的點按次數。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | 「資料夾`WKND`中是否有任何svg」？<br><br>「在資料夾`WKND`中顯示在2025年11月1日之後修改的資產」 |

**相關資訊**

* [AEM的代理程式功能：內容顧問 — 內容探索](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/discovery/use-cases)

### 內容最佳化

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 高解析度轉譯建立和通道最佳化的轉譯 | 以指定的解析度和品質等級產生資產的新轉譯，讓您無需手動編輯即可輕鬆準備通道就緒的變數。 您也可以根據平台特定需求量身打造轉譯，例如Instagram故事，確保資產自動符合格式、比例和品質准則。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | 「使用`80% quality`建立`2000px`轉譯為`JPEG`」<br><br>「為Instagram故事建立轉譯」 |
| 品牌覆蓋圖與複合圖產生 | 透過精確放置將促銷圖形、覆蓋圖或徽章套用至現有資產，可支援快速建立適用於行銷活動的複合專案。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | 「將含有`30%`折扣圖片的影像覆蓋在促銷橫幅上，從中心放置`100px`」 |
| 影像增強功能、背景色彩調整、方向轉換 | 套用視覺改善（銳利化影像）、取代背景顏色，以及執行方向轉換。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | 「將`PNG`的背景顏色變更為`#ff8932`」<br><br>「銳利化影像」<br><br>「水準映象影像」 |

**相關資訊**

* [AEM中的代理程式功能：內容警告器 — 內容最佳化](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/content-optimization/use-cases)

## 品牌控管

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 指引和區段查閱 | 擷取詳細的品牌指引，依區段、市場或類別設定範圍 | enterprise-context | Adobe Experience Manager (AEM) | 「這個品牌的聲調准則是什麼？」<br>「列出健康情況垂直領域使用的索賠類別」 |
| 根據品牌准則評估內容 | 根據已設定的品牌檢查評估已發佈/編寫的頁面、文字區塊或影像 | aem治理 | Adobe Experience Manager (AEM) | 「根據SecurBank准則評估此登陸頁面」<br>「此標語是否通過我們的語調檢查？」 |
| 偵錯AEM許可權 | 偵錯/瞭解許可權原則、ACL和繼承規則。 | aem治理 | Adobe Experience Manager (AEM) | 「為何主體管理員可以在`https://author/`上寫入`/content/folder/us`？」<br>「為何無法在`https://author`上的`/content/dam`上取樣作者寫入」 |

**相關資訊**

* [AEM的代理程式功能：品牌控管](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-governance/use-cases)

## 資料深入分析

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [提取CJA和AA報告與量度](data-insights/analytics-chat.md) | 即時查詢CJA或AA以提取量度、維度、區段、資料檢視和報告套裝 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「顯示過去30天的頁面檢視」 <br>「列出主要資料檢視中的排名最前的區段」 |
| 比較分析 | 並排比較不同管道、時段或區段的量度 | `cja-root-cause-analysis`, `cja`, `aa-root-cause-analysis`, `aa`, `dx-api`, `knowledge-graph` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「依管道月份和月份比較收入」 <br>「本季行動與案頭轉換看起來如何？」 |
| 行銷活動績效 | 測量在指定期間內行銷活動、管道和Web屬性的執行情形。 | `cja`, `aa`, `dx-api`, `knowledge-graph` | | 「上個月我們的Acrobat網路行銷活動表現如何？」 |
| funnel分析 | 逐步瞭解每個階段都有流失的多步驟轉換漏斗 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「逐步引導我完成結帳funnel」<br>「顯示從PDP到購買的轉換funnel」 |
| 預測 | 根據歷史CJA或AA資料預測未來的量度值 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「預測未來30天的工作階段」 <br> 「我們是否可望達成收入目標？」 |
| [根本原因分析](data-insights/root-cause-analysis.md) | 調查量度變更的原因：診斷下降、尖峰和異常 | `cja-root-cause-analysis`, `aa-root-cause-analysis` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「為什麼上週轉換率下降？」 <br> 「是什麼導致1月15日的收入激增？」 |
| 執行摘要和KPI摘要 | 製作適合利害關係人的效能摘要、規範性建議和投影片組大綱 | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `aa`, `dx-api` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | 「給我上個月的執行摘要」<br>「從這個季度的資料建立投影片投影片組大綱」 |
| [AA ↔ CJA資料驗證](data-insights/data-validation-aa-cja.md) | 在Adobe Analytics和Customer Journey Analytics之間比較、稽核及調解資料，尤其是從Adobe Analytics升級為Customer Journey Analytics時 | `aa-cja-validation`, `cja`, `aa`, `dx-api` | ADOBE ANALYTICS + CJA | 「比較我的AA報告套裝與CJA資料檢視」 <br>「驗證AA與CJA之間的頁面檢視」 |
| [驗證資料集和欄位品質](data-insights/data-validation-aep.md) | 對Experience Platform資料集和欄位執行統計和語意驗證，以在實作後或持續進行時擷取資料品質問題<!--TODO: confirm skill ID(s) with engineering before publishing--> | `data-validation` | Adobe Experience Platform | 「驗證資料集Electronics Sample 1000」 <br>「驗證Customers_2024資料集中的電子郵件欄位」 |
| 作業時間序列與因果分析 | 查詢和分析具有因果歸因的對象、資料集和歷程的歷史時間序列資料 | `operational-stats-causal-analysis` | 所有符合資格的應用程式 | 「顯示過去90天的對象人數趨勢」 <br> 「為什麼我的資料集列計數在3月3日激增？」 |
| 建立自訂CJA技能 | 將分析模式轉換為可重複使用、且跨工作階段儲存的技能 | `cja-skill-creator` | Customer Journey Analytics (CJA) | 「將此每週收入分析轉換為可重複使用的技能」 <br>「將此儲存為每月funnel報告的技能」 |

## 客群

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [從自然語言建立對象](audiences/create-audience-from-natural-language.md) | 透過每個階段的使用者核准，策劃逐步的受眾建立 | `audience-creation-flow` | Real-Time CDP (RTCDP) | 「建立過去30天內購買的使用者受眾」<br>「為加州的高價值忠誠會員建立區段」 |
| 建置PQL定義 | 從XDM屬性、行為事件或現有對象中組合對象定義；支援彙總和時間範圍 | `segment-definition-assembly` | Real-Time CDP (RTCDP) | 「為檢視3個以上產品但未購買的使用者建立PQL」 <br>「為我的事件條件新增7天時段」 |
| 搜尋和尋找對象 | 依ID、名稱、語意搜尋尋找對象；偵測重複專案並分析重疊 | `audience-search` | Real-Time CDP (RTCDP) | 「尋找所有忠誠受眾」<br>「我的『節日購物者』區段是否有重複專案？」 |
| 預估對象規模 | 使用Adobe Experience Platform預覽API搭配輪詢來預估PQL運算式的設定檔觸及率 | `audience-size-estimate` | Real-Time CDP (RTCDP) | 「此對象有多大？」 <br> 「此PQL運算式的預估觸及率」 |
| 對象人數瀑布 | 將PQL分解為子述詞，並顯示每個條件對最終對象規模的貢獻 | `audience-size-waterfall` | Real-Time CDP (RTCDP) | 「顯示此PQL的瀑布圖」 <br> 「劃分每個條件如何減少閱聽眾」 |
| 探索用於定位的XDM欄位 | 依名稱、說明或資料值搜尋欄位；檢視欄位的使用位置和使用位置 | `field-discovery` | Real-Time CDP (RTCDP) | 「我可以使用哪些欄位來鎖定忠誠度客戶？」 <br> 「尋找與購買歷史記錄相關的欄位」 |
| 發佈/儲存對象 | 透過命名慣例和合規性檢查將受眾定義儲存至Experience Platform細分服務 | `audience-publish` | Real-Time CDP (RTCDP) | 「將此專案儲存為草稿」<br>「以『春季促銷買家』名稱發佈對象」 |

## 歷程

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [從自然語言建立歷程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-create){target="_blank"} | 透過文字提示或上傳的影像/流程圖，在AJO中協調歷程建立 | `journey-create` | Adobe Journey Optimizer (AJO) | 「建立歡迎歷程，在註冊後傳送電子郵件、等待3天，然後傳送後續追蹤」 <br> 「從這個上傳的流程圖影像建立歷程」 |
| [分析歷程衝突](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 偵測使用中歷程之間的對象重疊、排程衝突及重複資料刪除問題 | `journey-analyze-conflict` | Adobe Journey Optimizer (AJO) | 「我的購物車放棄歷程是否與其他歷程衝突？」 <br> 「檢查我作用中歷程之間的受眾重疊」 |
| [分析歷程流失](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 識別客戶在歷程中下降的位置和原因，並偵測導致脫離參與的行為模式 | `journey-analyze-fallout` | Adobe Journey Optimizer (AJO) | 「我的重新參與歷程中哪裡有人員離開？」 <br> 「歷程X中的哪些節點流失率最高？」 |
| [分析自訂動作錯誤](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 識別歷程中自訂動作失敗或錯誤率飆升的時間，並在失敗升級為更廣泛的中斷之前診斷根本原因 | `journey-analyze-custom-action` | Adobe Journey Optimizer (AJO) | 「為什麼自訂動作會在我的熟客註冊歷程中失敗？」 <br> 「在我的歡迎歷程中，顯示自訂動作ExternalPush的錯誤率。」 |
| [偵測歷程異常](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 偵測並確認歷程登入、退出或傳送計數時依據歷史基準線的非預期尖峰、下降或平線，並找出可能的根本原因 | `journey-analyze-anomaly` | Adobe Journey Optimizer (AJO) | 「昨天為什麼我的歡迎歷程的專案會中斷？」 <br> 「本週購物車放棄歷程的退出次數尖峰嗎？」 |
| [業務績效分析](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 分析歷程績效並找出績效不佳歷程的具體最佳化機會。 呈現趨勢、瓶頸及導致結果降低的可能原因，讓您提升參與度和轉換率。 獲得可操作的建議，以根據業務績效見解調整歷程設計、目標定位或訊息策略。 | 歷程分析 | Adobe Journey Optimizer (AJO) | 「分析歷程[歷程名稱]的效能並建議最佳化。」<br> 「為什麼歷程[歷程名稱]與上個月相比表現不佳？」 <br> 「我應該進行哪些變更來提高歷程[歷程名稱]的效能？」 <br> 「歷程[歷程名稱]的哪些部分可能會限制轉換或參與？」 |
| [比較歷程版本](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 比較兩個歷程版本，並檢閱節點、連線和歷程層級屬性變更的結構化差異 | `journey-analyze-version-comparison` | Adobe Journey Optimizer (AJO) | 「比較我的歡迎歷程的版本2和3」<br>「這兩個歷程版本之間有何變更？」 |

**相關資訊**

* [使用AI](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}提供Adobe Journey Optimizer中同事和可用技能的概觀。

## Journey Optimizer內容管理


| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [套用品牌指引](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 尋找、選取並套用適用於行銷活動語音、文字、影像、術語和法律指引的核准品牌指引。 | `brand-lookup` | Adobe Journey Optimizer (AJO) | 「提取我們Acme品牌的撰寫與視覺化指引。」 |
| [檢查內容整備](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 針對品牌語調、編輯品質、參與度、清晰度和整備程度，審查行銷活動內容。 | `check-content-readiness` | Adobe Journey Optimizer (AJO) | 「此電子郵件副本是否準備好傳送？ 檢查品牌語調、清晰度、協助工具及法規遵循。」 |
| [協調內容製作](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 規劃、建立、檢閱、分析和儲存支援管道的行銷活動內容。 | `orchestrate-content-authoring` | Adobe Journey Optimizer (AJO) | 「透過這份簡報，針對我們的秋季銷售電子郵件行銷活動執行完整內容製作，然後檢閱並儲存最終的HTML。」 |
| [評估內容設計](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 分析視覺實施、識別版面配置和設計差距，並推薦階層、間距、影像和行動號召的改善專案。 | `assess-content-design` | Adobe Journey Optimizer (AJO) | 「這封電子郵件的視覺效果如何？ 檢查階層、間距、密度、影像和CTA。」 |
| [從Figma建置電子郵件](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 當副本準備出貨時，從即時圖形框架產生最終電子郵件HTML；不需要單獨的版面配置計畫。 | `build-email-from-figma` | Adobe Journey Optimizer (AJO) | 「從此圖形框架建立最終電子郵件HTML；設計中的復本是應該送出的內容。」 |
| [探索內容策略](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 比較接觸點、頻道、對象和訊息主題間的行銷活動策略，並在撰寫前規劃每則訊息。 | `explore-content-strategy` | Adobe Journey Optimizer (AJO) | 「比較單一回呼電子郵件與三點觸控電子郵件及簡訊程式。」 |
| [產生內容](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 為支援的管道撰寫或草擬新的受限制行銷訊息，包括電子郵件、簡訊、推播、WhatsApp和登陸頁面。 | `generate-content` | Adobe Journey Optimizer (AJO) | 「從核准的行銷活動方向建立電子郵件、推播和簡訊的品牌上啟動副本。」 |
| [建立內容簡介](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 將核准的行銷活動方向轉換為優惠方案、色調、關鍵訊息、頻道、地區設定、變體和所需內容的需求。 | `content-brief` | Adobe Journey Optimizer (AJO) | 「將這份簡訊變成給失效美國訂閱者的溫暖回傳電子郵件撰寫需求：截至週日優惠20%，以CTR為KPI。」 |
| [產生影像](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 建立或轉換核准版位的Campaign視覺效果，包括主圖影像、裁切、覆蓋、變體和已簽署的資產。 | `generate-image` | Adobe Journey Optimizer (AJO) | 「使用核准的品牌方向產生此春季銷售電子郵件的優質主圖影像。」 |
| [儲存頻道內容](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 將核准的行銷活動內容儲存為草稿資產，或填寫到AJO或其他支援的動作解決方案的來源範本中。 | `save-channel-content` | Adobe Journey Optimizer (AJO) | 「將核准的內容填入來源範本，並準備進行檢閱。」 |
| [修訂並重新產生內容](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 將已確認的變更套用至現有的行銷活動內容，包括措辭、語調、翻譯、主旨列、行動號召和檢閱發現。 | `revise-regenerate-content` | Adobe Journey Optimizer (AJO) | 「保持已核准的優惠方案和CTA，同時讓語氣升溫。」 |

**相關資訊**

* [使用AI](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}提供Adobe Journey Optimizer中同事和可用技能的概觀。

## 行銷方案

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 建置計畫 | 將現有的方案範本調整至新方案，利用從簡單語言說明或上傳的簡報產生的Smart Campaigns、排程和預留位置電子郵件 | `build-programs` | Adobe Marketo Engage | 「為我們8月產品示範建立網路研討會註冊計畫」<br><br>「建立當潛在客戶點選50分時觸發的計畫」<br><br>「為未作用中的90天潛在客戶建立3封電子郵件的重新參與系列」 |
| 從簡短的演講中站起程式 | 將純語言簡介或上傳的行銷活動檔案轉換為有效程式：複製最接近的相符範本、保留Smart Campaigns和Token，並更新事件詳細資料。 新的Smart Campaigns保持停用以供您檢閱 | `build-programs` | Adobe Marketo Engage | 「我即將於9月10日在芝加哥舉辦網路研討會。 為我設定程式&quot;<br><br>&quot;從此簡報設定下個月的路演程式並更新活動權杖&quot; |
| 複製並調整現有程式 | 複製新城市、季度或地區的先前方案，並更新日期、代號和命名。 子項智慧型行銷活動會移轉並維持停用狀態，直到您啟動為止 | `build-programs` | Adobe Marketo Engage | 「在10月17日複製我們紐約站的上季活動計畫，並更新日期與代號」<br><br>「複製我們英國受眾的芝加哥路演計畫」 |
| 使用資格邏輯建置Smart Campaign | 建立觸發器或批次Smart Campaign、新增智慧清單規則（例如「填寫表單」或「達到分數」），並設定流程步驟（例如「傳送電子郵件」） | `build-programs` | Adobe Marketo Engage | 「建立觸發行銷活動，在潛在客戶填寫「聯絡我們」表單時傳送我們的歡迎電子郵件」<br><br>「為點選50分的潛在客戶建立批次行銷活動並新增「傳送電子郵件」步驟」 |

## 忠誠度

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [建立、編輯和管理忠誠度挑戰](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-challenge-management){target="_blank"} | 簡化並加速熟客方案管理 | `loyalty` | Adobe Journey Optimizer (AJO) | 「建立挑戰，鼓勵會員嘗試新的季節性飲品」 <br> 「以最高的會員流失率向我展示忠誠度挑戰。」 |
| [分析熟客方案績效](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-data-insight){target="_blank"} | 使用自然語言查詢和分析熟客點數、成員層級、贖回和收入量度 | `loyalty-insights` | Adobe Journey Optimizer (AJO) | 「2026年8月期間已授與多少忠誠點數？」 <br> 「顯示2026年8月期間依日劃分的熟客方案總收入。」 |

**相關資訊**

* [使用AI](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}提供Adobe Journey Optimizer中同事和可用技能的概觀。

## 在Journey Optimizer中建立內容

使用「同事聊天」來規劃、產生、評估和調整行銷活動訊息文案和電子郵件HTML，然後直接將核准的內容儲存或傳遞給Journey Optimizer。

### 訊息復本

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [擷取行銷簡報](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 擷取行銷活動策略並植入創意簡報。 | `capture-marketing-brief` | Adobe Journey Optimizer (AJO) | 「為季節性產品上市建立行銷簡報」 <br> 「將此行銷活動策略化為行銷簡報」 |
| [擷取創意簡報](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 建構複製執行規格並建立內容計畫矩陣。 | `capture-creative-brief` | Adobe Journey Optimizer (AJO) | 「從這個核准的行銷簡報建立創意簡報」<br>「為我們的電子郵件和簡訊行銷活動建立內容計畫矩陣」 |
| [計畫內容策略](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 在產生副本之前腦力激盪訊息地圖、敘述弧和頻道角色。 | `plan-content-strategy` | Adobe Journey Optimizer (AJO) | 「透過電子郵件和推播為我們的產品上市計畫訊息策略」<br>「為我們的歡迎行銷活動提供敘述弧線建議」 |
| [產生復本](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 為電子郵件、簡訊、推播、WhatsApp、社交和橫幅產生全新的品牌內副本。 | `generate-copy` | Adobe Journey Optimizer (AJO) | 「撰寫品牌內電子郵件，宣告我們新的季節性系列」 <br> 「為擁有放棄購物車之客戶草擬簡訊提醒」 |
| [產生影像](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 使用Firefly產生、裁切、覆蓋、變更和簽署行銷活動影像。 | `generate-image` | Adobe Journey Optimizer (AJO) | 「為我們的季節性行銷活動電子郵件產生主圖影像」 <br>「從此核准的行銷活動影像建立橫幅變化」 |
| [評估復本](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 根據品牌和通路標準評估現有的復本並為其評分。 | `evaluate-copy` | Adobe Journey Optimizer (AJO) | 「根據我們的品牌指南評估此電子郵件復本」 <br> 「檢查此推播訊息是否符合我們的頻道標準」 |
| [編輯復本](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 對現有副本進行就地編輯 — 評估修正、重新定語、翻譯和導向修訂。 | `edit-copy` | Adobe Journey Optimizer (AJO) | 「修訂此電子郵件副本，以處理評估回饋」<br>「將此核准的SMS副本翻譯為法文」 |
| [展開行銷活動內容](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 跨管道、地區設定、對象和變體，將核准的內容計畫矩陣粉絲化為每個單位的副本。 | `expand-campaign` | Adobe Journey Optimizer (AJO) | 「為此核准的內容計畫中每個管道產生復本」 <br>「將此行銷活動展開為每個對象的英文和法文變體」 |
| [分析視覺化HTML](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 轉譯複製HTML至熒幕擷圖以供視覺化檢查。 | `analyze-visual-html` | Adobe Journey Optimizer (AJO) | 「在HTML轉譯此電子郵件，以便我檢查版面」 <br> 「顯示此行銷活動HTML的熒幕擷圖」 |
| [儲存內容](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 將核准的內容儲存回Adobe Journey Optimizer、Adobe Campaign v8或Marketo。 | `save-content` | Adobe Journey Optimizer (AJO) | 「將此核准的電子郵件內容儲存至Journey Optimizer」<br>「將核准的簡訊副本儲存至Journey Optimizer」 |

### 電子郵件設計

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [撰寫電子郵件](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 計畫會從行銷目標和品牌輸入封鎖結構和樣式。 | `compose-email` | Adobe Journey Optimizer (AJO) | 「使用我們的品牌指南規劃產品發佈的電子郵件版面配置」 <br> 「使用主圖區段、產品重點和call to action撰寫歡迎電子郵件」 |
| [建置電子郵件](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 從版面配置計畫、熒幕擷圖或Figma設計連結建立、調整、編輯及改良電子郵件HTML。 | `build-email` | Adobe Journey Optimizer (AJO) | 「從這個核准的版面配置計畫建置電子郵件HTML」<br>「從這個Figma設計連結建立電子郵件」 |
| [維護設計系統](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 維護品牌可重複使用的電子郵件設計系統 — 代號、版面模式及品牌語言。 | `maintain-design-system` | Adobe Journey Optimizer (AJO) | 「使用這些核准的品牌色彩更新我們的電子郵件設計系統」<br>「將此可重複使用的產品配置新增到我們的電子郵件設計系統」 |
| [檢閱合規性](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 根據品牌和通路指導方針及傳遞能力標準，稽核已組裝的電子郵件。 | `review-compliance` | Adobe Journey Optimizer (AJO) | 「對照我們的品牌和頻道指南檢閱此電子郵件」<br>「在移交前稽核此電子郵件是否有傳遞問題」 |
| [檢閱設計](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 針對階層、間距、敘述流程和品牌契合度提供主觀設計意見回饋。 | `review-design` | Adobe Journey Optimizer (AJO) | 「檢閱此電子郵件的視覺化階層與間距」 <br> 「評估此電子郵件設計是否符合我們的品牌」 |
| [檢閱協助工具](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 執行WCAG 2.1 AA協助工具稽核。 | `review-accessibility` | Adobe Journey Optimizer (AJO) | 「稽核此電子郵件以找出WCAG 2.1 AA協助工具問題」<br>「檢查此電子郵件的色彩對比和影像替代文字」 |
| [交出電子郵件](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 將核准的HTML匯出並傳遞至Adobe Journey Optimizer或Adobe Campaign。 | `handoff-email` | Adobe Journey Optimizer (AJO) | 「將此核准的電子郵件匯出至HTML至Journey Optimizer」<br>「將核准的電子郵件傳送至Journey Optimizer」 |

**相關資訊**

* [內容管理的同事](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"}提供Adobe Journey Optimizer內容管理工具和可用技能的詳細資訊。

## 最佳化

使用「同事聊天」來瀏覽、分析和規劃實驗，以及建立、執行和疑難排解Adobe Target活動、對象和建議。

### 實驗分析和策略

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 瀏覽和探索實驗 | 查詢實驗概述、清單、計數、原始結果、見解和機會 | `experiment-explorer` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | 「顯示我的實驗」 · 「列出作用中測試」 · 「正在執行多少個實驗？」 |
| 分析實驗效能 | 使用量度取得產品組合細目、單一實驗健康狀態檢查、執行摘要和跨實驗報告，可選擇使用CJA資料豐富這些內容 | `experiment-analysis` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | 「我的A/B測試表現如何？」 · 「使用CJA量度產生活動報表」 · 「此測試是否正常？」 |
| 計畫和設計實驗 | 取得要執行的影響最高的下一個測試、命名主題的設計、目標對量度轉換、失敗測試的復原指引，或循序多實驗藍圖 | `experiment-strategist` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | 「接下來應該測試哪些專案？」 · 「協助我設計實驗以改進結帳轉換」 · 「為第三季建立測試藍圖」 |
| 搜尋實驗歷史記錄 | 從過去的實驗中擷取假設、學習、結果和處理、依主題尋找先前的實驗，或擷取外部CSV以豐富結果 | `experiment-knowledge-base` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | 「實驗X有什麼改變？」 · 「我們以前測試過這個假設嗎？」 · 「擷取此CSV」 |

### Target活動和對象

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 瀏覽目標實體 | 探索、檢查及計算活動、選件、對象、mbox、屬性、工作區、AT.js設定、回應Token和修訂歷史記錄。 也可以擷取活動強制體驗的熒幕擷圖 | `target-browse` | Adobe Target | 「列出我的A/B測試」 · 「本月啟動多少活動？」 · 「顯示活動12345的詳細資訊」 |
| 分析活動績效 | 取得單一活動的轉換率、提升度、信賴區間、收入和曝光計數。 僅陳述事實，且永遠不會宣告獲勝者 | `target-analyze` | Adobe Target | 「活動X表現如何？」 · 「顯示轉換提升度」 · 「什麼是結帳測試的AOV？」 |
| 送貨或停止判決 | 取得活動的SHIP、WAIT、STOP或FIX建議，計算方式為原始計數的兩倍重要性加上設定缺陷檢查 | `target-activity-verdict` | Adobe Target | 「我是否應該送出這項測試？」 · 「哪個變體贏？」 · 「這重要嗎？」 |
| 建立及設定活動 | 建立、更新及設定活動、選件和回應Token，產生QA預覽URL，以及製作或最佳化選件內容 | `target-design` | Adobe Target | &quot;建立首頁的A/B測試&quot; · &quot;更新流量分割&quot; · &quot;最佳化此選件的JS&quot; |
| 建立視覺化體驗撰寫器活動 | 建立和編輯視覺化體驗撰寫器(VEC)活動，針對即時頁面URL以及涵蓋變體的頁面傳送對象，以DOM修改形式創作變體 | `target-vec` | Adobe Target | &quot;建立首頁的VEC A/B測試&quot; · &quot;變更視覺化編輯器中的主圖示題&quot; |
| 從頭開始設定完整測試 | 取得適用於A/B、XT和VEC測試的引導式端對端活動建立，涵蓋需求收集、先決條件、建立、排程和優先順序、QA連結，以及選用的啟用 | `target-setup` | Adobe Target | 「逐步引導我設定完整的A/B測試」 · 「我是Target的新手，請協助我建立第一個測試」 |
| 稽核方案健康狀況 | 取得整個方案的健康稽核，涵蓋風險和碰撞偵測、設定錯誤發現、對象和選件衛生，以及快速贏取建議 | `target-intelligence` | Adobe Target | 「稽核我的Target活動」 · 「尋找有風險或設定錯誤的測試」 · 「應清理哪些專案？」 |
| 尋找成功模式 | 請探究Target成功模式、有效策略及高績效對象或內容的相關歷史記錄，然後以您自己的資料為基礎，獲得後續測試內容的建議 | `target-strategist` | Adobe Target | 「什麼適合我們？」 · 「顯示我的成功模式」 · 「接下來應該根據過去的結果進行哪些測試？」 |
| 計算樣本大小和持續時間 | 規劃A/B/n範例大小、測試持續時間，以及轉換率和每位訪客收入量度的可偵測提升度（含Bonferroni校正） | `target-test-calculator` | Adobe Target | 「我的A/B測試該執行多久？」 · 「我需要多少樣本量？」 · 「我的測試是否已提供支援？」 |
| 取得方案層級的效能彙總 | 取得概觀面板、最近推出的表格，以及所有活動的彙總贏/虧/提升度人口普查，加上單一活動趨勢和動量顯示 | `target-portfolio-report` | Adobe Target | 「給我一次Target計畫的健康情況檢查」 · 「哪些是我的最好和最差的測試？」 · 「活動X是否趨向於獲勝？」 |
| 從自然語言建立對象 | 從自然語言說明、明確規則條件，或內嵌或上傳的值清單中建立或編輯Target原生對象。 將請求對應至規則文法，並在寫入之前驗證規則樹狀結構 | `target-audience-composer` | Adobe Target | 「建立來自加州回訪訪客的受眾」 · 「從這些郵遞區號建立受眾」 · 「縮小受眾X至回訪訪客」 |

### 推薦

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 瀏覽Recommendations實體 | 瀏覽並檢查Recommendations條件、集合、設計、促銷活動、排除專案、目錄和摘要，以及取得清理建議和目錄屬性指引 | `target-recs` | Adobe Target | 「列出我的Recommendations條件」 · 「我有哪些設計？」 · 「我們可以清理哪些記錄？」 |
| 診斷Recommendations問題 | 追蹤活動、條件、摘要、集合和設計鏈結，以說明Recommendations為何空白、過時或無法顯示 | `target-recs-diagnose` | Adobe Target | 「我的建議為何空白？」 · 「為什麼我的Recs活動在48小時內一直是『結果未就緒』？」 |
| 作者建議 | 建立和更新Recommendations條件、集合、設計、排除、促銷活動、摘要和推薦活動，包括一次橫跨多個活動的閘道大量作業 | `target-recs-design` | Adobe Target | 「建立『檢視次數最多』的條件」·「建立50美元以下庫存產品的集合」·「對所有銷售活動套用黑色星期五日期」 |

## 基本元素

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 產品知識與檔案 | 從官方Adobe檔案中回答操作說明、概念、疑難排解和最佳作法問題 | `product-knowledge` | 所有符合資格的應用程式 | 「如何設定串流目的地？」 <br> 「批次和串流細分之間有何差異？」 |
| 查詢Experience Platform / Journey Optimizer實體 | 作為平台實體相關問題的主要入口點；視需要路由至KG、欄位探索或API | `operational-insights` | 所有符合資格的應用程式 | 「我有多少資料集？」 <br> 「顯示所有使用中的歷程」<br>「列出我的目的地」 |
| 知識圖查詢 | 透過單一SQL查詢的彙總計數、跨實體聯結、關係查閱和中繼資料探索 | `knowledge-graph` | 所有符合資格的應用程式 | 「哪些對象使用此資料集？」 <br> 「顯示結構描述和資料集之間的關係」 |
| Experience Platform / Journey Optimizer / Customer Journey Analytics API作業 | 提供直接API閘道，用於變更、即時狀態檢查以及不在知識圖形中的實體型別 | `cxo-api` | 所有符合資格的應用程式 | &quot;刪除資料集X&quot; <br> &quot;檢查我的批次擷取工作的狀態&quot; |
| 實體解析度和連結 | 使用語意和辭彙搜尋來解析對實際Experience Platform實體的實體提及，並探索XDM欄位 | `entity-linking` | Adobe Experience Platform | 「將『節日購物者』解析為實際受眾」<br>「尋找與購買記錄相關的我欄位」 |
| 管理自訂技能 | 儲存、修改或刪除使用者擁有的可重複使用技能，這些技能會跨工作階段存留 | `manage-skill` | 所有符合資格的應用程式 | 「將工作流程另存為技能」 <br>「刪除我的每週報告技能」 <br>「將此變成可重複使用的技能」 |
| 監控串流容量和違規情形 | 檢查沙箱間目前和歷史串流使用情況、容量和違規狀態 | `observability-streaming-capacity`, `observability-streaming-usage`, `observability-capacity-breaches` | Adobe Experience Platform | 「我目前的沙箱中目前的串流容量是多少？」 <br> 「我目前的沙箱在上星期是否超過容量限制？」 |
| [檢視健康情況檢查評估結果](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/run-and-operate/health-checks/overview) | 檢視沙箱的最新健康情況檢查評估、深入研究失敗檢查，並檢視受影響的實體 | `rao-view-latest-health-checks-assessment` | Adobe Experience Platform | 「我的沙箱有什麼問題？」 <br> 「告訴我關於我最新的健康情況檢查評估」 <br> 「自訂名稱空間描述檢查有哪些問題？」 |
| 修正健康情況檢查問題 | 在進行任何變更之前，只要您核准，即可直接從聊天中修正標幟的身分名稱空間、合併原則和結構描述問題 | `rao-remediate-identity-namespace-description`, `rao-remediate-merge-policy-duplicate-name`, `rao-remediate-missing-audit-field-group`, `rao-remediate-default-merge-policy-naming` | Adobe Experience Platform | 「修正身分名稱空間說明」 <br> 「修正重複的合併原則名稱」 <br> 「修正缺少稽核欄位群組的結構描述」 <br> 「修正預設的合併原則命名」 |

## 資料管理

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [尋找值得最佳化或清理的資料](./data-management/manage-data-lake-retention.md#find-data-worth-optimizing) | 瞭解您是否可透過將最大、最少使用或忘記的資料集顯示為候選資料集來進行清理或資料湖保留原則，以最佳化您的Experience Event資料 | `List datasets` | Adobe Experience Platform | 「我感覺我的資料可以最佳化」 <br> 「協助我瞭解我的資料的價值」 <br> 「最佳化我的沙箱資料」 <br> 「清理我的沙箱資料集」 |
| [調查資料集的使用情況並管理其保留](./data-management/manage-data-lake-retention.md#check-how-actively-a-dataset-is-used) | 一旦您找到值得進一步檢視的資料集，即可瞭解資料集的使用積極性、模型化潛在資料湖保留原則的影響，並在您準備就緒時設定、變更或移除該原則，並在任何變更前完成稽核和核准 | `Analyze dataset usage`, `Analyze dataset retention`, `Manage dataset retention` | Adobe Experience Platform | 「使用我的Web事件資料集的積極性如何？」 <br> 「如果對此資料集設定60天的保留期，會有什麼影響？」 |

## 沙箱工具

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| [跨沙箱移動物件](/help/chat/use-cases/sandbox-tooling/sandbox-tooling.md) | 透過自動解析的相依性，順暢地跨沙箱移轉結構描述、受眾和其他物件設定 | `sandbox-tooling-workflow` | Adobe Experience Platform | 「將結構描述Luma忠誠會員白金從目前的沙箱移動到生產沙箱」<br>「將美國金級忠誠會員對象提升到中繼」 |

## 客戶警報

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 管理警報訂閱 | 透過自然語言對話檢視及管理警示訂閱。 | `alerts-subscribe` | Adobe Experience Platform | 「我訂閱了哪些警示？」<br><br>「訂閱此警示給我。」<br><br>「移除此警示的訂閱。」 |
| 檢閱警示活動 | 檢閱指定期間內的目前警示狀態和歷史警示活動。 | `alerts-list` | Adobe Experience Platform | 「過去24小時內發生了什麼事？」<br><br>「過去24小時內觸發了哪些警示？」<br><br>「顯示過去七天的作用中警示。」 |
| 識別週期性警報模式 | 分析警示歷史記錄，以識別經常觸發的警示型別和運作趨勢。 | `alerts-list` | Adobe Experience Platform | 「顯示前3個觸發的警示型別。」<br><br>「哪些警示型別本月發生頻率最高？」<br><br>「您在過去七天看到哪些警示模式？」 |
| 著重於高優先順序的問題 | 依嚴重程度篩選警示活動，以排定調查工作的優先順序。 | `alerts-list` | Adobe Experience Platform | 「僅顯示高嚴重度警示。」<br><br>「本週觸發了哪些嚴重性警示？」<br><br>「顯示過去30天的嚴重性警示。」 |
| 瞭解警報的影響半徑 | 識別受警示影響最大的物件，並決定應從何處開始調查。 | `alerts-list` | Adobe Experience Platform | 「前5個受影響的物件為何？」<br><br>「哪些物件與最高嚴重性警示相關？」 |
| 將警示型別連線到受影響的物件 | 分析警示型別與受影響資源之間的關係。 | `alerts-list` | Adobe Experience Platform | 「哪些警報型別最常影響此資料集？」<br><br>「顯示警報型別與受影響物件之間的關係。」<br><br>「哪些警報型別最常影響最受影響的物件？」 |
| 將焦點放在我的警報上 | 分析您訂閱並負責監督的警示。 | `alerts-list` | Adobe Experience Platform | 「顯示我訂閱的高嚴重度警示。」<br><br>「本週觸發了哪些來自我的警示的警示？」<br><br>「我的任何訂閱警示需要注意嗎？」 |

## 工作流程與規劃

| 使用案例 | 說明 | 技能 | 應用程式 | 範例提示 |
| --- | --- | --- | --- | --- |
| 管理Planning工作區 | 建立和改進Workfront Planning工作區、區段、記錄型別和欄位，以組織方案和追蹤工作 | `manage-workfront-planning`, `wf-planning-solution-architect` | Workfront規劃 | 「建立名為MKG Hub的工作區，並設定記錄型別以依地區追蹤程式」<br>「設定跨頻道和區域追蹤MKG程式所需的記錄型別和關係」 |
| 管理Planning記錄 | 在工作區中建立和更新計畫記錄（行銷活動、簡報）及其欄位值 | `manage-workfront-planning` | Workfront規劃 | 「建立秋季品牌上市行銷活動的簡報，包含目標、目標對象和重要訊息」 <br> 「使用預算和主要管道更新秋季品牌上市簡報」 |
| 建立和管理專案 | 啟動並建構專案：套用範本、設定優先順序和預算、排序作業、新增階段和相依性，以及指派人員或角色 | `manage-workfront-workflow` | Workfront工作流程 | 「建立春季行銷活動、以$200K預算將其設定為高優先順序，並排序任務」 <br> 「從[專案範本]建立名為[專案名稱]的Workfront專案計畫<br> 「為秋季啟動建立專案計畫：社交行銷活動，其中包含概念、設計、複製和稽核任務」 <br> 「新增電子郵件行銷任務並將其指派給Rachel Smith」 |
| 加速審查與核准 | 設定多階段核准、套用核准範本、新增/移除核准者、傳送提醒並進行大量更新 | `manage-workfront-workflow` | Workfront工作流程 | 「建立多階段核准（複製、設計、法律），並提醒所有尚未核准的人」<br>「從所有開啟的核准中移除Chris Smith，並以Jane Francis取代」 |
| 更新任務和工作狀態 | 標籤任務完成、更新完成百分比，並關閉您的工作 | `manage-workfront-workflow` | Workfront工作流程 | 「在秋季啟動時將我的『製作關鍵圖稿』任務標示為完成」 <br> 「100%關閉我的秋季啟動複製任務」 |
| 表面工作見解 | 提出探索性問題以尋找跨專案的風險工作、未指派任務、未完成問題和狀態 | `query-workfront` | Workfront工作流程 | 「在目前專案中尋找未指派給任何人員且本週到期的未完成任務」<br>「目前專案中有多少個未完成的問題？」 |
| 專案與任務摘要 | 提取專案、任務、問題和指派的清單、表格和計數 | `query-workfront` | Workfront工作流程 | 「以專案名稱、任務到期日和指派的使用者顯示已準備開始的任務的表格」 <br> 「取得指派給[使用者名稱]的所有任務」 |
| 追蹤核准和投資組合狀態 | 檢查您的核准狀態，並按投資組合彙總未完成的工作 | `query-workfront` | Workfront工作流程 | 「顯示我的核准狀態」 <br>「顯示包含不完整問題的表格，這些問題屬於[Portfolio名稱]投資組合的一部分」 |
