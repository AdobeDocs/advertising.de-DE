---
title: Unterstützung für das Aktivieren universeller IDs
description: Erfahren Sie mehr über die Unterstützung beim Importieren Ihrer universellen ID-Segmente, Erstellen benutzerdefinierter Segmente zum Nachverfolgen universeller IDs und Konvertieren anderer Benutzerkennung in Erstanbietersegmente in universelle IDs für das Cookie-lose Targeting.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Unterstützung für das Aktivieren universeller IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta-Funktion*

DSP unterstützt personenbasierte, universelle IDs für Cookie-loses Targeting von Einzelgeräten (nicht geräteübergreifend) in digitalen Formaten, die von DSP unterstützt werden.

* Sie können Ihre authentifizierten [[!DNL LiveRamp] [!DNL RampIDs]] manuell über das Dashboard [!DNL LiveRamp] [!DNL Connect] direkt an DSP senden. Siehe &quot;[Manueller Import authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP kann Ihre Erstanbietersegmente, die aus gehashten E-Mail-IDs bestehen, aufnehmen, die in Ihrer Kundendatenplattform (CDP) erstellt wurden, und sie in [!DNL LiveRamp] [!DNL RampIDs]- und [!DNL Unified ID 2.0 (UID2.0)]-IDs konvertieren. Weitere Informationen zu den unterstützten Kundendatenplattformen, den verfügbaren Funktionen für jeden unterstützten universellen ID-Typ und den zugehörigen Workflows finden Sie unter &quot;[ zu Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md).

* Sie können benutzerdefinierte Segmente erstellen, die Benutzer verfolgen, die mit universellen ID5-IDs verknüpft sind, die Anzeigen von Desktop- und Mobilgeräten ausgesetzt sind und bestimmte Web-Seiten besuchen. ID5 verwendet ein probabilistisches Modell, um eine ID zuzuweisen, die aus verschiedenen Benutzersignalen und Browser-Signalen abgeleitet wird. Anweisungen finden Sie unter [Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md).

* Drittanbietersegmente einiger Anbieter enthalten möglicherweise automatisch universelle IDs zusätzlich zu den Benutzern, die von Cookies oder Geräte-IDs verfolgt werden. Beispielsweise können Segmente aus [!DNL Eyeota] automatisch ID5-IDs enthalten, und Segmente aus [!DNL Lotame] können UID2.0-IDs enthalten. Die Segmentdetails enthalten die Größe für jeden Typ. Es gilt die übliche Nutzungsgebühr für jedes Segment, die neben dem Segmentnamen angegeben ist; für die ID5-IDs werden keine zusätzlichen Gebühren berechnet.

## Berichte nach universeller ID-Typ

* **Benutzerdefinierte Berichte:** Kosten-, Impression-, Klick-, Konversions- und Häufigkeitsdaten nach dem universellen ID-Typ sind in benutzerdefinierten Berichten verfügbar.

* **[!DNL Analytics]:** Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), die alle erforderlichen Schritte implementiert haben, können in [!DNL Analytics] View-Through-Konversionen nach universeller ID-Typ anzeigen.

  >[!IMPORTANT]
  >
  >Stellen Sie für eine ordnungsgemäße Konversionszuordnung sicher, dass die Clickthrough-URLs für Ihre Anzeigen sowohl die [EF-ID als auch die AMO-ID](/help/integrations/analytics/ids.md) enthalten.

* **Segmentdetails:** Die Segmentdetails enthalten für alle Segmenttypen die Zielgruppengröße nach dem universellen ID-Typ und nach dem Gerätetyp, der von Cookies oder Geräte-IDs verfolgt wird.

## So wählen Sie eine universelle ID-Zielgruppe in Ihren Platzierungen aus

>[!NOTE]
>
>Die Zielgruppen-ID-Typen in einer Live-Platzierung können nicht geändert werden. Bei Bedarf können Sie eine Live-Platzierung duplizieren und die Zielgruppen-ID-Typen in der neuen Platzierung ändern.

Gehen Sie in einer neuen, geplanten oder pausierten Platzierung wie folgt vor:

1. Geben Sie im Abschnitt [!UICONTROL Geo-Targeting] die geografischen Gebiete an, die Sie ansprechen möchten. Jeder universelle ID-Partner ermöglicht das Targeting von Benutzern nur in bestimmten geografischen Gebieten, und in den [!UICONTROL Targeting] Einstellungen sind nur geeignete ID-Typen verfügbar.

