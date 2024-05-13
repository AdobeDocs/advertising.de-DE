---
title: Propagieren von Inventar-Feed-Daten über Vorlagen
description: Erfahren Sie mehr über das Übertragen von Daten aus Ihren Inventar-Feeds über Anzeigenvorlagen, um die Kontostruktur zu verwalten und dynamische Anzeigen bereitzustellen.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propagieren von Inventar-Feed-Daten über Vorlagen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Nachdem Sie eine Anzeigen-Netzwerk-spezifische Feed-Vorlage erstellt und eine Feed-Datei oder eine [!DNL Google] oder [!DNL Microsoft] Merchant-Center-Konto mit ihm, können Sie Anzeigen dynamisch erstellen, indem Sie die Feed-Daten über die Vorlage entsprechend der [Feed-Dateneinstellungen](feed-settings-manage.md). Bei der Übertragung werden die Spaltennamen in der Vorlage durch Datenwerte im Feed ersetzt, und die generierten Kampagnen und ihre Komponenten haben die Standardeinstellungen, sofern in der Vorlage nichts anderes angegeben ist. Abhängig von den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Suchbegriffe) für die Anzeigen oder ordnet die Anzeigen der bestehenden Kontostruktur zu.

Wenn neue Feed-Daten neue Datenwerte für ein Element enthalten oder die Vorlage geändert wurde, werden vorhandene Anzeigen gelöscht und neue erstellt. Wenn die einzige Änderung die Bezeichnung der [!DNL Google Ads] Param 1 und Param 2, werden nur diese Werte aktualisiert. Duplizierte Anzeigen (dieselbe Anzeigenkopie und Landingpage) werden nie erstellt.

Wenn Sie Daten propagieren, können Sie optional die generierten Daten in einer Kampagnen-Hierarchieansicht in der Vorschau anzeigen, eine Bulksheet-Datei zur Überprüfung generieren oder eine Bulksheet-Datei für die sofortige Veröffentlichung in das Werbenetzwerk generieren. Wenn jede Vermehrungsaktion abgeschlossen ist, wird dem Tab Propagationen eine Zusammenfassung der Propagationen hinzugefügt, die die Anzahl der Entitätstypen angibt, die je nach Vermehrung erstellt, ausgesetzt oder gelöscht wurden. Wenn Sie die Daten nicht sofort posten, können Sie sie in der Vorschau anzeigen und später posten.

## Übertragen Sie Feed-Dateien aus der [!UICONTROL Templates] tab

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Aktivieren Sie das Kontrollkästchen neben den zu propagierenden Vorlagen.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Propagate]** und wählen Sie dann eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** So zeigen Sie die propagierten Daten auf der [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten. Sie können die Daten für jede Komponente und ihre Unterkomponenten auch später über die [!UICONTROL Templates] Registerkarte.

   * **[!UICONTROL Propagate and Preview]:** So erstellen Sie eine Bulksheet-Datei mit dem Namen`<feed file name>_<template name>`&quot;), die im [!UICONTROL Bulksheets] Ansicht zur Überprüfung (aber nicht auf [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten). Sie können die Bulksheet-Datei später über die [!UICONTROL Bulksheets] anzeigen.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

   * **[!UICONTROL Propagate and Post to SE]:** So erstellen Sie eine Bulksheet-Datei mit dem Namen`<feed file name>_<template name>`&quot;), der sofort zum Posten in das Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist im Abschnitt [!UICONTROL Bulksheets] Ansicht, aber nicht verfügbar im [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf.

   Die &quot;letzte Prop. Die Spalte Status zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

   Wenn jede Vermehrungsaktion abgeschlossen ist, wird der [!UICONTROL Propagations] -Tab, der die Anzahl der Entitätstypen angibt, die je nach Vermehrung erstellt, angehalten oder gelöscht wurden oder werden würden. Die Schätzung enthält keine Änderungen, die aus dem eigenen Anzeigeneditor des Werbenetzwerks vorgenommen wurden.

## Übertragen Sie Feed-Dateien aus der [!UICONTROL Feeds] Liste

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben der Feed-Datei.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Propagate/Post Feed Data]** und wählen Sie dann eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** So zeigen Sie die propagierten Daten auf der [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten. Sie können die Daten für jede Komponente und ihre Unterkomponenten auch später über die [!UICONTROL Templates] Registerkarte.

   * **[!UICONTROL Propagate and Preview]:** So erstellen Sie eine Bulksheet-Datei mit dem Namen`<feed file name>_<template name>`&quot;), die im [!UICONTROL Bulksheets] Ansicht zur Überprüfung (aber nicht auf [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten). Sie können die Bulksheet-Datei später über die [!UICONTROL Bulksheets] anzeigen.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

   * **[!UICONTROL Propagate and Post to SE]:** So erstellen Sie eine Bulksheet-Datei mit dem Namen`<feed file name>_<template name>`&quot;), der sofort zum Posten in das Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist im Abschnitt [!UICONTROL Bulksheets] Ansicht, aber nicht verfügbar im [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf.

1. Aktivieren Sie im Popup-Fenster das Kontrollkästchen neben jeder Vorlage, durch die Sie Daten aus der Feed-Datei übertragen möchten, und klicken Sie dann auf **[!UICONTROL Propagate Feed]**.

   Alle mit der Datei verknüpften Vorlagen werden aufgelistet.

Die [!UICONTROL Templates] wird geöffnet und das[!UICONTROL Last Prop. Status]&quot; zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

Wenn jede Vermehrungsaktion abgeschlossen ist, wird der [!UICONTROL Propagations] -Tab, der die Anzahl der Entitätstypen angibt, die je nach Vermehrung erstellt, angehalten oder gelöscht wurden oder werden würden. Die Schätzung enthält keine Änderungen, die aus dem eigenen Anzeigeneditor des Werbenetzwerks vorgenommen wurden.

## Anzeigen einer Propagierungszusammenfassung

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie auf **[!UICONTROL Propagations]** Registerkarte.

1. Klicken Sie neben dem Vorlagennamen auf ![Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;](/help/search-social-commerce/assets/settings.png "Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;") .

## Propagierungsauftrag stoppen

Sie können einen Übermittlungsauftrag für Inventar-Feed-Daten stoppen, während der Auftrag noch in der Warteschlange ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Im[!UICONTROL Last Prop. Status]&quot; neben dem Vorlagennamen, klicken Sie auf **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen für Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
