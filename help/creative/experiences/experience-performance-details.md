---
title: Leistungsberichte auf Erlebnisebene
description: Erfahren Sie, wie Sie Leistungsberichte auf Erlebnisebene anzeigen.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 118838e0236c0e40aea797edb1b2f8fb0efb2a79
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Leistungsberichte auf Erlebnisebene

*Geschlossene Beta-Version*

Sie können detaillierte Leistungsdaten für jedes Erlebnis anzeigen.

## Daten in Leistungsberichten auf Erlebnisebene

Die Berichtsansicht enthält die folgenden Daten:

* Registerkarte **Übersicht** : Ein Leistungsüberblick über alle Konversionsmetriken für das gesamte Erlebnis<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." --> einschließlich:

   * Abschnitt **Gesamtleistung**:

      * **Gesamtleistung**: Die Gesamtzahl der Impressionen; Klicks; Clickthrough-Rate (CTR); und Durchsichtskonversionen und Clickthrough-Konversionen.

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **Standardrate**: (Nur Erlebnisse beim Targeting mit Entscheidungsbäumen) Die Anzahl der Impressionen, die aus zielgerichteten Kreativen, allgemeinen Kreativen ohne Zielgruppe oder an „Alle anderen“ gerichtet sind, und das Standardkreativ für das Erlebnis.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **Leistungsaufschlüsselung** Abschnitt:

      * **Regionale Leistung:*: Einzelne Metriken nach geografischem Standort.

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Geräteleistung:** Einzelne Metriken nach Gerätetyp, Betriebssystem und Browser. Klicken Sie optional auf den Wert für eine beliebige Gerätekategorie, um eine Liste der Top-Kreativen <!-- NN --> sehen, die mit diesen Kriterien beliefert wurden.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* Registerkarte **Creative-***: Eine Leistungsübersicht nach Kreativ- und Bundle- oder Anzeigen-Tag, einschließlich:

   * **Kreative** Unterregisterkarte: Die Gesamtzahl der Impressionen, Klicks und CTR für jeden Kreativen im Erlebnis.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * Unterregisterkarte **Bundles/Tags**: Die Gesamtzahl der Impressionen, Klicks und CTR für einzelne Bundles (Erlebnisse beim Targeting mit Entscheidungsbäumen) oder Anzeigen-Tags (Erlebnisse ohne Targeting mit Entscheidungsbäumen) in dem Erlebnis.

## Anzeigen von Leistungsberichten für ein Erlebnis

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Erlebnisse einzuschließen.

1. Erlebnis auswählen:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Reports]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Reports]**.

   Die Registerkarte [!UICONTROL Overview] wird geöffnet.

