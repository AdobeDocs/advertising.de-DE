---
title: Über Zielgruppen-Management in Advertising DSP
description: Erfahren Sie mehr über die Funktionen des Zielgruppen-Managements.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Über Zielgruppen-Management in Advertising DSP

In DSP können Sie Zielgruppensegmente und Zielgruppensätze erstellen und verwalten, die Sie als Ziele für Ihre Platzierungen verwenden können:

* Sie können Ihre eigenen Erstanbieter-Zielgruppendaten erfassen, indem Sie Segmente erstellen und implementieren. Sie können später Benutzer im Segment mit Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment Anzeigen empfangen. Sie können die folgenden Segmenttypen erstellen:

   * [Benutzerspezifische Segmente](/help/dsp/audiences/custom-segment-create.md) zur Nachverfolgung a) Benutzer, die Anzeigen von Desktop-, Mobil- und CTV-Geräten ausgesetzt sind, und b) Benutzer, die bestimmte Webseiten besuchen.

   * [CCPA-Ausschluss von Verkaufssegmenten](/help/dsp/audiences/ccpa-opt-out-segment-create.md) , um die Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) zu verfolgen. Sie können monatliche Berichte über die Benutzer-IDs aus Opt-out-Kaufanfragen abrufen.

      Weitere Informationen zur Adobe Advertising-Unterstützung für CCPA-Opt-out-of-Sale-Anfragen finden Sie unter [Adobe Advertising Support für den California Consumer Privacy Act: Opt-out-Support für Verbraucher](/help/privacy/ccpa-opt-out-of-sale.md).

* Sie können eine Zielgruppenbibliothek von [Wiederverwendbare Zielgruppen](/help/dsp/audiences/reusable-audience-create.md). Gespeicherte Zielgruppen bestehen aus einem Ihrer verfügbaren Zielgruppensegmente und einer Ihrer anderen gespeicherten Zielgruppen. Alle Änderungen, die Sie an einer gespeicherten Zielgruppe vornehmen, werden automatisch auf alle Platzierungen angewendet, die die Zielgruppe als Ziel angeben oder ausschließen, sowie auf alle anderen Zielgruppen, die die gespeicherte Zielgruppe enthalten.

   Gespeicherte Zielgruppen ermöglichen es Medienplanern, Zielgruppen nach Bedarf zu gruppieren, indem mehrere Segmente mithilfe einer komplexen booleschen Logik einbezogen und ausgeschlossen werden. Die Größe jedes einzelnen Segments und die gesamte Zielgruppengröße werden beim Erstellen einer Zielgruppe angegeben. Kampagnenausführer können dann eine oder mehrere gespeicherte Zielgruppen als Platzierungsziele auswählen, anstatt Zielgruppenziele für jede Platzierung manuell zu konfigurieren.

Für das Platzierungs-Targeting stehen auch zusätzliche Zielgruppentypen zur Verfügung.

## Importieren von Erstanbieter- und Drittanbieter-Datensegmenten

DSP können Ihre eigenen Erstanbieter-Datensegmente aus Ihrer Datenverwaltungsplattform (DMP) importieren und bei Bedarf für beliebige Advertiser bereitstellen.

