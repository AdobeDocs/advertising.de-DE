---
title: Erstellen von [!DNL Google Ads] Kundenabgleichs-Zielgruppen aus [!DNL Adobe] Zielgruppen
description: Erfahren Sie, wie Sie aus bestehenden Adobe Analytics- und Audience Manager-Zielgruppen [!DNL Google Ads] Zielgruppen für die Kundenabstimmung erstellen.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Erstellen von [!DNL Google Ads] Zielgruppen zur Kundenabstimmung aus Adobe Analytics- und Audience Manager-Zielgruppen

*[!DNL Google Ads]Konten, die nur für eine Kundenübereinstimmung infrage kommen*

*Advertiser nur mit einer Adobe Advertising-Adobe Audience Manager- oder Adobe Advertising-Adobe Analytics-Integration*

Opt-in-Advertiser können Zielgruppen für die [!DNL Google Ads]-Kundenabstimmung erstellen, indem sie Benutzer-IDs aus a) [!DNL Analytics] -Segmenten verwenden, die für Adobe Experience Cloud freigegeben sind, und b) Audience Manager-Segmenten mit Search, Social und Commerce als Ziel verwenden, einschließlich [!DNL Analytics] -Segmenten, die in Adobe Experience Cloud veröffentlicht werden, und Segmenten, die mithilfe der Adobe Experience Cloud-Zielgruppenbibliothek erstellt werden. In Search, Social und Commerce wird automatisch eine [!DNL Google]-Tracking-URL an jedes [!DNL Analytics]- oder Audience Manager-Segment zurückgegeben, damit [!DNL Google] die Zielgruppe verfolgen kann.

Jede [!DNL Adobe] -Zielgruppe kann nur für eine [!DNL Google] -Zielgruppe verwendet werden.

Jede neue [!DNL Google] -Zielgruppe hat denselben Namen wie die ursprüngliche [!DNL Adobe] -Zielgruppe. [!DNL Google] bestimmt, wie groß die Zielgruppe sein muss, um eine Zielgruppenbestimmung durchzuführen.

>[!TIP]
>
>Verwenden Sie für die Echtzeit-Segmentierung vom Audience Manager erstellte Zielgruppen. Segmente, die in [!DNL Analytics] erstellt und mit Adobe Experience Cloud synchronisiert wurden, weisen möglicherweise kleinere Populationen auf, da sie nur täglich synchronisiert werden. Ein Surfer, der sich für ein Segment qualifiziert, kann erst am nächsten Tag in das Segment aufgenommen werden. Segmente aus [!DNL Analytics] haben die Datenquelle &quot;Report Suite - .&quot;

>[!NOTE]
>
>In Search, Social und Commerce werden keine Kundendaten aus Ihren [!DNL Adobe] -Segmenten gespeichert, die zum Erstellen oder Bearbeiten einer [!DNL Google] -Zielgruppe verwendet werden.

1. Führen Sie nach Bedarf die Voraussetzungen aus:

   1. (Um Benutzer-ID-Remarketing-Listen-Zielgruppen zu erstellen) Ein [!DNL Adobe] Admin-Benutzer oder -Kundenbetreuer muss die Einstellung auf Advertiser-Ebene auswählen, um Zielgruppen für die Kundenabstimmung zu aktivieren.

   1. Implementieren Sie den [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) Version 2.0 oder höher.

   1. Stellen Sie das folgende Tag so weit wie möglich auf den Webseiten des Advertisers bereit, von denen aus die Zielgruppe verfolgt werden soll

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      wobei `Advertising_Cloud_UserID` die eindeutige numerische Benutzer-ID ist, die dem Advertiser zugewiesen ist.

      Beispiel: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Falls noch nicht abgeschlossen) Ein autorisierter Benutzer muss das Konto des Advertisers so konfigurieren, dass es mit dem Organisationskonto des Advertisers in Adobe Experience Cloud ](/help/search-social-commerce/admin/sync-adobe-audiences.md) synchronisiert wird.[

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im Menü **[!UICONTROL Data Source]** die Option **[!UICONTROL Adobe Audience]** aus.

   1. Wählen Sie die [!UICONTROL Adobe Audience] aus, auf der die [!DNL Google]-Zielgruppe basieren soll.

      >[!NOTE]
      >
      >[!DNL Adobe] -Zielgruppen, die bereits für eine andere [!DNL Google] -Zielgruppe verwendet werden, sind nicht verfügbar.

      Sie können optional nach Zielgruppen suchen, die eine bestimmte Textzeichenfolge mit mindestens drei Zeichen enthalten. Klicken Sie für jede passende Zielgruppe auf **[!UICONTROL Include]** , um sie auszuwählen.

      Wenn Sie mehrere [!DNL Adobe] Zielgruppen auswählen, wird für jede Zielgruppe eine separate [!DNL Google] -Zielgruppe erstellt.

   1. Wählen Sie die zu erstellende **[!UICONTROL Audience Type]** aus: **[!UICONTROL Customer List_User ID]**.

      Das [!DNL Google Ads] -Konto des Advertisers muss [ für eine benutzerdefinierte Übereinstimmung qualifiziert sein](https://support.google.com/adspolicy/answer/6299717) und sich für das [Benutzer-ID-Remarketing](https://support.google.com/google-ads/answer/9199250) angemeldet haben.

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke zustimmen.

   1. Geben Sie die Anzahl von **[!UICONTROL Membership Days]** an, also die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt.

      Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist. Remarketing-Listen haben eine maximale Dauer von 540 Tagen. Kundenlisten haben keine maximale Dauer. Um anzugeben, dass das Cookie nie abläuft, geben Sie 10000 ein.

   1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] kann bis zu 24 Stunden dauern, bis die Datei verarbeitet wird.
>
>* Siehe die [[!DNL Google Ads] Dokumentation zur Funktionsweise der Kundenabgleich und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen einer [!DNL Google Ads] Kundenübereinstimmungs-Audience aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)
