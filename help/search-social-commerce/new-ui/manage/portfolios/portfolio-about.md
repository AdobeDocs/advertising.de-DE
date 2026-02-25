---
title: (Neue Benutzeroberfläche) Über Portfolios
description: Informationen zu Portfolios.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: de3c527bd359e0d5285b90e54278983104a2a5b5
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Über Portfolios

*Beta-Funktion*

Sie können Ihre Anzeigenkampagnen mithilfe von Portfolios gemeinsam verwalten (ähnlich wie Investmentportfolios). Ein Portfolio ist ein Satz von Anzeigenkampagnen oder Anzeigensets, einschließlich der zugehörigen Keywords und Anzeigen, die für ein einzelnes Geschäftsziel optimiert sind. Ein Ziel kann mehrere gewichtete Konversionen und ein einzelnes Budget oder ein Leistungsziel (z. B. ein monatliches Budget oder ein Ziel-ROI) umfassen. Da einzelne Kampagnen/Anzeigensätze, Keywords und Anzeigen unterschiedliche Leistungen aufweisen können (z. B. können sie unterschiedliche Beträge ausgeben oder unterschiedliche ROIs erzielen), nutzt die Optimierungsfunktion KI-gesteuerte Modelle, um das gesamte Portfolio zum Erreichen des Ziels zu steuern. Alle Kampagnen in einem Portfolio verwenden dieselbe Währung.

Einige Benutzerrollen können Portfolios erstellen und konfigurieren. Je nach Portfoliotyp können die Portfolioeinstellungen das Portfolioziel, die zugewiesenen Kampagnen, die Ausgabenstrategie, alle Gebotsbeschränkungen auf Portfolioebene und die Modellierungs- und Optimierungsparameter umfassen. Wenn Sie für Suche, Social und Commerce bereit sind, mit der Optimierung für ein Portfolio zu beginnen, ändern Sie den Status in „Optimiert“.

Sie können Portfolios optional in [Portfoliogruppen](portfolio-group-manage.md) gruppieren, sodass zusammengesetzte Daten für die gesamte Gruppe angezeigt werden können.

Je nach Ihrer Rolle können Sie möglicherweise Leistungssimulationen generieren, die prädiktive Modellierung verwenden, um Ihren optimalen Ausgabenpunkt und detaillierte Berichte zur Prognosegenauigkeit zu identifizieren.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Optimierungsunterstützung nach Angebotsstrategie {#optimization-by-bid-strategy}

Kampagnen sind für die Optimierung auf der Grundlage der Kampagnen- oder Anzeigengruppen-Bid-Strategie geeignet.

>[!NOTE]
>
>„Intelligente Gebote“ und „automatisierte Gebote“ werden oft synonym verwendet, sind aber nicht dasselbe. Smart Bidding bezieht sich nur auf [!DNL Google Ads] und [!DNL Microsoft Advertising] automatisierte Gebotsstrategien, die Auktionszeitgebote verwenden, was bedeutet, dass das Werbenetzwerk zum Zeitpunkt jeder Auktion für Konversionen oder Konversionswerte optimiert.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Angebotsstrategie | Intelligente Gebote? | Keyword-/Produktgruppenebenenangebot? | Unterstützungsebene | Objektivtyp | Gebotseinheit | Was legt Adobe fest? | Was legt das Werbenetzwerk fest? |
|---|---|---|---|---|---|---|---|
| Manueller CPC ([!DNL Google Ads] Option) | — | Ja | Erstellen, Bearbeiten, Optimieren | Ein einzelnes oder Ziel mit mehreren Eigenschaften mit beliebigem Gewichtungswert | Schlüsselwort + Übereinstimmungstyp + Kampagne | Keyword-Gebot, Kampagnenbudget, Gebotsanpassungswerte | Nicht zutreffend |
| ECPC (Enhanced CPC) | Ja | Ja | Erstellen, Bearbeiten, Optimieren | Ein einzelnes oder Ziel mit mehreren Eigenschaften mit beliebigem Gewichtungswert | Schlüsselwort + Übereinstimmungstyp + Kampagne | Keyword-Angebot, Kampagnenbudget | Passt Gebote in Echtzeit an |
| Klicks [1] | — | — | Erstellen, Bearbeiten, Optimieren | Keine; wird nur für Klicks optimiert | Campaign | Kampagnenbudget | Passt Gebote in Echtzeit an, um Klicks innerhalb des Budgets zu maximieren |
| Konversionen maximieren<br>(mit oder ohne TCPA) | Ja | — | Erstellen, Bearbeiten, Optimieren | Einzelobjektiv mit einer Gewichtung von 1 | Kampagne oder Anzeigengruppe ([!DNL Google Ads])<br>nur Kampagne ([!DNL Microsoft Advertising]) | Kampagnenbudget, Ziel-CPA bei <br>-TCPA kann eine eigenständige Bid-Strategie in [!DNL Microsoft Advertising] sein) | Passt Gebote in Echtzeit an, um Bestellungen/Leads innerhalb des Budgets zu maximieren und so ein CPA-Ziel bei festgelegtem Ziel zu erreichen |
| Konversionswert maximieren<br>(mit oder ohne TROAS) | Ja | — | Erstellen, Bearbeiten, Optimieren | Ziel mit mehreren Eigenschaften mit einem beliebigen Gewichtungswert oder Ziel mit einer einzelnen Eigenschaft mit einem Gewichtungswert größer als 1 (zur Darstellung eines Geldwerts) | Kampagne oder Anzeigengruppe ([!DNL Google Ads])<br>nur Kampagne ([!DNL Microsoft Advertising]) | Kampagnenbudget, Ziel-ROAS bei <br> (ROAS kann eine eigenständige Bid-Strategie in [!DNL Microsoft Advertising] sein) | Passt Gebote in Echtzeit an, um Umsatz/Gewinn innerhalb des Budgets zu maximieren und ein ROAS-Ziel bei der Zielsetzung zu erreichen |
| Ziel-Impression-Anteil | — | — | Erstellen, bearbeiten | Nicht zutreffend | Nicht zutreffend | K. A. - Kann keinem Portfolio zugewiesen werden | Passt Gebote in Echtzeit an ein Impression Share-Ziel an |

