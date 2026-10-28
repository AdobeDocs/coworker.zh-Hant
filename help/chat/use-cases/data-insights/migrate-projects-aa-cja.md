---
title: 將Adobe Analytics專案移轉至Customer Journey Analytics
description: 使用同事驗證、對應及移轉Adobe Analytics Workspace專案及其元件至Customer Journey Analytics，然後檢查移轉狀態。
feature: AI Tools
role: Admin
level: Intermediate
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: decc8d209d4c9c177c6329a30668f0bbb8bd2c00
workflow-type: tm+mt
source-wordcount: '1785'
ht-degree: 1%
---

# 與同事將Adobe Analytics專案移轉至Customer Journey Analytics

<!-- FLAG: Confidence: High for the conversation flow, which is sourced from screenshots of the Coworker UI (October 2026) and the aa-mcp tool descriptions. The component migration tools run through the aa-mcp integration; there's no dedicated skill yet. Medium for statements that Coworker shares mappings and migration rules with migrations in the Adobe Analytics user interface; the user believes this is likely. Confirm with engineering. -->

透過單一交談，使用Adobe CX Enterprise Coworker將Adobe Analytics專案及其相關元件移轉至Customer Journey Analytics。

同事會驗證專案中的維度和量度已對應至您的Customer Journey Analytics資料檢視，協助您對應未對應的任何檢視，然後在Customer Journey Analytics中重新建立專案。

<!-- FLAG: Add the planned general availability date when it's confirmed. -->

>[!AVAILABILITY]
>
>本文所述的功能處於發行的有限測試階段，可能尚未在您的環境中提供。 當功能正式可用時，將移除此附註。

>[!IMPORTANT]
>
>在移轉任何專案之前，請閱讀Adobe Analytics檔案中的[準備將元件和專案從Adobe Analytics移轉到Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration)。 它說明如何準備移轉、包含的內容、哪些元素會導致錯誤，以及對應如何影響整個組織。 此資訊適用於Co-worker中的移轉。

## 與Adobe Analytics使用者介面中移轉的差異

<!-- FLAG: Add rows as differences are confirmed. Who can migrate and How you migrate: SME Scott Tomko (October 2026); Coworker matches the Analytics 2.0 Component Migration APIs, and functionally both methods do much the same thing. Project owner: Coworker behavior is from a test conversation (October 2026); the Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. Mapping dimensions and metrics: Confidence Medium for the Coworker column, which is based on the aa-mcp tool descriptions and a test conversation, not on an observed failed validation. Confirm that Coworker suggests and updates mappings, and whether it asks for confirmation before it updates a mapping. The Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. -->

使用Co-worker移轉專案與在Adobe Analytics使用者介面中移轉專案有以下不同：

