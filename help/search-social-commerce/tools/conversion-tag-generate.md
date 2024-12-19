---
title: Erzeugen eines Adobe Advertising-Konversions-Tracking-Tags
description: Erfahren Sie, wie Sie ein Adobe Advertising-Konversions-Tag erstellen, um Ihre Konversionsereignisse zu verfolgen.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Erzeugen eines Adobe Advertising-Konversions-Tracking-Tags

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

Erstellen Sie für jeden Satz von Metriken, die Sie verfolgen möchten, ein separates Konversions-Tag und stellen Sie dem Advertiser oder der Agentur die Tags mit einer Liste von Web-Seiten zur Verfügung, auf denen sie jeweils eingefügt werden sollen.

>[!NOTE]
>
>Mit dieser Funktion werden den Web-Seiten des Werbetreibenden keine Bild-Tags oder [!DNL JavaScript]-Tags hinzugefügt. Die Tags müssen gemäß dem üblichen Verfahren des Advertisers zur Aktualisierung von Web-Seiten hinzugefügt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Geben Sie die [Konvertierungs-Tag-Einstellungen](#conversion-tag-settings) an.

1. Tag generieren:

   * Wenn die Website HTTP verwendet, klicken Sie auf **[!UICONTROL Generate Conversion Tag]**.

   * Wenn die Website auf einem sicheren Server (HTTPS) ausgeführt wird, klicken Sie auf **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopieren Sie das Tag aus dem Dialogfeld und fügen Sie es nach Bedarf auf den entsprechenden Web-Seiten ein.

>[!NOTE]
>
>Jede Metrik im neuen Konversions-Tag wird automatisch unter [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt, selbst wenn sie nicht implementiert ist oder die Web-Seiten, auf denen sie sich befindet, keine Klicks erhalten haben. Dieses Verhalten unterscheidet sich vom Verhalten von Metriken in Tags, die manuell oder an anderer Stelle erstellt wurden und die erst dann in [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt werden, wenn auf einer der Webseiten, auf denen sie sich befindet, ein Klick erfolgt ist. In allen Fällen ist jedoch jede Metrik zunächst von den Portfoliozielen, Berichten und Ansichten ausgeschlossen, bis Sie sie explizit verfügbar machen. Bevor Sie die Metriken zu Portfoliozielen hinzufügen, sollten Sie jedoch zunächst die Metriken verfügbar machen und sie zu Berichten hinzufügen, um zu überprüfen, wann sie Klicks erhalten.

## Adobe Advertising-Konvertierungs-Tag-Einstellungen {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Der Typ des zu erstellenden Tags:

* *[!UICONTROL Image]:* Erstellen eines Bild-Tags, um ein 1 Pixel x 1 Pixel großes transparentes Bild (Pixel) anzuzeigen, das für Endbenutzende unsichtbar ist, auf der Webseite. Als Best Practice wird empfohlen, Bild-Tags nur dann zu verwenden, wenn die Site eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

* *[!UICONTROL JavaScript]:* So erstellen Sie ein JavaScript-Tag.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter &quot;[FAQs about Adobe Advertising Conversion and Page View Tracking Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

**[!UICONTROL Tag Properties]:** Eine oder mehrere Konversionsmetriken, die verfolgt werden sollen, wenn ein Endbenutzer eine Seite mit dem Konversions-Tag aufruft. Um eine Metrik zur Liste hinzuzufügen, geben Sie den Namen der Metrik in das Feld &quot;[!UICONTROL Add new property]&quot; ein und klicken Sie auf **[!UICONTROL Add]**.

Wenn mehrere Metriken verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) im Tag verbunden, z. B. `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metriken, die dieser Liste hinzugefügt wurden, werden nirgendwo gespeichert oder in die [!UICONTROL Conversions] des Kunden auf der Registerkarte [!UICONTROL Admin] integriert. Metriken werden jedoch automatisch zur [!UICONTROL Conversions] des Kunden hinzugefügt, sobald Adobe Advertising Daten für eine Metrik erfasst. Dies geschieht, wenn das Konversions-Tag auf einer Seite implementiert wird und ein Endbenutzer eine Transaktion abschließt, die diese Seite öffnet.

**[!UICONTROL Include unique transaction IDs]:** (Optional) Enthält eine Transaktions-ID-Eigenschaft (`ev_transid=<transid>`) im -Tag. Die Option ist standardmäßig ausgewählt.

Wenn Sie diese Option auswählen, muss der Advertiser nach Abschluss der Transaktion einen eindeutigen Wert für die `<transid>` generieren (z. B. eine tatsächliche Bestell-ID) und ihn an den Adobe Advertising zurückgeben, z. B. `ev_transid=0123`. Adobe Advertising verwendet die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu eliminieren. Die Transaktions-ID darf keine kaufmännischen Und-Zeichen (`&`) enthalten, die als Parametertrennzeichen reserviert sind. Die Transaktions-ID ist in [der [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) enthalten, mit der Sie Daten in Search, Social und Commerce mit den Daten des Werbetreibenden validieren können.

Wenn die Daten keine eindeutige ID pro Transaktion enthalten, generiert Adobe Advertising weiterhin eine ID basierend auf der Transaktionszeit.

>[!NOTE]
>
>Wenn Sie [Transaktions-ID-Feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) mit Konversionsdaten für Offline-Konversionen senden, müssen Sie die Transaktions-ID (`ev_transid`) für den Online-Teil der Transaktion in den Feed-Daten für Offline-Teile der Transaktion übermitteln.

**[!UICONTROL Page is inside FB app]:** veraltet

**[!UICONTROL Segment users]:** veraltet

**[!UICONTROL JS Version]:** (nur [!DNL JavaScript] Tags) Welche Version des zu erstellenden [!DNL JavaScript]-Tags: *[!UICONTROL v2]* (Standard) oder *[!UICONTROL v3]*.

Siehe &quot;[Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).“ Weitere Informationen zu den Unterschieden finden Sie unter.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format von JavaScript-Konversionsverfolgungstags Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Das Adobe Advertising JavaScript Conversion Mapping Tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Über die Verwaltung der Konversionsmetriken eines Werbetreibenden](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
