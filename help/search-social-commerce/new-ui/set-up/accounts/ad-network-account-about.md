---
title: (Neue Benutzeroberfläche) Über Anzeigennetzwerkkonten
description: Erfahren Sie mehr über Anzeigennetzwerkkonten in der neuen Benutzeroberfläche für Suche, Social und Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Über Anzeigennetzwerkkonten

Search, Social und Commerce können jedes Konto eines Werbetreibenden in unterstützten Werbenetzwerken verfolgen. Um das Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz erstellen. Sie müssen Kontodetails für jede Art von Konto einrichten, unabhängig davon, ob Search, Social und Commerce mit ihr synchronisiert wird oder Angebote und Budgets für ihre Anzeigen optimiert.

## Über APIs synchronisierte Konten

*[!DNL Google Ads], [!DNL Microsoft Advertising] (früher [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten*

Search, Social und Commerce synchronisiert (*synchronisiert*) mit unterstützten Anzeigennetzwerkkonten, damit Sie die Leistung Ihrer Anzeigen verfolgen, Berichte dazu erstellen und visualisieren können. Für alle Werbenetzwerke außer [!DNL Yahoo! Display Network] können Sie optional die Kampagnen für Ihr Konto in Search, Social und Commerce; verwalten. [!DNL Yahoo! Display Network] sind Kampagnen schreibgeschützt. Für alle Werbenetzwerke können Sie die Optimierungsfunktion aktivieren, um Angebote, Kampagnenbudgets und Kampagnenangebotstrategie-Ziele für Kampagnen in verwalteten Konten zu optimieren, indem Sie die Kampagnen zu Portfolios hinzufügen.

Um die Synchronisierung eines Kontos zu aktivieren, muss der Kontodatensatz die Anmeldedaten für den Kontozugriff enthalten und aktiviert (aktiv) sein.

Während der Synchronisierung ruft Search, Social und Commerce die Kampagnenstrukturen und unterstützten Kampagnenentitäten des Advertisers ab, einschließlich der meisten ihrer Attribute, die in Search, Social und Commerce verwaltet oder gemeldet werden. Es enthält keine Klickdaten und auch keine Gebote und Gebotsmodifikatoren, die außerhalb von Search, Social und Commerce eingegeben und separat erfasst wurden. Search, Social und Commerce synchronisiert sich automatisch einmal täglich mit Ihren Anzeigennetzwerkkonten und auch immer dann, wenn eine neue Kampagne in einem Ihrer Anzeigennetzwerke erkannt wird. Darüber hinaus sendet es sofort alle Änderungen an Kampagnendaten, die innerhalb von Search, Social und Commerce vorgenommen wurden, an das Werbenetzwerk. Sie können bei Bedarf auch eine manuelle Synchronisierung anfordern.

Weitere Informationen zum Erstellen und Bearbeiten synchronisierter Kampagnen finden Sie im Kapitel „Kampagnenverwaltung“.

## Konten, für die Sie Daten manuell hochladen

Bei Online-Werbenetzwerken, für die Search, Social und Commerce keine API-Unterstützung bereitstellt, können Sie Kampagneninhalte und Offline-Kosten-, Klick- und Konversionsdaten für ein Konto für Berichte und Leistungssimulationen hochladen. Search, Social und Commerce synchronisieren keine Daten mit dem Werbenetzwerk, bieten keine automatisierten Gebote und keine Optimierungstypen, aber Sie können kanalübergreifende Einblicke optimieren und Möglichkeiten für die manuelle Optimierung identifizieren.

## Vorlagenbasierte Tracking-Konten

*Nur für bestehende [!DNL Naver]-Konten verfügbar*

Mit Tracking-Kampagnen können Sie die Leistung der Anzeigen, die Sie direkt im Anzeigennetzwerk kaufen, verfolgen, in Berichten anzeigen und visualisieren. Search, Social und Commerce synchronisieren keine Daten mit dem Werbenetzwerk, bieten keine automatisierten Gebote und bieten keine Optimierungs- oder Simulationstypen.

Damit Search, Social und Commerce Konversionen Klicks zuordnen können, richten Sie Tracking-Optionen im Kontodatensatz ein und aktivieren Sie den Kontodatensatz. Anschließend können Sie Bulksheets verwenden, um Tracking-URLs für Ihre Anzeigen und Keywords zu generieren, und die Tracking-URLs manuell in den [!DNL Naver] Ad Manager einfügen.

In Search, Social und Commerce können keine neuen [!DNL Naver] eingerichtet werden. Weitere Informationen zu [!DNL Naver] Kampagnen, die nur Tracking nutzen, finden Sie unter [Implementieren  [!DNL Naver]  Konten, die nur Tracking &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten über eine API-Verbindung](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Verwalten von Anzeigen-Netzwerkkonten für Daten-Uploads](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Verwalten [!DNL Naver] Konten nur für Tracking](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Nur [!DNL Naver] Tracking-Konten implementieren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Konten des Händlerzentrums verwalten](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
