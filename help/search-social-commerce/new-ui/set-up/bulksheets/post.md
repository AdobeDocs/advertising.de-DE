---
title: (Neue Benutzeroberfläche) Posten von Bulksheets oder korrigierten Fehlerdateien
description: Erfahren Sie, wie Sie in der neuen Benutzeroberfläche von Search, Social und Commerce Bulksheet-Dateien in Ihren Werbenetzwerken posten.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 739034010787c2016720bef37fb75dc8efbae58b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Posten von Bulksheets oder korrigierten Fehlerdateien

Sie können vorhandene Bulksheet-Dateien oder korrigierte Fehlerdateien in den entsprechenden Konten für [unterstützte Werbenetzwerke](about.md#bulksheet-functionality-by-network) posten. Wenn die Datei im ZIP-Format vorliegt, müssen Sie sie nicht zuerst entpacken.

Bulksheet-Dateien und Fehlerdateien werden 30 Tage nach dem Hochladen oder Generieren automatisch gelöscht.

>[!NOTE]
>
>Sie können auch eine Bulksheet-Datei oder Fehlerdatei posten, wenn Sie die Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Datei, die gepostet werden soll.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Post]**.

1. Geben Sie Informationen in die [[!UICONTROL Post Bulksheet] ein, wählen Sie diese aus ](#bulksheet-post-settings) klicken Sie dann auf **[!UICONTROL Post]**.

   Die gleichen Einstellungen gelten für alle Dateien, die Sie posten.

Wenn die Aufgabe beginnt, werden der Status und das geplante Veröffentlichungsdatum für die Zeile in der [!UICONTROL Bulksheets] aktualisiert. Wenn E-Mail-Benachrichtigungen für Bulksheets [in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md) aktiviert sind, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet, sobald die Datei veröffentlicht wird. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn keine der Daten veröffentlicht werden können, wird eine Fehlerdatei in der [!UICONTROL Bulksheets] angezeigt und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Die Veröffentlichung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei in der [!UICONTROL Progress] in der [!UICONTROL Bulksheets] verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
>* Bevor die Bulksheet-Datei veröffentlicht wird, können Sie die Veröffentlichung abbrechen.

## Einstellungen für Bulksheets und korrigierte Fehlerdateien posten {#bulksheet-post-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL Account (Search Engine)] | Das Netzwerkkonto der Anzeige, für das die Daten veröffentlicht werden. Wenn Sie mehrere Dateien gleichzeitig posten oder eine Datei, die für mehrere Konten gilt, lautet der Wert *Mehrere Konten ausgewählt*.<br><br>Der erste Buchstabe des Anzeigennetzwerknamens ist in Klammern nach dem Kontonamen (z. B. „Acme Realty (G)“ für ein [!DNL Google Ads]-Konto). |
| [!UICONTROL Scheduling] | Wann die Datei an das angegebene Anzeigennetzwerk gesendet werden soll:<ul><li>*[!UICONTROL Post to ad network now]* (Standard): Beginnt sofort mit der Veröffentlichung der Daten.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Beginnt mit dem Posten der Daten zum angegebenen Datum und zur angegebenen Uhrzeit; der Standardwert ist morgen um :00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum im Format TT/MM/JJJJ ein oder klicken Sie auf das Kalendersymbol, um den Kalender zu öffnen und ein Datum auszuwählen. Um die Zeit zu ändern, wählen Sie eine Zeit (in 15-Minuten-Intervallen) aus der Liste aus.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs aufgenommen werden sollen, für alle Keywords, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung: *[!UICONTROL Yes]* (Standard) oder *[!UICONTROL No]*. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie *[!UICONTROL Yes]* auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs vorhanden sind, werden sie standardmäßig erst dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Schlüsselworttyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert haben).<br><br>Wenn Sie &quot;*[!UICONTROL No]*&quot; auswählen, können Sie Tracking-URLs auch später noch generieren, indem Sie die hochgeladene Datei manuell posten.<br><br>**Hinweis:** Wenn der Werbetreibende Adobe Advertising-Konversionstracking verwendet und sich die Basis-URL geändert hat, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass Tracking-URLs automatisch generiert und hochgeladen werden. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Verfügbar, wenn [!UICONTROL Generate Tracking URLs] *[!UICONTROL Yes]* ist) Ersetzt jedes vorhandene Adobe Advertising-Tracking in den URLs der hochgeladenen Datei durch das neu generierte Tracking. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen für Kampagnen in optimierten Portfolios auf der Grundlage von veröffentlichten Daten. Standardmäßig ist diese Option nicht ausgewählt. Wenn Sie diese Option auswählen, gelten alle angegebenen Änderungen am Kampagnenbudget, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (normalerweise beim nächsten Gebotszyklus). <br><br>**Hinweis:** Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden am nächsten Tag in den Ansichten der Kampagnenverwaltung angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht bis zu einem bestimmten Enddatum Angebotsänderungen basierend auf den Daten in der Bulksheet. Wenn Sie diese Option wählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [ (Neue Benutzeroberfläche) Verwalten von Kampagnendaten mithilfe von Bulksheets](about.md)
>* [(Neue Benutzeroberfläche) Herunterladen/Erstellen einer Bulksheet-Datei](download.md)
>* [(Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](upload.md)
>* [(Neue Benutzeroberfläche) Validieren von Landingpages in Bulksheet-Dateien](validate-landing-pages.md)
>* [(Neue Benutzeroberfläche) Löschen hochgeladener Bulksheets und Fehlerdateien](delete.md)
