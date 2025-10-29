---
title: Erstellen einer Platzierung
description: Erfahren Sie, wie Sie eine Platzierung erstellen.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: d1be9ab441fd8abdc21491afb57763ec6eb2bec0
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# Erstellen einer Platzierung

>[!TIP]
>
>Erstellen Sie Platzierungen basierend auf bestimmten Kampagnenzielen oder Reporting-Anforderungen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in der die Platzierung enthalten sein soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Klicken Sie im Abschnitt [!UICONTROL Placement Types] des Menüs auf den Platzierungstyp.

   Der Platzierungstyp bestimmt den Anzeigentyp, den die Platzierung enthalten kann.

1. Geben Sie die [Platzierungseinstellungen](placement-settings.md) ein:

   1. Geben Sie die [!UICONTROL Placement Basics] an.

   1. Geben Sie im Abschnitt [!UICONTROL Goals] den [!UICONTROL Gross Budget] an und geben Sie optional zusätzliche Platzierungsziele an.

      Einige Felder verfügen über Standardwerte, die Sie überschreiben können.

      Wenn das Paket, dem die Platzierung zugewiesen wird, eine Geschwindigkeit auf Paketebene aufweist, spiegeln Ihre Ziele und Geschwindigkeitseinstellungen die Paketeinstellungen wider.

   1. (Optional) Grenzen Sie im Abschnitt [!UICONTROL Geo-Targeting] die Speicherorte ein, die ein- oder ausgeschlossen werden sollen.

      Wenn Sie keine bestimmten Standorte identifizieren, werden alle Standorte als Ziel ausgewählt.

      >[!NOTE]
      >
      >Orte in Städten und DMA sind für Roku-Platzierungen nicht verfügbar.

   1. Grenzen Sie im Abschnitt [!UICONTROL Inventory Targeting] die ein- oder auszuschließenden Inventarquellen ein.

      Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Für [!DNL Roku] Platzierungen müssen Sie den Inventartyp und die Quellen angeben.

   1. (Optional) Grenzen Sie im Abschnitt [!UICONTROL Site or app And Keyword Targeting] die Sites und Apps ein, die Sie ansprechen und ausschließen möchten.

   1. (Optional) Im [!UICONTROL Audience Targeting] Abschnitt:

      1. Einschränken Sie die Audience. Dazu gehört auch die Auswahl von Zielgruppensegmenten, die in der Platzierung angesprochen werden sollen.

         Für [!DNL Roku] Platzierungen können Sie den eindeutigen Zielgruppenabgleich von [DSP mit nutzen [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) indem Sie ein oder mehrere Zielgruppensegmente einbeziehen, die mit dem deterministischen [!DNL Roku]-Datensatz (Opt-in) abgeglichen werden können.

         Erstanbieter-RampID-Segmente, die nicht mit einer aktiven, geplanten oder angehaltenen Platzierung verknüpft sind, werden angehalten. Das Segment wird in der Segmentliste als „Automatisch angehalten“ angegeben.

      1. (Für Kampagnen mit geräteübergreifendem Targeting auf Benutzerebene; optional) Wenn die Platzierung auf eine oder mehrere bestimmte Zielgruppen abzielt, aktivieren Sie für die Platzierung geräteübergreifendes Targeting für Personen.

         Das personenbasierte geräteübergreifende Targeting wird von [!DNL LiveRamp] bereitgestellt, die ausschließlich US-Daten verwenden. Der Service steht allen Advertisern für 0,35 US-Dollar in CPM für Impressionen zur Verfügung, die mithilfe des [!DNL LiveRamp]-Gerätediagramms bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden).

   1. (Optional) Wenden Sie im Abschnitt [!DNL Brand Safety and Media Targeting] Markensicherheitsbeschränkungen für Ihre Platzierungen an.

   1. (Optional) Geben Sie im Abschnitt [!DNL Tracking] Ereignispixel von Drittanbietern oder Konversionspixel für Anzeigen in der Platzierung ein.

      >[!NOTE]
      >
      >([!DNL Roku] Platzierungen) Von [!DNL Roku] genehmigte Pixel-Drittanbieter sind [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] und [!DNL Research Now].

1. Klicken Sie auf **[!UICONTROL Create Placement]**.

1. (Optional) Fügen Sie der Platzierung Anzeigen hinzu:

   1. Klicken Sie auf **[!UICONTROL Attach an ad]**.

   1. Führen Sie einen der folgenden Schritte aus:

      * So erstellen Sie eine neue Anzeige:

         1. Klicken Sie auf **[!UICONTROL Create a New Ad].**

         1. Legen Sie die Anzeigeneinstellungen für [Audioanzeigen](/help/dsp/campaign-management/ads/ad-settings-audio.md), [Connected TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [Display-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md), [Mobile-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [native Anzeigen](/help/dsp/campaign-management/ads/ad-settings-native.md), [Pre-Roll-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) oder [universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) fest.

        >[!NOTE]
        >
        >Platzierungen von universellen Videos können nur universelle Videoanzeigen enthalten.

         1. Klicken Sie auf **[!UICONTROL Save & Submit for Review]**.

         1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie für die Platzierung erstellen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann die Schritte 1 bis 3.

         1. Wenn Sie keine vorhandenen Anzeigen anhängen möchten, klicken Sie auf **[!UICONTROL I'm done for now]**.

      * So fügen Sie vorhandene Anzeigen in der Kampagne hinzu:

         1. Klicken Sie auf **[!UICONTROL Select an Ad]**.

         1. Führen Sie einen der folgenden Schritte aus:

            * So fügen Sie jeweils eine Anzeige hinzu:

               1. Klicken Sie neben dem Anzeigenamen auf **[!UICONTROL Select].**

               1. (Optional) Klicken Sie für jede weitere Anzeige, die Sie anhängen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann den Vorgang.

            * So fügen Sie bis zu 20 Anzeigen gleichzeitig hinzu:

               1. Aktivieren Sie das Kontrollkästchen über der Anzeigenliste.

               1. Aktivieren Sie das Kontrollkästchen neben jeder hinzuzufügenden Anzeige.

               1. Klicken Sie auf **[!UICONTROL Attach]**.

               1. Klicken Sie neben dem Anzeigenamen auf **[!UICONTROL Select]**.

         1. (Optional) So überschreiben Sie den standardmäßigen Flugzeitraum und die Anzeigenrotation für bestimmte Anzeigen in der Platzierung:

            1. Klicken Sie auf **[!UICONTROL Custom Schedule Ads]**.

            1. Führen Sie einen der folgenden Schritte aus:

               * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

               * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie in der Anzeigenzeile für die Spalte Flug auf **[!UICONTROL +]**.

               * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie in der Anzeigenzeile für die Spalte Flug auf **[!UICONTROL x]**.

               * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie in den Fluginformationen auf **[!UICONTROL Even Rotation]** und geben Sie dann das relative Gewicht, um das jede Anzeige gedreht werden soll, als Prozentsatz ein.

                 Die Gesamtgewichte müssen 100 betragen.

            1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

            1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Angebotsmultiplikatoren für Platzierungen verwalten](placement-manage-bid-multipliers.md)
>* [Bearbeiten der Anzeigenzeitpläne für Platzierungen](placement-edit-ad-schedule.md)
>* [Platzierung deaktivieren oder aktivieren](placement-pause-activate.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
>* [Anzeigen des Berichts für Platzierungs-Forecasts](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [FAQs zu Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Fehlerbehebung für die Leistung](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: So erstellen Sie eine standardmäßige Anzeigeplatzierung](https://video.tv.adobe.com/v/340454)
