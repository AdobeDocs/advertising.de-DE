---
title: Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds
description: Erfahren Sie mehr über das erweiterte Kampagnenmanagement, mit dem Sie automatisch die Kontostruktur verwalten und dynamische Anzeigen bereitstellen können, die auf Daten zu Ihrem Produkt- oder Servicebestand basieren.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Mit der Ansicht [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] für das erweiterte Kampagnenmanagement können Sie die Kontostruktur für Anzeigen-Netzwerke automatisch erstellen und aktualisieren und dynamische Anzeigen bereitstellen, die auf Daten zu Ihrem Produkt- oder Service-Inventar basieren. Sie können neue Dateien mit Produktdaten täglich oder beliebig oft hochladen oder direkt ein [!DNL Google] - oder [!DNL Microsoft] -Handelscenter-Konto verknüpfen. Verwenden Sie die Funktion, um:

* Erstellen Sie neue Kampagnen aus geordneten Datenquellen.

* Dynamische Aktualisierung von Text- und responsiven Suchanzeigen, [!DNL Google Ads] Shopping-Anzeigen oder [!DNL Microsoft Advertising] Shopping-Anzeigen bei jeder Verarbeitung neuer Daten mithilfe dynamischer Variablen für veränderliche Datenelemente (wie Preis oder Menge). Jedes Mal, wenn Sie die Daten ändern, werden die vorhandenen Anzeigen gelöscht und neue erstellt.

* Werbegruppen, Suchbegriffe und Anzeigen automatisch anhalten oder entfernen, wenn der Lagerbestand gemäß einem bestimmten Enddatum unter eine bestimmte Ebene fällt oder wenn eine vorhandene Komponente aus den Feed-Daten weggelassen wird.

Um Ihre Anzeigen einzurichten, erstellen Sie Inventar-Feed-Vorlagen, die Variablen (Platzhalter) enthalten, und ersetzen Sie die Variablen dann durch die tatsächlichen Datenspalten aus einer hochgeladenen Datei oder einem [Google- oder Microsoft-Händlercenter-Konto, das synchronisiert wird](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die Variablen können auch Modifikatorgruppen enthalten, die Sie in einer Datei einrichten, oder einzelne Zeilen in der Datei, um mehrere Anzeigen, Suchbegriffe, Kampagnen oder Anzeigengruppen für jede relevante Zeile in der Datendatei zu erstellen. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe zwei Modifikatoren enthält (&quot;für billig&quot;und &quot;zu einem Rabatt&quot;), werden für jedes Produkt zwei separate Anzeigen erstellt - eine für jeden Modifikator. Bei dynamischen Suchanzeigen [!DNL Google Ads] und [!DNL Microsoft Advertising] können Sie auch Werte für Anzeigenanpassungen einbeziehen.

| [!UICONTROL Ad Variation] Abschnitt der Vorlage | Modifikatoren in Search, Social und Commerce | Feed-Inhalte | Resultierende Anzeigen |
|----|----|----|----|
| Titel: Kaufen Sie High-End \{<i>Produktkategorie</i>\} &lt;<i>CheapList</i>>.<br><br>Beschreibung 1: Riesiges Inventar von \<i>Produktname</i>\}.<br><br>Beschreibung 2: Verfügbar unter \<i>Rabattprozentsatz</i>\}% Rabatt. | Werte für die Modifikatorgruppe &quot;CheapList&quot;:<br><br>&quot;für billig&quot;<br><br>&quot;zu einem Rabatt&quot; | Produktkategorie, Produktname, Rabattprozentsatz<br>Elektronik, iPods,10<br><br>Kleidung,Hemden,15<br><br><b>Hinweis:</b> Sie können Werte entweder mit Kommas oder Registerkarten trennen. | <u>Kaufen Sie High-End-Elektronik zu günstigen Preisen.</u><br>Riesiges Inventar von Tablets. Verfügbar zu 10% Rabatt.<br><br><u>Kaufen Sie High-End-Elektronik zu einem Rabatt.</u><br>Riesiges Inventar von Tablets. Verfügbar zu 10% Rabatt.<br><br><u>Kaufen Sie High-End-Kleidung zu günstigen Preisen.</u><br>Riesiges Inventar von Hemden. Verfügbar zu 15% Rabatt.<br><br><u>Kaufen Sie High-End-Kleidung zu einem Rabatt.</u><br>Riesiges Inventar von Hemden. Verfügbar zu 15% Rabatt. |

