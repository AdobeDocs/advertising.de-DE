---
title: Über das Adobe Advertising von Konversionsverfolgungstags
description: Erfahren Sie mehr über die Verwendung der Adobe Advertising-Konversionsverfolgungstags.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Über das Adobe Advertising von Konversionsverfolgungstags

Adobe Advertising verfolgt Konversionen, die aus Klicks auf Anzeigen resultieren, mithilfe von Adobe Advertising-Konversionsverfolgungstags, die in die Web-Seiten eingefügt werden, die geöffnet werden, wenn ein Konversionsereignis auftritt, z. B. eine „Erfolgsseite“. Die Tags enthalten eingebettete Informationen, um die Transaktionsdaten zusammen mit dem Adobe Advertising-Cookie des Benutzers an einen Tracking-Server zu senden, von dem aus die Transaktion dem entsprechenden Anzeigenklick oder der Impression gutgeschrieben wird (gemäß den Konversionszuordnungseinstellungen des Advertisers).

>[!NOTE]
>
>Wenn der Benutzer kein gültiges Cookie hat, meldet Adobe Advertising die Konversion nicht.

Für jeden Satz von Konversionsmetriken, den Sie verfolgen möchten, müssen Sie ein separates Konversions-Tag erstellen. Stellen Sie dem Werbetreibenden oder der Agentur die Tags mit einer Liste von Web-Seiten zur Verfügung, auf denen jeder Tag eingefügt werden soll. Sie können einen der folgenden Typen von Konversions-Tags generieren. Anweisungen finden [&#x200B; unter „Generieren eines Adobe Advertising-](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot;.

* (Empfohlen) JavaScript-Tags (Version 3 oder Version 2), die nicht auf den Web-Seiten sichtbar sind.

* HTML von Bild-Tags zur Anzeige von 1 Pixel x 1 Pixel großen transparenten Bildern (Pixeln), die für Endbenutzer unsichtbar sind, auf den Web-Seiten. Verwenden Sie Bild-Tags nur, wenn das Unternehmen eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter [Häufig gestellte Fragen zu Advertising Cloud-Konversionsverfolgungstags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

>[!NOTE]
>
>* Mit dieser Funktion werden den Web-Seiten des Werbetreibenden keine Bild-Tags oder JavaScript-Tags hinzugefügt. Die Tags müssen gemäß dem üblichen Verfahren des Advertisers zur Aktualisierung von Web-Seiten hinzugefügt werden.
>* Stellen Sie sicher, dass Sie überlegen, wie lange es dauert, die Tags zu implementieren. Abhängig von den Richtlinien des Unternehmens kann die Implementierung Wochen oder sogar Monate dauern.

## Funktionen der Adobe Advertising-Konversionsverfolgungstags

Mit dem Konversionsverfolgungspixel kann Adobe Advertising Folgendes tun:

* Konversionsdaten für Suchkampagnen auf Keyword-Ebene verfolgen und melden.

* Konversionsdaten auf Anzeigenebene (kreativ) über alle Marketing-Kanäle (Paid Search und Display) verfolgen und melden, was kreative Tests erleichtern kann.

* Konversionsdaten auf Transaktionsebene über alle Marketing-Kanäle verfolgen und melden.

* Zeigen Sie, wie Ihre Konversionen auf Ihre verschiedenen Marketing-Kanäle verteilt sind, damit Sie sehen können, welche am effektivsten ist.

* Berichte und Optimierungen für verschiedene Attributionsebenen erstellen (z. B. Zuweisung von Konversionen zum letzten zugehörigen Ereignis oder gleichmäßige Gewichtung aller Ereignisse).

* Sichtbarkeit bei Klickassistenten (Suchbegriffe oder Platzierungen, die zu einem Konversionstrichter beigetragen haben) und Kanalassistenten (Benutzerereignisse, die zu einem Konversionstrichter beigetragen haben, möglicherweise über mehrere Marketing-Kanäle hinweg) bieten.

* Bieten Sie Einblicke in die geografische Verteilung und die verweisenden Domains Ihres Website-Traffics und der Konversionen, damit Sie Ihr geografisches und Website-Targeting verfeinern können.

* Analysieren Sie Wochentags- oder Intraday-Trends, die zur Verbesserung der Konversionsraten verwendet werden können.

>[!MORELIKETHIS]
>
>* [Konversionsverfolgungs-Optionen](conversion-tracking-about.md)
>* [Erzeugen eines Adobe Advertising-Konvertierungs-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format von JavaScript-Konversionsverfolgungstags Version 3](format-conversion-tag-jsv3.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](faqs-conversion-page-view-tracking-tags.md)
>* [Das Adobe Advertising JavaScript Conversion Mapping Tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
