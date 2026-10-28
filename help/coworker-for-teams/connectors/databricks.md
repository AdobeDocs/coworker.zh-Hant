---
description: 適用於團隊的同事可讓您連線並查詢Databricks工作區中的Unity目錄表格，以建立並啟用行銷活動對象。
title: 連線到Databricks
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: bd7454ee46cb1ee4ca8b7ae6ab07348a23854979
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# 連線到Databricks {#databricks}

適用於團隊的同事可讓您連線並查詢Databricks工作區中的Unity目錄表格，以建立並啟用行銷活動對象。

>[!PREREQUISITES]
>
>若要使用此聯結器，您必須先擁有：
>
>* 有效的Databricks帳戶
>* 您的Databricks Workspace主機、[SQL倉儲路徑](https://docs.databricks.com/aws/en/compute/sql-warehouse/create){target="_blank"}、[個人存取權杖](https://learn.microsoft.com/en-us/azure/databricks/dev-tools/auth/pat){target="_blank"}以及[Unity目錄](https://learn.microsoft.com/en-us/azure/databricks/discover/database-objects){target="_blank"}方便使用。

## 如何連線

1. 在[Co-worker for teams首頁](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，按一下&#x200B;**內容**&#x200B;並選取&#x200B;**聯結器**。

   ![團隊的同事已展開內容並醒目提示聯結器的左側導覽](./assets/databricks-1.png)

1. 按一下&#x200B;**新增整合**。

   ![在Connectors畫面中新增整合按鈕](./assets/databricks-2.png)

   >[!NOTE]
   >
   >如果這不是您的第一次整合，按鈕會顯示「新增聯結器」。

1. 在[資料庫]列中，按一下[連線]。**&#x200B;**

   ![具有[連線]按鈕的Databricks聯結器拼貼](./assets/databricks-3.png)

1. 輸入您的Databricks **Workspace主機**、**SQL倉儲路徑**、**個人存取權杖**&#x200B;和&#x200B;**Unity目錄**。 按一下&#x200B;**連線**。

   >[!NOTE]
   >
   >在您的Databriks首頁上時，可以直接在瀏覽器的位址列找到Workspace主機。 若要尋找所有其他認證，請參閱本文最上方的&#x200B;**必要條件**&#x200B;中的連結。

   ![連線資料庫對話方塊包含Workspace主機、SQL倉儲路徑、個人存取權杖和Unity目錄的欄位](./assets/databricks-4.png)

連線之後，Databricks會出現在聯結器清單中。

**中斷連線：**

1. 在Connectors畫面中，找到Databricks方塊，然後按一下&#x200B;**管理**。

1. 按一下&#x200B;**中斷連線** （目前不需要重新輸入您的個人存取權杖）。

1. 再按一下&#x200B;**中斷連線**&#x200B;以確認。
