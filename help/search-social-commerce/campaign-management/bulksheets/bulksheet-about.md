---
title: Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets
description: Erfahren Sie mehr über die vom Anzeigennetzwerk verfügbaren Bulksheet-Funktionen, den Bulksheet-Workflow und die Fehlerbehandlung.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets

Eine Bulksheet ist eine Datei, die Kampagnendaten in einem bestimmten Format enthält und dazu verwendet werden kann, schnell Kampagnen- und Anzeigengruppenstrukturdaten und Textanzeigen zu erstellen oder zu ändern. Sie können Bulksheets mit Daten für ein oder mehrere Konten, für bestimmte Kampagnen und Anzeigengruppen oder sogar für bestimmte Textanzeigen, Platzierungen und Produktgruppen generieren (herunterladen). Sie können Bulksheets verwenden, um große Datensätze zu verwalten oder kleine Änderungen vorzunehmen. Jedes Werbenetzwerk benötigt verschiedene Spalten mit Informationen.

Sie können Bulksheets mit beliebig vielen Daten generieren - oder optional manuell erstellen und hochladen (siehe das Kapitel „Erforderliche/Enthaltene Daten in Bulksheets„).

Nachdem Sie eine Bulksheet erstellt haben, können Sie alle fehlerhaften Landingpages, die korrigiert werden müssen, oder zusätzliche Daten, die hinzugefügt oder bearbeitet werden müssen, identifizieren. Anschließend können Sie die Datei bearbeiten und in Search, Social und Commerce hochladen. Optional können Sie planen, dass sie sofort oder später im entsprechenden Werbenetzwerk gepostet wird. Sie können auch eine verfügbare Bulksheet entweder sofort oder später posten.

Sie können optional Bulksheet-Dateien in ein angegebenes FTP-Konto hochladen, um sie abzurufen und automatisch zu veröffentlichen. Das Verzeichnis wird stündlich überprüft, und neue Dateien werden in der Reihenfolge, in der sie empfangen werden, an das Suchnetzwerk gesendet.

Alle Bulksheets, Dateien mit Fehlern bei der Landingpage-Validierung und andere Fehlerdateien werden 30 Tage nach ihrer Erstellung automatisch gelöscht, es sei denn, sie werden zuvor gelöscht.

## Funktionalität nach Werbenetzwerk

* **Herunterladen, Hochladen und Veröffentlichen:** [!DNL Baidu]-, [!DNL Google Ads]-, [!DNL Microsoft Advertising]- und [!DNL Yandex]

* **Nur herunterladen und hochladen:** [!DNL Naver] Konten

  Sie können [!DNL Naver] Daten zur Verwendung in Search, Social und Commerce hochladen, sie jedoch nicht in das Werbenetzwerk posten. Sie können auch vorhandene (nicht synchronisierte) Daten herunterladen.

* **Nur Daten herunterladen:** [!DNL Pinterest]-, [!DNL Yahoo Native]- und [!DNL Yahoo! Display Network]

  Sie können Ihre vorhandenen (nicht synchronisierten) Daten herunterladen.

## Übersicht über die Verwendung von Bulksheets

Die Standardschritte bei der Verwendung von Bulksheets für synchronisierte Konten lauten wie folgt:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Daten für ein oder mehrere Konten, Kampagnen oder Anzeigengruppen in eine Bulksheet-Datei herunterladen](bulksheet-download.md). Optional können Sie eine netzwerkspezifische Bulksheet für die Anzeige manuell ausfüllen und die Datei hochladen.

1. [Validieren Sie die Landingpages](bulksheet-validate-landing-pages.md) in den Basis-(endgültigen) URLs oder Ziel-URLs in der Datei.

1. Wenn Sie Daten hinzufügen oder Korrekturen vornehmen müssen:

   1. [Exportieren Sie die Datei](bulksheet-export.md) auf Ihren Desktop und bearbeiten Sie sie in [!DNL Microsoft Excel].

   1. [Manuelles Hochladen der bearbeiteten Datei](bulksheet-upload.md) in Search, Social und Commerce oder [Hochladen der Datei in ein angegebenes FTP-Konto](bulksheet-ftp-account.md) zur automatischen Veröffentlichung.

1. (Für manuell hochgeladene Dateien) [Veröffentlichen Sie die Datei](bulksheet-post.md) entweder beim Hochladen oder später in das Werbenetzwerk.

1. (Falls erforderlich) Laden Sie alle neuen Fehlerdateien herunter, korrigieren Sie die Zeilen und veröffentlichen Sie die Datei erneut.

## Fehler beim Hochladen und Veröffentlichen von Kampagnendaten beheben

Search, Social und Commerce laden so viele Datenzeilen hoch und veröffentlichen sie, wie sie von einem Kampagnen-Bulk-Sheet aus können, einschließlich der Tracking-URLs, die sie bei Bedarf generiert.

Wenn während des Bulksheet-Vorgangs Fehler auftreten, wird einer der beiden folgenden Fehlerdateitypen generiert:

* **[!UICONTROL EF Errors]:** Wenn eine Datei oder einzelne Zeilen in der Datei nicht hochgeladen oder verarbeitet werden können, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_ef_errors.<extension used for the bulksheet>` erstellt. Wenn das Problem bei einzelnen Zeilen besteht, werden diese Zeilen mit einer Erläuterung jedes Fehlers einbezogen, damit er korrigiert werden kann.

* **[!UICONTROL SE Errors]:** Wenn eine Datei veröffentlicht wird, das Anzeigennetzwerk jedoch einige oder alle Daten nicht akzeptiert, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_se_errors.<extension used for the bulksheet>` erstellt. Wenn einige, aber nicht alle Zeilen akzeptiert wurden, zeigt die Fehlerdatei die Zeilen an, die nicht veröffentlicht wurden, und eine Erklärung für jeden Fehler, damit er korrigiert werden kann. Die Fehlermeldungen werden in den letzten drei Spalten jeder Zeile angezeigt.

>[!NOTE]
>
>Wenn Sie [!DNL Google Ads] Anzeigen posten, die gegen die Werberichtlinien des Werbenetzwerks verstoßen, aber für Ausnahmen infrage kommen, werden diese Anzeigen automatisch mit Freistellungsanträgen erneut geschaltet. Schlägt die Freistellungsanfrage fehl, werden Informationen über die Verletzung in die Fehlerdatei aufgenommen.

Sie können beide Arten von Fehlerdateien herunterladen, Korrekturen direkt in den Zeilen vornehmen und dann die Datei erneut hochladen und veröffentlichen.

Fehlerdateien werden nach 30 Tagen automatisch gelöscht, es sei denn, Sie löschen sie früher.

## Informationen zu den einzelnen Dateien

Alle heruntergeladenen Datendateien, hochgeladenen Dateien und Fehlerdateien sind unter [!UICONTROL Search] > [!UICONTROL Bulksheets] verfügbar.

Zu den Informationen für jede Datei gehören der aktuelle Aufgabenstatus und der Prozentsatz der abgeschlossenen Aufgabe, das Erstellungsdatum, (falls zutreffend) das Datum, an dem sie im angegebenen Werbenetzwerk veröffentlicht wurde oder werden wird, das geplante Löschdatum und der Anmeldename des Benutzers, der die Aufgabe initiiert hat.

>[!MORELIKETHIS]
>
>* [Bulksheet-Datei herunterladen/erstellen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](bulksheet-upload.md)
>* [Buchen Sie Bulksheets oder korrigierte Fehlerdateien](bulksheet-post.md)
>* [Exportieren einer generierten oder hochgeladenen Bulksheet-Datei](bulksheet-export.md)
