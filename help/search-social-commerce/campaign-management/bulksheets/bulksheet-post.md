---
title: Post-Bulksheets oder korrigierte Fehlerdateien
description: Erfahren Sie, wie Sie Bulksheet-Dateien in Ihren Werbenetzwerken posten können.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Post-Bulksheets oder korrigierte Fehlerdateien

Sie können vorhandene Bulksheet-Dateien oder korrigierte Fehlerdateien in den entsprechenden Konten für [unterstützte Anzeigennetzwerke](bulksheet-about.md#bulksheet-functionality-by-network) posten. Wenn die Datei im ZIP-Format vorliegt, müssen Sie sie nicht zuerst dekomprimieren.

Bulksheet- und Fehlerdateien werden 30 Tage nach dem Hochladen oder Generieren automatisch gelöscht.

>[!NOTE]
>Sie können beim Hochladen der Datei auch eine Bulksheet- oder Fehlerdatei posten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben den einzelnen zu sendenden Dateien.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Post]**.

1. Geben Sie im Dialogfeld Informationen in die Einstellungen [[!UICONTROL Post Bulksheet]](#bulksheet-post-settings) ein oder wählen Sie sie aus und klicken Sie dann auf **[!UICONTROL Post]**.

   Die gleichen Einstellungen gelten für alle Dateien, die Sie posten.

Wenn die Aufgabe beginnt, werden der Status und das geplante Beitragsdatum für die Zeile in der Ansicht [!UICONTROL Bulksheets] geändert. Wenn die Datei gepostet wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Wenn jedoch keine Daten gepostet werden können, wird in der Ansicht &quot;[!UICONTROL Bulksheets]&quot;eine Fehlerdatei aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Die Veröffentlichung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei in der Spalte [!UICONTROL Progress] in der Ansicht [!UICONTROL Bulksheets] verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
* Bevor die Bulksheet-Datei veröffentlicht wird, können Sie den Beitrag abbrechen.

## Beitragseinstellungen für Bulksheets und korrigierte Fehlerdateien {#bulksheet-post-settings}

| Parameter | Beschreibung |
|----|----|
| [!UICONTROL Account (Search Engine)] | Das Anzeigennetzwerkkonto, für das die Daten veröffentlicht werden. Wenn Sie mehrere Dateien gleichzeitig oder eine Datei veröffentlichen, die für mehrere Konten gilt, lautet der Wert <i>Mehrere ausgewählte Konten</i>.<br><br>Der erste Buchstabe des Anzeigennetzwerknamens ist in Klammern hinter dem Kontonamen (z. B. &quot;Acme Realty (G)&quot;für ein [!DNL Google Ads] -Konto). |
| [!UICONTROL Scheduling] | Wann wird die Datei im angegebenen Anzeigennetzwerk veröffentlicht?<ul><li><i>[!UICONTROL Post to ad network now]</i> (Standard): Beginnt mit dem sofortigen Veröffentlichen der Daten.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Beginnt mit der Veröffentlichung der Daten am angegebenen Datum und zur angegebenen Uhrzeit; der Standardwert ist morgen um 02:00 Uhr (2 Uhr). Um das Datum zu ändern, geben Sie ein Datum in das Format TT/MM/JJJJ oder D/M/JJJJ ein oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") , um den Kalender zu öffnen, und [wählen Sie ein Datum aus](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um die Zeit zu ändern, geben Sie die Zeit im Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in Intervallen von 15 Minuten) aus der Liste aus.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Ob Tracking-Vorlagen und Landingpage-Suffixe (für zutreffende Anzeigennetzwerke) in Konten mit Tracking-Vorlagen oder Ziel-URLs mit eingebetteten Trackingcodes in Konten mit Ziel-URLs für alle Suchbegriffe, Anzeigen, Platzierungen, Sitelinks und [!DNL Google Ads] Produktgruppen in der Veröffentlichung eingeschlossen werden sollen: <i>[!UICONTROL Yes]</i> (Standard) oder <i>[!UICONTROL No]</i>. Es spielt keine Rolle, ob sich die Gebotseinheiten in einem Portfolio befinden.<br><br>Wenn Sie <i>[!UICONTROL Yes]</i> auswählen, werden die URLs gemäß den Parametern im Abschnitt [!UICONTROL Tracking Methods] der entsprechenden Kontoeinstellungen oder Kampagneneinstellungen generiert. Standardmäßig werden Tracking-URLs nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der Anzeigentext oder die Tracking-Parameter für die entsprechenden Konten geändert haben).<br><br>Wenn Sie <i>[!UICONTROL No]</i> auswählen, können Sie die Tracking-URLs später dennoch generieren, indem Sie die hochgeladene Datei manuell veröffentlichen.<br><br><b>Hinweis:</b> Wenn der Advertiser das Adobe Advertising-Konversions-Tracking verwendet und die Basis-URL geändert wurde, müssen Sie neue Tracking-URLs generieren, es sei denn, das Konto ist so konfiguriert, dass automatisch Tracking-URLs generiert und hochgeladen werden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Ermöglicht Budgetänderungen an Kampagnen in optimierten Portfolios basierend auf veröffentlichten Daten. Standardmäßig ist diese Option nicht aktiviert. Wenn Sie diese Option auswählen, gelten alle angegebenen Änderungen des Kampagnenbudgets, bis die Optimierungsfunktion bestimmt, dass das Budget neu zugewiesen werden soll (in der Regel beim nächsten Angebotszyklus).<br><br><b>Hinweis:</b> Alle Budgetänderungen, die sich aus den veröffentlichten Daten für Kampagnen in nicht optimierten Portfolios ergeben, treten beim Veröffentlichen der Datei auf. Änderungen werden in den Kampagnenverwaltungsansichten am nächsten Tag angezeigt. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wenn sich die enthaltenen Kampagnenkomponenten in einem optimierten Portfolio befinden, überschreibt diese Funktion die Optimierungsstrategie und ermöglicht Angebotsänderungen, die auf den Daten im Bulksheet bis zu einem bestimmten Enddatum basieren. Wenn Sie diese Option auswählen, geben Sie im Feld **[!UICONTROL Hold bulksheet bids until]** ein Enddatum zwischen 1 und 7 Tagen an. |

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](bulksheet-download.md)
>* [Bulksheets oder korrigierte Fehlerdateien hochladen](bulksheet-upload.md)
>* [Validieren von Landingpages in Bulksheet-Dateien](bulksheet-validate-landing-pages.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
