---
title: Google Ads外部聯結器
description: 瞭解如何為貴組織在CX Enterprise Coworker中設定Google Ads外部聯結器，並使用Google登入，以在聊天中使用Google Ads資料。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此聯結器為Beta版。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 33bbe0ce723fcad4e25353749039c6b81b0dbdf9
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 1%
---

# Google Ads外部聯結器 {#google-ads}

使用[!DNL Google Ads]外部聯結器在Adobe CX Enterprise Coworker中處理您的[!DNL Google Ads]資料。 設定聯結器後，請詢問同事您可存取哪些廣告帳戶、哪些欄位和量度可供使用，以及行銷活動的執行方式。 聯結器是模型內容通訊協定(MCP)伺服器。

>[!AVAILABILITY]
>
>[!DNL Google Ads]外部聯結器為Beta版。 文件和功能可能會有所變更。

## 聯結器設定 {#connector-configuration}

聯結器組態程式有兩個獨立的部分：

* **組織設定：**&#x200B;管理員會為整個組織設定一次聯結器，並選取成員可以使用的工具。 Adobe提供OAuth應用程式，因此沒有可輸入的應用程式認證。
* **成員登入：**&#x200B;每個成員都使用自己的[!DNL Google]帳戶登入。 成員只能存取其[!DNL Google]帳戶可存取的[!DNL Google Ads]帳戶。

儲存組織設定不會登入任何成員或授與[!DNL Google Ads]帳戶的存取權。 每個成員必須個別登入。

## 先決條件 {#prerequisites}

開始之前，請確定您具備下列條件：

* **對於組織設定：**&#x200B;具有在同事中管理組織聯結器的許可權的帳戶。
* **對於成員登入：**&#x200B;擁有您計畫使用[!DNL Google Ads]帳戶存取權的[!DNL Google]帳戶。

## 為您的組織設定聯結器 {#configure-organization}

管理員可讓組織中的所有人使用[!DNL Google Ads]聯結器。 組織頁面上的變更會套用至組織中的所有使用者。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 組織]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。 在&#x200B;**[!UICONTROL Google Ads]**&#x200B;卡片上，選取&#x200B;**[!UICONTROL 設定]**。

1. 在&#x200B;**[!UICONTROL 為您的組織設定Google廣告]**&#x200B;對話方塊中，確認&#x200B;**[!UICONTROL OAuth應用程式]**&#x200B;是&#x200B;**[!UICONTROL Adobe管理的OAuth應用程式]**。 Adobe提供[!DNL Google Ads]應用程式，因此您不需要輸入應用程式認證。 在&#x200B;**[!UICONTROL 使用者可用的工具]**&#x200B;下，選取貴組織需要的工具。 如需詳細資訊，請參閱[可用的工具](#available-tools)。 檢閱&#x200B;**[!UICONTROL 每個人單獨登入]**&#x200B;通知，然後選取&#x200B;**[!UICONTROL 儲存連線]**。

   ![使用Adobe管理的OAuth應用程式、選取的所有三個工具，以及每位人員分別登入通知，為您的組織設定Google Ads。](./assets/google-ads/org-configure.png){width="500" zoomable="yes"}

1. 檢閱已儲存的&#x200B;**[!UICONTROL google-ads]**&#x200B;聯結器詳細資料。

   | 設定 | 說明 |
   | --- | --- |
   | **[!UICONTROL Source]** | 您環境的MCP伺服器URL。 |
   | **[!UICONTROL 驗證]** | 驗證方法，`google-ads_login`。 |
   | **[!UICONTROL 工具原則]** | 允許的刀具名稱或陣列。 |
   | **[!UICONTROL Connection]** | 您自己的登入狀態。 |

   ![已儲存的Google-ads聯結器詳細資訊，其中顯示來源、驗證方法、具有三個允許工具的工具原則，以及具有「登出」和「重新整理」按鈕的「已登入」。](./assets/google-ads/org-details.png){width="700" zoomable="yes"}

聯結器詳細資料上的&#x200B;**[!UICONTROL 連線]**&#x200B;狀態是指您自己的連線，而不是組織的連線。 每個成員仍需使用自己的帳戶登入。 成員登入後，可以選取&#x200B;**[!UICONTROL 測試]**&#x200B;以測試工具探索。 若要自行使用聯結器，請依照[登入為成員](#sign-in-as-a-member)中的步驟操作。

若要停止提供聯結器給您的組織，請在聯結器詳細資訊頁面上選取&#x200B;**[!UICONTROL 移除]**。

### 可用的工具 {#available-tools}

[!DNL Google Ads]聯結器提供下列工具：

| 工具 | 說明 |
| --- | --- |
| `customers_list_accessible_customers` | 列出您登入的[!DNL Google]帳戶可直接存取的客戶ID。 |
| `metadata_get_resource_metadata` | 尋找可用於[!DNL Google Ads]資源（例如行銷活動或廣告群組）的欄位、量度和區段。 |
| `search_search` | 擷取[!DNL Google Ads]組態或報告資料。 |

## 以成員身分登入 {#sign-in-as-a-member}

管理員設定聯結器後，每個成員都會使用自己的[!DNL Google]帳戶登入。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 使用者]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。 在&#x200B;**[!UICONTROL Google Ads]**&#x200B;卡片上，選取&#x200B;**[!UICONTROL 登入]**。

   如果卡片顯示&#x200B;**[!UICONTROL 未設定]**&#x200B;或聯結器無法使用，請要求您的管理員[設定聯結器](#configure-organization)。