DSP ist ein integriertes Ziel für [die [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), sodass Sie authentifizierte Erstanbietersegmente für zugelassene Advertiser und Benutzer freigeben können, um Kampagnen zu aktivieren. Weitere Informationen zur Real-Time CDP-Integration finden Sie unter [Quellen, Abschnitt](/help/dsp/audiences/sources/source-about.md).

DSP können auch benutzerdefinierte Drittanbietersegmente importieren, einschließlich komplexer Kombinationen von Drittanbietersegmenten. Sie können die Segmente nach Bedarf für beliebige Advertiser bereitstellen.

Wenden Sie sich an [!DNL Adobe] Account-Team für weitere Informationen.

## Als Platzierungsziele verfügbare Zielgruppen

Sie können Ihre Platzierungen auf alle der folgenden Arten von Zielgruppen ausrichten.

* Alle vom Benutzer erstellten Zielgruppensätze, die in DSP gespeichert wurden.

* Alle vom Benutzer erstellten Zielgruppensegmente, die in DSP erstellt wurden:

   * Benutzerdefinierte Segmente für Benutzer, die bestimmte Webseiten besucht haben, und Benutzer, die Impressionen bestimmter Anzeigen ausgesetzt sind.

   * CCPA-Opt-out-of-Sale-Zielgruppensegmente für Benutzer, die Opt-out-Kaufanfragen auf Ihrer Website eingereicht haben, gemäß dem California Consumer Privacy Act (CCPA).

* Alle Ihre importierten Erstanbieter-Datensegmente.

* Alle von Ihnen importierten benutzerdefinierten Drittanbieter-Datensegmente.

* (Nur für die USA bestimmte Platzierungen) [Alle Datensegmente von Drittanbietern, die DSP Kunden von über 30 Anbietern zur Verfügung stehen](/help/dsp/audiences/third-party-data-providers.md), einschließlich [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]und vieles mehr.

   Sie können bestimmte Segmente als Ziel für Benutzer auswählen, die auf Zielgruppendaten basieren (z. B. Benutzer mit bestimmten demografischen Daten, Interessen oder Intents und/oder Verhaltensprofilen). Sie können nach Datenanbieter und Kategorie suchen, nach Segmenten nach Name oder Segment-ID suchen oder die Ergebnisse nach Datenanbieter, Gesamtgröße des Segments, Anzahl der Webbrowser oder Anzahl der Geräte filtern.

   Für Drittanbietersegmente fallen zusätzliche Gebühren an, die neben jedem Segmentnamen angegeben werden.

* (Advertiser mit Adobe Experience Platform und [!DNL Real-Time CDP], Adobe Audience Manager oder Adobe Analytics, die nur Adobe Advertising JavaScript-Konversions-Tags verwenden) Alle verfügbaren Erst-, Zweit- oder Drittanbieter-Zielgruppensegmente, die in erstellt wurden. [!DNL Real-Time CDP], die in Audience Manager erstellt oder von Audience Manager aus in Adobe Experience Cloud veröffentlicht wurden, oder [!DNL Analytics].

   Die Preise für die Verwendung der Segmente werden vorverhandelt und sind in DSP nicht sichtbar.

   Segmente aus [!DNL Analytics] sind ca. eine Stunde nach der Erstellung oder Veröffentlichung als Experience Cloud-Zielgruppen verfügbar. Segmente, die direkt von Audience Manager oder [!DNL Real-Time CDP] sind innerhalb von 24 Stunden nach der Freigabe verfügbar.

   >[!NOTE]
   >
   >Weitere Informationen finden Sie in der Dokumentation für [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)und [die [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) für Informationen zum Einrichten und Erfassen von Daten für Segmente in diesen Lösungen.

## Zielgruppengrößendaten

In den gespeicherten Zielgruppeneinstellungen und Platzierungseinstellungen können Sie detaillierte Daten zur Zielgruppengröße anzeigen:

* Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird angezeigt. Details können nach Gerätetyp (Browser, Mobilgerät oder vernetztes TV) angezeigt werden.

   ![die kombinierte Zielgruppengröße](/help/dsp/assets/audience-size.png)

* Für einzelne Segmente und gespeicherte Zielgruppen werden die Gesamtgröße der Zielgruppe und der CPM (falls zutreffend) neben dem Segmentnamen angezeigt. Sie können weitere Details zum Segment anzeigen, einschließlich der Größe nach Gerätetyp (Browser, Mobilgerät oder vernetztes TV). Bei gespeicherten Zielgruppen entspricht die Gesamtgröße dem deduplizierten Gesamtwert.

   ![die individuelle Segmentgröße](/help/dsp/assets/audience-size-segment.png)

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

* Alle importierten Erstanbietersegmente, die für den Benutzer verfügbar sind.

   Sie können keine Erstanbietersegmente bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an [!DNL Adobe] Account-Team , wenn Sie Erstanbietersegmente für zusätzliche Benutzer freigeben müssen.

* Alle benutzerdefinierten Drittanbietersegmente, die für den Benutzer verfügbar sind.

   Sie können keine Segmente von Drittanbietern bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an [!DNL Adobe] Account-Team , wenn Sie Segmente von Drittanbietern für zusätzliche Benutzer freigeben müssen.

>[!MORELIKETHIS]
>
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für Zielgruppensegmentlogik](audience-segment-logic-syntax.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

