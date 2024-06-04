---
title: Über Zielgruppen-Management in Advertising DSP
description: Erfahren Sie mehr über die Funktionen des Zielgruppen-Managements.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 94c41ec311ed79897e1e26a650605c0213450071
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 0%

---

# Über Zielgruppen-Management in Advertising DSP

In DSP können Sie Zielgruppensegmente und Zielgruppensätze erstellen und verwalten, die Sie als Ziele für Ihre Platzierungen verwenden können:

* Erfassen Sie Ihre eigenen Erstanbieter-Zielgruppendaten, indem Sie DSP Segmente erstellen und implementieren. Sie können später Benutzer im Segment mit Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment Anzeigen empfangen. Sie können die folgenden Segmenttypen erstellen:

   * [Benutzerspezifische Segmente](/help/dsp/audiences/custom-segment-create.md) zur Verfolgung a) Benutzer, die Anzeigen von Desktop- und Mobilgeräten ausgesetzt sind, und b) Benutzer, die bestimmte Webseiten besuchen. Das Tracking-Tag kann entweder Cookie-basierte Benutzer oder Benutzer verfolgen, die mit universellen IDs der ID5 verknüpft sind.

   * [CCPA-Ausschluss von Verkaufssegmenten](/help/dsp/audiences/ccpa-opt-out-segment-create.md) , um die Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) zu verfolgen. Sie können monatliche Berichte über die Benutzer-IDs aus Opt-out-Kaufanfragen abrufen.

     Weitere Informationen zur Adobe Advertising-Unterstützung für CCPA-Opt-out-Kaufanfragen finden Sie unter [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta-Funktion) [Abrufen und Verwenden von universellen IDs für Cookie-Targeting](/help/dsp/audiences/universal-ids.md):

   * Authentifizieren manuell senden [!DNL LiveRamp] [!DNL RampID] Segmente direkt DSP.

   * Ermöglicht DSP, Erstanbietersegmente aus Ihrer Kundendatenplattform zu importieren und in unterstützte universelle ID-Typen zu übersetzen.

   * Schließen Sie Segmente von Drittanbietern, die universelle IDs enthalten, ohne zusätzliche Schritte in Ihre Platzierungsziele ein.

* Erstellen einer Zielgruppenbibliothek von [Wiederverwendbare Zielgruppen](/help/dsp/audiences/reusable-audience-create.md). Gespeicherte Zielgruppen bestehen aus einem Ihrer verfügbaren Zielgruppensegmente und einer Ihrer anderen gespeicherten Zielgruppen. Alle Änderungen, die Sie an einer gespeicherten Zielgruppe vornehmen, werden automatisch auf alle Platzierungen angewendet, die die Zielgruppe als Ziel angeben oder ausschließen, sowie auf alle anderen Zielgruppen, die die gespeicherte Zielgruppe enthalten.

  Gespeicherte Zielgruppen ermöglichen es Medienplanern, Zielgruppen nach Bedarf zu gruppieren, indem mehrere Segmente mithilfe einer komplexen booleschen Logik einbezogen und ausgeschlossen werden. Die Größe jedes einzelnen Segments und die gesamte Zielgruppengröße werden beim Erstellen einer Zielgruppe angegeben. Kampagnenausführer können dann eine oder mehrere gespeicherte Zielgruppen als Platzierungsziele auswählen, anstatt Zielgruppenziele für jede Platzierung manuell zu konfigurieren.

Für das Platzierungs-Targeting stehen auch zusätzliche Zielgruppentypen zur Verfügung.

## Importieren von Erstanbieter- und Drittanbieter-Datensegmenten

Sie haben viele Möglichkeiten, Erstanbieter- und Drittanbieter-Datensegmente in DSP zu importieren, indem Sie die DSP-Benutzeroberfläche und/oder benutzerdefinierte Importdienste verwenden.

* DSP können Ihre Adobe Audience Manager und andere [!DNL Adobe] Zielgruppen für Targeting. Voraussetzungen und Anweisungen finden Sie unter &quot;[Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md).

