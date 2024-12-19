---
title: Einstellungen für Tabellenbericht-Feeds
description: Erfahren Sie mehr über die Einstellungen für Tabellen-Feeds.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Einstellungen für Tabellenbericht-Feeds

| Feld | Beschreibung |
|---|---|
| [!UICONTROL Feed Name] | Ein Name für den Tabellen-Feed. |
| [!UICONTROL Report Template] | Die Berichtsvorlage, die die erforderlichen Berichtsdaten angibt. Wählen Sie die Berichtsvorlage aus, die Sie zum Erstellen der [!DNL Excel] verwendet haben. Alle grundlegenden Berichtsvorlagen werden aufgelistet.<br><br><b>Hinweis:</b> Wenn Sie die für den Bericht verwendete Berichtsvorlage ändern oder die Spalten in der Vorlage aktualisieren, müssen Sie eine neue [!DNL Excel] erstellen und hochladen. |
| [!UICONTROL Excel Template] | Die speziell formatierte [!DNL Excel], die Sie im .XLSX-Format erstellt haben und die auf die in der Berichtsvorlage angegebenen Daten angewendet wird. Geben Sie die hochzuladende Datei an, indem Sie entweder den vollständigen Pfad und Dateinamen eingeben oder auf <b>[!UICONTROL Browse]</b> klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. |
| [!UICONTROL Back Fill From] | Das Anfangsdatum, für das die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] aktualisiert werden, angegeben durch eine Anzahl von Tagen in der Vergangenheit. Geben Sie einen Wert von bis zu 90 Tagen ein. Der Standardwert ist sieben (7) Tage.<br><br>Wenn der Wert beispielsweise 7 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] ab dem 1. März aktualisiert (bis zu dem im Parameter [!UICONTROL Back Fill Until] angegebenen Enddatum). Vorhandene Datenzeilen für Daten vor dem 1. März werden nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Back Fill Until] | Das Enddatum, für das die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] aktualisiert werden, was in der Vergangenheit durch eine Anzahl von Tagen dargestellt wurde. Der Standardwert ist ein (1) Tag.<br><br>Wenn dieser Wert beispielsweise 1 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] bis zum 6. März aktualisiert (und beginnen mit dem im Parameter [!UICONTROL Back Fill From] angegebenen Startdatum). Wenn dieser Wert 1 ist, der [!UICONTROL Back Fill Until] 7 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] vom 1. März bis zum 6. März aktualisiert. In beiden Beispielen werden vorhandene Datenzeilen für Daten nach dem 6. März nicht gelöscht, aber sie werden nicht aktualisiert. |
| [!UICONTROL Email Recipients] | E-Mail-Adressen, an die Benachrichtigungen bei jeder Aktualisierung des Berichts gesendet werden sollen, oder bei jeder Ausführung des Berichts, wenn die Vorlage einen Zeitplan enthält. Standardmäßig wird die Adresse für Ihr Benutzerkonto eingegeben. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas, Leerzeichen oder neue Zeilen. |
| [!UICONTROL Schedule Time] | Der Zeitpunkt, zu dem die Tabellen-Feeds aktualisiert werden: entweder um 08:00 Uhr oder zu einer beliebigen Stunde zwischen 10:00 und 23:00 Uhr in der Zeitzone des Werbetreibenden. Der Standardwert für neue Tabellen-Feeds ist 10:00.<br><br><b>Hinweis:</b> Aus Leistungsgründen können Tabellen-Feeds nicht um 09:00 Uhr aktualisiert werden, wenn andere Berichte generiert werden. |
| [!UICONTROL Email Notification] | (Wenn E-Mail-Empfänger angegeben sind) Was in E-Mail-Benachrichtigungen an bestimmte Adressen enthalten sein soll:<ul><li><i>Feed anhängen</i> — Versand einer Kopie des ausgefüllten Berichts im XLSX-Format. Wenn die Datei größer als 10 MB ist, enthält die Benachrichtigung keine Anlage.</li><li><i>Nur Benachrichtigung</i> (Standard) - Zum Senden nur einer Benachrichtigung über das Abschließen oder Fehlschlagen eines Berichts mit einem Link zum Bericht.</li></ul> |

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Erstellen einer  [!DNL Excel]  für einen Tabellenbericht-Feed](spreadsheet-feed-create-excel-template.md)
>* [Bearbeiten von Tabellenbericht-Feed-Einstellungen](spreadsheet-feed-edit.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Tabellenbericht-Feeds manuell aktualisieren](spreadsheet-feed-refresh.md)
>* [Tabellenbericht-Feeds löschen](spreadsheet-feed-delete.md)
