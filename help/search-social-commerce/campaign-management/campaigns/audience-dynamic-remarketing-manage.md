---
title: Dynamische Remarketing-Zielgruppen verwalten [!DNL Microsoft Advertising]
description: Erfahren Sie, wie Sie dynamische Remarketing-Zielgruppen erstellen und verwalten. [!DNL Microsoft Advertising]
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Dynamische Remarketing-Zielgruppen verwalten [!DNL Microsoft Advertising]

*[!DNL Microsoft Advertising]nur Konten*

Sie können eine dynamische Remarketing-Zielgruppe vom Typ [!DNL Microsoft Advertising] erstellen, wenn Sie das JavaScript-Konversions- und Zielgruppen-Tracking-Tag der Suchmaschine auf Ihren Webseiten verwenden. Jede Zielgruppe wird mithilfe eines bestimmten Tags erstellt, das in den Webseiten enthalten ist, deren Benutzer die Zielgruppe bilden. Sie können mehrere Zielgruppen mit demselben Tracking-Tag erstellen. Sie können auch den Namen und die Datenquelle für bestehende Zielgruppen ändern oder vorhandene Zielgruppen löschen.

Zielgruppen für dynamisches Remarketing haben den Zielgruppentyp &quot;[!UICONTROL Dynamic Remarketing] \&lt;Besuchertyp\>&quot;(z. B. &quot;Dynamische Remarketing-Angebote für vergangene Käufer&quot;).

Weitere Informationen zum dynamischen Remarketing und zur Implementierung des erforderlichen JavaScript-Tags finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zum dynamischen Remarketing](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Dynamische Remarketing-Zielgruppe erstellen

>[!NOTE]
>
>Für [!DNL Microsoft Advertising] -Konten muss das JavaScript -Tag die Parameter [Produkt-ID und Seitentyp](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) enthalten.

1. Identifizieren Sie den Namen des Tags [!DNL Microsoft Advertising] Universal Event Tracking (UET) , das auf den Webseiten enthalten ist, von denen aus die Zielgruppe erstellt wird.

   Sie benötigen den Tag-Namen in einem späteren Schritt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die Zielgruppeninformationen an:

   1. Wählen Sie im Menü **[!UICONTROL Data Source]** die Option **[!UICONTROL Dynamic Remarketing List]** aus.

   1. Geben Sie den Wert **[!UICONTROL Audience Name]** ein.

   1. Wählen Sie aus einer Liste aller für das Suchmaschinenkonto verfügbaren Tags den Namen des Tags [!DNL Microsoft Advertising] UET aus, das auf den Webseiten enthalten ist, deren Benutzer die Zielgruppe enthalten.

   1. Wählen Sie den Besuchertyp für die Zielgruppe aus, der auf den Besucheraktionen auf den relevanten Webseiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Geben Sie die Anzahl von **[!UICONTROL Membership Days]** an, also die Anzahl der Tage, in denen das Cookie eines Benutzers in der Zielgruppe verbleibt. Die Werte können zwischen 1 (1) und 180 liegen.

      Verwenden Sie die Zeitdauer, für die Sie erwarten, dass Ihre Anzeige für den Benutzer relevant ist.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!NOTE]
>
>Dynamische Remarketing-Listen vom Typ [!DNL Microsoft Advertising] sind für Targeting qualifiziert, sobald sie mindestens 300 Benutzer umfassen.

## Dynamische Remarketing-Zielgruppe bearbeiten

Sie können den Namen und die Datenquelle für eine dynamische Remarketing-Zielgruppe vom Typ [!DNL Microsoft Advertising] ändern. Sie können den Wert der Einstellung [!UICONTROL Membership Days] nicht bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Aktivieren Sie das Kontrollkästchen neben der zu bearbeitenden Audience.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die Zielgruppeninformationen:

   1. Klicken Sie im Abschnitt **[!UICONTROL Data Source]** auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

   1. (Optional) Ändern Sie die **[!UICONTROL Audience Name]**.

   1. (Optional) Ändern Sie aus einer Liste aller verfügbaren Tags für das Anzeigennetzwerkkonto den Namen des [!DNL Microsoft Advertising] UET-Tags, das auf den Webseiten enthalten ist, deren Benutzer die Zielgruppe umfassen.

   1. (Optional) Ändern Sie den Besuchertyp für die Zielgruppe, der auf den Besucheraktionen auf den relevanten Webseiten basiert: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* oder *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klicken Sie auf **[!UICONTROL Post]**.

## Dynamische Remarketing-Zielgruppe löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben den zu löschenden Zielgruppen.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Erstellen [!DNL Google Ads] von Kundenabgleichs-Zielgruppen aus  [!DNL Adobe] Zielgruppen](google-audience-from-adobe-audience.md)
>* [Erstellen einer [!DNL Google Ads] Kundenübereinstimmungs-Audience aus einer Adobe Campaign-E-Mail-Liste](google-audience-from-campaign-email-list.md)
>* [Verwalten von Zielgruppen zur Kundenabstimmung mithilfe von Kundendatenlisten](audience-from-customer-data-list.md)