1. 在[!DNL Google] **[!UICONTROL 選擇帳戶]**&#x200B;畫面上，選取可存取您[!DNL Google Ads]帳戶的帳戶，或選取&#x200B;**[!UICONTROL 使用其他帳戶]**。 然後完成貴組織所需的任何登入步驟，例如單一登入(SSO)、多重驗證(MFA)或身分驗證。

   步驟及其順序取決於您的組織和帳戶政策。

   ![Google為Adobe Experience Platform選擇一個帳戶畫面，其中列出兩個已編輯的帳戶以及「使用其他帳戶」選項。](./assets/google-ads/member-choose-account.png){width="500" zoomable="yes"}

1. 檢閱選取的帳戶和您授權的應用程式，然後選取[繼續]。**&#x200B;**

   [!DNL Google]將應用程式名稱顯示為[!DNL Adobe Experience Platform]。 如果您之前使用過應用程式，[!DNL Google]會顯示您正在重新登入。 初次使用的使用者可能會看到不同的提示。

   ![Google畫面顯示您正使用密文帳戶及[取消]和[繼續]按鈕重新登入Adobe Experience Platform。](./assets/google-ads/member-continue.png){width="500" zoomable="yes"}

1. 檢閱存取要求，然後選取[繼續]。**&#x200B;**

   ![Google熒幕顯示Adobe Experience Platform想要存取您的Google帳戶，該帳戶含有密文的帳戶、應用程式已擁有部分存取權的通知，以及「取消」和「繼續」按鈕。](./assets/google-ads/member-consent.png){width="500" zoomable="yes"}

   >[!IMPORTANT]
   >
   >只有在您識別應用程式且您的組織核准所要求的存取權時，才繼續。

1. 在[!DNL Google]將您送回同事之後，請開啟&#x200B;**[!UICONTROL google-ads]**&#x200B;聯結器詳細資料。 確認聯結器顯示&#x200B;**[!UICONTROL 已連線]**&#x200B;且&#x200B;**[!UICONTROL 已登入]**。

   將&#x200B;**[!UICONTROL 資源識別碼]**&#x200B;保留為預設值，除非管理員另有指示。 此欄位會設定在您登入時傳送的Token對象。 若要返回預設值，請清除欄位並選取&#x200B;**[!UICONTROL 儲存資源識別碼]**。

   ![google-ads聯結器詳細資訊，其中顯示「已連線」狀態、「已登出」和「重新整理」按鈕的「已登入」連線，以及「資源識別碼」欄位。](./assets/google-ads/member-connected.png){width="700" zoomable="yes"}

1. 選取&#x200B;**[!UICONTROL 測試]**&#x200B;以檢查同事是否可以探索聯結器工具。 然後檢閱管理員啟用的&#x200B;**[!UICONTROL 工具]**，以檢視您可以使用的工具。

   **[!UICONTROL 測試]**&#x200B;在您登入後即可使用。

   ![管理員區段所啟用的工具，列出三種Google廣告工具及其說明。](./assets/google-ads/member-tools.png){width="700" zoomable="yes"}

若要中斷您的[!DNL Google]帳戶與聯結器的連線，請選取&#x200B;**[!UICONTROL 登出]**。 聯結器詳細資料也顯示&#x200B;**[!UICONTROL 工具逾時]**&#x200B;設定和&#x200B;**[!UICONTROL 重新整理]**&#x200B;控制項。

**[!UICONTROL 已連線]**&#x200B;狀態無法確認存取特定廣告帳戶或每個報表是否成功執行。 若要確認您的存取權，[請檢查您的廣告帳戶存取權](#check-ad-account-access)。

## 檢查您的廣告帳戶存取權 {#check-ad-account-access}

若要確認您可以使用哪些[!DNL Google Ads]帳戶，請開始聊天並輸入提示。

範例提示：

* 「我可以存取哪些Google Ads帳戶？」

同事使用`customers_list_accessible_customers`工具列出您的[!DNL Google]帳戶可直接存取的客戶ID。 這是帳戶存取檢查，而非效能報表。 如果您使用管理員帳戶，清單不會包含該帳戶下的所有帳戶。

請求報表之前，請先執行下列動作：

* 從清單中選擇帳戶。
* 指定具有開始和結束日期的日期範圍。
* 要求同事尋找可用於報表的欄位和量度。

## 疑難排解存取權 {#troubleshoot-access}

如果您無法存取您的[!DNL Google Ads]資料，請向管理員檢查下列專案：

| 區域圖 | 檢查內容 |
| --- | --- |
| [!DNL Google]帳戶 | 您使用可存取[!DNL Google Ads]帳戶的[!DNL Google]帳戶登入。 |
| 帳戶許可權 | 您的[!DNL Google]帳戶擁有您要使用[!DNL Google Ads]帳戶的許可權。 |
| 管理員帳戶 | 如果您透過管理員帳戶存取帳戶，您的管理員會確認所需的管理員帳戶設定。 |
| 工具選取 | 您的管理員已在&#x200B;**[!UICONTROL 使用者可用的工具]**&#x200B;下啟用您需要的工具。 |
| 資源識別碼 | **[!UICONTROL 資源識別碼]**&#x200B;使用預設值，除非您的管理員另有指示。 |
