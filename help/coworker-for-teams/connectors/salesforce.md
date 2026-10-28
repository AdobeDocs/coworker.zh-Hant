---
description: 瞭解如何將團隊的同事連線到您的Salesforce帳戶以存取您的潛在客戶和聯絡人。
title: 連線至Salesforce
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 312450e09d9252f17cb2b5d471ee33e1a22b9a05
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%
---
# 連線至Salesforce {#salesforce}

團隊同事可讓您連線您的Salesforce帳戶，以存取您的銷售機會和聯絡人。

>[!PREREQUISITES]
>
>若要使用此聯結器，您必須先擁有：
>
>* 有效的Salesforce帳戶
>* Salesforce中的下列許可權： `api`、`sobjects.Contact.read`、`sobjects.Campaign.read`、`sobjects.CampaignMember.read`
>* 您的Salesforce執行個體URL、[使用者端ID和使用者端密碼](https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_client_credentials_flow.htm&type=5#:~:text=DESCRIPTION-,client_id,-The%20consumer%20key){target="_blank"}已可使用

## 如何連線

1. 在[Co-worker for teams首頁](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，按一下&#x200B;**內容**&#x200B;並選取&#x200B;**聯結器**。

   ![團隊的同事已展開內容並醒目提示聯結器的左側導覽](./assets/salesforce-1.png)

1. 按一下&#x200B;**新增整合**。

   ![在Connectors畫面中新增整合按鈕](./assets/salesforce-2.png)

   >[!NOTE]
   >
   >如果這不是您的第一次整合，按鈕會顯示「新增聯結器」。

1. 在Salesforce列中，按一下&#x200B;**連線**。

   ![Salesforce聯結器圖磚，帶有連線按鈕](./assets/salesforce-3.png)

1. 輸入您的Salesforce **執行個體URL**、**使用者端識別碼**&#x200B;和&#x200B;**使用者端密碼**。 按一下&#x200B;**連線**。

   >[!NOTE]
   >
   >* 在Salesforce中，使用者端ID =消費者金鑰，而使用者端密碼=消費者密碼。
   >
   >* 在您的Salesforce帳戶中，您可以在瀏覽器的位址列中找到執行個體URL，或瀏覽至&#x200B;**設定** > **公司設定** > **我的網域**。

   ![使用執行個體URL、使用者端ID和使用者端密碼的欄位連線Salesforce對話方塊](./assets/salesforce-4.png)

連線後，Salesforce會出現在聯結器清單中，並可在連結潛在客戶或連絡人清單以從Salesforce同步時選取。

**中斷連線：**

1. 在Connectors畫面中，找到Salesforce圖磚，然後按一下&#x200B;**管理**。

   ![聯結器畫面顯示Salesforce已連線並反白顯示「管理」按鈕](./assets/salesforce-5.png)

1. 按一下&#x200B;**中斷連線** （目前不需要重新輸入您的使用者端密碼）。

   ![管理Salesforce對話方塊，並反白顯示[中斷連線]按鈕](./assets/salesforce-6.png)

1. 再按一下&#x200B;**中斷連線**&#x200B;以確認。

   ![中斷連線確認對話方塊，反白顯示[中斷連線]按鈕](./assets/salesforce-7.png)
