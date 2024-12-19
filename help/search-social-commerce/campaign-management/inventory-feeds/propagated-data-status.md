---
title: Status der von Feeds generierten Daten
description: Erfahren Sie mehr über den Status von Daten, die aus Inventardaten-Feeds generiert werden.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status der von Feeds generierten Daten

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Jede Komponente kann einen der folgenden Status aufweisen:

* *[!UICONTROL New]:* Die Komponente existiert nicht im Werbenetzwerk und wurde nicht im Werbenetzwerk veröffentlicht. Sie können die Einstellungen bei Bedarf dennoch bearbeiten, indem Sie auf den Komponentennamen klicken. Wenn Sie bereit sind, die Daten zu posten, klicken Sie auf **[!UICONTROL Post to SE]** und geben Sie die zu sendenden Daten an.

* *[!UICONTROL Posted]:* (Nur Kampagnen und Anzeigengruppen) Die Kampagne oder Anzeigengruppe wurde teilweise im Anzeigennetzwerk veröffentlicht, aber einige Komponenten wurden aufgrund von Fehlern nicht veröffentlicht. Der Validierungsstatus jedes Keywords und jeder Anzeige zeigt an, welche Informationen korrigiert werden müssen. Sie können die Einstellungen der Komponente bei Bedarf bearbeiten, indem Sie auf den Komponentennamen klicken.

* *[!UICONTROL Active]:* Die Komponente ist bereits im Anzeigennetzwerk aktiv und Sie können ihre Einstellungen hier nicht bearbeiten. Aktive Komponenten können [!UICONTROL New] Unterkomponenten enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

* *[!UICONTROL Paused]:* Die Komponente wurde bereits im Werbenetzwerk angehalten und die Einstellungen können hier nicht bearbeitet werden. Anhaltende Komponenten können [!UICONTROL New] Unterkomponenten enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

* *[!UICONTROL Deleted]:* Die Komponente wurde bereits im Werbenetzwerk gelöscht und Sie können ihre Einstellungen hier nicht bearbeiten. Gelöschte Komponenten können [!UICONTROL New] Unterkomponenten enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Anzeigen der von Feeds generierten Daten](propagated-data-view.md)
>* [Bearbeiten der von Feeds generierten Daten](propagated-data-edit.md)
>* [Post-Kampagnendaten, die von Feeds an Werbenetzwerke generiert werden](propagated-data-post.md)
>* [Buchungsauftrag für Inventar-Feed-Daten anhalten](stop-job.md)
