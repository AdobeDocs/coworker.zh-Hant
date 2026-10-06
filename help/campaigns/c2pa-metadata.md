---
description: 瞭解同事行銷活動如何從產生到電子郵件傳遞，自動附加並保留影像上的C2PA中繼資料。
title: 同事行銷活動中的C2PA中繼資料
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 4%
---
# 同事行銷活動中的C2PA中繼資料 {#overview}

圍繞創作AI透明度的新法律不斷湧現，Adobe正在努力滿足各個司法轄區的適用要求。 [C2PA中繼資料](https://c2pa.org/)是Adobe用來符合這些法律要求的來源工具。

C2PA中繼資料是持久且隱藏的中繼資料，會記錄內容的建立或編輯方式。 當您使用Co-worker Campaigns中的產生AI工具產生或編輯影像時，C2PA中繼資料會自動附加至該影像。 您不需要採取任何動作。

## 電子郵件行銷活動中的C2PA中繼資料 {#c2pa-metadate-email}

電子郵件行銷活動中傳送的影像會儲存其C2PA中繼資料，讓收件者可以直接從傳送的電子郵件驗證任何影像的來源和真實性。

## 附加C2PA中繼資料的動作 {#actions}

下表根據在Co-worker Campaigns中產生影像時執行的影像動作，摘要附加C2PA中繼資料的時間。

| 動作 | 說明 | 要附加C2PA中繼資料嗎？ | 使用案例範例 |
| --- | --- | --- | --- |
| **產生影像** | 從文字提示或參考影像建立新影像，或從現有影像產生類似影像。 | 一律。 影像是由產生式AI產生，因此一律會攜帶最新的C2PA中繼資料。 | 電子郵件促銷活動的橫幅影像是從描述所需視覺效果的文字提示中產生。 |

## 內容型別及其範圍 {#content-types}

* **影像**：已涵蓋。 使用產生AI產生影像時，會附加C2PA中繼資料，並透過在Co-worker Campaigns中由影像產生執行的裁切、文字覆蓋和影像覆蓋作業來保留。
* **文字**：不適用。 「同事行銷活動」中的純文字輸出（例如產生副本、翻譯和品牌對齊建議）不需要C2PA中繼資料。

## 內容移動時發生什麼事 {#content-moves}

Co-worker Campaigns會保留與支援的影像資產相關聯的C2PA中繼資料。 如果影像在匯入至「同事行銷活動」時包含C2PA中繼資料，則當資產用於產生的行銷活動內容和傳出電子郵件體驗時，將保留這些憑證。

## 其他資源 {#resources}

* [Generative AI內容透明度](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency){target="_blank"}
* [Adobe Experience Cloud Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [護欄與限制](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/generate-content/gs-generative#generative-guardrails){target="_blank"}
