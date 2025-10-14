---
title: Von Feeds generierte Kampagnendaten in Werbenetzwerke posten
description: Erfahren Sie, wie Sie aus Inventardaten-Feeds generierte Daten in Werbenetzwerke posten.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Von Feeds generierte Kampagnendaten in Werbenetzwerke posten

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Sie können Kampagnendaten, die aus einem Feed generiert wurden, veröffentlichen, während Sie die Daten über die zugehörigen Vorlagen oder als separaten Prozess weitergeben. Sobald Sie Daten posten, werden alle vorhandenen propagierten Daten aus den [!UICONTROL Campaigns]-, [!UICONTROL Ad Groups]-, [!UICONTROL Keywords]- und [!UICONTROL Ads] entfernt.

Für eine erfolgreiche Veröffentlichung müssen alle Anzeigengruppen Kampagnen zugewiesen werden, alle Keywords und Anzeigen müssen Anzeigengruppen zugewiesen werden und alle erforderlichen Informationen müssen ohne Längenverletzungen enthalten sein.

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate and Preview]&quot; verwendet haben[&#x200B; veröffentlichen Sie die generierte Bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md)Datei (mit dem Namen &quot;`<feed file name>_<template name>`„) aus der [!UICONTROL Bulksheets].

  Wenn Sie Ihre Landingpages zuvor nicht [validiert haben](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) können Sie dies tun, bevor Sie die Datei posten.

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate only]&quot; verwendet haben, können Sie die generierten Daten für Komponenten mit dem [[!UICONTROL New] Status &#x200B;](propagated-data-status.md) einer Kampagnenhierarchieansicht von der Registerkarte &quot;[!UICONTROL Templates]&quot; aus veröffentlichen.

  >[!NOTE]
  >
  >Aktive oder gelöschte Komponenten können neue Unterkomponenten enthalten, und die Unterkomponenten können veröffentlicht werden, wenn die Daten gültig sind.

  >[!TIP]
  >
  >Wenn Sie Ihre Landingpages zuvor nicht validiert haben und dies tun möchten, [&#x200B; Sie die Daten in der [!UICONTROL Bulksheets]-Ansicht &#x200B;](feed-data-propagate.md) und in der Vorschau anzeigen, anstatt sie im Werbenetzwerk zu posten. Anschließend können Sie [URLs überprüfen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) bevor Sie die Datei manuell im Werbenetzwerk posten.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

   1. Aktivieren Sie das Kontrollkästchen neben der Vorlage.

   1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Post]**.

   1. Geben Sie in den Buchungseinstellungen Informationen in die Felder ein oder wählen Sie diese aus und klicken Sie dann auf **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Welche Kontokomponenten gebucht werden.

      * **[!UICONTROL Scheduling]:** Wann die Datei gepostet werden soll:

         * *[!UICONTROL Post to search engine now]* (Standard): Erstellt eine Bulk Sheet-Datei aus den weitergegebenen Feed-Daten und beginnt sofort mit der Veröffentlichung.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Erstellt eine Bulksheet-Datei und veröffentlicht sie später. Geben Sie Folgendes an:

            * **[!UICONTROL Start Time]:** Ein Datum und eine Uhrzeit in der Zukunft, zu der die Bulksheet-Datei im Anzeigennetzwerk veröffentlicht werden soll. Standardmäßig wird die Datei am nächsten Tag um 0:00 Uhr (12:00 Uhr) gesendet. **Hinweis** Bei großen Dateien, die eine längere Verarbeitung erfordern, sind die veröffentlichten Daten nicht sofort in den Kampagnenverwaltungsansichten oder im Anzeigenmanager des Netzwerks verfügbar.

            * **[!UICONTROL End Time]:** Ein künftiges Datum und eine zukünftige Uhrzeit, zu der die veröffentlichten Anzeigen basierend auf der Einstellung &quot;[-Daten“ &#x200B;](feed-settings-manage.md#feed-data-settings) &quot;[!UICONTROL When the Scheduled End Date is reached]&quot; angehalten oder gelöscht werden können. Standardmäßig ist die Endzeit um 00:00 Uhr (12:00 Uhr) 30 Tage von heute entfernt. Wählen Sie **[!UICONTROL None]** aus, um die Daten unbegrenzt aktiv zu halten (oder bis Sie neue Daten für die Vorlage übertragen), oder geben Sie ein Datum und eine Uhrzeit an.

              Um ein Datum anzugeben, verwenden Sie das Format TT/MM/JJJJ oder TT/M/JJJJ oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender"), um den Kalender zu öffnen und [ein Datum auszuwählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um eine Zeit zu ändern, geben Sie die Zeit im 24-Stunden-Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in 30-Minuten-Intervallen) aus der Liste aus.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Erstellt eine Bulk Sheet-Datei, die in der Ansicht [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] verfügbar ist. Sie können die Datei optional von dort aus posten.

           Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, liegt die Datei im ZIP-Format vor. Sie müssen die Datei nicht entpacken, um sie zu veröffentlichen.

      * **[!UICONTROL Generate Tracking URLs]:** Ob Tracking-URLs für Keywords und Anzeigenvarianten in die Bulksheet-Datei aufgenommen werden sollen: *[!UICONTROL Yes]* (Standard) oder *[!UICONTROL No]*.

        Wenn Sie *[!UICONTROL Yes]* auswählen, werden die URLs aus den Basis-URLs für die Keywords und Anzeigen gemäß den [!UICONTROL Tracking Methods] Parametern in den [Kontoeinstellungen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) oder, wenn Sie Daten vorhandenen Kampagnen zuordnen, den [!UICONTROL Tracking Methods] Parametern in den vorhandenen [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) generiert.

        Wenn für die entsprechenden Elemente Tracking-URLs vorhanden sind, werden sie nicht neu generiert, es sei denn, neue werden benötigt (z. B. wenn der Schlüsselwortübereinstimmungstyp, der Kreativtext oder die Tracking-Parameter des Kontos geändert wurden).

      * **[!UICONTROL Bulksheet Name]:** Der Name der aus den weitergegebenen Feed-Daten zu erstellenden Bulksheet-Datei. Standardmäßig trägt die Datei den Namen `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Sie können die Datei nach Wunsch umbenennen, sie muss jedoch mit einer der folgenden Dateierweiterungen enden: `.tsv` (für tabulatorgetrennte Werte), `.txt` (für ASCII-Text), `.csv` (für kommagetrennte Werte) oder `.zip` (für eine komprimierte TSV-Datei). Verwenden Sie für Daten, die internationale Zeichen enthalten, das TSV- oder TXT-Format.

        Die gepostete Datei ist in der [!UICONTROL Bulksheets]-Ansicht 30 Tage lang verfügbar, unabhängig davon, ob Sie sie im Anzeigennetzwerk posten oder nicht.

Die Spalte &quot;[!UICONTROL Last Prop. Status]&quot; zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

Wenn die Bulksheet erstellt wird, wird sie in der [!UICONTROL Bulksheets] angezeigt. Wenn die Datei veröffentlicht wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Wenn jedoch alle oder einige der Daten nicht veröffentlicht werden können, wird eine Fehlerdatei in der [!UICONTROL Bulksheets]-Ansicht aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Unabhängig von der ausgewählten Planungsoption werden die angegebenen Daten aus den [!UICONTROL Campaigns]-, [!UICONTROL Ad Groups]-, [!UICONTROL Keywords]- und [!UICONTROL Ads] entfernt.
>* Die Verarbeitung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei während des Prozesses verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
>* Bevor eine Bulksheet-Datei veröffentlicht wird, können Sie [die Veröffentlichung abbrechen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Anzeigen der von Feeds generierten Daten](propagated-data-view.md)
>* [Bearbeiten der von Feeds generierten Daten](propagated-data-edit.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
>* [Status der von Feeds generierten Daten](propagated-data-status.md)
