---
title: Über Anzeigennetzwerkkonten
description: Erfahren Sie mehr über Anzeigennetzwerkkonten in Search, Social und Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Über Anzeigennetzwerkkonten

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Administratorrollen*

Search, Social und Commerce können jedes Konto eines Werbetreibenden in unterstützten Werbenetzwerken verfolgen. Um das Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz erstellen. Sie müssen Kontodetails für jede Art von Konto einrichten, unabhängig davon, ob Search, Social und Commerce mit ihr synchronisiert wird oder Angebote und Budgets für ihre Anzeigen optimiert.

## Über APIs synchronisierte Konten

*[!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten*

Search, Social und Commerce synchronisiert (*synchronisiert*) mit unterstützten Anzeigennetzwerkkonten, damit Sie die Leistung Ihrer Anzeigen verfolgen, Berichte dazu erstellen und visualisieren können. Für alle Werbenetzwerke außer [!DNL Yahoo! Display Network] können Sie optional die Kampagnen für Ihr Konto in Search, Social und Commerce; verwalten. [!DNL Yahoo! Display Network] sind Kampagnen schreibgeschützt. Für alle Werbenetzwerke können Sie die Optimierungsfunktion aktivieren, um Angebote, Kampagnenbudgets und Kampagnenangebotstrategie-Ziele für Kampagnen in verwalteten Konten zu optimieren, indem Sie die Kampagnen zu Portfolios hinzufügen.

Um die Synchronisierung eines Kontos zu aktivieren, muss der Kontodatensatz die Anmeldedaten für den Kontozugriff enthalten und aktiviert (aktiv) sein.

Während der Synchronisierung ruft Search, Social und Commerce die Kampagnenstrukturen und unterstützten Kampagnenentitäten des Advertisers ab, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder gemeldet werden. Es enthält keine Klickdaten und auch keine Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben und separat erfasst wurden. Search, Social und Commerce synchronisiert sich automatisch einmal täglich mit Ihren Anzeigennetzwerkkonten und auch immer dann, wenn eine neue Kampagne in einem Ihrer Anzeigennetzwerke erkannt wird. Darüber hinaus sendet es sofort alle Änderungen an Kampagnendaten, die innerhalb von Search, Social und Commerce vorgenommen wurden, an das Werbenetzwerk. Sie können bei Bedarf auch eine manuelle Synchronisierung anfordern.

Weitere Informationen zum Erstellen und Bearbeiten synchronisierter Kampagnen finden Sie im Kapitel zu &quot;Campaign Management&quot;.

## Nur-Tracking-Konten

*[!DNL Naver]Konten*

Mit Tracking-Kampagnen können Sie die Leistung der Anzeigen, die Sie direkt im Anzeigennetzwerk kaufen, verfolgen, in Berichten anzeigen und visualisieren. Search, Social und Commerce synchronisieren keine Daten mit dem Anzeigennetzwerk, geben keine Gebote für das Konto ab und bieten keine Optimierungs- oder Simulationstypen an.

Damit Search, Social und Commerce Konversionen Klicks zuordnen können, richten Sie Tracking-Optionen im Kontodatensatz ein und aktivieren Sie den Kontodatensatz. Anschließend können Sie Bulksheets verwenden, um Tracking-URLs für Ihre Anzeigen und Keywords zu generieren, und die Tracking-URLs manuell in den [!DNL Naver] Ad Manager einfügen.

Weitere Informationen zu [!DNL Naver] Kampagnen, die nur Tracking nutzen, finden Sie unter [Implementieren  [!DNL Naver]  Konten, die nur Tracking ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigennetzwerkkonten](ad-network-account-manage.md)
>* [Konten des Händlerzentrums verwalten](merchant-account-manage.md)
>* [Aktualisieren des AMO-ID-Trackingcodes für ein  [!DNL Google Ads] -Konto](update-amo-id-google.md)
