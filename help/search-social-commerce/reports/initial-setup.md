---
title: Die anfänglichen Einrichtungsaufgaben für Berichte
description: Erfahren Sie, wie Sie Metriken in Berichten verfügbar machen und wie Sie Berichte automatisieren können.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Die anfänglichen Einrichtungsaufgaben für Berichte

Neue Benutzer sollten die folgenden grundlegenden Einrichtungsaufgaben ausführen:

* Stellen Sie die Konversionsmetriken, die von Adobe Advertising für einen Advertiser verfolgt werden, [für Berichte und andere Ansichten zur Verfügung](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) und benennen Sie optional [ eine der Konversionsmetriken um](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md, die in Spaltenüberschriften angezeigt werden, um lesbar zu sein.

  Transaktionseigenschaften stehen nur dann für Berichte zur Verfügung, wenn Sie sie speziell zur Verfügung stellen.

  Wenn Sie später mit der Verfolgung einer neuen Konversionsmetrik beginnen, müssen Sie diese Aufgabe wiederholen.

* (Optional) Automatisieren der Berichterstellung:

   * Wenn Sie regelmäßig Berichtsdaten für ein bestimmtes Zeitintervall generieren möchten, z. B. 0 für die letzte Woche oder die letzten 30 Tage, können Sie [Berichtsvorlagen](/help/search-social-commerce/reports/automation/templates/template-about.md) einrichten und planen, dass diese täglich oder an einem bestimmten Wochentag oder Monat ausgeführt werden. [!UICONTROL Campaign Report] Jedes Mal, wenn die Ausführung des Berichts geplant ist, wird ein neuer Bericht generiert. Sie können die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce nach Abschluss des Berichts entsprechend den in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md) konfigurierten [Benachrichtigungseinstellungen benachrichtigen.

   * Wenn Sie aktuelle, tägliche Berichtsdaten in einer benutzerdefinierten Tabelle anzeigen möchten, mit oder ohne Pivot-Tabellen und zusätzliche Spalten, die Sie für weitere Berechnungen benötigen, können Sie einen täglichen [Tabellenfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) einrichten. Arbeitsblatt-Feeds werden täglich mit den neuesten Leistungsdaten aktualisiert und behalten weiterhin Daten aus den vorherigen Daten bei. Um Tabellen-Feeds zu konfigurieren, müssen Sie zunächst eine benutzerdefinierte Tabellenvorlage in [!DNL Microsoft Excel] erstellen. Sie haben die Möglichkeit, die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce zu benachrichtigen, wenn eine Feed-Datei verfügbar ist, basierend auf den in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md) konfigurierten [Benachrichtigungseinstellungen.

   * Wenn Sie grundlegende und erweiterte Berichte an einem FTP-Speicherort erhalten möchten, können Sie den [FTP-Zugriff auf einfache und erweiterte Berichte](/help/search-social-commerce/reports/automation/ftp-reports.md) einrichten, indem Sie ein FTP-Konto anfordern und Berichtsvorlagen mithilfe einer bestimmten Benennungskonvention einrichten.

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Für Berichte verwendete Daten](data-used-for-reports.md)