1. Gehen Sie im Abschnitt [!UICONTROL Audience Targeting] wie folgt vor:

   1. Wählen Sie in der [!UICONTROL Included Audiences] das Segment aus, für das Benutzerdaten in universelle IDs konvertiert wurden.

      Sie können bei Bedarf weitere Segmente einbeziehen.

   1. In den [!UICONTROL Targeting] Einstellungen:

      1. Wählen Sie den universellen ID-Typ für das Targeting aus.

         Die Einstellung umfasst die Optionen &quot;[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID]&quot;, die die Unteroptionen &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot; und &quot;[!UICONTROL Unified ID2.0]&quot; enthalten können. Die ausgewählten geografischen Ziele bestimmen die verfügbaren Unteroptionen.

         Sie können sowohl &quot;[!UICONTROL Legacy IDs]&quot; als auch &quot;[!UICONTROL Universal ID]&quot; auswählen, aber Sie können nur einen universellen ID-Typ pro Platzierung auswählen. Wenn Sie sowohl ältere als auch universelle IDs auswählen, erhalten universelle IDs Vorrang für Gebote.

      1. (Falls erforderlich) Akzeptieren Sie die Nutzungsbedingungen für die Verwendung universeller IDs.

         Bevor Sie Daten in einen neuen ID-Typ konvertieren können, muss ein Benutzer im DSP-Konto die Nutzungsbedingungen akzeptieren. Die Bedingungen dürfen nur einmal pro ID-Typ und Konto akzeptiert werden.

Siehe &quot;[Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md).

## Best Practices für Tests und Datenvalidierung

Verwenden Sie die folgenden Best Practices für [!DNL RampID] und ID5-basierte Segmente, für die Adobe Analytics-Messungen verfügbar sind.

