---
title: Anzeigen des Berichts zur Platzierungsvorschau
description: Ermitteln Sie die Anzahl der Impressionen, Ausgaben und das für eine bestimmte Targeting-Strategie für eine Platzierung prognostizierte optimale maximale Angebot.
feature: DSP Placements
source-git-commit: bb44c1518a389a1decbedfa260939e75c8324aeb
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Anzeigen des Berichts zur Platzierungsvorschau

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Das Tool für die Platzierungsvorhersage zeigt die prognostizierte Anzahl von Impressionen, Ausgaben und das optimale Höchstgebot für eine bestimmte Targeting-Strategie. Die Prognose wird anhand des Gesamtinventars berechnet, das mit der Platzierung verfügbar ist, sowie anhand der verfügbaren Unique Users.

>[!NOTE]
>
>* Es wird keine Prognose für Platzierungen erstellt, deren Targeting nur programmgesteuert (PG) garantiert ist, da Verfügbarkeit und Ausgaben deterministisch sind.

## Informationen in der Prognose

Die Prognose enthält folgende Informationen:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** Die geschätzten Kosten pro Tausend Impressionen (eCPM), die die Targeting-Einstellungen voraussichtlich erreichen werden.

   * **[!UICONTROL Budget]:** Das geschätzte Budget für die Targeting-Einstellungen.

   * **[!UICONTROL Impression]:** Die geschätzte Anzahl von Impressionen für die Targeting-Einstellungen.

* **[!UICONTROL Budget Yield Curve]:** Die geschätzte Anzahl von Impressionen, die die Platzierung auf unterschiedlichen Budgetebenen liefern kann, wenn alle anderen Targeting-Einstellungen identisch sind.

* **[!UICONTROL Max Bid Yield Curve]:** Die geschätzten Ausgaben für die Platzierung auf unterschiedlichen Max. Gebotsebenen, wenn alle anderen Targeting-Einstellungen identisch sind.

* **[!UICONTROL Message]:** Enthält Informationen über die prognostizierte Ausgabe, einschließlich aller Szenarien, in denen die Prognose nicht erstellt werden konnte. Außerdem werden alle Targeting-Einstellungen hervorgehoben, die aufgrund fehlender Daten überprüft, aber in diesem Szenario nicht berücksichtigt wurden.

### Budgetberechnung

* Für Platzierungen, die keinem Paket zugewiesen sind, wird das Platzierungs-Budget für Berechnungen verwendet. Innerhalb eines Fluges wird das gleiche Gesamtbudget berechnet.

* Bei Platzierungen innerhalb eines Pakets wird das der Platzierung zugewiesene Budget für Berechnungen verwendet. Während des Fluges wird das für die Platzierung zugewiesene Budget berechnet und in der Nachricht angegeben.

* Bei Platzierungen, die zu einem Paket im Flug hinzugefügt werden, wird das Budget gleichmäßig auf die Anzahl der Platzierungen aufgeteilt. Wenn die Platzierung live geschaltet wird, wird das vom Paket zugewiesene Budget berechnet.

## Voraussetzungen

* Mindestausgaben: 25 USD pro Tag oder Gegenwert in Landeswährung pro Platzierung.

* Maximale Ausgaben: 15.000 USD pro Tag oder der Gegenwert in Landeswährung pro Platzierung.

* Mindest-Max. Angebot, Max. Angebot: Es gibt ein Mindest-Höchstgebot (für die Budget-Ertragskurve) und ein Maximal-Gebot (für die Max. Angebotsfeldkurve) nach Platzierungstyp. Diese Werte gelten global und berücksichtigen nicht regionale Unterschiede. Manchmal sind diese Werte für die Zielregion zu hoch oder zu niedrig.

* Historische Daten: Die Platzierungsvorhersage ist verfügbar, wenn ausreichende historische Daten verfügbar sind. Im Folgenden finden Sie Beispiele dafür, wann möglicherweise nicht genügend historische Daten verfügbar sind:

   * Die Platzierung richtet sich an eine neue Region für die Kampagne.

   * Die Platzierung zielt auf einen neuen Inventar-Deal für die Kampagne ab.

   * Die Platzierung verwendet einen neuen Anzeigentyp für die Kampagne.

     Eine Platzierung ist in der Regel eine Sammlung mehrerer Anzeigenvorlagen, die von angebotsseitigen Plattformen definiert werden. Selbst wenn die Platzierung also schon seit langem existiert, kann die zugrunde liegende Anzeigenvorlage neu sein und das Prognosetool wird nicht vorhersagen können.

## Platzierungsvorausschätzungsbericht öffnen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne und anschließend auf **[!UICONTROL Placements]**.

1. Klicken Sie neben dem Platzierungsnamen auf  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Suchen Sie die **[!UICONTROL Forecast]** oben rechts. Klicken Sie bei Bedarf auf ![Prognose](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Manchmal ist die Prognose aufgrund des Browser-Cache möglicherweise nicht verfügbar. Löschen Sie in diesem Fall den Cache und versuchen Sie es erneut.

>[!MORELIKETHIS]
>
>* [Über In-Platform-Berichte](campaign-reports-about.md)
>* [Anzeigen der platzierungsdiagnostischen Berichte](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
