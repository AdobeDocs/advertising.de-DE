---
title: Unterstützung für die Aktivierung von universellen IDs
description: Erfahren Sie mehr über die Unterstützung für den Import Ihrer universellen ID-Segmente, die Erstellung benutzerdefinierter Segmente zur Verfolgung universeller IDs und die Konvertierung anderer Benutzer-IDs in Erstanbietersegmente in universelle IDs für das Targeting von Cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Unterstützung für die Aktivierung von universellen IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta-Funktion*

DSP unterstützt benutzerbasierte, universelle IDs für Cookies, ein einzelnes Gerät (nicht geräteübergreifendes Targeting), das über digitale, von DSP unterstützte Formate hinweg verwendet wird.

* Sie können Ihre authentifizierte [[!DNL LiveRamp] [!DNL RampIDs]] manuell direkt an DSP senden, indem Sie das Dashboard [!DNL LiveRamp] [!DNL Connect] verwenden. Siehe &quot;[Manuelles Importieren authentifizierter Segmente aus  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP können Erstanbietersegmente erfassen, die aus in Ihrer Kundendatenplattform (CDP) erstellten Hash-E-Mail-IDs bestehen, und sie in [!DNL LiveRamp] [!DNL RampIDs] und [!DNL Unified ID 2.0 (UID2.0)] IDs konvertieren. Weitere Informationen zu den unterstützten Kundendatenplattformen, den verfügbaren Funktionen für die einzelnen unterstützten universellen ID-Typen und den zugehörigen Workflows finden Sie unter &quot;[Über Zielgruppenquellen von Erstanbietern](/help/dsp/audiences/sources/source-about.md)&quot;.

* Sie können benutzerdefinierte Segmente erstellen, die Benutzer verfolgen, die mit universellen IDs für ID5 verknüpft sind, die Anzeigen von Desktop- und Mobilgeräten erhalten und bestimmte Webseiten besuchen. ID5 verwendet ein probabilistisches Modell, um eine ID zuzuweisen, die aus verschiedenen Benutzersignalen und Browsersignalen abgeleitet wurde. Anweisungen finden Sie unter &quot;[Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md)&quot;.

* Drittanbietersegmente einiger Anbieter können zusätzlich zu den von Cookies oder Geräte-IDs verfolgten Benutzern automatisch universelle IDs enthalten. Beispielsweise können Segmente von [!DNL Eyeota] automatisch ID5-IDs enthalten, und Segmente von [!DNL Lotame] können UID2.0-IDs enthalten. Die Segmentdetails enthalten die Größe für jeden Typ. Für jedes Segment gilt die übliche Nutzungsgebühr, die neben dem Segmentnamen angegeben wird. Für die ID5-IDs werden keine zusätzlichen Gebühren erhoben.

## Berichterstellung nach dem universellen ID-Typ

* **Benutzerspezifische Berichte:** In benutzerspezifischen Berichten sind Kosten-, Impression-, Klick-, Konversions- und Häufigkeitsdaten nach dem universellen ID-Typ verfügbar.

* **[!DNL Analytics]Berichte:** Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), die alle erforderlichen Schritte implementiert haben, können Durchsichtskonversionen nach universellen ID-Typen in [!DNL Analytics] sehen.

  >[!IMPORTANT]
  >
  >Stellen Sie für eine ordnungsgemäße Konversionszuordnung sicher, dass die Clickthrough-URLs für Ihre Anzeigen sowohl die [EF ID als auch die AMO ID](/help/integrations/analytics/ids.md) enthalten.

* **Segmentdetails:** Die Segmentdetails enthalten für alle Segmenttypen die Zielgruppengröße nach dem universellen ID-Typ und nach dem Gerätetyp, der von Cookies oder Geräte-IDs verfolgt wird.

## Targeting einer universellen ID-Zielgruppe in Ihren Platzierungen

