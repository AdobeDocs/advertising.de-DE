---
title: Unterstützung für die Aktivierung universeller IDs
description: Erfahren Sie mehr über die Unterstützung für das Importieren Ihrer universellen ID-Segmente, das Erstellen benutzerdefinierter Segmente zum Nachverfolgen universeller IDs und das konvertieren anderer User-IDs in Ihren Erstanbietersegmenten in universelle IDs für Cookie-lose Targeting.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Unterstützung für die Aktivierung universeller IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta Funktion*

DSP unterstützt personenbasierte, universelle IDs für cookielose, einzelne Device (nicht Device übergreifende) Targeting in digitalen Formaten, die von DSP unterstützt werden.

* Sie können Ihre authentifizierten [[!DNL LiveRamp] [!DNL RampIDs]] direkt auf DSP über [!DNL LiveRamp] [!DNL Connect] Dashboard. Siehe &quot;[Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).“

* DSP kann Ihre First-Party-Segmente aufnehmen, die aus gehashten E-Mail-IDs bestehen, die in Ihrer Kundendatenplattform (CDP) erstellt wurden, und sie in konvertieren. [!DNL LiveRamp] [!DNL RampIDs] und [!DNL Unified ID 2.0 (UID2.0)] IDs. Weitere Informationen zu den unterstützten Kundendatenplattformen, den verfügbaren Funktionen für jeden unterstützten universellen ID-Typ und die zugehörigen Workflows finden Sie unter &quot;[Über First-Party-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md).“

* Sie können benutzerdefinierte Segmente erstellen, die Benutzer verfolgen, die mit universellen ID5-IDs verknüpft sind, die Anzeigen von Desktop- und Mobilgeräten ausgesetzt sind und bestimmte Web-Seiten besuchen. ID5 verwendet ein probabilistisches Modell, um eine ID zuzuweisen, die aus verschiedenen Benutzersignalen und Browser-Signalen abgeleitet wird. Anweisungen finden Sie unter &quot;[Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md).“

* Drittanbietersegmente einiger Anbieter können zusätzlich zu den durch Cookies oder Device IDs verfolgten Benutzern automatisch universelle IDs enthalten. Zum Beispiel können Segmente aus [!DNL Eyeota] automatisch ID5-IDs enthalten, und Segmente aus [!DNL Lotame] können UID2.0-IDs enthalten. Zu den Segment Details gehört die Größe für jeden Typ. Es fällt das übliche Nutzungsentgelt für jede Segment an, das neben dem Segment Namen angegeben ist; Für die ID5-IDs werden keine zusätzlichen Gebühren erhoben.

## Berichterstellung nach universellem ID-Typ

* **Benutzerdefinierte Berichte:** Kosten-, Impression-, Klick-, Konversion- und Häufigkeit-Daten nach universellem ID-Typ sind in benutzerspezifischen Berichten verfügbar.

* **[!DNL Analytics]Berichte:** Werbetreibende, die [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) alle erforderlichen Schritte implementiert haben, können Ansicht-Through-Conversions nach universellem ID-Typ in [!DNL Analytics]sehen.

  >[!IMPORTANT]
  >
  >Stellen Sie für eine ordnungsgemäße Konversion Attribution sicher, dass die Clickthrough-URLs für Ihre Anzeigen sowohl die [EF-ID als auch die AMO-ID](/help/integrations/analytics/ids.md) enthalten.

* **Segment Details:** Bei allen Segment Typen umfassen die Segment Details die Zielgruppe Größe nach universellem ID-Typ und nach den Device-Typ, die von Cookies oder Device-IDs nachverfolgt werden.

## So Target Sie eine universelle ID-Audience in Ihren Platzierungen

>[!NOTE]
>
>Sie können die Typen der Ziel-IDs nicht in einer Live-Platzierung ändern. Bei Bedarf können Sie eine Live-Platzierung Duplikat und die Typen der Ziel-IDs im neuen Platzierung ändern.

Gehen Sie in einer neuen, geplanten oder angehaltenen Platzierung wie folgt vor:

1. In der [!UICONTROL Geo-Targeting] geben Sie die geografischen Gebiete an, auf die Sie abzielen möchten. Jeder universelle ID-Partner ermöglicht das Benutzer-Targeting nur in bestimmten geografischen Gebieten, und in der sind nur geeignete ID-Typen verfügbar. [!UICONTROL Targeting] Einstellungen.

