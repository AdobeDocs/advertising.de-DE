---
title: Unterstützung für die Aktivierung von universellen IDs
description: Erfahren Sie mehr über die Unterstützung für den Import Ihrer universellen ID-Segmente, die Erstellung benutzerdefinierter Segmente zur Verfolgung universeller IDs und die Konvertierung anderer Benutzer-IDs in Erstanbietersegmente in universelle IDs für das Targeting von Cookies.
feature: DSP Audiences
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Unterstützung für die Aktivierung von universellen IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta-Funktion*

DSP unterstützt benutzerbasierte, universelle IDs für Cookies, ein einzelnes Gerät (nicht geräteübergreifendes Targeting), das über digitale, von DSP unterstützte Formate hinweg verwendet wird.

* Sie können Ihre authentifizierte Person manuell senden [[!DNL LiveRamp] [!DNL RampIDs]] direkt zu DSP mithilfe der [!DNL LiveRamp] [!DNL Connect] Dashboard. Siehe &quot;[Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP können Erstanbietersegmente erfassen, die aus in Ihrer Kundendatenplattform (CDP) erstellten Hash-E-Mail-IDs bestehen, und sie in konvertieren [!DNL LiveRamp] [!DNL RampIDs] und [!DNL Unified ID 2.0 (UID2.0)] IDs. Weitere Informationen zu den unterstützten Kundendatenplattformen, den verfügbaren Funktionen für jeden unterstützten universellen ID-Typ und den zugehörigen Workflows finden Sie unter &quot;[Über Erstanbieter-Zielgruppenquellen](/help/dsp/audiences/sources/source-about.md).&quot;

* Sie können benutzerdefinierte Segmente erstellen, die Benutzer verfolgen, die mit universellen IDs für ID5 verknüpft sind, die Anzeigen von Desktop- und Mobilgeräten erhalten und bestimmte Webseiten besuchen. ID5 verwendet ein probabilistisches Modell, um eine ID zuzuweisen, die aus verschiedenen Benutzersignalen und Browsersignalen abgeleitet wurde. Weitere Informationen finden Sie unter &quot;[Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md).&quot;

* Drittanbietersegmente von [!DNL Eyeota] und einige andere Anbieter können zusätzlich zu Benutzern, die von Cookies oder Geräte-IDs verfolgt werden, automatisch ID5-IDs enthalten. Die Segmentdetails enthalten die Größe für jeden Typ. Für jedes Segment gilt die übliche Nutzungsgebühr, die neben dem Segmentnamen angegeben wird. Für die ID5-IDs werden keine zusätzlichen Gebühren erhoben.

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## Berichterstellung nach dem universellen ID-Typ

* **Benutzerspezifische Berichte:** Kosten-, Impression-, Klick-, Konversions- und Häufigkeitsdaten nach dem universellen ID-Typ sind in benutzerdefinierten Berichten verfügbar.

* **[!DNL Analytics]Berichte:** Advertiser mit [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) die alle erforderlichen Schritte implementiert haben, können Durchsichtskonvertierungen nach dem universellen ID-Typ in [!DNL Analytics].

* **Segmentdetails:** Bei allen Segmenttypen umfassen die Segmentdetails die Zielgruppengröße nach dem universellen ID-Typ und nach dem Gerätetyp, der von Cookies oder Geräte-IDs verfolgt wird.

## Targeting einer universellen ID-Zielgruppe in Ihren Platzierungen

>[!NOTE]
>
>Sie können die zielgerichteten ID-Typen in einer Live-Platzierung nicht ändern. Bei Bedarf können Sie eine Live-Platzierung duplizieren und die Targeting-ID-Typen in der neuen Platzierung ändern.

Führen Sie in einer neuen, geplanten oder ausgesetzten Platzierung folgende Schritte aus:

* Im [!UICONTROL Geo-Targeting] die zu berücksichtigenden geografischen Gebiete. Jeder universelle ID-Partner ermöglicht das Benutzer-Targeting nur in bestimmten geografischen Bereichen, und in der [!UICONTROL Targeting] -Einstellungen.

* Im [!UICONTROL Audience Targeting] führen Sie folgende Schritte aus:

   * Im [!UICONTROL Included Audiences] -Einstellung wählen Sie das Segment aus, für das Benutzerdaten in universelle IDs konvertiert wurden.

     Sie können bei Bedarf weitere Segmente hinzufügen.

   * Im [!UICONTROL Targeting] -Einstellung wählen Sie den universellen ID-Typ aus, der als Ziel dienen soll.

     Die Einstellung enthält die Optionen &quot;[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID],&quot;die die Unteroptionen &quot;[!UICONTROL ID5], &quot;&quot;[!UICONTROL RampID],&quot; und &quot;[!UICONTROL Unified ID2.0].&quot; Die tatsächlichen Unteroptionen werden durch die ausgewählten geografischen Ziele bestimmt.

     Sie können beide[!UICONTROL Legacy IDs]&quot; und &quot;[!UICONTROL Universal ID],&quot;können Sie jedoch nur einen Typ der universellen ID pro Platzierung auswählen. Wenn Sie sowohl Legacy-IDs als auch universelle IDs auswählen, wird den universellen IDs die Gebotseinstellung vorgezogen.

Siehe &quot;[Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Best Practices für Tests und Datenvalidierung

Verwenden Sie die folgenden Best Practices für [!DNL RampID]-basierte Segmente und ID5-basierte Segmente, für die eine Adobe Analytics-Messung verfügbar ist.

* Ungefähr 24 Stunden nach der Aktivierung eines Segments überprüfen Sie die konvertierte ID-Anzahl für das Segment in [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Wenn die ID-Anzahl unerwartet ist, wenden Sie sich an Ihr Adobe-Account-Team.

  Siehe &quot;[Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs](#universal-ids-data-variances)&quot;, um weitere Informationen darüber zu erhalten, wie die Segmentzahlen variieren können.

* Ändern Sie Ihre vorhandenen Pakete und Platzierungen nicht. Wenn Sie jedoch über kein inkrementelles Budget zum Testen universeller IDs verfügen, reduzieren Sie die ursprünglichen Budgets zur Finanzierung der Tests.

* Kopieren Sie Ihre ursprünglichen Pakete und Platzierungen, passen Sie die Budgets an die Größe des Tests an, ändern Sie die Zielgruppen, die verwendet werden sollen. [!DNL RampID]-basierte Segmente (für authentifizierte Benutzer) oder ID5-basierte Segmente (für nicht authentifizierte Benutzer) und überprüfen, ob die neuen Pakete und Platzierungen ihr ganzes Budget ausgeben.

   * Um die Leistung universeller ID-basierter Segmente mit der Leistung von Platzierungen zu vergleichen, die auf andere Zielgruppen-IDs abzielen, z. B. Cookies oder mobile Werbe-IDs, erstellen Sie eine Kampagne mit einer separaten universellen ID-basierten Platzierung und einer Legacy-ID-basierten Platzierung.

     Die beste Leistung zu erzielen sollte nicht der Hauptvergleich sein. Bestimmen Sie stattdessen, welche IDs gut skaliert werden, was später Ihre Optimierung und Budgetzuweisungen beeinflussen kann. Das langfristige Ziel besteht darin, verlorene Impressionen und den Site-Traffic auszugleichen, wenn Cookies veraltet sind.

   * Um die gesamte Browserreichweite zu vergleichen, richten Sie universelle ID-basierte Segmente und ältere ID-basierte Segmente an derselben Platzierung an. Verwenden Sie dieselben Kampagneneinstellungen wie im vorherigen Anwendungsfall, allerdings müssen Sie das Kampagnenbudget nicht aufteilen.

     Universal-IDs erhalten eine Gebotseinstellung, ältere IDs erhalten jedoch Angebote, wenn keine universellen IDs verfügbar sind. Vergleichen Sie die Reichweite in verschiedenen Browsern (einschließlich Chrome, Safari und Mozilla).

     >[!NOTE]
     >
     >Die Frequenzlimitierung gilt für eine einzelne ID. Wenn ein Benutzer mehrere ID-Typen hat, erreichen Sie diesen Benutzer möglicherweise mehr als erwartet.

* Beachten Sie, dass die Reichweite für authentifizierte Zielgruppensegmente von Natur aus kleiner ist als die Reichweite für Cookie-basierte Segmente, und dass die Verwendung zusätzlicher Targeting-Optionen Ihre Reichweite weiter verringert. Achten Sie auf die Verwendung von granularem Targeting, insbesondere durch die Verbindung mehrerer Ziele mit AND-Anweisungen.

## Ursachen für Datenabweichungen zwischen E-Mail-IDs und universellen IDs {#universal-ids-data-variances}

Es gibt zwei Gründe für die Varianz von Hash-E-Mail-IDs, die in [!DNL RampIDs]:

* Wenn mehrere Profile dieselbe E-Mail-ID verwenden, kann die Anzahl der DSP Segmente niedriger sein als die Anzahl der Profile in Ihrer Kundendatenplattform. In Adobe Photoshop können Sie beispielsweise ein Unternehmenskonto und ein persönliches Konto mit einer einzelnen E-Mail-Adresse erstellen. Wenn jedoch beide Profile demselben Segment angehören, werden die Profile einer E-Mail-ID und entsprechend einer zugeordnet. [!DNL RampID].

* A [!DNL RampID] kann auf einen neuen Wert aktualisiert werden. Wenn [!DNL LiveRamp] erkennt keine E-Mail-ID oder kann sie nicht einer vorhandenen [!DNL RampID] in der Datenbank, weist sie dann eine neue [!DNL RampID] zur E-Mail-ID hinzu. Zukünftig, wenn sie die E-Mail-ID einer anderen zuordnen können [!DNL RampID] oder weitere Informationen über dieselbe E-Mail-ID erfassen kann, wird die [!DNL RampID] auf einen neuen Wert. [!DNL LiveRamp] bezieht sich auf diese Aktion als Upgrade von einer &quot;abgeleiteten&quot; [!DNL RampID] zu &quot;gepflegt&quot; [!DNL RampID]. DSP erhält jedoch keine Zuordnungen zwischen abgeleiteten und gewarteten [!DNL RampIDs] und kann daher die vorherige Version der RampID nicht aus dem DSP Segment entfernen. In diesem Fall kann die Segmentanzahl größer als die Profilanzahl sein.

  Beispiel: Ein Benutzer meldet sich bei der [!DNL Adobe] und besuchen Sie die Photoshop-Seite. Wenn [!DNL LiveRamp] keine vorhandenen Informationen über die E-Mail-ID hat, weist sie ihr eine abgeleitete [!DNL RampID], beispielsweise D123. Fünfzehn Tage später besucht der Benutzer die gleiche Seite, jedoch [!DNL LiveRamp] hat die [!DNL RampID] während dieser 15 Tage und hat die [!DNL RampID] zu M123. Obwohl das Segment &quot;Photoshop Enthusiast&quot;der Kundendatenplattform nur eine E-Mail-ID für den Benutzer hat, verfügt das DSP-Segment über zwei Ramp-IDs: D123 und M123.

>[!MORELIKETHIS]
>
>* [Erstellen einer Zielgruppenquelle zur Aktivierung von universellen ID-Zielgruppen](/help/dsp/audiences/sources/source-create.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Adobe Real-Time CDP] zu universellen IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus [!DNL Tealium] zu universellen IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](/help/dsp/audiences/custom-segment-create.md)
>* [Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)