>[!NOTE]
>
>Sie können die zielgerichteten ID-Typen in einer Live-Platzierung nicht ändern. Bei Bedarf können Sie eine Live-Platzierung duplizieren und die Targeting-ID-Typen in der neuen Platzierung ändern.

Führen Sie in einer neuen, geplanten oder ausgesetzten Platzierung folgende Schritte aus:

1. Geben Sie im Abschnitt [!UICONTROL Geo-Targeting] die geografischen Gebiete an, die als Ziel ausgewählt werden sollen. Jeder universelle ID-Partner ermöglicht das Benutzer-Targeting nur in bestimmten geografischen Bereichen, und in den Einstellungen für [!UICONTROL Targeting] sind nur infrage kommende ID-Typen verfügbar.

1. Gehen Sie im Abschnitt [!UICONTROL Audience Targeting] wie folgt vor:

   1. Wählen Sie in der Einstellung &quot;[!UICONTROL Included Audiences]&quot;das Segment aus, für das Benutzerdaten in universelle IDs konvertiert wurden.

      Sie können bei Bedarf weitere Segmente hinzufügen.

   1. In den Einstellungen für [!UICONTROL Targeting] :

      1. Wählen Sie den universellen ID-Typ aus, der als Ziel dienen soll.

         Die Einstellung enthält die Optionen &quot;[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID]&quot;, die die Unteroptionen &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot;und &quot;[!UICONTROL Unified ID2.0]&quot;enthalten können. Die ausgewählten geografischen Ziele bestimmen die verfügbaren Unteroptionen.

         Sie können sowohl &quot;[!UICONTROL Legacy IDs]&quot;als auch &quot;[!UICONTROL Universal ID]&quot;auswählen, Sie können jedoch nur einen Typ der universellen ID pro Platzierung auswählen. Wenn Sie sowohl Legacy-IDs als auch universelle IDs auswählen, wird den universellen IDs die Gebotseinstellung vorgezogen.

      1. (Bei Bedarf) Akzeptieren Sie die Nutzungsbedingungen für die Verwendung von universellen IDs.

         Bevor Sie Daten in einen neuen ID-Typ konvertieren können, muss ein Benutzer im DSP die Nutzungsbedingungen akzeptieren. Die Bedingungen dürfen pro ID-Typ und Konto nur einmal akzeptiert werden.

