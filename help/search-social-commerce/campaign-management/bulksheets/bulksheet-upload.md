---
title: Hochladen eines Bulksheets oder einer korrigierten Fehlerdatei
description: Erfahren Sie, wie Sie eine Bulksheet-Datei oder eine korrigierte Validierungsfehlerdatei für Landingpages manuell hochladen.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Hochladen eines Bulksheets oder einer korrigierten Fehlerdatei

Sie können Bulksheet-Dateien, korrigierte Validierungsfehlerdateien für Landingpages und andere korrigierte Fehlerdateien von Ihrem Gerät oder Netzwerk für [unterstützte Anzeigennetzwerke](bulksheet-about.md#bulksheet-functionality-by-network) hochladen. Alle benutzerdefinierten Spalten in der Datei werden beim Hochladen der Datei gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Upload Bulksheet]**.

1. Geben Sie Informationen in die [[!UICONTROL Upload Bulksheet] Einstellungen](#bulksheet-upload-settings) ein oder wählen Sie sie aus.

1. Klicken Sie auf **[!UICONTROL Apply]**.

Wenn die Aufgabe beginnt, wird die Datei in der Ansicht [!UICONTROL Bulksheets] aufgelistet. Nach Abschluss der Datei wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateierstellung jedoch fehlschlägt, wird in der [!UICONTROL Bulksheets]-Ansicht eine Fehlerdatei aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>Wenn Sie die Bulksheet-Daten in das Werbenetzwerk posten, können Sie den Fortschritt der Datei in der Spalte [!UICONTROL Progress] in der Ansicht [!UICONTROL Bulksheets] verfolgen. Die Veröffentlichung großer Datenmengen dauert länger.

## Upload-Einstellungen für Bulksheets und korrigierte Fehlerdateien {#bulksheet-upload-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL File to Upload] | Die hochzuladende Datei. Geben Sie die Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf <b>[!UICONTROL Browse]</b> klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.<br><br>Bulksheet-Dateien können bis zu 2,5 GB (etwa 2,5 Millionen Zeilen) aufweisen und müssen eine der folgenden Dateierweiterungen aufweisen: <i>[!UICONTROL .tsv]</i> (für tabulatorgetrennte Werte), <i>[!UICONTROL .txt]</i> (für Unicode-kompatiblen ASCII-Text), <i>[!UICONTROL .csv]</i> (für kommagetrennte Werte) oder <i>[!UICONTROL .zip]</i> (für komprimiertes ZIP-Format, das zu einer TSV-Datei dekomprimiert wird). Der Dateiname darf die folgenden Zeichen nicht enthalten: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Tipp:</b> Verwenden Sie für Daten, die internationale Zeichen enthalten, Dateien im TSV- oder TXT-Format. |
| [!UICONTROL Single Account] | Ob die Datei für ein Konto gilt: <i>[!UICONTROL Yes]</i> (für ein Konto) oder <i>[!UICONTROL No]</i> (für mehrere Konten). |
| [!UICONTROL Account (Search Engine)] | (Wenn die Datei für ein einzelnes Konto gilt) Das Konto, auf das die Daten hochgeladen werden sollen. |
| [!UICONTROL Search Engine] | (Wenn die Datei für mehrere Konten gilt) Das Werbenetzwerk, in das die Daten hochgeladen werden sollen. |
| [!UICONTROL Scheduling] | Wann oder ob die Datei im angegebenen Werbenetzwerk veröffentlicht wird:<ul><li><i>[!UICONTROL Post to ad network now]</i> (Standard): Beginnt mit dem sofortigen Veröffentlichen der Daten.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Beginnt mit der Veröffentlichung der Daten am angegebenen Datum und zur angegebenen Uhrzeit; der Standardwert ist morgen um 02:00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum in das Format TT/MM/JJJJ oder D/M/JJJJ ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") , um den Kalender zu öffnen, und [wählen Sie ein Datum aus](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um die Zeit zu ändern, geben Sie die Zeit im Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in Intervallen von 15 Minuten) aus der Liste aus.</li><li><i>[!UICONTROL Preview only]:</i> Um die Datei in Search, Social und Commerce hochzuladen, ohne die Daten in das Werbenetzwerk zu posten. Sie können die Datei auch später noch posten. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu posten.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für zutreffende Anzeigennetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Trackingcodes in Konten mit Ziel-URLs für alle Suchbegriffe, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung eingeschlossen werden sollen: <i>[!UICONTROL Yes]</i> (Standard) oder <i>[!UICONTROL No]</i>. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie <i>[!UICONTROL Yes]</i> auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Kontoeinstellungen oder Kampagneneinstellungen generiert. Standardmäßig werden Tracking-URLs nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert haben).<br><br>Wenn Sie <i>[!UICONTROL No]</i> auswählen, können Sie die Tracking-URLs später dennoch generieren, indem Sie die hochgeladene Datei manuell veröffentlichen.<br><br><b>Hinweis:</b> Wenn der Advertiser das Adobe Advertising-Konversions-Tracking verwendet und die Basis-URL geändert wurde, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass automatisch Tracking-URLs generiert und hochgeladen werden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen an Kampagnen in optimierten Portfolios basierend auf veröffentlichten Daten. Standardmäßig ist diese Option nicht aktiviert. Wenn Sie diese Option auswählen, gelten alle angegebenen Änderungen des Kampagnenbudgets, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (in der Regel beim nächsten Angebotszyklus).<br><br><b>Hinweis:</b> Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden in den Kampagnenverwaltungsansichten am nächsten Tag angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht Angebotsänderungen, die auf den Daten im Bulksheet bis zu einem bestimmten Enddatum basieren. Wenn Sie diese Option auswählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](bulksheet-download.md)
>* [Post-Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
