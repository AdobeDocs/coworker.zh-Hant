---
title: 透過同事偵測Experience Platform異常
description: 瞭解如何使用同事聊天在Adobe Experience Platform中偵測異常。 探索內嵌、細分和目的地啟用量度的提示。
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
jira: PLAT-313965
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 1%
---

# 偵測Experience Platform異常

使用[!DNL Adobe CX Enterprise Coworker]聊天來識別支援的Adobe Experience Platform量度中的尖峰和下降。 詢問資料流程和受眾，找出與基準的偏差。

先從寬泛的問題開始，然後專注於需要注意的流程或對象。 在決定調查之前，請先檢閱報告的量度及其基準線。

>[!AVAILABILITY]
>
>異常偵測的可用性有限。 預計於2027年第一季度全面推出。

>[!NOTE]
>
>異常偵測提供資訊而不變更您的資料或設定。

## 可用的診斷技能

使用`baseline-anomalies`外掛程式來偵測異常、比較趨勢，以及檢閱流量狀況或目前工作失敗。 外掛程式預設是以[!DNL Coworker]中的Experience Platform和Apps產品來設定。

根據您需要的資訊選擇問題型別。

| 技能 | 目的 |
| --- | --- |
| [!UICONTROL 基線異常搜尋流程異常] | 在擷取、細分、匯出和目的地階段偵測記錄磁碟區中的尖峰或下降，以及失敗的記錄。 |
| [!UICONTROL 基線異常搜尋對象異常] | 偵測已實現的受眾設定檔計數中的尖峰或下降，以及退出設定檔計數中的尖峰。 |
| [!UICONTROL 基線異常摘要流量趨勢] | 比較近期和一般流量輸送量，而不使用異常判斷。 |
| [!UICONTROL 基線異常摘要對象趨勢] | 比較批次細分的最近和典型合格與退出的設定檔計數，沒有異常判斷或預期的範圍。 |
| [!UICONTROL 基線異常檢查流程狀況] | 檢閱重複資料刪除的成功和失敗的執行計數，加上依活動或流程區分的失敗記錄總計。 |
| [!UICONTROL 基線異常搜尋失敗的工作] | 檢閱目前失敗的工作及其失敗原因，排除已復原的失敗和個別記錄的詳細資料。 |

趨勢摘要會說明變更，但不會判斷這些變更是否為異常。 當您需要尖峰或下降評估時，請使用異常問題。

## 開始之前

外掛程式已預設設定。 若要在詢問診斷問題之前檢查其狀態，請按照以下步驟操作。

1. 移至&#x200B;**[!UICONTROL 自訂]**。

1. 選取&#x200B;**[!UICONTROL 外掛程式]**。

1. 開啟&#x200B;**[!UICONTROL 基準線異常]**，並確認其狀態為&#x200B;**[!UICONTROL 作用中]**。

識別您要檢查的沙箱和區域。 針對特定資源，使其流程、區段或目的地名稱或識別碼準備就緒。

如需一般聊天指示，請參閱[開始聊天](/help/chat/ui-guide.md)。

## 詢問異常狀況

說明您要檢查的區域或資源，以及您要檢查的時間週期。

使用下列範例提示作為起點。 以您組織的名稱取代範例名稱。

| 目標 | 範例提示 |
| --- | --- |
| 檢查支援區域 | 過去24小時內是否有任何異常？ |
| 檢查內嵌 | 過去24小時內我的內嵌是否有任何異常？ |
| 檢查特定流程 | 在過去24小時內，擷取流程CustomerImport是否有任何異常？ |
| 檢查分段 | 在過去24小時中，我的區段是否有任何異常？ |
| 檢查特定區段 | 過去24小時內區段LoyaltyMembers是否有任何異常？ |
| 檢查目的地啟用 | 過去24小時內，我的目的地啟用是否有任何異常？ |
| 檢查已實現的設定檔尖峰 | 今天是否有對象在已實現的設定檔中看到尖峰？ |
| 檢查失敗的記錄異常 | 失敗的記錄在流量CustomerImport上是否異常高？ |

