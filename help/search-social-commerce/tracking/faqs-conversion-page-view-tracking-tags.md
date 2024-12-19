---
title: Häufig gestellte Fragen zu Adobe Advertising-Konvertierungs- und Seitenansichts-Tracking-Tags
description: Hier sehen Sie die Trackingtags für die Adobe Advertising-Konvertierung und die Seitenansicht im Vergleich .
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Adobe Advertising-Konvertierungs- und Seitenansichts-Tracking-Tags

Folgendes gilt für Adobe Advertising-Konversionsverfolgungstags und Seitenansichts-Verfolgungstags.

| | JS-Tags mit ECID | JS Version 3-Tags | JS Version 2-Tags | Bildtags |
| ---- | ---- | ---- | ---- | ---- |
| Kann auf derselben Webseite wie eine andere JS-Version verwendet werden | — | — | — | Nicht zutreffend |
| Ermöglicht die Verwendung mehrerer Tags mit denselben Advertiser-Benutzer-IDs auf derselben Webseite | Ja | Ja | Ja | — |
| Ermöglicht die Verwendung mehrerer Tags mit unterschiedlichen Advertiser-Benutzer-IDs auf derselben Web-Seite | Ja | Ja | — | — |
| Wird von der Adobe Advertising-Erweiterung für Adobe Experience Platform verwendet und ist mit anderen mit Experience Platform generierten Tags kompatibel | Ja | Ja | — | — |
| Ermöglicht das Tracking aller Konversionen, die von [!DNL Apple Safari] und [!DNL Mozilla Firefox] stammen, wenn sie mit dem Adobe Advertising JavaScript Conversion Mapping Tag verwendet werden | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alle neuen Implementierungen verwenden JavaScript Version 3.
>* Das JavaScript-Tag mit ECID verwendet zum Messen von Konversionen den [Adobe Experience Cloud ID (](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html))-Service sowie die veraltete ef_id und gsurferid. Dieses neueste Tag erstellt [Erstanbieter-Experience Cloud s_ecid-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) und bietet eine engere Integration mit anderen Experience Cloud-Produkten.
>* Verwenden Sie Tags der JavaScript-Version 2 nur, wenn sie bereits implementierte Tags auf den Web-Seiten des Werbetreibenden sind.
>* Es empfiehlt sich, JavaScript-Tags anstelle von Bild-Tags zu verwenden, es sei denn, die Website verfügt über eine Richtlinie gegen ihre Verwendung.
>* JavaScript-Tags sind für Werbetreibende erforderlich, die Zielgruppen ansprechen möchten, die in Adobe Experience Cloud erstellt, in Adobe Audience Manager erstellt oder von Audience Manager oder Adobe Analytics aus in Adobe Experience Cloud veröffentlicht wurden.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Erzeugen eines Adobe Advertising-Konvertierungs-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format von JavaScript-Konversionsverfolgungstags Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
