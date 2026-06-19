---
title: (Neue Benutzeroberfläche) Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets
description: Erfahren Sie mehr über die Bulksheet-Funktionen, die vom Anzeigennetzwerk verfügbar sind, den Bulksheet-Workflow und die Fehlerbehandlung in der neuen Benutzeroberfläche für Suche, Social und Commerce.
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
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 772
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets

Eine Bulksheet ist eine Datei, die Kampagnendaten in einem bestimmten Format enthält und dazu verwendet werden kann, schnell Kampagnen- und Anzeigengruppenstrukturdaten und Textanzeigen zu erstellen oder zu ändern. Sie können Bulksheets mit Daten für ein oder mehrere Konten, für bestimmte Kampagnen und Anzeigengruppen oder sogar für bestimmte Textanzeigen, Platzierungen und Produktgruppen generieren (herunterladen). Sie können Bulksheets verwenden, um große Datensätze zu verwalten oder kleine Änderungen vorzunehmen. Jedes Werbenetzwerk benötigt verschiedene Spalten mit Informationen.

Sie können Bulksheets mit beliebig vielen Daten generieren oder diese optional manuell erstellen und hochladen. Siehe &quot;[Erforderliche und eingeschlossene Daten in Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)&quot; für Dateiformatanforderungen und &quot;[Vorgänge, die Sie in Bulksheets ausführen können](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) für unterstützte Vorgänge nach Werbenetzwerk.

Nachdem Sie eine Bulksheet erstellt haben, können Sie alle fehlerhaften Landingpages, die korrigiert werden müssen, oder zusätzliche Daten, die hinzugefügt oder bearbeitet werden müssen, identifizieren. Anschließend können Sie die Datei bearbeiten und in Search, Social und Commerce hochladen. Optional können Sie planen, dass sie sofort oder später im entsprechenden Werbenetzwerk gepostet wird. Sie können auch eine verfügbare Bulksheet entweder sofort oder später posten.

Alle Bulksheets, Dateien mit Fehlern bei der Landingpage-Validierung und andere Fehlerdateien werden 30 Tage nach ihrer Erstellung automatisch gelöscht, es sei denn, sie werden zuvor gelöscht.

## Funktionalität nach Anzeigennetzwerk {#bulksheet-functionality-by-network}

* **Herunterladen, Hochladen und Veröffentlichen:** [!DNL Baidu]-, [!DNL Google Ads]-, [!DNL Microsoft Advertising]- und [!DNL Yandex]

* **Nur herunterladen und hochladen:** [!DNL Naver] Konten

  Sie können [!DNL Naver] Daten zur Verwendung in Search, Social und Commerce hochladen, sie jedoch nicht in das Werbenetzwerk posten. Sie können auch vorhandene (nicht synchronisierte) Daten herunterladen.

* **Nur Daten herunterladen:** [!DNL Pinterest], [!DNL Yahoo DSP], [!DNL Yahoo Native] Konten

  Sie können Ihre vorhandenen (nicht synchronisierten) Daten herunterladen.

## Übersicht über die Verwendung von Bulksheets

Die Standardschritte zur Verwendung von Bulksheets mit synchronisierten Konten lauten wie folgt:

1. [Daten für ein oder mehrere Konten, Kampagnen oder Anzeigengruppen in eine Bulksheet-Datei herunterladen](download.md). Optional können Sie eine netzwerkspezifische Bulksheet für die Anzeige manuell ausfüllen und die Datei hochladen.

1. [Validieren Sie die Landingpages](validate-landing-pages.md) in den Basis-(endgültigen) URLs oder Ziel-URLs in der Datei.

