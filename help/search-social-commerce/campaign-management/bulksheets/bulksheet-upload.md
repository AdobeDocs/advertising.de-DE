---
title: Hochladen einer Bulksheet- oder korrigierten Fehlerdatei
description: Erfahren Sie, wie Sie manuell eine Bulksheet-Datei oder eine korrigierte Fehlerdatei für die Landingpage-Validierung hochladen.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Hochladen einer Bulksheet- oder korrigierten Fehlerdatei

Sie können Bulksheet-Dateien, korrigierte Fehlerdateien für die Landingpage-Validierung und andere korrigierte Fehlerdateien von Ihrem Gerät oder Netzwerk für (unterstützte [-Netzwerke) ](bulksheet-about.md#bulksheet-functionality-by-network). Alle benutzerdefinierten Spalten in der Datei werden beim Hochladen der Datei gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Upload Bulksheet]**.

1. Geben Sie Informationen in die [[!UICONTROL Upload Bulksheet] ein oder wählen Sie diese aus](#bulksheet-upload-settings).

1. Klicken Sie auf **[!UICONTROL Apply]**.

Wenn die Aufgabe beginnt, wird die Datei in der [!UICONTROL Bulksheets] angezeigt. Wenn die Datei vollständig ist, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateigenerierung jedoch fehlschlägt, wird eine Fehlerdatei in der [!UICONTROL Bulksheets]-Ansicht aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>Wenn Sie die Bulksheet-Daten an das Anzeigennetzwerk senden, können Sie den Fortschritt der Datei in der Spalte [!UICONTROL Progress] in der [!UICONTROL Bulksheets] verfolgen. Die Veröffentlichung großer Datenmengen dauert länger.

## Hochladen von Einstellungen für Bulksheets und korrigierte Fehlerdateien {#bulksheet-upload-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL File to Upload] | Die hochzuladende Datei. Geben Sie die Datei an, indem Sie entweder den vollständigen Pfad und Dateinamen eingeben oder auf <b>[!UICONTROL Browse]</b> klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.<br><br>Bulksheet-Dateien können bis zu 2,5 GB (etwa 2,5 Millionen Zeilen) groß sein und müssen eine der folgenden Dateierweiterungen aufweisen: <i>[!UICONTROL .tsv]</i> (für tabulatorgetrennte Werte), <i>[!UICONTROL .txt]</i> (für Unicode-kompatiblen ASCII-Text), <i>[!UICONTROL .csv]</i> (für kommagetrennte Werte) oder <i>[!UICONTROL .zip]</i> (für das komprimierte ZIP-Format, das in eine TSV-Datei dekomprimiert wird). Der Dateiname darf die folgenden Zeichen nicht enthalten: `# % &amp; * \| \ : " < > . ? /`<br><br><b>Tipp:</b> Verwenden Sie für Daten, die internationale Zeichen enthalten, Dateien im TSV- oder TXT-Format. |
| [!UICONTROL Single Account] | Ob die Datei für ein Konto gilt: <i>[!UICONTROL Yes]</i> (für ein Konto) oder <i>[!UICONTROL No]</i> (für mehrere Konten). |
| [!UICONTROL Account (Search Engine)] | (Wenn die Datei für ein einzelnes Konto gilt) Das Konto, in das die Daten hochgeladen werden sollen. |
| [!UICONTROL Search Engine] | (Wenn die Datei für mehrere Konten gilt) Das Anzeigennetzwerk, in das die Daten hochgeladen werden sollen. |
| [!UICONTROL Scheduling] | Wann oder ob die Datei an das angegebene Anzeigennetzwerk gesendet werden soll:<ul><li><i>[!UICONTROL Post to ad network now]</i> (Standard): Beginnt sofort mit der Veröffentlichung der Daten.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Beginnt mit dem Posten der Daten zum angegebenen Datum und zur angegebenen Uhrzeit; der Standardwert ist morgen um :00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum im Format TT/MM/JJJJ oder TT/M/JJJJ ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender"), um den Kalender zu öffnen und [Datum auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um die Zeit zu ändern, geben Sie die Zeit im Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in 15-Minuten-Intervallen) aus der Liste aus.</li><li><i>[!UICONTROL Preview only]:</i> Um die Datei in Search, Social und Commerce hochzuladen, ohne die Daten an das Werbenetzwerk zu senden, können Sie die Datei später noch veröffentlichen. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor; Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs aufgenommen werden sollen, für alle Keywords, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung: <i>[!UICONTROL Yes]</i> (Standard) oder <i>[!UICONTROL No]</i>. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie <i>[!UICONTROL Yes]</i> auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs vorhanden sind, werden sie standardmäßig nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert wurden).<br><br>Wenn Sie <i>[!UICONTROL No]</i> auswählen, können Sie später trotzdem Tracking-URLs generieren, indem Sie die hochgeladene Datei manuell posten.<br><br><b>Hinweis:</b> Wenn der Advertiser das Adobe Advertising-Konversionstracking verwendet und die Basis-URL geändert wurde, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass Tracking-URLs automatisch generiert und hochgeladen werden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen für Kampagnen in optimierten Portfolios auf der Grundlage von veröffentlichten Daten. Standardmäßig ist diese Option nicht ausgewählt. Wenn Sie diese Option auswählen, werden alle angegebenen Änderungen am Kampagnenbudget wirksam, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (in der Regel beim nächsten Angebotszyklus).<br><br><b>Hinweis</b> Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden am nächsten Tag in den Ansichten der Kampagnenverwaltung angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht bis zu einem bestimmten Enddatum Angebotsänderungen basierend auf den Daten in der Bulksheet. Wenn Sie diese Option wählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Bulksheet-Datei herunterladen/erstellen](bulksheet-download.md)
>* [Buchen Sie Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
