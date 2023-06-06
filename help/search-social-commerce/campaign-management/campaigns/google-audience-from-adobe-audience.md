---
title: Erstellen [!DNL Google Ads] Kundenabgleich-Zielgruppen aus [!DNL Adobe] Zielgruppen
description: Erfahren Sie, wie Sie [!DNL Google Ads] Kundenabgleich von Zielgruppen aus Ihrer bestehenden Adobe Analytics- und Audience Manager-Zielgruppe.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Erstellen [!DNL Google Ads] Zielgruppen für die Kundenabstimmung aus Adobe Analytics- und Audience Manager-Zielgruppen

*[!DNL Google Ads]Konten, die nur für die Kundenübereinstimmung infrage kommen*

*Werbetreibende mit nur einer Adobe Advertising-Adobe Audience Manager- oder Adobe Advertising-Adobe Analytics-Integration*

Opt-in-Advertiser können [!DNL Google Ads] Kundenabgleich von Zielgruppen mithilfe von Benutzer-IDs aus a) [!DNL Analytics] Segmente, die für Adobe Experience Cloud freigegeben sind, und b) Audience Manager-Segmente, die über Search, Social und Commerce als Ziel verfügen, einschließlich [!DNL Analytics] Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die mithilfe der Adobe Experience Cloud-Zielgruppenbibliothek erstellt werden. In Search, Social und Commerce wird automatisch ein [!DNL Google] Tracking-URL zu jedem [!DNL Analytics] oder Audience Manager [!DNL Google] kann die Zielgruppe verfolgen.

Jeder [!DNL Adobe] Zielgruppe kann nur für eine [!DNL Google] Zielgruppe.

Jeder neue [!DNL Google] -Zielgruppe hat denselben Namen wie die ursprüngliche [!DNL Adobe] Zielgruppe. [!DNL Google] bestimmt, wie groß die Zielgruppe sein muss, um eine Zielgruppenbestimmung durchzuführen.

>[!TIP]
>
>Verwenden Sie für die Echtzeit-Segmentierung vom Audience Manager erstellte Zielgruppen. In erstellte Segmente [!DNL Analytics] und mit Adobe Experience Cloud synchronisiert werden, können kleinere Populationen aufweisen, da sie nur täglich synchronisiert werden; Ein Surfer, der sich für ein Segment qualifiziert, kann erst am nächsten Tag in das Segment aufgenommen werden. Segmente aus [!DNL Analytics] eine Datenquelle von &quot;Report Suite -&quot;haben.

>[!NOTE]
>
>Search, Social und Commerce speichert keine Kundendaten aus Ihren [!DNL Adobe] Segmente zum Erstellen oder Bearbeiten von [!DNL Google] Zielgruppe.

1. Führen Sie nach Bedarf die Voraussetzungen aus:

   1. (So erstellen Sie Benutzer-ID-Remarketing-Listenzielgruppen) Eine [!DNL Adobe] Admin-Benutzer oder -Kundenbetreuer müssen die Einstellung auf Advertiser-Ebene auswählen, um Zielgruppen für die Kundenabstimmung zu aktivieren. Die Einstellungen unterscheiden sich zwischen Advertisern mit Audience Manager und Advertisern mit [!DNL Analytics] nur.

   1. Implementieren des [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) Version 2.0 oder höher.

   1. Stellen Sie das folgende Tag so weit wie möglich auf den Webseiten des Advertisers bereit, von denen aus die Zielgruppe verfolgt werden soll

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      where `Advertising_Cloud_UserID` ist die eindeutige Benutzer-ID, die dem Advertiser zugewiesen ist. Beispiel:  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Falls noch nicht abgeschlossen) Ein autorisierter Benutzer muss das Konto des Werbetreibenden so konfigurieren, dass [Synchronisierung mit dem Organisationskonto des Advertisers in Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Im **[!UICONTROL Data Source]** Menü auswählen **[!UICONTROL Adobe Audience]**.

   1. Wählen Sie die [!UICONTROL Adobe Audience] auf der die [!DNL Google] Zielgruppe.

      >[!NOTE]
      >
      >[!DNL Adobe] Zielgruppen, die bereits für eine andere [!DNL Google] Zielgruppe nicht verfügbar.

      Sie können optional nach Zielgruppen suchen, die eine bestimmte Textzeichenfolge mit mindestens drei Zeichen enthalten. Klicken Sie für jede passende Zielgruppe auf **[!UICONTROL Include]** , um sie auszuwählen.

      Wenn Sie mehrere [!DNL Adobe] Zielgruppen und dann eine separate [!DNL Google] für jede Zielgruppe erstellt wird.

   1. Wählen Sie die **[!UICONTROL Audience Type]** , um Folgendes zu erstellen: **[!UICONTROL Customer List_User ID]**.

      Die [!DNL Google Ads] muss [für benutzerdefinierte Übereinstimmung geeignet](https://support.google.com/adspolicy/answer/6299717) und sich für [Benutzer-ID-Remarketing](https://support.google.com/google-ads/answer/9199250).

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie den Bedingungen der [!DNL Adobe] Datenschutzrichtlinien für Werbenetzwerke.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]**: die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt.

      Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist. Remarketing-Listen haben eine maximale Dauer von 540 Tagen. Kundenlisten haben keine maximale Dauer. um anzugeben, dass das Cookie nie abläuft, geben Sie 10000 ein.

   1. Klicken **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] kann bis zu 24 Stunden dauern, bis die Datei verarbeitet wird.
>
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise und Einschränkungen von Kundenabgleich](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen Sie eine [!DNL Google Ads] Zielgruppe für Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Zielgruppen verwalten](audience-dynamic-remarketing-manage.md)

