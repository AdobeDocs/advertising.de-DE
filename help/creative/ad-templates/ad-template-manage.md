---
title: Verwalten dynamischer Anzeigenvorlagen
description: Erfahren Sie, wie Sie dynamische Anzeigenvorlagen verwalten und daraus Anzeigen erstellen.
feature: Creative Templates
exl-id: 248f1467-ebd3-47f2-a24c-043bbfadcc6e
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Verwalten dynamischer Anzeigenvorlagen

Erstellen Sie eine separate Anzeigenvorlage für jede Kombination aus Anzeigentyp (static HTML5 oder dynamic HTML5) und Anzeigengröße, indem Sie eine komprimierte HTML5-Datei mit dem gewünschten Anzeigenformat hochladen. Bei dynamischen HTML5-Anzeigen können Sie auch eine Datei hochladen, die die Anzeigenattribute enthält<!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Erstellen einer dynamischen Anzeigenvorlage

>[!NOTE]
>
>Sie können auch eine dynamische Anzeigenvorlage hochladen, wenn Sie [dynamische Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-dynamic.md). Alle dort erstellten Anzeigenvorlagen werden in der [!UICONTROL Ad Templates] für die zukünftige Verwendung verfügbar.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create Ad Template]**

1. Geben Sie die [Anzeigenvorlageneinstellungen an](#ad-template-settings)

1. Klicken Sie auf **[!UICONTROL Create]**.

## Bearbeiten einer dynamischen Anzeigenvorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Halten Sie den Cursor über die Zeile mit der Anzeigenvorlage und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Anzeigenvorlageneinstellungen](#ad-template-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Dynamische Anzeigenvorlage herunterladen

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Halten Sie den Cursor über die Zeile mit der Anzeigenvorlage und klicken Sie auf **[!UICONTROL Download]**.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

## Löschen einer dynamischen Anzeigenvorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Halten Sie den Cursor über die Zeile mit der Anzeigenvorlage und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Erstellen dynamischer Anzeigen aus einer Anzeigenvorlage

>[!NOTE]
>
>Sie können auch [dynamische Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-dynamic.md) aus einer Kreativbibliothek heraus.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Halten Sie den Cursor über die Zeile mit der Anzeigenvorlage und klicken Sie auf **[!UICONTROL Create Dynamic Ad]**.

   Im [!UICONTROL New Dynamic Ad] werden die Felder [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type] und [!UICONTROL Ad Template] automatisch ausgewählt und schreibgeschützt.

1. Geben Sie die Einstellungen für dynamische Anzeigen an[&#x200B; um die dynamischen Anzeigen zu erstellen](/help/creative/creative-libraries/creative-add-dynamic.md).

## Einstellungen für Anzeigenvorlagen {#ad-template-settings}

### Details zur Anzeigenvorlage

**[!UICONTROL Advertiser]**: (Schreibgeschützt für vorhandene Vorlagen) Der Advertiser, für den Anzeigen generiert werden.

**[!UICONTROL Ad Template Name]**: Ein eindeutiger Name der Anzeigenvorlage für den Advertiser.

**[!UICONTROL Ad Template Type]**: (Schreibgeschützt für vorhandene Vorlagen) Das Anzeigenvorlagenformat: *Static HTML5* oder *Dynamic HTML5*.

**[!UICONTROL Ad Template Size]**: (Schreibgeschützt für vorhandene Vorlagen) Die Dimensionen der von der Vorlage erstellten Anzeigen.

**[!UICONTROL Description]**: (Optional) Informationen, die für alle Benutzer der Anzeigenvorlage hilfreich sind.

### (Statische HTML5-Anzeigenvorlagen) Klicken Sie auf Tags

**\[Click Tag Parameter\]**: Die Click-Tag-Parameter, um Weiterleitungen durch Klick-Tracking von Anzeigen zu ermöglichen, die mit der Anzeigenvorlage erstellt wurden. Um einen Parameter hinzuzufügen, klicken Sie auf **[!UICONTROL + Add More]** und geben Sie einen zusätzlichen Parameter ein. Sie können bis zu fünf Parameter einbeziehen.

### HTML5-Postleitzahl

Eine komprimierte HTML5-Datei mit dem gewünschten Anzeigenformat. Wenn Sie bereits eine Datei hochgeladen haben, wird der Dateiname aufgelistet.

Siehe die [HTML5 Creative Specification](/help/creative/creative-libraries/html5-creative-specification.md).

Hochladen einer Datei:

1. Klicken Sie auf **[!UICONTROL Upload HTML5 zip]**.

1. Suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.

### (Dynamische HTML5-Anzeigenvorlagen) Attributdatei

<!-- EXPLAIN and ad specs below for this file type -->Eine Datei, die Attribute für die Anzeigenvorlage enthält. Wenn Sie bereits eine Datei hochgeladen haben, wird der Dateiname aufgelistet.

Hochladen einer Datei:

1. Klicken Sie auf **[!UICONTROL Upload Attributes File]**.

1. Suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.

>[!MORELIKETHIS]
>
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Asset-Dateien](/help/creative/feeds/asset-manage.md)
>* [Verwalten von Feed-Vorlagen](/help/creative/feeds/feed-template-manage.md)
>* [Kataloge verwalten](/help/creative/feeds/catalog-manage.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](/help/creative/creative-libraries/creative-add-dynamic.md)
