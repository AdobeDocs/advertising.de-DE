---
title: Über Simulationen
description: Erfahren Sie mehr über Portfoliosimulationen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
source-git-commit: 73528e2aa905216584d1aa294f5581d2bca88432
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 0%

---

# Über Simulationen

*Beta-Funktion*

Simulationsberichte zeigen den geschätzten Grenzwert der Kosten im Verhältnis zum Ziel, die Kosten, die Anzahl der Klicks und den Zielwert, den Sie für ein Portfolio auf verschiedenen Ausgabenebenen (Kosten) und den entsprechenden Tagesbudgets oder anderen Zielen erwarten können. Sie können optional [Ansicht anpassen](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) um zusätzliche Traffic-Metriken, Simulationseinstellungen und nur einen bestimmten Simulationstyp ([!UICONTROL Weekly] oder [!UICONTROL Custom]) anzuzeigen.

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Simulationstypen

* Automatisierte wöchentliche Simulationen

* Benutzerdefinierte, benutzergenerierte Simulationen

### Automatisierte wöchentliche Simulationen

Simulationsberichte werden automatisch jede Woche unter Verwendung der aktuellen Portfolioeinstellungen ausgeführt. Automatisierte wöchentliche Simulationen sind nur für Zeiträume verfügbar, in denen das Portfolio ([ oder aktiv) ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

#### Heruntergeladene wöchentliche Simulationen

Jede heruntergeladene wöchentliche Simulation besteht aus einer Arbeitsmappe. Jede Arbeitsmappe enthält die Zielgruppe für jede der 20 Schrittebenen und die prognostizierten Kosten, Klicks, den gewichteten Umsatz (Zielwert) und die Konversionsmetriken, die in der Zielgruppe enthalten sind, basierend auf der entsprechenden Zielgruppe. Für die ersten 20 Datenzeilen wurden keine Einschränkungen angewendet, für die übrigen Datenzeilen hingegen Einschränkungen.

#### Wöchentliche Simulationsdetails auf dem Bildschirm

Simulationsdetails auf dem Bildschirm zeigen visuelle und tabellarische Einblicke auf Portfolioebene. Für Daten nach Kampagne, Anzeigengruppen, Gebotseinheiten oder Gerät [laden Sie stattdessen die Simulation ](simulation-download.md).

##### Diagrammansicht

Die Diagrammansicht zeigt für jedes der 20 Ausgabenebenen den erwarteten Zielwert oder eine andere angegebene Metrik ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) für das Ausgabenziel an. Der Zielmittelpunkt wird identifiziert, und Sie können optional den Zielmittelpunkt ändern, um die prognostizierten Daten mithilfe dieses Werts anzuzeigen. Halten Sie den Cursor über einen beliebigen Punkt im Diagramm, um die Daten für diesen Punkt anzuzeigen.

Sie können die Daten mit und ohne angewendete Einschränkungen, mit angewendeten Einschränkungen und ohne angewendete Einschränkungen anzeigen. Wenn Sie Daten anzeigen, die Einschränkungen berücksichtigen, werden die angewendeten Einschränkungen über dem Diagramm identifiziert.

##### Tabellenansicht

Die Tabellenansicht zeigt die Zielausgaben für jede der 20 Ausgabenebenen. Sie enthält auch die entsprechenden geschätzten Kosten, Grenzkosten zu Zielwert, Klicks, Zielwert und Konversionsmetriken im Ziel des Portfolios für jede Ausgabenebene. Der Zielmittelpunkt wird identifiziert, und Sie können optional den Zielmittelpunkt ändern, um die prognostizierten Daten mithilfe dieses Werts anzuzeigen.

Sie können die Daten mit und ohne angewendete Einschränkungen, mit angewendeten Einschränkungen und ohne angewendete Einschränkungen anzeigen. Wenn Sie Daten anzeigen, die Einschränkungen berücksichtigen, werden die angewendeten Einschränkungen über dem Diagramm identifiziert.

##### Simulationseinstellungen

Die Simulationseinstellungen werden unter dem Diagramm oder der Tabelle als schreibgeschützt angezeigt.

