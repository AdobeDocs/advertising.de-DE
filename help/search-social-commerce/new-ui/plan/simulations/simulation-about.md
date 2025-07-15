---
title: Über Simulationen
description: Erfahren Sie mehr über Portfoliosimulationen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Über Simulationen

*Beta-Funktion*

Simulationsberichte zeigen den geschätzten Grenzwert der Kosten im Verhältnis zum Ziel, die Kosten, die Anzahl der Klicks und den Zielwert, den Sie für ein Portfolio auf verschiedenen Ausgabenebenen (Kosten) und den entsprechenden Tagesbudgets oder anderen Zielen erwarten können. Sie können optional die Ansicht <!-- add link -->, um zusätzliche Traffic-Metriken, Simulationseinstellungen und nur einen bestimmten Simulationstyp ([!UICONTROL Weekly] oder [!UICONTROL Custom]) anzuzeigen.

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Simulationstypen

* **Automatisierte wöchentliche Simulationen:** Simulationsberichte werden automatisch jede Woche unter Verwendung der aktuellen Portfolioeinstellungen ausgeführt. Automatisierte wöchentliche Simulationen sind nur für Zeiträume verfügbar, in denen das Portfolio ([ oder aktiv) ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Jede heruntergeladene wöchentliche Simulation besteht aus einer Arbeitsmappe. Jede Arbeitsmappe enthält die Zielgruppe für jede der 20 Schrittebenen und die prognostizierten Kosten, Klicks, den gewichteten Umsatz (Zielwert) und die Konversionsmetriken, die in der Zielgruppe enthalten sind, basierend auf der entsprechenden Zielgruppe. Für die ersten 20 Datenzeilen wurden keine Einschränkungen angewendet, für die übrigen Datenzeilen hingegen Einschränkungen.

* **Benutzerdefinierte, benutzergenerierte Simulationen:** Sie können einen benutzerdefinierten Simulationsbericht für ein einzelnes [](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) optimiertes oder aktives) Portfolio erstellen, indem Sie die aktuellen Portfolioeinstellungen verwenden oder benutzerdefinierte Portfolioeinstellungen verwenden, um die Ergebnisse anzuzeigen, die diese Einstellungen erzeugen würden, ohne sie tatsächlich zu ändern. Sie können beispielsweise eine benutzerdefinierte Simulation erstellen, um die Auswirkungen der Verwendung einer anderen Ausgabenstrategie oder eines anderen Lernbudgets zu <!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. Sie können die geschätzte Leistung auf Portfolio-, Kampagnen-, Gebots- und Geräteebene anzeigen. Benutzerdefinierte Simulationen übernehmen die Ausgabenbeschränkungseinstellung aus dem Portfolio.

  >[!NOTE]
  >
  > Das neue benutzerdefinierte Simulationsformular verwendet dieselben Einstellungen wie das alte Formular, mit dem Unterschied, dass es die Informationen zu den Beschränkungen der Gebotseinheiten von den Portfolioeinstellungen übernimmt. Sie haben nicht die Möglichkeit, Einschränkungen für Gebotseinheiten zu ignorieren, wie Sie es auf der Seite mit den alten benutzerdefinierten Simulationseinstellungen getan haben.

  Jede heruntergeladene benutzerdefinierte Simulation besteht aus einer Arbeitsmappe. Jede Arbeitsmappe enthält ein Arbeitsblatt für jede angegebene Entitätsebene der Simulation (Portfolios, Kampagnen, Anzeigengruppen, Gebotseinheiten), wenn Daten für diese Ebene verfügbar sind. Wenn Sie Daten auf Geräteebene angeben, enthält jedes Arbeitsblatt eine [!UICONTROL Device] Spalte. Jedes Arbeitsblatt enthält eine Zeile mit Daten für jede anwendbare Entität und (wenn für den Bericht angegeben) sowie einen Gerätetyp für jeden der 20 Schritte (z. B. eine Zeile pro Kampagne). Die Daten in jeder Zeile umfassen die projizierten Grenzkosten zum Umsatz, Kosten, Klicks, den gewichteten Umsatz (Zielwert), den Gerätetyp und die Konversionsmetriken, die in dem Ziel enthalten sind, basierend auf dem entsprechenden Ziel. Das Arbeitsblatt auf Portfolioebene enthält auch die Zielgruppe für die Schrittebenen, und das Arbeitsblatt auf Entitätsebene enthält das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## Die [!UICONTROL Simulations]

