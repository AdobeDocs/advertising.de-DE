---
title: Adobe Advertising-Konversions-Tracking-Tag generieren
description: Erfahren Sie, wie Sie ein Adobe Advertising-Konversions-Tag erstellen, um Ihre Konversionsereignisse zu verfolgen.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Adobe Advertising-Konversions-Tracking-Tag generieren

*Advertiser mit nur Adobe Advertising-Konversions-Tracking*

Erstellen Sie für jeden Metriksatz, den Sie verfolgen möchten, ein separates Konversions-Tag und stellen Sie dem Advertiser oder der Agentur die Tags mit einer Liste von Webseiten zur Verfügung, auf denen jede Seite eingefügt werden soll.

>[!NOTE]
>
>Mit dieser Funktion werden den Webseiten des Advertisers keine Bild-Tags oder [!DNL JavaScript] -Tags hinzugefügt. Die Tags müssen entsprechend der üblichen Vorgehensweise des Werbetreibenden zur Aktualisierung von Webseiten hinzugefügt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Geben Sie die [Konversions-Tag-Einstellungen](#conversion-tag-settings) an.

1. Generieren Sie das Tag:

   * Wenn die Website HTTP verwendet, klicken Sie auf **[!UICONTROL Generate Conversion Tag]**.

   * Wenn die Website auf einem sicheren Server (HTTPS) ausgeführt wird, klicken Sie auf **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopieren Sie das Tag aus dem Dialogfeld und fügen Sie es nach Bedarf in die entsprechenden Webseiten ein.

>[!NOTE]
>
>Jede Metrik im neuen Konversions-Tag wird automatisch unter [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt, auch wenn sie nicht implementiert ist oder auf den Webseiten keine Klicks empfangen wurden. Dieses Verhalten unterscheidet sich vom Verhalten von Metriken in manuell oder an anderer Stelle erstellten Tags, die nicht unter [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt sind, bis eine der Webseiten, auf denen sie sich befindet, einen Klick erhalten hat. In allen Fällen wird jedoch jede Metrik zunächst aus Portfoliozielen, Berichten und Ansichten ausgeschlossen, bis Sie sie explizit verfügbar machen. Bevor Sie die Metriken zu Portfoliozielen hinzufügen, sollten Sie jedoch zuerst die Metriken verfügbar machen und sie zu Berichten hinzufügen, um zu überprüfen, wann sie Klicks erhalten.

## Adobe Advertising-Konversions-Tag-Einstellungen {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Der Typ des zu erstellenden Tags:

* *[!UICONTROL Image]:* Erstellen eines Bild-Tags zur Anzeige eines transparenten 1 Pixel x 1 Pixel großen Bildes (Pixel), das für Endbenutzer unsichtbar ist. Es empfiehlt sich, Bild-Tags nur zu verwenden, wenn die Site eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

* *[!UICONTROL JavaScript]:* So erstellen Sie ein JavaScript-Tag.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter &quot;[FAQs über Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;.

**[!UICONTROL Tag Properties]:** Eine oder mehrere Konversionsmetriken, die verfolgt werden sollen, wenn ein Endbenutzer eine Seite anzeigt, die das Konversions-Tag enthält. Um der Liste eine Metrik hinzuzufügen, geben Sie den Metriknamen in das Feld &quot;[!UICONTROL Add new property]&quot; ein und klicken Sie auf **[!UICONTROL Add]**.

Wenn mehrere Metriken verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) im Tag verbunden, z. B. `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metriken, die dieser Liste hinzugefügt werden, werden nirgendwo gespeichert oder in die Liste [!UICONTROL Conversions] des Kunden auf der Registerkarte [!UICONTROL Admin] integriert. Metriken werden jedoch automatisch zur [!UICONTROL Conversions] -Liste des Kunden hinzugefügt, sobald Adobe Advertising tatsächlich Daten für eine Metrik erfasst. Dies geschieht, wenn das Konversions-Tag auf einer Seite implementiert wird und ein Endbenutzer eine Transaktion abschließt, die diese Seite öffnet.

**[!UICONTROL Include unique transaction IDs]:** (Optional) Beinhaltet eine Transaktions-ID-Eigenschaft (`ev_transid=<transid>`) im Tag. Die Option ist standardmäßig ausgewählt.

Wenn Sie diese Option auswählen, muss der Werbetreibende einen eindeutigen Wert für `<transid>` (z. B. eine tatsächliche Bestell-ID) generieren, wenn die Transaktion abgeschlossen ist, und ihn an Adobe Advertising weiterleiten, z. B. `ev_transid=0123`. Adobe Advertising verwendet die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden. Die Transaktions-ID darf keine Zeichen und Zeichen (`&`) enthalten, die als Parametertrennzeichen reserviert sind. Die Transaktions-ID ist in [dem [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) enthalten, mit dem Sie Daten in Search, Social und Commerce mit den Daten des Advertisers validieren können.

Wenn die Daten keine eindeutige ID pro Transaktion enthalten, erzeugt Adobe Advertising immer noch eine auf der Transaktionszeit basierende ID.

>[!NOTE]
>
>Wenn Sie [Transaktions-ID-Feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) mit Konversionsdaten für Offline-Konversionen senden, müssen Sie die Transaktions-ID (`ev_transid`) für den Online-Teil der Transaktion in den Feed-Daten für Offline-Teile der Transaktion übermitteln.

**[!UICONTROL Page is inside FB app]:** veraltet

**[!UICONTROL Segment users]:** veraltet

**[!UICONTROL JS Version]:** ([!DNL JavaScript] nur Tags) Welche Version des zu erstellenden [!DNL JavaScript]-Tags ist: *[!UICONTROL v2]* (Standard) oder *[!UICONTROL v3]*.

Siehe &quot;[FAQs zum Adobe Advertising von Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)&quot;. für weitere Informationen zu den Unterschieden.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising von Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [FAQs über Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format der JavaScript-Konversions-Tracking-Tags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Das Adobe Advertising JavaScript-Konversions-Mapping-Tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
