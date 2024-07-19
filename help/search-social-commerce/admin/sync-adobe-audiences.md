---
title: Synchronisieren von  [!DNL Adobe] Zielgruppen
description: Erfahren Sie, wie Sie Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für Ihre [!DNL Adobe] Zielgruppen synchronisieren.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Synchronisieren von [!DNL Adobe] Zielgruppen

*[!DNL Direct Access]Nur Client-Manager und Administratoren*

*Advertiser nur mit einer Adobe Advertising-Adobe Audience Manager- oder Adobe Advertising-Adobe Analytics-Integration*

Sie können zulassen, dass Search, Social und Commerce Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle [!DNL Adobe] -Zielgruppen eines Advertisers oder einer Agentur in die Ansichten [!UICONTROL Campaigns] > [!UICONTROL Audiences] ziehen. Diese Informationen umfassen Daten für:

* Adobe Audience Manager-Segmente

* Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden

* Segmente, die mit dem Adobe Experience Cloud [!DNL Audience Library] erstellt wurden

Um zugelassen zu werden, muss der Advertiser oder die Agentur den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) implementieren und seine Organisations-ID (früher [!DNL IMS Org ID]) angeben.

Die anfängliche Synchronisation dauert etwa 24 Stunden. Danach werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Geben Sie die eindeutige Organisations-ID für das Adobe Experience Cloud-Konto des Advertisers ein und klicken Sie auf **[!UICONTROL Submit]**.

   Wenn Sie die Organisations-ID des Advertisers nicht kennen, suchen Sie sie im Feld **[!UICONTROL IMS Org ID]** in den Einstellungen des Advertisers unter [!UICONTROL Admin] > [!UICONTROL Manage Client] nach.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integration mit Adobe Experience Cloud-Lösungen und -Diensten](/help/search-social-commerce/introduction/integrations.md)
