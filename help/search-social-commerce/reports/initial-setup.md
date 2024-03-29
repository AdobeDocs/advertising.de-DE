---
title: Die anfänglichen Einrichtungsaufgaben für Berichte
description: Erfahren Sie, wie Sie Metriken in Berichten verfügbar machen und wie Sie Berichte automatisieren können.
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Die anfänglichen Einrichtungsaufgaben für Berichte

Neue Benutzer sollten die folgenden grundlegenden Einrichtungsaufgaben ausführen:

* Konversionsmetriken festlegen, die der Adobe Advertising für einen Advertiser verfolgt [für Berichte und andere Ansichten verfügbar](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)und optional [Konversionsmetriken umbenennen](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md), die zur Lesbarkeit in Spaltenüberschriften angezeigt werden.

  Transaktionseigenschaften stehen nur dann für Berichte zur Verfügung, wenn Sie sie speziell zur Verfügung stellen.

  Wenn Sie später mit der Verfolgung einer neuen Konversionsmetrik beginnen, müssen Sie diese Aufgabe wiederholen.

* (Optional) Automatisieren der Berichterstellung:

   * Wenn Sie regelmäßig Berichtsdaten für eine bestimmte Zeitinkrementierung generieren möchten, z. B. eine [!UICONTROL Campaign Report] für die letzte Woche oder die letzten 30 Tage, können Sie [Berichtsvorlagen](/help/search-social-commerce/reports/automation/templates/template-about.md) und planen die tägliche Ausführung oder einen bestimmten Tag der Woche oder des Monats. Jedes Mal, wenn die Ausführung des Berichts geplant ist, wird ein neuer Bericht generiert. Sie haben die Möglichkeit, die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce zu benachrichtigen, wenn der Bericht abgeschlossen ist, basierend auf der Variablen [In konfigurierte Benachrichtigungseinstellungen [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Wenn Sie aktuelle, tägliche Berichtsdaten in einer benutzerdefinierten Tabelle anzeigen möchten, mit oder ohne Pivot-Tabellen und zusätzliche Spalten, die Sie für weitere Berechnungen benötigen, können Sie einen täglichen [Tabellenfeed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Arbeitsblatt-Feeds werden täglich mit den neuesten Leistungsdaten aktualisiert und behalten weiterhin Daten aus den vorherigen Daten bei. Um Tabellen-Feeds zu konfigurieren, müssen Sie zunächst eine benutzerdefinierte Tabellenvorlage in [!DNL Microsoft Excel]. Sie haben die Möglichkeit, die E-Mail-Adressen bestimmter Benutzer von Search, Social und Commerce zu benachrichtigen, wenn eine Feed-Datei verfügbar ist, basierend auf dem [In konfigurierte Benachrichtigungseinstellungen [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Wenn Sie grundlegende und erweiterte Berichte an einem FTP-Speicherort erhalten möchten, können Sie [FTP-Zugriff auf grundlegende und erweiterte Berichte](/help/search-social-commerce/reports/automation/ftp-reports.md) , indem Sie ein FTP-Konto anfordern und Berichtsvorlagen mithilfe einer bestimmten Benennungskonvention einrichten.

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Für Berichte verwendete Daten](data-used-for-reports.md)
