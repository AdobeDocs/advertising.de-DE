---
title: Anzeigen an Platzierungen anhängen
description: Erfahren Sie, wie Sie Anzeigen an Platzierungen anhängen.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Anzeigen an Platzierungen anhängen

Verwenden Sie die Ansicht &quot;[!UICONTROL Ad Tools]&quot;, um Anzeigen an Platzierungen anzuhängen, Tracking-Pixel von Drittanbietern an die Anzeigen anzuhängen und vorhandene Tracking-Pixel von Drittanbietern von den Anzeigen zu trennen.

>[!NOTE]
>
>Universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

## Öffnen Sie die Ansicht &quot;[!UICONTROL Ad Tools]&quot; {#ad-tools-open}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Öffnen Sie die Ansicht [!UICONTROL Ad Tools] auf eine der folgenden Arten:

   * (Klicken Sie in der Ansicht [!UICONTROL Packages] , [!UICONTROL Placements] oder [!UICONTROL Ads] rechts oben auf **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Klicken Sie in der Ansicht [!UICONTROL Placements] neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Klicken Sie in der Ansicht [!UICONTROL Ads] neben dem Anzeigennamen auf **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   Die Registerkarte [!UICONTROL Attach Ads] ist standardmäßig ausgewählt.

## Anzeigen an Platzierungen anhängen {#attach-ads-campaign}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Führen Sie in der Unteransicht &quot;[!UICONTROL Edit]&quot;für jede Gruppe von Anzeigen, die Sie Platzierungen hinzufügen möchten, folgende Schritte aus:

   1. (Optional) Suchen Sie bestimmte Platzierungen und Anzeigen auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filter](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Paket, Platzierungstyp, Platzierungsstatus, Anzeigentyp oder Anzeigenstatus.

      * Suchen Sie über der linken und rechten Tabelle nach bestimmten Textzeichenfolgen in der Platzierung und den Anzeigennamen.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Platzierung, an die die Anzeigen angehängt werden sollen.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jeder Anzeige, die Sie an die ausgewählten Platzierungen anhängen möchten.

      Es können nur Anzeigen ausgewählt werden, die für den Platzierungstyp relevant sind und noch nicht an die ausgewählten Platzierungen angehängt sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Attach]**.

