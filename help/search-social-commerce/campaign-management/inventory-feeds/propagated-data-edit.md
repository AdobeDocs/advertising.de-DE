---
title: Aus Feeds generierte Daten bearbeiten
description: Erfahren Sie, wie Sie Daten bearbeiten, die aus Bestandsdaten-Feeds generiert wurden.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Aus Feeds generierte Daten bearbeiten

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Wenn Sie Feed-Daten propagieren, ohne sie gleichzeitig in das Werbenetzwerk zu posten, können Sie die Daten auf eine der folgenden Arten bearbeiten. Später können Sie optional [Daten ](propagated-data-post.md) von beiden Standorten an die relevanten Anzeigennetzwerke posten:

* Wenn Sie die Option für &quot;[!UICONTROL Propagate and Preview]&quot; verwendet haben, können Sie die generierte Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) bearbeiten, indem Sie sie aus der [!UICONTROL Bulksheets]-Ansicht herunterladen, die Datei bearbeiten und erneut hochladen. Auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] sind keine Daten enthalten.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate only]&quot; verwendet haben, können Sie die generierten Daten für Komponenten mit dem Status [[!UICONTROL New] status](propagated-data-status.md) in einer Kampagnen-Hierarchieansicht auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] bearbeiten.

  Die Ansichten der Kampagnenhierarchie zeigen nur die aus der Feed-Datei generierten Daten, nicht die vorhandenen Kontokomponenten. Nachdem die Daten für eine Komponente und alle zugehörigen Unterkomponenten in das Werbenetzwerk veröffentlicht wurden, werden sie nicht mehr in der Kampagnenhierarchie aufgeführt.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

   1. (Optional) So zeigen Sie nur Kampagnenkomponenten an, die für eine bestimmte Vorlage erstellt wurden:

      1. Klicken Sie auf den Vorlagennamen.

      1. Erweitern Sie im Menü [!UICONTROL Accounts] im linken Navigationsbereich den Knoten Werbenetzwerk und das Konto für das Anzeigen-Netzwerk und aktivieren Sie dann das Kontrollkästchen neben dem Vorlagennamen.

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** oder **[!UICONTROL Ads]**, je nachdem, welche Komponenten Sie anzeigen möchten.

      >[!NOTE]
      >
      >* Sofern Sie keine Daten für eine bestimmte Vorlage anzeigen, werden in den Registerkarten [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] alle Anzeigengruppen, Suchbegriffe und Anzeigen aufgelistet, die aus allen Vorlagen und Feed-Dateien erstellt wurden. Für [!DNL Google Ads] -Shopping-Anzeigen verwendete Produktgruppen werden auf der Registerkarte [!UICONTROL Keywords] aufgelistet.
      >* Um nur die Unterkomponenten einer bestimmten Kampagne anzuzeigen, rufen Sie zunächst den Tab [!UICONTROL Campaigns] auf. Um nur die Unterkomponenten einer bestimmten Anzeigengruppe anzuzeigen, beginnen Sie mit der Anzeige der Registerkarte [!UICONTROL Ad Groups] .

   1. (Optional; nur zur Bearbeitung von Anzeigengruppen, Suchbegriffen oder Anzeigen) Filtern Sie die Liste so, dass nur die Unterkomponenten einer bestimmten Kampagne oder Anzeigengruppe einbezogen werden:

      * Um alle Anzeigengruppen in einer Kampagne aufzulisten, klicken Sie auf den Kampagnennamen.

      * Um alle Suchbegriffe aus einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen.

      * Um alle als in einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen und dann auf die Registerkarte [!UICONTROL Ads] .

   1. Klicken Sie neben der Kampagne, Anzeigengruppe, dem Keyword oder dem Anzeigennamen auf [Einstellungssymbol anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;") .

   1. Bearbeiten Sie die Einstellungen und klicken Sie dann auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
