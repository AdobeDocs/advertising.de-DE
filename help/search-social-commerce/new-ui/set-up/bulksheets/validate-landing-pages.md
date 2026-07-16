---
title: (Neue Benutzeroberfläche) Überprüfen von Landingpages in Bulksheet-Dateien
description: Erfahren Sie, wie Sie die Ziel-URLs in einer Bulksheet-Datei mit einem Konto in der neuen Benutzeroberfläche für Suche, Social und Commerce validieren.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Überprüfen von Landingpages in Bulksheet-Dateien

*Nur Konten mit Ziel-URLs*

Sie können die Landingpages in allen Ziel-URLs in einer Bulksheet-Datei mit einem Konto validieren. Sie können alle Phrasen und URLs angeben, die auf eine ungültige Seite hinweisen, und optional Umleitungen auf Landingpages als Fehler melden. Search, Social und Commerce überprüfen Ihre angegebenen Bedingungen und fehlende Landingpages (was zu HTTP 404- oder „Not Found“-Fehlern führt).

Wenn Fehler gefunden werden, erstellt Search, Social und Commerce eine Bulksheet-Fehlerdatei, die alle Zeilen in der ursprünglichen Bulksheet-Datei und Fehlermeldungen für alle Zeilen mit ungültigen Landingpages enthält. Die Fehler sind in der Spalte [!UICONTROL EF Errors] aufgeführt. Die Dateinamenkonvention ist `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Sie können die Datei später herunterladen, die Fehler korrigieren und die korrigierte Datei hochladen und die korrigierte Datei dann in das Anzeigennetzwerkkonto posten.

>[!NOTE]
>
>* Diese Funktion validiert keine Werte in der Spalte Basis-URL/Endgültige URL.
>* Sie können Bulksheet-Dateien posten, während sie validiert werden oder auch wenn Fehler gefunden werden.

>[!IMPORTANT]
>
>Die Unterstützung für Nicht-ASCII-Zeichen bei der Validierung von Landingpages wurde vorübergehend ausgesetzt. Wenn Ihre Landingpage-URLs Nicht-ASCII-Zeichen enthalten, wenden Sie sich an den technischen Support, um Hilfe zu erhalten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu validierenden Datei.

   >[!NOTE]
   >
   >Sie können nur EF-Bulksheets mit einem Konto validieren, die derzeit nicht in Bearbeitung sind. Wenn Sie ein Bulksheet mit mehreren Konten oder ein Bulksheet auswählen, das derzeit verarbeitet wird, werden diese Dateien ausgeschlossen.

1. Klicken Sie in der Aktionsleiste auf **[!UICONTROL Validate URLs]**.

1. Geben Sie im Dialogfeld Informationen in die Felder ein und klicken Sie dann auf **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Text im Text einer Landingpage, der anzeigt, dass die Seite ungültig ist. Um mehrere Werte anzugeben, geben Sie sie in separaten Zeilen ein.

   **[!UICONTROL Enter invalid landing pages (one per line):]** Die URLs von Seiten, die als Landingpages ungültig sind. Um mehrere Werte anzugeben, geben Sie sie in separaten Zeilen ein.

   **[!UICONTROL User Agent:]**, wie der Landingpage-Validierungs-Agent für den Webserver identifiziert wird, auf dem sich die Landingpage befindet. Der Standardwert ist `default`, d. h., Ansichten des Agenten werden einem anonymen [!DNL Mozilla Firefox] Benutzer zugeordnet. Wenn der Webserver Anfragen anonymer [!DNL Mozilla Firefox] blockiert, geben Sie den Namen eines anderen Agenten ein. Geben Sie beispielsweise [!DNL Googlebot] `Googlebot/2.1;+http://www.google.com/bot.html` ein.

   **[!UICONTROL Report redirects as errors]:** Wenn eine Landingpage zu einer anderen Seite umgeleitet wird (z. B. wenn die Landingpage fehlt und die Site eine Ersatzseite anzeigt), gibt die [!UICONTROL EF Errors] Spalte in der Fehlerdatei der Landingpage die URL an, zu der die Landingpage umgeleitet wird.

Wenn die Aufgabe beginnt, wird eine neue Zeile zur [!UICONTROL Bulksheets] hinzugefügt. Wenn E-Mail-Benachrichtigungen für Bulksheets [in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md) aktiviert sind, wird bei der Erstellung der Datei eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Sie können die Datei herunterladen, um sie zu bearbeiten, und sie dann erneut zur Veröffentlichung hochladen oder Sie können die Datei unverändert veröffentlichen.

>[!NOTE]
>
>* Die Validierung großer Dateien dauert länger.
>* Bulksheet-Dateien für mehrere Kampagnen können bis zu 500.000 Datenzeilen enthalten. Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` usw. aufgeteilt.

>[!MORELIKETHIS]
>
>* [&#x200B; (Neue Benutzeroberfläche) Verwalten von Kampagnendaten mithilfe von Bulksheets](about.md)
>* [(Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](upload.md)
>* [&#x200B; (neue Benutzeroberfläche) Posten von Bulksheets oder korrigierte Fehlerdateien](post.md)
>* [(Neue Benutzeroberfläche) Löschen hochgeladener Bulksheets und Fehlerdateien](delete.md)
>* [(Neue Benutzeroberfläche) Halten Sie einen laufenden Bulksheet-Vorgang an](stop-job.md)
