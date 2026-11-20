---
title: Jira / Atlassian Rovo外部聯結器
description: 瞭解如何在CX Enterprise Coworker中設定Jira / Atlassian Rovo外部聯結器，並使用Atlassian登入以讀取和搜尋Jira工作專案。
role: Admin, User
level: Beginner
badgeBeta: label="Beta" type="Informative" tooltip="此聯結器為Beta版。"
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
hide: true
source-git-commit: 92e7715a5eb7ab4f8feb7348384c94fabc1b78cf
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%
---

# Jira / Atlassian Rovo外部聯結器 {#jira-atlassian-rovo}

使用[!DNL Jira] / [!DNL Atlassian Rovo]外部聯結器讀取和搜尋Adobe CX Enterprise Coworker中的[!DNL Jira]個工作專案。 設定聯結器後，請要求同事尋找工作專案、閱讀其詳細資訊，並使用Jira查詢語言(JQL)進行搜尋。 聯結器是由[!DNL Atlassian]裝載的模型內容通訊協定(MCP)伺服器。

>[!AVAILABILITY]
>
>[!DNL Jira] / [!DNL Atlassian Rovo]外部聯結器為Beta版。 文件和功能可能會有所變更。

## 聯結器設定 {#connector-configuration}

聯結器組態程式有三個獨立的部分：

* **[!DNL Atlassian]準備：** [!DNL Atlassian]組織管理員允許Co-worker重新導向URL網域並檢閱MCP存取原則。
* **組織設定：**&#x200B;同事管理員會為整個組織設定一次聯結器。 管理員選擇成員可以使用的唯讀工具。
* **成員登入：**&#x200B;每個成員都使用自己的[!DNL Atlassian]帳戶登入。 成員只能存取其帳戶有權檢視的[!DNL Jira]資料。

儲存組織組態不會登入任何成員或授予[!DNL Jira]許可權。 每個成員必須個別登入。

聯結器沒有共用服務帳戶或API權杖選項。 Co-worker會自動向[!DNL Atlassian]註冊OAuth應用程式，因此您不會輸入使用者端ID或使用者端密碼。

雖然聯結器名稱包含[!DNL Atlassian Rovo]，但聯結器僅要求[!DNL Jira]讀取及搜尋存取權。 它不會要求[!DNL Confluence]、[!DNL Rovo]特定、寫入或破壞性存取。 其他[!DNL Atlassian] MCP功能不一定可透過此聯結器使用。

## 先決條件 {#prerequisites}

開始之前，請確定您具備下列條件：