* Etwa 24 Stunden nach der Aktivierung eines Segments überprüfen Sie die Anzahl der konvertierten IDs für das Segment unter [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Wenn die Anzahl der IDs unerwartet ist, wenden Sie sich an Ihr Adobe-Account-Team.

  Weitere Informationen [, wie die Segmentzahlen variieren können, finden Sie unter „Datenabweichungen zwischen E-Mail](#universal-ids-data-variances)IDs und universellen IDs“.

* Vorhandene Pakete und Platzierungen nicht ändern. Wenn Sie jedoch kein inkrementelles Budget haben, um universelle IDs zu testen, reduzieren Sie die ursprünglichen Budgets, um die Tests zu finanzieren.

* Kopieren Sie Ihre ursprünglichen Pakete und Platzierungen, passen Sie die Budgets auf der Grundlage der Größe des Tests an, ändern Sie die Zielgruppen so, dass [!DNL RampID] Segmente (für authentifizierte Benutzer) oder ID5-basierte Segmente (für nicht authentifizierte Benutzer) verwendet werden, und überprüfen Sie, ob die neuen Pakete und Platzierungen ihr gesamtes Budget verwenden.

   * Um die Leistung universeller ID-basierter Segmente mit der Leistung von Platzierungen zu vergleichen, die auf andere Zielgruppenkennungen wie Cookies oder Mobile-Advertising-IDs abzielen, erstellen Sie eine Kampagne mit einer separaten universellen ID-basierten Platzierung und einer Legacy-ID-basierten Platzierung.

     Für einen vollständigen Retargeting-Test richten Sie sowohl RampIDs auf authentifizierte Benutzer als auch ID5s auf nicht authentifizierte Benutzer aus.

     Die beste Leistung zu erzielen, sollte nicht der primäre Vergleich sein. Bestimmen Sie stattdessen, welche IDs gut skaliert werden können, was später Informationen zu Optimierungs- und Budgetzuweisungen liefern kann. Das langfristige Ziel besteht darin, verlorene Impressionen und Website-Traffic auszugleichen, wenn Cookies veraltet sind.

   * Um die gesamte Browser-Reichweite zu vergleichen, wählen Sie universelle ID-basierte Segmente und veraltete ID-basierte Segmente in derselben Platzierung aus. Verwenden Sie dieselben Kampagneneinstellungen wie für den vorherigen Anwendungsfall, mit der Ausnahme, dass Sie das Kampagnenbudget nicht aufteilen müssen.

     Bietervorteil wird universellen IDs zugewiesen, aber Legacy-IDs erhalten Gebote, wenn keine universellen IDs verfügbar sind. Vergleichen Sie die Reichweite in verschiedenen Browsern (einschließlich Chrome, Safari und Mozilla).

     >[!NOTE]
     >
     >Die Frequenzlimitierung gilt für eine einzelne ID. Wenn ein(e) Benutzende(r) mehrere ID-Typen hat, können Sie diesen/r Benutzenden besser erreichen als erwartet.

* Denken Sie daran, dass die Reichweite authentifizierter Zielgruppensegmente naturgemäß kleiner ist als die Reichweite Cookie-basierter Segmente, und dass die Verwendung zusätzlicher Targeting-Optionen Ihre Reichweite weiter verringert. Seien Sie vorsichtig bei der Verwendung von granularem Targeting, insbesondere indem Sie mehrere Ziele mit AND-Anweisungen verbinden.

## Datenabweichungen zwischen E-Mail-IDs und universellen IDs {#universal-ids-data-variances}

### Zulässige Varianzniveaus

Die Übersetzungsrate von gehashten E-Mail-Adressen in universelle IDs sollte größer als 90 % sein. Die Übersetzungsrate insbesondere für [!DNL RampIDs] sollte 95 % betragen, wenn alle gehashten E-Mail-Adressen eindeutig sind. Wenn Sie beispielsweise 100 gehashte E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mindestens 95 [!DNL RampIDs] oder mehr als 90 andere Arten von universellen IDs übersetzt werden. Eine niedrigere Übersetzungsrate kann auf ein Problem hinweisen. Mögliche Erklärungen finden Sie unter [Ursachen der ]#universal-ids-data-variances-causes“.

Wenden Sie sich [!DNL RampIDs] an Ihr Adobe-Account-Team, wenn Sie weitere Informationen benötigen, falls die Übersetzungsrate unter 70 % liegt.

### Ursachen der Varianz {#universal-ids-data-variances-causes}

* Alle Segmente:

  Die Segment-zu-Gerät-Zählung verwendet ein probabilistisches Modell, das eine Fehlervarianz von +/- 5 % aufweist. Dies bedeutet, dass die Zielgruppenanzahl um 5 % überschätzt oder unterschätzt werden kann.

* Hash-E-Mail-IDs, die in [!DNL RampIDs] übersetzt wurden:

   * Wenn mehrere Profile dieselbe E-Mail-ID verwenden, kann die DSP-Segmentanzahl niedriger sein als die Profilanzahl in Ihrer Kundendatenplattform. In Adobe Photoshop können Sie beispielsweise ein Unternehmenskonto und ein Privatkonto mit einer einzigen E-Mail-ID erstellen. Wenn jedoch beide Profile derselben Person angehören, werden die Profile einer einzelnen E-Mail-ID und entsprechend einer [!DNL RampID] zugeordnet.

   * Ein [!DNL RampID] kann auf einen neuen Wert aktualisiert werden. Wenn [!DNL LiveRamp] eine E-Mail-ID nicht erkennt oder sie keiner vorhandenen [!DNL RampID] in der Datenbank zuordnen kann, weist sie der E-Mail-ID einen neuen [!DNL RampID] zu. Wenn der Benutzer die E-Mail-ID in Zukunft einem anderen [!DNL RampID] zuordnen oder weitere Informationen über dieselbe E-Mail-ID sammeln kann, aktualisiert er die [!DNL RampID] auf einen neuen Wert. [!DNL LiveRamp] bezieht sich auf diese Aktion als Upgrade von einer „abgeleiteten“ [!DNL RampID] auf eine „gepflegte“ [!DNL RampID]. DSP erhält jedoch keine Zuordnungen zwischen abgeleiteten und verwalteten [!DNL RampIDs] und kann daher nicht die vorherige Version der RampID aus dem DSP-Segment entfernen. In diesem Fall kann die Segmentanzahl größer als die Profilanzahl sein.

     Beispiel: Ein Benutzer meldet sich bei der [!DNL Adobe]-Website an und besucht die Photoshop-Seite. Wenn [!DNL LiveRamp] noch keine Informationen über die E-Mail-ID hat, weisen sie ihr einen abgeleiteten [!DNL RampID] zu, z. B. D123. Fünfzehn Tage später besucht der Benutzer dieselbe Seite, aber [!DNL LiveRamp] hat die [!DNL RampID] in diesen 15 Tagen aktualisiert und die [!DNL RampID] auf M123 neu zugewiesen. Obwohl das Segment &quot;Photoshop Enthusiast“ der Kundendatenplattform nur eine E-Mail-ID für den Benutzer hat, verfügt das DSP-Segment über zwei RampIDs: D123 und M123.

## Fehlerbehebung

Wenn Sie keine Benutzeranzahl sehen oder Ihre Zielgruppengrößen niedrig sind, überprüfen Sie Folgendes:

* Wenn Sie [!DNL Flashtalking] oder [!DNL Google Campaign Manager 360] Anzeigen verwenden, stellen Sie sicher, dass die Clickthrough-URLs Ihrer Anzeigen mit den richtigen Makros angehängt werden. Siehe Makros für [[!DNL Flashtalking] Anzeigen](/help/integrations/analytics/macros-flashtalking.md) und [[!DNL Google Campaign Manager 360] Anzeigen](/help/integrations/analytics/macros-google-campaign-manager.md).

* Stellen Sie sicher, dass auf Ihrer Website der richtige, universelle Partner-spezifische ID-Code implementiert ist, um Ereignisse vor Ort und Anzeigen-Expositionen abzugleichen. Arbeiten Sie bei Bedarf mit Ihrem [!DNL LiveRamp] oder [!DNL ID5].

* (Für [!DNL RampIDs]- und [!DNL UID 2.0]-IDs) Vergewissern Sie sich, dass Ihre [DSP-Datenquelle korrekt konfiguriert ist ](/help/dsp/audiences/sources/source-manage.md#source-settings) dass die Benutzerzahlen für die generierten Zielgruppensegmente ausgefüllt sind.

* Wenn Sie weniger Reichweite haben als erwartet, stellen Sie sicher, dass die Logik des Zielgruppensegments nicht zu detailliert ist.

* Stellen Sie sicher, dass Ihre Kampagnen-, Paket- und Platzierungseinstellungen korrekt sind.<!-- wording-->

Wenn Sie das Problem nicht beheben können, wenden Sie sich an Ihr Adobe-Account-Team.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](/help/dsp/audiences/sources/source-manage.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md)
>* [Importieren Sie authentifizierte Segmente manuell aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
