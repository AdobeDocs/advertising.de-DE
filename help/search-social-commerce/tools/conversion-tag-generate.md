---
title: Generieren eines Adobe Advertising-Konversions-Tracking-Tags
description: Erfahren Sie, wie Sie ein Adobe Advertising-Konversions-Tag erstellen, um Ihre Konversionsereignisse zu verfolgen.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Generieren eines Adobe Advertising-Konversions-Tracking-Tags

*Werbetreibende, die nur Adobe Advertising-Konversions-Tracking verwenden*

Erstellen Sie für jeden Metriksatz, den Sie verfolgen möchten, ein separates Konversions-Tag und stellen Sie dem Advertiser oder der Agentur die Tags mit einer Liste von Webseiten zur Verfügung, auf denen jede Seite eingefügt werden soll.

>[!NOTE]
>
>Diese Funktion fügt keine Bild-Tags hinzu oder [!DNL JavaScript] Tags auf den Webseiten des Advertisers hinzufügen. Die Tags müssen entsprechend der üblichen Vorgehensweise des Werbetreibenden zur Aktualisierung von Webseiten hinzugefügt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Geben Sie die [Konversions-Tag-Einstellungen](#conversion-tag-settings).

1. Generieren Sie das Tag:

   * Wenn die Website HTTP verwendet, klicken Sie auf **[!UICONTROL Generate Conversion Tag]**.

   * Wenn die Website auf einem sicheren Server (HTTPS) ausgeführt wird, klicken Sie auf **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopieren Sie das Tag aus dem Dialogfeld und fügen Sie es nach Bedarf in die entsprechenden Webseiten ein.

>[!NOTE]
>
>Jede Metrik im neuen Konversions-Tag wird automatisch in [!UICONTROL Admin] > [!UICONTROL Transaction Properties], auch wenn sie nicht implementiert wurde oder auf den Webseiten keine Klicks empfangen wurden. Dieses Verhalten unterscheidet sich vom Verhalten von Metriken in manuell oder an anderer Stelle erstellten Tags, die nicht in [!UICONTROL Admin] > [!UICONTROL Transaction Properties] bis eine der Webseiten, auf denen sie sich befindet, einen Klick erhalten hat. In allen Fällen wird jedoch jede Metrik zunächst aus Portfoliozielen, Berichten und Ansichten ausgeschlossen, bis Sie sie explizit verfügbar machen. Bevor Sie die Metriken zu Portfoliozielen hinzufügen, sollten Sie jedoch zuerst die Metriken verfügbar machen und sie zu Berichten hinzufügen, um zu überprüfen, wann sie Klicks erhalten.

## Adobe Advertising-Konversions-Tag-Einstellungen {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Der Typ des zu erstellenden Tags:

* *[!UICONTROL Image]:* So erstellen Sie ein Bild-Tag, um ein transparentes Bild (Pixel) von 1 Pixel x 1 Pixel anzuzeigen, das für Endbenutzer unsichtbar ist. Es empfiehlt sich, Bild-Tags nur zu verwenden, wenn die Site eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

* *[!UICONTROL JavaScript]:* So erstellen Sie ein JavaScript-Tag.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter[Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Eine oder mehrere Transaktionseigenschaften (Metriken), die verfolgt werden sollen, wenn ein Endbenutzer eine Seite anzeigt, die das Konversions-Tag enthält. Um der Liste eine Metrik hinzuzufügen, geben Sie den Metriknamen in die[!UICONTROL Add new property]&quot; und klicken Sie auf **[!UICONTROL Add]**.

Wenn mehrere Metriken verfolgt werden, werden sie durch ein Und-Zeichen (`&`) im -Tag, z. B. `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metriken, die dieser Liste hinzugefügt werden, werden nirgendwo gespeichert oder in die Liste des Kunden integriert [!UICONTROL Transaction Properties] Liste auf [!UICONTROL Admin] Registerkarte. Metriken werden jedoch zum [!UICONTROL Transaction Properties] automatisch auflistet, sobald der Adobe Advertising tatsächlich Daten für eine Metrik erfasst. Dies geschieht, wenn das Konversions-Tag auf einer Seite implementiert wird und ein Endbenutzer eine Transaktion abschließt, die diese Seite öffnet.

**[!UICONTROL Include unique transaction IDs]:** (Optional) Enthält eine Transaktions-ID-Eigenschaft (`ev_transid=<transid>`) im -Tag. Die Option ist standardmäßig ausgewählt.

Wenn Sie diese Option auswählen, muss der Advertiser einen eindeutigen Wert für `<transid>` (z. B. eine tatsächliche Bestell-ID), wenn die Transaktion abgeschlossen ist, und sie an den Adobe Advertising zurückgeben, z. B. `ev_transid=0123`. Adobe Advertising verwendet die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden. Die Transaktions-ID darf keine Zeichen und Zeichen enthalten (`&`), die als Parametertrennzeichen reserviert sind. Die Transaktions-ID ist in [die [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), mit dem Sie Daten in Search, Social und Commerce mit den Daten des Advertisers validieren können.

Wenn die Daten keine eindeutige ID pro Transaktion enthalten, erzeugt der Adobe Advertising immer noch eine auf der Transaktionszeit basierende ID.

>[!NOTE]
>
>Wenn Sie [Transaktions-ID-Feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) mit Konversionsdaten für Offline-Konversionen verwenden, müssen Sie die Transaktions-ID (`ev_transid`) für den Online-Teil der Transaktion in den Feed-Daten für Offline-Teile der Transaktion.

**[!UICONTROL Page is inside FB app]:** Obsolete

**[!UICONTROL Segment users]:** Obsolete

**[!UICONTROL JS Version]:** ([!DNL JavaScript] nur -Tags) Welche Version der [!DNL JavaScript] -Tag zu erstellen: *[!UICONTROL v2]* (Standardeinstellung) oder *[!UICONTROL v3]*.

Siehe &quot;[Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; für weitere Informationen zu den Unterschieden.

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Das Adobe Advertising-Tag für die JavaScript-Konversions-Zuordnung](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Über die Verwaltung der Transaktionseigenschaften eines Advertisers](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
