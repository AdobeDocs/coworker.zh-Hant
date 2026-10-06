---
title: 使用Co-worker的資料驗證技能驗證Customer Journey Analytics資料
description: 瞭解如何使用Co-worker中的資料驗證技能驗證Customer Journey Analytics資料，並在建立儀表板之前解決問題。
feature: AI Tools
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 330
last-substantial-update: 2026-09-16
jira: KT-22622
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%
---
# 使用[!DNL Coworker]中的資料驗證技能驗證Customer Journey Analytics資料

資料品質是Adobe Customer Journey Analytics (CJA)中準確報告的基礎。 在建立量度、控制面板、區段或客戶歷程之前，瞭解底層Adobe Experience Platform (AEP)資料是否值得信任至關重要。

在本影片中，您將會瞭解如何使用Co-worker **中的**&#x200B;資料驗證技能，快速評估支援Customer Journey Analytics實作的資料集品質，而不需要撰寫查詢或手動檢查資料。

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## 探索CJA報告背後的資料集

瞭解同事如何識別：

- 哪些資料集已連線至Customer Journey Analytics
- 與特定沙箱關聯的連線和資料檢視
- 資料集正在積極支援報告
- 重要資料集特性，例如串流狀態和身分名稱空間

透過準確地瞭解哪些資料集為您的報表提供資料，您可以將驗證工作集中在最重要的地方。

## 探索資料集方案和可用欄位

瞭解如何直接從Adobe Experience Platform檢查資料集結構。

同事會擷取結構描述詳細資料和介面：

- Commerce和交易欄位
- 產品資訊
- 網路互動資料
- 身分識別欄位
- 行銷活動和行銷屬性
- 裝置和地理維度

這會提供可用於分析的欄位詳細目錄，並醒目顯示結構描述中存在的欄位與包含可用資料的欄位之間的差異。

## 驗證身分品質

身分資料對於Customer Journey Analytics而言至關重要，因為它支援個人層級報表和跨管道歷程分析。

在本影片中，您將會瞭解同事如何：

- 驗證身分欄位
- 檢查空值和資料完整性
- 評估識別碼品質
- 表面遺失或無法使用的身分屬性

範例驗證顯示範例中ECID和電子郵件身分已完整填入且有效，但無法擷取Analytics ID。 這在決定哪些識別碼可支援設定檔拼接和報表時，會提供有用的訊號。

## 分析個別欄位品質

欄位可能存在於資料集中，但仍不適合用於報表。

觀看同事如何驗證行銷活動追蹤欄位和報告：

- 母體比率
- Null百分比
- 資料一致性
- 無效值偵測

在此範例中，顯示的追蹤程式碼值是乾淨且一致的，但約85%的列是空值。 這顯示在欄位上建立CJA維度或行銷活動量度之前的主要報告盲點。

## 執行AI支援的資料集驗證

Co-worker可以評估整個資料集，而不是一次驗證一個欄位。

您將學習資料驗證技能：

- 選取要驗證的重要欄位
- 評估完整性和品質
- 比較各欄位的資料健康情況
- 強調優點與潛在報告風險

驗證結果可為CJA提供可行性圖。 網頁名稱和電子郵件代碼等清除欄位可能已準備好進行報告，而購買值、促銷活動名稱和追蹤代碼等稀疏欄位則需要調查。

## 識別收入和歸因風險

影片也會示範資料驗證如何找出影響報表正確性的問題，包括：

- 稀疏行銷活動資料
- 缺少歸因資訊
- 不完整的交易值
- 收入測量差距

在顯示的資料集中，雖然有採購計數，但無法可靠地填入訂單金額。 這是信任收入報告之前要調查的問題。

## 為何資料驗證對Customer Journey Analytics很重要

Customer Journey Analytics的可靠性取決於其背後的資料。

在建置報表之前驗證資料集有助於團隊：

- 增加分析結果的信賴度
- 改善資料控管實務
- 減少報告錯誤
- 儘早識別實作問題
- 更有效率地疑難排解非預期的量度

使用Co-worker，可以使用自然語言提示來啟動這些檢查，讓技術和非技術使用者更容易存取資料驗證。

