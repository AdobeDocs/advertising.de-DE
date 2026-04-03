---
title: Geräteübergreifende Lösungen
description: Weitere Informationen zu geräteübergreifenden Funktionen.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
TQID: https://experienceleague.adobe.com/CEof59dFrZItQBNhFh6MdlvMGWSNv3em7OJzSeyP0Gg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 997
ht-degree: 0%

---

# Geräteübergreifende Lösungen

Durch die Integration von Advertising DSP mit [!DNL LiveRamp] können Sie Ihre Zielgruppe auf alle bekannten Geräte einer Person erweitern, nicht nur auf die Geräte, die Ihre Marke verfolgt hat. Die Integration bietet auch eine Frequenzlimitierung und Attributionsmessung auf allen Geräten.

Wenn Sie ein unterstütztes personenbasiertes Gerätediagramm verwenden, können Sie:

* Ordnen Sie Zielgruppen kanalübergreifend und geräteübergreifend zu, um Anzeigen für Personen und Haushalte statt für Geräte bereitzustellen.
* Ausgewogenheit und Exposition durch Verständnis und Begrenzung der Häufigkeit bei allen Personen.
* Teststrategien, die Zielgruppen kanalübergreifend oder geräteübergreifend verfügbar machen bzw. konvertieren.

## Vorteile des [!DNL LiveRamp] Gerätediagramms

* Stellt einen deterministischen Datenpool bereit, einschließlich Offline-Kundendaten

* Bietet gleichmäßige Abdeckung zwischen Cookie-IDs und IDs von Mobilgeräten

* Umfasst Daten vorwiegend aus den USA

* Ist kostenlos für Frequenzlimitierung und Attributionsmessung

* Für erweiterte Impressionen (Impressionen, die ausschließlich mithilfe des [!DNL LiveRamp]-Gerätediagramms und nicht auf Geräten innerhalb der Zielgruppensegmente bereitgestellt werden) wird ein Preis von 0,35 US-Dollar berechnet.

  Der Tarif wird auf der Tarifkarte Ihres Kontos angezeigt.

## Personenbasiertes Frequenzmanagement

Mit dem personenbasierten Frequenzmanagement können Sie Frequenzlimits auf der Personenebene und nicht auf Geräteebene festlegen, um die tatsächliche Medienexposition zu steuern.

### Aktivieren des personenbasierten Häufigkeitsmanagements

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie eine [!UICONTROL Cross-Device Level] festlegen. &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; aktivieren und ein Gerätediagramm auswählen. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf der Platzierungsebene als auch für das personenbasierte Häufigkeitsmanagement auf Kampagnen-, Paket- und Platzierungsebene verwendet. Häufigkeitsbegrenzungen gelten für alle bekannten Geräte einer Person.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Nachdem Sie eine Kampagne gespeichert haben, können Sie ihre [!UICONTROL Cross Device Level] nicht mehr ändern.

* **Pakete:** Sie können optional zusätzliche Häufigkeitsbegrenzungen auf Paketebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.

* **Platzierungen** Sie können optional zusätzliche Häufigkeitsbegrenzungen auf Platzierungsebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.

## Personenbasiertes Targeting

Mit dem personenbasierten Targeting können Sie Kunden über Desktop- und Mobilgeräte hinweg finden.

### Personenbasiertes Targeting aktivieren

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie eine [!UICONTROL Cross-Device Level] festlegen. &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; aktivieren und ein Gerätediagramm auswählen. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf Platzierungsebene als auch für das personenbasierte Frequenzmanagement verwendet.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Platzierungen:** Wenn Sie Zielgruppenziele für eine Platzierung in einer Kampagne mit einem angegebenen Gerätediagramm auswählen, können Sie mit einer [!UICONTROL Cross-Device Targeting] Option die Zielgruppenbestimmung auf alle bekannten Geräte einer Person (gemäß dem in den Kampagneneinstellungen angegebenen Gerätediagramm) erweitern, auch auf Geräte, die nicht in den angegebenen Segmenten enthalten sind.

### Einrichten von Berichten für das personenbasierte Targeting

Sie können die folgenden Metriken in benutzerdefinierte Berichte aufnehmen:

