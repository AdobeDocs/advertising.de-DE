---
title: Konversions-Tracking für Ihre Webseiten einrichten
description: Erfahren Sie, wie Sie Adobe Advertising aktivieren, um Konversionen zu verfolgen, die aus Anzeigenimpressionen und -klicks resultieren.
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Konversions-Tracking für Ihre Webseiten einrichten

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

Bevor Sie Berichte zu Konversionsdaten, Daten zu Adobe Advertising-Anforderungen, Impressionen, Klicks, Kosten und Konversionsdaten (Transaktionen) für jeden Ihrer Suchbegriffe und Anzeigen erstellen können. Adobe Advertising verwendet diese Daten auch, um die Datenprognosemodelle zu erstellen, die zur Optimierung der Kampagnenbudgets und der Gebote für Suchbegriffe und Anzeigen erforderlich sind.

Damit Adobe Advertising Konversionen aus Anzeigenimpressionen und -klicks verfolgen kann, müssen Sie Folgendes tun:

* Fügen Sie in jeder Anzeigenkampagne, die von Search, Social und Commerce verwaltet wird, einen eindeutigen Klick-Trackingcode (und möglicherweise zusätzlichen Code zur Umleitung des Endbenutzers auf einen Tracking-Server) in die Tracking-Vorlage oder Ziel-URL ein. Dadurch kann Adobe Advertising jede Anzeigenimpression (nur für Display- und Social-) und jeden Klick auf eine Anzeige verfolgen.

* Verfolgen Sie Konversionsdaten auf eine der folgenden Arten:

   * **Adobe Advertising-verfolgte Konversionen:** Der Advertiser fügt auf jeder Konversionsseite ein Adobe Advertising-Konversions-Tracking-Tag ein.

   * **Adobe Analytics-Konversionen:** Der Advertiser verwendet das Adobe Analytics-Tracking für alle Konversionen.

   * **[!DNL Google Analytics]Konvertierungen:** Der Advertiser verwendet die [!DNL Google Analytics] -Tag, um alle Konversionen zu verfolgen.

   * **Vom Advertiser verfolgte Konversionen:** Der Advertiser stellt eine tägliche Feed-Datei mit einer beliebigen Kombination von Online- und Offline-Konversionsdaten bereit.

Ausführliche Informationen zur Implementierung von Tracking finden Sie im Hilfekapitel zum Thema &quot;Tracking&quot;.

>[!MORELIKETHIS]
>
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Generieren einer Klick-Tracking-URL für Search, Social und Commerce mithilfe des Tools Tracking-URLs](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [Dekodieren einer Klick-Tracking-URL für Suche, Social und Commerce](/help/search-social-commerce/tools/click-tracking-url-decode.md)

