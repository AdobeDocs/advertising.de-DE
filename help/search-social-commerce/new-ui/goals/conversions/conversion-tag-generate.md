---
title: (Neue Benutzeroberfläche) Generieren und Implementieren eines Adobe Advertising-Konversionsverfolgungs-Tags
description: Erfahren Sie, wie Sie ein Adobe Advertising-Konversions-Tag erstellen, um Ihre Konversionsereignisse zu verfolgen.
feature: Search Tools, Search Tracking
source-git-commit: f97a636a55c6cc823f0041e7acd6f48dca769a3e
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Generieren und Implementieren eines Adobe Advertising-Konversionsverfolgungs-Tags

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

Erstellen Sie für jeden Satz von Metriken, den Sie verfolgen möchten, ein separates Konversions-Tag . Sie können Tags in Search, Social und Commerce oder mithilfe von Tags in Adobe Experience Platform (ehemals Adobe Experience Platform Launch) mit der Adobe Advertising-Erweiterung generieren.

## Generieren und Implementieren eines Conversion-Tracking-Tags in Search, Social und Commerce

>[!NOTE]
>
>Mit dieser Funktion werden den Web-Seiten des Werbetreibenden keine Bild-Tags oder [!DNL JavaScript]-Tags hinzugefügt. Stellen Sie dem Werbetreibenden oder der Agentur die Tags mit einer Liste von Web-Seiten zur Verfügung, auf denen jeder Tag eingefügt werden soll. Die Tags müssen gemäß dem üblichen Verfahren des Advertisers zur Aktualisierung von Web-Seiten hinzugefügt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Klicken Sie in der Hauptsymbolleiste auf **[!UICONTROL Conversion Tag]**.

