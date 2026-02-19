---
title: Workflows für dynamische Anzeigen
description: Erfahren Sie mehr über die Workflows zum Verwalten dynamischer Anzeigen.
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '643'
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
>* Anzeigenvorlagen: Eine Anzeigenvorlage (eine ZIP-Datei mit HTML5-Dateien) oder eine Videoanzeigenvorlage (eine ZIP-Datei mit einer Scene-Datei)
>* Produktkataloge im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX)

1. [Dynamische Kreative erstellen](/help/creative/creative-libraries/creative-add-dynamic.md) für eine Kreativbibliothek. Laden Sie für dynamische HTML5- und Videoanzeigen eine vorhandene Anzeigenvorlage und einen vorhandenen Katalog hoch oder wählen Sie diese aus.

1. Verwenden Sie die dynamischen Kreativen für Anzeigen-Erlebnisse:

   1. [Erstellen dynamischer Anzeigenpakete](/help/creative/creative-libraries/bundle-manage.md) die Sie gleichzeitig an ein Anzeigenerlebnis anhängen können.

   1. Erstellen Sie dynamische Anzeigenerlebnisse [mit ](/help/creative/experiences/experience-create-targeting.md) oder [ohne Targeting](/help/creative/experiences/experience-create-no-targeting.md) und [weisen Sie den Erlebnissen die Kreativ-Bundles zu](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Erstellen und Implementieren von Anzeigen-Erlebnis-](/help/creative/experiences/experience-tag-export.md), um sie als Anzeigen in Ihrer DSP auszuführen.

      Um ein Anzeigen-Erlebnis als Anzeige in Adobe Advertising DSP zu verwenden, laden Sie das Anzeigen-Erlebnis-Tag in eine Advertising DSP-Kampagne hoch. Um ein Anzeigen-Erlebnis als Anzeige in einer anderen DSP zu verwenden, implementieren Sie das Anzeigen-Erlebnis-Tag in dieser DSP.

## Workflow 2

1. [Erstellen Sie eine ](/help/creative/ad-templates/ad-template-manage.md) für Ihre dynamischen Anzeigen basierend auf den verfügbaren Assets. Die Anzeigenvorlage muss im ZIP-Format vorliegen und Folgendes enthalten:<!-- Need to add more specs for templates -->

* Kreative anzeigen: HTML5-Dateien mit dem gewünschten Anzeigenformat und (nur für dynamische HTML5-Anzeigen) eine -Datei mit den Anzeigenattributen (.tdf)

* Videokreative: Eine Szenendatei mit dem gewünschten Anzeigenformat und eine Datei mit den Anzeigenattributen (.tdf)

1. Werbeelemente einrichten:

   * (Für einzelne statische HTML5-Anzeigen) Erfassen und [laden Sie die Bild-Assets ](/help/creative/feeds/asset-manage.md) Ihre Anzeigen hoch.

   * (Für dynamische HTML5- und Videoanzeigen) Erstellen Sie Kataloge Ihrer Werbeelemente:

      1. Erstellen Sie eine Feed-Datei im XLSX-Format (Microsoft Excel Spreadsheet) mit einer Zeile für jede Anzeigenvariante. Fügen Sie in jeder Zeile einen Bild- oder Videonamen ein. Erfassen Sie die zugehörigen Bild- und Video-Assets separat.

      1. [Laden Sie die Feed-Datei und die Assets hoch](/help/creative/feeds/asset-manage.md).

      1. [Erstellen Sie eine Feed](/help/creative/feeds/feed-template-manage.md)Vorlage, um die Felder in Ihrer Feed-Datei (Kalkulationstabelle) den Feldern im Advertising Creative-Backend zuzuordnen. Optional können Sie eine universelle Feed-Vorlage mit Feldern herunterladen und ausfüllen, die für jeden Kampagnentyp relevant sind.

      1. [Erstellen Sie einen ](/help/creative/feeds/catalog-manage.md#feed-catalog-create) aus einer angegebenen Feed-Datei und einer angegebenen Feed-Vorlage und [verarbeiten Sie dann den Katalog](/help/creative/feeds/catalog-manage.md#feed-catalog-process) um die Anzeigenvarianten anzuzeigen, die daraus erstellt werden können.

         Jede Feed-Datei kann nur für einen Katalog verwendet werden.

         Sie können [ Status von Katalogverarbeitungsaufträgen ](/help/creative/feeds/job-status-track.md) der Registerkarte [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] verfolgen.

1. [Dynamische Kreative erstellen](/help/creative/creative-libraries/creative-add-dynamic.md) für eine Kreativbibliothek. Verwenden Sie für dynamische HTML5-Anzeigen eine bestimmte Anzeigenvorlage und bestimmte Kataloge.

1. Verwenden Sie die dynamischen Kreativen für Anzeigen-Erlebnisse:

   1. [Erstellen dynamischer Anzeigenpakete](/help/creative/creative-libraries/bundle-manage.md) die Sie gleichzeitig an ein Anzeigenerlebnis anhängen können.

   1. Erstellen Sie dynamische Anzeigenerlebnisse [mit ](/help/creative/experiences/experience-create-targeting.md) oder [ohne Targeting](/help/creative/experiences/experience-create-no-targeting.md) und [weisen Sie den Erlebnissen die Kreativ-Bundles zu](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Erstellen und Implementieren von Anzeigen-Erlebnis-](/help/creative/experiences/experience-tag-export.md), um sie als Anzeigen in Ihrer DSP auszuführen.

      Um ein Anzeigen-Erlebnis als Anzeige in Adobe Advertising DSP zu verwenden, laden Sie das Anzeigen-Erlebnis-Tag in eine Advertising DSP-Kampagne hoch. Um ein Anzeigen-Erlebnis als Anzeige in einer anderen DSP zu verwenden, implementieren Sie das Anzeigen-Erlebnis-Tag in dieser DSP.
