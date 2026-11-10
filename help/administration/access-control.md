---
title: 同事的存取控制
description: 瞭解Adobe CX Enterprise Coworker的存取控制功能以及相容Adobe產品的許可權。 尋找管理員控制項，並取得存取權的說明。
last-substantial-update: 2026-11-04
level: beginner
role: Admin
jira: KT-22980
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: a14bd350d7259294368acdcb08549ea6e084f1c1
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%
---
# 同事的存取控制 {#access-control}

使用Adobe CX Enterprise Coworker存取控制來管理誰可以使用同事，以及他們可以使用哪些功能。

>[!NOTE]
>
>您的組織必須啟用「同事」功能，才能使用此功能。 存取控制將逐步推出，並非所有同事組織都能在啟動時啟用。 如需詳細資訊，請參閱[同事聊天概述](https://experienceleague.adobe.com/en/docs/coworker/content/chat/overview)。

## 存取權的決定方式 {#how-access-is-determined}

同事存取許可權是由整個組織的設定所控制，且可選的使用者或群組覆寫。 組織範圍的設定可啟用或停用組織中使用者的「同事」存取權。 依預設會為每個人啟用存取權。

| 設定 | 如何影響存取 |
| --- | --- |
| 組織範圍設定 | 為每個人啟用同事存取，或為您的組織停用它。 |
| 使用者或使用者群組覆寫 | 覆寫可讓管理員控制特定使用者或使用者群組的同事存取權。 |
| 相容的應用程式許可權 | 同事存取控制可決定您是否可以存取任何一般可用的同事功能。 同事會從與同事相容的CX Enterprise應用程式繼承您的使用者許可權，並尊重每個應用程式已強制執行的許可權。 |


## 同事管理員 {#add-coworker-admins}

同事管理員是指派為組織的&#x200B;**[!UICONTROL 系統管理員]**，或是[!DNL Adobe Admin Console]中[!DNL Adobe Experience Platform]的&#x200B;**[!UICONTROL 產品管理員]**&#x200B;的使用者。

## 管理使用者存取權 {#manage-user-access}

1. 開啟同事體驗。 如需指示，請參閱[登入同事](/help/chat/ui-guide.md#sign-in)。
2. 開啟設定檔功能表並選取&#x200B;**[!UICONTROL 管理員設定]**。

   ![已反白設定檔功能表控制項的同事首頁。](./assets/access-control/coworker-home.png)

   ![已反白顯示管理員設定的[同事設定檔]功能表。](./assets/access-control/admin-settings.png)

3. 選取&#x200B;**[!UICONTROL 存取控制]**。

   ![反白顯示存取控制卡的管理設定。](./assets/access-control/access-control.png)

   使用本影片瞭解如何管理同事使用者。

   >[!VIDEO](https://video.tv.adobe.com/v/3507151?learn=on){transcript=true}

4. 在同事中，使用&#x200B;**[!UICONTROL 使用者]**&#x200B;管理個人的存取權，或使用&#x200B;**[!UICONTROL 使用者群組]**&#x200B;管理使用者群組的同事存取權。 使用者群組設定適用於其成員。

   同事使用者群組與[!DNL Adobe Admin Console]群組不同。 即將從[!DNL Adobe Admin Console]將使用者群組同步至同事。

   使用者清單包含您組織中的使用者。 預設會為這些使用者啟用同事存取。

   * **已啟用：**&#x200B;使用者或使用者群組為作用中。
   * **已停用：**&#x200B;使用者或使用者群組為非使用中。

   當所有人的存取權停用時，請開啟&#x200B;**[!UICONTROL 允許覆寫]**&#x200B;並選取&#x200B;**[!UICONTROL 新增覆寫]**&#x200B;以新增仍應具有存取權的使用者或群組。

## 與同事相容的CX Enterprise應用程式中的許可權 {#permissions-in-compatible-applications}

與同事相容的CX Enterprise應用程式會繼續強制執行其本身的許可權。

同事尊重相容應用程式中的許可權。 例如，如果您無法存取[!DNL Adobe Experience Platform]中的資料集，Co-worker將無法為您擷取或處理該資料集。

## 取得存取權相關協助 {#get-help-with-access}

如果您沒有看到[!UICONTROL 存取控制]，請聯絡您的Adobe管理員或Adobe代表。 他們可以確認您的組織是否已啟用該功能，以及您是否有存取其設定的許可權。

如果您被拒絕存取，請要求您的管理員檢閱整個組織的預設值以及任何使用者或群組設定。 若為與同事相容的CX Enterprise應用程式，請要求他們檢查針對該應用程式個別管理的許可權。

## 有關此主題的更多說明 {#more-help}

使用這些資源取得有關同事和管理的詳細資訊。

* [同事聊天總覽](/help/chat/overview.md)
* [開始使用同事聊天](/help/chat/ui-guide.md)
* [管理外掛程式和市集](/help/customizations/plugins/manage-plugins-for-your-org.md)
