---
title: Über Adobe Advertising von Konversions-Tracking-Tags
description: Erfahren Sie mehr über die Verwendung der Adobe Advertising-Konversions-Tracking-Tags.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Über Adobe Advertising von Konversions-Tracking-Tags

Adobe Advertising verfolgt Konversionen, die aus Klicks auf Anzeigen resultieren, mithilfe von Adobe Advertising-Konversions-Tracking-Tags, die in Webseiten eingefügt werden, die geöffnet werden, wenn ein Konversionsereignis auftritt, z. B. eine &quot;Erfolgsseite&quot;. Die Tags enthalten eingebettete Informationen zum Senden der Transaktionsdaten zusammen mit dem Adobe Advertising-Cookie des Benutzers an einen Tracking-Server, von dem aus die Transaktion dem entsprechenden Anzeigenklick oder der entsprechenden Impression gutgeschrieben wird (gemäß den Konversions-Attributionseinstellungen des Advertisers).

>[!NOTE]
>
>Wenn der Benutzer über kein gültiges Cookie verfügt, meldet Adobe Advertising die Konversion nicht.

Für jeden Satz von Konversionsmetriken, den Sie verfolgen möchten, müssen Sie ein separates Konversions-Tag erstellen. Geben Sie dem Werber oder der Agentur die Tags mit einer Liste von Webseiten an, auf denen jede Seite eingefügt werden soll. Sie können einen der folgenden Konversions-Tagtypen generieren. Anweisungen finden Sie unter &quot;[Generate an Adobe Advertising Conversion Tag](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot;.

* (Empfohlen) JavaScript-Tags (Version 3 oder Version 2), die nicht auf den Webseiten sichtbar sind.

* HTML von Bild-Tags zur Anzeige transparenter Bilder (Pixel) mit einer Auflösung von 1 Pixel x 1 Pixel, die für Endbenutzer unsichtbar sind. Verwenden Sie Bild-Tags nur, wenn das Unternehmen eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter &quot;[FAQs zu Advertising Cloud-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;.

>[!NOTE]
>
>* Mit dieser Funktion werden den Webseiten des Advertisers keine Bild-Tags oder JavaScript-Tags hinzugefügt. Die Tags müssen entsprechend der üblichen Vorgehensweise des Werbetreibenden zur Aktualisierung von Webseiten hinzugefügt werden.
>* Achten Sie darauf, wie lange die Implementierung der Tags dauert. Abhängig von den Richtlinien des Unternehmens kann die Implementierung Wochen oder sogar Monate dauern.

## Funktionen der Adobe Advertising-Konversions-Tracking-Tags

Das Konversions-Tracking-Pixel ermöglicht Adobe Advertising Folgendes:

* Verfolgen und melden Sie Konversionsdaten auf Suchbegriffebene für Suchkampagnen.

* Verfolgen und melden Sie Konversionsdaten auf Anzeigenebene (kreativ) über alle Marketing-Kanäle (Paid Search und Display) hinweg, was kreative Tests erleichtern kann.

* Verfolgen und melden Sie Konversionsdaten auf Transaktionsebene über alle Marketing-Kanäle hinweg.

* Zeigen Sie, wie Ihre Konversionen auf die verschiedenen Marketing-Kanäle verteilt sind, damit Sie sehen können, welche am effektivsten ist.

* Berichte und Optimierungen auf unterschiedlichen Attributionsebenen (z. B. Zuordnung von Konversionen zum letzten verwandten Ereignis oder ausgewogene Gewichtung aller Ereignisse).

* Bieten Sie Sichtbarkeit auf Klick-Assistenten (Suchbegriffe oder Platzierungen, die zu einem Konversionstrichter beigetragen haben) und Kanalassistenten (Benutzerereignisse, die zu einem Konversionstrichter beigetragen haben, möglicherweise über mehrere Marketing-Kanäle hinweg).

* Zeigen Sie die geografische Verteilung und die Referrer-Domänen Ihres Site-Traffics und Ihrer Konversionen an, damit Sie Ihr geografisches Ziel und das Website-Targeting verfeinern können.

* Analysieren Sie Wochentagstrends oder Intra-Tagestrends, die zur Verbesserung der Konversionsraten verwendet werden können.

>[!MORELIKETHIS]
>
>* [Konversions-Tracking-Optionen](conversion-tracking-about.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](format-conversion-tag-jsv3.md)
>* [Format der JavaScript-Konversions-Tracking-Tags, Version 2](format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
>* [FAQs über Konversions- und Seitenansichts-Tracking-Tags](faqs-conversion-page-view-tracking-tags.md)
>* [Das Adobe Advertising JavaScript-Konversions-Mapping-Tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
