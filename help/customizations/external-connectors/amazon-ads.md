---
title: Amazon Ads外部聯結器
description: 瞭解如何為貴組織在CX Enterprise Coworker中設定Amazon Ads外部聯結器，並使用Amazon登入，以在聊天中使用Amazon Ads工具。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此聯結器為Beta版。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 80dda0b442d6c7fe560c965b985f58173b73fe13
workflow-type: tm+mt
source-wordcount: '3078'
ht-degree: 1%
---

# Amazon Ads外部聯結器 {#amazon-ads}

使用[!DNL Amazon Ads]外部聯結器在Adobe CX Enterprise Coworker中處理您的[!DNL Amazon Ads]資料。 設定聯結器後，請詢問同事您可存取哪些廣告帳戶，並檢閱行銷活動、報表、帳單和其他帳戶資訊。 聯結器是由[!DNL Amazon]裝載的模型內容通訊協定(MCP)伺服器。

>[!AVAILABILITY]
>
>[!DNL Amazon Ads]外部聯結器為Beta版。 文件和功能可能會有所變更。

## 聯結器設定 {#connector-configuration}

聯結器組態程式有三個獨立的部分：

* **[!DNL Amazon]準備：** [!DNL Amazon Ads]帳戶管理員可讓每個成員存取他們所需的Advertising帳戶。 如果您的組織使用自己的OAuth應用程式，應用程式擁有者會確認其核准，並註冊同事重新導向URL。
* **組織設定：**&#x200B;同事管理員會為整個組織設定一次聯結器。 管理員會選擇區域、OAuth應用程式以及成員可以使用的工具。
* **成員登入：**&#x200B;每個成員都使用自己的[!DNL Amazon]帳戶登入。 成員只能存取其[!DNL Amazon]帳戶有使用許可權的廣告帳戶。

儲存組織組態不會登入任何成員或授予[!DNL Amazon Ads]許可權。 每個成員都必須在[!DNL Amazon Ads]中擁有必要的存取權，而且必須個別登入。

## 先決條件 {#prerequisites}

開始之前，請確定您具備下列條件：

* **同事存取：**&#x200B;在有[!DNL Amazon Ads]聯結器可用的組織中，具有管理組織聯結器的許可權的帳戶。
* **Advertising帳戶：**&#x200B;您打算使用的廣告帳戶及其[!DNL Amazon Ads]地區，以及具有這些帳戶所需許可權的成員。 如需詳細資訊，請參閱[授與Advertising帳戶存取權](#grant-member-access)。
* **OAuth應用程式決定：**&#x200B;選擇下列選項：
  * **Adobe管理的OAuth應用程式：** Adobe管理應用程式註冊及其認證。 受管理的應用程式必須在您的環境中可用。
  * **您自己的OAuth應用程式：**&#x200B;已針對[!DNL Amazon Ads] API核准的[!DNL Login with Amazon]應用程式、其OAuth使用者端ID和使用者端密碼，以及可編輯其安全性設定檔的管理員。 已註冊的安全性設定檔本身不會授予[!DNL Amazon Ads] API核准。

引導式設定支援每個組織一個[!DNL Amazon Ads]連線和一個區域。 每個成員都使用自己的[!DNL Amazon]帳戶登入。 Adobe管理的應用程式是共用應用程式註冊，而非共用[!DNL Amazon]帳戶。

## 準備Amazon存取權 {#prepare-amazon}

在Co-worker中設定聯結器之前，請在[!DNL Amazon]中準備您的應用程式和帳戶存取權。 應用程式設定存取權和廣告資料存取權是分開的。 使用聯結器的成員不需要許可權即可編輯應用程式。

### 確認應用程式核准 {#confirm-app-approval}

