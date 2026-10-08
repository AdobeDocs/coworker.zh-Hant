---
title: 與同事一同規劃您的Customer Journey Analytics或串流媒體實作
description: 瞭解同事的實作指南技能如何透過可匯出的核對清單，將探索對話轉換為個人化、有序的實作計畫。
hold: true
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 1%
---

# 與同事一起規劃您的實作

Adobe CX Enterprise Coworker包含五個實作指南技能，每個產品介面各一個：Customer Journey Analytics、Adobe Analytics升級至Customer Journey Analytics、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)和串流媒體。 每項技能都會將簡短探索對話轉換為個人化、相依性感知的實作計畫，並透過互動式檢查清單和隨時可使用的匯出功能，全部透過單一同事聊天對話完成。

如果您正站起來或移轉至這些產品的任一項，您便可以使用這些技能來取得循序漸進的計畫，無需手動研究Adobe的實作需求，或從頭開始建立專案計畫。

>[!NOTE]
>
>考慮以下事項：
>
>* 這些實作指南技能是較大選擇性工作流程的一部分：自訂實作或升級步驟（這些指南）、實作（請參閱[與同事專案產生實作檢查清單](./intelligent-checklist.md)）和驗證（例如，[驗證您的Adobe Analytics升級至Customer Journey Analytics](./data-validation-aa-cja.md)或[驗證您的串流媒體實作](./streaming-media-validation.md)）。 您不需要使用全部三個階段。 例如，您無需產生計畫或檢查清單即可驗證資料。
>* 這些技能不會存取您的Adobe系統或進行任何變更。 它們可協助您規劃實作。 他們不會針對即時租使用者執行或驗證。

使用這些技能：

* 取得個人化、有序的計畫，以從頭開始站起Customer Journey Analytics，包括每個步驟的擁有者、投入估計和相依性。

* 取得從Adobe Analytics升級至Customer Journey Analytics的移轉計畫，包括Adobe Analytics功能對等對應、歷史回填順序和驗證入口，以便您解除Adobe Analytics的委任。

* 取得實作Content Analytics (ACA)的引導式計畫，包括授權、隱私權和PII範圍設定，以及引導式設定精靈。

* 無論您使用Marketing Campaign Analytics來源聯結器、自己的資料集或混合方法，取得適合您擷取路徑的Adobe (MCA)上線計畫。

* 取得Edge上串流媒體收集的實作計畫，包括資料流設定、每個平台的SDK/API實作，以及媒體事件模型。

## 開始之前

<!-- FLAG: Best guess, not confirmed by source docs. Requirements doc doesn't state explicit prerequisites for starting a discovery conversation — verify with skills-overview.md or SME before publishing. -->

### 所需資訊

若要開始實作指南對話，您需要：

* 您適用這五個實作路徑中的哪一個： Customer Journey Analytics （新增）、Adobe Analytics至Customer Journey Analytics升級、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)或串流媒體。

* 有關您目前環境的基本細節，例如您是否擁有現有的Adobe Analytics實作、您的授權狀態或您規劃的資料擷取路徑。 探索對話會要求您提供這些詳細資訊，但請您準備好這些資訊，可加快處理過程。

### 限制

在使用這些技能之前，請牢記以下限制：

* **僅限Planning**：這些技能不會存取您的Adobe系統或進行任何變更。 他們不會針對即時租使用者執行實作或驗證它。
* **每個技能一個產品介面**：每個技能都涵蓋單一實作路徑。 如果您的要求適用於不同的產品表面，則技能會將您導向正確的表面，而非直接回答。
* **本身不是專案追蹤體驗**：這些技能會產生計畫和匯出，但不會單獨追蹤進行中的狀態、共同作業或核准。 若要追蹤計畫在一段時間內的變化，請使用預先定義的行動手冊將其轉換為同事專案。 請參閱[與同事專案產生實作檢查清單](./intelligent-checklist.md)。

## 開始實作規劃工作階段

1. 登入同事。

1. 選取&#x200B;[!UICONTROL **新增聊天**]。

1. 在文字欄位中，說明您要計畫的實施或移轉。 例如：

   **提示**

   > 協助我規劃Customer Journey Analytics的實作。

   您的請求會路由至對應的實作指南技能，這會開始互動式探索對話。

