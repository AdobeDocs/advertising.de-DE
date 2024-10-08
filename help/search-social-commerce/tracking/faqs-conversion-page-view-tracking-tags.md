---
title: Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags
description: Sehen Sie sich einen Vergleich der Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags an.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags

Folgendes gilt für Adobe Advertising-Konversions-Tracking-Tags und Seitenansichts-Tracking-Tags.

| | JS-Tags mit ECID | JS-Version 3-Tags | JS Version 2 Tags | Bild-Tags |
| ---- | ---- | ---- | ---- | ---- |
| Kann auf derselben Webseite wie auf einer anderen JS-Version verwendet werden | — | — | — | Nicht zutreffend |
| Ermöglicht die Verwendung mehrerer Tags mit denselben Advertiser-Benutzer-IDs auf derselben Webseite | Ja | Ja | Ja | — |
| Ermöglicht die Verwendung mehrerer Tags mit verschiedenen Advertiser-Benutzer-IDs auf derselben Webseite | Ja | Ja | — | — |
| Wird von der Adobe Advertising-Erweiterung für Adobe Experience Platform verwendet und ist mit anderen Tags kompatibel, die mithilfe von Experience Platform generiert werden. | Ja | Ja | — | — |
| Ermöglicht das Tracking aller Konversionen von [!DNL Apple Safari] und [!DNL Mozilla Firefox] bei Verwendung mit dem Adobe Advertising JavaScript-Konversions-Mapping-Tag | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alle neuen Implementierungen verwenden JavaScript Version 3.
>* Das JavaScript-Tag mit ECID verwendet den [Adobe Experience Cloud ID(ECID)-Dienst](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) sowie die Legacy-ef_id und gsurferid zum Messen von Konversionen. Dieses neueste Tag erstellt [Erstanbieter-Experience Cloud s_ecid-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) und bietet eine engere Integration mit anderen Experience Cloud-Produkten.
>* Verwenden Sie JavaScript Version 2-Tags nur, wenn sie bereits Tags auf den Webseiten des Advertisers implementiert haben.
>* Es empfiehlt sich, JavaScript-Tags anstelle von Bild-Tags zu verwenden, es sei denn, die Site verfügt über eine Richtlinie, die die Verwendung dieser Tags verhindert.
>* JavaScript-Tags sind für Advertiser erforderlich, die Zielgruppen auswählen möchten, die in Adobe Experience Cloud erstellt, in Adobe Audience Manager erstellt oder aus Audience Manager oder Adobe Analytics in Adobe Experience Cloud veröffentlicht wurden.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising von Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format der JavaScript-Konversions-Tracking-Tags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
