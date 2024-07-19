---
title: Feed-Einstellungen für Tabellenberichte
description: Erfahren Sie mehr über die Einstellungen für Tabellen-Feeds.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Feed-Einstellungen für Tabellenberichte

| Feld | Beschreibung |
|---|---|
| [!UICONTROL Feed Name] | Ein Name für den Tabellenfeed. |
| [!UICONTROL Report Template] | Die Berichtsvorlage, die die erforderlichen Berichtsdaten angibt. Wählen Sie die Berichtsvorlage aus, die Sie zum Erstellen der [!DNL Excel] -Vorlage verwendet haben. Alle grundlegenden Berichtvorlagen werden aufgelistet.<br><br><b>Hinweis:</b> Wenn Sie die für den Bericht verwendete Berichtsvorlage ändern oder die Spalten in der Vorlage aktualisieren, müssen Sie eine neue [!DNL Excel] -Vorlage erstellen und hochladen. |
| [!UICONTROL Excel Template] | Die speziell formatierte [!DNL Excel] -Vorlage, die Sie im .XLSX-Format erstellt haben und die auf die in der Berichtsvorlage angegebenen Daten angewendet wird. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf <b>[!UICONTROL Browse]</b> klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. |
| [!UICONTROL Back Fill From] | Das Anfangsdatum, für das die auf der Registerkarte [!UICONTROL RAW] vorhandenen Daten aktualisiert werden, was durch eine Anzahl von Tagen in der Vergangenheit dargestellt wird. Geben Sie einen Wert von bis zu 90 Tagen ein. Der Standardwert ist sieben (7) Tage.<br><br>Wenn der Wert beispielsweise 7 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW], die mit dem 1. März beginnt, aktualisiert (bis zum Enddatum, das durch den Parameter [!UICONTROL Back Fill Until] angegeben wird). Vorhandene Datenzeilen für Datumsangaben vor dem 1. März werden nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Back Fill Until] | Das Enddatum, für das vorhandene Daten auf der Registerkarte [!UICONTROL RAW] aktualisiert werden, was durch eine Anzahl von Tagen in der Vergangenheit dargestellt wird. Der Standardwert ist ein (1) Tag.<br><br>Wenn dieser Wert beispielsweise 1 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] bis zum 6. März aktualisiert (und beginnen mit dem Startdatum, das durch den Parameter [!UICONTROL Back Fill From] angegeben wird). Wenn dieser Wert 1 beträgt, ist der Parameter [!UICONTROL Back Fill Until] 7 und heute der 7. März, werden die auf der Registerkarte [!UICONTROL RAW] vorhandenen Daten vom 1. März bis 6. März aktualisiert. In beiden Beispielen werden vorhandene Datenzeilen für Datumsangaben nach dem 6. März nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Email Recipients] | E-Mail-Adressen, an die Benachrichtigungen bei jeder Aktualisierung des Berichts oder bei jeder Ausführung des Berichts gesendet werden sollen, wenn die Vorlage einen Zeitplan enthält. Standardmäßig wird die Adresse für Ihr Benutzerkonto angegeben. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas, Leerzeichen oder neue Zeilen. |
| [!UICONTROL Schedule Time] | Der Zeitpunkt, zu dem Tabellen-Feeds aktualisiert werden: entweder um 08:00 Uhr oder zu einer beliebigen Stunde zwischen 10:00 und 23:00 Uhr in der Zeitzone des Werbetreibenden. Die Standardeinstellung für neue Tabellen-Feeds ist 10:00 Uhr.<br><br><b>Hinweis:</b> Aus Leistungsgründen können Sie die Tabellenfeeds nicht um 9:00 Uhr aktualisieren, wenn andere Berichte generiert werden. |
| [!UICONTROL Email Notification] | (Wenn E-Mail-Empfänger angegeben sind) Was soll in E-Mail-Benachrichtigungen an bestimmte Adressen eingefügt werden?<ul><li><i>Feed anhängen</i> — Zum Senden einer Kopie des abgeschlossenen Berichts im XLSX-Format. Wenn die Datei größer als 10 MB ist, enthält die Benachrichtigung keinen Anhang.</li><li><i>Nur Benachrichtigung</i> (Standard) - Um nur eine Benachrichtigung über den Abschluss oder Fehler eines Berichts mit einem Link zum Bericht zu senden,</li></ul> |

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Erstellen einer [!DNL Excel] Vorlage für einen Tabellenbericht-Feed](spreadsheet-feed-create-excel-template.md)
>* [Bearbeiten Sie die Einstellungen des Tabellenbericht-Feeds](spreadsheet-feed-edit.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Manuelles Aktualisieren von Tabellenbericht-Feeds](spreadsheet-feed-refresh.md)
>* [Löschen von Tabellenbericht-Feeds](spreadsheet-feed-delete.md)
