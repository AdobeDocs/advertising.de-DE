---
title: Geräteübergreifende Lösungen
description: Erfahren Sie mehr über geräteübergreifende Funktionen.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Geräteübergreifende Lösungen

Durch die Integration von Advertising DSP mit [!DNL LiveRamp] können Sie Ihre Zielgruppe auf alle bekannten Geräte einer Person erweitern, nicht nur auf die Geräte, die Ihre Marke verfolgt hat. Die Integration bietet außerdem Frequenzlimitierung und Attributionsmessung für alle Geräte.

Wenn Sie ein unterstütztes benutzerbasiertes Gerätediagramm verwenden, können Sie:

* Passen Sie Zielgruppen kanalübergreifend und geräteübergreifend an, um Anzeigen für Personen und Haushalte und nicht für Geräte bereitzustellen.
* Ausgewogenheit und Exposition durch Verständnis und Begrenzung der Häufigkeit einzelner Personen.
* Teststrategien, die Zielgruppen über Kanäle oder Geräte hinweg verfügbar machen oder konvertieren.

## Vorteile des [!DNL LiveRamp]-Gerätediagramms

* Stellt einen deterministischen Datenpool bereit, einschließlich Offline-Kundendaten

* Gewährt eine gleichmäßige Abdeckung zwischen Cookie-IDs und Mobilgeräte-IDs

* Umfasst Daten überwiegend aus den Vereinigten Staaten

* Ist frei für Frequenzlimitierung und Attributionsmessung

* Preiswert von 0,35 USD für erweiterte Impressionen (Impressionen, die ausschließlich durch Verwendung des [!DNL LiveRamp]-Gerätediagramms und nicht durch Verwendung von Geräten in Zielgruppensegmenten bereitgestellt werden)

  Der Preis wird auf Ihrer Kreditkarte angezeigt.

## Personenbasiertes Frequenzmanagement

Mit dem personenbasierten Frequenzmanagement können Sie Frequenzobergrenzen auf der Ebene der Person und nicht des Geräts für eine echte Steuerung der Medienbelichtung festlegen.

### Benutzerbasiertes Frequenzmanagement aktivieren

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie die Einstellung [!UICONTROL Cross-Device Level] festlegen. Aktivieren Sie &quot;[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]&quot;und wählen Sie ein Gerätediagramm aus. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf Platzierungsebene als auch für benutzerbasiertes Frequenzmanagement auf Kampagnen-, Paket- und Platzierungsebene verwendet. Häufigkeitsbegrenzungen gelten für alle bekannten Geräte einer Person.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Nachdem Sie eine Kampagne gespeichert haben, können Sie die Einstellung [!UICONTROL Cross Device Level] nicht mehr ändern.

* **Pakete:** Sie können optional zusätzliche Häufigkeitsbegrenzungen auf Paketebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

* **Platzierungen:** Sie können optional zusätzliche Häufigkeitsbegrenzungen auf der Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

## Personenbasiertes Targeting

Mit personenbasiertem Targeting können Sie Kunden auf dem Desktop und auf Mobilgeräten finden.

### Aktivieren von personenbasiertem Targeting

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie die Einstellung [!UICONTROL Cross-Device Level] festlegen. Aktivieren Sie &quot;[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]&quot;und wählen Sie ein Gerätediagramm aus. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf Platzierungsebene als auch für benutzerbasiertes Frequenzmanagement verwendet.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Platzierungen:** Wenn Sie Zielgruppen für eine Platzierung in einer Kampagne mit einem bestimmten Gerätediagramm auswählen, können Sie mit der Option [!UICONTROL Cross-Device Targeting] Ihr Targeting auf alle bekannten Geräte einer Person (gemäß dem in den Kampagneneinstellungen festgelegten Gerätediagramm) erweitern, selbst auf Geräte, die nicht in den angegebenen Segmenten enthalten sind.

### Einrichten von Berichten für personenbasiertes Targeting

Sie können die folgenden Metriken in benutzerspezifische Berichte aufnehmen:

