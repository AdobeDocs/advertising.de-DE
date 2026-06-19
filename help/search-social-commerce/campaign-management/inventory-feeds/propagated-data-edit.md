---
title: Bearbeiten der von Feeds generierten Daten
description: Erfahren Sie, wie Sie Daten bearbeiten, die aus Inventardaten-Feeds generiert wurden.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/YAjOramjWXPJmOkLB2dhjG3PLUUAEbDAPRBYLVSl3vo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 426
ht-degree: 0%

---

# Bearbeiten der von Feeds generierten Daten

*[!DNL Google Ads], [!DNL LY Ads] (nur Löschaktionen), [!DNL Microsoft Advertising] und [!DNL Yandex] Konten*

Wenn Sie Feed-Daten übertragen, ohne sie gleichzeitig im Anzeigennetzwerk zu posten, können Sie die Daten auf eine der folgenden Arten bearbeiten. Später können Sie optional [Daten](propagated-data-post.md) von beiden Standorten an die entsprechenden Werbenetzwerke senden:

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate and Preview]&quot; verwendet haben, können Sie die generierte Bulksheet-Datei (mit dem Namen &quot;`<feed file name>_<template name>`„) bearbeiten, indem Sie sie aus der [!UICONTROL Bulksheets]-Ansicht herunterladen, die Datei bearbeiten und erneut hochladen. Auf den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] sind keine Daten enthalten.

* Wenn Sie die Option auf &quot;[!UICONTROL Propagate only]&quot; verwendet haben, können Sie die generierten Daten für Komponenten mit dem [[!UICONTROL New] Status &#x200B;](propagated-data-status.md) einer Kampagnenhierarchieansicht von den Registerkarten [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] aus bearbeiten.

  Die Kampagnenhierarchieansichten zeigen nur die aus der Feed-Datei generierten Daten an, nicht die vorhandenen Kontokomponenten. Nachdem Daten für eine Komponente und alle zugehörigen Unterkomponenten an das Werbenetzwerk gesendet wurden, werden sie nicht mehr in der Kampagnenhierarchie aufgeführt.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

   1. (Optional) So zeigen Sie nur Kampagnenkomponenten an, die für eine bestimmte Vorlage erstellt wurden:

      1. Klicken Sie auf den Namen der Vorlage.

      1. Erweitern Sie im Menü [!UICONTROL Accounts] im linken Navigationsbereich den Knoten „Anzeigennetzwerk“ und den Knoten „Anzeigennetzwerkkonto“ und aktivieren Sie dann das Kontrollkästchen neben dem Vorlagennamen.

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** oder **[!UICONTROL Ads]**, je nachdem, welche Komponenten Sie anzeigen möchten.

      >[!NOTE]
      >
      >* Sofern Sie keine Daten für eine bestimmte Vorlage anzeigen, werden auf den Registerkarten [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] alle Anzeigengruppen, Keywords und Anzeigen aufgelistet, die aus allen Vorlagen und Feed-Dateien erstellt wurden. Für [!DNL Google Ads] Shopping-Anzeigen verwendete Produktgruppen werden auf der Registerkarte [!UICONTROL Keywords] aufgeführt.
      >* Um nur die Unterkomponenten einer bestimmten Kampagne anzuzeigen, öffnen Sie zunächst die Registerkarte [!UICONTROL Campaigns] . Um nur die Unterkomponenten einer bestimmten Anzeigengruppe anzuzeigen, zeigen Sie zunächst die Registerkarte [!UICONTROL Ad Groups] an.

   1. (Optional, um Anzeigengruppen, Keywords oder Anzeigen zu bearbeiten) Filtern Sie die Liste so, dass nur die Unterkomponenten einer bestimmten Kampagne oder Anzeigengruppe enthalten sind:

      * Um alle Anzeigengruppen in einer Kampagne aufzulisten, klicken Sie auf den Namen der Kampagne.

      * Um alle Schlüsselwörter in einer Anzeigengruppe aufzulisten, klicken Sie auf den Namen der Anzeigengruppe.

      * Um alle Anzeigengruppen in einer Anzeigengruppe aufzulisten, klicken Sie auf den Namen der Anzeigengruppe und anschließend auf die Registerkarte [!UICONTROL Ads] .

   1. Klicken Sie [&#x200B; Symbol „Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Symbol „Einstellungen anzeigen/bearbeiten“") neben der Kampagne, der Anzeigengruppe, dem Keyword oder dem Anzeigenamen.

   1. Bearbeiten Sie die Einstellungen und klicken Sie dann auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Anzeigen der von Feeds generierten Daten](propagated-data-view.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
>* [Status der von Feeds generierten Daten](propagated-data-status.md)
