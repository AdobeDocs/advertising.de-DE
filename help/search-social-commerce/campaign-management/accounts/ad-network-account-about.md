---
title: Über Werbenetzkonten
description: Erfahren Sie mehr über Ad-Netzwerk-Konten in Search, Social und Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Über Werbenetzkonten

*Nur für Adobe Account Manager,  Account Manager und Administrator-Benutzerrollen*

Search, Social und Commerce können beliebige Konten eines Advertisers in unterstützten Werbenetzwerken verfolgen. Um das Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz erstellen. Sie müssen Kontodetails für jeden Kontotyp einrichten, unabhängig davon, ob Search, Social und Commerce mit ihm synchronisiert oder Angebote und Budgets für dessen Anzeigen optimiert werden.

## Über APIs synchronisierte Konten

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads]und [!DNL Yandex] Konten*

Synchronisierungen für Suche, Social und Commerce (*syncs*) mit unterstützten Anzeigennetzwerkkonten, damit Sie die Leistung Ihrer Anzeigen verfolgen, in Berichten darstellen und visualisieren können. Alle Werbenetzwerke außer [!DNL Yahoo! Display Network]können Sie optional die Kampagnen für Ihr Konto in Search, Social und Commerce verwalten. [!DNL Yahoo! Display Network], sind Kampagnen schreibgeschützt. Für alle Werbenetzwerke können Sie mit der Optimierungsfunktion Gebote für Anzeigen in verwalteten Konten optimieren, indem Sie sie zu Portfolios hinzufügen.

Um die Synchronisierung eines Kontos zu aktivieren, muss der Kontodatensatz die Kontozugriffsberechtigungen enthalten und aktiviert (aktiv) sein.

Während der Synchronisierung ruft Search, Social und Commerce die Kampagnenstrukturen und unterstützten Kampagnenentitäten des Advertisers ab, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder in Berichten aufgeführt werden. Er enthält keine Klickdaten sowie Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben werden und separat gesammelt werden. Search, Social und Commerce synchronisiert automatisch mit Ihren Anzeigennetzwerkkonten einmal täglich und immer dann, wenn eine neue Kampagne in einem Ihrer Werbenetzwerke erkannt wird. Darüber hinaus werden sofort alle Änderungen an Kampagnendaten aus Search, Social und Commerce an das Werbenetzwerk gesendet. Sie können bei Bedarf optional eine manuelle Synchronisierung anfordern.

Weitere Informationen zum Erstellen und Bearbeiten synchronisierter Kampagnen finden Sie im Kapitel &quot;Campaign Management&quot;.

## Nur-Tracking-Konten

*[!DNL Naver]Konten*

Mit Tracking-Kampagnen können Sie die Leistung der Anzeigen, die Sie direkt über das Werbenetzwerk kaufen, verfolgen, in Berichten darstellen und visualisieren. Search, Social und Commerce synchronisiert keine Daten mit dem Werbenetzwerk, platzieren keine Angebote für das Konto und bieten keine Optimierungs- oder Simulationsmöglichkeiten.

Damit Search, Social und Commerce Konversionen Klicks zuordnen können, richten Sie Tracking-Optionen im Kontodatensatz ein und aktivieren Sie den Kontodatensatz. Sie können dann Bulksheets verwenden, um Tracking-URLs für Ihre Anzeigen und Suchbegriffe zu generieren, und die Tracking-URLs manuell innerhalb der [!DNL Naver] Anzeigenmanager.

Weitere Informationen finden Sie unter [!DNL Naver] reine Tracking-Kampagnen, siehe[Implementierung [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
>* [Verwalten von Merchant-Center-Konten](merchant-account-manage.md)
>* [Aktualisieren Sie den s\_kwcid-Trackingcode für eine [!DNL Google Ads] account](update-skwcid-google.md)
