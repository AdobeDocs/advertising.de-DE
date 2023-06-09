---
title: Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds
description: Erfahren Sie mehr über das erweiterte Kampagnenmanagement, mit dem Sie automatisch die Kontostruktur verwalten und dynamische Anzeigen bereitstellen können, die auf Daten zu Ihrem Produkt- oder Servicebestand basieren.
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '836'
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

## Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Testen Sie zunächst mindestens eine Feed-Datei oder ein Konto und dann können Sie den Prozess vollständig automatisieren oder ihn bei jedem Schritt weiter steuern:

1. (Optional) Wenden Sie sich an Ihr Adobe Account Team, um ein FTP-Verzeichnis für die Speicherung von Datendateien einzurichten.

   Wenn Sie den FTP-Ordner verwenden, sucht der Feed-Dienst alle zwei Stunden nach neuen Dateien.

   Andernfalls können Sie Dateien manuell im [!UICONTROL Advanced (ACM)] anzeigen.

1. Satz [Parameter für die Verarbeitung von Feed-Daten](feed-settings-manage.md#feed-data-settings).

   Wenn Sie FTP verwenden, veröffentlichen Sie anfangs nicht automatisch Daten in den Werbenetzwerken. Nachdem Sie die Ausgabe aus der ersten Datei überprüft haben und mit den Ergebnissen zufrieden sind, können Sie die Einstellungen ändern.

1. Hochladen einer Datendatei in das FTP-Verzeichnis, [manuell eine Datendatei hochladen](feed-files-manage.md) im [!UICONTROL Advanced (ACM) view]oder [Zugriff auf ein Google- oder Microsoft®-Merchant-Center-Konto aktivieren](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Um Dateien manuell hochzuladen, können Sie warten, bis Sie eine Vorlage erstellen, die die Datendatei verwendet.

1. (Optional) Erstellen Sie Gruppen von [modifiers](modifiers-manage.md) zur Verwendung als Variablen in verschiedenen Datenfeldern in Feed-Datenvorlagen.

1. [Erstellen einer oder mehrerer Vorlagen](ad-templates/ad-template-manage.md) die die Datenspalten verwenden, um Kampagnen, Anzeigengruppen, Suchbegriffe und/oder Anzeigenkopien für ein bestimmtes Anzeigennetzwerkkonto zu erstellen.

1. [Übertragen von Feed-Daten über die Vorlagen](feed-data-propagate.md), der die Spaltennamen in der Vorlage durch Daten in der Datei oder dem Konto ersetzt. Abhängig von den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Suchbegriffe) für die Anzeigen mit Standardeinstellungen oder ordnet die Anzeigen der vorhandenen Kontostruktur zu.

1. (Optional) [Vorschau der Ausgabe anzeigen](propagated-data-view.md) im [!UICONTROL Advanced (ACM)] Ansichten und optional eine Zusammenfassung der Datenänderungen auf der [!UICONTROL Propagations] Registerkarte.

1. [Posten der Daten](propagated-data-post.md) zu den entsprechenden Anzeigennetzkonten hinzugefügt.

1. (Wenn Sie zum Hochladen Ihrer Daten FTP oder ein Händlercenter-Konto verwenden; (optional) Nachdem Sie die Ausgabe aus der ersten Feed-Datei validiert haben, [Parameter bearbeiten](feed-settings-manage.md#feed-data-settings) um nachfolgende Daten automatisch über die verknüpften Vorlagen zu übertragen und an die entsprechenden Werbenetzwerke zu posten.

1. (Wenn Sie neue Datendateien haben) Laden Sie bei Bedarf neue Dateien hoch, propagieren Sie die Daten über Vorlagen und posten Sie die Daten in das relevante Anzeigennetzwerk. Sie können die Daten optional in einem Schritt propagieren und posten.

>[!MORELIKETHIS]
>
>* [Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?](when-are-components-created-deleted.md)
