---
title: Über die Zielgruppenverwaltung in Advertising DSP
description: Erfahren Sie mehr über Funktionen zur Zielgruppenverwaltung.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Über die Zielgruppenverwaltung in Advertising DSP

In DSP können Sie Zielgruppensegmente und Zielgruppensätze erstellen und verwalten, die Sie als Ziele für Ihre Platzierungen verwenden können:

* Erfassen Sie Ihre eigenen First-Party-Zielgruppendaten, indem Sie DSP-Segmente erstellen und implementieren. Sie können später Benutzende im Segment erneut mit Anzeigen ansprechen oder verhindern, dass Benutzende im Segment Anzeigen erhalten. Sie können die folgenden Segmenttypen erstellen:

   * [Benutzerdefinierte Segmente](/help/dsp/audiences/custom-segment-create.md) um a) Benutzende zu verfolgen, die Anzeigen von Desktop- und Mobilgeräten ausgesetzt sind, und b) Benutzende, die bestimmte Web-Seiten besuchen. Das Tracking-Tag kann entweder Cookie-basierte Benutzer oder Benutzer verfolgen, die mit universellen ID5-IDs verknüpft sind.

   * [CCPA-Opt-out-of-Sale-Segmente](/help/dsp/audiences/ccpa-opt-out-segment-create.md) um die Benutzer-IDs aus Verbraucher-Opt-out-of-Sale-Anfragen auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) zu verfolgen. Sie können monatliche Berichte zu Benutzer-IDs aus Opt-out-Kaufanfragen abrufen.

     Weitere Informationen zur Adobe Advertising-Unterstützung für CCPA-Opt-out-Anfragen finden Sie unter [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Verbraucher-Opt-out-Unterstützung](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta-Funktion) [Abrufen und Verwenden universeller IDs für das Cookie-lose Targeting](/help/dsp/audiences/universal-ids.md):

   * Senden Sie Ihre authentifizierten [!DNL LiveRamp] [!DNL RampID] Segmente manuell direkt an DSP.

   * DSP erlauben, Erstanbietersegmente aus Ihrer Kundendatenplattform zu importieren und in unterstützte universelle ID-Typen zu übersetzen.

   * Einbeziehen von Drittanbietersegmenten, die universelle IDs enthalten, in Ihre Platzierungsziele ohne zusätzliche Schritte.

* Erstellen Sie eine Zielgruppenbibliothek mit [wiederverwendbaren Zielgruppen](/help/dsp/audiences/reusable-audience-create.md). Gespeicherte Zielgruppen bestehen aus einem Ihrer verfügbaren Zielgruppensegmente und einer Ihrer anderen gespeicherten Zielgruppen. Alle Änderungen, die Sie an einer gespeicherten Zielgruppe vornehmen, werden automatisch auf alle Platzierungen angewendet, die die Zielgruppe ansprechen oder ausschließen, sowie auf alle anderen Zielgruppen, die die gespeicherte Zielgruppe enthalten.

  Gespeicherte Zielgruppen ermöglichen es Medienplanern, Zielgruppen nach Bedarf zu gruppieren, indem sie mehrere Segmente mithilfe einer komplexen booleschen Logik ein- und ausschließen. Die Größe der einzelnen Segmente und die Gesamtgröße der Zielgruppe werden beim Erstellen einer Zielgruppe angezeigt. Ausführende von Kampagnen können dann einfach eine oder mehrere gespeicherte Zielgruppen als Platzierungsziele auswählen, anstatt Zielgruppenziele für jede Platzierung manuell zu konfigurieren.

Für das Platzierungs-Targeting sind auch zusätzliche Zielgruppentypen verfügbar.

## Importieren von Datensegmenten von Erstanbietern und Drittanbietern

Sie haben viele Möglichkeiten, Datensegmente von Erstanbietern und Drittanbietern mithilfe der DSP-Benutzeroberfläche und/oder über benutzerdefinierte Importdienste in DSP zu importieren.

* DSP kann Ihre Adobe Audience Manager- und andere [!DNL Adobe] Zielgruppen für die Zielgruppenbestimmung abrufen. Informationen zu Voraussetzungen und Anweisungen finden Sie unter [Adobe Audience Manager-Segmente für das Anzeigen-Targeting ](/help/integrations/audience-manager/import-audiences.md).

