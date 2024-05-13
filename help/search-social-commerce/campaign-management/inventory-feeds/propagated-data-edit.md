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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Wenn Sie Feed-Daten propagieren, ohne sie gleichzeitig in das Werbenetzwerk zu posten, können Sie die Daten auf eine der folgenden Arten bearbeiten. Später können Sie optional [Post-Daten](propagated-data-post.md) von beiden Standorten zu den relevanten Werbenetzwerken:

* Wenn Sie die Option für &quot;[!UICONTROL Propagate and Preview],&quot;können Sie die generierte Bulksheet-Datei bearbeiten (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) durch Herunterladen aus dem [!UICONTROL Bulksheets] die Datei anzeigen, bearbeiten und erneut hochladen. Es sind keine Daten im [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate only],&quot;können Sie die generierten Daten für Komponenten mit der [[!UICONTROL New] status](propagated-data-status.md) innerhalb einer Kampagnenhierarchie aus der [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Registerkarten.

  Die Ansichten der Kampagnenhierarchie zeigen nur die aus der Feed-Datei generierten Daten, nicht die vorhandenen Kontokomponenten. Nachdem die Daten für eine Komponente und alle zugehörigen Unterkomponenten in das Werbenetzwerk veröffentlicht wurden, werden sie nicht mehr in der Kampagnenhierarchie aufgeführt.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

   1. (Optional) So zeigen Sie nur Kampagnenkomponenten an, die für eine bestimmte Vorlage erstellt wurden:

      1. Klicken Sie auf den Vorlagennamen.

      1. Im [!UICONTROL Accounts] im linken Navigationsbereich den Knoten des Anzeigennetzwerks und den Knoten des Anzeigennetzwerks erweitern und dann das Kontrollkästchen neben dem Vorlagennamen aktivieren.

   1. Klicken Sie auf **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** oder **[!UICONTROL Ads]** Registerkarte, abhängig davon, welche Komponenten Sie anzeigen möchten.

      >[!NOTE]
      >
      >* Wenn Sie keine Daten für eine bestimmte Vorlage anzeigen, wird die [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] in den Registerkarten werden alle Anzeigengruppen, Suchbegriffe und Anzeigen aufgelistet, die aus allen Vorlagen und Feed-Dateien erstellt wurden. Für [!DNL Google Ads] Shopping-Anzeigen finden Sie auf der [!UICONTROL Keywords] Registerkarte.
      >* Um nur die Unterkomponenten einer bestimmten Kampagne anzuzeigen, sehen Sie zunächst die [!UICONTROL Campaigns] Registerkarte. Um nur die Unterkomponenten einer bestimmten Anzeigengruppe anzuzeigen, beginnen Sie mit der Anzeige der [!UICONTROL Ad Groups] Registerkarte.

   1. (Optional; nur zur Bearbeitung von Anzeigengruppen, Suchbegriffen oder Anzeigen) Filtern Sie die Liste so, dass nur die Unterkomponenten einer bestimmten Kampagne oder Anzeigengruppe einbezogen werden:

      * Um alle Anzeigengruppen in einer Kampagne aufzulisten, klicken Sie auf den Kampagnennamen.

      * Um alle Suchbegriffe aus einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen.

      * Um alle als in einer Anzeigengruppe aufzulisten, klicken Sie auf den Anzeigengruppennamen und anschließend auf die [!UICONTROL Ads] Registerkarte.

   1. Klicks [Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;](/help/search-social-commerce/assets/settings.png "Symbol &quot;Einstellungen anzeigen/bearbeiten&quot;") neben der Kampagne, Anzeigengruppe, dem Keyword oder dem Anzeigennamen.

   1. Bearbeiten Sie die Einstellungen und klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