##### Portfolio-Einstellungen

Um die schreibgeschützten Einstellungen für das entsprechende Portfolio anzuzeigen, klicken Sie oben rechts auf **[!UICONTROL Portfolio Settings]** .

### Benutzerdefinierte, benutzergenerierte Simulationen

Sie können einen benutzerdefinierten Simulationsbericht für ein einzelnes [optimiertes oder aktives](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) Portfolio unter Verwendung der aktuellen Portfolioeinstellungen oder unter Verwendung der benutzerdefinierten Portfolioeinstellungen mit oder ohne Einschränkungen auf Ebene der Gebotseinheiten erstellen, um die Ergebnisse anzuzeigen, die diese Einstellungen erzeugen würden, ohne sie tatsächlich zu ändern. Sie können beispielsweise eine benutzerdefinierte Simulation erstellen, um die Auswirkungen einer anderen Ausgabenstrategie oder eines anderen Lernbudgets zu sehen, ohne aktive Einschränkungen für Gebotseinheiten im Portfolio zu berücksichtigen. Sie können die geschätzte Leistung auf Portfolio-, Kampagnen-, Gebots- und Geräteebene anzeigen.

#### Heruntergeladene benutzerdefinierte Simulationen

Jede heruntergeladene benutzerdefinierte Simulation besteht aus einer Arbeitsmappe. Jede Arbeitsmappe enthält ein Arbeitsblatt für jede angegebene Entitätsebene der Simulation (Portfolios, Kampagnen, Anzeigengruppen, Gebotseinheiten), wenn Daten für diese Ebene verfügbar sind. Wenn Sie Daten auf Geräteebene angeben, enthält jedes Arbeitsblatt eine [!UICONTROL Device] Spalte. Jedes Arbeitsblatt enthält eine Zeile mit Daten für jede anwendbare Entität und (wenn für den Bericht angegeben) sowie einen Gerätetyp für jeden der 20 Schritte (z. B. eine Zeile pro Kampagne). Die Daten in jeder Zeile umfassen die projizierten Grenzkosten zum Umsatz, Kosten, Klicks, den gewichteten Umsatz (Zielwert), den Gerätetyp und die Konversionsmetriken, die in dem Ziel enthalten sind, basierend auf dem entsprechenden Ziel. Das Arbeitsblatt auf Portfolioebene enthält auch die Zielgruppe für die Schrittebenen, und das Arbeitsblatt auf Entitätsebene enthält das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Benutzerdefinierte Simulationsdetails auf dem Bildschirm

Simulationsdetails auf dem Bildschirm zeigen visuelle und tabellarische Einblicke auf Portfolioebene. Für Daten nach Kampagne, Anzeigengruppen, Gebotseinheiten oder Gerät [laden Sie stattdessen die Simulation ](simulation-download.md).

#### Diagrammansicht

Die Diagrammansicht zeigt den erwarteten Zielwert oder eine andere angegebene Metrik ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) für das Ausgabenziel für die angegebene Anzahl von Ausgabenebenen (Schritten) für die Simulation an. Der Zielmittelpunkt ist identifiziert. Halten Sie den Cursor über einen beliebigen Punkt im Diagramm, um die Daten für diesen Punkt anzuzeigen.

Wenn die Simulation unter Berücksichtigung von Abhängigkeiten erstellt wurde, werden die angewendeten Abhängigkeiten über dem Diagramm identifiziert.

##### Tabellenansicht

Die Tabellenansicht zeigt die Zielausgaben für jede der angegebenen Ausgabenebenen (Schritte) für die Simulation an. Es zeigt auch die entsprechenden geschätzten Kosten, Grenzkosten zu Zielwert, Klicks, Zielwert und Konversionsmetriken im Ziel des Portfolios für jede Ausgabenebene. Der Zielmittelpunkt ist identifiziert.

Wenn die Simulation unter Berücksichtigung von Abhängigkeiten erstellt wurde, werden die angewendeten Abhängigkeiten über dem Diagramm identifiziert.

##### Simulationseinstellungen

Die Simulationseinstellungen werden unter dem Diagramm oder der Tabelle als schreibgeschützt angezeigt.

