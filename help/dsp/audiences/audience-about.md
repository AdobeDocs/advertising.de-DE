---
title: About audience management in Advertising DSP
description: Learn about audience management features.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
TQID: https://experienceleague.adobe.com/IocF0s67I-vJAUx9Eom-aWEf-Q6H-ZOjczyGr0f9PsA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1394
ht-degree: 0%

---

# About audience management in Advertising DSP

In DSP, you can create and manage audience segments and audience sets, which you can use as targets for your placements:

* Collect your own first-party audience data by creating and implementing DSP segments. You can later retarget users in the segment with ads or prevent users in the segment from receiving ads. You can create the following types of segments:

   * [Custom segments](/help/dsp/audiences/custom-segment-create.md) to track a) users exposed to ads from desktop and mobile devices and b) users who visit specific webpages. The tracking tag can track either cookie-based users or users associated with ID5 universal IDs.

   * [CCPA opt-out-of-sale segments](/help/dsp/audiences/ccpa-opt-out-segment-create.md) to track the users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). You can retrieve monthly reports of the user IDs from opt-out-of-sale requests.

     For more information about Adobe Advertising support for CCPA opt-out-of-sale requests, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta feature) [Obtain and use universal IDs for cookieless targeting](/help/dsp/audiences/universal-ids.md):

   * Manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP.

   * Allow DSP to import first-party segments from your customer data platform and translate them to supported universal ID types.

   * Include third-party segments that contain universal IDs in your placement targets without any extra steps.

* Create an audience library of [reusable audiences](/help/dsp/audiences/reusable-audience-create.md). Saved audiences are composed of any of your available audience segments and any of your other saved audiences. Any changes you make to a saved audience are automatically applied to all placements that target or exclude the audience and to all other audiences that include the saved audience.

  Saved audiences allow media planners to group audiences as needed, by including and excluding multiple segments using complex Boolean logic. The  (targetable) size of each individual segment and the overall active audience size are indicated as you build an audience. Campaign executioners can then simply select one or more saved audiences as placement targets rather than manually configure audience targets for each placement.

Für das Platzierungs-Targeting sind auch zusätzliche Zielgruppentypen verfügbar.

## Importieren von Datensegmenten von Erstanbietern und Drittanbietern

Sie haben viele Möglichkeiten, Datensegmente von Erstanbietern und Drittanbietern mithilfe der DSP-Benutzeroberfläche und/oder über benutzerdefinierte Importdienste in DSP zu importieren.

