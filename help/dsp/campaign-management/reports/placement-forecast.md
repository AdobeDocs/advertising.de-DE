---
title: Bericht zu Platzierungs-Forecasts anzeigen
description: Anzeigen der Anzahl der Impressionen, Ausgaben und des optimalen Maximalangebots, die für eine bestimmte Targeting-Strategie für eine Platzierung prognostiziert wurden.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Bericht zu Platzierungs-Forecasts anzeigen

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Das Tool für Platzierungs-Forecasts zeigt die prognostizierte Anzahl von Impressions, Ausgaben und das optimale Maximalgebot für eine bestimmte Zielgruppenstrategie an. Die Prognose wird auf der Grundlage des Gesamtbestands berechnet, der mit der Platzierung verfügbar ist, sowie der eindeutigen Benutzenden, die verfügbar sind.

>[!NOTE]
>
>* Postleitzahlen werden bei den Berechnungen für Platzierungs-Forecasts nicht berücksichtigt.
>* Für Platzierungen mit nur programmgesteuertem garantiertem (PG) Targeting wird keine Prognose generiert, da Verfügbarkeit und Ausgaben deterministisch sind.

## Prognoseinformationen

Die Prognose enthält folgende Angaben:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** Die geschätzten Kosten pro Tausend Impressionen (eCPM), die von den Zielgruppeneinstellungen erwartet werden können.

   * **[!UICONTROL Budget]:** Das geschätzte Budget für die Zielgruppeneinstellungen.

   * **[!UICONTROL Impression]:** Die geschätzte Anzahl von Impressionen für die Zielgruppeneinstellungen.

* **[!UICONTROL Budget Yield Curve]:** Die geschätzte Anzahl der Impressionen, die die Platzierung in verschiedenen Budgetstufen liefern kann, wenn alle anderen Zielgruppeneinstellungen identisch sind.

* **[!UICONTROL Max Bid Yield Curve]:** Die geschätzten Ausgaben für die Platzierung auf verschiedenen maximalen Angebotsebenen, wenn alle anderen Zielgruppeneinstellungen identisch sind.

* **[!UICONTROL Message]:** Enthält Informationen zum prognostizierten Output, einschließlich aller Szenarien, in denen die Prognose nicht erstellt werden konnte. Außerdem werden alle überprüften Zielgruppeneinstellungen hervorgehoben, die in diesem Szenario aufgrund fehlender Daten nicht berücksichtigt wurden.

### Budgetberechnung

* Für Platzierungen, die keinem Paket zugewiesen sind, wird das Platzierungsbudget für Berechnungen verwendet. Innerhalb eines Fluges wird das gleiche Gesamtbudget berechnet.

* Bei Platzierungen innerhalb eines Pakets wird das der Platzierung zugewiesene Budget für Berechnungen verwendet. Während des Fluges wird das der Platzierung zugewiesene Budget berechnet und in der Nachricht enthalten.

* Für Platzierungen, die zu einem Paket im Flug hinzugefügt werden, wird das Budget gleichmäßig auf der Grundlage der Anzahl der Platzierungen aufgeteilt. Wenn die Platzierung live geschaltet wird, wird das vom Paket zugewiesene Budget berechnet.

## Anforderungen

* Mindestausgaben: 25 USD pro Tag oder gleichwertig in der lokalen Währung pro Platzierung.

* Maximale Ausgaben: 15.000 USD pro Tag oder der Gegenwert in lokaler Währung pro Platzierung.

* Mindest-Max-Gebot, Höchstgebot: Es gibt ein Mindest-Max-Gebot (für die Budgetertragskurve) und ein Höchstgebot (für die Max-Gebotsertragskurve) nach Platzierungstyp. Diese Werte gelten global und berücksichtigen keine regionalen Unterschiede. Manchmal können diese Werte für den Zielbereich zu hoch oder zu niedrig sein.

* Historische Daten: Die Platzierungsprognose ist verfügbar, wenn ausreichende historische Daten verfügbar sind. Im Folgenden finden Sie Beispiele für Fälle, in denen nicht genügend historische Daten verfügbar sind:

   * Die Platzierung zielt auf eine neue Region für die Kampagne ab.

   * Die Platzierung zielt auf ein neues Lagerangebot für die Kampagne ab.

   * Die Platzierung verwendet einen neuen Anzeigentyp für die Kampagne.

     Eine Platzierung ist in der Regel eine Sammlung mehrerer Anzeigenvorlagen, die von anbieterseitigen Plattformen definiert werden. Selbst wenn die Platzierung schon lange besteht, kann das Prognose-Tool keine Prognose erstellen, wenn die zugrunde liegende Anzeigenvorlage neu ist.

## Bericht „Platzierungs-Forecast“ öffnen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne und dann auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Suchen Sie den Abschnitt **[!UICONTROL Forecast]** oben rechts. Klicken Sie bei Bedarf auf ![Prognose](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Manchmal ist die Prognose aufgrund des Browser-Cache möglicherweise nicht verfügbar. Löschen Sie in diesem Fall den Cache und versuchen Sie es erneut.

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
>* [Anzeigen der Platzierungs-Diagnoseberichte](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
