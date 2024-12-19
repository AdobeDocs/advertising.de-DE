---
title: Automatisieren der Anzeigenverwaltung mithilfe von Inventar-Feeds
description: Erfahren Sie mehr über das erweiterte Kampagnen-Management, mit dem Sie automatisch die Kontostruktur verwalten und dynamische Anzeigen basierend auf Daten zu Ihrem Produkt- oder Service-Inventar bereitstellen können.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Automatisieren der Anzeigenverwaltung mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Die Ansicht [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] für erweiterte Kampagnenverwaltung ermöglicht es Ihnen, automatisch die Struktur der Werbenetzwerkkonten zu erstellen und zu aktualisieren und dynamische Anzeigen basierend auf den Daten über Ihr Produkt- oder Service-Inventar bereitzustellen. Sie können täglich oder beliebig oft neue Dateien mit Produktdaten hochladen oder direkt auf ein [!DNL Google]- oder [!DNL Microsoft] Merchant Center-Konto verlinken. Verwenden Sie die Funktion, um:

* Erstellen Sie neue Kampagnen aus sortierten Datenquellen.

* Dynamische Aktualisierung von Text- und responsiven Suchanzeigen, [!DNL Google Ads] Shopping-Anzeigen oder [!DNL Microsoft Advertising] Shopping-Anzeigen, wenn neue Daten verarbeitet werden, mithilfe dynamischer Variablen für veränderliche Datenelemente (z. B. Preis oder Menge). Jedes Mal, wenn Sie die Daten ändern, werden die vorhandenen Anzeigen gelöscht und neue erstellt.

* Werbegruppen, Keywords und Anzeigen werden automatisch angehalten oder entfernt, wenn der Bestand gemäß einem angegebenen Enddatum unter eine bestimmte Ebene fällt oder wenn eine vorhandene Komponente in den Feed-Daten weggelassen wird.

