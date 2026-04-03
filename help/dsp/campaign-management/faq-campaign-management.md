---
title: Häufig gestellte Fragen zur Kampagnenverwaltung
description: Erfahren Sie mehr über die Kampagnenverwaltung, einschließlich der Latenzzeit für Änderungen und was passiert, wenn Sie während eines Fluges Budgetänderungen vornehmen.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Häufig gestellte Fragen zur Kampagnenverwaltung

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latenz bei Einstellungsänderungen

* Wann wird die Änderung wirksam, wenn Sie eine Platzierungs- oder Paketeinstellung ändern?

  Änderungen der Einstellungen werden in der Regel sofort wirksam, können jedoch bis zu 12 Stunden dauern.

  Wenn es der letzte Tag der Lieferung ist, nehmen Sie die Änderungen frühzeitig vor, sodass DSP genügend Zeit hat, das Paket basierend auf den Änderungen neu zu kalibrieren. Wenn Sie z. B. von gleichmäßiger Geschwindigkeit auf Frontlast-Geschwindigkeit wechseln, muss DSP neu überdenken, wie die Ausgaben über den Rest des Fluges verteilt werden. Nehmen Sie keine solche Änderung vor, wenn Sie am letzten Tag des Fluges nur noch eine Stunde Zeit haben.

## Budgetaktualisierungen während des Fluges

* Wie lange dauert es bei einer Änderung an einer Platzierung, bis DSP das Paketbudget neu zuweist?

  Die Budgetzuweisung basiert auf der Platzierungsleistung, die anhand eines 14-Tage-Durchschnitts bewertet wird. Änderungen an einer Platzierung führen nur dann zu Änderungen bei der Budgetzuweisung, wenn sie im 14-Tage-Durchschnitt Leistungsänderungen verursachen.

  Wenn Leistungsänderungen auftreten, ordnet DSP das Paketbudget im nächsten Budgetoptimierungszyklus, der um etwa Mitternacht (00) in der Zeitzone der Kampagne :00, entsprechend den Platzierungen zu.

* Wie wird das Budget neu zugewiesen, wenn eine Platzierung aus einem Paket entfernt und einem anderen Paket hinzugefügt wird?

  Der gesamte Ausgabenverlauf einer Platzierung wird an die Platzierung angehängt und bewegt sich mit ihr von Paket zu Paket.

  Wenn Sie eine Platzierung aus einem Paket entfernen, verfügt das Paket nicht mehr über einen Verlauf der Ausgaben der Platzierung. Das Paketbudget wird (Paketbudget - entferntes Platzierungsbudget) / Zeitintervall, das im Flug verbleibt. Das Paketbudget wird dann den Platzierungen zugewiesen, die im Paket verbleiben.

  Wenn Sie dieselbe Platzierung einem anderen Paket hinzufügen, berücksichtigt DSP den Ausgabenverlauf der Platzierung, wenn es das Budget für alle Platzierungen im neuen Paket zuweist.

* Wie ändert sich das Paket-Tempo am letzten Tag eines Fluges?

  Am letzten Tag eines Fluges wird der Tag von 24 auf 23 Stunden verkürzt, damit das Paket-Budget nicht überschritten wird. Außerdem ändert sich die Geschwindigkeits-Füllstrategie des Pakets automatisch in &quot;[!UICONTROL Frontload]&quot;, auch wenn sie auf &quot;[!UICONTROL even]&quot; eingestellt ist. Das bedeutet, dass 65 % des täglichen Budgets bis 11.00 :30 EST bereitgestellt werden sollten.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best Practices für die Einrichtung von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