##### Portfolio-Einstellungen

Um die schreibgeschützten Einstellungen für das entsprechende Portfolio anzuzeigen, klicken Sie oben rechts auf **[!UICONTROL Portfolio Settings]** .

## Die [!UICONTROL Simulations]

In der [!UICONTROL Simulations] Ansicht sind wöchentliche Simulationen und benutzerdefinierte Simulationen aufgeführt. Der Administrator und einige andere Benutzertypen <!-- Verify which --> benutzerdefinierte Simulationen sehen, die von anderen Benutzern erstellt wurden. Alle anderen Benutzer können nur die von ihnen erstellten benutzerdefinierten Simulationen sehen.

Die Datentabelle enthält den Fortschritt jeder Simulation, eine [!UICONTROL Target Midpoint] Spalte, die für jede Zeile ausgefüllt wird, und Spalten für Prognosen von Kosten/Impressionen/Klicks/Zielwerten, Istwerten und Genauigkeit. Sie können optional zusätzliche benutzerdefinierte Spalten hinzufügen (einschließlich Steigerungsmetriken, wie z. B. tatsächlicher Zielwert dividiert durch die Kosten).

### Verfügbare Aktionen {#simulations-actions}

* [Passen Sie die Ansicht ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md), um zusätzliche Metriken einzuschließen, einschließlich der geschätzten Impressions, der tatsächlichen Kosten, Klicks, Impressions und Zielwert, des Kosten-Ziel-Werts, der Kostengenauigkeit, der Klickgenauigkeit und der Zielwertgenauigkeit sowie der Differenz (Delta) zwischen dem prognostizierten und dem tatsächlichen Zielwert und dem Kosten-Ziel-Wert. Sie können auch Spalten für die meisten Simulationseinstellungen und den Simulationstyp ([!UICONTROL Custom] oder [!UICONTROL Weekly]) einbeziehen.

* [Generieren oder erneutes Ausführen einer benutzerdefinierten Simulation](simulation-create.md) für ein einzelnes Portfolio. Sie können entweder eine neue Simulation erstellen oder eine vorhandene Simulation in der Liste neu generieren.

* [Zeigen Sie eine wöchentliche oder benutzerdefinierte Simulation auf dem Bildschirm ](simulation-view.md).

* [Wöchentliche und benutzerdefinierte Simulationen herunterladen](simulation-download.md) als [!DNL Microsoft Excel] in ZIP-Dateien.

* Öffnen Sie über die Schaltfläche [!UICONTROL Spend Planner] das Tool für alte Ausgabenempfehlungen, mit dem Sie die optimale Ausgabenverteilung auf die Portfolios ermitteln können.

## Best Practices

Überwachen Sie Simulationsberichte in den folgenden Situationen:

* Bevor Sie ein Portfolio starten, schätzen Sie die Leistung ein, die Sie mit den entsprechenden Portfolioeinstellungen erwarten können. Verwenden Sie dazu Daten aus mindestens zwei Wochen. Wenn die Simulationsergebnisse eine geringere Leistung zeigen, als Sie anhand historischer Daten für die eingeschlossenen Kampagnen erwarten würden, untersuchen und beheben Sie die Probleme, bevor Sie das Portfolio starten.

* Nach jeder größeren Änderung an einem Portfolio, z. B. beim Hinzufügen einer Kampagne oder beim Ändern des Ziels. Wenn Sie Änderungen am Startdatum der Modellierung des Portfolios, an der Gewichtung einer Konversionsmetrik oder am Klickwert eines Ziels vornehmen, warten Sie bis zum nächsten Tag (nach 17 :00), um die Simulation auszuführen, wenn aktualisierte Kosten- und Umsatzmodelle verfügbar sind.

* Regelmäßige Überwachung der Leistungstrends auf der Ebene der Konversionsmetriken

>[!MORELIKETHIS]
>
>* [Simulation ausführen oder erneut ausführen](simulation-create.md)
>* [Anzeigen von Simulationsdetails](simulation-view.md)
>* [Simulationen herunterladen](simulation-download.md)
