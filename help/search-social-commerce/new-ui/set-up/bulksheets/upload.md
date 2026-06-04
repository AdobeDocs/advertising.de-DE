---
title: (Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei
description: Erfahren Sie, wie Sie in der neuen Benutzeroberfläche für Suche, Social und Commerce manuell eine Bulksheet-Datei oder eine korrigierte Fehlerdatei für die Validierung der Landingpage hochladen.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei

Sie können Bulksheet-Dateien, korrigierte Fehlerdateien für die Landingpage-Validierung und andere korrigierte Fehlerdateien von Ihrem Gerät oder Netzwerk für (unterstützte [-Netzwerke) ](about.md#bulksheet-functionality-by-network). Alle benutzerdefinierten Spalten in der Datei werden beim Hochladen der Datei gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Geben Sie Informationen in die [[!UICONTROL Upload Bulksheet] ein oder wählen Sie diese aus](#bulksheet-upload-settings).

1. Klicken Sie auf **[!UICONTROL Upload]**.

Wenn die Aufgabe beginnt, wird die Datei in der [!UICONTROL Bulksheets] angezeigt. Wenn E-Mail-Benachrichtigungen für Bulksheets [in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md) aktiviert sind, wird nach Abschluss des Vorgangs eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateigenerierung fehlschlägt, wird eine Fehlerdatei in der [!UICONTROL Bulksheets]-Ansicht aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>Wenn Sie die Bulksheet-Daten an das Anzeigennetzwerk senden, können Sie den Fortschritt der Datei in der Spalte [!UICONTROL Progress] in der [!UICONTROL Bulksheets] verfolgen. Die Veröffentlichung großer Datenmengen dauert länger.

## Hochladen von Einstellungen für Bulksheets und korrigierte Fehlerdateien {#bulksheet-upload-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL File to Upload] | Die hochzuladende Datei. Geben Sie die Datei an, indem Sie entweder auf **[!UICONTROL Choose File]** klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.<br><br>Bulksheet-Dateien können bis zu 2,5 GB (etwa 2,5 Millionen Zeilen) groß sein und müssen eine der folgenden Dateierweiterungen aufweisen: *[!UICONTROL .tsv]* (für tabulatorgetrennte Werte), *[!UICONTROL .txt]* (für Unicode-kompatiblen ASCII-Text), *[!UICONTROL .csv]* (für kommagetrennte Werte) oder *[!UICONTROL .zip]* (für das komprimierte ZIP-Format, das in eine TSV-Datei dekomprimiert wird). Der Dateiname darf die folgenden Zeichen nicht enthalten: `# % & * \| \ : " < > . ? /`<br><br>**Tipp:** Verwenden Sie für Daten, die internationale Zeichen enthalten, Dateien im TSV- oder TXT-Format. |
| [!UICONTROL Single Account] | Ob die Datei für ein Konto gilt: *[!UICONTROL Yes]* (für ein Konto) oder *[!UICONTROL No]* (für mehrere Konten). |
| [!UICONTROL Account (Search Engine)] | (Wenn die Datei für ein einzelnes Konto gilt) Das Konto, in das die Daten hochgeladen werden sollen. |
| [!UICONTROL Search Engine] | (Wenn die Datei für mehrere Konten gilt) Das Anzeigennetzwerk, in das die Daten hochgeladen werden sollen.<br><br>**Hinweis:** Angebotsänderungen für Schlüsselwörter in optimierten Portfolios werden nicht mit Bulksheets mit mehreren Konten unterstützt. |
| [!UICONTROL Scheduling] | Wann oder ob die Datei an das angegebene Anzeigennetzwerk gesendet werden soll:<ul><li>*[!UICONTROL Post to search engine now]* (Standard): Beginnt sofort mit der Veröffentlichung der Daten.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Beginnt mit dem Posten der Daten zum angegebenen Datum und zur angegebenen Uhrzeit; der Standardwert ist morgen um :00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum im Format TT/MM/JJJJ ein oder klicken Sie auf das Kalendersymbol, um den Kalender zu öffnen und ein Datum auszuwählen. Um die Zeit zu ändern, wählen Sie eine Zeit (in 15-Minuten-Intervallen) aus der Liste aus.</li><li>*[!UICONTROL Preview only]:* Lädt die Datei in Search, Social und Commerce hoch, ohne die Daten an das Werbenetzwerk zu senden. Sie können die Datei später noch veröffentlichen. Wenn die Bulksheet-Datei größer als 10 MB, aber kleiner als 2 GB ist, liegt die Datei im ZIP-Format vor; Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs aufgenommen werden sollen, für alle Keywords, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung: *[!UICONTROL Yes]* (Standard) oder *[!UICONTROL No]*. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie *[!UICONTROL Yes]* auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs vorhanden sind, werden sie standardmäßig erst dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Schlüsselworttyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert haben).<br><br>Wenn Sie &quot;*[!UICONTROL No]*&quot; auswählen, können Sie Tracking-URLs auch später noch generieren, indem Sie die hochgeladene Datei manuell posten.<br><br>**Hinweis:** Wenn der Werbetreibende Adobe Advertising-Konversionstracking verwendet und sich die Basis-URL geändert hat, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass Tracking-URLs automatisch generiert und hochgeladen werden. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Verfügbar, wenn [!UICONTROL Generate Tracking URLs] *[!UICONTROL Yes]* ist) Ersetzt jedes vorhandene Adobe Advertising-Tracking in den URLs der hochgeladenen Datei durch das neu generierte Tracking. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen für Kampagnen in optimierten Portfolios auf der Grundlage von veröffentlichten Daten. Standardmäßig ist diese Option nicht ausgewählt. Wenn Sie diese Option auswählen, gelten alle angegebenen Änderungen am Kampagnenbudget, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (normalerweise beim nächsten Gebotszyklus). <br><br>**Hinweis:** Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden am nächsten Tag in den Ansichten der Kampagnenverwaltung angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht bis zu einem bestimmten Enddatum Angebotsänderungen basierend auf den Daten in der Bulksheet. Wenn Sie diese Option wählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [ (Neue Benutzeroberfläche) Verwalten von Kampagnendaten mithilfe von Bulksheets](about.md)
>* [(Neue Benutzeroberfläche) Herunterladen/Erstellen einer Bulksheet-Datei](download.md)
>* [ (neue Benutzeroberfläche) Posten von Bulksheets oder korrigierte Fehlerdateien](post.md)
>* [(Neue Benutzeroberfläche) Validieren von Landingpages in Bulksheet-Dateien](validate-landing-pages.md)