1. (Optional) Um zu den Detailansichten der Kampagne zurückzukehren, klicken Sie auf ![Zurück zum Ordner](/help/dsp/assets/breadcrumb-return.png "Zurück zum Ordner") links von [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## Anzeigen, die an Platzierungen angehängt sind {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Wechseln Sie zur Option **[!UICONTROL View]** oben rechts.

1. (Optional) Suchen Sie nach Bedarf spezifische Platzierungen und Anzeigen:

   * Klicken Sie über der linken Tabelle auf ![Filter](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Paket, Platzierungstyp, Platzierungsstatus, Anzeigentyp oder Anzeigenstatus.

   * Suchen Sie in der rechten und linken Tabelle nach bestimmten Textzeichenfolgen in der Platzierung oder im Anzeigennamen.

1. Klicken Sie auf eine beliebige Platzierungszeile in der linken Tabelle, um die angehängten Anzeigen in der rechten Tabelle anzuzeigen.

1. (Optional) Um weitere Anzeigen an die Platzierungen der Kampagne anzuhängen, wechseln Sie zur Ansicht &quot;**[!UICONTROL Edit]**&quot;oben rechts. Anweisungen finden Sie unter Schritt 2 im vorherigen Verfahren &quot;[Anzeigen an Platzierungen anhängen](#attach-ads-campaign)&quot;.

## Anhängen von Tracking-Pixeln von Drittanbietern an Anzeigen an einer Platzierung {#attach-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. In der Unteransicht [!UICONTROL Edit] :

   1. (Optional) Suchen Sie Anzeigen und Pixel von Drittanbietern auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filter](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

      * Suchen Sie über der linken und rechten Tabelle nach bestimmten Textzeichenfolgen in den Anzeigennamen und Pixelnamen.

   1. (Wenn für die Kampagne keine Tracking-Pixel von Drittanbietern vorhanden sind) Erstellen Sie ein Pixel:

      1. Klicken Sie in der rechten Tabelle auf **[!UICONTROL Create pixel]**.

      1. Geben Sie die Einstellungen an:

         **[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel ausgelöst wird, z. B. *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

         **[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

         **[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

         **[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

      1. Klicken Sie auf **[!UICONTROL Save]**.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Anzeige, für die Sie Tracking-Pixel von Drittanbietern anhängen möchten.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jedem Verfolgungs-Pixel von Drittanbietern, das Sie an die ausgewählten Anzeigen anhängen möchten.

      Es können nur Pixel ausgewählt werden, die nicht bereits an die ausgewählten Anzeigen angehängt sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Attach]**.

1. (Optional) Um zu den Detailansichten der Kampagne zurückzukehren, klicken Sie auf ![Zurück zum Ordner](/help/dsp/assets/breadcrumb-return.png "Zurück zum Ordner") links von [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## Trennen von Tracking-Pixeln von Drittanbietern von Anzeigen an einer Platzierung {#detach-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. In der Unteransicht [!UICONTROL Edit] :

   1. (Optional) Suchen Sie Anzeigen und Pixel von Drittanbietern auf eine der folgenden Arten:

      * Klicken Sie über der linken Tabelle auf ![Filter](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

      * Suchen Sie über der linken und rechten Tabelle nach bestimmten Textzeichenfolgen in den Anzeigennamen und Pixelnamen.

   1. Aktivieren Sie in der linken Tabelle das Kontrollkästchen neben jeder Anzeige, von der Sie Tracking-Pixel von Drittanbietern trennen möchten.

   1. Aktivieren Sie in der rechten Tabelle das Kontrollkästchen neben jedem Tracking-Pixel eines Drittanbieters, das Sie von den ausgewählten Anzeigen trennen möchten.

      Es können nur Pixel ausgewählt werden, die an alle ausgewählten Anzeigen angehängt sind.

   1. Klicken Sie unten rechts auf **[!UICONTROL Detach]**.

1. (Optional) Um zu den Detailansichten der Kampagne zurückzukehren, klicken Sie auf ![Zurück zum Ordner](/help/dsp/assets/breadcrumb-return.png "Zurück zum Ordner") links von [!UICONTROL Ad Tools] und wählen Sie den Kampagnennamen aus.

## An Anzeigen angehängte Anzeigepixel {#view-pixels-ads}

1. [Öffnen Sie die [!UICONTROL Ad Tools] Ansicht](#ad-tools-open).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Attach Pixels]** .

1. Wechseln Sie zur Option **[!UICONTROL View]** oben rechts.

1. (Optional) Suchen Sie nach Bedarf Anzeigen und Pixel von Drittanbietern:

   * Klicken Sie über der linken Tabelle auf ![Filter](/help/dsp/assets/filter.png) und filtern Sie die Listen nach Anzeigenstatus, Anzeigentyp, Pixelintegrationsereignis oder Pixeltyp.

   * Suchen Sie über der linken und rechten Tabelle nach bestimmten Textzeichenfolgen in den Anzeigennamen und Pixelnamen.

1. Klicken Sie auf eine beliebige Anzeigenzeile in der linken Tabelle, um die angehängten Pixel in der rechten Tabelle anzuzeigen.

1. (Optional) Um weitere Pixel an die Anzeigen anzuhängen, wechseln Sie zur Ansicht &quot;**[!UICONTROL Edit]**&quot;oben rechts. Anweisungen finden Sie in Schritt 3 des vorherigen Verfahrens, &quot;[Verfolgungspixel von Drittanbietern an Anzeigen in einer Platzierung anhängen](#attach-pixels-ads)&quot;.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-multiple.md)
>* [Bearbeiten einer Anzeige](ad-edit.md)
>* [Auflisten der mit einer Anzeige verknüpften Platzierungen](ad-list-placements.md)
>* [Bearbeiten der Anzeigenzeitpläne für Platzierungen](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [FAQs über universelle Videos](/help/dsp/campaign-management/faq-universal-video.md)
