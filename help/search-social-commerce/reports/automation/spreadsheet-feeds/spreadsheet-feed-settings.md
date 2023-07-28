---
title: Feed-Einstellungen für Tabellenberichte
description: Erfahren Sie mehr über die Einstellungen für Tabellen-Feeds.
exl-id: 9a7e0a21-5db4-4829-a191-cacaa51f6cb6
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Feed-Einstellungen für Tabellenberichte

| Feld | Beschreibung |
|---|---|
| [!UICONTROL Feed Name] | Ein Name für den Tabellenfeed. |
| [!UICONTROL Report Template] | Die Berichtsvorlage, die die erforderlichen Berichtsdaten angibt; wählen Sie die Berichtsvorlage aus, die Sie zum Erstellen der [!DNL Excel] Vorlage. Alle grundlegenden Berichtvorlagen werden aufgelistet.<br><br><b>Hinweis:</b> Wenn Sie die für den Bericht verwendete Berichtsvorlage ändern oder die Spalten in der Vorlage aktualisieren, müssen Sie eine neue erstellen und hochladen. [!DNL Excel] Vorlage. |
| [!UICONTROL Excel Template] | Die speziell formatierten [!DNL Excel] Vorlage, die Sie im .XLSX-Format erstellt haben und die auf die in der Berichtsvorlage angegebenen Daten angewendet wird. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf <b>[!UICONTROL Browse]</b> , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. |
| [!UICONTROL Back Fill From] | Das Anfangsdatum, für das die vorhandenen Daten auf der [!UICONTROL RAW] -Tab aktualisiert wurde, was in der Vergangenheit durch eine Reihe von Tagen dargestellt wurde. Geben Sie einen Wert von bis zu 90 Tagen ein. Der Standardwert ist sieben (7) Tage.<br><br>Wenn der Wert beispielsweise 7 beträgt und heute der 7. März ist, werden die vorhandenen Daten für die [!UICONTROL RAW] -Registerkarte, die mit dem 1. März beginnt, aktualisiert wird (bis zum Enddatum, das durch die Variable [!UICONTROL Back Fill Until] -Parameter). Vorhandene Datenzeilen für Datumsangaben vor dem 1. März werden nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Back Fill Until] | Das Enddatum, für das vorhandene Daten zum [!UICONTROL RAW] -Tab aktualisiert wurde, was in der Vergangenheit durch eine Reihe von Tagen dargestellt wurde. Der Standardwert ist ein (1) Tag.<br><br>Wenn dieser Wert beispielsweise 1 beträgt und heute der 7. März ist, werden die vorhandenen Daten für die [!UICONTROL RAW] -Tab bis zum 6. März aktualisiert (und beginnt mit dem Startdatum, das durch die Variable [!UICONTROL Back Fill From] -Parameter). Wenn dieser Wert 1 ist, wird der Wert [!UICONTROL Back Fill Until] den Parameter 7 hat und heute den 7. März ist, werden die vorhandenen Daten für die [!UICONTROL RAW] -Tab vom 1. März bis 6. März aktualisiert. In beiden Beispielen werden vorhandene Datenzeilen für Datumsangaben nach dem 6. März nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Email Recipients] | E-Mail-Adressen, an die Benachrichtigungen bei jeder Aktualisierung des Berichts oder bei jeder Ausführung des Berichts gesendet werden sollen, wenn die Vorlage einen Zeitplan enthält. Standardmäßig wird die Adresse für Ihr Benutzerkonto angegeben. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas, Leerzeichen oder neue Zeilen. |
| [!UICONTROL Schedule Time] | Der Zeitpunkt, zu dem Tabellen-Feeds aktualisiert werden: entweder um 08:00 Uhr oder zu einer beliebigen Stunde zwischen 10:00 und 23:00 Uhr in der Zeitzone des Werbetreibenden. Die Standardeinstellung für neue Tabellen-Feeds ist 10:00 Uhr.<br><br><b>Hinweis:</b> Aus Leistungsgründen ist es nicht möglich, Arbeitsblatt-Feeds um 9:00 Uhr zu aktualisieren, wenn andere Berichte generiert werden. |
| [!UICONTROL Email Notification] | (Wenn E-Mail-Empfänger angegeben sind) Was soll in E-Mail-Benachrichtigungen an bestimmte Adressen eingefügt werden?<ul><li><i>Feed anhängen</i> — Zum Senden einer Kopie des abgeschlossenen Berichts im XLSX-Format. Wenn die Datei größer als 10 MB ist, enthält die Benachrichtigung keinen Anhang.</li><li><i>Nur Benachrichtigung</i> (Standardeinstellung) - Um nur eine Benachrichtigung über den Abschluss oder das Fehlschlagen eines Berichts mit einem Link zum Bericht zu senden.</li></ul> |

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Erstellen Sie eine [!DNL Excel] Vorlage für einen Tabellenbericht-Feed](spreadsheet-feed-create-excel-template.md)
>* [Bearbeiten der Feed-Einstellungen für Tabellenberichte](spreadsheet-feed-edit.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Manuelles Aktualisieren von Tabellenbericht-Feeds](spreadsheet-feed-refresh.md)
>* [Löschen von Tabellenbericht-Feeds](spreadsheet-feed-delete.md)
