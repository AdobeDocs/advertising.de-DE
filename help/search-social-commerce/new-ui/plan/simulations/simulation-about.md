---
title: Über Simulationen
description: Erfahren Sie mehr über Portfoliosimulationen.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
TQID: 'https://experienceleague.adobe.com/9B4gKrZnnUmgj0LzxwM2CIkJsIO9Pe9R8RDR4mAmIwo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%
---
# Über Simulationen

*Beta-Funktion*

Simulationsberichte zeigen den geschätzten Grenzwert der Kosten im Verhältnis zum Ziel, die Kosten, die Anzahl der Klicks und den Zielwert, den Sie für ein Portfolio auf verschiedenen Ausgabenebenen (Kosten) und den entsprechenden Tagesbudgets oder anderen Zielen erwarten können. Sie können optional [Ansicht anpassen](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) um zusätzliche Traffic-Metriken, Simulationseinstellungen und nur einen bestimmten Simulationstyp ([!UICONTROL Weekly] oder [!UICONTROL Custom]) anzuzeigen.

<!--
 Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Simulationstypen

* Automatisierte wöchentliche Simulationen

* Benutzerdefinierte, benutzergenerierte Simulationen

### Automatisierte wöchentliche Simulationen

Search, Social und Commerce führen Simulationsberichte unter Verwendung der aktuellen Portfolioeinstellungen automatisch wöchentlich aus. Automatisierte wöchentliche Simulationen sind nur für Zeiträume verfügbar, in denen das Portfolio ([ oder aktiv) ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

Sie können [wöchentliche Simulationen für bis zu 100 Portfolios für ein ausgewähltes Ausführungsdatum aus der [!UICONTROL Portfolios] Ansicht herunterladen](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations) oder [einzelne Simulationen aus der [!UICONTROL Simulations] Ansicht herunterladen](simulation-download.md).

#### Heruntergeladene wöchentliche Simulationen

Sie können wöchentliche Simulationen als einzelne Arbeitsmappen herunterladen oder in einer Arbeitsmappe kombinieren. Der Bericht für jede Simulation enthält das Ziel für jede der 20 Schrittebenen und die prognostizierten Kosten, Klicks, den gewichteten Umsatz (Zielwert) und die Konversionsmetriken im Ziel, basierend auf dem entsprechenden Ziel. Die Simulation berechnet die ersten 20 Datenzeilen ohne Einschränkungen und die verbleibenden Datenzeilen mit Einschränkungen.

#### Wöchentliche Simulationsdetails auf dem Bildschirm

Simulationsdetails auf dem Bildschirm zeigen visuelle und tabellarische Einblicke auf Portfolioebene. Für Daten nach Kampagne, Anzeigengruppen, Gebotseinheiten oder Gerät [laden Sie stattdessen die Simulation ](simulation-download.md).

##### Diagrammansicht

Die Diagrammansicht zeigt für jedes der 20 Ausgabenebenen den erwarteten Zielwert oder eine andere angegebene Metrik ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) für das Ausgabenziel an. Das Diagramm identifiziert den Zielmittelpunkt, und Sie können optional den Zielmittelpunkt ändern, um die prognostizierten Daten mithilfe dieses Werts anzuzeigen. Halten Sie den Cursor über einen beliebigen Punkt im Diagramm, um die Daten für diesen Punkt anzuzeigen.

Sie können Daten mit Einschränkungen, ohne Einschränkungen oder mit beiden anzeigen. Wenn Sie Daten mit Einschränkungen anzeigen, identifiziert die Ansicht diese Einschränkungen oberhalb des Diagramms.

##### Tabellenansicht

Die Tabellenansicht zeigt die Zielausgaben für jede der 20 Ausgabenebenen. Sie enthält auch die entsprechenden geschätzten Kosten, Grenzkosten zu Zielwert, Klicks, Zielwert und Konversionsmetriken im Ziel des Portfolios für jede Ausgabenebene. Die Tabelle identifiziert den Zielmittelpunkt, und Sie können optional den Zielmittelpunkt ändern, um die prognostizierten Daten mithilfe dieses Werts anzuzeigen.

Sie können Daten mit Einschränkungen, ohne Einschränkungen oder mit beiden anzeigen. Wenn Sie Daten mit Einschränkungen anzeigen, identifiziert die Ansicht diese Einschränkungen oberhalb des Diagramms.

