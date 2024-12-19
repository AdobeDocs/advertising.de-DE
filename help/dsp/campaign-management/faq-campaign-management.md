---
title: Häufig gestellte Fragen zu Campaign Management
description: Erfahren Sie mehr über die Kampagnenverwaltung, einschließlich der Latenzzeit für Änderungen und was passiert, wenn Sie während eines Fluges Budgetänderungen vornehmen.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latenz bei Einstellungsänderungen

* Wann wird die Änderung wirksam, wenn Sie eine Platzierungs- oder Paketeinstellung ändern?

  Änderungen der Einstellungen werden in der Regel sofort wirksam, können jedoch bis zu 12 Stunden dauern.

  Wenn es der letzte Tag der Lieferung ist, nehmen Sie die Änderungen früh am Tag vor, sodass DSP genügend Zeit hat, das Paket basierend auf den Änderungen neu zu kalibrieren. Wenn Sie z. B. von gleichmäßigem Tempo zu Frontlast-Geschwindigkeit wechseln, muss DSP neu überdenken, wie die Ausgaben über den Rest des Fluges verteilt werden. Nehmen Sie keine solche Änderung vor, wenn Sie am letzten Tag des Fluges nur noch eine Stunde Zeit haben.

## Budgetaktualisierungen während des Fluges

* DSP Wie lange dauert es bei einer Änderung an einer Platzierung, bis das Paketbudget neu zugewiesen wird?

  Die Budgetzuweisung basiert auf der Platzierungsleistung, die anhand eines 14-Tage-Durchschnitts bewertet wird. Änderungen an einer Platzierung führen nur dann zu Änderungen bei der Budgetzuweisung, wenn sie im 14-Tage-Durchschnitt Leistungsänderungen verursachen.

  Wenn Leistungsänderungen auftreten, ordnet DSP das Paketbudget im nächsten Budgetoptimierungszyklus, der um etwa Mitternacht (00:00 Uhr) in der Zeitzone der Kampagne stattfindet, entsprechend den Platzierungen zu.

* Wie wird das Budget neu zugewiesen, wenn eine Platzierung aus einem Paket entfernt und einem anderen Paket hinzugefügt wird?

  Der gesamte Ausgabenverlauf einer Platzierung wird an die Platzierung angehängt und bewegt sich mit ihr von Paket zu Paket.

  Wenn Sie eine Platzierung aus einem Paket entfernen, verfügt das Paket nicht mehr über einen Verlauf der Ausgaben der Platzierung. Das Paketbudget wird (Paketbudget - entferntes Platzierungsbudget) / Zeitintervall, das im Flug verbleibt. Das Paketbudget wird dann den Platzierungen zugewiesen, die im Paket verbleiben.

  Wenn Sie dieselbe Platzierung einem anderen Paket hinzufügen, berücksichtigt DSP den Ausgabenverlauf der Platzierung, wenn es das Budget für alle Platzierungen im neuen Paket zuweist.

* Wie ändert sich das Paket-Tempo am letzten Tag eines Fluges?

  Am letzten Tag eines Fluges wird der Tag von 24 auf 23 Stunden verkürzt, damit das Paket-Budget nicht überschritten wird. Außerdem ändert sich die Geschwindigkeits-Füllstrategie des Pakets automatisch in &quot;[!UICONTROL Frontload]&quot;, auch wenn sie auf &quot;[!UICONTROL even]&quot; eingestellt ist. Das bedeutet, dass 65 % des Tagesbudgets bis 11.30 Uhr EST bereitgestellt werden sollten.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