* **對於組織設定：**&#x200B;在有[!DNL Jira] / [!DNL Atlassian Rovo]聯結器可用的組織中，具有許可權可管理同事中組織聯結器的帳戶。
* **針對[!DNL Atlassian]準備：**&#x200B;可以核准MCP存取和同事重新導向URL網域的[!DNL Atlassian]組織管理員。
* **對於成員登入：** [!DNL Atlassian]帳戶，可存取預期的[!DNL Jira]網站、專案和工作專案。
* **對於網路存取：** [!DNL Atlassian]允許連線的IP允許清單和應用程式原則。 登入成功並不會確認是否允許工具請求。
* **[!DNL Rovo]已啟用：** [!DNL Rovo]已在成員使用聯結器之前，為您的[!DNL Atlassian]組織和預期的[!DNL Jira]網站啟用。 如需詳細資訊，請參閱[!DNL Atlassian]檔案中的[如何啟用Rovo](https://www.atlassian.com/software/rovo/guides/admin-guide/rovo-activation)。

## 準備[!DNL Atlassian]存取權 {#prepare-atlassian}

在成員登入之前，[!DNL Atlassian]組織管理員已在[!DNL Atlassian Administration]中準備存取權：

1. 開啟[!DNL Atlassian Administration]，然後選取所要的組織。

1. Select **[!UICONTROL 聯結器]** > **[!UICONTROL Atlassian MCP伺服器]** > **[!UICONTROL 新增網域]**。

1. 新增Co-worker設定對話方塊中顯示的&#x200B;**[!UICONTROL 重新導向URL]**&#x200B;的網域。 對於對話方塊，請參閱[設定組織的聯結器](#configure-organization)。

   請遵循[!DNL Atlassian]網域格式規則，而非貼上完整的URL。 如需詳細資訊，請參閱[!DNL Atlassian]檔案中的[可用的Atlassian MCP伺服器網域](https://support.atlassian.com/security-and-access-policies/docs/available-atlassian-mcp-server-domains/)。

1. 與[!DNL Atlassian]管理員一起檢閱MCP許可權群組、應用程式原則和IP允許清單。 如需詳細資訊，請參閱下列[!DNL Atlassian]檔案：

   * [支援的Atlassian MCP工具](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)，適用於每個工具所需的許可權群組與範圍
   * [控制Atlassian MCP伺服器設定](https://support.atlassian.com/security-and-access-policies/docs/control-atlassian-mcp-server-settings/)，用於驗證和IP允許清單

請一律使用您設定之環境的「同事」對話方塊中所顯示的重新導向URL。 請勿從其他環境複製重新導向URL。

## 為您的組織設定聯結器 {#configure-organization}

管理員可讓組織中的所有人使用[!DNL Jira] / [!DNL Atlassian Rovo]聯結器。 組織頁面上的變更會套用至組織中的所有使用者。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 組織]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。 在&#x200B;**[!UICONTROL Jira / Atlassian Rovo]**&#x200B;卡上，選取&#x200B;**[!UICONTROL 設定]**。 成員無法設定或移除此連線。

1. 在&#x200B;**[!UICONTROL 連線Jira / Atlassian Rovo]**&#x200B;對話方塊中，檢閱固定的&#x200B;**[!UICONTROL 伺服器URL]**，`https://mcp.atlassian.com/v2/mcp`。

   檢閱&#x200B;**[!UICONTROL 重新導向URL]**，並確定[!DNL Atlassian]系統管理員核准其網域，如[準備Atlassian存取](#prepare-atlassian)中所述。 您未輸入任何OAuth認證。

1. 在&#x200B;**[!UICONTROL 使用者可用的工具]**&#x200B;下，選擇成員可以使用的工具。 如需詳細資訊，請參閱[可用的工具](#available-tools)。

   `getAccessibleAtlassianResources`網站探索工具為必要項，且會保持啟用狀態。 其他五個工具為選用工具。 若要封鎖組織中每個人的選用工具，請移除該工具。 若要復原您移除的工具，請選取&#x200B;**[!UICONTROL 還原所有工具]**。 您可以只儲存啟用網站探索的組態，但成員無法讀取或搜尋工作專案。

   ![Connect Jira / Atlassian Rovo對話方塊，顯示伺服器URL、編輯的重新導向URL，以及使用者可用的六個工具，以及必要的getAccessibleAtlassianResources工具和五個選用工具。](./assets/jira-atlassian-rovo/org-configure.png){width="500" zoomable="yes"}

1. Select **[!UICONTROL 儲存連線]**，然後檢閱連線詳細資料。

   每個成員登入時，聯結器會要求下列OAuth範圍：

   | 範圍 | 目的 |
   | --- | --- |
   | `read:me`, `read:account` | 支援成員的[!DNL Atlassian]帳戶授權。 |
   | `read:jira:agent-interface` | 讀取[!DNL Jira]資料。 |
   | `search:jira:agent-interface` | 搜尋[!DNL Jira]資料。 |
   | `offline_access` | 重新整理登入權杖。 |

   工具逾時為60秒。 第一次連線和工具探索可能需要更長的時間。

### 可用的工具 {#available-tools}

[!DNL Jira] / [!DNL Atlassian Rovo]聯結器提供下列唯讀工具：

| 工具 | 說明 | 管理員控制 |
| --- | --- | --- |
| `getAccessibleAtlassianResources` | 尋找您可存取的[!DNL Atlassian]網站和雲端ID。 [!DNL Jira]工具需要此工具。 | 必要 |
| `atlassianUserInfo` | 取得登入使用者的帳戶資訊。 | 選填 |
| `getJiraIssue` | 依ID或金鑰取得[!DNL Jira]工作專案。 | 選填 |
| `searchJiraIssuesUsingJql` | 使用JQL搜尋[!DNL Jira]個工作專案。 | 選填 |
| `discover` | 尋找其他工具操作及其輸入結構描述。 | 選填 |
| `executeRead` | 執行透過`discover`找到的讀取作業，例如讀取註解、變更記錄檔、專案、展示板和衝刺。 | 選填 |

>[!IMPORTANT]
>
>`discover`和`executeRead`工具可讓成員以群組的形式存取其他允許的讀取作業。 您無法關閉個別作業。 如果您的組織不接受此存取權，請移除兩個工具。 聯結器不包含寫入作業(`executeWrite`)或破壞性作業(`executeDestructive`)。

移除選用工具會限制Co-worker的可用性。 這不會減少聯結器在登入時請求的OAuth範圍。

每個工具都需要特定的[!DNL Atlassian]許可權群組與範圍。 如需詳細資訊，請參閱[!DNL Atlassian]檔案中的[支援的Atlassian MCP工具](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)。

## 以成員身分登入 {#sign-in-as-a-member}

管理員設定聯結器後，每個成員都會使用自己的[!DNL Atlassian]帳戶登入。 您不需要使用者端ID、使用者端密碼或存取權杖即可登入。

1. 開啟&#x200B;**[!UICONTROL 自訂]**，選取&#x200B;**[!UICONTROL 使用者]**，然後選取&#x200B;**[!UICONTROL 外部聯結器]**。

1. 尋找&#x200B;**[!UICONTROL Jira / Atlassian Rovo]**&#x200B;卡。 如果卡片顯示&#x200B;**[!UICONTROL 未設定]**&#x200B;且&#x200B;**[!UICONTROL 尚無法使用。 您的管理員需要設定此專案。]**，請要求您的管理員[設定聯結器](#configure-organization)。 成員無法設定聯結器。

1. Select **[!UICONTROL 登入]**，並使用可存取預期[!DNL Jira]網站的[!DNL Atlassian]帳戶。 完成任何必要的單一登入(SSO)、多重驗證(MFA)和同意提示。 在您同意之前，請檢閱要求的讀取和搜尋存取權。

   >[!IMPORTANT]
   >
   >只有在您識別應用程式且您的組織核准所要求的存取權時，才繼續。

1. 返回Co-worker，並開啟聯結器詳細資料。 連線對成員而言是唯讀的，您可以檢視管理員啟用的工具。 Select **[!UICONTROL 測試連線]**&#x200B;以確認連線。

1. 選擇性地執行小型唯讀檢查，如[檢查您的Jira存取權](#check-access)中所述。

成功的測試並未確認您可以存取每個[!DNL Jira]網站、專案或工作專案。

## 檢查您的[!DNL Jira]存取權 {#check-access}

若要確認聯結器可以讀取您的資料，請開始聊天並輸入唯讀提示。

範例提示：

* 「搜尋Jira以取得指派給我的最多五個工作專案，並依照最近更新的順序進行。 包含其索引鍵和連結。 請勿修改任何專案。」

為了讓此提示生效，您的管理員必須啟用搜尋工具，且您的[!DNL Jira]帳戶必須擁有檢視工作專案的許可權。

## 疑難排解存取權 {#troubleshoot-access}

如果登入或存取失敗，請向您的管理員檢查下列專案：

| 問題 | 檢查內容 |
| --- | --- |
| 使用者端或網域的登入遭到封鎖 | 在&#x200B;**[!UICONTROL Atlassian MCP伺服器]**&#x200B;設定下，確認已在[!DNL Atlassian Administration]中核准您環境的重新導向URL網域。 |
| 同意成功，但工具呼叫遭拒 | 檢查您的[!DNL Jira]許可權、[!DNL Atlassian] MCP許可權群組、應用程式原則及IP允許清單。 如需每個工具所需的許可權群組，請參閱[支援的Atlassian MCP工具](https://support.atlassian.com/atlassian-ai-gateway/docs/supported-tools/)。 |
| JQL搜尋失敗，但其他讀取可以運作 | 確認您的管理員已啟用`searchJiraIssuesUsingJql`，且連線要求`search:jira:agent-interface`範圍。 |
| 同意傳回`invalid_request` | 請要求您的系統管理員確認連線要求`read:me`與`read:account`以及[!DNL Jira]範圍。 |
| 變更後，您仍可看到較舊的範圍 | 過時的使用者層級`jira_login`驗證提供者覆寫優先於組織連線。 要求管理員僅更新或移除過時的覆寫，然後重新登入。 |
| 缺少工具 | 請要求您的管理員檢查工具選擇。 其他讀取作業需要`discover`和`executeRead`、必要的範圍以及正確的許可權。 |
| **[!UICONTROL 測試連線]**&#x200B;緩慢或逾時 | 工具探索可能需要超過60秒工具逾時的時間。 在變更認證之前，請檢查問題是否為探索速度緩慢或登入失敗。 |

當您要求協助時，請勿共用密碼、權杖、授權代碼或同意URL。 請勿將其納入熒幕擷取畫面或支援票證。
