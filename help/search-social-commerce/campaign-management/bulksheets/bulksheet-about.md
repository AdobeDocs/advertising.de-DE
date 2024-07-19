---
title: Verwalten von Kampagnendaten mithilfe von Bulksheets
description: Erfahren Sie mehr über die Bulksheet-Funktionalität, die über das Werbenetzwerk verfügbar ist, den Bulksheet-Workflow und die Fehlerbehandlung.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Verwalten von Kampagnendaten mithilfe von Bulksheets

Ein Bulksheet ist eine Datei, die Kampagnendaten in einem bestimmten Format enthält und verwendet werden kann, um schnell Kampagnen- und Anzeigengruppendaten und Textanzeigen zu erstellen oder zu ändern. Sie können Bulksheets mit Daten für ein oder mehrere Konten, für bestimmte Kampagnen und Anzeigengruppen oder sogar für bestimmte Textanzeigen, Platzierungen und Produktgruppen generieren (herunterladen). Sie können Bulksheets verwenden, um große Datensätze zu verwalten oder kleine Änderungen vorzunehmen. Für jedes Anzeigennetzwerk sind unterschiedliche Informationsspalten erforderlich.

Sie können Bulksheets mit beliebig vielen Daten generieren oder diese optional manuell erstellen und hochladen (siehe Kapitel &quot;Erforderliche/einbezogene Daten in Bulksheets&quot;).

Nachdem Sie ein Bulksheet erstellt haben, können Sie fehlerhafte Landingpages identifizieren, die korrigiert werden müssen, oder zusätzliche Daten zum Hinzufügen oder Bearbeiten. Anschließend können Sie die Datei bearbeiten und in Search, Social und Commerce hochladen und optional planen, dass sie sofort oder später im entsprechenden Anzeigennetzwerk veröffentlicht wird. Sie können ein verfügbares Bulksheet auch sofort oder später posten.

Sie können optional Bulksheet-Dateien in ein bestimmtes FTP-Konto hochladen, um sie abzurufen und automatisch zu posten. Das Verzeichnis wird stündlich gescannt und neue Dateien werden in der Reihenfolge des Eingangs in das Suchnetzwerk veröffentlicht.

Alle Bulksheets, Validierungsfehlerdateien für Landingpages und andere Fehlerdateien werden 30 Tage nach ihrer Erstellung automatisch gelöscht, es sei denn, Sie löschen sie zuvor.

## Funktionalität nach Anzeigennetzwerk

* **Herunterladen, Hochladen und Posten:** [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] und [!DNL Yandex] Konten

* **Nur Herunterladen und Hochladen:** [!DNL Naver] Konten

  Sie können [!DNL Naver] -Daten zur Verwendung in Search, Social und Commerce hochladen, sie jedoch nicht im Werbenetzwerk veröffentlichen. Sie können auch Ihre vorhandenen (nicht synchronisierten) Daten herunterladen.

* **Nur Daten herunterladen:** [!DNL Pinterest], [!DNL Yahoo Native] und [!DNL Yahoo! Display Network] Konten

  Sie können Ihre vorhandenen (nicht synchronisierten) Daten herunterladen.

## Übersicht über die Verwendung von Bulksheets

Die Standardschritte bei der Verwendung von Bulksheets für synchronisierte Konten lauten wie folgt:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Laden Sie Daten für ein oder mehrere Konten, Kampagnen oder Anzeigengruppen in eine Bulksheet-Datei herunter](bulksheet-download.md). Optional können Sie ein netzwerkspezifisches Anzeigenblatt manuell ausfüllen und die Datei hochladen.

1. [Validieren Sie die Landingpages](bulksheet-validate-landing-pages.md) in den Basis-URLs (endgültigen) oder Ziel-URLs in der Datei.

1. Wenn Sie Daten hinzufügen oder Korrekturen vornehmen müssen:

   1. [Exportieren Sie die Datei](bulksheet-export.md) auf Ihren Desktop und bearbeiten Sie sie in [!DNL Microsoft Excel].

   1. [ Laden Sie die bearbeitete Datei manuell hoch ](bulksheet-upload.md) in Search, Social und Commerce oder [laden Sie die Datei zur automatischen Veröffentlichung in ein angegebenes FTP-Konto hoch](bulksheet-ftp-account.md).

1. (Für Dateien, die manuell hochgeladen werden) [Posten Sie die Datei](bulksheet-post.md) entweder beim Hochladen oder später im Werbenetzwerk.

1. (Bei Bedarf) Laden Sie alle neuen Fehlerdateien herunter, korrigieren Sie die Zeilen und posten Sie die Datei erneut.

## Fehler beim Hochladen und Veröffentlichen von Kampagnendaten beheben

In Search, Social und Commerce werden so viele Datenzeilen hochgeladen und veröffentlicht, wie es in einem Kampagnen-Massenblatt möglich ist, einschließlich der Tracking-URLs, die bei Bedarf generiert werden.

Wenn beim Bulksheet-Vorgang Fehler auftreten, wird eine der beiden folgenden Arten von Fehlerdateien generiert:

* **[!UICONTROL EF Errors]:** Wenn eine Datei oder einzelne Zeilen in der Datei nicht hochgeladen oder verarbeitet werden können, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_ef_errors.<extension used for the bulksheet>` erstellt. Wenn das Problem mit einzelnen Zeilen auftritt, werden diese Zeilen mit einer Erklärung für jeden Fehler eingefügt, damit er korrigiert werden kann.

* **[!UICONTROL SE Errors]:** Wenn eine Datei gepostet wird, das Werbenetzwerk jedoch einige oder alle Daten nicht akzeptiert, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_se_errors.<extension used for the bulksheet>` erstellt. Wenn einige, aber nicht alle Zeilen akzeptiert wurden, zeigt die Fehlerdatei die Zeilen an, die nicht veröffentlicht wurden, und eine Erläuterung jedes Fehlers, damit er korrigiert werden kann. Die Fehlermeldungen werden in den letzten drei Spalten jeder Zeile angezeigt.

>[!NOTE]
>
>Wenn Sie [!DNL Google Ads]-Anzeigen posten, die gegen die Werberichtlinien des Werbenetzwerks verstoßen, aber für Ausnahmen infrage kommen, werden diese Anzeigen automatisch mit Freistellungsanfragen neu gepostet. Wenn die Ausnahmeanfrage fehlschlägt, werden Informationen über die Verletzung in die Fehlerdatei aufgenommen.

Sie können jede Fehlerdatei herunterladen, Korrekturen direkt in den Zeilen vornehmen und die Datei dann erneut hochladen und posten.

Fehlerdateien werden nach 30 Tagen automatisch gelöscht, es sei denn, Sie löschen sie zuvor.

## Informationen zu den einzelnen Dateien

Alle heruntergeladenen Datendateien, hochgeladenen Dateien und Fehlerdateien sind unter [!UICONTROL Search] > [!UICONTROL Bulksheets] verfügbar.

Zu den Informationen für jede Datei gehören der aktuelle Aufgabenstatus, der Prozentsatz der abgeschlossenen Aufgabe, das Erstellungsdatum, (falls zutreffend) das Datum, an dem die Aufgabe im angegebenen Anzeigennetzwerk veröffentlicht wurde oder werden soll, das geplante Löschdatum und der Anmeldename des Benutzers, der die Aufgabe initiiert hat.

>[!MORELIKETHIS]
>
>* [Herunterladen/Erstellen einer Bulksheet-Datei](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](bulksheet-upload.md)
>* [Post-Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
