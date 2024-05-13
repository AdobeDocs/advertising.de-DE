---
title: Aus Feeds generierte Daten anzeigen
description: Erfahren Sie, wie Sie Daten anzeigen können, die aus Bestandsdaten-Feeds generiert wurden.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Aus Feeds generierte Daten anzeigen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Wenn Sie Feed-Daten propagieren, ohne sie gleichzeitig in das Werbenetzwerk zu posten, können Sie die Daten auf eine der folgenden Arten in der Vorschau anzeigen. Später können Sie optional [Post-Daten](propagated-data-post.md) von beiden Standorten zu den relevanten Werbenetzwerken.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate and Preview],&quot;dann das generierte Bulksheet anzeigen (mit dem Namen`<feed file name>_<template name>`&quot;) aus dem [!UICONTROL Bulksheets] anzeigen. Es sind keine Daten im [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten. Mit dieser Option können Sie [Landingpages validieren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) mit den Anzeigen und Suchbegriffen verknüpft sind, bevor Sie die Daten veröffentlichen.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate only],&quot;dann die generierten Daten in einer Kampagnen-Hierarchieansicht in der Ansicht [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten.

  Die Ansichten der Kampagnenhierarchie zeigen nur die aus der Feed-Datei generierten Daten, nicht die vorhandenen Kontokomponenten. Nachdem die Daten für eine Komponente und alle zugehörigen Unterkomponenten in das Werbenetzwerk veröffentlicht wurden, werden sie nicht mehr in der Kampagnenhierarchie angezeigt.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

   1. (Optional) So zeigen Sie nur Kampagnenkomponenten an, die für eine bestimmte Vorlage erstellt wurden:

      1. Klicken Sie auf den Vorlagennamen.

      1. Im [!UICONTROL Accounts] im linken Navigationsbereich den Knoten des Anzeigennetzwerks und den Knoten des Anzeigennetzwerks erweitern und dann das Kontrollkästchen neben dem Vorlagennamen aktivieren.

   1. Klicken Sie auf **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** oder **[!UICONTROL Ads]** Registerkarte, abhängig davon, welche Komponenten Sie anzeigen möchten.

      >[!NOTE]
      >
      >* Wenn Sie keine Daten für eine bestimmte Vorlage anzeigen, wird die [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] in den Registerkarten werden alle Anzeigengruppen, Suchbegriffe und Anzeigen aufgelistet, die aus allen Vorlagen und Feed-Dateien erstellt wurden. Für [!DNL Google Ads] Shopping-Anzeigen finden Sie auf der [!UICONTROL Keywords] Registerkarte.
      >* Um nur die Unterkomponenten einer bestimmten Kampagne anzuzeigen, sehen Sie zunächst die [!UICONTROL Campaigns] Registerkarte. Um nur die Unterkomponenten einer bestimmten Anzeigengruppe anzuzeigen, beginnen Sie mit der Anzeige der [!UICONTROL Ad Groups] Registerkarte.

   1. (Optional) Um weitere Informationen anzuzeigen, führen Sie einen der folgenden Schritte aus:

      * Um die Einstellungen für Kampagnen, Anzeigengruppen, Keywords oder Anzeigen anzuzeigen, klicken Sie auf [Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;](/help/search-social-commerce/assets/settings.png "Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;") neben dem Namen.

      * Gehen Sie wie folgt vor, um die Unterkomponenten einer Kampagne oder Anzeigengruppe anzuzeigen:

         * Um alle Anzeigengruppen in einer Kampagne aufzulisten, klicken Sie auf den Kampagnennamen.

         * Um alle Suchbegriffe oder Produktziele in einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen.

         * Um alle Anzeigen in einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen und anschließend auf das [!UICONTROL Ads] Registerkarte.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
