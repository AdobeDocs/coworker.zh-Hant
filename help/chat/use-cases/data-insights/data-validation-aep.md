---
title: 與同事驗證您的Experience Platform資料
description: 瞭解如何使用CX Enterprise Coworker資料驗證技能，透過聊天來檢查Adobe Experience Platform資料集和欄位的品質。
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
last-substantial-update: 2026-08-27T00:00:00.000Z
jira: PLAT-302857
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%
---

# 與同事驗證您的Experience Platform資料

Adobe CX Enterprise Coworker包含資料驗證技能，可檢查Experience Platform資料集的資料品質。 利用它執行資料集的統計和語意驗證、分析資料集欄位，並識別資料品質問題，所有這些都透過一個同事聊天對話完成。

資料工程師、資料管理員和實作工程師會使用它來進行快速的品質檢查，而不使用SQL查詢或複雜的結構描述階層。

使用此技能可以：

* 在新實作或實作更新後驗證金鑰身分和事件欄位。
* 檢查欄位頂端值和無效值，以調查疑似的對應問題。
* 對關鍵資料集執行持續的資料管理檢查，以及早擷取回歸。

<!--TODO: skill display name "Data Validation skill" confirmed via the published KT-22622 video page (validate-dataset-quality-for-cja.md, merged 2026-09-16). Still need the technical skill ID from engineering (Petru Adrian Snep) for the use-cases overview table row. That page didn't add one either.-->

>[!NOTE]
>
>此技能為唯讀。 這不會變更您的資料、結構或對應。

## 開始之前

若要與同事驗證您的資料，您需要：

* 您要驗證之資料集的名稱或ID。
* （選擇性）如果不想讓技能自動選取欄位，要驗證的特定欄位名稱。

## 開始驗證工作階段

1. 登入同事。

1. 選取&#x200B;[!UICONTROL **新交談**]。

1. 在文字欄位中，提示代理程式驗證欄位或資料集。 例如：

   **提示**

   > 驗證資料集「Electronics Sample 1000」

   ![同事聊天首頁畫面，提示訊息欄位中輸入驗證資料集Electronics Sample 1000。](../../assets/data-validation-aep/start-session.png)

   >[!TIP]
   >
   >在資料集名稱前面加上「dataset」一詞，以便技能能正確識別。 例如，使用「驗證資料集Electronics Sample 1000」而非「驗證Electronics Sample 1000」。

   您的請求會路由至資料驗證技能，該技能會分析資料集的範例並在相同交談中傳回結果。

## 選擇要驗證的內容

您可以驗證單一欄位或整個資料集。

>[!BEGINTABS]

>[!TAB 欄位驗證]

驗證資料集中的特定欄位。 此選項提供：

* Null計數和相異值計數。
* 前幾個相異值及其頻率。
* AI輔助語意驗證，會根據欄位的中繼資料及其實際值，標籤不符合欄位預期格式的值。

提示範例：

* 驗證Customers_2024資料集中的電子郵件欄位。
* 驗證資料集customer_events_2024的欄位狀態。
* 驗證客戶資料集的欄位person.address.city。

>[!TAB 資料集驗證]

一次驗證資料集中最多五個欄位。 您可以自行指定欄位，或讓技能分析資料集並自動選取最相關的欄位。 在您驗證的每個欄位中，此選項會傳回與欄位驗證相同的資訊。

提示範例：

* 驗證Customer Data 2024資料集
* 驗證欄位電子郵件、Customers_2024電話。
* 摘要客戶資料的firstName、lastName、birthDate。

>[!ENDTABS]

## 檢閱結果

對於每個已驗證的欄位，結果會以一列顯示在表格中，內含下列欄：

