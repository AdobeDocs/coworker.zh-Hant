---
title: 與同事驗證您的串流媒體實作
description: 瞭解同事的串流媒體驗證技能如何檢查您的設定、工作階段和記錄，以確認您的實施是否正確追蹤。
hold: true
source-git-commit: 94cf399a48d13ee83c702804b50fdccd4baa9d71
workflow-type: tm+mt
source-wordcount: '1301'
ht-degree: 0%
---

# 與同事驗證您的串流媒體實施

Co-worker包含串流媒體驗證技能，可檢查您在Edge Network上的Adobe串流媒體（視訊和音訊Analytics）實施，以提供Customer Journey Analytics和/或Adobe Analytics。 您不會手動交叉參考Assurance、資料集設定、XDM結構欄位群組、Customer Journey Analytics資料檢視設定和原始網路記錄，而是會取得單一驗證報告。

如果您要實作或疑難排解串流媒體追蹤，可以使用此技能確認您的實作已正確設定、如預期收集資料並擷取您打算追蹤的內容，所有這些都在單一同事聊天對話中。

>[!NOTE]
>
>考慮以下事項：
>
>* 此技能是較大選擇性工作流程的一部分：自訂實作或升級步驟（請參閱[與同事一起規劃實作](./implementation-guide.md)）、實作（請參閱[與同事專案產生實作檢查清單](./intelligent-checklist.md)）以及驗證（此技能）。 您不需要使用全部三個階段。 例如，您可以驗證串流媒體實施，永遠不需要產生計畫或檢查清單。
>* 此技能會驗證和診斷問題。 它不會修正您的設定或資料。 利用其發現來指導您自己的修復。

使用此技能可以：

* 跨資料串流、XDM結構、資料集和Customer Journey Analytics資料檢視執行設定稽核，並將第一個中斷的查核點標示為可能的原因。

  此功能目前處於「有限可用性」。

* 驗證特定的視訊工作階段ID，並檢視確切的哪個躍點、資料集擷取或Customer Journey Analytics對應，以及在發生差異。

* 驗證來自已上傳Charles或HAR記錄或較簡單URL清單的工作階段，而不需要即時Assurance工作階段。

  此功能目前處於「有限可用性」。

* 透過單一提示取得整體健康狀態檢查，不需要工作階段ID或記錄，並彙總您的設定和最近工作階段的範例。

## 開始之前

<!-- FLAG: General access prerequisite is inferred, not stated explicitly in source docs. Per-mode inputs (session ID, log file) are directly sourced from Functional Requirements. -->

### 所需資訊

若要驗證串流媒體實作，您需要：

* 存取與您組織的Adobe Experience Platform和Customer Journey Analytics資料連線的同事。

* 針對工作階段ID驗證，您要檢查的視訊工作階段ID。

* 對於以記錄為基礎的驗證，可使用Charles或HAR記錄檔案，或使用.txt、.md或.json格式的較簡單URL清單。

組態稽核或整體健康狀態檢查不需要特定輸入。 Co-worker會自動讀取您現有的設定，並取樣最近的工作階段。

### 限制

使用此技能之前，請牢記以下事項：

* **僅診斷**：此技能無法修正您的設定或資料。 它會識別問題；您會進行變更。
* **僅限串流媒體**：此技能涵蓋Edge Network上的串流媒體實作。 其他同事驗證技能會涵蓋非媒體資料集和標準網頁或應用程式分析實作。
* **僅隨選**：此技能不提供即時或持續監視。 當您想要檢查時，請執行它，而不是作為持續的警報。
* **沒有內建爬蟲**：此技能不會抓取您的網站或應用程式。 如果您想要驗證以抓取的涵蓋範圍，請提供爬蟲或Headless瀏覽器輸出作為證據。
* **僅限Edge Network實作**：不支援舊版Media SDK和僅限Analytics實作路徑。
* **尚未包含更廣的功能**：即時事件和心率資料流驗證、客戶行動手冊或案例驗證、多平台歷史儀表板統計，以及下游Real-Time CDP或Adobe Journey Optimizer啟用驗證，預計於稍後版本推出。

## 開始驗證工作階段

1. 登入同事。

1. 選取&#x200B;[!UICONTROL **新增聊天**]。

1. 在文字欄位中，說明您要驗證的內容。 例如：

   **提示**

   > 驗證視訊工作階段ID#123定。

   您的請求會路由至串流媒體驗證技能，此技能會執行相符的驗證模式。

