---
title: Warnhinweise anzeigen
description: Erfahren Sie, wie Sie Warnhinweise und empfohlene Lösungen für Ihre Kampagnen und Kampagnenkomponenten anzeigen.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 5b07096e5f07c60a3efcbf4213b3bc2f061f36a4
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Warnhinweise anzeigen

*Beta-Funktion*

DSP hilft Ihnen bei der Identifizierung, wann Probleme mit einer Ihrer Kampagnen oder Kampagnenkomponenten auftreten. DSP erstellt für jedes Problem einen Warnhinweis mit einem Zeitstempel und der empfohlenen Aktion zur Behebung des Problems. Gründe für Warnhinweise sind Konfigurationsprobleme (z. B. wenn keine Anzeigen an eine Platzierung angehängt sind oder ein Deal falsch eingerichtet wurde), Probleme mit der Ablehnung von Anzeigen und dem Kampagnen-Gesundheitszustand (z. B. schlechte Anzeigenbereitstellung oder Leistung). Warnhinweise sind auf der Kampagnen-, Paket-, Platzierungs-, Anzeigen- und Transaktionsebene verfügbar.

Warnhinweise sind an den folgenden Stellen verfügbar:

* Ein [!UICONTROL Pulse Panel] -Symbol in den Ansichten [!UICONTROL Campaigns], [!UICONTROL Packages] und &quot;Package Details&quot;, [!UICONTROL Placements] und [!UICONTROL Ads] zeigt an, ob Warnhinweise für die Elemente in dieser Ansicht verfügbar sind. Wenn das Symbol einen blauen Punkt aufweist (![Bedienfeldsymbol &quot;Pulsen&quot;, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Bedienfeldsymbol &quot;Pulsen&quot;, wenn Warnhinweise verfügbar sind")), sind Warnhinweise verfügbar. Wenn kein Punkt sichtbar ist (![Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind")), sind keine Warnhinweise verfügbar.

* Die Datentabellen in denselben Ansichten enthalten eine Spalte &quot;[!UICONTROL Alerts]&quot;, die angibt, wann das Element (oder seine Komponenten) ein Problem hat. Zu den Warnindikatoren gehören &quot;Kritisch&quot;(![Kritisch](/help/dsp/assets/indicator-critical.png "Kritisch")), &quot;Warning&quot;(![Warnung](/help/dsp/assets/indicator-warning.png "Warnung")) und &quot;Information&quot;(![Informationen](/help/dsp/assets/indicator-information.png "Informationen")).

Sie können die entsprechende Kampagnenverwaltungsansicht für jeden Warnhinweis öffnen, damit Sie die Einstellungen nach Bedarf bearbeiten können, um das Problem zu beheben.

Sie können auch einen einzelnen Warnhinweis ignorieren, um ihn aus dem Bedienfeld [!UICONTROL Pulse] zu entfernen.

Warnhinweise und Warnhinweise verschwinden automatisch, wenn die zugrunde liegenden Probleme gelöst werden.

## Warnhinweise im [!UICONTROL Pulse Panel] anzeigen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Für alle Warnhinweise, die für die Ansicht gelten) Klicken Sie rechts neben der Symbolleiste in einer beliebigen Kampagnenverwaltungsansicht auf das Symbol &quot;![Bedienfeld-Pulse&quot;, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Bedienfeld-Symbol &quot;Pulsen&quot;, wenn Warnhinweise verfügbar sind").

   * (Für alle Warnhinweise für eine bestimmte Kampagne) Klicken Sie auf den Warnhinweis für eine Kampagnenzeile und dann auf **[!UICONTROL View in Pulse panel]**.

   * (Für alle Warnhinweise für ein bestimmtes Paket, eine bestimmte Platzierung oder Anzeige) Führen Sie folgende Schritte aus:

      1. Klicken Sie auf den Kampagnennamen.

      1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**, **[!UICONTROL Placements]** oder **[!UICONTROL Ads]** , um die entsprechende Ansicht der Kampagnenkomponente zu öffnen.

      1. Klicken Sie auf den Warnhinweis für ein Paket, eine Platzierung oder eine Anzeigenzeile und dann auf **[!UICONTROL View in Pulse Panel]**.

   Alle Warnungen, die mit der Kampagne und ihren Komponenten verknüpft sind, einschließlich zielgerichteter Angebote, werden aufgelistet. Kritische Warnhinweise werden standardmäßig zuerst aufgeführt.

1. (Optional) Um die Warnhinweise nach ihrem ersten Erkennungsdatum zu gruppieren oder die Warnhinweise nach Warnungsstatus, Komponentenstatus, Komponententyp oder einem bestimmten Kampagnennamen zu filtern, klicken Sie oben rechts im Bedienfeld auf die Schaltfläche ![Filter](/help/dsp/assets/filter.png) , wählen Sie die Filteroptionen aus und klicken Sie auf **[!UICONTROL Apply]**.

1. Um eine Liste aller betroffenen Kampagnenkomponenten für einen bestimmten Warnhinweistyp anzuzeigen, klicken Sie auf den Warnungsnamen, z. B. &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Um die Details für jede betroffene Komponente anzuzeigen, einschließlich der empfohlenen Aktion, klicken Sie auf [!UICONTROL EXPAND ALL] oder klicken Sie auf den Komponentennamen. Um die relevante Kampagnenverwaltungsansicht für jede betroffene Komponente zu öffnen, damit Sie die empfohlenen Änderungen vornehmen können, halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Gehe zu Ansicht](/help/dsp/assets/go-to-view.png "Gehe zu Ansicht").

1. (Optional) Um einen Warnhinweis zu ignorieren (auszublenden), halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Ignore](/help/dsp/assets/alert-ignore.png "Ignore") und klicken Sie dann auf **[!UICONTROL Ignore indefinitely]** <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->.

Sie haben einige Sekunden Zeit, nachdem Sie einen Warnhinweis ignoriert haben, um die Aktion rückgängig zu machen. Sobald die Optionsmeldung geschlossen wurde, können Sie die Aktion nicht mehr abbrechen.

1. (Optional) Um ignorierte Warnhinweise abzurufen, filtern Sie die Warnhinweise so, dass [!UICONTROL Alert Status] von &quot;[!UICONTROL All]&quot; oder &quot;[!UICONTROL Ignored]&quot; angezeigt wird. Um einen Warnhinweis zu ignorieren, halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Ignorieren](/help/dsp/assets/alert-un-ignore.png "Ignorieren") aufheben.

## Schließen Sie den [!UICONTROL Pulse Panel]

* Klicken Sie rechts in der Symbolleiste auf das Symbol &quot;![Bedienfeld ziehen&quot;, wenn Warnhinweise verfügbar sind.](/help/dsp/assets/alerts-panel.png "Symbol Bedienfeld-Pulse, wenn Warnhinweise verfügbar sind") oder ![Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Symbol &quot;Bedienfeld auswerten&quot;, wenn keine Warnhinweise verfügbar sind").

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