1. Führen Sie in diesem [!UICONTROL Audience Targeting] Abschnitt die folgenden Schritte aus:

   1. Wählen Sie in der [!UICONTROL Included Audiences] Einstellung die Segment aus, für die User Daten in universelle IDs konvertiert wurden.

      Sie können bei Bedarf weitere Segmente einschließen.

   1. In den [!UICONTROL Targeting] Einstellungen:

      1. Wählen Sie den universellen ID-Typ für das Targeting aus.

         Die Einstellung umfasst die Optionen &quot;&quot;[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID],“ die die Unteroptionen enthalten können &quot;[!UICONTROL ID5],“ &quot;[!UICONTROL RampID]und &quot;[!UICONTROL Unified ID2.0].“ Die ausgewählten geografischen Ziele bestimmen die verfügbaren Unteroptionen.

         Sie können beide auswählen[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID],“, Sie können jedoch nur einen Typ der universellen ID pro Platzierung auswählen. Wenn Sie sowohl ältere als auch universelle IDs auswählen, erhalten universelle IDs Vorrang für Gebote.

      1. (Falls erforderlich) Akzeptieren Sie die Nutzungsbedingungen für die Verwendung universeller IDs.

         Bevor Sie Daten in einen neuen ID-Typ konvertieren können, muss ein Benutzer im DSP-Konto die Vereinbarung über die Nutzungsbedingungen akzeptieren. Die Begriffe dürfen nur einmal pro ID-Typ und pro Konto akzeptiert werden.

