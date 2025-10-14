---
title: Zielgruppen  [!DNL Google Ads]  Kundenabgleich aus Zielgruppen  [!DNL Adobe]  Zielgruppen erstellen
description: Erfahren Sie, wie Sie  [!DNL Google Ads]  Ihren bestehenden Adobe Analytics- und Audience Manager-Zielgruppen Kundenabgleich erstellen.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Erstellen [!DNL Google Ads] Zielgruppen für den Kundenabgleich aus Adobe Analytics- und Audience Manager-Zielgruppen

*[!DNL Google Ads]Konten, die nur für den Kundenabgleich infrage kommen*

*Werbetreibende nur mit einer Adobe Advertising-Adobe Audience Manager- oder Adobe Advertising-Adobe Analytics-Integration*

[!DNL Google Ads] Opt-in-Werbetreibende können Zielgruppen für den Kundenabgleich erstellen, indem sie Benutzer-IDs aus a) [!DNL Analytics] Segmenten verwenden, die für Adobe Experience Cloud freigegeben sind, und b) Audience Manager-Segmenten, die Search, Social und Commerce als Ziel haben, einschließlich [!DNL Analytics] Segmenten, die für Adobe Experience Cloud veröffentlicht wurden, und Segmenten, die mit der Adobe Experience Cloud-Zielgruppenbibliothek erstellt wurden. Search, Social und Commerce sendet automatisch eine [!DNL Google] Tracking-URL zurück an jedes [!DNL Analytics]- oder Audience Manager-Segment, damit [!DNL Google] die Audience verfolgen können.

Jede [!DNL Adobe] Zielgruppe kann nur für eine [!DNL Google] Zielgruppe verwendet werden.

Jede neue [!DNL Google] Zielgruppe hat denselben Namen wie die ursprüngliche [!DNL Adobe] Zielgruppe. [!DNL Google] bestimmt, wie groß die Zielgruppe sein muss, damit sie anvisiert werden kann.

>[!TIP]
>
>Verwenden Sie für die Echtzeit-Segmentierung von Audience Manager erstellte Zielgruppen. Segmente, die in [!DNL Analytics] erstellt und mit Adobe Experience Cloud synchronisiert wurden, können kleinere Populationen haben, da sie nur täglich synchronisiert werden. Ein Surfer, der für ein Segment qualifiziert ist, kann erst am nächsten Tag in das Segment aufgenommen werden. Segmente aus [!DNL Analytics] haben die Datenquelle „Report Suite - &quot;.

>[!NOTE]
>
>Search, Social und Commerce speichern keine Kundendaten aus Ihren [!DNL Adobe] Segmenten, die zum Erstellen oder Bearbeiten einer [!DNL Google] Zielgruppe verwendet werden.

1. Schließen Sie die Voraussetzungen nach Bedarf ab:

   1. (Um Benutzer-ID-Remarketing-Listen-Zielgruppen zu erstellen) Ein [!DNL Adobe]-Admin-Benutzer oder Account Manager muss die Einstellung auf Advertiser-Ebene auswählen, um Zielgruppen für den Kundenabgleich zu aktivieren.

   1. Implementieren Sie [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) Version 2.0 oder höher.

   1. Stellen Sie das folgende Tag so hoch wie möglich auf den Webseiten des Werbetreibenden bereit, von denen aus die Zielgruppe verfolgt werden soll

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      wobei `Advertising_Cloud_UserID` die eindeutige numerische Benutzer-ID ist, die dem Advertiser zugewiesen ist.

      Beispiel: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Wenn dies noch nicht abgeschlossen ist) Ein autorisierter Benutzer muss das Konto des Werbetreibenden so konfigurieren, [&#x200B; es mit dem Organisationskonto des Werbetreibenden in Adobe Experience Cloud synchronisiert &#x200B;](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im **[!UICONTROL Data Source]** Menü **[!UICONTROL Adobe Audience]** aus.

   1. Wählen Sie die [!UICONTROL Adobe Audience] aus, auf der die [!DNL Google]-Zielgruppe basieren soll.

      >[!NOTE]
      >
      >[!DNL Adobe] Zielgruppen, die bereits für eine andere [!DNL Google] Zielgruppe verwendet werden, sind nicht verfügbar.

      Sie können optional nach Zielgruppen suchen, die eine bestimmte Textzeichenfolge mit mindestens drei Zeichen enthalten. Klicken Sie für jede passende Zielgruppe auf **[!UICONTROL Include]** , um sie auszuwählen.

      Wenn Sie mehrere [!DNL Adobe] Zielgruppen auswählen, wird für jede eine separate [!DNL Google] erstellt.

   1. Wählen Sie die zu erstellende **[!UICONTROL Audience Type]** aus: **[!UICONTROL Customer List_User ID]**.

      Das [!DNL Google Ads] Konto des Werbetreibenden muss ([&#x200B; für benutzerdefinierte Übereinstimmung) &#x200B;](https://support.google.com/adspolicy/answer/6299717) und für das (Benutzer[ID Remarketing) &#x200B;](https://support.google.com/google-ads/answer/9199250).

   1. Aktivieren Sie das Kontrollkästchen, um anzugeben, dass Sie mit den Bedingungen der Datenschutzrichtlinien für [!DNL Adobe] und Werbenetzwerke einverstanden sind.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]** an, d. h. die Anzahl der Tage, die das Cookie eines Benutzers in der Zielgruppe verbleibt.

      Verwenden Sie die Zeitspanne, für die Ihre Anzeige für den Benutzer relevant sein soll. Remarketing-Listen haben eine maximale Dauer von 540 Tagen. Kundenlisten haben keine maximale Dauer. Um anzugeben, dass das Cookie nie abläuft, geben Sie 10000 ein.

   1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] kann bis zu 24 Stunden dauern, um die Datei zu verarbeiten.
>
>* Siehe [[!DNL Google Ads] Dokumentation zur Funktionsweise von Customer Match und zu Einschränkungen](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Erstellen einer Zielgruppe  [!DNL Google Ads]  Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Audiences verwalten](audience-dynamic-remarketing-manage.md)
