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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Nachdem Sie eine Ad-Netzwerk-spezifische Feed-Vorlage erstellt und eine Feed-Datei oder ein Merchant-Center-Konto vom Typ [!DNL Google] oder [!DNL Microsoft] damit verknüpft haben, können Sie dynamische Anzeigen erstellen, indem Sie die Feed-Daten gemäß den [Feed-Dateneinstellungen](feed-settings-manage.md) über die Vorlage propagieren. Bei der Übertragung werden die Spaltennamen in der Vorlage durch Datenwerte im Feed ersetzt, und die generierten Kampagnen und ihre Komponenten haben die Standardeinstellungen, sofern in der Vorlage nichts anderes angegeben ist. Abhängig von den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Suchbegriffe) für die Anzeigen oder ordnet die Anzeigen der bestehenden Kontostruktur zu.

Wenn neue Feed-Daten neue Datenwerte für ein Element enthalten oder die Vorlage geändert wurde, werden vorhandene Anzeigen gelöscht und neue erstellt. Wenn die einzige Änderung die Bezeichnung von [!DNL Google Ads] Param 1 und Param 2 ist, werden nur diese Werte aktualisiert. Duplizierte Anzeigen (dieselbe Anzeigenkopie und Landingpage) werden nie erstellt.

Wenn Sie Daten propagieren, können Sie optional die generierten Daten in einer Kampagnen-Hierarchieansicht in der Vorschau anzeigen, eine Bulksheet-Datei zur Überprüfung generieren oder eine Bulksheet-Datei für die sofortige Veröffentlichung in das Werbenetzwerk generieren. Wenn jede Vermehrungsaktion abgeschlossen ist, wird dem Tab Propagationen eine Zusammenfassung der Propagationen hinzugefügt, die die Anzahl der Entitätstypen angibt, die je nach Vermehrung erstellt, ausgesetzt oder gelöscht wurden. Wenn Sie die Daten nicht sofort posten, können Sie sie in der Vorschau anzeigen und später posten.

## Übertragen von Feed-Dateien über die Registerkarte &quot;[!UICONTROL Templates]&quot;

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Aktivieren Sie das Kontrollkästchen neben den zu propagierenden Vorlagen.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Propagate]** und wählen Sie dann eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** Zum Anzeigen der propagierten Daten auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]. Sie können die Daten für jede Komponente und ihre Unterkomponenten auch später auf der Registerkarte [!UICONTROL Templates] posten.

   * **[!UICONTROL Propagate and Preview]:** Um eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) zu erstellen, die in der [!UICONTROL Bulksheets]-Ansicht zur Überprüfung verfügbar ist (jedoch nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]). Sie können die Bulksheet-Datei später über die Ansicht &quot;[!UICONTROL Bulksheets]&quot;posten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

   * **[!UICONTROL Propagate and Post to SE]:** Um eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) zu erstellen, die sofort zum Posten in das Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist in der Ansicht [!UICONTROL Bulksheets] verfügbar, aber nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads].

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf.

   Die &quot;letzte Prop. Die Spalte Status zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

   Wenn jede Vermehrungsaktion abgeschlossen ist, wird dem Tab [!UICONTROL Propagations] eine Zusammenfassung der Vermehrung hinzugefügt, die die Anzahl der Entitätstypen angibt, die basierend auf der Vermehrung erstellt, ausgesetzt oder gelöscht wurden. Die Schätzung enthält keine Änderungen, die aus dem eigenen Anzeigeneditor des Werbenetzwerks vorgenommen wurden.

## Übertragen von Feed-Dateien aus der Liste &quot;[!UICONTROL Feeds]&quot;

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben der Feed-Datei.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Propagate/Post Feed Data]** und wählen Sie dann eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** Zum Anzeigen der propagierten Daten auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]. Sie können die Daten für jede Komponente und ihre Unterkomponenten auch später auf der Registerkarte [!UICONTROL Templates] posten.

   * **[!UICONTROL Propagate and Preview]:** Um eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) zu erstellen, die in der [!UICONTROL Bulksheets]-Ansicht zur Überprüfung verfügbar ist (jedoch nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]). Sie können die Bulksheet-Datei später über die Ansicht &quot;[!UICONTROL Bulksheets]&quot;posten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

   * **[!UICONTROL Propagate and Post to SE]:** Um eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) zu erstellen, die sofort zum Posten in das Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist in der Ansicht [!UICONTROL Bulksheets] verfügbar, aber nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads].

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf.

1. Aktivieren Sie im Popup-Fenster das Kontrollkästchen neben jeder Vorlage, durch die Sie Daten aus der Feed-Datei übertragen möchten, und klicken Sie dann auf **[!UICONTROL Propagate Feed]**.

   Alle mit der Datei verknüpften Vorlagen werden aufgelistet.

Die Registerkarte [!UICONTROL Templates] wird geöffnet und die Spalte &quot;[!UICONTROL Last Prop. Status]&quot; zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

Wenn jede Vermehrungsaktion abgeschlossen ist, wird dem Tab [!UICONTROL Propagations] eine Zusammenfassung der Vermehrung hinzugefügt, die die Anzahl der Entitätstypen angibt, die basierend auf der Vermehrung erstellt, ausgesetzt oder gelöscht wurden. Die Schätzung enthält keine Änderungen, die aus dem eigenen Anzeigeneditor des Werbenetzwerks vorgenommen wurden.

## Anzeigen einer Propagierungszusammenfassung

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Propagations]** .

1. Klicken Sie neben dem Vorlagennamen auf ![Einstellungssymbol anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungssymbol anzeigen/bearbeiten") .

## Propagierungsauftrag stoppen

Sie können einen Übermittlungsauftrag für Inventar-Feed-Daten stoppen, während der Auftrag noch in der Warteschlange ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Klicken Sie in der Spalte &quot;[!UICONTROL Last Prop. Status]&quot; neben dem Vorlagennamen auf **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen für Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
