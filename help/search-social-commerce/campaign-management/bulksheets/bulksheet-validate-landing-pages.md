---
title: Validieren von Landingpages in Bulksheet-Dateien
description: Erfahren Sie, wie Sie die Ziel-URLs in einer Bulksheet-Datei mit einem Konto validieren.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validieren von Landingpages in Bulksheet-Dateien

*Nur Konten mit Ziel-URLs*

Sie können die Landingpages in allen Ziel-URLs in einer Bulksheet-Datei mit einem Konto validieren. Sie können alle Phrasen und URLs angeben, die auf eine ungültige Seite hinweisen, und optional Umleitungen auf Landingpages als Fehler melden. Search, Social und Commerce überprüfen Ihre angegebenen Bedingungen und fehlende Landingpages (was zu HTTP 404- oder „Not Found“-Fehlern führt).

Wenn Fehler gefunden werden, erstellt Search, Social und Commerce eine Bulksheet-Fehlerdatei, die alle Zeilen in der ursprünglichen Bulksheet-Datei und Fehlermeldungen für alle Zeilen mit ungültiger Landingpage enthält. Die Fehler sind in der Spalte [!UICONTROL EF Errors] aufgeführt. Die Dateinamenkonvention ist `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Sie können die Datei später herunterladen, die Fehler korrigieren und die korrigierte Datei hochladen und die korrigierte Datei dann in das Anzeigennetzwerkkonto posten.

>[!NOTE]
>
>* Diese Funktion validiert keine Werte in der Spalte Basis-URL/Endgültige URL.
>* Sie können Bulksheet-Dateien posten, während sie validiert werden oder auch wenn Fehler gefunden werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu validierenden Datei.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Validate URLs]**.

1. Geben Sie im Dialogfeld Informationen in die Felder ein, und klicken Sie dann auf **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Text im Text einer Landingpage, der anzeigt, dass die Seite ungültig ist. Um mehrere Werte anzugeben, geben Sie sie in separaten Zeilen ein.

   **[!UICONTROL Enter invalid landing pages(one per line):]** Die URLs von Seiten, die als Landingpages ungültig sind. Um mehrere Werte anzugeben, geben Sie sie in separaten Zeilen ein.

   **[!UICONTROL User Agent:]**, wie der Landingpage-Validierungs-Agent für den Webserver identifiziert wird, auf dem sich die Landingpage befindet. Der Standardwert ist „default“ und schreibt vom Agenten Ansichten einem anonymen [!DNL Mozilla Firefox] Benutzer zu. Wenn der Webserver Anfragen anonymer [!DNL Mozilla Firefox] blockiert, geben Sie den Namen eines anderen Agenten ein. Geben Sie beispielsweise [!DNL Googlebot] `Googlebot/2.1;+http://www.google.com/bot.html` ein.

   **[!UICONTROL Report redirects as errors]:** Wenn eine Landingpage zu einer anderen Seite umgeleitet wird (z. B. wenn die Landingpage fehlt und die Site eine Ersatzseite anzeigt), gibt die [!UICONTROL ER Errors] Spalte in der Fehlerdatei der Landingpage die URL an, zu der die Landingpage umgeleitet wird.

Wenn die Aufgabe beginnt, wird eine neue Zeile zur [!UICONTROL Bulksheets view] hinzugefügt. Wenn die Datei erstellt wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Sie können die Datei herunterladen, um sie zu bearbeiten, und sie dann erneut zur Veröffentlichung hochladen oder Sie können die Datei unverändert veröffentlichen. Wenn die Dateigenerierung jedoch fehlschlägt, wird auf der Seite [!UICONTROL Bulksheet Management] eine Fehlerdatei aufgeführt und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Die Validierung großer Dateien dauert länger.
>* Bulksheet-Dateien für mehrere Kampagnen können bis zu 500.000 Datenzeilen enthalten. Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` usw. aufgeteilt.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Hochgeladene Bulksheets und Fehlerdateien löschen](bulksheet-delete.md)
>* [Buchen Sie Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Anhalten eines laufenden Bulksheet-Vorgangs](bulksheet-stop-job.md)
>* [Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](bulksheet-upload.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
