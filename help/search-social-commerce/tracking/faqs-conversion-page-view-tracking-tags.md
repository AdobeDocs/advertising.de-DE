---
title: Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags
description: Sehen Sie sich einen Vergleich der Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags an.
exl-id: 5eb414a7-2f96-47de-b157-a17851653206
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags

Folgendes gilt für Adobe Advertising-Konversions-Tracking-Tags und Seitenansichts-Tracking-Tags.

| | JS-Tags mit ECID | JS-Version 3-Tags | JS Version 2 Tags | Bild-Tags |
| ---- | ---- | ---- | ---- | ---- |
| Kann auf derselben Webseite wie auf einer anderen JS-Version verwendet werden | — | — | — | Nicht zutreffend |
| Ermöglicht die Verwendung mehrerer Tags mit denselben Advertiser-Benutzer-IDs auf derselben Webseite | Ja | Ja | Ja | — |
| Ermöglicht die Verwendung mehrerer Tags mit verschiedenen Advertiser-Benutzer-IDs auf derselben Webseite | Ja | Ja | Nein | Nein |
| Wird von der Adobe Advertising-Erweiterung für Adobe Experience Platform verwendet und ist mit anderen Tags kompatibel, die mithilfe von Experience Platform generiert wurden. | Ja | Ja | — | — |
| Ermöglicht alle Konversionen, die von [!DNL Apple Safari] und [!DNL Mozilla Firefox] zur Verfolgung bei Verwendung mit dem Adobe Advertising-JavaScript-Konversions-Mapping-Tag | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alle neuen Implementierungen verwenden JavaScript Version 3.
>* Das JavaScript-Tag mit ECID verwendet die [Adobe Experience Cloud ID-Dienst (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) sowie die Legacy ef_id und gsurferid zum Messen von Konversionen. Dieses neueste Tag erstellt [s_ecid-Cookies von Erstanbietercookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) und bietet eine engere Integration mit anderen Experience Cloud-Produkten.
>* Verwenden Sie JavaScript Version 2-Tags nur, wenn sie bereits Tags auf den Webseiten des Advertisers implementiert haben.
>* Es empfiehlt sich, JavaScript-Tags anstelle von Bild-Tags zu verwenden, es sei denn, die Site verfügt über eine Richtlinie, die die Verwendung dieser Tags verhindert.
>* JavaScript-Tags sind für Advertiser erforderlich, die Zielgruppen auswählen möchten, die in Adobe Experience Cloud erstellt, in Adobe Audience Manager erstellt oder aus Audience Manager oder Adobe Analytics in Adobe Experience Cloud veröffentlicht wurden.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