這廣泛的問題會檢查資料流程和對象。 確認回應中識別的沙箱和時段。

<!-- Author review: Confirm exact supported time windows, defaults, time zone handling, and data freshness. -->

## 檢閱異常結果

比較受影響資源與時間週期的報告值與其基準。 使用差異來識別需要進一步調查的專案，而不是將異常視為已確認的原因。

例如，擷取輸入記錄的減少可識別磁碟區變更。 這項變更本身並不能解釋為何抵達的記錄較少。

結果可以顯示為表格或書面摘要。 表格可以在[!UICONTROL 高風險]和[!UICONTROL Medium風險]下將異常分組。

![異常結果群組擷取和目的地磁碟區在中高風險下尖峰和下降，資源名稱和值已修訂。](assets/anomaly-detection/anomaly-detection-results.png){width="900" zoomable="yes"}

此範例會依風險將流量異常分組，並建議調查執行計數或趨勢歷史記錄。 資源名稱和值會加上密文。

| 結果詳細資料 | 檢閱內容 |
| --- | --- |
| [!UICONTROL 時間(UTC)] | 國際標準時間中的事件時間或時間視窗。 |
| [!UICONTROL 階段] | 受影響的處理階段，例如擷取或目的地。 |
| [!UICONTROL 流量] | 受影響的流程，以名稱或識別碼識別。 |
| [!UICONTROL 發生什麼事] | 偵測到變更，例如音量尖峰或下降。 |
| [!UICONTROL 實際與預期] | 觀察值與基線或預期範圍比較。 |

與風險分組一起檢閱說明。 若為對象異常，高表示與正常值有大幅偏離。 Medium表示明顯但中度偏離。 僅傳回高和Medium異常。

當基線歷史記錄高度變數時，受眾結果會排除Medium異常。 因此，任何具有高度變數記錄的傳回異常都會屬於高風險階層。

請使用風險層級來排定調查的優先順序，而非建立根本原因。

例如，一個回應會針對一到四的預期範圍識別10筆輸入記錄，作為中度風險尖峰。 一般水準大約是一筆記錄，因此相對於基準線的偏差較大。 絕對體積仍然很小。

將歷史異常視為目前問題之前，請檢查事件時間。 過去24小時以外的事件不會建立基礎條件是否復原。

<!-- Author review: Confirm flow risk tier definitions and whether persistence is reported. -->

### 基準線和預期範圍

每小時異常比較會使用過去14天的相同小時。 這雖然可說明每小時的典型模式，但無法說明更廣的季節性。

針對對象異常，預期範圍會以中間值為中心，並根據歷史計數的變數加寬。 如果計算出的下限為負數，則範圍會改用最低的歷史計數。 因此，範圍可以延伸至中間值以上、而非下方。

超過預期範圍的已實現設定檔計數為尖峰。 低於範圍的計數會下降。 設定檔正常存在時，零計數為高風險下降。

退出的設定檔計數只會產生尖峰預測。 較少的退出點會被視為正常，而不是下降異常。

### 未傳回任何異常

回應可報告請求的對象和期間未傳回任何高或Medium異常。

![對象異常摘要不會報告超過168小時的高或Medium異常，並包含有關已排除歷程記錄的警告。](assets/anomaly-detection/anomaly-detection-no-anomalies.png){width="900" zoomable="yes"}

此範例包括關於歷史記錄不足或大部分為零的警告。 它不會確認每小時都評估過，或此對象已排除。 對象名稱和識別碼會經過編輯。

### 基準線歷史記錄不足

基線歷史記錄會影響對象是否可評估異常。

對象異常偵測不會評估歷程記錄少於五天或歷程記錄大多包含零的列。

>[!IMPORTANT]
>
>沒有報告的異常並不表示已評估每個資源。 回應可能無法確認對象是否評估或略過。

<!-- Author review: Confirm flow minimum history requirements and whether audience evaluation status or excluded resources can be retrieved. -->

## 精簡您的問題

