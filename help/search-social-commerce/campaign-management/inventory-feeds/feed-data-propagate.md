---
title: Übertragen von Inventar-Feed-Daten über Vorlagen
description: Erfahren Sie, wie Sie Daten aus Ihren Inventar-Feeds über Anzeigenvorlagen übertragen können, um die Kontostruktur zu verwalten und dynamische Anzeigen bereitzustellen.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Übertragen von Inventar-Feed-Daten über Vorlagen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Nachdem Sie eine Anzeigennetzwerk-spezifische Feed-Vorlage erstellt und eine Feed-Datei oder ein [!DNL Google]- oder [!DNL Microsoft]-Händlercenter-Konto damit verknüpft haben, können Sie Anzeigen dynamisch erstellen, indem Sie die Feed-Daten gemäß den Einstellungen für [-Daten über die Vorlage ](feed-settings-manage.md). Während der Übertragung werden die Spaltennamen in der Vorlage durch Datenwerte im Feed ersetzt, und die generierten Kampagnen und ihre Komponenten haben die Standardeinstellungen, sofern die Vorlage nicht etwas Anderes angibt. Je nach den Vorlagenoptionen erstellt Search, Social und Commerce entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Keywords) für die Anzeigen oder ordnet die Anzeigen der bestehenden Kontostruktur zu.

Wenn neue Feed-Daten neue Datenwerte für ein Element enthalten oder die Vorlage geändert wurde, werden vorhandene Anzeigen gelöscht und neue erstellt. Wenn die einzige Änderung die Bezeichnung von [!DNL Google Ads] Param 1 und Param 2 ist, werden nur diese Werte aktualisiert. Doppelte Anzeigen (dieselbe Anzeigenkopie und Landingpage) werden nie erstellt.

Bei der Übertragung von Daten können Sie optional eine Vorschau der generierten Daten in einer Hierarchieansicht der Kampagne anzeigen, eine Bulksheet-Datei zur Überprüfung generieren oder eine Bulksheet-Datei zur sofortigen Veröffentlichung im Werbenetzwerk generieren. Wenn jede Verbreitungsaktion abgeschlossen ist, wird der Registerkarte Ausbreitungen eine Zusammenfassung der Ausbreitung hinzugefügt, die die Anzahl jedes Entitätstyps angibt, der basierend auf der Ausbreitung erstellt wurde oder erstellt, angehalten oder gelöscht werden würde. Wenn Sie die Daten nicht sofort posten, können Sie sie in der Vorschau anzeigen und später posten.

## Übertragen von Feed-Dateien über die Registerkarte [!UICONTROL Templates]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Aktivieren Sie das Kontrollkästchen neben den zu propagierenden Vorlagen.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Propagate]** und wählen Sie eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** Anzeigen der propagierten Daten auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]. Sie können die Daten für eine beliebige Komponente und ihre Unterkomponenten auch später über die Registerkarte [!UICONTROL Templates] posten.

   * **[!UICONTROL Propagate and Preview]:** So erstellen Sie eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`„), die in der [!UICONTROL Bulksheets] zur Überprüfung verfügbar ist (jedoch nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]). Sie können die Bulksheet-Datei später über die [!UICONTROL Bulksheets] posten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen.

   * **[!UICONTROL Propagate and Post to SE]:** Erstellen einer Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`„), die sofort zur Veröffentlichung im Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist in der [!UICONTROL Bulksheets] verfügbar, nicht jedoch auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads].

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, liegt die Datei im ZIP-Format vor.

   Die „letzte Prop. Die Spalte „Status“ zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

   Wenn jede Weiterleitungsaktion abgeschlossen ist, wird der Registerkarte [!UICONTROL Propagations] eine Zusammenfassung der Weiterleitung hinzugefügt, die die Anzahl jedes Entitätstyps angibt, der basierend auf der Weiterleitung erstellt wurde oder werden würde, angehalten oder gelöscht wurde. Die Schätzung umfasst keine Änderungen, die im eigenen Anzeigeneditor des Anzeigennetzwerks vorgenommen wurden.

## Übertragen von Feed-Dateien aus der [!UICONTROL Feeds]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben der Feed-Datei.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Propagate/Post Feed Data]** und wählen Sie dann eine der folgenden Optionen aus:

   * **[!UICONTROL Propagate Only]:** Anzeigen der propagierten Daten auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]. Sie können die Daten für eine beliebige Komponente und ihre Unterkomponenten auch später über die Registerkarte [!UICONTROL Templates] posten.

   * **[!UICONTROL Propagate and Preview]:** So erstellen Sie eine Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`„), die in der [!UICONTROL Bulksheets] zur Überprüfung verfügbar ist (jedoch nicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads]). Sie können die Bulksheet-Datei später über die [!UICONTROL Bulksheets] posten.

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen.

   * **[!UICONTROL Propagate and Post to SE]:** Erstellen einer Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`„), die sofort zur Veröffentlichung im Werbenetzwerk in die Warteschlange gestellt wird. Die Bulksheet-Datei ist in der [!UICONTROL Bulksheets] verfügbar, nicht jedoch auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads].

     Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, liegt die Datei im ZIP-Format vor.

1. Aktivieren Sie im Popup-Fenster das Kontrollkästchen neben jeder Vorlage, durch die Sie Daten aus der Feed-Datei übertragen möchten, und klicken Sie dann auf **[!UICONTROL Propagate Feed]**.

   Alle mit der Datei verknüpften Vorlagen werden aufgelistet.

Die Registerkarte &quot;[!UICONTROL Templates]&quot; wird geöffnet und in der Spalte &quot;[!UICONTROL Last Prop. Status]&quot; wird der Auftragsstatus für die entsprechenden Vorlagen angezeigt.

Wenn jede Weiterleitungsaktion abgeschlossen ist, wird der Registerkarte [!UICONTROL Propagations] eine Zusammenfassung der Weiterleitung hinzugefügt, die die Anzahl jedes Entitätstyps angibt, der basierend auf der Weiterleitung erstellt wurde oder werden würde, angehalten oder gelöscht wurde. Die Schätzung umfasst keine Änderungen, die im eigenen Anzeigeneditor des Anzeigennetzwerks vorgenommen wurden.

## Anzeigen einer Ausbreitungszusammenfassung

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Propagations]** .

1. Klicken Sie neben dem Vorlagennamen auf das Symbol ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungssymbol anzeigen/bearbeiten") .

## Stoppen eines Ausbreitungsauftrags

Sie können einen Verbreitungsauftrag für Inventar-Feed-Daten stoppen, während der Auftrag noch in der Warteschlange ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Klicken Sie in der Spalte &quot;[!UICONTROL Last Prop. Status]&quot; neben dem Vorlagennamen auf **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen für Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Anzeigen der von Feeds generierten Daten](propagated-data-view.md)
>* [Bearbeiten der von Feeds generierten Daten](propagated-data-edit.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
>* [Status der von Feeds generierten Daten](propagated-data-status.md)