[^1]: Die Einstellung für die [!UICONTROL Maximize Clicks] Angebotsstrategie im Anzeigennetzwerk ist nicht identisch mit der [!UICONTROL Maximize Clicks] für Suche, Social und Commerce. Wenn die Bid-Strategie [!UICONTROL Maximize Clicks] ist, sollten Sie sie nur einem Portfolio mit Optimierung auf Kampagnen- oder Anzeigengruppenebene zuweisen, nicht einem Portfolio mit Optimierung auf Schlüsselwortebene.

## Portfolio-Status {#portfolio-status}

Ein Portfolio kann die folgenden Status aufweisen:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## Die [!UICONTROL Portfolios]

In der [!UICONTROL Portfolios] Ansicht werden Ihre vorhandenen Portfolios mit anpassbaren Leistungsdaten aufgelistet. Sie können [die Spalten innerhalb der Ansicht anpassen](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) und Daten so filtern, dass bestimmte Portfolios [aus der Symbolleiste ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) aus der [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

Oberhalb der Datentabelle können Sie ein Leistungsdiagramm mit bis zu drei Metriken öffnen, die sich über alle Portfolios in der Ansicht für den angegebenen Datumsbereich summieren.

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Verfügbare Aktionen

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Portfolio erstellen](portfolio-create.md)

* [Duplizieren eines Portfolios](portfolio-duplicate.md)

* [Portfolioeinstellungen bearbeiten](portfolio-edit.md)

* [Massenbearbeitung von Portfolioeinstellungen mithilfe von Bulksheet-Dateien](portfolio-bulksheets.md)

* [Anzeigen eines Leistungsdiagramms für alle Portfolios in der Ansicht](portfolio-view-performance-graph.md)

* [Anzeigen von Portfolioleistungsdetails](portfolio-details.md)

* [Daten in der [!UICONTROL Portfolios] herunterladen](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Erstellen eines Portfolios](portfolio-create.md)
>* [Duplizieren eines Portfolios](portfolio-duplicate.md)
>* [Bearbeiten eines Portfolios](portfolio-edit.md)
>* [Verwalten von Datenansichtsberichten aus der [!UICONTROL Portfolios] Ansicht](portfolio-view-report.md)