1. （視條件而定）如果技能無法判斷哪個實施路徑適用於您，請回答它詢問的澄清問題，然後繼續。

## 選擇您的實作路徑

每個實施指南技能涵蓋一個產品表面。

### Customer Journey Analytics

取得個人化、有序的實作計畫，讓您從頭開始站立Customer Journey Analytics，而不需移轉現有的Adobe Analytics部署。 您的計畫包括每個步驟的擁有者、工作量估計和相依性。

提示範例：

* 協助我規劃Customer Journey Analytics的實作。
* 我從頭開始站起Customer Journey Analytics。 為我建置實施計畫。

### Adobe Analytics升級至Customer Journey Analytics

取得將Adobe Analytics功能同位對映至Customer Journey Analytics的移轉計畫，對歷史回填進行排序，並包含驗證和平行執行閘道，然後再將Adobe Analytics解除委任。

提示範例：

* 協助我規劃從Adobe Analytics升級至Customer Journey Analytics的程式。
* 建立從Adobe Analytics到Customer Journey Analytics的移轉計畫。

### Content Analytics (ACA)

取得實作Content Analytics (ACA)的引導式計畫，包括授權、隱私權和PII範圍設定，以及引導式設定精靈。 由於ACA沒有DULE、CMK或HIPAA涵蓋範圍，因此您的計畫包含隱私權閘道步驟。

提示範例：

* 協助我規劃Content Analytics的實作。
* 為我建立ACA實作計畫。

### Marketing Campaign Analytics (MCA)

取得Marketing Campaign Analytics (MCA) Essentials的入門計畫，以根據您的擷取路徑進行調整，無論您使用Adobe來源聯結器、您自己的資料集或混合方法，因此funnel對應和資料對齊步驟會符合您的環境。

提示範例：

* 協助我規劃Marketing Campaign Analytics的實作。
* 使用我自己的資料集，為我建立MCA上線計畫。

### 串流媒體

取得在Edge上串流媒體收集的實作計畫，其中涵蓋資料流設定、每個平台的SDK/API實作，以及媒體事件模型，因此您可以正確檢測Customer Journey Analytics和/或Adobe Analytics報表的工作階段、Ping和完成。

提示範例：

* 協助我規劃我的串流媒體實作。
* 建立在Edge上檢測串流媒體的計畫。

## 檢閱結果

同事會在同一次交談中，以互動式檢查清單和摘要的形式傳回您的實作計畫。

**互動式檢查清單**

HTML檢查清單，將您的實作步驟分組為階段和里程碑。 檢查清單包含每個步驟的：

* 工作量估計
* 主要擁有者和任何支援擁有者
* 其他步驟的硬相依性
* 是否可跳過該步驟
* 相關Experience League或developer.adobe.com檔案的連結

**匯出**

以適合您工作流程的格式下載計畫：

| 匯出 | 包含的內容 |
| --- | --- |
| CSV | 簡單的步驟清單 |
| Jira匯入CSV | 使用劇本點、優先順序和標籤格式化的步驟，以便匯入至Jira |
| WORKFRONT CSV | 以持續期間和前置任務格式化的步驟，以便匯入Workfront |
| Markdown | 您可以貼到檔案或Wiki中的檢查清單 |

**聊天摘要**

除了檢查清單，「同事」在交談中直接提供三部分摘要：

1. 計畫總覽
1. 完整的步驟表
1. 每次匯出的下載連結

## 如何建置計畫

每個實施指南技能都遵循相同的四個階段程式：

* **探索**：階段式交談會詢問五到九組問題（針對您的實作路徑），以瞭解您的環境和目標。
* **計算**： LLM會決定哪些條件步驟和相依性覆寫適用於您的答案。 它不會自行撰寫計畫。
* **組合併轉譯**：確定性程式會解析步驟之間的相依性、排序這些步驟、計算關鍵路徑（相依步驟的最長鏈結），並產生檢查清單和匯出。
* **傳遞**：同事提供您計畫的下載連結和聊天摘要。

這種引導式探索與確定性組裝的結合，代表您的計畫會根據您的回答一致地產生，而不是由手繪書寫。
