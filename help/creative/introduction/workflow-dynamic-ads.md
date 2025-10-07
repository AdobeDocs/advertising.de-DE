---
title: Workflows für dynamische Anzeigen
description: Erfahren Sie mehr über die Workflows zum Verwalten dynamischer Anzeigen.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Workflows für dynamische Anzeigen

*Benutzer mit Berechtigungen zum Erstellen dynamischer Anzeigen*

Sie können dynamische Anzeigen auf zwei Arten einrichten:

* Workflow 1: Laden Sie eine Anzeigenvorlage und einen Anzeigenvariantenkatalog direkt in die dynamischen Anzeigeneinstellungen hoch, wenn Sie dynamische Anzeigen zu einer Kreativbibliothek hinzufügen. Sie können eine vorhandene Feed-Vorlage herunterladen, um den Katalog zu erstellen.

  Verwenden Sie diesen Workflow, wenn dieselbe Person alle Informationen (mit Ausnahme der Feed-Vorlage) bereitstellen kann, um die Anzeigen zu erstellen. Die hochgeladenen Dateien bleiben für die zukünftige Verwendung verfügbar.

* Workflow 2: Richten Sie eine Anzeigenvorlage und Anzeigenvariantenkataloge in separaten Ansichten ein und fügen Sie dann einem Kreativen mithilfe der bereits verfügbaren Anzeigenvorlage und Kataloge separat dynamische Anzeigen hinzu.

  Verwenden Sie diesen Workflow, wenn mehrere Personen verschiedene Aufgaben ausführen oder wenn Sie jeweils nur eine Aufgabe ausführen möchten.

## Workflow 1

>[!PREREQUISITES]
>
>* Anzeigenvorlagen im HTML5-Format
>* Produktkataloge im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX)

1. [Dynamische Kreative erstellen](/help/creative/creative-libraries/creative-add-dynamic.md) für eine Kreativbibliothek. Laden Sie für dynamische HTML5-Anzeigen eine Anzeigenvorlage und Kataloge hoch.

1. Verwenden Sie die dynamischen Kreativen für Anzeigen-Erlebnisse:

   1. [Erstellen dynamischer Anzeigenpakete](/help/creative/creative-libraries/bundle-manage.md) die Sie gleichzeitig an ein Anzeigenerlebnis anhängen können.

   1. Erstellen Sie dynamische Anzeigenerlebnisse [mit &#x200B;](/help/creative/experiences/experience-create-targeting.md) oder [ohne Targeting](/help/creative/experiences/experience-create-no-targeting.md) und [weisen Sie den Erlebnissen die Kreativ-Bundles zu](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Erstellen und Implementieren von Anzeigen-Erlebnis-](/help/creative/experiences/experience-tag-export.md), um sie als Anzeigen in Ihrer DSP auszuführen.

      Um ein Anzeigen-Erlebnis als Anzeige in Adobe Advertising DSP zu verwenden, laden Sie das Anzeigen-Erlebnis-Tag in eine Advertising DSP-Kampagne hoch. Um ein Anzeigen-Erlebnis als Anzeige in einer anderen DSP zu verwenden, implementieren Sie das Anzeigen-Erlebnis-Tag in dieser DSP.

## Workflow 2

1. [Erstellen Sie eine &#x200B;](/help/creative/ad-templates/ad-template-manage.md) für Ihre dynamischen Anzeigen basierend auf den verfügbaren Assets. Die Anzeigenvorlage enthält eine HTML5-Datei mit dem gewünschten Anzeigenformat und (nur für dynamische HTML5-Anzeigen) eine -Datei mit den Anzeigenattributen.

1. Werbeelemente einrichten:

   * (Für einzelne statische HTML5-Anzeigen) Erfassen und [laden Sie die Bild-Assets &#x200B;](/help/creative/feeds/asset-manage.md) Ihre Anzeigen hoch.

   * (Für dynamische HTML5-Anzeigen) Erstellen Sie Kataloge Ihrer Werbeelemente:

      1. Erstellen Sie eine Feed-Datei im XLSX-Format (Microsoft Excel Spreadsheet) mit einer Zeile für jede Anzeigenvariante. Fügen Sie in jeder Zeile einen Bildnamen ein. Erfassen Sie die zugehörigen Bild-Assets separat.

      1. [Laden Sie die Feed-Datei und Bild-Assets hoch](/help/creative/feeds/asset-manage.md).

      1. [Erstellen Sie eine Feed](/help/creative/feeds/feed-template-manage.md)Vorlage, um die Felder in Ihrer Feed-Datei (Kalkulationstabelle) den Feldern im Advertising Creative-Backend zuzuordnen.

      1. [Erstellen Sie einen &#x200B;](/help/creative/feeds/catalog-manage.md#feed-catalog-create) aus einer angegebenen Feed-Datei und einer angegebenen Feed-Vorlage und [verarbeiten Sie dann den Katalog](/help/creative/feeds/catalog-manage.md#feed-catalog-process) um die Anzeigenvarianten anzuzeigen, die daraus erstellt werden können.

         Jede Feed-Datei kann nur für einen Katalog verwendet werden.

         Sie können [&#x200B; Status von Katalogverarbeitungsaufträgen &#x200B;](/help/creative/feeds/job-status-track.md) der Registerkarte [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] verfolgen.

1. [Dynamische Kreative erstellen](/help/creative/creative-libraries/creative-add-dynamic.md) für eine Kreativbibliothek. Verwenden Sie für dynamische HTML5-Anzeigen eine bestimmte Anzeigenvorlage und bestimmte Kataloge.

1. Verwenden Sie die dynamischen Kreativen für Anzeigen-Erlebnisse:

   1. [Erstellen dynamischer Anzeigenpakete](/help/creative/creative-libraries/bundle-manage.md) die Sie gleichzeitig an ein Anzeigenerlebnis anhängen können.

   1. Erstellen Sie dynamische Anzeigenerlebnisse [mit &#x200B;](/help/creative/experiences/experience-create-targeting.md) oder [ohne Targeting](/help/creative/experiences/experience-create-no-targeting.md) und [weisen Sie den Erlebnissen die Kreativ-Bundles zu](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Erstellen und Implementieren von Anzeigen-Erlebnis-](/help/creative/experiences/experience-tag-export.md), um sie als Anzeigen in Ihrer DSP auszuführen.

      Um ein Anzeigen-Erlebnis als Anzeige in Adobe Advertising DSP zu verwenden, laden Sie das Anzeigen-Erlebnis-Tag in eine Advertising DSP-Kampagne hoch. Um ein Anzeigen-Erlebnis als Anzeige in einer anderen DSP zu verwenden, implementieren Sie das Anzeigen-Erlebnis-Tag in dieser DSP.