如果您使用自己的OAuth應用程式，請要求應用程式擁有者確認正確的[!DNL Login with Amazon]安全性設定檔及其[!DNL Amazon Ads] API核准。 建立安全性設定檔，或在[!DNL Amazon]開發人員控制檯中檢視應用程式，不會取代[!DNL Amazon Ads] API核准。 如需詳細資訊，請參閱[!DNL Amazon Ads]檔案中的[Amazon Ads MCP快速入門](https://advertising.amazon.com/API/docs/en-us/mcp/get-started)和[使用OAuth連線至Ads MCP伺服器](https://advertising.amazon.com/API/docs/en-us/mcp/oauth)。

若是您自己的應用程式，「同事」會自動套用下列設定。 您無法在設定對話方塊中輸入這些值。

| 設定 | 值 |
| --- | --- |
| 授權 URL | `https://lwa.amazon.com/ap/oa` |
| 權杖 URL | `https://api.amazon.com/auth/o2/token` |
| 要求的範圍 | `advertising::campaign_management` |
| 程式碼交換(PKCE)的校訂金鑰 | 已啟用 |
| 權杖端點使用者端驗證 | `client_secret_post`，作為機密使用者端 |
| 動態用戶端註冊 | 不支援 |
| 傳輸和工具逾時 | 可串流的HTTP，60秒 |

如果您使用Adobe管理的OAuth應用程式，Adobe會管理應用程式註冊及其認證。 您不需要完成此步驟或輸入應用程式認證。

### 註冊重新導向URL {#register-redirect-url}

如果您使用自己的OAuth應用程式，請在您的[!DNL Login with Amazon]應用程式中註冊Co-worker重新導向URL：

1. 在Co-worker中，開啟&#x200B;**[!UICONTROL 為您的組織設定Amazon Ads]**&#x200B;對話方塊，如[為您的組織設定聯結器](#configure-organization)中所述。 Select **[!UICONTROL 使用我自己的OAuth應用程式]**&#x200B;來顯示&#x200B;**[!UICONTROL 重新導向URL]**，然後複製完整的值。
1. 在[使用Amazon主控台登入](https://developer.amazon.com/loginwithamazon/console/site/lwa/overview.html)中，尋找您應用程式的安全性設定檔。 Select **[!UICONTROL 管理]** > **[!UICONTROL 網頁設定]**，然後選取&#x200B;**[!UICONTROL 編輯]**。
1. 在&#x200B;**[!UICONTROL 允許的傳回URL]**&#x200B;下新增完整的重新導向URL，然後儲存。 如果其他團隊共用應用程式，請先保留現有URL並取得應用程式擁有者的核准，然後再變更設定。
1. 請注意來自相同安全性設定檔的OAuth使用者端ID和使用者端密碼。 您會在[設定聯結器](#configure-organization)時輸入它們。

請一律從您設定環境中的Co-worker對話方塊複製重新導向URL。 請勿自行建立URL、在瀏覽器中使用Co-worker頁面的URL，或重複使用來自其他環境或MCP使用者端的重新導向URL。 如需詳細資訊，請參閱[!DNL Amazon]檔案中的[使用Amazon註冊](https://developer.amazon.com/docs/login-with-amazon/register-web.html)。

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL 重新導向URL]**&#x200B;只顯示路徑`/connectors/oauth/callback`，則您的環境尚未支援此聯結器的登入。 請勿登入部分路徑，或猜測主機名稱。 請聯絡您的 Adobe 代表。

### 授予Advertising帳戶存取權 {#grant-member-access}

[!DNL Amazon Ads]帳戶管理員邀請每位成員加入他們所需的Advertising帳戶：

1. 開啟[Amazon Ads主控台](https://advertising.amazon.com/)，然後選取&#x200B;**[!UICONTROL 變更帳戶]**&#x200B;以選擇廣告商或管理員帳戶。
1. Select **[!UICONTROL 管理]** > **[!UICONTROL 帳戶存取與設定]** > **[!UICONTROL 使用者]** > **[!UICONTROL 邀請使用者]**。 確切的選項取決於帳戶型別。 邀請成員的[!DNL Amazon]帳戶，具有他們計畫執行之任務的最低許可權。
1. 對於經理帳戶，檢查存取權是否涵蓋整個經理帳戶或僅涵蓋選取的連結廣告商。 要求成員接受與其同事使用相同[!DNL Amazon]帳戶的邀請。
1. 確認成員可以在[!DNL Amazon Ads]中選取廣告商。 在核准的內部記錄中記下預期的帳戶名稱、地區和廣告商ID，以便您稍後在同事中確認存取權。

選擇支援您計畫之工作的最低許可權角色。 請勿僅授予管理員存取權以成功進行存取檢查。 [!DNL Amazon Marketing Cloud]執行個體的存取權與廣告商行銷活動的存取權不同。 如需詳細資訊，請參閱下列[!DNL Amazon Ads]檔案：

* [以管理員帳戶管理使用者](https://advertising.amazon.com/help/G4M4JGKGV2VAY9JC)
* [從您的帳戶新增或移除使用者](https://advertising.amazon.com/help/GDQVHVQMY9F88PCA)
* [瞭解帳戶許可權](https://advertising.amazon.com/help/GM4EFDQQPG9LGL3F)
* [Amazon Ads API許可權](https://advertising.amazon.com/API/docs/en-us/guides/account-management/permissions)

## 為您的組織設定聯結器 {#configure-organization}

管理員可讓組織中的所有人使用[!DNL Amazon Ads]聯結器。 組織頁面上的變更會套用至組織中的所有使用者。 成員無法從&#x200B;**[!UICONTROL 使用者]**&#x200B;範圍設定組織連線。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 組織]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。 在&#x200B;**[!UICONTROL Amazon Ads]**&#x200B;卡片上，選取&#x200B;**[!UICONTROL 設定]**。

   **[!UICONTROL 為您的組織設定Amazon Ads]**&#x200B;對話方塊開啟，其中包含&#x200B;**[!UICONTROL 連線詳細資料]**、**[!UICONTROL 使用者可用的工具]**&#x200B;以及&#x200B;**[!UICONTROL 存取和許可權]**&#x200B;區段。 儲存組態之後，卡片會顯示&#x200B;**[!UICONTROL 已儲存的組態]**，以及&#x200B;**[!UICONTROL 設定]**&#x200B;對&#x200B;**[!UICONTROL 檢視組態]**&#x200B;的變更。

1. 在&#x200B;**[!UICONTROL Amazon Ads地區]**&#x200B;下，選取符合廣告帳戶的地區。 Co-worker會在選取範圍下方的區域顯示MCP伺服器URL。

   | 區域 | MCP伺服器URL |
   | --- | --- |
   | [!UICONTROL 北美] （預設） | `https://advertising-ai.amazon.com/mcp` |
   | [!UICONTROL 歐洲] | `https://advertising-ai-eu.amazon.com/mcp` |
   | [!UICONTROL 遠東] | `https://advertising-ai-fe.amazon.com/mcp` |

   引導式設定會儲存一個區域。 若要稍後切換區域，請移除連線並重新設定。 然後每個成員都需要再次登入，因此在中斷工作連線之前請規劃變更。

1. Select和&#x200B;**[!UICONTROL OAuth應用程式]**：

   * **[!UICONTROL Adobe管理的OAuth應用程式]：** Adobe提供[!DNL Amazon Ads]應用程式，因此您不需要輸入應用程式認證。 每個成員都使用自己的[!DNL Amazon]帳戶登入並授權Adobe應用程式。

     ![使用北美地區、選取的Amazon管理的OAuth應用程式，以及收合的工具群組，為您的組織對話方塊設定Adobe Ads。](./assets/amazon-ads/org-configure.png){width="500" zoomable="yes"}

   * **[!UICONTROL 使用我自己的OAuth應用程式]：**&#x200B;每個成員都使用自己的[!DNL Amazon]帳戶授權您的組織應用程式。 在&#x200B;**[!UICONTROL 您的Amazon應用程式]**&#x200B;下，完成下列步驟：

     1. 請確定已在您的應用程式中登入&#x200B;**[!UICONTROL 重新導向URL]**。 如需詳細資訊，請參閱[註冊重新導向URL](#register-redirect-url)。
     1. 輸入&#x200B;**[!UICONTROL Amazon應用程式ID]**&#x200B;和&#x200B;**[!UICONTROL Amazon應用程式密碼]**。 **[!UICONTROL Amazon應用程式ID]**&#x200B;欄位採用OAuth使用者端ID，而非廣告商ID、管理員帳戶ID或[!DNL Amazon]應用程式ID。 同事會將您輸入的值儲存為組織機密。
     1. 若要改用已儲存的認證，請選取&#x200B;**[!UICONTROL 使用現有的密碼]**。 然後選取儲存應用程式識別碼&#x200B;**的**&#x200B;[!UICONTROL &#x200B;密碼以及儲存應用程式密碼&#x200B;]&#x200B;**的**&#x200B;密碼。 如果您的組織還沒有秘密，請在&#x200B;**[!UICONTROL 設定]** > **[!UICONTROL 秘密]**&#x200B;中新增這些秘密。

     需要兩個認證。 只在安全欄位中輸入認證值。 請勿在純值欄位中輸入機密參考。

1. 在&#x200B;**[!UICONTROL 使用者可用的工具]**&#x200B;下，展開每個工具群組並選取貴組織所需的工具。 依預設，僅選取`ads_accounts-list_ads_accounts`和`ads_accounts-get_ads_account`工具。 若要一次變更所有工具，請使用&#x200B;**[!UICONTROL Select全部]**&#x200B;或&#x200B;**[!UICONTROL 清除全部]**。 您必須至少選取一個工具。

   開始使用兩個帳戶工具進行第一次存取檢查。 Select行銷活動和報告工具只會在貴組織需要並核准它們時才提供。 如需詳細資訊，請參閱[工具群組](#tool-groups)。

1. Select **[!UICONTROL 儲存連線]**，然後檢閱儲存的&#x200B;**[!UICONTROL amazon-ads]**&#x200B;聯結器詳細資料。

   | 設定 | 說明 |
   | --- | --- |
   | **[!UICONTROL Source]** | 您所選取地區的MCP伺服器URL。 |
   | **[!UICONTROL 驗證]** | 驗證方法，`amazon-ads_login`。 |
   | **[!UICONTROL 工具逾時]** | Co-worker等待工具回應的時間。 |
   | **[!UICONTROL Connection]** | 使用中的OAuth應用程式以及您自己的登入狀態。 |
   | **[!UICONTROL 工具]** | 為成員選取的工具，具有&#x200B;**[!UICONTROL Select all]**&#x200B;和&#x200B;**[!UICONTROL Clear]**&#x200B;控制項以及選取的工具計數。 |

   ![已儲存的amazon-ads聯結器詳細資訊，其中顯示北美地區來源、驗證方法、具有「登出」和「重新整理」按鈕的「已登入」連線，以及選取的47種工具中的兩種。](./assets/amazon-ads/org-details.png){width="700" zoomable="yes"}

儲存不會將您或任何成員登入[!DNL Amazon]。 聯結器詳細資料上的&#x200B;**[!UICONTROL 連線]**&#x200B;狀態是指您自己的連線，而不是組織的連線。 若要檢查連線，請在聯結器詳細資訊頁面上選取&#x200B;**[!UICONTROL 登入]**，以使用您自己的[!DNL Amazon]帳戶登入，然後選取&#x200B;**[!UICONTROL 測試]**。 結果顯示&#x200B;**[!UICONTROL 連線成功]**&#x200B;或&#x200B;**[!UICONTROL 連線失敗]**，並傳回工具或錯誤。 成功的結果不會確認存取特定廣告商操作。

若要變更日後成員可用的工具，請使用&#x200B;**[!UICONTROL Select all]**&#x200B;或&#x200B;**[!UICONTROL Clear]**，更新&#x200B;**[!UICONTROL 可用工具]**&#x200B;下的選取專案，然後選取&#x200B;**[!UICONTROL 儲存工具選取專案]**。 至少必須保持選取一個工具。 成員無法變更工具選擇。

若要停止提供聯結器給您的組織，請在聯結器詳細資訊頁面上選取&#x200B;**[!UICONTROL 移除]**。

### 工具群組 {#tool-groups}

[!DNL Amazon Ads]聯結器將其工具組織成下列群組：

| 工具群組 | 工具 | 工具的作用 |
| --- | --- | --- |
| [!UICONTROL 行銷活動管理和目標定位] | 7 | 查詢行銷活動、廣告群組、廣告、目標、產品組合及其關聯，以及檢查產品資格。 |
| [!UICONTROL 帳戶和組織] | 6 | 列出並取得廣告帳戶，以及查詢廣告商和帳戶連結、經理帳戶和測試帳戶。 |
| [!UICONTROL 使用者存取和安全性] | 5 | 列出使用者、角色、許可權和邀請，然後取得邀請。 |
| [!UICONTROL 報告與分析] | 1 | 擷取報表。 不包含報告建立。 |
| [!UICONTROL Amazon Marketing Cloud] | 6 | 讀取工作流程和資料來源，以及現有執行的狀態和下載URL。 不包含工作流程執行。 |
| [!UICONTROL 帳單與財務摘要] | 4 | 讀取商業發票、商業發票摘要、帳單設定檔使用方式及帳單通知。 |
| [!UICONTROL Amazon Live] | 12 | 讀取頻道、廣播、直播串流、媒體、輪播和促銷程式碼資訊。 |
| [!UICONTROL 資格與優惠方案] | 6 | 閱讀方案和產品資格、促銷優惠和獎勵，以及條款代號資訊。 |

隨著[!DNL Amazon]更新聯結器，每個群組中的工具都可以變更。 引導式設定會儲存您選取的精確工具清單，即使您選取每個工具亦然。 您未選取的工具，以及伺服器稍後新增的工具，在您選取它們之前，將無法供成員使用。

>[!IMPORTANT]
>
>設定工具清單是專為讀取資料而編排的，但聯結器整體並非唯讀。 成員授權`advertising::campaign_management`範圍，其範圍比設定清單更廣。 當您測試連線時，工具清單還可以包含伺服器傳回的工具。 請先檢閱每個工具定義以及成員的[!DNL Amazon Ads]許可權，然後再選取更多工具。

## 以成員身分登入 {#sign-in-as-a-member}

管理員設定聯結器後，每個成員都會使用自己的[!DNL Amazon]帳戶登入。 您不需要應用程式密碼或存取權杖即可登入。

>[!NOTE]
>
>如果聯結器指出您的環境中尚未提供登入和&#x200B;**[!UICONTROL 測試]**，請在此停止。 僅組織設定無法讓成員登入可用。 請聯絡您的 Adobe 代表。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 使用者]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。 尋找&#x200B;**[!UICONTROL Amazon Ads]**&#x200B;卡片。

1. 如果卡片顯示&#x200B;**[!UICONTROL 未設定]**，請要求您的管理員[設定聯結器](#configure-organization)。 成員無法設定聯結器。

1. 當卡片顯示&#x200B;**[!UICONTROL 未登入]**&#x200B;時，請選取&#x200B;**[!UICONTROL 登入]**。 允許登入快顯視窗，然後使用可存取您的Advertising帳戶的[!DNL Amazon]帳戶登入。

1. 完成[!DNL Amazon]驗證提示，例如多重驗證(MFA)和同意提示。 核准之前，請先檢閱應用程式名稱和要求的存取權。

   透過Adobe管理應用程式，您可以授權Adobe應用程式。 透過您自己的組織應用程式，您可以改為授權該應用程式。

   >[!IMPORTANT]
   >
   >只有在您識別應用程式且您的組織核准所要求的存取權時，才繼續。

1. 返回同事並確認卡片顯示&#x200B;**[!UICONTROL 已登入]**。 Select **[!UICONTROL 檢視詳細資料]**，然後檢閱由您的管理員啟用的&#x200B;**[!UICONTROL 工具]**。 成員可以檢視工具，但無法變更它們或移除組織連線。

1. Select **[!UICONTROL 測試]**&#x200B;以檢查工具探索和連線狀態。

僅已關閉的快顯視窗無法確認登入成功。 成功的測試不會確認存取每個廣告商、行銷活動、報告或[!DNL Amazon Marketing Cloud]執行個體。 管理員登入時，其他成員未登入。

若要中斷您的[!DNL Amazon]帳戶與聯結器的連線，請選取&#x200B;**[!UICONTROL 登出]**。

## 檢查您的廣告帳戶存取權 {#check-account-access}

若要確認您可以使用哪些廣告帳戶，請執行唯讀檢查。 使用已核准的測試帳戶，並確定您的管理員已啟用`ads_accounts-list_ads_accounts`和`ads_accounts-get_ads_account`工具。 然後開始聊天並輸入提示。

範例提示：

* 「使用Amazon Ads，列出最多五個我可以在設定地區存取的廣告帳戶。 如果傳回帳戶名稱、帳戶ID和區域，則僅顯示這些欄位。 請勿建立、更新、刪除、啟動、執行工作流程、產生報表或變更許可權。 如果不支援清單限制，則僅彙總五個結果，並且不請求其他頁面。」

確認結果包含您預期的帳戶。 若要檢視更多詳細資料，請要求同事使用結果中的帳戶ID取得該帳戶的詳細資料。 請勿猜測帳戶ID，也不要要求促銷活動僅測試登入。

空的帳戶清單並不一定表示聯結器無法運作。 檢查您用來登入的[!DNL Amazon]帳戶、您接受的邀請、經理帳戶涵蓋的連結廣告商，以及設定的區域。 沒有行銷活動的測試帳戶也可以傳回空白行銷活動清單。 如果您需要的工具未啟用，請洽詢管理員。 請勿使用變更資料的工具來取代資料。

## 疑難排解存取權 {#troubleshoot-access}

如果您無法存取您的[!DNL Amazon Ads]資料，請向管理員檢查下列專案：

| 問題 | 檢查內容 |
| --- | --- |
| 缺少&#x200B;**[!UICONTROL Amazon Ads]**&#x200B;卡或&#x200B;**[!UICONTROL 設定]** | 確認聯結器可供您的組織使用，且您具有管理組織聯結器的許可權。 成員必須等待組織設定。 |
| Adobe管理的設定會儲存，但登入失敗 | 請聯絡您的Adobe代表，確認您的環境中可以使用Adobe管理的應用程式。 成功儲存無法確認這一點。 |
| 重新導向URL不相符 | 比較來自Co-worker對話方塊的完整&#x200B;**[!UICONTROL 重新導向URL]**&#x200B;與[!DNL Login with Amazon]中的&#x200B;**[!UICONTROL 允許的傳回URL]**，包括配置、主機和路徑。 請勿使用來自其他MCP使用者端、地區或環境的重新導向URL，或瀏覽器中Co-worker頁面的URL。 |
| **[!UICONTROL 重新導向URL]**&#x200B;僅顯示`/connectors/oauth/callback` | 您的環境尚未顯示完整的重新導向URL，或支援登入和&#x200B;**[!UICONTROL 測試]**。 請勿登入部分路徑，或猜測主機名稱。 請聯絡您的 Adobe 代表。 |
| 您無法儲存自己的OAuth應用程式設定 | 輸入OAuth使用者端ID和使用者端密碼，並至少選取一個工具。 確定&#x200B;**[!UICONTROL Amazon應用程式ID]**&#x200B;是OAuth使用者端ID，而非廣告商ID或[!DNL Amazon]應用程式ID。 |
| 同意或應用程式授權失敗 | 檢查[!DNL Amazon Ads] API核准、安全性設定檔、使用者端ID和密碼配對、重新導向URL註冊，以及同意畫面上顯示的應用程式。 當您要求協助時，請勿共用同意URL、授權碼或權杖。 |
| 您已登入，但帳戶或工具遭到拒絕或空白 | 檢查您用來登入的[!DNL Amazon]帳戶、您接受的邀請、管理員帳戶涵蓋的連結廣告商、設定的區域，以及工作所需的許可權。 存取應用程式或合作夥伴工具無法確認廣告商存取權。 [!DNL Amazon Marketing Cloud]存取權是獨立的。 |
| [!DNL Amazon Ads]指出目前的帳戶無法存取頁面 | Select **[!UICONTROL 變更帳戶]**&#x200B;並選擇廣告商或經理帳戶。 如果帳戶遺失，請要求其管理員檢查您是否接受邀請，以及您是否被指派該帳戶。 如果帳戶存在但使用者管理無法使用，請要求管理員檢查您的角色。 |
| 工具遺失或無法使用 | 檢查您組織的工具選擇、伺服器傳回的工具，以及您的[!DNL Amazon Ads]許可權。 伺服器稍後新增的工具不會自動選取。 依預設，僅啟用兩個帳戶工具。 |
| **[!UICONTROL 測試]**&#x200B;報告同名的個人聯結器 | 具有相同名稱的個人聯結器可優先於組織聯結器。 遵循所顯示的指引，在取得衝突個人聯結器擁有者的核准後，僅移除或重新命名衝突個人聯結器。 |
| 登入快顯視窗遭到封鎖、未完成或狀態未更新 | 允許快顯視窗，然後返回「同事」以檢查狀態和任何錯誤詳細資料。 請勿假設成功，因為快顯視窗已關閉或顯示登陸頁面。 |
| 工具逾時，或您必須重複登入 | 檢查60秒&#x200B;**[!UICONTROL 工具逾時]**、錯誤詳細資料、網路和[!DNL Amazon]可用性，以及應用程式設定。 |
| 同事表示安裝程式未啟用，或仍在設定新的密碼 | 請洽詢您的Adobe代表以檢查狀態。 不要重複建立認證，也不要將失敗的儲存視為成功。 |

聯絡支援時，請僅包含錯誤文字、錯誤時間、您的環境、所選區域和OAuth應用程式選項。 請勿共用應用程式機密、存取權杖、授權代碼、授權標頭、同意或重新導向查詢引數，或客戶帳戶資料。
