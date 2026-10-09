---
title: 管理資料湖保留
description: 瞭解如何使用CX Coworker來識別值得最佳化的體驗事件資料、分析資料集使用和保留影響，以及管理資料湖保留政策。
role: Developer
level: Beginner, Intermediate
doc-type: Feature Video
duration: 160
last-substantial-update: 2026-10-09
jira: KT-22762
source-git-commit: 7ae11e6865d847c6a3c316ffa26b2e4303f7e40d
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 1%
---
# 管理資料湖保留

使用CX Coworker瞭解沙箱中Experience Event資料的價值，並識別可能受益於最佳化的資料。 您可以從廣泛的請求開始，例如要求同事最佳化您的沙箱資料或清除資料集。 Co-worker使用資料管理代理程式來呈現值得調查的資料集、分析資料集的使用主動性、模擬保留期間的影響，並在適當時協助您管理其Data Lake保留政策。

>[!VIDEO](https://video.tv.adobe.com/v/3504105?captions=chi_hant&learn=on)

## 開始之前 {#before-you-begin}

確保您使用的沙箱包含您要檢閱的資料集。 您也需要存取資料管理代理程式和所需的Adobe Experience Platform許可權。 請參閱[資料管理代理程式先決條件](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/agents/data-management#prerequisites)。

## 將沙箱中的資料最佳化 {#optimize-data-in-your-sandbox}

將這些技能搭配使用當作工作流程。 從廣泛的資料管理目標開始，例如瞭解資料的價值或最佳化沙箱中的資料。 Co-worker可協助您尋找值得調查的資料集、檢查資料集的使用主動性、模擬潛在保留期間的影響，然後在您準備好採取行動時設定、變更或移除保留原則。

### 尋找值得最佳化的資料 {#find-data-worth-optimizing}

若要決定從何處開始，請要求同事識別值得調查的體驗事件資料集。 您可以從詢問資料、資料最佳化或資料集清理的值開始。 使用「列出資料集」技能來檢閱儲存大小、列計數、現有保留狀態和設定檔啟用。 您可以依資料集大小、列計數或最近存取等條件篩選結果，以縮小清單範圍。 此技能為唯讀。 Co-worker會傳回可掃描和比較的表格，以及可依大小、列計數和資料保留時間強調資料集的視覺效果。

![在表格中顯示體驗事件資料集的同事結果，包含儲存空間、列數、保留資訊，以及資料集大小和資料期限的視覺效果。](../../assets/data-management/dataset-discovery-results.png)

縮小清單範圍後，請使用「分析資料集使用情形」技能，瞭解特定資料集的使用情形。

並非所有以此技能顯示且未使用或放棄的資料集都是資料湖保留原則的理想適用對象。 如果您需要移除整個資料集或管理其他Experience Platform存放區的資料，請參閱[選擇正確的資料生命週期管理功能](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-lifecycle/choose-a-capability)。 在設定資料湖保留原則之前，請確認資料集是體驗事件資料集。

提示範例：

- 「我覺得我的資料可以最佳化。」
- 「協助我瞭解資料的價值。」
- 「最佳化我的沙箱資料。」
- 「清理我的沙箱資料集。」
- 「顯示我最大的事件資料集。」
- 「顯示大於100 GB且沒有資料湖保留設定的資料集。」
- 「我需要移除約2 TB的資料。 我應該從哪裡開始？」
- 「您可以協助我尋找孤立、捨棄或未使用的資料嗎？」
- 「優先處理過去90天內未存取的資料集。」

### 檢查資料集的使用主動性 {#check-how-actively-a-dataset-is-used}

在您決定資料集是否為資料湖保留原則的合適候選資料集之前，請先瞭解資料集的使用主動性。 使用分析資料集使用技巧，針對多個使用訊號評估特定資料集。 這些訊號包括最近的擷取活動、查詢活動、結構描述穩定性，以及資料集是否提供其他Adobe Experience Platform應用程式。 此技能為唯讀。 Co-worker會傳回整體使用層級、訊號劃分，以及資料集相關資訊的簡單語言摘要。

<!-- TODO: Confirm the final usage-tier thresholds with engineering after the planned update from a 7-day to a 30-day analysis window is complete. Update this section with the final definitions before publishing. -->

>[!NOTE]
>
>顯示的量度旨在提供有用的訊號，但可能並不代表與您的決定相關的所有因素。 我們建議您在採取行動之前，先檢閱可用的詳細資料並套用您的業務內容。

![顯示使用階層、個別使用訊號及資料集活動摘要的同事資料集使用量分析。](../../assets/data-management/dataset-usage-analysis.png)

提示範例：

- 「使用我的Web事件資料集的積極性如何？」

### 模擬保留期間的影響 {#model-the-impact-of-a-retention-period}

在您認可特定的保留期間之前，請先瞭解將保留或移除多少資料。 使用「分析資料集保留率」技能，檢閱資料集的儲存量度及其資料的使用年齡分佈。 然後它會使用該分佈來模型化建議的保留期間將保留或移除的資料量。 Co-worker會依資料列計數和儲存大小顯示預估的影響。

![同事比較保留期30、60和90天保留和移除的資料列數目。](../../assets/data-management/retention-period-comparison.png)

此技能為唯讀。 Co-worker會直接在交談中傳回資料年齡和影響分析，讓您在決定是否變更結果之前，先將結果與資料集目前的保留設定進行比較。

提示範例：

- 「如果對此資料集設定60天的保留期，會有什麼影響？」

### 設定、變更或移除保留原則 {#set-change-or-remove-a-retention-policy}

>[!IMPORTANT]
>
>資料湖保留期間下限為30天。 不支援較短的句點。

決定保留期間後，請使用「管理資料集保留期間」技能，在資料集上設定、變更或移除資料湖保留政策。 此技能會顯示套用任何變更前的建議影響。 只有在您明確核准請求後，才會套用原則。 描述您想要的變更並不會套用它。

![在套用變更前，顯示所建議Data Lake保留原則、其影響及所需確認的共同工作者。](../../assets/data-management/retention-impact-preview.png)

在您確認保留原則後，可能需要一段時間才會將變更顯示在Adobe Experience Platform UI中。 保留原則不會立即刪除過期的資料。 初始保留工作會在套用原則後24小時內開始。 初次執行後，排程的工作會每隔30天評估及刪除過期的記錄。 請參閱[Experience Event資料集保留(TTL)指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide)，以取得有關保留和清除的詳細資訊。

每次保留原則變更都會記錄在稽核軌跡中，包括原則設定、變更或移除的時間。 稽核軌跡會記錄每次變更的人員、變更發生的時間以及變更內容。 您可以依照同事提供的連結，在Adobe Experience Platform的資料集「稽核記錄」標籤中檢閱這些事件。 如需詳細資訊，請參閱[稽核記錄總覽](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview)。

![Adobe Experience Platform稽核記錄檔顯示資料湖保留原則更新，包括時間戳記、使用者、資料集、動作和狀態。](../../assets/data-management/retention-audit-log.png)

提示範例：

- 「將此資料集的保留時間設為60天。」
- 「移除此資料集的保留原則。」

## 最佳實務 {#best-practices}

使用Data Management Agent時，請記住下列實務作法：

- **從廣泛的目標開始。** 如果您不知道哪些資料集需要注意，請要求同事協助您瞭解資料的價值，或最佳化沙箱中的資料。 在分析個別資料集之前，先使用清單資料集技能來識別具有訊號的資料集，該訊號指出最近使用率低或沒有使用率。
- **確認前請先檢閱影響預覽。** 在您核准保留變更之前，請先檢閱將保留和移除的專案。
- **允許有時間顯示變更。** 在CX Coworker中確認保留變更後，請留出一段時間讓Adobe Experience Platform UI反映變更。

## 後續步驟 {#next-steps}

若要進一步瞭解資料管理代理程式的技能、範圍、行為和限制，請參閱[資料管理代理程式概述](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/agents/data-management)。 如需Adobe Experience Platform中資料湖保留原則如何運作的詳細資訊，請參閱[Experience Event資料集保留(TTL)指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide)。
