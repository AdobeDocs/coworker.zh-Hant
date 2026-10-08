---
title: CX Coworker Gateway中的Journey Optimizer工具
description: 瞭解可透過Adobe Journey Optimizer Gateway使用的CX Coworker工具。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 2%
---
# CX Coworker Gateway中的Adobe Journey Optimizer工具 {#ajo-mcp}

使用Adobe Journey Optimizer產品工具，從相容於MCP的使用者端檢查行銷活動、歷程和管道設定。 當您的組織已啟用，且您的使用者帳戶擁有必要的Journey Optimizer許可權時，即可透過[CX Coworker閘道](overview.md)使用這些工具。

如需詳細資訊，請參閱Adobe Journey Optimizer檔案中的[使用MCP使用者端](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/combine/ajo-mcp){target="_blank"}。

若要建立、分析和模擬歷程的對話式代理程式體驗，請改為參閱[Journey Agent](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/agents/ajo-agent)。

>[!AVAILABILITY]
>
>Journey Optimizer產品工具位於Beta中。 存取許可權僅限透過邀請，且需要Adobe組織啟用。 請參閱[存取CX Coworker閘道工具](access.md)。

## 主要功能 {#mcp-capabilities}

Journey Optimizer工具為行銷活動、歷程和管道設定檢閱提供唯讀介面。 您可以：

- 列出Journey Optimizer促銷活動並按狀態篩選。
- 擷取行銷活動詳細資料，包括目標定位、排程、頻道和內容設定中繼資料。
- 列出並檢查沙箱中的歷程，包括分支、條件和動作。
- 列出電子郵件、簡訊、推播和WhatsApp頻道的頻道設定。
- 列出可用於資料治理原則執行的行銷動作。
- 使用自然語言檢閱行銷活動、歷程和頻道設定，而不需導覽產品畫面。

>[!IMPORTANT]
>
>目前Beta中的所有Journey Optimizer工具均為唯讀。 不支援建立、更新、刪除、啟動、停止或發佈行銷活動或歷程。

## 可用的工具 {#mcp-tools}

| 工具 | 說明 |
| --- | --- |
| `ajo_campaign_list` | 瀏覽Journey Optimizer行銷活動。 支援依狀態篩選，例如`DRAFT`、`LIVE`、`STOPPED`和`COMPLETED`。 |
| `ajo_campaign_get` | 依ID擷取特定行銷活動的詳細資料和設定，包括對象鎖定目標、排程、頻道和內容設定中繼資料。 |
| `ajo_journey_list` | 瀏覽您Journey Optimizer沙箱中的所有歷程。 |
| `ajo_journey_get` | 依ID擷取特定歷程的完整詳細資料，包括其分支、條件和動作。 |
| 歷程視覺效果 | 呈現歷程的結構和流程，以進行互動式視覺探索。 |
| `ajo_channel_configuration_list`, `ajo_channel_configuration_get` | 檢視電子郵件、簡訊、推播或[!DNL WhatsApp]管道的表面預設集和品牌設定。 |
| `ajo_channel_configuration_resource_list`, `ajo_channel_configuration_resource_get` | 列出及擷取頻道設定所參考的支援設定資源，例如推播認證、電子郵件子網域、IP集區、SMS認證和[!DNL WhatsApp]認證。 |
| `ajo_marketing_action_list` | 列出資料治理原則強制的可用行銷動作。 |

## 提示範例 {#mcp-use-cases}

| 目標 | 範例提示 |
| --- | --- |
| Campaign 概觀 | 「顯示我的所有Journey Optimizer行銷活動。」 |
| 狀態稽核 | 「哪些行銷活動目前處於上線狀態？」 |
| 行銷活動詳細資料 | 「取得行銷活動`[campaign ID]`的完整詳細資料。」 |
| 歷程概觀 | 「顯示我的所有Journey Optimizer歷程。」 |
| 歷程詳細資料 | 「取得歷程`[journey ID]`的完整詳細資料，包括分支和條件。」 |
| 對象和鎖定 | 「行銷活動`[campaign ID]`鎖定了哪些對象？」 |
| 時程表和時間 | 「行銷活動`[campaign ID]`排定何時執行？」 |
| 疑難排解 | 「檢閱行銷活動`[campaign ID]`的設定，並標示可能的問題。」 |
| 管道設定 | 「有哪些電子郵件通道設定可用？」 |
| 管道稽核 | 「哪些管道設定遺漏或不完整？」 |
| 治理 | 「我的沙箱中有哪些行銷動作可用？」 |

## 內容管理工具 {#mcp-content-management}

除了上述唯讀產品工具之外，Journey Optimizer使用者還可以使用自然語言提示，直接從CX Coworker探索及管理內容資產（內容範本、片段、登陸頁面，以及歷程或行銷活動內嵌訊息內容）。 此功能由一組適用於Journey Optimizer內容的獨立可讀取和可寫入的MCP工具提供支援，可供有權存取CX Coworker的所有客戶使用。

如需詳細資訊，請參閱Adobe Journey Optimizer檔案中的[內容管理工具](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/ajo-coworker-skills#content-management){target="_blank"}。

內容管理工具可讓您：

- 瀏覽內容範本、片段和登入頁面，並擷取其結構、中繼資料和狀態。
- 擷取在歷程或行銷活動動作節點上設定的內嵌訊息內容。
- 建立和更新任何管道的內容範本。
- 建立、更新、複製和發佈片段。
- 取代歷程或行銷活動動作節點內嵌訊息上的頻道變體。

>[!IMPORTANT]
>
>與上述唯讀產品工具不同，內容管理工具支援寫入作業。 不支援跨範本或片段、範本或片段驗證、建立或發佈登入頁面，以及刪除內容範本、片段或登入頁面的全文檢索搜尋。

## 產品內容和許可權 {#mcp-context}

您的使用者帳戶必須有權檢視您查詢的Journey Optimizer行銷活動、歷程和管道設定。 MCP不會略過產品許可權。

如果您的組織使用多個沙箱，請在您需要特定沙箱的結果時，在提示中指定沙箱或環境內容。

## 已知限制 {#mcp-limitations}

| 限制 | 說明 | 因應措施 |
| --- | --- | --- |
| 唯讀表面 | Journey Optimizer工具只會公開擷取操作。 您無法建立、更新、刪除、開始、停止或發佈行銷活動或歷程。 | 使用Journey Optimizer UI或API進行寫入操作。 |
| 無參與或績效量度 | 工具不會傳回曝光數、點進率、轉換或傳遞統計資料等報表資料。 | 使用Journey Optimizer報表、Customer Journey Analytics工具或Adobe Analytics工具來瞭解績效量度。 |
| 行銷活動清單分頁受到限制 | 行銷活動清單會傳回結果的第一頁，最多達50個行銷活動會依字母順序排序。 未套用位移和限制值。 | 如果行銷活動ID已知，請直接使用`Get Campaign`。 使用Journey Optimizer UI進行完整的瀏覽和篩選。 |
| 無依據日期、頻道或排程的伺服器端篩選 | 行銷活動清單支援狀態篩選，但不支援發佈日期、排程日期、管道或行銷活動型別篩選。 | 使用Journey Optimizer UI行銷活動清單進行原生日期和管道篩選。 |
| 無法透過產品工具擷取訊息內容 | 訊息HTML、主旨列、個人化代號和選件內容無法透過上述唯讀產品工具取得。 | 使用[內容管理工具](#mcp-content-management)來擷取和更新內嵌訊息內容，或直接在Journey Optimizer UI中檢視內容。 |