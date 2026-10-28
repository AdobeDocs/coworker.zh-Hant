---
description: 瞭解如何將您的Marketo Engage帳戶連線到團隊的同事，以便同步Marketo智慧和靜態清單。
title: 連線至Marketo Engage
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: bd7454ee46cb1ee4ca8b7ae6ab07348a23854979
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%
---
# 連線至Marketo Engage {#marketo}

適用於團隊的同事可讓您連線您的Marketo Engage帳戶，以提取智慧和靜態清單。

>[!PREREQUISITES]
>
>若要使用此聯結器，您必須先擁有：
>
>* 有效的Marketo Engage帳戶
>* 您的Marketo **執行個體URL**
>* 為Marketo團隊的同事建立的[自訂服務](https://experienceleague.adobe.com/zh-hant/docs/marketo-developer/marketo/rest/custom-services#custom-services-1){target="_blank"}，其有[使用者端ID和使用者端密碼](https://experienceleague.adobe.com/zh-hant/docs/marketo-developer/marketo/rest/authentication#creating-an-access-token){target="_blank"}

## 如何連線

1. 在[Co-worker for teams首頁](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，按一下&#x200B;**內容**&#x200B;並選取&#x200B;**聯結器**。

   ![團隊的同事已展開內容並醒目提示聯結器的左側導覽](./assets/marketo-1.png)

1. 按一下&#x200B;**新增整合**。

   ![在Connectors畫面中新增整合按鈕](./assets/marketo-2.png)

   >[!NOTE]
   >
   >如果這不是您的第一次整合，按鈕會顯示「新增聯結器」。

1. 在Marketo列中，按一下&#x200B;**連線**。

   ![Marketo聯結器圖磚，帶有連線按鈕](./assets/marketo-3.png)

1. 輸入您的Marketo **執行個體URL**、**使用者端識別碼**&#x200B;和&#x200B;**使用者端密碼**。 按一下&#x200B;**連線**。

   >[!NOTE]
   >
   >檢視「我的Marketo」頁面時，您可以在瀏覽器的位址列中找到您的Marketo執行個體URL。

   ![使用執行個體URL、使用者端ID和使用者端密碼的欄位連線Marketo對話方塊](./assets/marketo-4.png)

連線後，Marketo會出現在聯結器清單中，並可在連結連絡人清單以從Marketo同步時選取。

**中斷連線：**

1. 在Connectors畫面中，找到Marketo圖磚，然後按一下&#x200B;**管理**。

   ![Connectors畫面，Marketo圖磚顯示[連線]狀態和[管理]按鈕](./assets/marketo-5.png)

1. 按一下&#x200B;**中斷連線** （目前不需要重新輸入您的使用者端密碼）。

   ![使用執行個體URL和使用者端ID欄位以及中斷連線按鈕來管理Marketo對話方塊](./assets/marketo-6.png)

   >[!NOTE]
   >
   >第一次新增執行個體URL後，預設為REST端點URL，結尾為`*.mktorest.com`。

1. 再按一下&#x200B;**中斷連線**&#x200B;以確認。

   ![中斷連線確認對話方塊](./assets/marketo-7.png)
