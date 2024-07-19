---
title: Validieren von Landingpages in Bulksheet-Dateien
description: Erfahren Sie, wie Sie die Ziel-URLs in einer Bulksheet-Datei mit nur einem Konto validieren.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validieren von Landingpages in Bulksheet-Dateien

*Nur Konten mit Ziel-URLs*

Sie können die Landingpages in allen Ziel-URLs in einer Bulksheet-Datei mit nur einem Konto validieren. Sie können Ausdrücke und URLs angeben, die auf eine ungültige Seite hinweisen, und optional Landingpage-Umleitungen als Fehler melden. Suchen, Social und Commerce sucht nach Ihren angegebenen Bedingungen und nach fehlenden Landingpages (was zu HTTP 404- oder &quot;Nicht gefunden&quot;-Fehlern führt).

Wenn Fehler gefunden werden, erstellt Search, Social und Commerce eine Bulksheet-Fehlerdatei, die alle Zeilen im ursprünglichen Bulksheet und Fehlermeldungen für alle Zeilen mit ungültiger Landingpage enthält. Die Fehler werden in der Spalte [!UICONTROL EF Errors] aufgeführt. Die Dateinamenkonvention lautet `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Sie können die Datei später herunterladen, die Fehler korrigieren und die korrigierte Datei hochladen und dann die korrigierte Datei in das Konto des Werbenetzwerks posten.

>[!NOTE]
>
>* Diese Funktion überprüft keine Werte in der Spalte Basis-URL/Endgültige URL .
>* Sie können Bulksheet-Dateien veröffentlichen, während sie validiert werden, oder auch, wenn Fehler gefunden werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Aktivieren Sie das Kontrollkästchen neben den zu validierenden Dateien.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Validate URLs]**.

1. Geben Sie im Dialogfeld Informationen in die Felder ein und klicken Sie auf **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Text im Hauptteil einer Landingpage, der angibt, dass die Seite ungültig ist. Um mehrere Werte anzugeben, geben Sie sie in separate Zeilen ein.

   **[!UICONTROL Enter invalid landing pages(one per line):]** Die URLs von Seiten, die als Landingpages ungültig sind. Um mehrere Werte anzugeben, geben Sie sie in separate Zeilen ein.

   **[!UICONTROL User Agent:]** Identifizieren des Validierungsagenten der Landingpage für den Webserver, auf dem sich die Landingpage befindet. Die Standardeinstellung ist, die Ansichten des Agenten einem anonymen [!DNL Mozilla Firefox] -Benutzer zuordnet. Wenn der Webserver Anforderungen von anonymen [!DNL Mozilla Firefox] -Benutzern blockiert, geben Sie den Namen eines anderen Agenten ein. Geben Sie beispielsweise für [!DNL Googlebot] den Wert `Googlebot/2.1;+http://www.google.com/bot.html` ein.

   **[!UICONTROL Report redirects as errors]:** Wenn eine Landingpage zu einer anderen Seite umleitet (z. B. wenn die Landingpage fehlt und die Site eine Ersatzseite anzeigt), gibt die Spalte [!UICONTROL ER Errors] in der Fehlerdatei der Landingpage die URL an, zu der die Landingpage umgeleitet wird.

Wenn die Aufgabe beginnt, wird dem [!UICONTROL Bulksheets view] eine neue Zeile hinzugefügt. Bei der Erstellung der Datei wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Je nach Menge der kompilierten Daten kann die E-Mail-Benachrichtigung mehrere Minuten oder länger dauern. Sie können die Datei herunterladen, um sie zu bearbeiten, und sie dann erneut zum Posten hochladen, oder Sie können die Datei unverändert posten. Wenn die Dateierstellung jedoch fehlschlägt, wird eine Fehlerdatei auf der Seite [!UICONTROL Bulksheet Management] aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Die Validierung großer Dateien dauert länger.
>* Bulksheet-Dateien für mehrere Kampagnen können bis zu 500.000 Datenzeilen enthalten. Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` usw. aufgeteilt.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](bulksheet-about.md)
>* [Löschen hochgeladener Bulksheets und Fehlerdateien](bulksheet-delete.md)
>* [Post-Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Beenden eines laufenden Bulksheet-Auftrags](bulksheet-stop-job.md)
>* [Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](bulksheet-upload.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
