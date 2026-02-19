---
title: Verwalten von Feed-Vorlagen
description: Erfahren Sie, wie Sie Feed-Vorlagen verwalten.
feature: Creative Dynamic Creatives
exl-id: 63f8af87-639c-45c8-b17f-99ce19594d35
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Verwalten von Feed-Vorlagen

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Feed-Vorlagen ordnen Felder in Ihren Feed-Dateien/Katalogen den Feldern im Advertising Creative-Backend zu. Dynamische HTML5- und Videoanzeigen, jedoch keine statischen HTML5-Anzeigen, erfordern eine Feed-Vorlage, um dynamische Anzeigen zu erstellen. Optional können Sie universelle Feed-Vorlagen ([!UICONTROL Retail] für Einzelhandelskampagnen und [!UICONTROL Adobe Creative Template] für jeden Kampagnentyp) herunterladen und ausfüllen.

Sie können eine Feed-Vorlage mit mehreren Anzeigenvorlagen verwenden.

>[!TIP]
>
>Für alle Konten mit dynamischen Videos empfiehlt es sich, [ universellen Feed-Vorlagen-[!UICONTROL Adobe Creative Template]](feed-template-manage.md) herunterzuladen, jedes Feld in der Asset-Datei einem Feld im Advertising Creative-Backend zuzuordnen und dann die Feed-Vorlage umzubenennen und hochzuladen. Verwenden Sie die neue Feed-Vorlage zusammen mit der Asset-Datei, um [Katalog zu erstellen](catalog-manage.md).

## Erstellen einer Feed-Vorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Klicken Sie oben rechts auf **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Geben Sie die [Feed-Vorlageneinstellungen](#feed-template-settings) an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten einer Feed-Vorlage

**Hinweis:** Sie können nur von Ihnen erstellte Feed-Vorlagen bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Duplicate]**.

1. Bearbeiten Sie [Feed-Vorlageneinstellungen](#feed-template-settings) nach Bedarf.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Anzeigen einer Feed-Vorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL View]**.

## Duplizieren einer Feed-Vorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Duplicate]**.

1. Geben Sie im Bildschirm [!UICONTROL Duplicate Template] eine eindeutige **[!UICONTROL Template Name]** ein. Wenn Sie eine von einer anderen Person erstellte Vorlage duplizieren, wählen Sie die **[!UICONTROL Advertiser]** aus. Bearbeiten Sie bei Bedarf [ anderen Einstellungen ](#feed-template-settings)Feed-Vorlage).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Herunterladen einer Feed-Vorlage

Heruntergeladene Feed-Vorlagen sind im ZIP-Format von Microsoft Excel-Tabellen (XLSX) verfügbar.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Download]**.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

## Einstellungen der Feed-Vorlage {#feed-template-settings}

### [!UICONTROL General]

**[!UICONTROL Template Name]:** Ein eindeutiger Vorlagenname für den angegebenen Advertiser.

**[!UICONTROL Advertiser]:** Der Werbetreibende, der die Vorlage verwenden kann.

**[!UICONTROL Description]:** (Optional) Informationen, die für alle Benutzer der Feed-Vorlage hilfreich sind.

### [!UICONTROL Field Mapping]

Ordnen Sie jedes Feld in der Feed-Datei einem Feld im Advertising Creative-Backend zu. Unter [Verfügbare Felder für dynamische Ad-Feed-](/help/creative/appendix-available-feed-fields.md)&quot; finden Sie eine Liste der Backend-Felder und der erforderlichen Attribute.<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

Mindestens ein Feld der Feed-Datei muss als &quot;[!UICONTROL Is Unique]&quot; markiert sein. Um eine Feldzuordnung hinzuzufügen, klicken Sie auf **[!UICONTROL +]**. Um die letzte Feldzuordnung zu entfernen, klicken Sie auf **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** Das Feld in der Feed-Datei.

**[!UICONTROL Description]:** (Optional) Informationen, die für alle Benutzer der Feed-Vorlage hilfreich sind.

**[!UICONTROL Is Unique]:** Gibt an, dass das Feld eine eindeutige ID (Schlüssel) ist. Mindestens ein Feld pro Feed-Vorlage muss eindeutig sein. Um diese Option auszuwählen, klicken Sie auf die Schaltfläche, um sie nach rechts zu verschieben.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** Das [Feld im Advertising Creative-Backend](/help/creative/appendix-available-feed-fields.md) das dem angegebenen [!UICONTROL Field Name] in der Feed-Datei zugeordnet wird.

>[!MORELIKETHIS]
>
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Asset-Dateien](/help/creative/feeds/asset-manage.md)
>* [Kataloge verwalten](/help/creative/feeds/catalog-manage.md)
>* [Verfolgen Sie den Status von Katalogverarbeitungsaufträgen](/help/creative/feeds/job-status-track.md)
>* [Verwalten dynamischer Anzeigenvorlagen](/help/creative/ad-templates/ad-template-manage.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](/help/creative/creative-libraries/creative-add-dynamic.md)
