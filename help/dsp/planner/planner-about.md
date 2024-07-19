---
title: Über das DSP Planer-Tool
description: Erfahren Sie mehr über das Planer-Tool, um die einzigartige Reichweite von vernetzten TV-Platzierungen (CTV) gemäß den festgelegten Budget- und Targeting-Kriterien vorherzusagen.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Über das DSP Planer-Tool

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta-Funktion*

Mit dem Planer-Tool können Sie die einzigartige Reichweite von vernetzten TV-Platzierungen (CTV) auf Haushaltsebene entsprechend den festgelegten Budget- und Targeting-Kriterien vorhersagen, bevor Sie mit den Ausgaben für Inventar beginnen. Nachdem Sie mehrere Zielgruppenpläne ausgewertet haben, können Sie den Plan implementieren, der am besten mit den gewünschten Ergebnissen in Ihren Paketen und Platzierungen übereinstimmt.

Das Planer-Tool verwendet historische Gebots-, Impressions- und Reichweitendaten aus den letzten 90 Tagen, um die eindeutige Reichweite, den durchschnittlichen CPM, die durchschnittliche Häufigkeit und die Impressionen für eine Plankonfiguration zu schätzen.

## Planprognose

Jede Prognose besteht aus einer Prognosekurve für den erreichten Haushalt, aus der hervorgeht, wie viel mit den Planeinstellungen erreichbar ist. Bewegen Sie den Cursor über die Visualisierung, um die inkrementellen Reichweitenmöglichkeiten mit höheren Budgets anzuzeigen.

![Planerprognose](/help/dsp/assets/planner-forecast.png "Planerprognose")

Die Prognoseausgabe enthält auch einen Abschnitt &quot;[!UICONTROL Inventory Breakdown]&quot;, der zeigt, wie verschiedene Herausgeber zur einzigartigen Reichweite beitragen und wertvolle Entdeckungsmöglichkeiten bieten.

>[!NOTE]
>
>* Im Abschnitt [!UICONTROL Inventory Breakdown] werden nur Daten für den privaten und den [!UICONTROL On Demand] Bestand angezeigt.
>* Die geschätzte eindeutige Reichweite, die für zwei Herausgeber angezeigt wird, kann sich überschneiden.

## Die Planeransicht

In der Ansicht [!UICONTROL Planner] können Sie Ihre vorhandenen CTV-Reichweitenpläne anzeigen und neue erstellen.

Sie können die Vorschau für jeden Plan auch bearbeiten, duplizieren, exportieren, archivieren oder neu generieren.

## FAQs

++ Welche Inventartypen unterstützt das Planer-Tool?

Das Planer-Tool unterstützt alle Arten von Beständen, einschließlich programmgesteuerter (PG), privater Marketplace (PMP), [!UICONTROL On Demand] und öffentlicher Ressourcen. Um genaue Prognosen zu erstellen, schließen Sie Angebote mit mindestens 50.000 Impressionen in den letzten sieben Tagen ein.

+++

+++ Warum wird &quot;[!UICONTROL Unable to generate forecast]&quot;angezeigt?

Einer der häufigsten Gründe für diesen Fehler ist ein unzureichendes Budget oder ein nicht ausreichendes Maximalgebot. Verwenden Sie für optimale Ergebnisse ein Mindestbudget von 5000 USD. Wenn der Medientyp [!UICONTROL Connected TV] ausgewählt ist, geben Sie ein Höchstgebot von mindestens 10 USD ein.

Stellen Sie außerdem sicher, dass die eingeschlossenen Herausgeber oder Angebote aktiv sind und über eine Impressionsaktivität verfügen.

+++

+++I baute eine Platzierung auf der Grundlage der Prognose, erreichte aber nicht die in der Reichweitenvorhersage angegebene Menge an einzigartiger Reichweite. Warum?

Die Prognose ist nur eine Schätzung, und die tatsächlichen Ergebnisse werden aufgrund verschiedener Faktoren, die sich häufig ändern, voraussichtlich variieren, z. B. Saisonabhängigkeit, Gebotswettbewerbsfähigkeit sowie Angebot und Nachfrage. Es wird nicht erwartet, dass es vollständig präzise ist, aber am nützlichsten für Trend-Einblicke in Kampagnenstrategien, die potenziell die besten Ergebnisse erzielen können.

+++

++ Kann der Planer unterschiedliche Prognoseergebnisse mit denselben Eingabeeinstellungen generieren?

Der Planer generiert Prognosen basierend auf den neuesten beobachteten Daten, sodass die prognostizierte Ausgabe zu unterschiedlichen Zeiten variieren kann, auch wenn die Planeinstellungen unverändert bleiben. Erwägen Sie die Erstellung mehrerer Prognosen für denselben Plan und den Export der Ergebnisse für jeden Plan.

+++

++ + Kann ich die Planervorhersage speichern?

Ja, Sie können eine Vorschau in eine [!DNL Microsoft Excel] Tabelle exportieren, indem Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Export]** klicken. Die Tabelle erfasst die in der Reichweiten-Budgetkurve angezeigten Informationen mithilfe von zwei Datenspalten: [!UICONTROL Budget] und [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [Über das DSP Planer-Tool](planner-about.md)
>* [Erstellen eines Anbindungs-TV-Reichweitenplans](planner-create.md)
>* [Duplizieren eines Anbindungs-TV-Reichweitenplans](planner-duplicate.md)
>* [Bearbeiten eines Anbindungs-TV-Reichweitenplans](planner-edit.md)
>* [Einen Plan für die Anbindung an den Fernsehempfang exportieren](planner-export.md)
>* [Vorhersage für einen vernetzten TV-Reichweitenplan regenerieren](planner-forecast.md)
>* [Archivieren eines Anbindungs-TV-Reichweiten-Plans](planner-archive.md)
>* [Einstellungen für Pläne zur Anbindung an TV-Kanäle](planner-settings.md)