##### Simulationseinstellungen

Die Ansicht zeigt schreibgeschützte Simulationseinstellungen unterhalb des Diagramms oder der Tabelle an.

##### Portfolio-Einstellungen

Um die schreibgeschützten Einstellungen für das entsprechende Portfolio anzuzeigen, klicken Sie oben rechts auf **[!UICONTROL Portfolio Settings]** .

### Benutzerdefinierte, benutzergenerierte Simulationen

Sie können einen benutzerdefinierten Simulationsbericht für ein einzelnes [optimiertes oder aktives](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) Portfolio unter Verwendung der aktuellen Portfolioeinstellungen oder unter Verwendung der benutzerdefinierten Portfolioeinstellungen mit oder ohne Einschränkungen auf Ebene der Gebotseinheiten erstellen, um die Ergebnisse anzuzeigen, die diese Einstellungen erzeugen würden, ohne sie tatsächlich zu ändern. Sie können beispielsweise eine benutzerdefinierte Simulation erstellen, um die Auswirkungen einer anderen Ausgabenstrategie oder eines anderen Lernbudgets zu sehen, ohne aktive Einschränkungen für Gebotseinheiten im Portfolio zu berücksichtigen. Sie können die geschätzte Leistung auf Portfolio-, Kampagnen-, Gebots- und Geräteebene anzeigen.

#### Heruntergeladene benutzerdefinierte Simulationen

Sie können benutzerdefinierte Simulationen als einzelne Arbeitsmappen herunterladen oder in einer Arbeitsmappe kombinieren. Der Bericht für jede Simulation enthält ein Arbeitsblatt für jede von Ihnen angegebene Entitätsebene (Portfolios, Kampagnen, Anzeigengruppen, Gebotseinheiten), wenn Daten für diese Ebene verfügbar sind. Wenn Sie Daten auf Geräteebene angeben, enthält jedes Arbeitsblatt eine [!UICONTROL Device] Spalte. Jedes Arbeitsblatt enthält eine Zeile für jede anwendbare Entität und, wenn Sie Daten auf Geräteebene anfordern, einen Gerätetyp für jeden der 20 Schritte (z. B. eine Zeile pro Kampagne). Die Daten in jeder Zeile umfassen die projizierten Grenzkosten zum Umsatz, Kosten, Klicks, den gewichteten Umsatz (Zielwert), den Gerätetyp und Konversionsmetriken im Ziel, basierend auf dem entsprechenden Ziel. Das Arbeitsblatt auf Portfolioebene enthält auch die Zielgruppe für die Schrittebenen, und das Arbeitsblatt auf Entitätsebene enthält das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### Benutzerdefinierte Simulationsdetails auf dem Bildschirm

Simulationsdetails auf dem Bildschirm zeigen visuelle und tabellarische Einblicke auf Portfolioebene. Für Daten nach Kampagne, Anzeigengruppen, Gebotseinheiten oder Gerät [laden Sie stattdessen die Simulation ](simulation-download.md).

#### Diagrammansicht

Die Diagrammansicht zeigt den erwarteten Zielwert oder eine andere angegebene Metrik ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) für das Ausgabenziel für die angegebene Anzahl von Ausgabenebenen (Schritten) für die Simulation an. Das Diagramm identifiziert den Zielmittelpunkt. Halten Sie den Cursor über einen beliebigen Punkt im Diagramm, um die Daten für diesen Punkt anzuzeigen.

Berücksichtigt die Simulation Einschränkungen, werden diese über dem Diagramm angezeigt.

##### Tabellenansicht

Die Tabellenansicht zeigt die Zielausgaben für jede der angegebenen Ausgabenebenen (Schritte) für die Simulation an. Es zeigt auch die entsprechenden geschätzten Kosten, Grenzkosten zu Zielwert, Klicks, Zielwert und Konversionsmetriken im Ziel des Portfolios für jede Ausgabenebene. Die Tabelle identifiziert den Zielmittelpunkt.

Berücksichtigt die Simulation Einschränkungen, werden diese über dem Diagramm angezeigt.

##### Simulationseinstellungen

Die Ansicht zeigt schreibgeschützte Simulationseinstellungen unterhalb des Diagramms oder der Tabelle an.

##### Portfolio-Einstellungen

