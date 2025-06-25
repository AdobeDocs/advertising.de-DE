---
title: Posten von Bulksheets oder korrigierten Fehlerdateien
description: Erfahren Sie, wie Sie Bulksheet-Dateien in Ihren Werbenetzwerken posten.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Posten von Bulksheets oder korrigierten Fehlerdateien

Sie können vorhandene Bulksheet-Dateien oder korrigierte Fehlerdateien in den entsprechenden Konten für [unterstützte Werbenetzwerke](bulksheet-about.md#bulksheet-functionality-by-network) posten. Wenn die Datei im ZIP-Format vorliegt, müssen Sie sie nicht zuerst entpacken.

Bulksheet-Dateien und Fehlerdateien werden 30 Tage nach dem Hochladen oder Generieren automatisch gelöscht.

>[!NOTE]
>Sie können auch eine Bulksheet-Datei oder Fehlerdatei posten, wenn Sie die Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Datei, die gepostet werden soll.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Post]**.

1. Geben Sie im Dialogfeld in den [[!UICONTROL Post Bulksheet] Einstellungen Informationen ein, oder wählen Sie diese aus](#bulksheet-post-settings) und klicken Sie dann auf **[!UICONTROL Post]**.

   Die gleichen Einstellungen gelten für alle Dateien, die Sie posten.

Wenn die Aufgabe beginnt, werden der Status und das geplante Veröffentlichungsdatum für die Zeile in der [!UICONTROL Bulksheets] geändert. Wenn die Datei veröffentlicht wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn jedoch keine der Daten veröffentlicht werden können, wird eine Fehlerdatei in der [!UICONTROL Bulksheets]-Ansicht aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Die Veröffentlichung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei in der [!UICONTROL Progress] in der [!UICONTROL Bulksheets] verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
>* Bevor die Bulksheet-Datei veröffentlicht wird, können Sie die Veröffentlichung abbrechen.

## Einstellungen für Bulksheets und korrigierte Fehlerdateien posten {#bulksheet-post-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL Account (Search Engine)] | Das Netzwerkkonto der Anzeige, für das die Daten veröffentlicht werden. Wenn Sie mehrere Dateien gleichzeitig posten oder eine Datei, die für mehrere Konten gilt, lautet der Wert <i>Mehrere Konten ausgewählt</i>.<br><br>Der erste Buchstabe des Anzeigennetzwerknamens befindet sich in Klammern hinter dem Kontonamen (z. B. „Acme Realty (G)“ für ein [!DNL Google Ads] Konto). |
| [!UICONTROL Scheduling] | Wann die Datei an das angegebene Anzeigennetzwerk gesendet werden soll:<ul><li><i>[!UICONTROL Post to ad network now]</i> (Standard): Beginnt sofort mit der Veröffentlichung der Daten.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Beginnt mit der Veröffentlichung der Daten zum angegebenen Datum und zur angegebenen Uhrzeit. Der Standardwert ist morgen um 02:00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum im Format TT/MM/JJJJ oder TT/M/JJJJ ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender"), um den Kalender zu öffnen und [Datum auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um die Zeit zu ändern, geben Sie die Zeit im Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in 15-Minuten-Intervallen) aus der Liste aus.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für entsprechende Werbenetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Tracking-Codes in Konten mit Ziel-URLs aufgenommen werden sollen, für alle Keywords, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung: <i>[!UICONTROL Yes]</i> (Standard) oder <i>[!UICONTROL No]</i>. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie <i>[!UICONTROL Yes]</i> auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Konto- oder Kampagneneinstellungen generiert. Wenn Tracking-URLs vorhanden sind, werden sie standardmäßig nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert wurden).<br><br>Wenn Sie <i>[!UICONTROL No]</i> auswählen, können Sie später trotzdem Tracking-URLs generieren, indem Sie die hochgeladene Datei manuell posten.<br><br><b>Hinweis:</b> Wenn der Advertiser das Adobe Advertising-Konversionstracking verwendet und die Basis-URL geändert wurde, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass Tracking-URLs automatisch generiert und hochgeladen werden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen für Kampagnen in optimierten Portfolios auf der Grundlage von veröffentlichten Daten. Standardmäßig ist diese Option nicht ausgewählt. Wenn Sie diese Option auswählen, werden alle angegebenen Änderungen am Kampagnenbudget wirksam, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (in der Regel beim nächsten Angebotszyklus).<br><br><b>Hinweis</b> Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden am nächsten Tag in den Ansichten der Kampagnenverwaltung angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht bis zu einem bestimmten Enddatum Angebotsänderungen basierend auf den Daten in der Bulksheet. Wenn Sie diese Option wählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Bulksheet-Datei herunterladen/erstellen](bulksheet-download.md)
>* [Hochladen von Bulksheets oder korrigierten Fehlerdateien](bulksheet-upload.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
