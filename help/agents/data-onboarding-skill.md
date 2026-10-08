---
title: 與同事一起將資料上線
description: 瞭解如何使用CX Coworker中的資料上線技能，透過對話工作流程將新資料來源上線到Adobe Experience Platform。
hide: true
source-git-commit: 8f7d5307b1928c052f020ca5e7aae3feee7af03e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 2%
---

# 與同事一起將資料上線

>[!AVAILABILITY]
>
>資料入門技能為測試版。 文件和功能可能會有所變更。
>
>此資料上線技能可供有權存取Adobe CX Enterprise Coworker的客戶使用，其中您的組織也必須啟用此技能。<!-- VERIFY BEFORE PUBLISH: confirm exact permission/entitlement name with Umesh Gohil, PLAT-296546. -->

使用CX Coworker中的資料上線技能，透過單一對話工作流程將新資料上線到Adobe Experience Platform中。 請描述您的意圖和同事指導您完成來源選擇、資料品質、語意擴充、結構描述對應、結構描述建立和資料流建立，而不是透過多個畫面來手動連線來源和建立結構描述。

<!-- VERIFY BEFORE PUBLISH: confirm the loaded skill name ("Onboard Data to Experience Platform") and the exact post-landing prompt/flow with Umesh Gohil once flag access is arranged. -->

## 先決條件 {#prerequisites}

在開始之前，請確定您已：

- 存取Adobe Experience Platform以及適當的組織和沙箱。
- 存取為貴組織啟用資料上線技能的Adobe CX Enterprise Coworker。
- 在Adobe Experience Platform中建立結構描述的許可權。

如需有關安裝外掛程式的說明，請參閱[Co-worker UI指南](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 使用資料上線技能 {#use-the-data-onboarding-skill}

今天，資料上線技能從Experience Platform UI中的方案建立開始，這會開啟已完成您意圖的同事。

使用資料上線技能：

1. 在Adobe Experience Platform中，導覽至&#x200B;**[!UICONTROL 結構描述]**，然後選取&#x200B;**[!UICONTROL 建立結構描述]**。
1. 在&#x200B;**[!UICONTROL 建立結構描述]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL 使用AI載入資料]**，然後選取&#x200B;**[!UICONTROL 選取]**。

   ![已選取[建立結構描述]對話方塊中的[內建資料與AI]選項。](./assets/data-onboarding-skill/create-a-schema-dialog.png)

1. CX Coworker會在新的瀏覽器標籤中開啟，系統已預先填入您結構描述建立意圖的提示，因此您不需要重新陳述。
1. 在提示時選擇要上線的來源，例如[!DNL Amazon S3]、[!DNL Data Landing Zone]、[!DNL Delta Share]或[!DNL Marketo]。

   <!-- VERIFY BEFORE PUBLISH: screenshot of the Coworker landing/session-start state does not exist yet anywhere. Capture once flag access is confirmed. -->

1. 透過資料品質審查、語意擴充、結構描述對應和結構描述建立繼續與同事對話，並隨時確認每個步驟。

如需使用CX Coworker的詳細資訊，請參閱[同事UI指南](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)。

## 支援的使用案例 {#supported-use-cases}

探索資料上線技能幫助您完成的上線工作流程部分。

### 選取並連線來源

請說明您要匯入的資料，讓Co-worker協助識別正確的來源，而不是手動尋找和設定來源聯結器。

### 檢閱資料品質

在您認可結構描述之前，同事會針對選取的來源顯示資料品質訊號，因此您可以在處理程式的較早階段發現問題。

### 在語義上豐富資料

Co-worker建議傳入欄位的語意意義，減少將原始欄位對應到標準定義的手動工作。

### 對應和建立結構描述

同事會將檢閱的欄位對應到新的或現有的結構描述，並直接在Adobe Experience Platform中建立它，作為相同交談的一部分。

### 建立資料流

同事透過建立所需資料流來持續將資料匯入，完成上線。

## 後續步驟 {#next-steps}

閱讀本指南後，您應該瞭解如何從架構建立開始資料入門技能，以及它有助於您在CX Coworker中完成什麼。

如需Experience Platform UI程式和存取/適用案例，請參閱結構描述UI指南中的[使用AI載入資料](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#data-onboarding-skill)。