* **Erweiterte Impressions:** (im [!UICONTROL Build Your Report] Abschnitt unter [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Das Volumen der inkrementellen Impressions, die mithilfe eines Gerätediagramms bereitgestellt werden (und nicht in den ursprünglichen Zielgruppensegmenten gefunden werden). Diese Metrik wird auch verwendet, um die Gebühren zu berechnen, die für die Verwendung eines Gerätediagramms eines Drittanbieters anfallen.

  Um die Kosten Ihrer erweiterten Impressionen während eines Zeitraums zu ermitteln, führen Sie einen benutzerdefinierten Bericht aus, der die Spalte &quot;[!UICONTROL Extended Impressions]&quot; enthält, und multiplizieren Sie dann die Gesamtzahl der erweiterten Impressionen mit 0,00035 USD ($0,35/1000 Impressionen).

  Die aggregierten Kosten sind auch in der Spalte [!UICONTROL Billable Other Net Spend] enthalten (unter [!UICONTROL Metrics] > [!UICONTROL Spend]), obwohl diese Metrik auch andere Kampagnengebühren enthält, die Sie möglicherweise hinzugefügt haben.

* **Gerätediagramm:** (im [!UICONTROL Build Your Report] Abschnitt unter [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Das ausgewählte Gerätediagramm für eine bestimmte Kampagne, ein bestimmtes Paket oder eine bestimmte Platzierung.

## Personenbasierte Attributionsmessung

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

Mit der personenbasierten Attribution können Sie Konversionen zuordnen, die auf einem anderen Gerät stattgefunden haben als auf dem Gerät, auf dem die Medienbelichtung stattgefunden hat. Personenbasierte Attributionsmessungen sind in DSP, [!DNL Adobe Advertising Creative] und [!DNL Adobe Advertising Search, Social, & Commerce] für Werbetreibende verfügbar, die Adobe Advertising-Konversionspixel auf ihren Sites implementiert haben.

### Personenbasierte Attributionsmessung aktivieren

Wenn Sie die geräteübergreifende Attributionsmessung aktivieren möchten, wenden Sie sich an Ihr Adobe-Account-Team.

### Einrichten von [!UICONTROL Conversion] für geräteübergreifende Konversionszuordnung

#### Berichtseinstellungen [!UICONTROL Conversion]

Wenn ein Gerätediagramm für die Attributionsmessung aktiviert ist, enthält der [!UICONTROL Conversion] eine [!UICONTROL Cross-Device Breakout], mit der Sie bis zu drei separate Spalten für jede Konversionsmetrik einbeziehen können, darunter:

* „ph id=&#39;1&#39;/>Konversion *>[!UICONTROL (tp)]: Umfasst die Gesamtkonversionen (Personen insgesamt), die sowohl Konversionen auf demselben Gerät als auch geräteübergreifende Konversionen (falls zutreffend) umfasst.* Im Bericht wird &quot;[!UICONTROL (tp)]&quot; an den Namen der Konversionsmetrik, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. „Responses(le)(tl)(tp)„).

* „ph id=&#39;1&#39;/>Konversion *>[!UICONTROL (sd)]: (Optional) Umfasst nur Konversionen, bei denen im Konvertierungspfad nur ein einzelnes Gerät verfolgt wurde.* Im Bericht wird &quot;[!UICONTROL (sd)]&quot; an den Namen der Konversionsmetrik, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. „Responses(le)(tl)(sd)„).

* „ph id=&#39;1&#39;/>Konversion *>[!UICONTROL (xd)]: (Optional) Umfasst nur Konversionen, bei denen mehr als ein Gerät im Konversionspfad verfolgt wurde.* Im Bericht wird &quot;[!UICONTROL (xd)]&quot; an den Namen der Konversionsmetrik, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. „Responses(le)(tl)(xd)„).

#### Interpretation des [!UICONTROL Conversion]

Sortieren Sie den Prozentsatz der gesamten Konversionen, die geräteübergreifend sind ([!UICONTROL (xd)]/[!UICONTROL (tl)]), von hoch nach niedrig, um zu verstehen, was zu überdurchschnittlichen geräteübergreifenden Konversionen führt. Auf diese Weise können Sie Ihre Kreativ- oder Targeting-Strategie so gestalten, dass Messaging und Kanalinvestitionen auf das Benutzerverhalten abgestimmt werden.

* Pakete - Ermitteln Sie, welche Pakete die meisten Konversionen insgesamt erzielen und welche einen hohen Prozentsatz geräteübergreifender Konversionen aufweisen. Dies kann Ihnen helfen zu verstehen, wo Sie Ihre Ausgaben konzentrieren sollten.

* Platzierungen - Vergleich der Platzierungsleistung und -zuordnung (z. B. kann eine mobile Web-Anzeige auf dem Desktop zu Konversionen führen). Ohne ein Gerätediagramm für die Attribution können Sie die Auswirkungen einer mobilen Web-Platzierung auf Desktop-Konversionen verpassen oder sie kann begraben werden, wenn die Mehrheit Ihrer Benutzer auf dem Desktop und nicht im mobilen Web konvertiert.

* Anzeigen - Entdecken Sie, welche Anzeigen zu höheren Konversionen führen, und quantifizieren Sie deren Wert und Wirkung sowohl in Webbrowsern als auch in Mobile-App-Umgebungen.

* Sites - Optimieren Sie über Sites hinweg, anstatt Sites manuell vollständig auszuschließen. Wenn eine Website geräteübergreifende Konversionen auslöst, können Sie sehen, auf welchen Geräten dieses Verhalten auftritt.

* Angebote - Verbessern Sie die manuelle Optimierung, indem Sie überprüfen, welche Inventarangebote geräteübergreifende Konversionen liefern, und entscheiden Sie dann, ob Sie Ihr Targeting erweitern sollten, um mehr Geräte und Kanäle in diese Angebote einzubeziehen.

>[!MORELIKETHIS]
>
>* [Berichteinstellungen](/help/dsp/reports/report-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
