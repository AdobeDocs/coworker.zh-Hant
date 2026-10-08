---
title: Adobe CX Coworker閘道概觀
description: Adobe CX Coworker閘道是適用於Adobe CX Enterprise的統一MCP，為MCP使用者端提供單一連線到支援的產品工具。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 3%
---
# Adobe CX Coworker閘道 {#mcp-overview}

Adobe CX Coworker閘道是適用於Adobe CX Enterprise的統一模型內容通訊協定(MCP)。 只要連線一次，MCP相容的使用者端就能存取貴組織和帳戶有權使用的Adobe產品工具。

>[!IMPORTANT]
>
>您必須先啟用您的Adobe組織，才能使用&#x200B;**CX Coworker閘道**&#x200B;工具。
>
>如果貴組織尚未取得存取權，請傳送電子郵件給[cx-coworker-gateway-support@adobe.com](mailto:cx-coworker-gateway-support@adobe.com)，要求啟用貴組織。

對所有MCP使用者端設定使用CX Coworker閘道端點：

```
https://cx-coworker-gateway.adobe.io/mcp
```

連線之後，端點會公開您的Adobe組織和憑證可用的工具。 本指南中的產品特定頁面說明每個產品工具的功能、可存取的資料以及任何產品特定限制。

## 什麼是模型內容通訊協定？ {#mcp-what-is}

MCP (Model Context Protocol)是一種開放原始碼標準，用於將AI應用程式連線到外部系統。 與MCP相容的使用者端（例如[!DNL Claude]、[!DNL ChatGPT]、[!DNL Cursor]、[!DNL Claude Code]、[!DNL Codex]和[!DNL VS Code]）可以使用這些工具來擷取產品內容、執行支援的作業，並以自然語言傳回答案。

CX Coworker Gateway為CX Coworker Gateway產品工具提供受控端點。 與其新增個別的產品伺服器，只需連線至端點並使用為您的授權解決方案浮現的產品工具。

## 可用的產品工具 {#available-product-tools}

本指南記錄下列產品工具：


| 產品工具 | 透過端點公開的內容 | 可用性 | 文件 |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Real-Time CDP** | 受眾、目的地、來源、身分名稱空間和啟用健康狀態（唯讀） | Beta | [Real-Time CDP工具](rtcdp-mcp.md) |
| **Experience Platform** | 結構描述、資料集、資料治理、查詢服務、稽核事件、可觀察性量度和沙箱健康狀態檢查評估（唯讀） | Beta | [Experience Platform工具](aep-mcp.md) |
| **Journey Optimizer** | 行銷活動、歷程和管道設定（唯讀）；內容範本、片段、登陸頁面和內嵌訊息內容（讀取和寫入） | Beta | [Journey Optimizer工具](ajo-mcp.md) |
| **Customer Journey Analytics** | 資料檢視、維度、量度、報表、區段、日期範圍、專案和對象（讀取和寫入） | 可用 | [Customer Journey Analytics工具](cja-mcp.md) |
| **Adobe Analytics** | 報表套裝、維度、量度、報表、區段、日期範圍和Workspace專案（可讀取和寫入支援的元件） | 可用 | [Adobe Analytics工具](analytics-mcp.md) |
| **Workfront** | 專案、任務和核准工作流程的工作管理工具 | 預覽 | [Workfront MCP伺服器](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) |


>[!NOTE]
>
>工具可用性取決於您的產品授權、組織啟用、產品許可權以及用於驗證的Adobe憑證。 MCP只會顯示您的組織和使用者帳戶有權存取的工具。 請參閱[存取CX Coworker閘道工具](access.md)。



## 開始使用 {#mcp-get-started}

1. 檢閱[存取CX Coworker閘道工具](access.md)，以確認產品可用性、啟用和許可權。
2. 依照[安裝適用於CX Coworker閘道的Adobe](install.md)將您的MCP使用者端連線到端點。
3. 檢閱您計畫使用的每個產品工具的產品頁面。