Siehe &quot;[Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Best Practices für Tests und Datenvalidierung

Verwenden Sie die folgenden Best Practices für [!DNL RampID]-basierte Segmente und ID5-basierte Segmente, für die eine Adobe Analytics-Messung verfügbar ist.

* Ungefähr 24 Stunden nach der Aktivierung eines Segments überprüfen Sie die konvertierte ID-Anzahl für das Segment in [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Wenn die ID-Anzahl unerwartet ist, wenden Sie sich an Ihr Adobe-Account-Team.

  Weitere Informationen dazu, wie die Segmentzählung variieren kann, finden Sie unter &quot;[Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

* Ändern Sie Ihre vorhandenen Pakete und Platzierungen nicht. Wenn Sie jedoch über kein inkrementelles Budget zum Testen universeller IDs verfügen, reduzieren Sie die ursprünglichen Budgets zur Finanzierung der Tests.

* Kopieren Sie Ihre ursprünglichen Pakete und Platzierungen, passen Sie die Budgets an die Größe des Tests an, ändern Sie die Zielgruppen so, dass sie [!DNL RampID]-basierte Segmente (für authentifizierte Benutzer) oder ID5-basierte Segmente (für nicht authentifizierte Benutzer) verwenden, und überprüfen Sie, ob die neuen Pakete und Platzierungen ihr ganzes Budget ausgeben.

   * Um die Leistung universeller ID-basierter Segmente mit der Leistung von Platzierungen zu vergleichen, die auf andere Zielgruppen-IDs abzielen, z. B. Cookies oder mobile Werbe-IDs, erstellen Sie eine Kampagne mit einer separaten universellen ID-basierten Platzierung und einer Legacy-ID-basierten Platzierung.

     Für einen vollständigen Retargeting-Test sollten Sie sowohl RampIDs für authentifizierte Benutzer als auch ID5s für nicht authentifizierte Benutzer als Ziel auswählen.

     Die beste Leistung zu erzielen sollte nicht der Hauptvergleich sein. Bestimmen Sie stattdessen, welche IDs gut skaliert werden, was später Ihre Optimierung und Budgetzuweisungen beeinflussen kann. Das langfristige Ziel besteht darin, verlorene Impressionen und den Site-Traffic auszugleichen, wenn Cookies veraltet sind.

   * Um die gesamte Browserreichweite zu vergleichen, richten Sie universelle ID-basierte Segmente und ältere ID-basierte Segmente an derselben Platzierung an. Verwenden Sie dieselben Kampagneneinstellungen wie im vorherigen Anwendungsfall, allerdings müssen Sie das Kampagnenbudget nicht aufteilen.

     Universal-IDs erhalten eine Gebotseinstellung, ältere IDs erhalten jedoch Angebote, wenn keine universellen IDs verfügbar sind. Vergleichen Sie die Reichweite in verschiedenen Browsern (einschließlich Chrome, Safari und Mozilla).

     >[!NOTE]
     >
     >Die Frequenzlimitierung gilt für eine einzelne ID. Wenn ein Benutzer mehrere ID-Typen hat, erreichen Sie diesen Benutzer möglicherweise mehr als erwartet.

* Beachten Sie, dass die Reichweite für authentifizierte Zielgruppensegmente von Natur aus kleiner ist als die Reichweite für Cookie-basierte Segmente, und dass die Verwendung zusätzlicher Targeting-Optionen Ihre Reichweite weiter verringert. Achten Sie auf die Verwendung von granularem Targeting, insbesondere durch die Verbindung mehrerer Ziele mit AND-Anweisungen.

## Datenabweichungen zwischen E-Mail-IDs und universellen IDs {#universal-ids-data-variances}

### Zulässige Varianzstufen

Die Übersetzungsrate von Hash-E-Mail-Adressen in universelle IDs sollte über 90 % liegen. Insbesondere für [!DNL RampIDs] sollte die Übersetzungsrate 95 % betragen, wenn alle Hash-E-Mail-Adressen eindeutig sind. Wenn Sie beispielsweise 100 Hash-E-Mail-Adressen von Ihrer Kundendatenplattform senden, sollten diese in mindestens 95 [!DNL RampIDs] oder mehr als 90 andere Typen universeller IDs übersetzt werden. Eine niedrigere Übersetzungsrate kann auf ein Problem hinweisen. Mögliche Erklärungen finden Sie unter &quot;[Varianzursachen](#universal-ids-data-variances-reasons&quot;.

Wenden Sie sich für [!DNL RampIDs] an Ihr Adobe Account Team, um weitere Informationen zu erhalten, wenn die Übersetzungsraten unter 70 % liegen.

### Ursachen von Abweichungen {#universal-ids-data-variances-causes}

* In ID5-IDs übersetzte Hash-E-Mail-IDs:

  Das probabilistische Modell weist eine Fehlervarianz von +/- 5 % auf. Das bedeutet, dass die Zielgruppenanzahl dadurch um 5 % überschätzt oder unterschätzt werden kann.

* Hash-E-Mail-IDs, übersetzt in [!DNL RampIDs]:

   * Wenn mehrere Profile dieselbe E-Mail-ID verwenden, kann die Anzahl der DSP Segmente niedriger sein als die Anzahl der Profile in Ihrer Kundendatenplattform. In Adobe Photoshop können Sie beispielsweise ein Unternehmenskonto und ein persönliches Konto mit einer einzelnen E-Mail-Adresse erstellen. Wenn jedoch beide Profile derselben Person angehören, werden die Profile einer E-Mail-ID und entsprechend einem [!DNL RampID] zugeordnet.

   * Ein [!DNL RampID] kann auf einen neuen Wert aktualisiert werden. Wenn [!DNL LiveRamp] eine E-Mail-ID nicht erkennt oder sie nicht einer vorhandenen [!DNL RampID] in der Datenbank zuordnen kann, wird der E-Mail-ID eine neue [!DNL RampID] zugewiesen. Wenn sie zukünftig die E-Mail-ID einem anderen [!DNL RampID] zuordnen oder mehr Informationen über dieselbe E-Mail-ID erfassen können, aktualisieren sie [!DNL RampID] auf einen neuen Wert. [!DNL LiveRamp] bezieht sich auf diese Aktion, da ein Upgrade von einem &quot;abgeleiteten&quot; [!DNL RampID] auf einen &quot;gepflegten&quot; [!DNL RampID] durchgeführt wird. DSP erhält jedoch keine Zuordnungen zwischen abgeleitetem und verwaltetem [!DNL RampIDs] und kann daher die vorherige Version der RampID nicht aus dem DSP Segment entfernen. In diesem Fall kann die Segmentanzahl größer als die Profilanzahl sein.

     Beispiel: Ein Benutzer meldet sich bei der [!DNL Adobe] -Website an und besucht die Photoshop-Seite. Wenn [!DNL LiveRamp] keine vorhandenen Informationen über die E-Mail-ID hat, wird ihr eine abgeleitete [!DNL RampID], z. B. D123, zugewiesen. Fünfzehn Tage später besucht der Benutzer dieselbe Seite, aber [!DNL LiveRamp] hat die [!DNL RampID] in diesen 15 Tagen aktualisiert und die [!DNL RampID] der M123 neu zugewiesen. Obwohl das Segment &quot;Photoshop Enthusiast&quot;der Kundendatenplattform nur eine E-Mail-ID für den Benutzer hat, verfügt das DSP-Segment über zwei Ramp-IDs: D123 und M123.

## Fehlerbehebung

Wenn keine Benutzerzahlen angezeigt werden oder Ihre Zielgruppengrößen niedrig sind, überprüfen Sie Folgendes:

* Wenn Sie [!DNL Flashtalking] - oder [!DNL Google Campaign Manager 360] -Anzeigen verwenden, stellen Sie sicher, dass die Clickthrough-URLs Ihrer Anzeigen mit den richtigen Makros angehängt sind. Siehe Makros für [[!DNL Flashtalking] Anzeigen](/help/integrations/analytics/macros-flashtalking.md) und [[!DNL Google Campaign Manager 360] Anzeigen](/help/integrations/analytics/macros-google-campaign-manager.md).

* Stellen Sie sicher, dass auf Ihrer Website der korrekte, universelle ID-Partner-spezifische Code implementiert ist, um On-site-Ereignisse und Anzeigenbelichtungen abzugleichen. Arbeiten Sie bei Bedarf mit Ihrem [!DNL LiveRamp] - oder [!DNL ID5] -Vertreter zusammen.

* (Für [!DNL RampIDs] - und [!DNL UID 2.0] -IDs) Stellen Sie sicher, dass Ihre [DSP-Datenquelle richtig konfiguriert ist](/help/dsp/audiences/sources/source-manage.md#source-settings) und dass die Benutzerzahlen für die generierten Zielgruppensegmente aufgefüllt sind.

* Wenn Ihre Reichweite geringer ist als erwartet, überprüfen Sie, ob die Zielgruppensegmentlogik nicht zu detailliert ist.

* Vergewissern Sie sich, dass die Einstellungen für Kampagne, Paket und Platzierung korrekt sind.<!-- wording-->

Wenn Sie das Problem nicht beheben können, wenden Sie sich an Ihr Adobe-Account-Team.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md)
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](/help/dsp/audiences/sources/source-manage.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md)
>* [ Manuelles Importieren authentifizierter Segmente aus  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