* DSP kann Erstanbieter-Datensegmente von unterstützten Kundendatenplattformen mithilfe der [Quellen-Funktion](/help/dsp/audiences/sources/source-about.md). Sie können auch [Manuelles Senden Ihrer authentifizierten [!DNL LiveRamp] [!DNL RampID] Segmente direkt DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP können Ihre anderen Erstanbieter-Datensegmente direkt aus Ihrer Data Management Platform (DMP) importieren und bei Bedarf für beliebige Advertiser bereitstellen.

* DSP können benutzerdefinierte Drittanbietersegmente importieren, einschließlich komplexer Kombinationen aus Drittanbietersegmenten. Sie können die Segmente nach Bedarf für beliebige Advertiser bereitstellen.

Wenden Sie sich für weitere Informationen an Ihr Adobe-Account-Team.

## Als Platzierungsziele verfügbare Zielgruppen

Sie können Ihre Platzierungen auf alle der folgenden Arten von Zielgruppen ausrichten.

* Alle vom Benutzer erstellten Zielgruppen, die in DSP gespeichert wurden.

* Alle vom Benutzer erstellten Zielgruppensegmente, die in DSP erstellt wurden:

   * Benutzerdefinierte Segmente für Benutzer, die bestimmte Webseiten besucht haben, und Benutzer, die Impressionen bestimmter Anzeigen ausgesetzt sind.

     Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

   * CCPA-Opt-out-of-Sale-Zielgruppensegmente für Benutzer, die Opt-out-Kaufanfragen auf Ihrer Website eingereicht haben, gemäß dem California Consumer Privacy Act (CCPA).

* Alle von Ihnen importierten Erstanbieter-Datensegmente, einschließlich Segmenten, die in universelle IDs übersetzt wurden.

  Für Impressionen, die an universelle IDs gesendet werden, fallen zusätzliche Gebühren an. Siehe &quot;[Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)&quot;für Tarife.

* Alle von Ihnen importierten benutzerdefinierten Drittanbieter-Datensegmente.

* (Nur für die USA bestimmte Platzierungen) [Alle Datensegmente von Drittanbietern, die DSP Kunden von über 30 Anbietern zur Verfügung stehen](/help/dsp/audiences/third-party-data-providers.md), einschließlich [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]und vieles mehr.

  Sie können bestimmte Segmente als Ziel für Benutzer auswählen, die auf Zielgruppendaten basieren (z. B. Benutzer mit bestimmten demografischen Daten, Interessen oder Intents und/oder Verhaltensprofilen). Sie können nach Datenanbieter und Kategorie suchen, nach Segmenten nach Name oder Segment-ID suchen oder die Ergebnisse nach Datenanbieter, Gesamtgröße des Segments, Anzahl der Webbrowser oder Anzahl der Geräte filtern.

  Für Drittanbietersegmente fallen zusätzliche Gebühren an, die neben jedem Segmentnamen angegeben werden.

* (Werbetreibende mit Adobe Experience Platform und [!DNL Real-Time CDP], Adobe Audience Manager oder Adobe Analytics, die nur Adobe Advertising-JavaScript-Konversions-Tags verwenden) Alle verfügbaren Erst-, Zweit- oder Drittanbieter-Zielgruppensegmente, die in erstellt wurden [!DNL Real-Time CDP], die in Audience Manager erstellt oder von Audience Manager aus in Adobe Experience Cloud veröffentlicht wurden, oder [!DNL Analytics].

  Die Preise für die Verwendung der Segmente werden vorverhandelt und sind in DSP nicht sichtbar.

  Segmente aus [!DNL Analytics] sind ca. eine Stunde nach der Erstellung oder Veröffentlichung als Experience Cloud-Audiences verfügbar. Segmente, die direkt von Audience Manager oder [!DNL Real-Time CDP] sind innerhalb von 24 Stunden nach der Freigabe verfügbar.

  >[!NOTE]
  >
  >Siehe die Dokumentation für [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), und [die [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) für Informationen zum Einrichten und Erfassen von Daten für Segmente in diesen Lösungen.

## Zielgruppengrößendaten

Unter Zielgruppen > Alle Zielgruppen und im Abschnitt Zielgruppen-Targeting der Platzierungseinstellungen können Sie jede Segmentliste nach Größenbereich filtern, einschließlich des Gesamtbereichs und separater Bereiche für bestimmte Gerätetypen oder universelle ID-Typen.

![nach Zielgruppengröße filtern](/help/dsp/assets/audience-size-filter.png)

Sie können auch detaillierte Daten zur Zielgruppengröße anzeigen:

* Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird angezeigt. Details können nach Gerätetyp (Browser, Mobilgerät oder vernetztes TV) angezeigt werden.

  ![die kombinierte Zielgruppengröße](/help/dsp/assets/audience-size.png)

* Bei einzelnen Segmenten werden die Gesamtzielgruppengröße und CPM (falls zutreffend) neben dem Segmentnamen angezeigt.

  ![die individuelle Segmentgröße](/help/dsp/assets/audience-size-segment.png)

* Sie können weitere Details zu einem einzelnen Segment oder einer gespeicherten Zielgruppe anzeigen, einschließlich der Größe nach Browser, Mobilgerät, vernetztem TV und Partner vom Typ universelle ID . Bei gespeicherten Zielgruppen entspricht die Gesamtgröße dem deduplizierten Gesamtwert.

  ![das einzelne Segment oder die gespeicherten Zielgruppendetails](/help/dsp/assets/audience-size-segment-details.png)

## Ansichten der Zielgruppen

### Ansicht &quot;Alle Zielgruppen&quot;

Im [!UICONTROL All Audiences] -Ansicht oder Zielgruppenbibliothek können Sie wiederverwendbare Zielgruppen speichern und verwalten, die Zielgruppen aus Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen enthalten. Sie können Zielgruppen als Ziele für mehrere Platzierungen verwenden. Die Anzahl der Platzierungen, in denen jede Zielgruppe verwendet wird, wird neben dem Platzierungsnamen angezeigt.

Sie können beliebige Zielgruppen bearbeiten, klonen, löschen, exportieren oder freigeben.

### Die Segmentansicht

Im [!UICONTROL Segments] -Ansicht können alle Benutzer zusätzliche benutzerdefinierte Segmente erstellen.

Die [!UICONTROL Segments] -Ansicht listet auch die folgenden Segmenttypen auf:

* Alle vom Benutzer erstellten benutzerdefinierten Segmente, die für den Benutzer verfügbar sind.

  Sie können Tracking-Tags für jedes der von Ihnen erstellten benutzerdefinierten Segmente anzeigen und diese Segmente für andere Benutzer freigeben. Sie können auch die von Ihnen erstellten benutzerdefinierten Segmente bearbeiten oder löschen.

  Sie können keine benutzerdefinierten Segmente bearbeiten oder freigeben, die andere Benutzer für Sie freigegeben haben.

* Alle Erstanbietersegmente, die unverändert importiert wurden und für den Benutzer verfügbar sind.

  Sie können keine Erstanbietersegmente bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an Ihr Adobe Account-Team, wenn Sie Erstanbietersegmente für weitere Benutzer freigeben möchten.

* Alle benutzerdefinierten Drittanbietersegmente, die für den Benutzer verfügbar sind.

  Sie können keine Segmente von Drittanbietern bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an Ihr Adobe Account-Team, wenn Sie Segmente von Drittanbietern für weitere Benutzer freigeben möchten.

### Die Ansicht &quot;Quellen&quot;

Im [!UICONTROL Sources] -Ansicht können Sie Quellen für Erstanbietersegmente in unterstützten Kundendatenplattformen konfigurieren, die Sie in Segmente mit bestimmten universellen ID-Typen konvertieren möchten. Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie Ihrer Kundendatenplattform zur Herstellung der Verbindung zur Verfügung stellen.

Weitere Informationen zu den unterstützten Kundendatenplattformen, unterstützten universellen ID-Typen und den Workflows zum Einrichten von Verbindungen zu den einzelnen Kundendatenplattformen finden Sie unter &quot;[Über Quellen](/help/dsp/audiences/sources/source-about.md).&quot;

Die übersetzten Segmente können in wiederverwendbare Zielgruppen und in Platzierungseinstellungen für das Cookie-Targeting einbezogen werden.

>[!MORELIKETHIS]
>
>* [Unterstützung für die Aktivierung von universellen IDs](/help/dsp/audiences/universal-ids.md)
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
