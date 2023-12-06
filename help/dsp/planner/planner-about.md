---
title: Über das DSP Planer-Tool
description: Erfahren Sie mehr über das Planer-Tool, um die einzigartige Reichweite von vernetzten TV-Platzierungen (CTV) gemäß den festgelegten Budget- und Targeting-Kriterien vorherzusagen.
feature: DSP Planner
source-git-commit: 9799ff5464d48e6258026ec997c5d5091576b9c6
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

![Planprognose](/help/dsp/assets/planner-forecast.png "Planprognose")

Die prognostizierte Ausgabe umfasst auch eine [!UICONTROL Inventory Breakdown] -Abschnitt, der zeigt, wie verschiedene Herausgeber zur einzigartigen Reichweite beitragen und wertvolle Entdeckungsmöglichkeiten bieten.

>[!NOTE]
>
>* Die [!UICONTROL Inventory Breakdown] -Abschnitt zeigt Daten nur für private und [!UICONTROL On Demand] Inventar.
>* Die geschätzte eindeutige Reichweite, die für zwei Herausgeber angezeigt wird, kann sich überschneiden.

## Die Planeransicht

Im [!UICONTROL Planner] anzeigen, können Sie Ihre vorhandenen CTV-Reichweitenpläne anzeigen und neue erstellen.

Sie können die Vorschau für jeden Plan auch bearbeiten, duplizieren, exportieren, archivieren oder neu generieren.

## FAQs

++ Welche Inventartypen unterstützt das Planer-Tool?

Das Planer-Tool unterstützt alle Arten von Beständen, einschließlich programmgesteuerter (PG), privater Marketplace (PMP), [!UICONTROL On Demand]und öffentlich. Um genaue Prognosen zu erstellen, schließen Sie Angebote mit mindestens 50.000 Impressionen in den letzten sieben Tagen ein.

+++

+++ Warum sehe ich &quot;[!UICONTROL Unable to generate forecast]?&quot;

Einer der häufigsten Gründe für diesen Fehler ist ein unzureichendes Budget oder ein nicht ausreichendes Maximalgebot. Verwenden Sie für optimale Ergebnisse ein Mindestbudget von 5000 USD. Wenn die Variable [!UICONTROL Connected TV] Medientyp ausgewählt ist, geben Sie ein Höchstgebot von mindestens 10 USD ein.

Stellen Sie außerdem sicher, dass die eingeschlossenen Herausgeber oder Angebote aktiv sind und über eine Impressionsaktivität verfügen.

+++

+++I baute eine Platzierung auf der Grundlage der Prognose, erreichte aber nicht die in der Reichweitenvorhersage angegebene Menge an einzigartiger Reichweite. Warum?

Die Prognose ist nur eine Schätzung, und die tatsächlichen Ergebnisse werden aufgrund verschiedener Faktoren, die sich häufig ändern, voraussichtlich variieren, z. B. Saisonabhängigkeit, Gebotswettbewerbsfähigkeit sowie Angebot und Nachfrage. Es wird nicht erwartet, dass es vollständig präzise ist, aber am nützlichsten für Trend-Einblicke in Kampagnenstrategien, die potenziell die besten Ergebnisse erzielen können.

+++

++ Kann der Planer unterschiedliche Prognoseergebnisse mit denselben Eingabeeinstellungen generieren?

Der Planer generiert Prognosen basierend auf den neuesten beobachteten Daten, sodass die prognostizierte Ausgabe zu unterschiedlichen Zeiten variieren kann, auch wenn die Planeinstellungen unverändert bleiben. Erwägen Sie die Erstellung mehrerer Prognosen für denselben Plan und den Export der Ergebnisse für jeden Plan.

+++

++ + Kann ich die Planervorhersage speichern?

Ja, Sie können eine Vorschau in eine [!DNL Microsoft® Excel] Tabelle durch Klicken auf **[!UICONTROL ...]** > **[!UICONTROL Export]** oben rechts. Die Tabelle erfasst die in der Reichweiten-Budgetkurve angezeigten Informationen mithilfe von zwei Datenspalten: [!UICONTROL Budget] und [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [Über das DSP Planer-Tool](planner-about.md)
>* [Erstellen eines Anbindungsplans für TV-Geräte](planner-create.md)
>* [Connected TV-Reichweitenplan duplizieren](planner-duplicate.md)
>* [Bearbeiten eines Anbindungs-TV-Reichweitenplans](planner-edit.md)
>* [Connected TV-Reichweitenplan exportieren](planner-export.md)
>* [Vorhersage für einen vernetzten TV-Reichweitenplan regenerieren](planner-forecast.md)
>* [Archivieren eines Anbindungsplans für TV](planner-archive.md)
>* [Einstellungen für Pläne zur Anbindung an das Fernsehen](planner-settings.md)
