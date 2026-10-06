---
description: 瞭解同事行銷活動提示最佳實務 — CO-STAR框架、有無、不支援的內容，以及提示的品質檢查清單。
title: 提示最佳做法
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: ee66c1cc95ef1dd8c5e45c1fcb699547e63b9c8a
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 1%
---
# 提示最佳實務 {#best-practices}

充分運用同事行銷活動始於您的提示方式。 瞭解產生最佳結果的實務：用於建構提示的CO-STAR框架、要包含哪些內容和要避免什麼，以及情景型範例，這些範例為AI提供產生相關、準確定位內容所需的上下文。

>[!NOTE]
>
>目前，您只能連線至同事行銷活動支援的整合。 如果您有任何現有的Adobe Enterprise應用程式（可儲存對象或建立歷程），我們建議您改用[CX Enterprise Coworker](/help/chat/use-cases/overview.md)。

## 使用CO-STAR架構

為了獲得最佳結果，請使用CO-STAR框架組織您的提示。 這種結構化方法可確保AI完全瞭解您所需的內容。

| 元件 | 其含義 | 為何這很重要 |
|-|-|-|
| **C — 內容** | 有關您的行銷活動、產品或情況的背景 | 協助AI瞭解整體情況 |
| **O — 目標** | 您的特定行銷目標 | 推動內容應達到的目標 |
| **— 樣式** | 您想要如何溝通 | 設定方法 |
| **T — 音調** | 情感風格和聲音 | 塑造您訊息的感受 |
| **A — 對象** | 您正在定位的對象 | 確保訊息可與適當的人產生共鳴 |
| **R — 需求** | 特定限制或必備條件 | 定義邊界和關鍵元素 |

## AI提示要點

### 做和不做

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>執行</th>
<th>不要</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>使用CO-STAR架構進行結構</p>
<p>使用特定摘取指引的焦點行銷簡報</p>
<p>草擬您的提示以產生所需的意圖</p>
</td>
<td>
<p>在提示中要求結構變更、樣式或影像編輯</p>
<p>使用模糊的指示，例如「推廣我們的產品」</p>
<p>透過提示預期版面修改</p>
</td>
</tr>
</tbody>
</table>

### 提示中支援的內容

使用&#x200B;**電子郵件編輯器**&#x200B;或&#x200B;**Adobe Express**&#x200B;進行視覺/影像修改。 支援的請求型別如下。

- **指定行銷活動的頻率和步調**： 「建立每週傳送的電子郵件行銷活動……」

- **從較大型的清單鎖定特定對象**：「僅針對在&#39;all-attendees.csv&#39;公園中進行&#x200B;_Bark_&#x200B;活動的有狗的與會者建立行銷活動」

- **上傳HTML檔案**：「使用我附加的HTML檔案作為建立電子郵件行銷活動的基礎。」

- **在交談期間進行變更**：「將此行銷活動結束前的天數從兩天變更為三天。」

### 提示中不支援的內容

這些要求&#x200B;**不支援**，應該透過其他工具處理：

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✗電子郵件結構修改</th>
<th>✗立視覺化樣式變更</th>
<th>編✗器內作業</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>選取要變更的特定區段</li>
<li>刪除或複製元素</li>
<li>條件式選取專案</li>
<li>新增或移除配置區段</li>
</ul>
</td>
<td>
<ul>
<li>自訂字型</li>
<li>色彩修改</li>
<li>版面樣式（框線、邊框間距、邊界）</li>
<li>視覺效果（陰影）</li>
</ul>
</td>
<td>
<ul>
<li>背景變更</li>
<li>新增文字覆蓋圖或標誌</li>
<li>影像裁切或調整大小</li>
<li>色彩調整</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 品質檢查清單

在產生內容之前，請先確定下列事項：

✓ **清除目標**：清楚說明動作、產品/服務、值和內容。

✓ **已定義的目標對象**：指定人口統計、角色或區段。

✓ **指派正確的品牌為預設值**：已選取適當的品牌准則。

✓ **真實範圍**：避免請求配置變更、樣式或結構編輯。

## 以案例為基礎的提示範例

一律提供內容和價值主張，讓AI可產生相關內容。

>[!NOTE]
>
>雖然您目前只能產生和啟動電子郵件行銷活動，您可以隨時要求同事產生社群媒體、WhatsApp或簡訊的副本。

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>行業</th>
<th>範例提示</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B技術</strong></td>
<td>「產生四點式電子郵件行銷活動，展示ROI和技術規格，同時解決IT決策者評估雲端基礎架構解決方案時的安全性問題，強調99.9%的運作時間、SLA與SOC 2法規遵循，以及40%的成本節省。」</td>
</tr>
<tr>
<td><strong>電子商務零售</strong></td>
<td>「透過單次接觸式行銷活動，緊急處理限量供應的節日商品，同時強調免運費和方便最後一刻購物者的退貨，並著重於限量商品（剩餘50件以下）和24小時停運規定。」</td>
</tr>
<tr>
<td><strong>教育與訓練</strong></td>
<td>「建立兩點式行銷活動，著重於職業晉升成果和業界認證，同時展示講師的專業知識、92%的職位安排率及專案型課程。」</td>
</tr>
<tr>
<td><strong>諮詢</strong></td>
<td>「透過展示三個具有詳細ROI標準的客戶成功案例（IBM：成本降低45%、Accenture：銷售機會增加200%、Microsoft：節省時間60%），打造三點式行銷活動，以擁有1000多名員工的公司的IT主管為目標，培育企業潛在客戶。」</td>
</tr>
</tbody>
</table>

## 一般行銷提示概念

### 內容行銷

- 「產生20個部落格主題，回答首次購房者的常見問題。」
- 「LinkedIn集思廣益，為B2B網路安全初創公司張貼創意。」
- 「建立三個月的內容行事曆，著重於教育新客戶。」
- 「建議可重新用於部落格、影片、電子報和社交貼文的內容主題。」

### 電子郵件行銷

- 「為對可持續時尚感興趣的新訂閱者產生歡迎電子郵件序列。」
- 「腦力激盪主旨行，這些主旨行創造好奇心，聽起來卻不像點選誘餌。」
- 「建議不活躍客戶重新參與行銷活動的想法。」
- 「為已完成入門的使用者建立生命週期電子郵件構想。」

>[!MORELIKETHIS]
>
>瀏覽更多[同事行銷活動的提示模式](use-cases.md)。