將您的下一個問題集中在受影響的資源上。 例如，在廣泛的擷取檢查後，詢問已命名流程的異常狀況。

詢問關於最近24小時的問題後，請延長此後續追蹤的期間：

```text
What about in the past two weeks?
```

即使過去24小時內未出現任何異常，回應仍可識別歷史異常。

如需更深入的調查，請詢問關於資料流執行計數、資料流趨勢、對象趨勢或目前失敗的工作。 您也可以在調查時詢問個別工作的相關資訊。

根據您需要的資訊選擇下一個問題。 趨勢和健康情況摘要不提供異常判決。

| 目標 | 範例提示 | 有何期望 |
| --- | --- | --- |
| 檢閱對象趨勢 | 我的對象在上星期有什麼變化？ | 批次細分的最近和典型合格及退出設定檔計數，沒有預期範圍。 |
| 檢閱流程趨勢 | 擷取量在上星期有什麼改變？ | 相較於一般輸送量，近期的輸送量並無異常判斷。 |
| 檢閱流程健康狀態 | 在過去24小時中，我的擷取流程執行了多少次成功或失敗？ | 無失敗原因的重複執行計數與彙總失敗記錄總計。 |
| 調查失敗的工作 | 哪些匯出作業在過去24小時內失敗，為什麼？ | 最新狀態在請求範圍內失敗的工作，其中包含工作失敗原因。 |
| 調查流程失敗 | 流程CustomerImport發生什麼錯誤？ | 目前與流程相關聯之失敗工作的失敗原因，沒有個別記錄的詳細資料。 |

對象趨勢歷史記錄會保留約兩週或336小時。 一般值是該小時前14天的中位數。

對於目前失敗的工作，空白結果表示在要求的範圍內目前沒有失敗的工作。 這並不表示在要求的期間內沒有發生任何失敗。 排除失敗且稍後成功的作業。

使用健康情況檢查技能繼續調查，或使用警示技能為支援的資產啟用警示。 這些動作會使用個別技能，而非異常偵測本身。

如需相關警示工作流程，請參閱[客戶警示技能](/help/chat/use-cases/customer-alerts/customer-alerts.md)。

<!-- Author review: Validate a complete public example response and the supported alert assets and setup before adding an alert procedure. -->

## 量度參考

限量版包含下列七個涵蓋擷取、細分和目的地啟用的量度。 使用此參考來識別與每個區域關聯的計數。

| 區域圖 | 量度識別碼 | 測量計數 |
| --- | --- | --- |
| 攝取 | `input_record_count` | 擷取流程的輸入記錄計數。 |
| 攝取 | `failed_record_count` | 擷取流程的失敗記錄數。 |
| 分段 | `__segment_{segment_id}__realized_profiles` | 符合區段資格的設定檔計數。 |
| 分段 | `__segment_{segment_id}__exited_profiles` | 退出區段的設定檔計數。 |
| 目的地啟用 | `{destination}_input_record_count` | 目的地的輸入記錄計數。 |
| 目的地啟用 | `{destination}_skipped_record_count` | 目的地的略過記錄數。 |
| 目的地啟用 | `{destination}_output_record_count` | 目的地的輸出記錄計數。 |

<!-- Author review: Confirm metric aggregation intervals and identifier visibility. -->

## 範圍和限制

使用異常偵測來識別偏差，而不是確認根本原因或修復資源。

您可以依名稱或識別碼詢問流程、區段和目的地。 流量異常偵測涵蓋擷取、細分、匯出和目的地階段。

將失敗的工作技能用於目前失敗的工作及其失敗原因。 已復原的故障會被排除。 作業診斷不包含個別記錄的詳細資訊或異常裁決。

流量健康情況提供彙總計數，而非失敗原因。 趨勢摘要則說明最近的和典型值，而非異常判決。 對象趨勢摘要僅涵蓋批次細分。

異常偵測不會變更您的資料或設定。 針對支援的警示動作和更深入的健康調查，使用不同的技能。

<!-- Author review: Confirm job identifier support and any recommendation capabilities before adding examples. -->
