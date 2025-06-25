---
title: Anzeigen der von Feeds generierten Daten
description: Erfahren Sie, wie Sie Daten anzeigen, die aus Inventardaten-Feeds generiert wurden.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Anzeigen der von Feeds generierten Daten

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Wenn Sie Feed-Daten übertragen, ohne sie gleichzeitig im Anzeigennetzwerk zu posten, können Sie die Daten auf eine der folgenden Arten in der Vorschau anzeigen. Sie können später optional [Daten](propagated-data-post.md) von beiden Standorten an die entsprechenden Werbenetzwerke senden.

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate and Preview]&quot; verwendet haben, zeigen Sie das generierte Bulksheet (mit dem Namen &quot;`<feed file name>_<template name>`„) in der [!UICONTROL Bulksheets] an. Auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] sind keine Daten enthalten. Mit dieser Option können Sie [ Landingpages, die mit den Anzeigen und Keywords ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) sind, validieren, bevor Sie die Daten posten.

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate only]&quot; verwendet haben, zeigen Sie die generierten Daten in einer Kampagnenhierarchieansicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] an.

  Die Kampagnenhierarchieansichten zeigen nur die aus der Feed-Datei generierten Daten an, nicht die vorhandenen Kontokomponenten. Nachdem Daten für eine Komponente und alle zugehörigen Unterkomponenten an das Werbenetzwerk gesendet wurden, werden sie nicht mehr in der Kampagnenhierarchieansicht aufgelistet.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

   1. (Optional) So zeigen Sie nur Kampagnenkomponenten an, die für eine bestimmte Vorlage erstellt wurden:

      1. Klicken Sie auf den Namen der Vorlage.

      1. Erweitern Sie im Menü [!UICONTROL Accounts] im linken Navigationsbereich den Knoten „Anzeigennetzwerk“ und den Knoten „Anzeigennetzwerkkonto“ und aktivieren Sie dann das Kontrollkästchen neben dem Vorlagennamen.

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** oder **[!UICONTROL Ads]**, je nachdem, welche Komponenten Sie anzeigen möchten.

      >[!NOTE]
      >
      >* Sofern Sie keine Daten für eine bestimmte Vorlage anzeigen, werden auf den Registerkarten [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] alle Anzeigengruppen, Keywords und Anzeigen aufgelistet, die aus allen Vorlagen und Feed-Dateien erstellt wurden. Für [!DNL Google Ads] Shopping-Anzeigen verwendete Produktgruppen werden auf der Registerkarte [!UICONTROL Keywords] aufgeführt.
      >* Um nur die Unterkomponenten einer bestimmten Kampagne anzuzeigen, öffnen Sie zunächst die Registerkarte [!UICONTROL Campaigns] . Um nur die Unterkomponenten einer bestimmten Anzeigengruppe anzuzeigen, zeigen Sie zunächst die Registerkarte [!UICONTROL Ad Groups] an.

   1. (Optional) Führen Sie einen der folgenden Schritte aus, um weitere Informationen anzuzeigen:

      * Um die Einstellungen für eine beliebige Kampagne, Anzeigengruppe, ein beliebiges Keyword oder eine beliebige Anzeige anzuzeigen, klicken Sie [Einstellungssymbol anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Symbol „Einstellungen anzeigen/bearbeiten“") neben dem Namen.

      * Gehen Sie wie folgt vor, um die Unterkomponenten einer Kampagne oder Anzeigengruppe anzuzeigen:

         * Um alle Anzeigengruppen in einer Kampagne aufzulisten, klicken Sie auf den Namen der Kampagne.

         * Um alle Keywords oder Produktziele in einer Anzeigengruppe aufzulisten, klicken Sie auf den Namen der Anzeigengruppe.

         * Um alle Anzeigen in einer Anzeigengruppe aufzulisten, klicken Sie auf den Namen der Anzeigengruppe und anschließend auf die Registerkarte [!UICONTROL Ads] .

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Bearbeiten der von Feeds generierten Daten](propagated-data-edit.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
>* [Status der von Feeds generierten Daten](propagated-data-status.md)