Siehe &quot;[Platzierung Einstellungen](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Best Practices für Tests und Daten Validierung

Verwenden Sie die folgenden Best Practices für [!DNL RampID]ID5-basierte Segmente und ID5-basierte Segmente, für die Adobe Analytics Messungen verfügbar sind.

* Überprüfen Sie etwa 24 Stunden nach der Aktivierung einer Segment die konvertierte ID-Anzahl für die Segment innerhalb von [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Wenn die ID-Anzahl unerwartet ist, wenden Sie sich an das Adobe Systems Account-Team.

  Weitere Informationen darüber, wie die Segment variieren kann, finden Sie unter &quot;[Ursachen für Daten Abweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;.

* Ändern Sie Ihre vorhandenen Pakete und Platzierungen nicht. Wenn Sie jedoch kein zusätzliches Budget für die Test universeller IDs haben, reduzieren Sie die ursprünglichen Budgets, um die Tests zu finanzieren.

* Passen Sie Kopie Ihrer ursprünglichen Pakete und Platzierungen die Budgets basierend auf der Größe der Test an, ändern Sie die Zielgruppen so, dass sie -basierte Segmente (für authentifizierte Benutzer) oder ID5-basierte Segmente (für nicht authentifizierte Benutzer) verwenden [!DNL RampID], und überprüfen Sie, ob die neuen Pakete und Platzierungen ihre vollen Budgets ausgeben.

   * Um die Leistung universeller ID-basierter Segmente mit der Leistung von Platzierungen Targeting anderen Zielgruppe-IDs, wie z. B. Cookies oder Mobile Advertising-IDs, zu vergleichen, erstellen Sie eine Kampagne mit einem separaten universellen ID-basierten Platzierung und einem Legacy-ID-basierten Platzierung.

     Für ein vollständiges Retargeting Test Target-Komponente Sie sowohl RampIDs für authentifizierte Benutzer als auch ID5s für nicht authentifizierte Benutzer.

     Das Erzielen der besten Leistung sollte nicht der primäre Vergleich sein. Bestimmen Sie stattdessen, welche IDs gut skaliert werden können, was später Informationen zu Optimierungs- und Budgetzuweisungen liefern kann. Langfristiges Ziel ist es, verlorene Impressionen und Sitetraffic durch veraltete Cookies wettzumachen.

   * Zum Vergleich der gesamten Browser Reichweite Target-Komponente Sie universelle ID-basierte Segmente und ältere ID-basierte Segmente auf derselben Platzierung. Verwenden Sie dieselben Kampagne Einstellungen wie im vorherigen Anwendungsfall, mit der Ausnahme, dass Sie das Kampagne Budget nicht aufteilen müssen.

     Universelle IDs werden bevorzugt, aber Legacy-IDs erhalten Gebote, wenn keine universellen IDs verfügbar sind. Vergleichen Sie die Reichweite in verschiedenen Browsern (einschließlich Chrom, Safari und Mozilla).

     >[!NOTE]
     >
     >Das Frequency Capping gilt für eine Kontakt-ID. Wenn ein(e) Benutzende(r) mehrere ID-Typen hat, können Sie diesen/r Benutzenden besser erreichen als erwartet.

* Denken Sie daran, dass die Reichweite für authentifizierte Zielgruppe-Segmente naturgemäß kleiner ist als die Reichweite für Cookie-basierte Segmente und dass die Verwendung zusätzlicher Targeting-Optionen Ihre Reichweite weiter verringert. Gehen Sie bei der Verwendung von granularen Targeting umsichtig vor, insbesondere durch Verknüpfen mehrerer Ziele mit UND-Anweisungen.

## Ursachen für Daten Abweichungen zwischen E-Mail-IDs und universellen IDs {#universal-ids-data-variances}

* In ID5-IDs übersetzte E-Mail-IDs mit Hash-Wert:

  Das probabilistische Modell hat einen Fehler Varianz von +/- 5%. Dies bedeutet, dass die Anzahl der Zielgruppe um 5 % über- oder unterschätzt werden kann.

* E-Mail-IDs mit Hash übersetzt in [!DNL RampIDs]:

   * Wenn mehrere Profile dieselbe E-Mail-ID verwenden, kann die DSP Segment-Anzahl niedriger sein als die Profil-Anzahl in Ihrer Kundendatenplattform. In Adobe Photoshop können Sie beispielsweise eine Firma Konto und eine persönliche Konto mit einer einzigen E-Mail-ID erstellen. Wenn jedoch beide Profile zu derselben Person gehören, werden die Profile einer E-Mail-ID und entsprechend einer [!DNL RampID]zugeordnet.

   * A [!DNL RampID] kann auf einen neuen Wert hochgestuft werden. Wenn [!DNL LiveRamp] eine E-Mail-ID nicht erkannt wird oder sie nicht einer vorhandenen [!DNL RampID] in der Datenbank zugeordnet werden kann, wird der E-Mail-ID eine neue [!DNL RampID] zugewiesen. Wenn sie in Zukunft die E-Mail-ID einer anderen [!DNL RampID] zuordnen oder weitere Informationen über dieselbe E-Mail-ID sammeln können, führen sie ein Upgrade auf [!DNL RampID] einen neuen Wert durch. [!DNL LiveRamp]bezeichnet diese Aktion als Upgrade von einer &quot;abgeleiteten&quot; [!DNL RampID] zu einer &quot;gepflegten&quot;. [!DNL RampID] DSP erhält jedoch keine Zuordnungen zwischen abgeleitet und verwaltet [!DNL RampIDs] und kann daher die vorherige Version der RampID nicht aus dem DSP Segment entfernen. In diesem Fall kann die Segmentanzahl größer als die Profilanzahl sein.

     Beispiel: Ein User meldet sich bei der [!DNL Adobe] Website an und besucht die Photoshop Seite. Wenn [!DNL LiveRamp] keine Informationen über die E-Mail-ID vorhanden sind, weisen sie ihr eine abgeleitete [!DNL RampID], z. B. D123. Fünfzehn Tage später besucht die User die gleiche Seite, hat sie [!DNL RampID] aber [!DNL LiveRamp] in diesen 15 Tagen aufgerüstet und der [!DNL RampID] M123 zugewiesen. Obwohl die Segment &quot;Photoshop Enthusiast&quot; der Kundendatenplattform nur eine E-Mail-ID für die User hat, hat die DSP Segment zwei RampIDs: D123 und M123.

## Fehlerbehebung

Wenn keine User angezeigt wird oder Ihre Zielgruppe Größen niedrig sind, überprüfen Sie Folgendes:

* Wenn Sie [!DNL Flashtalking] oder [!DNL Google Campaign Manager 360] Anzeigen hinzufügen und dann sicherstellen, dass die Clickthrough-URLs Ihrer Anzeigen mit den richtigen Makros angehängt werden. Siehe Makros für [[!DNL Flashtalking] Werbeanzeigen](/help/integrations/analytics/macros-flashtalking.md) und [[!DNL Google Campaign Manager 360] Werbeanzeigen](/help/integrations/analytics/macros-google-campaign-manager.md).

* Stellen Sie sicher, dass auf Ihrer Website der richtige, universelle Partner-spezifische ID-Code implementiert ist, um Ereignisse vor Ort und Anzeigen-Expositionen abzugleichen. Arbeiten mit [!DNL LiveRamp] oder [!DNL ID5] ggf. Vertreter.

* (für [!DNL RampIDs] und [!DNL UID 2.0] IDs) Stellen Sie sicher, dass Sie [DSP-Datenquelle ist korrekt konfiguriert](/help/dsp/audiences/sources/source-manage.md#source-settings)und dass die Anzahl der Benutzer für die generierten Zielgruppensegmente angegeben wird.

* Wenn Sie weniger Reichweite haben als erwartet, stellen Sie sicher, dass die Logik des Zielgruppensegments nicht zu detailliert ist.

* Stellen Sie sicher, dass Ihre Kampagne-, Paket- und Platzierung Einstellungen korrekt sind.<!-- wording-->

Wenn Sie das Problem nicht lösen können, wenden Sie sich an das Adobe Systems Account-Team.

>[!MORELIKETHIS]
>
>* [Informationen zu Erstanbieter-Audience Quellen](/help/dsp/audiences/sources/source-about.md)
>* [Audience Quellen verwalten, um universelle ID-Audiences zu aktivieren](/help/dsp/audiences/sources/source-manage.md)
>* [Erstellen und implementieren Sie benutzerdefinierte Segment](/help/dsp/audiences/custom-segment-create.md)
>* [Authentifizierte Segmente manuell aus Importieren [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Über Audience Management](/help/dsp/audiences/audience-about.md)
>* [Platzierung Einstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
