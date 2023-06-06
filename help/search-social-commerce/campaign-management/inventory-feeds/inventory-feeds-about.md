---
title: Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds
description: Erfahren Sie mehr über das erweiterte Kampagnenmanagement, mit dem Sie automatisch die Kontostruktur verwalten und dynamische Anzeigen bereitstellen können, die auf Daten zu Ihrem Produkt- oder Servicebestand basieren.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Die [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] Ansicht für erweiterte Kampagnenverwaltung ermöglicht Ihnen, die Kontostruktur für Anzeigen-Netzwerke automatisch zu erstellen und zu aktualisieren und dynamische Anzeigen bereitzustellen, die auf Daten zu Ihrem Produkt- oder Service-Inventar basieren. Sie können neue Dateien mit Produktdaten täglich oder beliebig oft hochladen oder direkt auf eine [!DNL Google] oder [!DNL Microsoft®] Konto des Händlers. Verwenden Sie die Funktion, um:

* Erstellen Sie neue Kampagnen aus geordneten Datenquellen.

* Dynamisches Aktualisieren von Text und responsiven Suchanzeigen, [!DNL Google Ads] Shopping-Anzeigen oder [!DNL Microsoft® Advertising] Shopping-Anzeigen bei jeder Verarbeitung neuer Daten mithilfe dynamischer Variablen für veränderliche Datenelemente (z. B. Preis oder Menge). Jedes Mal, wenn Sie die Daten ändern, werden die vorhandenen Anzeigen gelöscht und neue erstellt.

* Werbegruppen, Suchbegriffe und Anzeigen automatisch anhalten oder entfernen, wenn der Lagerbestand gemäß einem bestimmten Enddatum unter eine bestimmte Ebene fällt oder wenn eine vorhandene Komponente aus den Feed-Daten weggelassen wird.

Um Ihre Anzeigen einzurichten, erstellen Sie Inventar-Feed-Vorlagen mit Variablen (Platzhalter) und ersetzen Sie die Variablen dann durch tatsächliche Datenspalten aus einer hochgeladenen Datei oder einem [Google- oder Microsoft®-Merchant-Center-Konto, das synchronisiert wird](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die Variablen können auch Modifikatorgruppen enthalten, die Sie in einer Datei einrichten, oder einzelne Zeilen in der Datei, um mehrere Anzeigen, Suchbegriffe, Kampagnen oder Anzeigengruppen für jede relevante Zeile in der Datendatei zu erstellen. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe zwei Modifikatoren enthält (&quot;für billig&quot;und &quot;zu einem Rabatt&quot;), werden für jedes Produkt zwei separate Anzeigen erstellt - eine für jeden Modifikator. Für [!DNL Google Ads] und [!DNL Microsoft® Advertising] dynamische Suchanzeigen, können Sie auch Werte für Anzeigenanpassungen einbeziehen.

| [!UICONTROL Ad Variation] Vorlagenabschnitt | Modifikatoren in Search, Social und Commerce | Feed-Inhalte | Resultierende Anzeigen |
|----|----|----|----|
| Titel: High-End \{ kaufen<i>Produktkategorie</i>\} &lt;<i>CheapList</i>>.<br><br>Beschreibung 1: Riesiges Inventar von \{<i>Produktname</i>\}.<br><br>Beschreibung 2: Verfügbar unter \{<i>Rabattprozentsatz</i>\}% Rabatt. | Werte für die Modifikatorgruppe &quot;CheapList&quot;:<br><br>&quot;billig&quot;<br><br>&quot;zu einem Rabatt&quot; | Produktkategorie, Produktname, Rabattprozentsatz<br>Elektronik,iPods,10<br><br>Bekleidung,Hemden,15<br><br><b>Hinweis:</b> Sie können Werte mit Kommas oder Tabulatoren trennen. | <u>Kaufen Sie High-End-Elektronik für günstige Preise.</u><br>Riesige Vorräte an Tabletten. Verfügbar zu 10% Rabatt.<br><br><u>Kaufen Sie High-End-Elektronik zu einem Rabatt.</u><br>Riesige Vorräte an Tabletten. Verfügbar zu 10% Rabatt.<br><br><u>Kaufen Sie hochwertige Kleidung zu günstigen Preisen.</u><br>Große Vorräte an Hemden. Verfügbar zu 15% Rabatt.<br><br><u>Kaufen Sie High-End-Kleidung zu einem Rabatt.</u><br>Große Vorräte an Hemden. Verfügbar zu 15% Rabatt. |

Nachdem Sie die Anzeigen generiert haben, können Sie sie optional überprüfen und dann im Werbenetzwerk veröffentlichen.

>[!NOTE]
>Informationen zum Erstellen oder Bearbeiten von Kampagnendaten in großen Mengen mithilfe von Tabellendateien finden Sie unter &quot;[Verwalten von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds](inventory-feeds-workflow.md)
>* [Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?](when-are-components-created-deleted.md)