1. Geben Sie die [Konvertierungs-Tag-Einstellungen](#conversion-tag-settings) an.

1. Klicken Sie auf **[!UICONTROL Generate]**.

1. Klicken Sie auf **[!UICONTROL Copy]** , um das Tag in die Zwischenablage zu kopieren. Geben Sie dem Advertiser oder der Agentur das Tag zur Implementierung.

>[!NOTE]
>
>Jede Metrik im neuen Konversions-Tag wird automatisch unter [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt, selbst wenn sie nicht implementiert ist oder die zugehörigen Web-Seiten keine Klicks erhalten haben. Dieses Verhalten unterscheidet sich vom Verhalten von Metriken in Tags, die manuell oder an anderer Stelle erstellt wurden und die erst dann in [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt werden, wenn auf einer der Webseiten, auf denen sie sich befindet, ein Klick erfolgt ist. In allen Fällen ist jedoch jede Metrik zunächst von den Portfoliozielen, Berichten und Ansichten ausgeschlossen, bis Sie sie explizit verfügbar machen. Bevor Sie die Metriken zu Portfoliozielen hinzufügen, sollten Sie zunächst die Metriken verfügbar machen und sie zu Berichten hinzufügen, um zu überprüfen, wann sie Klicks erhalten.

### Einstellungen für Adobe Advertising-Konversions-Tags {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Der Typ des zu erstellenden Tags:

* *[!UICONTROL JavaScript]:* So erstellen Sie ein JavaScript-Tag.

* *[!UICONTROL Image]:* Erstellen eines Bild-Tags, um ein 1 Pixel x 1 Pixel großes transparentes Bild (Pixel) anzuzeigen, das für Endbenutzende unsichtbar ist, auf der Webseite. Als Best Practice wird empfohlen, Bild-Tags nur dann zu verwenden, wenn die Site eine Richtlinie gegen die Verwendung von JavaScript-Tags hat.

Weitere Informationen zu den Unterschieden zwischen den Tag-Typen finden Sie unter [Häufig gestellte Fragen zu Adobe Advertising-Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

**[!UICONTROL Include unique transaction IDs]:** (Optional) Enthält eine Transaktions-ID-Eigenschaft (`ev_transid=<transid>`) im -Tag. Die Option ist standardmäßig ausgewählt.

Wenn Sie diese Option auswählen, muss der Advertiser nach Abschluss der Transaktion einen eindeutigen Wert für die `<transid>` generieren (z. B. eine tatsächliche Auftrags-ID) und ihn an Adobe Advertising zurückgeben, z. B. `ev_transid=0123`. Adobe Advertising verwendet die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu eliminieren. Die Transaktions-ID darf keine kaufmännischen Und-Zeichen (`&`) enthalten, die als Parametertrennzeichen reserviert sind. Die Transaktions-ID ist in [der [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) enthalten, mit der Sie Daten in Search, Social und Commerce mit den Daten des Werbetreibenden validieren können.

Wenn die Daten keine eindeutige ID pro Transaktion enthalten, generiert Adobe Advertising weiterhin eine auf der Grundlage der Transaktionszeit.

>[!NOTE]
>
>Wenn Sie [Transaktions-ID-Feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) mit Konversionsdaten für Offline-Konversionen senden, müssen Sie die Transaktions-ID (`ev_transid`) für den Online-Teil der Transaktion in den Feed-Daten für Offline-Teile der Transaktion übermitteln.

**[!UICONTROL JS Version]:** (nur [!DNL JavaScript] Tags) Welche Version des zu erstellenden [!DNL JavaScript]-Tags: *[!UICONTROL v2]* (Standard) oder *[!UICONTROL v3]*.

**[!UICONTROL Security]:** Das Sicherheitsprotokoll für Ihre Website erstellen: *[!UICONTROL Standard]* (für Websites, die HTTP verwenden) oder *[!UICONTROL Secure]* (für Websites, die HTTP verwenden).

**[!UICONTROL Properties]:** Eine oder mehrere Konversionsmetriken, die verfolgt werden sollen, wenn ein Endbenutzer eine Seite mit dem Konversions-Tag aufruft. Um eine Metrik zur Liste hinzuzufügen, geben Sie den Namen der Metrik in das Feld &quot;[!UICONTROL Property name]&quot; ein und klicken Sie auf **[!UICONTROL Add]**.

Wenn mehrere Metriken verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) im Tag verbunden, z. B. `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metriken, die dieser Liste hinzugefügt wurden, werden nirgendwo gespeichert oder in die [!UICONTROL Conversions] des Kunden auf der Registerkarte [!UICONTROL Admin] integriert. Metriken werden jedoch automatisch zur [!UICONTROL Conversions] des Kunden hinzugefügt, sobald Adobe Advertising Daten für eine Metrik erfasst. Dies geschieht, wenn das Konversions-Tag auf einer Seite implementiert wird und ein Endbenutzer eine Transaktion abschließt, durch die diese Seite geöffnet wird.

## Implementieren von Konversionsverfolgungstags mit Adobe Experience Platform-Tags und der Adobe Advertising-Erweiterung

Sie können das Konversions-Tracking für Search, Social und Commerce mithilfe von Tags in Adobe Experience Platform einrichten. Tags stehen Adobe CX Enterprise-Kunden als integrierte Mehrwertfunktion zur Verfügung.

Die folgenden Aufgaben sind erforderlich, um Konversionsverfolgungstags für Suche, Social und Commerce über die Experience Platform-Benutzeroberfläche oder die Experience Platform-Datenerfassungs-Benutzeroberfläche zu konfigurieren. Vollständige Informationen und Anweisungen zum Konfigurieren von Tags finden Sie im Experience Platform Tags-Handbuch, beginnend mit der „Übersicht über [&#x200B; Tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) und der &quot;[Schnellstartanleitung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start).

>[!PREREQUISITES]
>
>Um die erforderliche Tag-Erweiterung zu installieren, fragen Sie Ihren Organisations-Admin nach dem Zugriff auf Datenerfassungsfunktionen in der Benutzeroberfläche, einschließlich der `manage_properties`.

1. Installieren Sie in [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/#/data-collection/) die Adobe Advertising [Erweiterung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview):

   1. Öffnen Sie in der entsprechenden Eigenschaft den Erweiterungskatalog und wählen Sie **Adobe Advertising**.

   1. Wählen Sie aus dem Pulldown-Menü **SSC** (für Suche, Social und Commerce) aus.

   1. Geben **im Feld SSC UserID** die numerische Benutzer-ID für das Search-, Social- und Commerce-Konto Ihres Unternehmens ein.

      Wenn Sie Ihre Benutzer-ID nicht kennen, wenden Sie sich an Ihr Adobe Account Team.

   1. Klicken Sie **Speichern**.

1. Erstellen Sie eine neue Regel (z. B. „form_completes„) zum Trigger des Konversions-Tags für Search, Social und Commerce:

   1. Im Abschnitt Ereigniskonfiguration :

      1. Wählen Sie die folgenden Werte aus:

         **Erweiterung:** `Core`

         **Ereignistyp:** `Library Loaded (Page Top)`

      1. Klicken Sie **Änderungen beibehalten**.

   1. Im Abschnitt Bedingungskonfiguration :

      1. Geben Sie die folgenden Werte an:

         **Logiktyp:** `Regular`

         **Erweiterung:** `Core`

         **Bedingungstyp:** `Path Without Query String`

         **Gibt „true“ zurück, wenn der Pfad gleich ist** Der Pfad, unter dem die Konversion verfolgt werden soll (z. B. `/form_complete`).

      1. Klicken Sie **Änderungen beibehalten**.

   1. Im Abschnitt Aktionskonfiguration :

      1. Geben Sie die folgenden Werte an:

         **Erweiterung:** `Adobe Advertising`

         **Aktionstyp:** `AMO Measurement`

         **Name der Konversionseigenschaft:** Der Name der Konversionseigenschaft (z. B. `form_completes`).

         **Value:** Der numerische Wert der Konvertierungseigenschaft (z. B. `1` Tracking von form_completes) oder wählen Sie ein vorhandenes [Datenelement](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements).

      1. Klicken Sie **Änderungen beibehalten**.

   1. Speichern Sie die Regel.

1. Veröffentlichen Sie die Änderungen.

>[!MORELIKETHIS]
>
>* [Über Konversionsverfolgungstags in Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Format von JavaScript-Konversionsverfolgungstags Version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Das Adobe Advertising JavaScript-Konversionszuordnungs-Tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
