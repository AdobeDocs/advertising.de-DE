---
title: Workflow für dynamische Anzeigen
description: Erfahren Sie mehr über den Workflow zum Verwalten dynamischer Anzeigen.
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Workflow für dynamische Anzeigen

1. [Erstellen Sie eine Anzeigenvorlage](/help/creative/ad-templates/ad-template-manage.md) für Ihre dynamischen Anzeigen basierend auf den verfügbaren Assets

1. Werbeelemente einrichten:

   * (Für einzelne statische HTML5-Anzeigen) Erfassen und [laden Sie die Bild-Assets ](/help/creative/feeds/asset-manage.md) Ihre Anzeigen hoch.

   * (Für dynamische HTML5-Anzeigen) Erstellen Sie Kataloge Ihrer Werbeelemente:

      1. Erstellen Sie eine Feed-Datei im XLSX-Format (Microsoft Excel Spreadsheet) mit einer Zeile für jede Anzeigenvariante. Fügen Sie in jeder Zeile einen Bildnamen oder einen Verweis auf eine Adobe Experience Manager ein. Erfassen Sie die zugehörigen Bild-Assets separat.

      1. [Laden Sie die Feed-Datei und Bild-Assets hoch](/help/creative/feeds/asset-manage.md).

      1. [Erstellen Sie eine Feed](/help/creative/feeds/feed-template-manage.md)Vorlage, um die Felder in Ihrer Feed-Datei (Kalkulationstabelle) den Feldern im Advertising Creative-Backend zuzuordnen.

      1. [Erstellen Sie einen ](/help/creative/feeds/catalog-manage.md#feed-catalog-create) aus einer angegebenen Feed-Datei und einer angegebenen Feed-Vorlage und [verarbeiten Sie dann den Katalog](/help/creative/feeds/catalog-manage.md#feed-catalog-process) um die Anzeigenvarianten anzuzeigen, die daraus erstellt werden können.

         Jede Feed-Datei kann nur für einen Katalog verwendet werden.

         Sie können [ Status von Katalogverarbeitungsaufträgen ](/help/creative/feeds/job-status-track.md) der Registerkarte [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] verfolgen.

1. [Dynamische Kreative erstellen](/help/creative/creative-libraries/creative-add-dynamic.md) für eine Kreativbibliothek. Verwenden Sie für dynamische HTML5-Anzeigen eine bestimmte Anzeigenvorlage und bestimmte Kataloge.

1. [Erstellen dynamischer Anzeigenpakete](/help/creative/creative-libraries/bundle-manage.md) die Sie gleichzeitig an ein Anzeigenerlebnis anhängen können.

1. Erstellen Sie dynamische Anzeigenerlebnisse mit [mit ](/help/creative/experiences/experience-create-targeting.md) oder [ohne Targeting](/help/creative/experiences/experience-create-no-targeting.md) und [weisen Sie sie Ihren dynamischen Anzeigenerlebnissen zu](/help/creative/experiences/experience-assign-creative-bundles.md).

1. [Erstellen und Implementieren von Anzeigen-Erlebnis-](/help/creative/experiences/experience-tag-export.md), um sie als Anzeigen in Ihrer DSP auszuführen.

   Um ein Anzeigen-Erlebnis als Anzeige in Adobe Advertising DSP zu verwenden, laden Sie das Anzeigen-Erlebnis-Tag in eine Advertising DSP-Kampagne hoch. Um ein Anzeigen-Erlebnis als Anzeige in einer anderen DSP zu verwenden, implementieren Sie das Anzeigen-Erlebnis-Tag in dieser DSP.
