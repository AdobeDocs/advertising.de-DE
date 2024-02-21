---
title: Warnhinweise anzeigen
description: Erfahren Sie, wie Sie Warnhinweise und empfohlene Lösungen für Ihre Kampagnen und Kampagnenkomponenten anzeigen.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Warnhinweise anzeigen

*Beta-Funktion*

DSP hilft Ihnen bei der Identifizierung, wann Probleme mit einer Ihrer Kampagnen oder Kampagnenkomponenten auftreten. DSP erstellt für jedes Problem einen Warnhinweis mit einem Zeitstempel und der empfohlenen Aktion zur Behebung des Problems. Gründe für Warnhinweise sind Konfigurationsprobleme (z. B. wenn keine Anzeigen an eine Platzierung angehängt sind oder ein Deal falsch eingerichtet wurde), Probleme mit der Ablehnung von Anzeigen und dem Kampagnen-Gesundheitszustand (z. B. schlechte Anzeigenbereitstellung oder Leistung). Warnhinweise sind auf der Kampagnen-, Paket-, Platzierungs-, Anzeigen- und Transaktionsebene verfügbar.

Warnhinweise sind an den folgenden Stellen verfügbar:

* A [!UICONTROL Pulse Panel] im [!UICONTROL Campaigns], [!UICONTROL Packages] und Paketdetails, [!UICONTROL Placements], und [!UICONTROL Ads] -Ansichten zeigen an, ob Warnhinweise für die Elemente in dieser Ansicht verfügbar sind. Wenn das Symbol einen blauen Punkt (![Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind")), sind Warnhinweise verfügbar. Wenn kein Punkt sichtbar ist (![Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind")), sind keine Warnhinweise verfügbar.

* Die Datentabellen in denselben Ansichten enthalten ein &quot;[!UICONTROL Alerts]&quot;-Spalte, die angibt, wann das Element oder seine Komponenten ein Problem haben. Zu den Warnindikatoren zählen &quot;Kritisch&quot; (![Kritisch](/help/dsp/assets/indicator-critical.png "Kritisch")), &quot;Warning&quot;(![Warnung](/help/dsp/assets/indicator-warning.png "Warnung")) und &quot;Informationen&quot;(![Informationen](/help/dsp/assets/indicator-information.png "Informationen")).

Sie können die entsprechende Kampagnenverwaltungsansicht für jeden Warnhinweis öffnen, damit Sie die Einstellungen nach Bedarf bearbeiten können, um das Problem zu beheben.

Sie können auch einen einzelnen Warnhinweis ignorieren, um ihn aus dem [!UICONTROL Pulse] Bedienfeld.

Warnhinweise und Warnhinweise verschwinden automatisch, wenn die zugrunde liegenden Probleme gelöst werden.

## Warnhinweise anzeigen im [!UICONTROL Pulse Panel]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Für alle Warnhinweise, die für die Ansicht gelten) Klicken Sie rechts neben der Symbolleiste in einer beliebigen Kampagnenverwaltungsansicht auf ![Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind").

   * (Für alle Warnhinweise für eine bestimmte Kampagne) Klicken Sie auf die Warnhinweis-Anzeige für eine Kampagnenzeile und klicken Sie dann auf **[!UICONTROL View in Pulse panel]**.

   * (Für alle Warnhinweise für ein bestimmtes Paket, eine bestimmte Platzierung oder Anzeige) Führen Sie folgende Schritte aus:

      1. Klicken Sie auf den Kampagnennamen.

      1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**, **[!UICONTROL Placements]** oder **[!UICONTROL Ads]** , um die entsprechende Ansicht der Kampagnenkomponente zu öffnen.

      1. Klicken Sie auf den Warnhinweis für ein Paket, eine Platzierung oder eine Anzeigenzeile und dann auf **[!UICONTROL View in Pulse Panel]**.

   Alle Warnungen, die mit der Kampagne und ihren Komponenten verknüpft sind, einschließlich zielgerichteter Angebote, werden aufgelistet. Kritische Warnhinweise werden standardmäßig zuerst aufgeführt.

1. (Optional) Um die Warnhinweise nach ihrem ersten Erkennungsdatum zu gruppieren oder die Warnhinweise nach Warnungsstatus, Komponentenstatus, Komponententyp oder nach einem bestimmten Kampagnennamen zu filtern, klicken Sie auf ![Filterschaltfläche](/help/dsp/assets/filter.png) Wählen Sie oben rechts im Bedienfeld die Filteroptionen aus und klicken Sie auf **[!UICONTROL Apply]**.

1. Um eine Liste aller betroffenen Kampagnenkomponenten für einen bestimmten Warnhinweistyp anzuzeigen, klicken Sie auf den Warnungsnamen, z. B.[!UICONTROL Package: No Active Placement (*N*)]&quot;. Um die Details für jede betroffene Komponente anzuzeigen, einschließlich der empfohlenen Aktion, klicken Sie auf [!UICONTROL EXPAND ALL] oder klicken Sie auf den Komponentennamen. Um die entsprechende Kampagnenverwaltungsansicht für jede betroffene Komponente zu öffnen, damit Sie die empfohlenen Änderungen vornehmen können, halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Zur Ansicht wechseln](/help/dsp/assets/go-to-view.png "Zur Ansicht wechseln").

1. (Optional) Um einen Warnhinweis zu ignorieren (auszublenden), halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Ignorieren](/help/dsp/assets/alert-ignore.png "Ignorieren")und klicken Sie anschließend auf **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

Sie haben einige Sekunden Zeit, nachdem Sie einen Warnhinweis ignoriert haben, um die Aktion rückgängig zu machen. Sobald die Optionsmeldung geschlossen wurde, können Sie die Aktion nicht mehr abbrechen.

1. (Optional) Um ignorierte Warnhinweise abzurufen, filtern Sie die Warnhinweise, um eine [!UICONTROL Alert Status] von &quot;[!UICONTROL All]&quot; oder &quot;[!UICONTROL Ignored].&quot; Um eine Warnung zu ignorieren, halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Ignorieren](/help/dsp/assets/alert-un-ignore.png "Ignorieren").

## Schließen Sie die [!UICONTROL Pulse Panel]

* Klicken Sie rechts neben der Symbolleiste auf ![Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn Warnhinweise verfügbar sind") oder ![Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind").

>[!MORELIKETHIS]
>
>* [Arten von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