In der [!UICONTROL Simulations] Ansicht sind wöchentliche Simulationen und benutzerdefinierte Simulationen aufgeführt. Der Administrator und einige andere Benutzertypen <!-- Verify which --> benutzerdefinierte Simulationen sehen, die von anderen Benutzern erstellt wurden. Alle anderen Benutzer können nur die von ihnen erstellten benutzerdefinierten Simulationen sehen.

Die Datentabelle enthält den Fortschritt jeder Simulation, eine [!UICONTROL Target Midpoint] Spalte, die für jede Zeile ausgefüllt wird, und Spalten für Prognosen von Kosten/Impressionen/Klicks/Zielwerten, Istwerten und Genauigkeit. Sie können optional zusätzliche benutzerdefinierte Spalten hinzufügen (einschließlich Steigerungsmetriken, wie z. B. tatsächlicher Zielwert dividiert durch die Kosten).

### Verfügbare Aktionen {#simulations-actions}

* [Passen Sie die Ansicht ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md), um zusätzliche Metriken einzuschließen, einschließlich der geschätzten Impressions, der tatsächlichen Kosten, Klicks, Impressions und Zielwert, des Kosten-Ziel-Werts, der Kostengenauigkeit, der Klickgenauigkeit und der Zielwertgenauigkeit sowie der Differenz (Delta) zwischen dem prognostizierten und dem tatsächlichen Zielwert und dem Kosten-Ziel-Wert. Sie können auch Spalten für die meisten Simulationseinstellungen und den Simulationstyp ([!UICONTROL Custom] oder [!UICONTROL Weekly]) einbeziehen.

* [Generieren oder erneutes Ausführen einer benutzerdefinierten Simulation](simulation-create.md) für ein einzelnes Portfolio. Sie können entweder eine neue Simulation erstellen oder eine vorhandene Simulation in der Liste neu generieren.

* [Wöchentliche und benutzerdefinierte Simulationen herunterladen](simulation-download.md) als [!DNL Microsoft Excel] in ZIP-Dateien.

* Öffnen Sie über die Schaltfläche [!UICONTROL Spend Planner] das Tool für alte Ausgabenempfehlungen, mit dem Sie die optimale Ausgabenverteilung auf die Portfolios ermitteln können.

## Best Practices

Überwachen Sie Simulationsberichte in den folgenden Situationen:

* Bevor Sie ein Portfolio starten, schätzen Sie die Leistung ein, die Sie mit den entsprechenden Portfolioeinstellungen erwarten können. Verwenden Sie dazu Daten aus mindestens zwei Wochen. Wenn die Simulationsergebnisse eine geringere Leistung zeigen, als Sie anhand historischer Daten für die eingeschlossenen Kampagnen erwarten würden, untersuchen und beheben Sie die Probleme, bevor Sie das Portfolio starten.

* Nach jeder größeren Änderung an einem Portfolio, z. B. beim Hinzufügen einer Kampagne oder beim Ändern des Ziels. Wenn Sie Änderungen am Startdatum der Modellierung des Portfolios, an der Gewichtung einer Konversionsmetrik oder am Klickwert eines Ziels vornehmen, warten Sie bis zum nächsten Tag, um 17:00 Uhr PST, bis die Simulation ausgeführt wird, wenn aktualisierte Kosten- und Umsatzmodelle verfügbar sind.

* Regelmäßige Überwachung der Leistungstrends auf der Ebene der Konversionsmetriken

>[!MORELIKETHIS]
>
>* [Simulation ausführen oder erneut ausführen](simulation-create.md)
>* [Simulationen herunterladen](simulation-download.md)
