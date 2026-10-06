---
title: 在同事中建立及執行品質門技能
description: 瞭解如何使用自訂同事技能，在部署前根據隱藏清單、頻率上限和命名標準自動驗證對象啟用。
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 101
last-substantial-update: 2026-09-08
jira: KT-22379
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%
---

# 使用自訂AI技能建立和執行品質門技能

行銷團隊仰賴規則和治理程式，確保受眾可正確啟動。 將對象啟動到目的地之前，團隊通常需要驗證隱藏清單、頻率上限、同意要求和命名慣例。
 
難題在於這些檢查通常取決於部落知識和手動審查。 當程式在人腦中執行時，可能會發生錯誤。

在本影片中，您將會瞭解自訂同事技能如何作為啟動門，在對象向下游移動之前，根據組織的啟動標準自動驗證對象。

>[!VIDEO](https://video.tv.adobe.com/v/3503174/?captions=chi_hant&learn=on&enablevpops)

## 啟動品質閘道技能範例
 
您可以將提示貼到Co-worker中，以建立您自己的可重複使用的&#x200B;**啟動品質門**&#x200B;技能。 同事的技能撰寫功能會將提示轉換為在&#x200B;**您自己的環境**&#x200B;內儲存的技能。 以下是根據影片示範的範例。
 
關鍵是為三個治理閘道定義您自己的&#x200B;**通過/失敗標準**：
 
1. 隱藏/同意
2. 頻率上限
3. 命名慣例
 
每個人的架構都相同。 自訂標示&#x200B;**`[...]`**&#x200B;的區段以符合您組織的標準。

## 主提示

> **將此項儲存為名為「啟動品質閘道」的技能。**

```text
It's a governance gate that runs a pre-activation checklist before any audience is sent to a destination.

It is read-only. It never activates, mutates, or copies anything.

Resolve the named audience and destination from our Knowledge Graph, evaluate the three gates below, then render one visual scorecard containing:

- An Alert banner
- One MetricCard per gate
- A DataTable with:
- Gate
- Status
- Finding
- Required Fix

Provide a single verdict:

- CLEARED only if all three gates pass
- BLOCKED if any gate fails

For every failed gate, provide the specific remediation needed.
 
All gates fail closed:

- Missing data = BLOCKED
- Never assume success when information is unavailable
 
Trigger phrases:

- "run the activation gate"
- "is this audience ready to activate"
- "pre-activation checklist"
- "can I activate to ..."

The three gates are:
 
[Paste Gate 1, Gate 2, and Gate 3 definitions here]
```

## 入口1：隱藏/同意
 
> 編輯此區段以符合您組織的隱藏和同意要求。
 

```text
Gate 1 – Suppression List

Pass only if a recognized suppression, opt-out, or consent audience is applied alongside the target audience.

Discover eligible lists using name patterns such as:

- suppress
- opt-in
- opt out
- consent
- do not contact
 
Because suppression lists may live in destination dataflows rather than audience metadata, require the marketer to confirm one is attached.
 
If no suppression or consent list exists anywhere in the sandbox, fail hard.
 
Our standard:

[Example: A consent audience is mandatory for all email and SMS destinations. For direct mail destinations it is optional.]
```

## 閘道2：頻率上限

> 編輯此區段以符合您組織的傳送頻率要求。

```text
Gate 2 – Frequency Cap
 
Read the delivery frequency on the resolved destination.

Pass if:

- Frequency is present
- Frequency is bounded

Fail if:

- Frequency is blank
- Frequency is unbounded

Our standard:

[Example: Frequency must be DAILY or less frequent. Any hourly cadence or blank value is blocked.]
```

## 閘門3：命名慣例
 
> 編輯此區段以符合您組織的對象命名規則。
 

```text
Gate 3 – Naming Convention

Evaluate the audience name programmatically.

Any rule violation causes failure.

Block names that:

- Contain "test"
- Contain "copy"
- Contain an auto-copy suffix such as _[6-hex]
- Contain timestamps
- Contain 24-character object IDs
- Start with a bare number or cryptic short code
- Are entirely lowercase
- Are excessively short or unclear
- Use generic defaults such as:
- Save audience
- Email
- New Accounts
- Lack a category–qualifier separator

Our standard:

[Example: [Line of Business] – [Criteria] in title case]

Example:

Mortgage – High Propensity Prospects

When blocked on naming, always propose a compliant replacement name.
```

## 指南

### &#x200B;1. 僅自訂括弧內的區段

僅更新&#x200B;**`[...]`**&#x200B;中包含的區段。
 
這些區段會定義組織的特定治理標準。
 
其他所有專案應維持不變：

- 對象解析度
- 閘道評估
- 計分卡轉譯
- 判決邏輯


### &#x200B;2. 驗證先決條件
 
此技能取決於：
 
- 知識圖存取
- 客群探索
- 目的地探索
- 隱藏清單探索
- 視覺成品支援
- 警示橫幅
- 量度卡
- DataTable轉譯

如果客戶的環境中沒有這些功能，技能就無法如期執行。

### &#x200B;3. 將技能設為唯讀

此技能應一律保持唯讀。

在提示中明確包含此要求，以確保技能永遠不會與啟動工作流程混淆。

Activation Quality Gate只會評估啟動整備程度。 它&#x200B;**不會**&#x200B;啟用對象、修改設定或複製資料。