Erstellen Sie zum Einrichten Ihrer Anzeigen Inventar-Feed-Vorlagen mit Variablen (Platzhalter) und ersetzen Sie dann die Variablen durch die tatsächlichen Datenspalten aus einer hochgeladenen Datei oder einem synchronisierten [Google- oder Microsoft-Händlerkonto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Die Variablen können auch Modifikatorgruppen enthalten, die Sie in einer Datei oder einzelnen Zeilen in der Datei einrichten, um mehrere Anzeigen, Schlüsselwörter, Kampagnen oder Anzeigengruppen für jede anwendbare Zeile in der Datendatei zu erstellen. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe zwei Modifikatoren („billig“ und „mit Rabatt„) enthält, werden für jedes Produkt zwei separate Anzeigen erstellt - eine für jeden Modifikator. Für [!DNL Google Ads] und [!DNL Microsoft Advertising] dynamische Suchanzeigen können Sie auch Werte für Anzeigenanpassungen einbeziehen.

| Abschnitt der Vorlage [!UICONTROL Ad Variation] | Modifikatoren in Search, Social und Commerce | Feed-Inhalte | Entsprechende Anzeigen |
|----|----|----|----|
| Titel: Kaufen Sie High-End \{<i>Produktkategorie</i>\} &lt;<i>CheapList</i>>.<br><br>Beschreibung 1: Riesiger Bestand von \{<i>Product Name</i>\}.<br><br>Beschreibung 2: Verfügbar unter \{<i>Rabatt in Prozent</i>\} % Rabatt. | Werte für die Modifikatorgruppe „CheapList“:<br><br>„for Cheap“<br><br>„at a Discount“ | Produktkategorie,Produktname,Rabatt-Prozentsatz<br>Elektronik,iPods,10<br><br>Bekleidung,Hemden,15<br><br><b>Hinweis:</b> Sie können Werte durch Kommas oder Tabulatoren trennen. | <u>Kaufen Sie High-End-Elektronik für günstig.</u><br>Großer Bestand an Tablets. Erhältlich mit 10% Rabatt.<br><br><u>Kaufen Sie High-End-Elektronik zu einem Rabatt.</u><br>Großer Bestand an Tablets. Erhältlich mit 10% Rabatt.<br><br><u>Kaufen Sie High-End-Kleidung für günstig.</u><br>Riesige Auswahl an Hemden. Erhältlich mit 15% Rabatt.<br><br><u>Kaufen Sie High-End-Kleidung zu einem Rabatt.</u><br>Riesige Auswahl an Hemden. Erhältlich mit 15% Rabatt. |

Nachdem Sie die Anzeigen erstellt haben, können Sie sie optional überprüfen und dann im Anzeigennetzwerk posten.

>[!NOTE]
>Informationen zum Massenerstellen oder Bearbeiten von Kampagnendaten mithilfe von Kalkulationstabellendateien finden Sie unter &quot;[ zum Verwalten von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

## Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Zunächst sollten Sie mindestens eine Feed-Datei oder ein Konto testen und dann den Prozess vollständig automatisieren oder bei jedem Schritt weiter steuern:

1. (Optional) Wenden Sie sich an Ihr Adobe-Konto-Team, um ein FTP-Verzeichnis für das Ablegen von Datendateien einzurichten.

   Wenn Sie das FTP-Verzeichnis verwenden, sucht der Feed-Service alle zwei Stunden nach neuen Dateien.

   Andernfalls können Sie Dateien manuell in die [!UICONTROL Advanced (ACM)] hochladen.

1. Legen Sie [Parameter für die Verarbeitung von Feed-Daten](feed-settings-manage.md#feed-data-settings) fest.

   Wenn Sie FTP verwenden, veröffentlichen Sie zunächst nicht automatisch Daten in den Werbenetzwerken. Nachdem Sie die Ausgabe aus Ihrer ersten Datei überprüft haben und mit den Ergebnissen zufrieden sind, können Sie die Einstellungen ändern.

1. Laden Sie eine Datendatei in das FTP-Verzeichnis hoch [laden Sie eine Datendatei manuell ](feed-files-manage.md) die [!UICONTROL Advanced (ACM) view] hoch oder [aktivieren Sie den Zugriff auf ein Google- oder Microsoft-Händlerkonto](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Um Dateien manuell hochzuladen, können Sie warten, bis Sie eine Vorlage erstellen, die die Datendatei verwendet.

1. (Optional) Erstellen Sie Gruppen von [Modifikatoren](modifiers-manage.md) die als Variablen in verschiedenen Datenfeldern in Feed-Datenvorlagen verwendet werden können.

1. [Erstellen Sie eine oder mehrere Vorlagen](ad-templates/ad-template-manage.md) die die Datenspalten verwenden, um Kampagnen, Anzeigengruppen, Keywords und/oder Anzeigenkopien für ein bestimmtes Anzeigennetzwerkkonto zu erstellen.

1. [Verbreiten Sie Feed-Daten über die Vorlagen](feed-data-propagate.md) wodurch die Spaltennamen in der Vorlage durch Daten in der Datei oder im Konto ersetzt werden. Je nach den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Keywords) für die Anzeigen mit Standardeinstellungen oder ordnet die Anzeigen der bestehenden Kontostruktur zu.

1. (Optional) [Vorschau der Ausgabe](propagated-data-view.md) in den [!UICONTROL Advanced (ACM)] Ansichten und optional eine Zusammenfassung der Datenänderungen auf der Registerkarte &quot;[!UICONTROL Propagations]&quot; anzeigen.

1. [Daten posten](propagated-data-post.md) an die entsprechenden Anzeigennetzwerkkonten.

1. (Wenn Sie FTP oder ein Merchant Center-Konto verwenden, um Ihre Daten hochzuladen; optional) Nachdem Sie die Ausgabe aus der ersten Feed-Datei validiert haben, [bearbeiten Sie die Parameter](feed-settings-manage.md#feed-data-settings), um nachfolgende Daten automatisch über die zugehörigen Vorlagen weiterzugeben und an die entsprechenden Werbenetzwerke zu senden.

1. (Wenn Sie neue Datendateien haben) Laden Sie bei Bedarf neue Dateien hoch, übertragen Sie die Daten über Vorlagen und senden Sie die Daten an das entsprechende Werbenetzwerk. Sie können die Daten optional in einem Schritt weitergeben und posten.

>[!MORELIKETHIS]
>
>* [Wann werden Kontokomponenten von Inventar-Feeds erstellt oder gelöscht?](when-are-components-created-deleted.md)
