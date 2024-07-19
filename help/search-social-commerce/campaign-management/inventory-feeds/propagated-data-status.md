---
title: Status der aus Feeds generierten Daten
description: Erfahren Sie mehr über die Status von Daten, die aus Bestandsdaten-Feeds generiert wurden.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Status der aus Feeds generierten Daten

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Jede Komponente kann einen der folgenden Status aufweisen:

* *[!UICONTROL New]:* Die Komponente ist nicht im Werbenetzwerk vorhanden und wurde nicht im Werbenetzwerk veröffentlicht. Sie können ihre Einstellungen dennoch bearbeiten, wenn nötig, indem Sie auf den Komponentennamen klicken. Wenn Sie bereit sind, die Daten zu posten, klicken Sie auf **[!UICONTROL Post to SE]** und geben Sie die zu sendenden Daten an.

* *[!UICONTROL Posted]:* (Nur Kampagnen und Anzeigengruppen) Die Kampagne oder Anzeigengruppe wurde teilweise im Werbenetzwerk veröffentlicht, einige Komponenten wurden jedoch aufgrund von Fehlern nicht veröffentlicht. Der Validierungsstatus jedes Suchbegriffs und jeder Anzeige zeigt an, welche Informationen korrigiert werden müssen. Sie können bei Bedarf die Einstellungen der Komponente bearbeiten, indem Sie auf den Komponentennamen klicken.

* *[!UICONTROL Active]:* Die Komponente ist bereits im Werbenetzwerk aktiv und Sie können ihre Einstellungen hier nicht bearbeiten. Aktive Komponenten können Unterkomponenten mit dem Wert &quot;[!UICONTROL New]&quot;enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

* *[!UICONTROL Paused]:* Die Komponente wurde bereits im Werbenetzwerk angehalten und Sie können ihre Einstellungen hier nicht bearbeiten. Ausgesetzte Komponenten können Unterkomponenten mit dem Wert [!UICONTROL New] enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

* *[!UICONTROL Deleted]:* Die Komponente wurde bereits im Werbenetzwerk gelöscht und Sie können ihre Einstellungen hier nicht bearbeiten. Gelöschte Komponenten können Unterkomponenten mit dem Wert &quot;[!UICONTROL New]&quot; enthalten, die veröffentlicht werden können, wenn die Daten gültig sind.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke](propagated-data-post.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
