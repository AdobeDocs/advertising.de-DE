---
title: Erstellen einer Platzierung
description: Erfahren Sie, wie Sie eine Platzierung erstellen.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Erstellen einer Platzierung

>[!TIP]
>
>Erstellen Sie Platzierungen basierend auf bestimmten Kampagnenzielen oder Berichtsanforderungen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in der die Platzierung enthalten sein soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Klicken Sie im Abschnitt [!UICONTROL Placement Types] des Menüs auf den Platzierungstyp.

   Der Platzierungstyp bestimmt den Anzeigentyp, den die Platzierung enthalten kann.

1. Geben Sie die [Platzierungseinstellungen](placement-settings.md) ein:

   1. Geben Sie die Einstellungen für [!UICONTROL Placement Basics] an.

   1. Geben Sie im Abschnitt [!UICONTROL Goals] die [!UICONTROL Gross Budget] und optional zusätzliche Platzierungsziele an.

      Einige Felder verfügen über Standardwerte, die Sie überschreiben können.

      Wenn das Paket, dem die Platzierung zugewiesen wird, über Geschwindigkeit auf Paketebene verfügt, spiegeln Ihre Ziele und Schritteinstellungen die Paketeinstellungen wider.

   1. (Optional) Schränken Sie im Abschnitt [!UICONTROL Geo-Targeting] die ein- oder ausgeschlossenen Orte ein.

      Wenn Sie bestimmte Orte nicht identifizieren, werden alle Orte als Ziel ausgewählt.

      >[!NOTE]
      >
      >Orte für Stadt und DMA sind nicht für Roku-Platzierungen verfügbar.

   1. Schränken Sie im Abschnitt [!UICONTROL Inventory Targeting] die Inventarquellen ein, die ein- oder ausgeschlossen werden sollen.

      Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Bei [!DNL Roku] -Platzierungen müssen Sie den Inventartyp und die Quellen angeben.

   1. (Optional) Schränken Sie im Abschnitt [!UICONTROL Site Targeting] die Sites ein, die als Ziel ausgewählt werden sollen, und geben Sie die Sites an, die Sie ausschließen möchten.

   1. (Optional) Im Abschnitt [!UICONTROL Audience Targeting] :

      1. Schränken Sie die Zielgruppe ein. Dazu gehört die Auswahl von Zielgruppensegmenten für das Targeting innerhalb der Platzierung.

         Für [!DNL Roku] Platzierungen können Sie die eindeutige Übereinstimmung von [DSP mit  [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) nutzen, indem Sie ein oder mehrere Zielgruppensegmente einschließen, die mit dem deterministischen Datensatz [!DNL Roku] (opted-in) abgeglichen werden können.

      1. (Für Kampagnen mit geräteübergreifendem Targeting auf Benutzerebene; optional) Wenn die Platzierung auf eine oder mehrere spezifische Zielgruppen ausgerichtet ist, aktivieren Sie für die Platzierung benutzerbasiertes geräteübergreifendes Targeting.

         Personenbasiertes geräteübergreifendes Targeting wird von [!DNL LiveRamp] nur unter Verwendung von US-Daten bereitgestellt. Der Dienst steht allen Advertisern mit einem CPM-Preis von 0,35 USD für Impressionen zur Verfügung, die mithilfe des Gerätediagramms [!DNL LiveRamp] bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden).

   1. (Optional) Wenden Sie im Abschnitt [!DNL Brand Safety and Media Targeting] Einschränkungen hinsichtlich der Markensicherheit für Ihre Platzierungen an.

   1. (Optional) Geben Sie im Abschnitt &quot;[!DNL Tracking]&quot;Drittanbieter-Ereignispixel oder Konversionspixel für Anzeigen in der Platzierung ein.

      >[!NOTE]
      >
      >([!DNL Roku] Platzierungen) Zu den von [!DNL Roku] zugelassenen Drittanbieter für Pixel gehören [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] und [!DNL Research Now].

1. Klicken Sie auf **[!UICONTROL Create Placement]**.

1. (Optional) Fügen Sie der Platzierung Anzeigen hinzu:

   1. Klicken Sie auf **[!UICONTROL Attach an ad]**.

   1. Führen Sie einen der folgenden Schritte aus:

      * So erstellen Sie eine neue Anzeige:

         1. Klicken Sie auf **[!UICONTROL Create a New Ad].**

         1. Geben Sie die Anzeigeneinstellungen für [Audioanzeigen](/help/dsp/campaign-management/ads/ad-settings-audio.md), [vernetzte TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [Display-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobile Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [native Anzeigen](/help/dsp/campaign-management/ads/ad-settings-native.md), [Pre-Roll-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) oder [universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) an.

        >[!NOTE]
        >
        >Universelle Videoplatzierungen können nur universelle Videoanzeigen enthalten.

         1. Klicken Sie auf **[!UICONTROL Save & Submit for Review]**.

         1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie für die Platzierung erstellen möchten, auf &quot;**[!UICONTROL Attach Another Ad]**&quot;und wiederholen Sie dann die Schritte 1 bis 3.

         1. Wenn Sie keine vorhandenen Anzeigen hinzufügen möchten, klicken Sie auf **[!UICONTROL I'm done for now]**.

      * So fügen Sie vorhandene Anzeigen in der Kampagne hinzu:

      1. Klicken Sie auf **[!UICONTROL Select an Ad]**.

      1. Führen Sie einen der folgenden Schritte aus:

         * So fügen Sie jeweils eine Anzeige hinzu:

            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select].**

            1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie anhängen möchten, auf &quot;**[!UICONTROL Attach Another Ad]**&quot;und wiederholen Sie dann den Vorgang.

         * So fügen Sie bis zu 20 Anzeigen gleichzeitig hinzu:

            1. Aktivieren Sie das Kontrollkästchen über der Anzeigenliste.

            1. Aktivieren Sie das Kontrollkästchen neben jeder hinzuzufügenden Anzeige.

            1. Klicken Sie auf **[!UICONTROL Attach]**.

            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select]**.

      1. (Optional) So überschreiben Sie die standardmäßige Flugzeit und Anzeigenrotation für bestimmte Anzeigen in der Platzierung:

         1. Klicken Sie auf **[!UICONTROL Custom Schedule Ads]**.

         1. Führen Sie einen der folgenden Schritte aus:

            * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

            * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie in der Anzeigenzeile für die Flugspalte auf **[!UICONTROL +]** .

            * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie in der Anzeigenzeile für die Flugspalte auf **[!UICONTROL x]** .

            * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie in den Fluginformationen auf **[!UICONTROL Even Rotation]** und geben Sie dann die relative Gewichtung ein, um die jede Anzeige gedreht werden soll (in Prozent).

              Die Gesamtgewichte müssen 100 betragen.

         1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

         1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Verwalten von Angebotsmultiplikatoren für Platzierungen](placement-manage-bid-multipliers.md)
>* [Bearbeiten der Anzeigenzeitpläne für Platzierungen](placement-edit-ad-schedule.md)
>* [Eine Platzierung anhalten oder aktivieren](placement-pause-activate.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
>* [Anzeigen des Berichts zur Platzierungsvorschau](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [FAQs über universelle Videos](/help/dsp/campaign-management/faq-universal-video.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Fehlerbehebung bei der Leistung](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: Erstellen einer standardmäßigen Anzeigeplatzierung](https://video.tv.adobe.com/v/340454)
