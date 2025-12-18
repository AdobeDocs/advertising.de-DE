---
title: Anzeigen von Warnhinweisen
description: Erfahren Sie, wie Sie Warnhinweise und empfohlene Lösungen für Ihre Kampagnen und Kampagnenkomponenten anzeigen.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# Anzeigen von Warnhinweisen

DSP hilft Ihnen bei der Identifizierung, wenn bei einer Ihrer Kampagnen- oder Kampagnenkomponenten Probleme auftreten. Für jedes Problem erstellt DSP einen Warnhinweis mit einem Zeitstempel und der empfohlenen Aktion zur Behebung des Problems. Gründe für Warnhinweise sind Konfigurationsprobleme (z. B. wenn keine Anzeigen an eine Platzierung angehängt sind oder ein Angebot falsch eingerichtet wurde), Anzeigenablehnungen und Probleme mit dem Kampagnenstatus (z. B. schlechte Bereitstellung oder Leistung von Anzeigen). Warnhinweise sind auf Kampagnen-, Paket-, Platzierungs-, Anzeigen- und Deal-Ebene verfügbar.

Warnhinweise sind an den folgenden Orten verfügbar:

* Ein [!UICONTROL Pulse Panel] in der Ansicht [!UICONTROL Campaigns], [!UICONTROL Packages] und Paketdetails, [!UICONTROL Placements] und [!UICONTROL Ads] zeigt an, ob Warnhinweise für die Elemente in dieser Ansicht verfügbar sind. Wenn das Symbol einen blauen Punkt aufweist (![Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind")), sind Warnhinweise verfügbar. Wenn kein Punkt sichtbar ist (![Pulsbedienfeld-Symbol, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Pulsbedienfeld-Symbol, wenn keine Warnhinweise verfügbar sind")), sind keine Warnhinweise verfügbar.

* Die Datentabellen in denselben Ansichten enthalten eine Spalte &quot;[!UICONTROL Alerts]&quot;, die angibt, wann das Element - oder seine Komponenten - ein Problem hat. Zu den Warnhinweisen gehören „Kritisch![&#x200B; (Kritisch](/help/dsp/assets/indicator-critical.png "Kritisch")), „Warnung“ (![Warnung](/help/dsp/assets/indicator-warning.png "Warnung")) und „Information“ (![Information](/help/dsp/assets/indicator-information.png "Information")).

Sie können für jeden Warnhinweis die entsprechende Ansicht der Kampagnenverwaltung öffnen, um die Einstellungen nach Bedarf zu bearbeiten und das Problem zu beheben.

Sie können auch einzelne Warnhinweise ignorieren, wodurch sie aus dem [!UICONTROL Pulse] entfernt werden.

Warnhinweise und Warnhinweise werden automatisch ausgeblendet, wenn die zugrunde liegenden Probleme behoben sind.

## Anzeigen von Warnhinweisen im [!UICONTROL Pulse Panel]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Für alle Warnhinweise, die für die Ansicht gelten) Klicken Sie in einer beliebigen Kampagnenverwaltungsansicht rechts neben der Symbolleiste auf ![Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind").

   * (Für alle Warnhinweise für eine bestimmte Kampagne) Klicken Sie auf die Warnhinweisanzeige für eine Kampagnenzeile und dann auf **[!UICONTROL View in Pulse panel]**.

   * (Für alle Warnhinweise für ein bestimmtes Paket, eine bestimmte Platzierung oder eine bestimmte Anzeige) Gehen Sie wie folgt vor:

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**, **[!UICONTROL Placements]** oder **[!UICONTROL Ads]** , um die entsprechende Ansicht der Kampagnenkomponente zu öffnen.

      1. Klicken Sie auf die Warnmeldung für ein Paket, eine Platzierung oder eine Anzeigenzeile, und klicken Sie dann auf **[!UICONTROL View in Pulse Panel]**.

   Alle mit der Kampagne und ihren Komponenten verbundenen Warnhinweise, einschließlich zielgerichteter Angebote, werden aufgelistet. Standardmäßig werden kritische Warnhinweise zuerst aufgeführt.

1. (Optional) Um die Warnhinweise nach ihrem ersten Entdeckungsdatum zu gruppieren oder die Warnhinweise nach Warnhinweisstatus, Komponentenstatus, Komponententyp oder einem bestimmten Kampagnennamen zu filtern, klicken Sie auf ![Filterschaltfläche](/help/dsp/assets/filter.png) oben rechts im Bedienfeld, wählen Sie die Filteroptionen aus und klicken Sie dann auf **[!UICONTROL Apply]**.

1. Um eine Liste aller betroffenen Kampagnenkomponenten für einen bestimmten Warnhinweistyp anzuzeigen, klicken Sie auf den Namen des Warnhinweises, z. B. &quot;[!UICONTROL Package: No Active Placement (*N*)]. Um die Details für jede betroffene Komponente anzuzeigen, einschließlich der empfohlenen Aktion, klicken Sie auf [!UICONTROL EXPAND ALL] oder auf den Komponentennamen. Um die entsprechende Kampagnenverwaltungsansicht für eine betroffene Komponente zu öffnen, sodass Sie die empfohlenen Änderungen vornehmen können, halten Sie den Cursor über dem Komponentennamen und klicken Sie auf ![Gehe zu Ansicht](/help/dsp/assets/go-to-view.png "Gehe zu Ansicht").

1. (Optional) Um einen Warnhinweis zu ignorieren (auszublenden), halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Ignorieren](/help/dsp/assets/alert-ignore.png "Ignorieren") und klicken Sie dann auf **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]** oder **[!UICONTROL Ignore indefinitely]**.

Sie haben einige Sekunden, nachdem Sie einen Warnhinweis ignoriert haben, um die Aktion rückgängig zu machen. Sobald die Optionsmeldung geschlossen ist, können Sie die Aktion nicht mehr abbrechen.

1. (Optional) Um ignorierte Warnhinweise abzurufen, filtern Sie die Warnhinweise, sodass ein [!UICONTROL Alert Status] von &quot;[!UICONTROL All]&quot; oder &quot;[!UICONTROL Ignored]&quot; angezeigt wird. Um die Ignorierung eines Warnhinweises aufzuheben, halten Sie den Cursor über den Komponentennamen und klicken Sie auf ![Nicht ignorieren](/help/dsp/assets/alert-un-ignore.png "Nicht ignorieren").

## [!UICONTROL Pulse Panel] schließen

* Klicken Sie rechts in der Symbolleiste auf ![Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel.png "Pulsbedienfeld-Symbol, wenn Warnhinweise verfügbar sind") oder ![Pulsbedienfeld-Symbol, wenn keine Warnhinweise verfügbar sind](/help/dsp/assets/alerts-panel-empty.png "Pulsbedienfeld-Symbol, wenn keine Warnhinweise verfügbar sind").

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Ansichten des Kampagnen-Managements](campaign-reports-about.md)