| 欄 | 說明 |
| --- | --- |
| [!UICONTROL 欄位名稱] | 欄位名稱。 |
| [!UICONTROL 欄位路徑] | 結構描述中的欄位完整路徑。 |
| [!UICONTROL 欄位型別] | 欄位的資料型別。 |
| [!UICONTROL 有效值] | 通過驗證的抽樣值的百分比。 |
| [!UICONTROL 不同的值] | 相異的取樣值的百分比。 |
| [!UICONTROL Null值] | 空值的抽樣值的百分比。 |
| [!UICONTROL 前5個相異值] | 五個最常見的值及其頻率。 |
| [!UICONTROL 前5個無效值] | 五個最常見的無效值，每個都有說明，例如「不是有效的電子郵件格式」。 |
| [!UICONTROL 其他insight] | 有關欄位品質的簡短自然語言備註。 |

在結果底下，同事新增了&#x200B;**後續步驟**&#x200B;清單，建議後續提示，例如驗證其他欄位或重新執行資料集。

當您驗證單一欄位時，Co-worker也會傳回圖表：

![同事聊天顯示Brand欄位的環圈圖和書面摘要，報告79.5%的有效值、20.5%的null值，以及未偵測到無效值。](../../assets/data-validation-aep/null-values.png)

選取&#x200B;[!UICONTROL **圖表**]&#x200B;或&#x200B;[!UICONTROL **表格**]&#x200B;以切換相同結果的檢視。

驗證資料集時，結果會顯示在表格中，且每個欄位會有一列。 您自行命名的欄位會依您的指定顯示：

![標題為Electronics Sample 1000 Field Validation的同事聊天表，顯示使用者在提示中命名的類別、品牌和價格欄位的驗證結果。](../../assets/data-validation-aep/field-validation.png)

技能選取的欄位會自動以相同方式顯示：

![同事聊天表顯示Electronics Sample 1000資料集中五個自動選取欄位的驗證結果：類別、品牌、價格、詳細目錄及狀況。](../../assets/data-validation-aep/dataset-validation.png)

選取&#x200B;[!UICONTROL **CSV**]&#x200B;以下載完整結果表格。

## 資料驗證執行的檢查

此技能會針對每個欄位和資料集執行下列型別的檢查：

* **完整度檢查**： null且遺漏計數和百分比。
* **分佈檢查**：最上層的相異值及其分佈，以及高基數偵測。
* **針對結構描述進行語意檢查**：使用XDM欄位名稱、型別和描述來推斷有效值的樣子，然後標示異常。
* **資料型別感知檢查**，若適用：
  * 電子郵件：格式和網域可行性。
  * 電話：格式整備，例如E.164。
  * 日期和時間戳記：基本格式檢查，例如ISO-8601。

這些檢查將確定性統計資料與LLM輔助語意驗證結合，以偵測看起來錯誤的值，即使這些值在技術上符合結構描述亦然。

## 限制

在驗證資料之前，請記住下列限制。 這些限制在效能與功能之間取得平衡，並設定您對分析和深入分析的期望。

* **僅取樣**：技能會驗證資料集的範例（通常是最近的1,000列），而不是整個資料集。 無法使用完整資料集掃描。
* **欄位計數限制**：當您驗證資料集時，技能會分析每個請求最多五個欄位。 您可以指定這些欄位，或讓技能自動選取它們。
* **機率語意**：無效值的偵測部分依賴於LLM型推斷，這有時可能會遺漏細微的錯誤或標幟邊界值。
* **唯讀**：技能不會變更您的資料或其結構描述。 它會強調潛在問題，但不會執行自動化修正。

如果您的驗證需求較為詳盡或需要複雜的商業邏輯，請以其他工具（例如查詢服務或資料準備驗證）來補充這些結果。

**相關資訊**

* [升級時驗證Adobe Analytics至Customer Journey Analytics的資料](./data-validation-aa-cja.md)
* [使用Co-worker中的資料驗證技能驗證Customer Journey Analytics資料](./validate-dataset-quality-for-cja.md)
* [驗證您的資料（AI助理）](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/agents/data-validation)
* [信任您的Customer Journey Analytics報告： Adobe CX Enterprise Coworker中的資料驗證技能](https://www.youtube.com/watch?v=gCSm_QYSYhk) （影片）
