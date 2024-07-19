---
title: Über Werbenetzkonten
description: Erfahren Sie mehr über Anzeigennetzwerkkonten in Search, Social und Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Über Werbenetzkonten

*Nur für Agenturkontomanager, Adobe-Kontomanager und Administratorbenutzer*

Search, Social und Commerce können beliebige Konten eines Advertisers in unterstützten Werbenetzwerken verfolgen. Um das Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz erstellen. Sie müssen Kontodetails für jeden Kontotyp einrichten, unabhängig davon, ob Search, Social und Commerce damit synchronisiert oder Angebote und Budgets für seine Anzeigen optimiert.

## Über APIs synchronisierte Konten

*[!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten*

Die Suche, Social und Commerce synchronisiert (*synchronisiert*) mit unterstützten Anzeigennetzwerkkonten, sodass Sie die Leistung Ihrer Anzeigen verfolgen, in Berichten darstellen und visualisieren können. Bei allen Werbenetzwerken mit Ausnahme von [!DNL Yahoo! Display Network] können Sie optional die Kampagnen für Ihr Konto in Search, Social und Commerce verwalten. [!DNL Yahoo! Display Network] Kampagnen sind schreibgeschützt. Für alle Werbenetzwerke können Sie mit der Optimierungsfunktion Gebote für Anzeigen in verwalteten Konten optimieren, indem Sie sie zu Portfolios hinzufügen.

Um die Synchronisierung eines Kontos zu aktivieren, muss der Kontodatensatz die Kontozugriffsberechtigungen enthalten und aktiviert (aktiv) sein.

Während der Synchronisierung ruft Search, Social und Commerce die Kampagnenstrukturen und unterstützten Kampagnenentitäten des Advertisers ab, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder in Berichten aufgeführt werden. Er enthält keine Klickdaten sowie Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben werden und separat gesammelt werden. Search, Social und Commerce synchronisiert automatisch mit Ihren Anzeigennetzwerkkonten einmal täglich und immer dann, wenn eine neue Kampagne in einem Ihrer Werbenetzwerke erkannt wird. Darüber hinaus werden alle in Search, Social und Commerce vorgenommenen Änderungen an Kampagnendaten sofort an das Werbenetzwerk gesendet. Sie können bei Bedarf optional eine manuelle Synchronisierung anfordern.

Weitere Informationen zum Erstellen und Bearbeiten synchronisierter Kampagnen finden Sie im Kapitel &quot;Campaign Management&quot;.

## Nur-Tracking-Konten

*[!DNL Naver]Konten*

Mit Tracking-Kampagnen können Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, in Berichten darstellen und visualisieren. Search, Social und Commerce synchronisieren keine Daten mit dem Werbenetzwerk, platzieren keine Angebote für das Konto und bieten keine Optimierungs- oder Simulationsmöglichkeiten.

Damit Search, Social und Commerce Konversionen Klicks zuordnen können, richten Sie Tracking-Optionen im Kontodatensatz ein und aktivieren Sie den Kontodatensatz. Sie können dann Bulksheets verwenden, um Tracking-URLs für Ihre Anzeigen und Suchbegriffe zu generieren, und die Tracking-URLs manuell im Anzeigenmanager [!DNL Naver] hinzufügen.

Weitere Informationen zu [!DNL Naver] reine Tracking-Kampagnen finden Sie unter &quot;[Implementieren [!DNL Naver] reine Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
>* [Verwalten von Händlermittelkonten](merchant-account-manage.md)
>* [Aktualisieren des AMO-ID-Trackingcodes für ein [!DNL Google Ads] Konto](update-amo-id-google.md)