1. （視條件而定）如果技能需要更多資訊，例如工作階段ID或記錄檔，請在詢問時提供。

## 選擇您的驗證模式

串流媒體驗證技能包括四種模式。

### 設定稽核

此功能目前處於「有限可用性」。

驗證從資料流到Customer Journey Analytics資料檢視的整個Adobe Experience Platform流程，包括您的XDM結構、資料集和任何「資料準備」規則或Customer Journey Analytics衍生的欄位。 同事會報告每個躍點通過/失敗計分卡，並將第一個中斷的查核點標示為可能的原因。

提示範例：

* 驗證資料檢視、資料集和資料流的串流媒體設定。
* 檢查我的串流媒體端對端設定。
* 我的Media Analytics資料流已針對Customer Journey Analytics正確設定嗎？

### Session-ID驗證

針對特定視訊工作階段，以Customer Journey Analytics資料檢視交叉檢查Adobe Experience Platform資料集列，並查明差距是資料集擷取問題還是Customer Journey Analytics對應問題。

提示範例：

* 驗證視訊工作階段ID#123定。
* 為什麼工作階段abc-123沒有顯示在Customer Journey Analytics中？
* 比較資料集和Customer Journey Analytics資料檢視之間的工作階段xyz 。

### 記錄檔驗證

此功能目前處於「有限可用性」。

從您上傳的Charles或HAR記錄或較簡單的URL清單驗證工作階段，而不需要即時Assurance工作階段。 Co-worker會驗證端點模式、回應代碼、事件順序和Ping步調，以及檢查在完全可信度、降低可信度下執行或略過的狀態。

提示範例：

* 驗證附加的串流媒體資料記錄。
* 檢查此Charles記錄檔以取得工作階段ID #456。
* 根據預期的媒體Ping驗證此URL清單。

### 驗證儀表板

透過單一提示取得整體健康狀態檢查。 Co-worker會將設定稽核與輕量型的取樣工作階段檢查彙總到一個狀態，並明確指出如果未提供記錄，則不會執行以記錄為基礎的檢查。

提示範例：

* 檢查串流媒體資料。
* 給我一份有關我的串流媒體實作的報告。
* 我的串流媒體實作整體情況如何？

## 檢閱結果

每個模式都會傳回符合您驗證格式的結果。

**組態稽核結果**

每個躍點的通過/失敗計分卡涵蓋資料串流、XDM結構、資料集、Customer Journey Analytics資料檢視，以及「資料準備」或衍生的欄位規則。 Co-worker會將第一個失敗的躍點識別為可能的根本原因。

**工作階段ID驗證結果**

僅限Customer Journey Analytics的報告摘要，包括工作階段ID、內容中繼資料、依事件型別的列計數、關鍵量度值和完整性備註。 如果出現間隙，Co-worker會識別這是否發生在資料集擷取或Customer Journey Analytics對應步驟中。

>[!NOTE]
>
>根據預設，工作階段ID和已驗證的身分值會從任何匯出或共用的摘要中排除。

**以記錄檔為基礎的驗證結果**

已上傳記錄的結構化和順序驗證，涵蓋端點模式、回應代碼、事件順序和Ping步調。 同事會根據您提供完整記錄擷取或較簡單的URL清單，判斷檢查是否以完整可信度執行、以較低可信度執行以及略過。

**個儀表板結果**

標示為「組態+可用資料」的單一整合狀態，結合您的組態稽核結果與最近工作階段的抽樣檢查。 取樣工作階段的同事名稱，並明確指出未執行以記錄為基礎的檢查，因為未提供記錄。

## 驗證如何運作

每個模式都會對應至專屬的引擎：

* **設定驗證引擎**：讀取您的資料串流、XDM結構描述、資料集和Customer Journey Analytics資料檢視設定，並根據一組固定的查核點進行評估。
* **工作階段交叉檢查引擎**：給定工作階段ID，查詢您的資料集和Customer Journey Analytics資料檢視，計算該工作階段的預期資料列計數和型別，並比較每個躍點的實際結果。
* **Log Parser and Validator**：剖析您上傳的記錄檔或URL清單、重新建構要求順序和時間，並套用結構化、順序化和網路層檢查。
* **儀表板彙總引擎**：執行設定驗證引擎和工作階段交叉檢查引擎的抽樣執行，並在您未提供工作階段ID、記錄檔或行動手冊時，將它們合併為單一狀態。