1. (Optional) Geben Sie in der Symbolleiste oben rechts den Datumsbereich, die Konversionszuordnungsregel und die Konversionen an, die in allen Leistungsberichten gemeldet werden:

   * (Optional) Um den Datumsbereich für die Leistungsdaten zu ändern, wählen Sie eine Option im Menü „Datum“:

      * Um einen voreingestellten Zeitraum festzulegen, wählen Sie den Bericht aus: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* oder *[!UICONTROL Yesterday]*.

      * Um einen benutzerdefinierten Datumsbereich anzugeben, geben Sie das Start- und Enddatum ein oder klicken Sie ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png) neben einem Feld und wählen Sie ein Datum aus.

   * (Optional) Um die Regel zu ändern, mit der Konversionsdaten in einer Reihe von Ereignissen zugeordnet werden, die zu einer Konversion führen, klicken Sie auf ![Einstellungen](/help/creative/assets/settings.png) und ändern Sie die **[!UICONTROL Attribution Rule]**.

     Weitere Informationen zu Attributionsregeln finden Sie unter &quot;[ der Berechnung von Attributionsregeln](/help/search-social-commerce/reports/attribution-rules.md).

   * (Optional) Um die gemeldeten Konversionen zu ändern, klicken Sie auf ![Einstellungen](/help/creative/assets/settings.png) und wählen Sie die Konversionsnamen im Menü &quot;**[!UICONTROL Conversions]**&quot; aus. Derzeit ist nur die Metrik „Alle auswählen“ verfügbar, um alle Konversionsmetriken einzuschließen.

     Die verfügbaren Konversionsspalten enthalten die Konversionen, die in Advertising Search, Social und Commerce verfügbar sind, unabhängig davon, ob Sie Kunde von Search, Social und Commerce sind oder nicht. Die Liste kann Konversions- und Site-Interaktionsmetriken enthalten, die mit Adobe Analytics synchronisiert werden, wenn der Advertiser über [eine [!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md) verfügt. [!DNL Analytics] berechnete Metriken und erweiterte berechnete Metriken sind nicht verfügbar. Weitere Informationen zum Einschließen erfasster Konversionen in Berichte finden Sie im Handbuch zu Search, Social und Commerce [Über die Verwaltung der Konversionsmetriken eines Werbetreibenden](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md).

1. (Auf der Registerkarte [!UICONTROL Overview] ):

   * (Optional) Halten Sie im [!UICONTROL Overall Regional Performance] Abschnitt den Cursor über einen Punkt im Diagramm, um Daten für diesen Punkt anzuzeigen.

   * (Optional) Führen Sie im Abschnitt [!UICONTROL Regional Performance] einen der folgenden Schritte aus:

      * Klicken Sie auf einen Metriknamen (z. B. [!UICONTROL Impressions]), um diese Metrik anzuzeigen.

      * Wählen Sie im Menü [!UICONTROL Region] die Region aus.

      * Halten Sie den Cursor über ein Land oder einen Staat, um Daten für diese Region anzuzeigen.

   * (Optional) Führen Sie im Abschnitt [!UICONTROL Device Performance] einen der folgenden Schritte aus:

      * Halten Sie den Cursor über den Wert für eine beliebige Gerätekategorie, um Daten für dieses Kriterium anzuzeigen.

      * Klicken Sie auf den Wert für eine beliebige Gerätekategorie, um eine Liste der <!-- NN--> Kreativen anzuzeigen, die mit diesen Kriterien beliefert wurden.

1. (Optional) Um Daten nach Kreativ- und Bundle- oder Anzeigen-Tag anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Creative Performance]** .

   * Auf der Unterregisterkarte [!UICONTROL Creatives] haben Sie folgende Möglichkeiten:

      * (Optional) Um zwischen der Diagrammansicht und der Rasteransicht zu wechseln, klicken Sie ![Diagramm](/help/creative/assets/chart-view-button.png "Diagramm") bzw. ![Gitter](/help/creative/assets/table-view-button.png "Gitter").

      * (Optional) Halten Sie in der Diagrammansicht den Cursor über einen Punkt im Diagramm, um Daten für diesen Punkt anzuzeigen.

      * (Nur Erlebnisse mit Targeting mit Entscheidungsbäumen; optional) Aktivieren Sie **[!UICONTROL Split targeting]**, um die Leistung für jede angewendete Anzeigenzielgruppe aufzuschlüsseln.

1. Um Daten nach Bundle (Erlebnisse beim Targeting mit Entscheidungsbäumen) oder Anzeigen-Tag (Erlebnisse ohne Targeting mit Entscheidungsbäumen) anzuzeigen, klicken Sie auf die Unterregisterkarte **[!UICONTROL Bundles]** . Sie können einen der folgenden Schritte ausführen:

   * (Optional) Um zwischen der Diagrammansicht und der Rasteransicht zu wechseln, klicken Sie ![Diagramm](/help/creative/assets/chart-view-button.png "Diagramm") bzw. ![Gitter](/help/creative/assets/table-view-button.png "Gitter").

   * (Optional) Halten Sie in der Diagrammansicht den Cursor über einen Punkt im Diagramm, um Daten für diesen Punkt anzuzeigen.

   * (Nur Erlebnisse mit Targeting mit Entscheidungsbäumen; optional) Aktivieren Sie **[!UICONTROL Split targeting]**, um die Leistung für jede angewendete Anzeigenzielgruppe aufzuschlüsseln.

## Herunterladen von Leistungsberichten für ein Erlebnis

* Klicken Sie in der Symbolleiste oben in den Leistungsberichten auf ![Herunterladen](/help/creative/assets/download.png "Herunterladen").

  Die Datei wird in einer [!DNL Microsoft Excel]-Datei im XLSX-Format (Spreadsheet) heruntergeladen, entsprechend dem normalen Verfahren Ihres Browsers.

>[!MORELIKETHIS]
>
>* [Benutzerdefinierter Creative-Bericht](/help/creative/report-custom-creative.md)
>* [Alle Erlebnisse in der Ansicht herunterladen](/help/creative/experiences/experience-download-view.md)
>* [Über Erlebnisse in Advertising Creative](/help/creative/experiences/experience-about.md)