1. Wenn Sie Daten hinzufügen oder Korrekturen vornehmen müssen:

   1. Exportieren Sie die Datei auf Ihren Desktop und bearbeiten Sie sie in [!DNL Microsoft Excel].

   1. [Laden Sie die bearbeitete Datei manuell &#x200B;](upload.md) Search, Social und Commerce hoch.

1. (Für manuell hochgeladene Dateien) [Veröffentlichen Sie die Datei](post.md) entweder beim Hochladen oder später in das Werbenetzwerk.

1. (Falls erforderlich) Laden Sie alle neuen Fehlerdateien herunter, korrigieren Sie die Zeilen und veröffentlichen Sie die Datei erneut.

## Fehler beim Hochladen und Veröffentlichen von Kampagnendaten beheben

Search, Social und Commerce laden so viele Datenzeilen hoch und veröffentlichen sie, wie sie von einer Kampagnenbulktabelle aus können, einschließlich der Tracking-URLs, die sie bei Bedarf generiert.

Wenn während eines Bulksheet-Vorgangs Fehler auftreten, wird einer der beiden folgenden Fehlerdateitypen generiert:

* **[!UICONTROL EF Errors]:** Wenn eine Datei oder einzelne Zeilen in der Datei nicht hochgeladen oder verarbeitet werden können, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_ef_errors.<extension used for the bulksheet>` erstellt. Wenn das Problem bei einzelnen Zeilen besteht, werden diese Zeilen mit einer Erläuterung jedes Fehlers einbezogen, damit er korrigiert werden kann.

* **[!UICONTROL SE Errors]:** Wenn eine Datei veröffentlicht wird, das Anzeigennetzwerk jedoch einige oder alle Daten nicht akzeptiert, wird eine Fehlerdatei mit dem Namen `<uploaded file name>_se_errors.<extension used for the bulksheet>` erstellt. Wenn einige, aber nicht alle Zeilen akzeptiert wurden, zeigt die Fehlerdatei die Zeilen an, die nicht veröffentlicht wurden, und eine Erklärung für jeden Fehler, damit er korrigiert werden kann. Die Fehlermeldungen werden in den letzten drei Spalten jeder Zeile angezeigt.

>[!NOTE]
>
>Wenn Sie [!DNL Google Ads] Anzeigen posten, die gegen die Werberichtlinien des Werbenetzwerks verstoßen, aber für Ausnahmen infrage kommen, werden diese Anzeigen automatisch mit Freistellungsanträgen erneut geschaltet. Schlägt die Freistellungsanfrage fehl, werden Informationen über die Verletzung in die Fehlerdatei aufgenommen.

Sie können beide Arten von Fehlerdateien herunterladen, Korrekturen direkt in den Zeilen vornehmen und dann die Datei erneut hochladen und veröffentlichen.

Fehlerdateien werden nach 30 Tagen automatisch gelöscht, es sei denn, Sie löschen sie früher.

## Informationen zu den einzelnen Dateien

Alle heruntergeladenen Datendateien, hochgeladenen Dateien und Fehlerdateien sind über [!UICONTROL Setup] [!UICONTROL Bulksheets] \> verfügbar.

Zu den Informationen für jede Datei gehören der aktuelle Aufgabenstatus und der Prozentsatz der abgeschlossenen Aufgabe, das Erstellungsdatum, (falls zutreffend) das Datum, an dem sie im angegebenen Werbenetzwerk veröffentlicht wurde oder werden wird, das geplante Löschdatum und der Anmeldename des Benutzers, der die Aufgabe initiiert hat.

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Herunterladen/Erstellen einer Bulksheet-Datei](download.md)
>* [(Neue Benutzeroberfläche) Hochladen einer Bulksheet- oder korrigierten Fehlerdatei](upload.md)
>* [&#x200B; (neue Benutzeroberfläche) Posten von Bulksheets oder korrigierte Fehlerdateien](post.md)
>* [(Neue Benutzeroberfläche) Validieren von Landingpages in Bulksheet-Dateien](validate-landing-pages.md)
>* [(Neue Benutzeroberfläche) Löschen hochgeladener Bulksheets und Fehlerdateien](delete.md)
>* [(Neue Benutzeroberfläche) Halten Sie einen laufenden Bulksheet-Vorgang an](stop-job.md)
