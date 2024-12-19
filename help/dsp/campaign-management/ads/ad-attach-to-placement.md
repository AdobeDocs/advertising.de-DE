---
title: Hinzufügen von Anzeigen zu Platzierungen
description: Erfahren Sie, wie Sie Anzeigen an Platzierungen anhängen.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Hinzufügen von Anzeigen zu Platzierungen

Verwenden Sie die [!UICONTROL Ad Tools], um Anzeigen an Platzierungen anzuhängen, Tracking-Pixel von Drittanbietern an die Anzeigen anzuhängen und vorhandene Tracking-Pixel von Drittanbietern von den Anzeigen zu trennen.

>[!NOTE]
>
>Universelle Videoanzeigen können nur an Platzierungen für universelle Videos angehängt werden.

## [!UICONTROL Ad Tools] öffnen {#ad-tools-open}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Öffnen Sie die [!UICONTROL Ad Tools] auf eine der folgenden Arten:

   * (In der [!UICONTROL Packages]-, [!UICONTROL Placements]- oder [!UICONTROL Ads] Ansicht) Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (In der [!UICONTROL Placements] Ansicht) Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (In der [!UICONTROL Ads] Ansicht) Klicken Sie neben dem Anzeigenamen auf **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   Die Registerkarte [!UICONTROL Attach Ads] ist standardmäßig ausgewählt.

## Hinzufügen von Anzeigen zu Platzierungen {#attach-ads-campaign}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Gehen Sie in der [!UICONTROL Edit]-Unteransicht für jede Gruppe von Anzeigen, die Sie Platzierungen anhängen möchten, wie folgt vor:

   1. (Optional) Suchen Sie bestimmte Platzierungen und Anzeigen auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filtern](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Paket, Platzierungstyp, Platzierungsstatus, Anzeigentyp oder Anzeigenstatus.

      * Suchen Sie über der rechten und der linken Tabelle nach bestimmten Textzeichenfolgen in den Platzierungs- und Anzeigenamen.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Platzierung, an die die Anzeigen angehängt werden sollen.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jeder Anzeige, die Sie an die ausgewählten Platzierungen anhängen möchten.

      Es können nur Anzeigen ausgewählt werden, die für den Platzierungstyp gelten und noch nicht an die ausgewählten Platzierungen angehängt sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Attach]**.

1. (Optional) Um zu den Kampagnendetailansichten zurückzukehren, klicken Sie auf ![Zurück ](/help/dsp/assets/breadcrumb-return.png " Ordner") links neben [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## Anzeigen anzeigen, die Platzierungen angehängt sind {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Wechseln Sie zur Option **[!UICONTROL View]** oben rechts.

1. (Optional) Suchen Sie nach Bedarf bestimmte Platzierungen und Anzeigen:

   * Klicken Sie über der linken Tabelle auf ![Filtern](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Paket, Platzierungstyp, Platzierungsstatus, Anzeigentyp oder Anzeigenstatus.

   * Suchen Sie in der rechten und linken Tabelle nach bestimmten Textzeichenfolgen in der Platzierung oder im Anzeigenamen.

1. Klicken Sie auf eine beliebige Platzierungszeile in der linken Tabelle, um die angehängten Anzeigen in der rechten Tabelle anzuzeigen.

1. (Optional) Um den Platzierungen der Kampagne weitere Anzeigen hinzuzufügen, wechseln Sie zur **[!UICONTROL Edit]** Ansicht oben rechts. Anweisungen finden Sie in Schritt 2 des vorherigen Verfahrens [Anhängen von Anzeigen an ](#attach-ads-campaign)&quot;.

## Anfügen von Tracking-Pixeln von Drittanbietern an Anzeigen in einer Platzierung {#attach-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. In der [!UICONTROL Edit] Unteransicht:

   1. (Optional) Suchen Sie Anzeigen und Pixel von Drittanbietern auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filtern](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

      * Suchen Sie über der rechten und linken Tabelle nach bestimmten Textzeichenfolgen in den Anzeigenamen und Pixelnamen.

   1. (Wenn für die Kampagne keine Tracking-Pixel von Drittanbietern vorhanden sind) Erstellen Sie ein Pixel:

      1. Klicken Sie in der rechten Tabelle auf **[!UICONTROL Create pixel]**.

      1. Legen Sie die Einstellungen fest:

         **[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel zum Auslösen Trigger wird, z. B. *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (Bilddatei mit 1 x 1 Pixel), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

         **[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

         **[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, der Ihnen die Identifizierung des Pixels erleichtert.

         **[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

      1. Klicken Sie auf **[!UICONTROL Save]**.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Anzeige, für die Sie Tracking-Pixel von Drittanbietern anhängen möchten.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jedem Tracking-Pixel eines Drittanbieters, das Sie an die ausgewählten Anzeigen anhängen möchten.

      Es können nur Pixel ausgewählt werden, die noch nicht mit den ausgewählten Anzeigen verbunden sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Attach]**.

1. (Optional) Um zu den Kampagnendetailansichten zurückzukehren, klicken Sie auf ![Zurück ](/help/dsp/assets/breadcrumb-return.png " Ordner") links neben [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## Trennen von Tracking-Pixeln von Drittanbietern von Anzeigen in einer Platzierung {#detach-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. In der [!UICONTROL Edit] Unteransicht:

   1. (Optional) Suchen Sie Anzeigen und Pixel von Drittanbietern auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filtern](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

      * Suchen Sie über der rechten und linken Tabelle nach bestimmten Textzeichenfolgen in den Anzeigenamen und Pixelnamen.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Anzeige, von der Sie die Tracking-Pixel von Drittanbietern trennen möchten.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jedem Tracking-Pixel eines Drittanbieters, das Sie von den ausgewählten Anzeigen trennen möchten.

      Es können nur Pixel ausgewählt werden, die mit allen ausgewählten Anzeigen verbunden sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Detach]**.

1. (Optional) Um zu den Kampagnendetailansichten zurückzukehren, klicken Sie auf ![Zurück ](/help/dsp/assets/breadcrumb-return.png " Ordner") links neben [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## An Anzeigen angehängte Pixel anzeigen {#view-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. Wechseln Sie zur Option **[!UICONTROL View]** oben rechts.

1. (Optional) Suchen Sie nach Bedarf Anzeigen und Pixel von Drittanbietern:

   * Klicken Sie über der linken Tabelle auf ![Filtern](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

   * Suchen Sie über der rechten und linken Tabelle nach bestimmten Textzeichenfolgen in den Anzeigenamen und Pixelnamen.

1. Klicken Sie auf eine beliebige Anzeigenzeile in der linken Tabelle, um die angehängten Pixel in der rechten Tabelle anzuzeigen.

1. (Optional) Um mehr Pixel an die Anzeigen anzuhängen, wechseln Sie zur **[!UICONTROL Edit]** oben rechts. Anweisungen finden Sie in Schritt 3 des vorherigen Verfahrens [Anhängen von Tracking-Pixeln von Drittanbietern an Anzeigen in einer ](#attach-pixels-ads)&quot;.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen Sie mehrere Anzeigen von Drittanbietern](ad-create-multiple.md)
>* [Bearbeiten einer Anzeige](ad-edit.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](ad-list-placements.md)
>* [Bearbeiten der Anzeigenzeitpläne für Platzierungen](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [FAQs zu Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
