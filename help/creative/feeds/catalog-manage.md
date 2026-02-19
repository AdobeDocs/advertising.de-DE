---
title: Verwalten von Feed-Katalogen
description: Erfahren Sie, wie Sie Feed-Kataloge verwalten.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Verwalten von Feed-Katalogen

Verarbeitete Feed-Kataloge sind Gruppen von potenziellen und Varianten, die aus einer bestimmten Feed-Datei und einer bestimmten Feed-Vorlage erstellt wurden. Für dynamische HTML5- und Videoanzeigen, jedoch nicht für statische HTML5-Anzeigen, ist ein Katalog erforderlich, um dynamische Anzeigen zu erstellen.

Bevor Sie Anzeigenvarianten erstellen und [dynamische Anzeigen zu einer Kreativbibliothek hinzufügen können](/help/creative/creative-libraries/creative-add-dynamic.md) verarbeiten Sie den Katalog. Sie können die Feed-Datei später aktualisieren und den Katalog erneut verarbeiten, um einen neuen Satz von Anzeigenvarianten zu erstellen.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Jede Feed-Datei kann bis zu 500 Zeilen mit Video-Assets verarbeiten.

>[!TIP]
>
>Für alle Konten mit dynamischen Videos empfiehlt es sich, [ universellen Feed-Vorlagen-[!UICONTROL Adobe Creative Template]](feed-template-manage.md) herunterzuladen, jedes Feld in der Asset-Datei einem Feld im Advertising Creative-Backend zuzuordnen und dann die Feed-Vorlage umzubenennen und hochzuladen. Verwenden Sie die neue Feed-Vorlage zusammen mit der Asset-Datei, um einen Katalog zu erstellen.

## Erstellen eines Katalogs {#feed-catalog-create}

>[!NOTE]
>
>Sie können einen Katalog auch direkt hochladen, wenn Sie [dynamische Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-dynamic.md). Alle dort erstellten Kataloge werden in der [!UICONTROL Catalogs] für die zukünftige Verwendung verfügbar.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Catalog]** .

1. Klicken Sie oben rechts auf **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Geben Sie die [Katalogeinstellungen](#catalog-settings) nach Bedarf an.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die potenziellen Anzeigenvarianten, die für den Katalog erstellt werden können.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten eines Katalogs

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Catalog]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie [Katalogeinstellungen](#catalog-settings) nach Bedarf.

1. Überprüfen Sie die potenziellen Anzeigenvarianten, die für den Katalog erstellt werden können.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Verarbeiten eines Katalogs {#feed-catalog-process}

Durch die Verarbeitung eines Katalogs werden die Anzeigenvarianten verfügbar, um dynamische HTML5-Anzeigen zu erstellen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Catalog]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Run Now]**.

## Aktiven Katalog pausieren

Katalog pausieren, um ihn inaktiv zu machen.<!-- Can you Activate it again? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Aktivieren eines angehaltenen Katalogs

<!-- Verify if this is available. -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Activate]**.

## Archivieren eines Katalogs

Archivieren Sie einen Katalog, um ihn zu löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **[!UICONTROL Archive]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Archive]**.

## Katalogeinstellungen {#catalog-settings}

**[!UICONTROL Advertiser]:** Der Werbetreibende, der den Katalog verwenden kann.

**[!UICONTROL Asset]:** Die Feed-Datei, die als Eingabe für den Katalog verwendet werden soll.

**[!UICONTROL Catalog Name]:** Ein eindeutiger Katalogname für den angegebenen Advertiser. Standardmäßig wird der Name der Feed-Datei verwendet, einschließlich der Dateierweiterung. Dies ist die Best Practice zur Identifizierung.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** Die Feed-Vorlage, die für die Zuordnung von Feldern in der angegebenen Asset-/Feed-Datei zu Feldern im Advertising Creative-Backend verwendet werden soll.

>[!MORELIKETHIS]
>
>* [Verfolgen Sie den Status von Katalogverarbeitungsaufträgen](/help/creative/feeds/job-status-track.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Asset-Dateien](/help/creative/feeds/asset-manage.md)
>* [Verwalten von Feed-Vorlagen](/help/creative/feeds/feed-template-manage.md)
>* [Verwalten dynamischer Anzeigenvorlagen](/help/creative/ad-templates/ad-template-manage.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](/help/creative/creative-libraries/creative-add-dynamic.md)
