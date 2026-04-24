---
title: Zielgruppen  [!DNL Google Ads]  Kundenabgleich aus Zielgruppen  [!DNL Adobe]  Zielgruppen erstellen
description: Erfahren Sie, wie Sie  [!DNL Google Ads]  Ihren bestehenden Adobe Analytics- und Audience Manager-Zielgruppen Kundenabgleich erstellen.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/Ep3X-eo2kcGlW3NsV3CJEKBkEapa-oAv0HLexc1xnhM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 0%

---

# Erstellen [!DNL Google Ads] Zielgruppen für den Kundenabgleich aus Adobe Analytics- und Audience Manager-Zielgruppen

*[!DNL Google Ads]Konten, die nur für den Kundenabgleich infrage kommen*

*Werbetreibende nur mit einer Adobe Advertising-Adobe Audience Manager- oder Adobe Advertising-Adobe Analytics-Integration*

[!DNL Google Ads] Opt-in-Werbetreibende können Zielgruppen für den Kundenabgleich erstellen, indem sie Benutzer-IDs aus a) [!DNL Analytics] Segmenten verwenden, die für Adobe CX Enterprise freigegeben sind, und b) Audience Manager-Segmenten, die Search, Social und Commerce als Ziel haben, einschließlich [!DNL Analytics] Segmenten, die für Adobe CX Enterprise veröffentlicht wurden, und Segmenten, die mit der Adobe CX Enterprise-Zielgruppenbibliothek erstellt wurden. Search, Social und Commerce sendet automatisch eine [!DNL Google] Tracking-URL zurück an jedes [!DNL Analytics]- oder Audience Manager-Segment, damit [!DNL Google] die Audience verfolgen können.

Jede [!DNL Adobe] Zielgruppe kann nur für eine [!DNL Google] Zielgruppe verwendet werden.

Jede neue [!DNL Google] Zielgruppe hat denselben Namen wie die ursprüngliche [!DNL Adobe] Zielgruppe. [!DNL Google] bestimmt, wie groß die Zielgruppe sein muss, damit sie anvisiert werden kann.

>[!TIP]
>
>Verwenden Sie für die Echtzeit-Segmentierung von Audience Manager erstellte Zielgruppen. Segmente, die in [!DNL Analytics] erstellt und mit Adobe CX Enterprise synchronisiert wurden, können kleinere Populationen haben, da sie nur täglich synchronisiert werden. Ein Surfer, der für ein Segment qualifiziert ist, kann erst am nächsten Tag in das Segment aufgenommen werden. Segmente aus [!DNL Analytics] haben die Datenquelle „Report Suite - &quot;.

>[!NOTE]
>
>Search, Social und Commerce speichern keine Kundendaten aus Ihren [!DNL Adobe] Segmenten, die zum Erstellen oder Bearbeiten einer [!DNL Google] Zielgruppe verwendet werden.

1. Schließen Sie die Voraussetzungen nach Bedarf ab:

   1. (Um Benutzer-ID-Remarketing-Listen-Zielgruppen zu erstellen) Ein [!DNL Adobe]-Admin-Benutzer oder Account Manager muss die Einstellung auf Advertiser-Ebene auswählen, um Zielgruppen für den Kundenabgleich zu aktivieren.

   1. Implementieren Sie [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) Version 2.0 oder höher.

   1. Stellen Sie das folgende Tag so hoch wie möglich auf den Webseiten des Werbetreibenden bereit, von denen aus die Zielgruppe verfolgt werden soll

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      wobei `Advertising_Cloud_UserID` die eindeutige numerische Benutzer-ID ist, die dem Advertiser zugewiesen ist.

      Beispiel: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Wenn dies noch nicht abgeschlossen ist) Ein autorisierter Benutzer muss das Konto des Werbetreibenden so konfigurieren, [&#x200B; es mit dem Organisationskonto des Werbetreibenden in Adobe CX Enterprise synchronisiert &#x200B;](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im **[!UICONTROL Data Source]** Menü **[!UICONTROL Adobe Audience]** aus.

   1. Select the [!UICONTROL Adobe Audience] on which to base the [!DNL Google] audience.

      >[!NOTE]
      >
      >[!DNL Adobe] audiences that are already used for another [!DNL Google] audience aren&#39;t available.

      You can optionally search for audiences that contain a specific text string with a minimum of three characters. For any matching audience, click **[!UICONTROL Include]** to select it.

      If you select multiple [!DNL Adobe] audiences, then a separate [!DNL Google] audience is created for each.

   1. Select the **[!UICONTROL Audience Type]** to create: **[!UICONTROL Customer List_User ID]**.

      The advertiser&#39;s [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID remarketing](https://support.google.com/google-ads/answer/9199250).

   1. Select the check box to indicate that you agree with the terms of the [!DNL Adobe] and ad network privacy policies.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]** an, d. h. die Anzahl der Tage, die das Cookie eines Benutzers in der Zielgruppe verbleibt.

      Verwenden Sie die Zeitspanne, für die Ihre Anzeige für den Benutzer relevant sein soll. Remarketing lists have a maximum duration of 540 days. Customer lists don&#39;t have a maximum duration; to indicate that the cookie never expires, enter 10000.

   1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] may take up to 24 hours to process the file.
>
>* See [[!DNL Google Ads] documentation on how customer match works and limitations](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Erstellen einer Zielgruppe  [!DNL Google Ads]  Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
>* [Dynamische Remarketing-Audiences verwalten](audience-dynamic-remarketing-manage.md)