Um die schreibgeschützten Einstellungen für das entsprechende Portfolio anzuzeigen, klicken Sie oben rechts auf **[!UICONTROL Portfolio Settings]** .

## Die [!UICONTROL Simulations]

In der [!UICONTROL Simulations] Ansicht sind wöchentliche Simulationen und benutzerdefinierte Simulationen aufgeführt. Der Administrator und einige andere Benutzertypen können <!-- Verify which --> benutzerdefinierten Simulationen sehen, die von anderen Benutzern erstellt werden. Alle anderen Benutzer können nur die von ihnen erstellten benutzerdefinierten Simulationen sehen.

Die Datentabelle zeigt den Fortschritt jeder Simulation an, die [!UICONTROL Target Midpoint] für jede Zeile sowie Spalten für Kosten-/Impressions-/Klick-/Zielwert-Prognosen, Istwerte und Genauigkeit. Sie können optional zusätzliche benutzerdefinierte Spalten hinzufügen (einschließlich Steigerungsmetriken, wie z. B. tatsächlicher Zielwert dividiert durch die Kosten).

### Verfügbare Aktionen {#simulations-actions}

* [Passen Sie die Ansicht ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md), um zusätzliche Metriken einzuschließen, einschließlich der geschätzten Impressions, der tatsächlichen Kosten, Klicks, Impressions und Zielwert, des Kosten-Ziel-Werts, der Kostengenauigkeit, der Klickgenauigkeit und der Zielwertgenauigkeit sowie der Differenz (Delta) zwischen dem prognostizierten und dem tatsächlichen Zielwert und dem Kosten-Ziel-Wert. Sie können auch Spalten für die meisten Simulationseinstellungen und den Simulationstyp ([!UICONTROL Custom] oder [!UICONTROL Weekly]) einbeziehen.

* [Erstellen einer benutzerdefinierten Simulation](simulation-create.md#simulation-create) für ein einzelnes Portfolio, wobei die aktuellen Einstellungen des Portfolios als Standardeinstellungen verwendet werden.

* [Führen Sie bis zu 10 Simulationen mit den vorhandenen Einstellungen erneut ](simulation-create.md#rerun-a-simulation-with-the-existing-settings). Suche, Social und Commerce überspringen Simulationen mit dem Status [!UICONTROL Queued] oder [!UICONTROL In Progress].

* [Zeigen Sie eine wöchentliche oder benutzerdefinierte Simulation auf dem Bildschirm ](simulation-view.md).

* [Herunterladen von bis zu 10 wöchentlichen und benutzerdefinierten ](simulation-download.md) als einzelne [!DNL Microsoft Excel] oder als separate Arbeitsmappen in einer ZIP-Datei.

* Öffnen Sie über die Schaltfläche [!UICONTROL Spend Planner] das Tool für alte Ausgabenempfehlungen, mit dem Sie die optimale Ausgabenverteilung auf die Portfolios ermitteln können.

## Best Practices

Überwachen Sie Simulationsberichte in den folgenden Situationen:

* Bevor Sie ein Portfolio starten, schätzen Sie die Leistung ein, die Sie mit den entsprechenden Portfolioeinstellungen erwarten können. Verwenden Sie dazu Daten aus mindestens zwei Wochen. Wenn die Simulationsergebnisse eine geringere Leistung zeigen, als Sie anhand historischer Daten für die eingeschlossenen Kampagnen erwarten würden, untersuchen und beheben Sie die Probleme, bevor Sie das Portfolio starten.

* Nach jeder größeren Änderung an einem Portfolio, z. B. beim Hinzufügen einer Kampagne oder beim Ändern des Ziels. Wenn Sie Änderungen am Startdatum der Modellierung des Portfolios, an der Gewichtung einer Konversionsmetrik oder am Klickwert eines Ziels vornehmen, warten Sie bis zum nächsten Tag, um 17:00 Uhr PST, bis die Simulation ausgeführt wird, wenn aktualisierte Kosten- und Umsatzmodelle verfügbar sind.

* Regelmäßige Überwachung der Leistungstrends auf der Ebene der Konversionsmetriken

>[!MORELIKETHIS]
>
>* [Simulation ausführen oder erneut ausführen](simulation-create.md)
>* [Anzeigen von Simulationsdetails](simulation-view.md)
>* [Simulationen herunterladen](simulation-download.md)