* **Erweiterte Impressionen:** (Im Abschnitt [!UICONTROL Build Your Report] unter [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Das Volumen der inkrementellen Impressionen, die durch Nutzung eines Gerätediagramms bereitgestellt werden (und nicht in den ursprünglichen Zielgruppensegmenten gefunden werden). Diese Metrik wird auch zur Berechnung der anwendbaren Gebühren für die Verwendung eines Gerätediagramms eines Drittanbieters verwendet.

  Um die Kosten Ihrer erweiterten Impressionen während eines Zeitraums zu ermitteln, führen Sie einen benutzerspezifischen Bericht aus, der die Spalte &quot;[!UICONTROL Extended Impressions]&quot;enthält, und multiplizieren Sie dann die Gesamtanzahl der erweiterten Impressionen um 0,0035 USD ($0,35/1000 Impressionen).

  Die aggregierten Kosten sind auch in der Spalte [!UICONTROL Billable Other Net Spend] enthalten (unter [!UICONTROL Metrics] > [!UICONTROL Spend]), obwohl diese Metrik auch andere Kampagnengebühren enthält, die Sie möglicherweise hinzugefügt haben.

* **Gerätediagramm:** (Im Abschnitt [!UICONTROL Build Your Report] unter [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Das ausgewählte Gerätediagramm für eine bestimmte Kampagne, ein bestimmtes Paket oder eine bestimmte Platzierung.

## Benutzerbasierte Attributionsmessung

*Advertiser mit nur Adobe Advertising-Konversions-Tracking*

Mit der benutzerbezogenen Attribution können Sie Konversionen zuordnen, die auf einem anderen Gerät stattgefunden haben als auf dem Gerät, auf dem die Medienbelichtung stattgefunden hat. Die personenbasierte Attributionsmessung ist für Advertiser DSP, [!DNL Adobe Advertising Creative] und [!DNL Adobe Advertising Search, Social, & Commerce] verfügbar, die Adobe Advertising-Konversionspixel auf ihren Sites implementiert haben.

### Benutzerbasierte Attributionsmessung aktivieren

Wenden Sie sich an Ihr Adobe Account-Team, wenn Sie die geräteübergreifende Attributionsmessung aktivieren möchten.

### Einrichten von Konversionsberichten für die geräteübergreifende Konversionszuordnung

#### Konversionsberichtseinstellungen

Wenn ein Gerätediagramm für die Attributionsmessung aktiviert ist, enthält der Bericht [!UICONTROL Conversion] eine Einstellung [!UICONTROL Cross-Device Breakout] , mit der Sie bis zu drei separate Spalten für jede Konversionsmetrik einbeziehen können, darunter:

* &lt;*Konversion*>[!UICONTROL (tp)]: Umfasst die Gesamtkonversionen (Personen insgesamt), die sowohl Konversionen auf demselben Gerät als auch geräteübergreifende Konversionen enthalten (falls zutreffend). Im Bericht wird &quot;[!UICONTROL (tp)]&quot; an den Namen, den Regeltyp und die Konversionstypen der Konversionsmetrik im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(tp)).

* &lt;*Konversion*>[!UICONTROL (sd)]: (Optional) Umfasst nur Konversionen, für die im Konversionspfad nur ein einziges Gerät verfolgt wurde. Im Bericht wird &quot;[!UICONTROL (sd)]&quot; an den Namen, den Regeltyp und die Konversionstypen der Konversionsmetrik im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(sd)).

* &lt;*Konversion*>[!UICONTROL (xd)]: (Optional) Umfasst nur Konversionen, für die im Konversionspfad mehr als ein Gerät verfolgt wurde. Im Bericht wird &quot;[!UICONTROL (xd)]&quot; an den Namen, den Regeltyp und die Konversionstypen der Konversionsmetrik im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(xd)).

#### Interpretieren des Konversionsberichts

Sortieren Sie den Prozentsatz der gesamten Konversionen, die geräteübergreifend sind ([!UICONTROL (xd)]/[!UICONTROL (tl)]), von hoch zu niedrig, um zu verstehen, was zu überdurchschnittlichen geräteübergreifenden Konversionen führt. Sie können dies verwenden, um Ihre Kreativ- oder Targeting-Strategie zu informieren, um Messaging und Kanalinvestitionen auf das Benutzerverhalten abzugleichen.

* Pakete - Ermitteln Sie, welche Pakete die meisten Konversionen erzielen und welche einen hohen Prozentsatz geräteübergreifender Konversionen aufweisen. Auf diese Weise können Sie erkennen, wo die Ausgaben konzentriert werden.

* Platzierungen - Vergleichen Sie Platzierungsleistung und Attribution (z. B. kann eine mobile Webanzeige Konversionen auf dem Desktop fördern). Ohne Gerätediagramm für die Attribution können Sie die Auswirkungen einer mobilen Webplatzierung auf die Desktop-Konversionen verpassen oder sie kann begraben werden, wenn die Mehrheit Ihrer Benutzer auf dem Desktop und nicht im mobilen Internet konvertiert.

* Anzeigen - Erfahren Sie, welche Anzeigen zu höheren Konversionen führen und deren Wert und Wirkung über Webbrowser und Mobile-App-Umgebungen hinweg quantifizieren.

* Sites - Optimieren Sie Sites, anstatt Sites manuell vollständig auszuschließen. Wenn eine Website geräteübergreifende Konvertierungen durchführt, können Sie sehen, auf welchen Geräten dieses Verhalten auftritt.

* Angebote - Verbessern Sie die manuelle Optimierung, indem Sie überprüfen, welche Inventarangebote geräteübergreifende Konversionen liefern, und dann entscheiden, ob Sie Ihr Targeting erweitern sollten, um mehr Geräte und Kanäle in diese Angebote einzubeziehen.

>[!MORELIKETHIS]
>
>* [Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