| | Coworker | Adobe Analytics使用者介面 |
| --- | --- | --- |
| **誰可以移轉專案** | Adobe Analytics管理員和具有&#x200B;[!UICONTROL **元件移轉**]&#x200B;許可權的使用者 | 僅限Adobe Analytics管理員 |
| **專案所有者** | 執行移轉的使用者 | 您在&#x200B;[!UICONTROL **專案所有者**]&#x200B;欄位中指定的使用者 |
| **對應維度和量度** | 同事會驗證專案，並列出每個維度和量度的對應方式。 對於無法自動對應的專案，同事會在資料檢視中建議維度或量度，並更新對應。 | 在&#x200B;[!UICONTROL **對應結構描述**]&#x200B;區段中，您選取每個具有&#x200B;[!UICONTROL **未對應**]&#x200B;狀態的維度或量度，並手動進行對應。 |
| **如何移轉** | 說明您要在提示中顯示的內容。 由同事負責工作，並在此過程中提出幾個問題。 例如，Co-worker可以使用您命名的元件來建立專案，然後進行移轉。 請參閱[從特定元件開始](#start-from-specific-components)。 | 在Analysis Workspace中建立專案、新增您要移轉的元件，並儲存專案。 然後，在&#x200B;[!UICONTROL **元件移轉**]&#x200B;中，選取專案、指定專案所有者、對應每個報表套裝的結構描述，並選取&#x200B;[!UICONTROL **移轉**]。 |

## 先決條件

<!-- FLAG: Confidence: High for the Adobe Analytics MCP and permission bullets, which come from the release announcement and SME Scott Tomko (October 2026): like the Analytics 2.0 Component Migration APIs, Coworker lets non-admins with the Component Migration permission migrate projects, while the Adobe Analytics UI is admin-only. Open question: Coworker makes the user who runs the migration the owner of the new project, but the aa-mcp tool description says the owner "should be an admin" and the Adobe Analytics component migration docs say the owner must be a Customer Journey Analytics administrator. Confirm whether a non-admin who runs a migration needs Customer Journey Analytics admin rights, or whether Coworker assigns a different owner. -->

若要與同事移轉專案，您需要：

* 存取Adobe Analytics MCP。 擁有Adobe Analytics MCP存取權的客戶會自動啟用元件移轉工具。 若要確認&#x200B;[!UICONTROL **aa-mcp**]&#x200B;已連線，請參閱[開始使用同事聊天分析資料](/help/chat/use-cases/data-insights/analytics-chat.md)。

* Adobe Analytics管理員許可權，或Admin Console中的&#x200B;[!UICONTROL **元件移轉**]&#x200B;許可權。 您不需要成為管理員。

* Adobe Analytics檔案中元件移轉的[必要條件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#prerequisites)。

* 使用基本報表套裝的專案。 無法移轉虛擬報表套裝。<!-- FLAG: Sourced from Coworker's response in the UI. The Adobe Analytics component migration docs don't mention virtual report suites. Confirm, and consider adding it to those docs. -->

## 移轉前先檢閱報表套裝對應

<!-- FLAG: Confidence: Medium. The recommendation to review mappings before the first migration from a report suite is inferred from the Adobe Analytics guidance to decide mappings as an organization; Coworker also validates mappings during each migration. Confirm with Scott. -->

在您首次從該報表套裝移轉之前，請考慮檢閱報表套裝的維度和量度如何對應。 對應會套用至您的組織移轉的每個專案，因此先處理這些對應有助於後續的專案通過驗證。 如需選擇對應的指引，請參閱Adobe Analytics檔案中的[決定作為組織如何對應元件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#decide-as-an-organization-how-you-will-map-components)。

若要檢閱對應，請在&#x200B;[!UICONTROL **範圍**]&#x200B;索引標籤上選取&#x200B;[!UICONTROL **僅檢閱對應**]，或直接詢問同事：

**提示**

* 「顯示如何將我的報表套裝中的維度和量度對應至我的資料檢視」
* 「報表套裝中的哪些維度和量度未對應至我的資料檢視？」

您也可以要求同事更新對應。

如果您略過此檢閱，同事仍會[檢查您移轉的每個專案的對應](#review-the-validation-results-and-mappings)。

## 開始移轉

<!-- FLAG: Confidence: High that migration works at the project level and that components migrate with their project (component-migration.md in the Adobe Analytics docs), and that components that already exist in Customer Journey Analytics aren't re-created (prepare-component-migration.md). Medium-low for when to use each method and for combining them; this guidance is inferred and isn't in the Adobe Analytics docs. Confirm with Scott. Also confirm whether Coworker creates a project automatically when you ask it to migrate only components (for example, "Migrate my Spring sale segments to CJA"), or whether you must ask it to create the project. -->

同事一律會移轉專案及其相關元件。 若要移轉特定元件，請要求同事將元件新增至新專案，然後移轉該專案。

Customer Journey Analytics中已存在的元件不會重新建立，因此您可以使用這兩種方法。 例如，先移轉您最重要的專案，然後移轉任何剩餘的元件。 根據您想要在Customer Journey Analytics中看到的內容選擇開始位置：

* **當您想要在Customer Journey Analytics中保留專案的面板和視覺效果時，請移轉專案**。 請參閱[從專案開始](#start-from-a-project)。
* **當您想要在Customer Journey Analytics中使用區段、計算量度或日期範圍等元件，但不需要使用這些元件的任何專案時，請移轉特定元件**。 例如，您可能會計畫在Customer Journey Analytics中建置包含這些專案的新專案。 請參閱[從特定元件開始](#start-from-specific-components)。

### 從專案開始

若要移轉專案及其相關元件，請執行下列動作：

1. 登入同事。

1. 選取&#x200B;**[!UICONTROL 新增聊天]**。

1. 在文字欄位中，提示同事移轉您的專案。 例如：

   **提示**

   > 我想將元件從Adobe Analytics移轉至Customer Journey Analytics。

   同事描述可以移轉的專案，並啟動問卷。

1. 在&#x200B;[!UICONTROL **領域**]&#x200B;索引標籤上，選取下列其中一個選項，然後選取&#x200B;[!UICONTROL **下一步**]：

   <!-- FLAG: Confidence: Medium for the "Plan a full upgrade" description. It likely hands off to the implementation guide skill and leaves the migration flow. Confirm with engineering. Also confirm what the Source & target tab asks; it was skipped in the screenshots. The Next and Submit buttons on the first questionnaire's Source & target and Review tabs are assumed to work like the second questionnaire. -->

   | 選項 | 說明 |
   | --- | --- |
   | [!UICONTROL **特定AA專案**] | 移轉您命名的專案。 請依照本節中的其餘步驟操作。 |
   | [!UICONTROL **僅檢閱對應**] | 檢查報表套裝的量度和維度如何對應至資料檢視，而不移轉任何專案。 在移轉[&#128279;](#review-report-suite-mappings-before-you-migrate)之前，請參閱檢閱報表套裝對應。 |
   | [!UICONTROL **計畫完整升級**] | 取得從Adobe Analytics移轉至Customer Journey Analytics的端對端計畫。 請參閱[與同事一起規劃您的實作](/help/chat/use-cases/data-insights/implementation-guide.md)。 |

1. （選擇性）回答&#x200B;[!UICONTROL **Source &amp; target**]&#x200B;標籤上的問題，然後選取&#x200B;[!UICONTROL **下一步**]。

1. 在&#x200B;[!UICONTROL **檢閱**]&#x200B;標籤上，確認您的答案，然後選取&#x200B;[!UICONTROL **提交**]。

   同事會檢查您有權存取哪些Adobe Analytics公司，以及每個公司都有多少個基本報表套裝，然後開始進行第二次問卷調查。

1. 回答下列問題，並在每個問題之後選取&#x200B;[!UICONTROL **下一個**]：

   | 標記 | 問題 | 其他內容 |
   | --- | --- | --- |
   | [!UICONTROL **專案**] | 您要移轉的AA專案名稱為何？ | 部分名稱沒有問題。 |
   | [!UICONTROL **報告套裝**] | 專案使用哪個報表套裝？ | 從清單中選取報表套裝，或輸入其他報表套裝的名稱。 |
   | [!UICONTROL **資料檢視**] | 它應該移轉至哪個CJA資料檢視？ | （選擇性）輸入資料檢視的名稱，或保留空白，Co-worker會建議相符的資料檢視。 |

1. 在&#x200B;[!UICONTROL **檢閱**]&#x200B;標籤上，確認您的答案，然後選取&#x200B;[!UICONTROL **提交**]。

   若要在任何步驟略過問卷，請選取&#x200B;[!UICONTROL **略過問卷**]，並改為說明您想在聊天中看到的內容。

1. 繼續[檢閱驗證結果和對應](#review-the-validation-results-and-mappings)。

### 從特定元件開始

<!-- FLAG: Sourced from a prompt that SME Scott Tomko ran in Coworker (October 2026). The example is generalized; the original prompt named a customer. Coworker may ask a few questions along the way. Confirm what happens to the project that Coworker creates in Adobe Analytics, and to its migrated copy in Customer Journey Analytics, if you only wanted the components. -->

若要移轉特定元件：

1. 請要求同事使用這些元件建立專案，然後進行移轉。 例如：

   **提示**

   > 我想要將名稱中包含「春季促銷」的所有Analytics區段移轉至CJA。 新增所有這些區段後，建立新的Workspace專案，然後將該專案移轉至CJA。

   同事會在Adobe Analytics中建立專案。

1. 繼續下列區段，[檢閱驗證結果和對應](#review-the-validation-results-and-mappings)。

## 檢閱驗證結果和對應

<!-- FLAG: Confidence: Medium for the steps that fix a failed validation. They're based on the aa-mcp tool descriptions and on a test conversation where validation passed only after the project's panel was switched to a base report suite. Confirm how Coworker presents a failed validation, and whether it asks for confirmation before it updates a mapping. -->

同事會根據您選取的資料檢視驗證專案，然後報告是否可以移轉專案。 結果會列出專案中的每個維度和量度，以及與其對應的Customer Journey Analytics維度或量度。 例如：

* **量度：**&#x200B;發生次數變成事件
* **Dimension：**&#x200B;小時會維持一小時

有關移轉的元件和專案元素，請參閱[瞭解Adobe Analytics檔案中移轉所包含的內容](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-what-is-included-in-a-migration)。

如果驗證未通過：

* **無法自動對應的維度或量度：**&#x200B;同事建議您在資料檢視中對應每個維度或量度，更新對應，然後再次驗證專案。 您也可以告訴同事要將它與哪個維度或量度對應，例如「將頁面檢視對應至web.webPageDetails.pageViews.value」。

* **不支援的元素：**&#x200B;從Adobe Analytics的專案移除任何不支援的元素。 例如，請確定每個面板都使用基本報表套裝，而非虛擬報表套裝。 然後要求同事再次檢查專案。 如需不支援的元素清單，請參閱Adobe Analytics檔案中的[瞭解造成錯誤的不支援的元素](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-unsupported-elements-that-cause-errors)。

若要在移轉前檢查整個報表套裝的對應，請參閱[在移轉前先檢閱報表套裝的對應](#review-report-suite-mappings-before-you-migrate)。

## 移轉專案

1. 驗證通過時，Co-worker會詢問是否要在您選取的資料檢視上建立專案的Customer Journey Analytics版本。 選取&#x200B;[!UICONTROL **是，移轉**]，然後選取&#x200B;[!UICONTROL **提交**]。

   若要停止而不移轉，請選取&#x200B;[!UICONTROL **否，在此停止**]。

   同事會在Customer Journey Analytics中重新建立專案，而您則是專案所有者。 您原始的Adobe Analytics專案不會變更。

1. 繼續下列章節，[檢查移轉狀態](#check-the-migration-status)。

## 檢查移轉狀態

移轉會在背景執行，因此新專案可能尚未立即準備就緒。

1. 提示同事檢查移轉狀態：

   **提示**

   > 檢查狀態

   <!-- FLAG: The Failed row links to Retry a failed migration in the Adobe Analytics docs, but those steps use the Component migration page in the Adobe Analytics UI, which is admin-only. A non-admin with the Component Migration permission can't follow them. Confirm with Scott whether Coworker can retry a failed migration (for example, "Retry the migration"). If so, replace the link with a prompt. -->

   同事會報告下列其中一種狀態：

   | 狀態 | 其含義 |
   | --- | --- |
   | 已排入佇列 | 移轉正在等待開始。 |
   | 已開始 | 移轉進行中。 |
   | 已完成 | 移轉已完成。 Co-worker提供已移轉專案的摘要，包括專案名稱和資料檢視。 |
   | 失敗 | 移轉失敗。 您可以重試移轉。 請參閱Adobe Analytics檔案中的[重試失敗的移轉](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration#retry-a-failed-migration)。 |

1. 移轉完成後，請在Customer Journey Analytics Workspace中從您的專案清單開啟新專案。

1. （選用）將專案的所有權轉移給Customer Journey Analytics中的任何使用者。 如需詳細資訊，請參閱[轉移資產](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/asset-transfer/transfer-assets)。

移轉完成後，同事可建議另一個專案進行下一次移轉。

## 取得更好結果的秘訣

* 如果您不確定要使用哪個資料檢視，請將調查問卷中的資料檢視保留空白。 同事會建議符合報表套裝的資料檢視。
* 移轉後，請比較Adobe Analytics和Customer Journey Analytics資料，確認報表彼此相符。 從Adobe Analytics升級至Customer Journey Analytics時，請參閱[與同事驗證資料](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)。

## 後續步驟

* 若要改在Adobe Analytics使用者介面中移轉專案，請參閱Adobe Analytics檔案中的[將元件和專案從Adobe Analytics移轉至Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration)。
* 如需其他實作與管理使用案例，請參閱[智慧型實作與管理概觀](/help/chat/use-cases/data-insights/data-governance-and-validation.md)。