Nachdem Sie die Anzeigen generiert haben, können Sie sie optional überprüfen und dann im Werbenetzwerk veröffentlichen.

>[!NOTE]
>Informationen zum Erstellen oder Bearbeiten von Kampagnendaten in großen Mengen mithilfe von Tabellendateien finden Sie unter &quot;[Über die Verwaltung von Kampagnendaten mit Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;.

## Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Testen Sie zunächst mindestens eine Feed-Datei oder ein Konto und dann können Sie den Prozess vollständig automatisieren oder ihn bei jedem Schritt weiter steuern:

1. (Optional) Wenden Sie sich an Ihr Adobe-Account-Team, um ein FTP-Verzeichnis für die Speicherung von Datendateien einzurichten.

   Wenn Sie den FTP-Ordner verwenden, sucht der Feed-Dienst alle zwei Stunden nach neuen Dateien.

   Andernfalls können Sie Dateien in der Ansicht [!UICONTROL Advanced (ACM)] manuell hochladen.

1. Legen Sie [Parameter für die Verarbeitung von Feed-Daten fest](feed-settings-manage.md#feed-data-settings).

   Wenn Sie FTP verwenden, veröffentlichen Sie anfangs nicht automatisch Daten in den Werbenetzwerken. Nachdem Sie die Ausgabe aus der ersten Datei überprüft haben und mit den Ergebnissen zufrieden sind, können Sie die Einstellungen ändern.

1. Laden Sie eine Datendatei in das FTP-Verzeichnis hoch, laden Sie [manuell eine Datendatei ](feed-files-manage.md) in den Ordner [!UICONTROL Advanced (ACM) view] hoch oder aktivieren Sie den Zugriff auf ein Google- oder Microsoft-Handelscenter-Konto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).[

Um Dateien manuell hochzuladen, können Sie warten, bis Sie eine Vorlage erstellen, die die Datendatei verwendet.

1. (Optional) Erstellen Sie Gruppen von [Modifikatoren](modifiers-manage.md) , die in verschiedenen Datenfeldern in Feed-Datenvorlagen als Variablen verwendet werden.

1. [Erstellen Sie eine oder mehrere Vorlagen](ad-templates/ad-template-manage.md), die die Datenspalten verwenden, um Kampagnen, Anzeigengruppen, Suchbegriffe und/oder Anzeigenkopien für ein bestimmtes Anzeigennetzwerkkonto zu erstellen.

1. [Übertragen Sie Feed-Daten über die Vorlagen](feed-data-propagate.md), wodurch die Spaltennamen in der Vorlage durch Daten in der Datei oder dem Konto ersetzt werden. Abhängig von den Vorlagenoptionen erstellen Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Suchbegriffe) für die Anzeigen mit Standardeinstellungen oder ordnen die Anzeigen der bestehenden Kontostruktur zu.

1. (Optional) [Zeigen Sie die Ausgabe in der Vorschau an](propagated-data-view.md) in den [!UICONTROL Advanced (ACM)]-Ansichten und optional eine Zusammenfassung der Datenänderungen auf der Registerkarte [!UICONTROL Propagations] an.

1. [Posten Sie die Daten](propagated-data-post.md) in den relevanten Anzeigen-Netzwerk-Konten.

1. (Wenn Sie zum Hochladen Ihrer Daten FTP oder ein Händlernetzwerk-Konto verwenden (optional) Nachdem Sie die Ausgabe aus der ersten Feed-Datei validiert haben, bearbeiten Sie [die Parameter](feed-settings-manage.md#feed-data-settings), um nachfolgende Daten automatisch über die verknüpften Vorlagen zu übertragen und an die relevanten Anzeigennetzwerke zu posten.

1. (Wenn Sie neue Datendateien haben) Laden Sie bei Bedarf neue Dateien hoch, propagieren Sie die Daten über Vorlagen und posten Sie die Daten in das relevante Anzeigennetzwerk. Sie können die Daten optional in einem Schritt propagieren und posten.

>[!MORELIKETHIS]
>
>* [Wann werden Kontokomponenten durch Inventar-Feeds erstellt oder gelöscht?](when-are-components-created-deleted.md)
