---
title: 在同事專案中產生實作檢查清單
description: 瞭解Co-worker Projects如何從您的「實作指南」計畫產生預先填入的實作檢查清單，以及您可以指派和追蹤的步驟。
hold: true
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%
---

# 產生與同事專案的實作檢查清單

Adobe CX Enterprise Coworker可在同事專案中產生實作檢查清單專案，預先填入您的Customer Journey Analytics、Adobe Analytics升級至Customer Journey Analytics、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)或串流媒體實作指南計畫中的有序步驟。 在技術層面，同事可儘可能自動執行或協助執行多個步驟，讓您和您的團隊擁有單一且可追蹤的位置，方便您進行實作。

如果您正在領導實作、執行技術步驟，或只是需要瞭解進度，您可以使用此檢查清單指派工作、追蹤狀態並與團隊共同作業，而不需要離開同事。

>[!NOTE]
>
>考慮以下事項：
>
>* 此功能是較大選擇性工作流程的一部分：自訂實作或升級步驟（請參閱[與同事一起規劃實作](./implementation-guide.md)）、實作（此檢查清單）及驗證（例如，[驗證Adobe Analytics以升級至Customer Journey Analytics](./data-validation-aa-cja.md)或[驗證您的串流媒體實作](./streaming-media-validation.md)）。 您不需要使用全部三個階段，但產生此檢查清單確實需要完整的實作指南計畫。
>* Co-worker執行或協助的步驟會自動包含信賴度或驗證訊號。 在標籤完成之前先檢閱這些步驟 — Co-worker不會將自動化結果顯示為已驗證的事實。

使用此檢查清單來執行下列作業：

* 使用針對您的產品路徑預先填入的有序步驟集開始實作或移轉，而非手動彙編計畫。

* 不必直接詢問實作負責人，即可檢查實作中間的狀態，包括哪些專案遭到封鎖，以及後續專案。

* 規劃多平台或多區域實施，讓步驟平行或分階段執行，而非單一直線。

* 儘可能讓同事直接執行步驟，例如在Adobe Analytics和Customer Journey Analytics設定之間執行驗證檢查。

* 對於團隊前進之前需要簽核的步驟，引入核准門檻。


## 開始之前

<!-- FLAG: Open question — release note confirms a "predefined playbook" transforms the guide plan into a Coworker Project, but it's unconfirmed whether Coworker runs that playbook automatically or the user has to trigger/follow it manually. Written below as if Coworker does it automatically; verify before publishing. Exact UI mechanics also unconfirmed since Coworker Projects platform documentation doesn't exist yet. -->

### 所需資訊

若要產生「實施檢查清單」，您需要：

* 針對您的產品路徑完成實作指南對話。 請參閱[與同事一起規劃您的實作](./implementation-guide.md)。 Co-worker使用預先定義的行動手冊，自動將此計畫轉換為Co-worker專案 — 您不需要自行匯出任何內容。

* 存取組織中的同事專案。

### 限制

使用此功能前，請記住下列事項：

* **沒有指南內容**：此功能會使用實作指南技能中的計畫。 它不會編寫或維護該基礎內容。
* **尚未完全定義同步行為**：檢查清單旨在與您的實作指南計畫的更新保持同步，但確切的同步機制仍在定義中。 如果您的實施需要很長的時間，請手動檢查指南計畫更新。
* **需要同事專案**：此功能取決於貴組織中可用的同事專案平台。

## 產生檢查清單

<!-- FLAG: Best guess, not confirmed by source docs. Coworker Projects UI isn't documented in this repo yet — verify exact navigation and UI labels once available. -->

1. 登入同事。

1. 在導覽邊欄中選取&#x200B;[!UICONTROL **專案**]。

1. 選取「[!UICONTROL **新專案**]」，然後選取符合您實作指南計畫的預先定義行動手冊。

   同事會將您的計畫轉換為專案，預先填入您路徑的有序步驟。

## 檢閱結果

「同事」會產生您的「實作檢查清單」作為「同事專案」，供您和您的團隊使用。

**專案檢視**

您的專案會將您計畫中排序的實作步驟分組。 對於每個步驟，您可以：

* 指派擁有者
* 更新狀態，例如進行中或完成
* 將步驟標籤為不適用，或如果步驟不適用於您的實作，則略過該步驟
* 新增評論並與團隊共同作業
* 需要核准的步驟，在步驟被視為完成之前需要核准

**自動化和輔助步驟**

在技術可行的情況下，同事會直接執行或協助執行步驟，例如從Adobe Analytics或Customer Journey Analytics呈現設定或狀態資料。 這些步驟包括如上所述的信賴度或驗證訊號。

**匯出**

將您的檢查清單或其摘要層級進度匯出至Jira、Workfront或Excel，以便將其摺疊至您現有的專案管理工作流程中。

**多個檢查清單**

如果您同時管理多個實施，例如多個報表套裝、區域或品牌，您可以維護多個實施檢查清單專案，而不限於一個。
