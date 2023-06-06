---
title: Die anfänglichen Einrichtungsaufgaben für Berichte
description: Erfahren Sie, wie Sie Metriken in Berichten verfügbar machen und wie Sie Berichte automatisieren können.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Die anfänglichen Einrichtungsaufgaben für Berichte

Neue Benutzer sollten die folgenden grundlegenden Einrichtungsaufgaben ausführen:

* Transaktionseigenschaften festlegen, die Adobe Advertising für einen Advertiser verfolgt [für Berichte und andere Ansichten verfügbar](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)und optional [einen der Eigenschaftsnamen umbenennen](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) die zur besseren Lesbarkeit in Spaltenüberschriften angezeigt werden.

   Transaktionseigenschaften stehen nur dann für Berichte zur Verfügung, wenn Sie sie speziell zur Verfügung stellen.

   Wenn Sie später mit der Verfolgung einer neuen Transaktionseigenschaft beginnen, müssen Sie diese Aufgabe wiederholen.

* (Optional) Automatisieren der Berichterstellung:

   * Wenn Sie regelmäßig Berichtsdaten für eine bestimmte Zeitinkrementierung generieren möchten, z. B. eine [!UICONTROL Campaign Report] für die letzte Woche oder die letzten 30 Tage, können Sie [Berichtsvorlagen](/help/search-social-commerce/reports/automation/templates/template-about.md) und planen, dass sie täglich oder an einem bestimmten Wochentag oder Monat ausgeführt werden. Jedes Mal, wenn die Ausführung des Berichts geplant ist, wird ein neuer Bericht generiert. Sie haben die Möglichkeit, die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce zu benachrichtigen, wenn der Bericht abgeschlossen ist, basierend auf der Variablen [In konfigurierte Benachrichtigungseinstellungen [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Wenn Sie aktuelle, tägliche Berichtsdaten in einer benutzerdefinierten Tabelle anzeigen möchten, mit oder ohne Pivot-Tabellen und zusätzliche Spalten, die Sie für weitere Berechnungen benötigen, können Sie einen täglichen [Tabellenfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Arbeitsblatt-Feeds werden täglich mit den neuesten Leistungsdaten aktualisiert und behalten weiterhin Daten aus den vorherigen Daten bei. Um Tabellen-Feeds zu konfigurieren, müssen Sie zunächst eine benutzerdefinierte Tabellenvorlage in [!DNL Microsoft Excel]. Sie haben die Möglichkeit, die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce zu benachrichtigen, wenn eine Feed-Datei verfügbar ist, basierend auf dem [In konfigurierte Benachrichtigungseinstellungen [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Wenn Sie grundlegende und erweiterte Berichte an einem FTP-Speicherort erhalten möchten, können Sie [FTP-Zugriff auf grundlegende und erweiterte Berichte](/help/search-social-commerce/reports/automation/ftp-reports.md) , indem Sie ein FTP-Konto anfordern und Berichtsvorlagen mithilfe einer bestimmten Benennungskonvention einrichten.

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Für Berichte verwendete Daten](data-used-for-reports.md)