* DSP kann First-Party-Datensegmente mithilfe der (Quellen[Funktion von unterstützten Kundendatenplattformen in Segmente mit universellen IDs ](/help/dsp/audiences/sources/source-about.md). Sie können [ authentifizierte Segmente auch manuell  [!DNL LiveRamp] [!DNL RampID] DSP ](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kann Ihre anderen Erstanbieter-Datensegmente direkt von Ihrer Datenverwaltungsplattform (DMP) importieren und sie nach Bedarf für eine beliebige Gruppe von Werbetreibenden bereitstellen.

* DSP kann benutzerdefinierte Drittanbietersegmente importieren, einschließlich komplexer Kombinationen von Drittanbietersegmenten. Sie können die Segmente nach Bedarf für eine beliebige Gruppe von Advertisern bereitstellen.

Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.

## Zielgruppen, die als Platzierungsziele verfügbar sind

Sie können Ihre Platzierungen für alle folgenden Arten von Zielgruppen auswählen.

* Alle von Benutzenden erstellten Zielgruppensätze, die in DSP gespeichert wurden.

* Alle vom Benutzer erstellten Zielgruppensegmente, die in DSP erstellt wurden:

   * Benutzerdefinierte Segmente für Benutzer, die bestimmte Web-Seiten besucht haben, und für Benutzer, die Impressionen bestimmter Anzeigen ausgesetzt waren.

     Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

   * Zielgruppensegmente für das CCPA-Opt-out vom Verkauf für Benutzer, die Opt-out vom Verkauf auf Ihrer Website eingereicht haben, gemäß dem California Consumer Privacy Act (CCPA).

* Alle Ihre importierten Erstanbieter-Datensegmente, einschließlich der Segmente, die in universelle IDs übersetzt wurden.

  Für Impressionen, die an universelle IDs gesendet werden, werden zusätzliche Gebühren berechnet. Weitere Informationen zu [ finden Sie unter „Über First-Party](/help/dsp/audiences/sources/source-about.md)Zielgruppenquellen“.

* Alle Ihre importierten benutzerdefinierten Datensegmente von Drittanbietern

* (Platzierungen, die nur für die USA bestimmt sind) [Alle Drittanbieterdatensegmente, die DSP-Kunden von über 30 Anbietern zur Verfügung stehen](/help/dsp/audiences/third-party-data-providers.md) einschließlich [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]), [!DNL Lotame], [!DNL Neustar] und vielen mehr.

  Sie können bestimmte Segmente auswählen, die Benutzende auf der Grundlage von Zielgruppendaten ansprechen (z. B. Benutzende mit bestimmter Demografie, Interessen oder Absichten und/oder Verhaltensprofile). Sie können nach Datenanbieter und Kategorie suchen, nach Segmenten nach Name oder Segment-ID suchen oder die Ergebnisse nach Datenanbieter, Gesamtgröße des Segments, Anzahl der Webbrowser oder der Geräte filtern.

  Für Drittanbietersegmente fallen zusätzliche Gebühren an, die neben jedem Segmentnamen angegeben werden.

* (Werbetreibende mit Adobe Experience Platform und [!DNL Real-Time CDP], Adobe Audience Manager oder Adobe Analytics, die nur Adobe Advertising-JavaScript-Konversions-Tags verwenden) Alle Ihre verfügbaren Zielgruppensegmente von Erst-, Zweit- oder Drittanbietern, die in [!DNL Real-Time CDP] erstellt, in der Audience Manager erstellt oder von Audience Manager oder [!DNL Analytics] aus in Adobe Experience Cloud veröffentlicht wurden.

  Die Preise für die Verwendung der Segmente werden vorab ausgehandelt und sind in DSP nicht sichtbar.

  Segmente aus [!DNL Analytics] sind etwa eine Stunde nach dem Erstellen oder Veröffentlichen als Experience Cloud-Zielgruppen verfügbar. Segmente, die direkt aus dem Audience Manager oder [!DNL Real-Time CDP] stammen, sind innerhalb von 24 Stunden nach ihrer Freigabe verfügbar.

  >[!NOTE]
  >
  >In der Dokumentation für [Audience Manager ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html) und [die [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) finden Sie Informationen zum Einrichten und Erfassen von Daten für Segmente in diesen Lösungen.

## Daten zur Zielgruppengröße

Unter Zielgruppen > Alle Zielgruppen und im Abschnitt Zielgruppen-Targeting der Platzierungseinstellungen können Sie jede Segmentliste nach Größenbereich filtern, einschließlich des Gesamtbereichs und separater Bereiche für bestimmte Gerätetypen oder universelle ID-Typen.

![Nach Zielgruppengröße filtern](/help/dsp/assets/audience-size-filter.png)

Sie können auch detaillierte Daten zur Zielgruppengröße sehen:

* Die gesamte und aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird angezeigt, und Sie können Details nach Gerätetyp (Browser, Mobilgerät oder vernetztes Fernsehen) anzeigen.

  ![Die kombinierte Zielgruppengröße](/help/dsp/assets/audience-size.png)

* Für einzelne Segmente werden die Gesamtgröße der Zielgruppe und CPM (falls zutreffend) neben dem Segmentnamen angezeigt.

  ![Die Größe des einzelnen Segments](/help/dsp/assets/audience-size-segment.png)

* Sie können weitere Details zu einem einzelnen Segment oder einer gespeicherten Zielgruppe anzeigen, einschließlich der Größe nach Browser, Mobiltelefon, vernetztem TV und universeller ID-Partnertyp. Bei gespeicherten Zielgruppen entspricht die Gesamtgröße der deduplizierten Gesamtgröße.

  ![Das einzelne Segment oder gespeicherte Zielgruppendetails](/help/dsp/assets/audience-size-segment-details.png)

## Die Zielgruppenansichten

### Die Ansicht Alle Zielgruppen

In der [!UICONTROL All Audiences] oder Zielgruppenbibliothek können Sie wiederverwendbare Zielgruppen speichern und verwalten, darunter auch Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen. Sie können Zielgruppen als Ziele für mehrere Platzierungen verwenden. Die Anzahl der Platzierungen, in denen jede Zielgruppe verwendet wird, wird neben dem Platzierungsnamen angezeigt.

Sie können jede Zielgruppe bearbeiten, klonen, löschen, exportieren oder freigeben.

### Die Segmentansicht

In der [!UICONTROL Segments] können alle Benutzenden zusätzliche benutzerdefinierte Segmente erstellen.

In der [!UICONTROL Segments] Ansicht werden auch die folgenden Segmenttypen aufgelistet:

* Alle benutzererstellten benutzerdefinierten Segmente, die dem Benutzer zur Verfügung stehen.

  Sie können Tracking-Tags für jedes der von Ihnen erstellten benutzerdefinierten Segmente anzeigen und diese Segmente für andere Benutzer freigeben. Sie können die von Ihnen erstellten benutzerdefinierten Segmente auch bearbeiten oder löschen.

  Benutzerdefinierte Segmente, die andere Benutzende für Sie freigegeben haben, können nicht bearbeitet oder freigegeben werden.

* Alle Erstanbietersegmente, die im Istzustand importiert wurden und dem Benutzer zur Verfügung stehen.

  First-Party-Segmente, die für Sie freigegeben wurden, können nicht bearbeitet oder freigegeben werden. Wenden Sie sich an Ihr Adobe-Konto-Team , wenn Sie Erstanbietersegmente für weitere Benutzende freigeben müssen.

* Alle benutzerdefinierten Drittanbietersegmente, die dem Benutzer zur Verfügung stehen.

  Sie können keine Drittanbietersegmente bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an Ihr Adobe-Account-Team , wenn Sie Drittanbietersegmente für zusätzliche Benutzer freigeben müssen.

### Die Quellenansicht

In der [!UICONTROL Sources] können Sie Quellen für Erstanbietersegmente in unterstützten Kundendatenplattformen konfigurieren, die Sie in Segmente mit angegebenen universellen ID-Typen konvertieren möchten. Die Quelleinstellungen enthalten einen automatisch generierten Quellschlüssel, den Sie Ihrer Kundendatenplattform bereitstellen, um die Verbindung herzustellen.

Weitere Informationen zu den unterstützten Kundendatenplattformen, den unterstützten universellen ID-Typen und den Workflows zum Einrichten von Verbindungen zu jeder Kundendatenplattform finden Sie unter &quot;[ zu Quellen](/help/dsp/audiences/sources/source-about.md).

Die übersetzten Segmente können in wiederverwendbare Zielgruppen und in Platzierungseinstellungen für das Cookie-lose Targeting einbezogen werden.

>[!MORELIKETHIS]
>
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Erstellen einer wiederverwendbaren Zielgruppe](reusable-audience-create.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](/help/dsp/audiences/sources/source-manage.md)
>* [Importieren Sie authentifizierte Segmente manuell aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
