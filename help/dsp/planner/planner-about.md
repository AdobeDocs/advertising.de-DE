---
title: Über das DSP-Planer-Tool
description: Erfahren Sie mehr über das Planer-Tool zur Prognose der eindeutigen Reichweite für Platzierungen von vernetztem Fernsehen (CTV) gemäß den festgelegten Budget- und Zielgruppenkriterien.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Über das DSP-Planer-Tool

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta-Funktion*

Das Planer-Tool hilft Ihnen, die einzigartige Reichweite von CTV-Platzierungen (Connected TV) auf Haushaltsebene gemäß den festgelegten Budget- und Zielgruppenkriterien vorherzusagen, bevor Sie mit den Ausgaben für Inventar beginnen. Nachdem Sie mehrere Reichweitenpläne bewertet haben, können Sie den Plan implementieren, der am besten zu den gewünschten Ergebnissen in Ihren Paketen und Platzierungen passt.

Das Planer-Tool nutzt historische Bid-, Impression- und Reichweitendaten aus den letzten 90 Tagen, um die eindeutige Reichweite, den durchschnittlichen CPM, die durchschnittliche Häufigkeit und die Impressionen für eine Plankonfiguration zu schätzen.

## Planerprognose

Jede Prognose besteht aus einer Reach-Budget-Prognosekurve, die den Umfang der mit den Planeinstellungen erreichbaren Reichweite anzeigt. Bewegen Sie den Cursor über die Visualisierung, um inkrementelle Reichweitenchancen mit höheren Budgets anzuzeigen.

![Planerprognose](/help/dsp/assets/planner-forecast.png "Planerprognose")

Die Prognoseausgabe enthält auch einen [!UICONTROL Inventory Breakdown] Abschnitt, der zeigt, wie verschiedene Herausgeber zur einzigartigen Reichweite beitragen und wertvolle Entdeckungsmöglichkeiten bieten.

>[!NOTE]
>
>* Im Abschnitt [!UICONTROL Inventory Breakdown] werden nur Daten für das private und [!UICONTROL On Demand] Inventar angezeigt.
>* Die geschätzte eindeutige Reichweite, die für zwei Herausgeber angezeigt wird, kann sich überschneiden.

## Die Planeransicht

In der [!UICONTROL Planner] können Sie Ihre vorhandenen CTV-Reichweitenpläne anzeigen und neue erstellen.

Sie können die Prognose auch für jeden Plan bearbeiten, duplizieren, exportieren, archivieren oder neu generieren.

## Häufig gestellte Fragen

+++Welche Arten von Inventar unterstützt das Planer-Tool?

Das Planer-Tool unterstützt alle Arten von Inventar, einschließlich programmgesteuert garantierter (PG), privater Marktplatz (PMP), [!UICONTROL On Demand] und öffentlicher. Um genaue Prognosen zu generieren, sollten Sie Angebote mit mindestens 50.000 Impressionen in den letzten sieben Tagen einschließen.

+++

+++Warum sehe ich &quot;[!UICONTROL Unable to generate forecast]?“

Einer der häufigsten Gründe für diesen Fehler ist ein unzureichendes Budget oder ein Höchstgebot. Für optimale Ergebnisse verwenden Sie ein Mindestbudget von 5000 USD. Wenn der [!UICONTROL Connected TV] Medientyp ausgewählt ist, geben Sie ein maximales Angebot von mindestens 10 USD ein.

Stellen Sie außerdem sicher, dass die enthaltenen Herausgeber oder Angebote aktiv sind und eine aktuelle Impressionsaktivität aufweisen.

+++

+++Ich habe eine Platzierung basierend auf der Prognose erstellt, aber es wurde nicht die in der Reach-Prognose angegebene Anzahl an einzigartigen Reichweiten erreicht. Warum?

Die REACH-Prognose ist nur eine Schätzung, und es wird erwartet, dass die tatsächlichen Ergebnisse aufgrund mehrerer Faktoren, die sich häufig ändern, wie Saisonabhängigkeit, Angebotswettbewerbsfähigkeit und Angebot und Nachfrage, variieren. Es wird nicht erwartet, dass er vollständig korrekt ist, aber am nützlichsten für direktionale Einblicke in Kampagnenstrategien, die möglicherweise die besten Ergebnisse erzielen können.

+++

+++Kann der Planer mit denselben Eingabeeinstellungen verschiedene Prognoseergebnisse generieren?

Der Planer generiert Prognosen auf der Basis der zuletzt beobachteten Daten, sodass die prognostizierte Leistung zu unterschiedlichen Zeiten variieren kann, obwohl die Planeinstellungen unverändert bleiben. Erwägen Sie, mehrere Prognosen für denselben Plan zu generieren und die Ergebnisse für jeden Plan zu exportieren.

+++

+++Kann ich die Planungsausgabe des Planers speichern?

Ja, Sie können eine Prognose in eine [!DNL Microsoft Excel] Tabelle exportieren, indem Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Export]** klicken. Das Arbeitsblatt erfasst die in der Reichweitenbudgetkurve angezeigten Informationen mithilfe von zwei Datenspalten: [!UICONTROL Budget] und [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [Über das DSP-Planer-Tool](planner-about.md)
>* [Erstellen eines Plans für die Reichweite von vernetzten Fernsehgeräten](planner-create.md)
>* [Duplizieren Sie einen Plan für die Reichweite eines verbundenen Fernsehers](planner-duplicate.md)
>* [Bearbeiten eines Connected TV-Reach-Plans](planner-edit.md)
>* [Exportieren eines Connected TV Reach Plans](planner-export.md)
>* [Regenerieren Sie die Prognose für einen Connected TV Reach Plan](planner-forecast.md)
>* [Archivieren eines Connected TV Reach Plans](planner-archive.md)
>* [Einstellungen für Connected TV Reach Plans](planner-settings.md)
