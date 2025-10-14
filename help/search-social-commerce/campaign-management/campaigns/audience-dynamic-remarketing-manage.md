---
title: Verwalten [!DNL Microsoft Advertising] dynamischer Remarketing-Audiences
description: Erfahren Sie, wie Sie dynamische Remarketing [!DNL Microsoft Advertising] Zielgruppen erstellen und verwalten.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Verwalten [!DNL Microsoft Advertising] dynamischen Remarketing-Audiences

Nur *[!DNL Microsoft Advertising]Konten*

Sie können eine [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppe erstellen, wenn Sie das Konversions- und Zielgruppen-Tracking-Tag der Suchmaschine für JavaScript auf Ihren Web-Seiten verwenden. Jede Zielgruppe wird mit einem angegebenen Tag erstellt, das in den Web-Seiten enthalten ist, aus deren Benutzern die Zielgruppe besteht. Sie können mehrere Zielgruppen mit demselben Tracking-Tag erstellen. Sie können auch den Namen und die Datenquelle für vorhandene Zielgruppen ändern oder vorhandene Zielgruppen löschen.

Dynamische Remarketing-Zielgruppen haben den Zielgruppentyp &quot;[!UICONTROL Dynamic Remarketing] \&lt;Besuchertyp\>&quot; (z. B. „Dynamisches Remarketing für frühere Käufer„).

Weitere Informationen zu dynamischem Remarketing und zur Implementierung des erforderlichen JavaScript-Tags finden Sie unter [[!DNL Microsoft Advertising] Dokumentation zu dynamischem Remarketing](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Erstellen einer dynamischen Remarketing-Zielgruppe

>[!NOTE]
>
>Bei [!DNL Microsoft Advertising]-Konten muss das JavaScript-Tag die [Produkt-ID und Seitentypparameter“ &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Geben Sie den Namen des [!DNL Microsoft Advertising] UET-Tags (Universal Event Tracking) an, das in den Web-Seiten enthalten ist, von denen aus die Zielgruppe erstellt wird.

   Sie benötigen den Tag-Namen in einem späteren Schritt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im **[!UICONTROL Data Source]** Menü **[!UICONTROL Dynamic Remarketing List]** aus.

   1. Geben Sie die **[!UICONTROL Audience Name]** ein.

   1. Wählen Sie aus einer Liste aller verfügbaren Tags für das Suchmaschinenkonto den Namen des [!DNL Microsoft Advertising] UET-Tags aus, das in den Web-Seiten enthalten ist, aus deren Benutzern die Zielgruppe besteht.

   1. Wählen Sie den Besuchertyp für die Zielgruppe aus, der auf Besucheraktionen auf den entsprechenden Web-Seiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]** an, d. h. die Anzahl der Tage, die das Cookie eines Benutzers in der Zielgruppe verbleibt. Die Werte können zwischen 1 und 180 liegen.

      Verwenden Sie die Zeitspanne, für die Ihre Anzeige für den Benutzer relevant sein soll.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>Ihre [!DNL Microsoft Advertising] dynamischen Remarketing-Listen sind für das Targeting geeignet, sobald sie mindestens 300 Benutzer enthalten.

## Bearbeiten einer dynamischen Remarketing-Zielgruppe

Sie können den Namen und die Datenquelle für eine [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppe ändern. Der Wert der [!UICONTROL Membership Days] kann nicht bearbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der Audience, die Sie bearbeiten möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die Zielgruppeninformationen:

   1. Klicken Sie im Abschnitt **[!UICONTROL Data Source]** auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

   1. (Optional) Ändern Sie die **[!UICONTROL Audience Name]**.

   1. (Optional) Ändern Sie aus einer Liste aller verfügbaren Tags für das Anzeigennetzwerkkonto den Namen des [!DNL Microsoft Advertising] UET-Tags, das in den Web-Seiten enthalten ist, aus denen die Benutzenden die Audience bilden.

   1. (Optional) Ändern Sie den Besuchertyp für die Zielgruppe, der auf Besucheraktionen auf den entsprechenden Web-Seiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klicken Sie auf **[!UICONTROL Post]**.

## Löschen einer dynamischen Remarketing-Zielgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu löschenden Zielgruppe.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich von Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen einer Zielgruppe  [!DNL Google Ads]  Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen für den Kundenabgleich mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