* DSP kann Ihre Adobe Audience Manager- und andere [!DNL Adobe] Zielgruppen für die Zielgruppenbestimmung abrufen. Informationen zu Voraussetzungen und Anweisungen finden Sie unter [Adobe Audience Manager-Segmente für das Anzeigen-Targeting &#x200B;](/help/integrations/audience-manager/import-audiences.md).

* DSP kann First-Party-Datensegmente mithilfe der (Quellen[Funktion von unterstützten Kundendatenplattformen in Segmente mit universellen IDs &#x200B;](/help/dsp/audiences/sources/source-about.md). Sie können [&#x200B; authentifizierte Segmente auch manuell  [!DNL LiveRamp] [!DNL RampID] DSP &#x200B;](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kann Ihre anderen Erstanbieter-Datensegmente direkt von Ihrer Datenverwaltungsplattform (DMP) importieren und sie nach Bedarf für eine beliebige Gruppe von Werbetreibenden bereitstellen.

* DSP kann benutzerdefinierte Drittanbietersegmente importieren, einschließlich komplexer Kombinationen von Drittanbietersegmenten. Sie können die Segmente nach Bedarf für eine beliebige Gruppe von Advertisern bereitstellen.

Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

## Zielgruppen, die als Platzierungsziele verfügbar sind

Sie können Ihre Platzierungen für alle folgenden Arten von Zielgruppen auswählen.

* Alle von Benutzenden erstellten Zielgruppensätze, die in DSP gespeichert wurden.

* Alle vom Benutzer erstellten Zielgruppensegmente, die in DSP erstellt wurden:

   * Benutzerdefinierte Segmente für Benutzer, die bestimmte Web-Seiten besucht haben, und für Benutzer, die Impressionen bestimmter Anzeigen ausgesetzt waren.

     Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

   * Zielgruppensegmente für das CCPA-Opt-out vom Verkauf für Benutzer, die Opt-out vom Verkauf auf Ihrer Website eingereicht haben, gemäß dem California Consumer Privacy Act (CCPA).

* Alle Ihre importierten Erstanbieter-Datensegmente, einschließlich der Segmente, die in universelle IDs übersetzt wurden.

  Für Impressionen, die an universelle IDs gesendet werden, werden zusätzliche Gebühren berechnet. Tarife finden [&#x200B; unter „Über Erstanbieter-](/help/dsp/audiences/sources/source-about.md)&quot;.

* Alle Ihre importierten benutzerdefinierten Datensegmente von Drittanbietern

* (Nur für USA) [Alle Drittanbieterdatensegmente, die DSP-Kunden von über 30 Anbietern zur Verfügung stehen](/help/dsp/audiences/third-party-data-providers.md) einschließlich [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]), [!DNL Lotame], [!DNL Neustar] und vielen mehr.

  Sie können bestimmte Segmente auswählen, die Benutzende auf der Grundlage von Zielgruppendaten ansprechen (z. B. Benutzende mit bestimmter Demografie, Interessen oder Absichten und/oder Verhaltensprofile). Sie können nach Datenanbieter und Kategorie suchen, nach Segmenten nach Name oder Segment-ID suchen oder die Ergebnisse nach Datenanbieter, aktiver Segmentgröße, Anzahl der Webbrowser oder der Geräte filtern.

  Für Drittanbietersegmente fallen zusätzliche Gebühren an, die neben jedem Segmentnamen angegeben werden.

* (Werbetreibende mit Adobe Experience Platform und [!DNL Real-Time CDP], Adobe Audience Manager oder Adobe Analytics, die nur Adobe Advertising JavaScript-Konversions-Tags verwenden) Alle Ihre verfügbaren Zielgruppensegmente von Erst-, Zweit- oder Drittanbietern, die in [!DNL Real-Time CDP] erstellt, in Audience Manager erstellt oder aus Audience Manager oder [!DNL Analytics] in Adobe CX Enterprise veröffentlicht wurden.

  Die Preise für die Verwendung der Segmente werden vorab ausgehandelt und sind in DSP nicht sichtbar.

  Segmente aus [!DNL Analytics] sind etwa eine Stunde nach dem Erstellen oder Veröffentlichen als CX Enterprise-Zielgruppen verfügbar. Segmente, die direkt aus Audience Manager oder [!DNL Real-Time CDP] stammen, sind innerhalb von 24 Stunden nach ihrer Freigabe verfügbar.

  >[!NOTE]
  >
  >Weitere Informationen zum Einrichten und Erfassen von Daten für Segmente in [&#128279;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html) Lösungen finden Sie in [&#x200B; Dokumentation für &lbrace;0 [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html)Audience Manager[, Analytics](https://experienceleague.adobe.com/docs/analytics.html) und.

## Daten zur Zielgruppengröße

Unter Zielgruppen > Alle Zielgruppen und im Abschnitt Zielgruppen-Targeting der Platzierungseinstellungen können Sie jede Segmentliste nach Größenbereich filtern, einschließlich separater Bereiche für bestimmte Gerätetypen oder universelle ID-Typen.

![Nach Zielgruppengröße filtern](/help/dsp/assets/audience-size-filter.png)

Sie können auch detaillierte Daten zur Zielgruppengröße sehen:

* Die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird angezeigt, und Sie können Details nach Gerätetyp (Browser, Mobilgerät oder vernetztes Fernsehen) anzeigen.

  ![Die kombinierte Zielgruppengröße](/help/dsp/assets/audience-size.png)

* Für einzelne Segmente werden die aktive Zielgruppengröße und CPM (falls zutreffend) neben dem Segmentnamen angezeigt.

  ![Die Größe des einzelnen Segments](/help/dsp/assets/audience-size-segment.png)

* Sie können weitere Details zu einem einzelnen Segment oder einer gespeicherten Zielgruppe anzeigen, einschließlich der Größe nach Browser, Mobiltelefon, vernetztem TV und universeller ID-Partnertyp. Bei gespeicherten Zielgruppen entspricht die gesamte aktive Zielgruppengröße der deduplizierten Gesamtgröße.

  ![Das einzelne Segment oder gespeicherte Zielgruppendetails](/help/dsp/assets/audience-size-segment-details.png)

## Die [!UICONTROL Audiences]

### Die [!UICONTROL All Audiences]

In der [!UICONTROL All Audiences] oder Zielgruppenbibliothek können Sie wiederverwendbare Zielgruppen speichern und verwalten, darunter auch Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen. Sie können Zielgruppen als Ziele für mehrere Platzierungen verwenden. Die Anzahl der Platzierungen, in denen jede Zielgruppe verwendet wird, wird neben dem Platzierungsnamen angezeigt.

Sie können jede Zielgruppe bearbeiten, klonen, löschen, exportieren oder freigeben.

### Die [!UICONTROL Segments]

In der [!UICONTROL Segments] können alle Benutzenden zusätzliche benutzerdefinierte Segmente erstellen.

The [!UICONTROL Segments] view also lists the following segment types:

* All user-created custom segments available to the user.

  You can view tracking tags for any of the custom segments you created, and share those segments with other users. You can also edit or delete the custom segments you created.

  You can&#39;t edit or share custom segments that other users have shared with you.

* All first-party segments imported as-is that are available to the user.

  You can&#39;t edit or share first-party segments that were shared with you. Contact your Adobe Account Team if you need to share first-party segments with additional users.

* All custom third-party segments available to the user.

  You can&#39;t edit or share third-party segments that were shared with you. Contact your Adobe Account Team if you need to share third-party segments with additional users.

### Die [!UICONTROL Sources]

In the [!UICONTROL Sources] view, you can configure sources for first-party segments in supported customer data platforms that you want to convert to segments containing specified universal ID types. The source settings include an auto-generated source key, which you&#39;ll provide to your customer data platform to establish the connection.

For more information about the supported customer data platforms, supported universal ID types, and the workflows to set up connections to each customer data platform, see &quot;[About first-party audience sources](/help/dsp/audiences/sources/source-about.md).&quot;

The translated segments are available to include in reusable audiences and in placement settings for cookieless targeting.

>[!MORELIKETHIS]
>
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Create a reusable audience](reusable-audience-create.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](/help/dsp/audiences/sources/source-manage.md)
>* [Manually import authenticated segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
