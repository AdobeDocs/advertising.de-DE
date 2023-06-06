---
title: Verwalten [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppen
description: Erfahren Sie, wie Sie [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Verwalten [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppen

*[!DNL Microsoft Advertising]Nur Konten*

Sie können eine [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppe, wenn Sie das JavaScript-Konversions- und Zielgruppen-Tracking-Tag der Suchmaschine auf Ihren Webseiten verwenden. Jede Zielgruppe wird mithilfe eines bestimmten Tags erstellt, das in den Webseiten enthalten ist, deren Benutzer die Zielgruppe enthalten werden. Sie können mehrere Zielgruppen mit demselben Tracking-Tag erstellen. Sie können auch den Namen und die Datenquelle für bestehende Zielgruppen ändern oder vorhandene Zielgruppen löschen.

Zielgruppen für dynamisches Remarketing haben den Zielgruppentyp &quot;[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot;(z. B. &quot;Dynamische Remarketing-Käufer in der Vergangenheit&quot;).

Weitere Informationen zum dynamischen Remarketing und zur Implementierung des erforderlichen JavaScript-Tags finden Sie unter [[!DNL Microsoft Advertising] Dokumentation zum dynamischen Remarketing](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Dynamische Remarketing-Zielgruppe erstellen

>[!NOTE]
>
>Für [!DNL Microsoft Advertising] Konten, muss das JavaScript-Tag die [Produkt-ID und Seitentypparameter](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifizieren Sie den Namen der [!DNL Microsoft Advertising] Universal Event Tracking (UET)-Tag, das in den Webseiten enthalten ist, von denen aus die Zielgruppe erstellt wird.

   Sie benötigen den Tag-Namen in einem späteren Schritt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Im **[!UICONTROL Data Source]** Menü auswählen **[!UICONTROL Dynamic Remarketing List]**.

   1. Geben Sie die **[!UICONTROL Audience Name]**.

   1. Wählen Sie aus einer Liste aller verfügbaren Tags für das Suchmaschinenkonto den Namen der [!DNL Microsoft Advertising] UET-Tag, das auf den Webseiten enthalten ist, deren Benutzer die Zielgruppe enthalten werden.

   1. Wählen Sie den Besuchertyp für die Zielgruppe aus, der auf den Besucheraktionen auf den relevanten Webseiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Geben Sie die Anzahl der **[!UICONTROL Membership Days]**: die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt. Die Werte können zwischen 1 (1) und 180 liegen.

      Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist.

1. Klicken **[!UICONTROL Post]**.

>[!NOTE]
>
>Ihre [!DNL Microsoft Advertising] Dynamische Remarketing-Listen sind für Targeting qualifiziert, sobald sie mindestens 300 Benutzer umfassen.

## Dynamische Remarketing-Zielgruppe bearbeiten

Sie können den Namen und die Datenquelle für eine [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppe. Sie können den Wert der [!UICONTROL Membership Days] -Einstellung.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der zu bearbeitenden Audience.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die Zielgruppeninformationen:

   1. Im **[!UICONTROL Data Source]** Abschnitt, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

   1. (Optional) Ändern Sie die **[!UICONTROL Audience Name]**.

   1. (Optional) Ändern Sie in einer Liste aller verfügbaren Tags für das Anzeigennetzwerkkonto den Namen der [!DNL Microsoft Advertising] UET-Tag, das auf den Webseiten enthalten ist, deren Benutzer die Zielgruppe enthalten werden.

   1. (Optional) Ändern Sie den Besuchertyp für die Zielgruppe, der auf den Besucheraktionen auf den relevanten Webseiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klicken **[!UICONTROL Post]**.

## Dynamische Remarketing-Zielgruppe löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben den zu löschenden Zielgruppen.

   Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] Kundenabgleich-Zielgruppen aus [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen Sie eine [!DNL Google Ads] Zielgruppe für Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)

