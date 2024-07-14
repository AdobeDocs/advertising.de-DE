---
title: Markensicherheit und Medienqualität
description: Erfahren Sie mehr über Markensicherheit und Medienqualitätsmerkmale.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: a927c073fd27e0b2c84bd1929eb4d6d233a29cb5
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Markensicherheit und Medienqualität

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP bietet eine Reihe von Markenschutzfunktionen, um sicherzustellen, dass jede Ihrer Kampagnen echte Benutzer in einer markensicheren Umgebung erreicht.

Unser Team von Fraud Surveillance arbeitet eng mit branchenführenden Partnern wie den [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] und [!DNL WhiteOps] zusammen, um den Bestand auf unserer Plattform sorgfältig zu kuratieren. Durch die proaktive Verwaltung unseres Angebots stellt DSP sicher, dass alle Advertiser auf der ganzen Plattform vor unmenschlichem Traffic (Bots, Crawler, Data Center Traffic und Betrug) geschützt sind und nur in markensicheren Kontexten bereitstellen.

Neben dem zentralen Qualitätsmanagement möchten wir Werbetreibende in die Lage versetzen, die ihrer Marke entsprechenden Steuerelemente zu entwerfen. DSP bietet Integrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] und [!DNL Peer39], um sicherzustellen, dass jeder Advertiser das gewünschte Maß an Betrugsschutz, kontextbezogener Filterung und Keyword-Targeting auswählen kann.

## Qualitätsinitiativen

### Lagerbestandsverifizierung mit [!DNL Ads.txt] Unterstützung

[[!DNL Ads.txt], was für  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) steht, ist eine Initiative, die von den [!DNL Interactive Advertising Bureau] ([!DNL IAB]) im Juni 2017 eingeleitet wurde, um die ordnungsgemäße Darstellung des Bestands auf dem freien Markt zu erleichtern und damit unrechtmäßige Quellen von Traffic und Domain-Spoofing zu bekämpfen. Beteiligte Herausgeber und Distributoren erklären öffentlich die Unternehmen, die zum Verkauf ihres digitalen Bestands berechtigt sind, sowie die Art dieser Beziehungen, indem sie eine `ads.txt` -Seite auf oberster Ebene der Domäne (z. B. `example.com/ads.txt`) verwalten.

DSP unterstützt &quot;[!DNL ads.txt]&quot;, indem die `ads.txt` -Datei jedes Herausgebers gelesen wird und Sie die Option erhalten, nur bei verifizierten [!DNL ads.txt] Verkäufern zu kaufen. Wenn wir beispielsweise die verkauften Artikel, auf die wir zugreifen, mit der Datei `ads.txt` der New York Times verknüpfen, können wir ermitteln, welche rechtmäßig sind und welche nicht, und wir blockieren die Straftäter, wenn die Platzierung so konfiguriert ist, dass sie nur bei bestätigten Verkäufern gekauft wird. <!-- can we actually mention NY Times? -->`nytimes.com`

Sie können die standardmäßigen [!DNL ads.txt] -Steuerelemente für jeden Advertiser<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> festlegen und dann optional [die Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) anpassen, um:

* Inventar nur von autorisierten Direktverkäufern einer Domain kaufen

* Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain kaufen

* Kaufbestand von autorisierten Direktverkäufern und Wiederverkäufern einer Domain priorisieren

* Inventar von allen Verkäufern kaufen

### Überwachung von Platform-Betrug

DSP hat leistungsstarke interne Tools und Systeme zur Verwaltung von Betrug auf unserer gesamten Plattform entwickelt und arbeitet mit führenden Branchenanbietern wie [!DNL Whiteops] und [!DNL Integral Ad Science] zusammen.

Darüber hinaus arbeitet Adobe eng mit [!DNL IAB] und [!DNL TAG] zusammen, um eine robuste und branchenübliche Betrugsblockierung zu gewährleisten, um unsere Advertiser zu schützen, indem es Tools wie [!DNL ads.txt] (siehe vorherigen Abschnitt), die Liste [!DNL IAB] Bots and Spiders und die IP-Liste [!DNL TAG] Datacenter nutzt.

Durch unseren mehrdimensionalen Qualitätsansatz überwacht unser Team Anomalien und ungültige Traffic-Muster und sorgt so für weniger als 3 % ungültigen Traffic im geschützten Inventar. Alle Bestände, die verdächtig sind - einschließlich Inventar auf bestimmten Domänen oder von bestimmten Herausgebern oder Verkäufern - werden sofort auf der gesamten Plattform blockiert.

### Inventarzuordnung, -unterteilung und -kategorisierung

Die Bestandszuordnung ist der detaillierte Überprüfungs- und Onboarding-Prozess, der für alle neuen Bestände erforderlich ist, bevor er zu unserer Plattform hinzugefügt wird. Dieser Prozess soll die Sicherheit und Qualität des gesamten Bestands auf DSP gewährleisten.

* **Zuordnung:** Unser Inventar-Team überprüft jede Domäne sorgfältig und bewertet Aspekte wie:

   * Markensicherheit

   * Verifizierung des Anzeigentyps

   * Allgemeine Inhalte, doppelte Domänen und gefälschte Adserving

* **Tiering:** Wir untersuchen ganzheitlich die Markenpräsenz im gesamten Ökosystem, um Inventare über verschiedene Ebenen hinweg zu klassifizieren. Sie können Ihre Platzierungen ](/help/dsp/campaign-management/placements/placement-settings.md) für die gewünschte Reichweite auf diese Stufen ausrichten:[

   * **[!UICONTROL T1]** - Markenname, international erkennbare Sites

   * **[!UICONTROL T2]** - Sehr ansprechende Sites, die aktuell und aktuell sind, ohne benutzergenerierten Inhalt und in der Regel keine globale Erkennung aufweisen

   * **[!UICONTROL T3]** - Benutzergenerierte Inhalte und Nischeninhalte

* **Site-Kategorisierung:** Um einfaches Content-Targeting und -Blockieren sicherzustellen, versehen wir jede Eigenschaft mit einer DSP definierten Site-Kategorie, die auf dem Inhalt der Eigenschaft basiert. Sie können diese Site-Kategorien anhand der Platzierungsziele für jede Platzierung ](/help/dsp/campaign-management/placements/placement-settings.md) als Ziel festlegen oder ausschließen.[

### Umfassende Unterstützung für Site-Blocking

DSP bietet sowohl eine global gesperrte Siteliste als auch die Option, benutzerdefinierte Blockierungslisten für Advertiser und Konten zu erstellen.

#### DSP Liste global blockierter Sites {#global-blocked-sites}

DSP verwaltet eine global gesperrte Site-Liste von Sites, die für unsicher erachtet werden, um Anzeigen auf dieser Site auszuführen. Diese Liste enthält Websites mit verwerflichen Inhalten (z. B. Hass oder Terror) und von Bots infizierten Websites, gefälschten Pre-Roll-Dateien, nicht übereinstimmenden Domänen und anderen betrügerischen Aktivitäten.

Im Rahmen unserer Initiative zur Markensicherheit, um Aktivitäten auszurotten, die Werbetreibende betrügen, werden alle Sites anhand der in der Liste der blockierten Sites der Grafik aufgeführten Maßnahmen überprüft. Alle Sites, die die Markensicherheitsprüfungen nicht bestehen, werden der Liste der global blockierten Sites hinzugefügt. Da DSP diese Liste dynamisch verwaltet, können Sites auf der Grundlage der neuesten Analyse der Markensicherheit jederzeit aus der Liste wechseln.

Wenn Sie eine Site in die Liste der global blockierten Sites als Platzierungsziel einschließen, wird die Site mit einem roten Ausrufezeichen (!) gekennzeichnet. Dies bedeutet, dass Anzeigen nicht auf der gekennzeichneten Site ausgeführt werden.

>[!NOTE]
>
>Sie können optional die globale Liste der blockierten Sites für Standardanzeigen umgehen, die an ein vertrauenswürdiges privates Geschäft angehängt sind, indem Sie die Option &quot;[!UICONTROL Allow unscreened sites]&quot; in den [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md) aktivieren. Falls nötig, kann das Adobe Account Team optional auch die Site-Blockierung für einen öffentlichen (Auktionsebene) Deal in den Publisher-Einstellungen für den Deal deaktivieren.

#### Blockierte Sites auf Kontoebene und Advertiser-Ebene

Benutzer können auch Blockierungslisten auf Kontoebene und auf Advertiser-Ebene verwalten<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, die automatisch für alle Platzierungen verwendet werden. Die Liste der blockierten Sites der unteren Ebene wird zusätzlich zur Liste der global blockierten Sites angewendet.

## Drittanbieterintegrationen

### Kontextuelle Filterung

Mit kontextuellen Filtern können Sie Anzeigenangebote basierend auf dem Kontext der Seite, auf der die Anzeige bereitgestellt wird, gezielt ausrichten oder blockieren. Adobe bietet kontextbezogene Filterung über Integrationen mit führenden Anbietern in der Branche: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Beispiele für aktuelle Filter sind [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] und [!UICONTROL G-rated Sites].

Sie können für jeden Advertiser standardmäßige Steuerelemente für kontextbezogene Filter festlegen<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> und dann optional [die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![Komprimierungslogo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png) ![Peer39 logo](/help/dsp/assets/peer39-logo.png)

### Blockierung von Vorab-Angebotsbetrug

Nutzen Sie unsere Drittanbieterintegrationen mit [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39], um nicht menschlichen Traffic von Ihren Kampagnen zu blockieren. Diese Integrationen bieten branchenführende Pre-Bid-Blockierungsfunktionen, mit denen Sie den allgemeinen und komplexen ungültigen Traffic (GIVT und SIVT) in Ihren Kampagnen minimieren können.

Sie können für jeden Advertiser Standardkontrollen zum Blockieren von Betrug vor dem Angebot festlegen<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> und dann optional die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). [ Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

Weitere Informationen zur Funktionalität erhalten Sie direkt bei Ihrem bevorzugten Anbieter oder bei Ihrem Adobe-Account-Team.

![DoubleVerify logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png) ![Peer39 logo](/help/dsp/assets/peer39-logo.png)

### Vorabanzeige {#pre-bid-viewability}

Mit den von unseren branchenführenden Partnern bereitgestellten Vorab-Sichtbarkeitsfiltern [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) und [!DNL Integral Ad Science] können Werbetreibende sicherstellen, dass ihre Kampagnen ihre gewünschten Leistungsziele bezüglich der Sichtbarkeit über Video- und Anzeigebestände hinweg erfüllen.

>[!NOTE]
>
>[!DNL Oracle] wird sein Werbegeschäft bis zum 30. September 2024 einstellen, einschließlich aller Dienste von [!DNL MOAT].

Sie können für jeden Advertiser standardmäßige Sichtbarkeitsfilter festlegen<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> und dann optional die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). [ Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![DoubleVerify logo](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising logo](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png)

### Aufmerksamkeit-Targeting und -Messung

[!DNL Adobe's] Durch die Partnerschaft mit [!DNL Adelaide] erhalten Werbetreibende Unterstützung für die Adelaide-Metrik &quot;[!DNL Attention Units]&quot;, die die Medienqualität anhand von Augentracking, Belichtung und Ergebnisdaten misst.

[Das Targeting der Aufmerksamkeit auf Platzierungsebene vor dem Angebot](/help/dsp/campaign-management/placements/placement-settings.md) ermöglicht Werbetreibenden, bestimmte Aufmerksamkeitsstufen auf eine bessere Kundeninteraktion auszurichten.

Darüber hinaus können Advertiser das [Tracking für die Metrik auf Platzierungsebene [!UICONTROL Attention Score]](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (die gewichtete durchschnittliche Anzahl von [!DNL Attention Units] über Impressionen hinweg) für jede Kampagne aktivieren, um zu verstehen, welche Platzierungs-Taktiken die besten Geschäftsergebnisse liefern.

Für jede einzelne Funktion fallen zusätzliche Gebühren an.

### Themen-Targeting

DSP Thema-Targeting ermöglicht es Ihnen, Suchbegrifflisten durch Nutzung unserer branchenführenden kontextbezogenen Partner [!DNL Comscore] und [!DNL Oracle Data Cloud] (früher [!DNL Grapeshot]) als Ziel festzulegen oder zu blockieren. Das Thema-Targeting hilft Ihnen dabei sicherzustellen, dass Ihre Anzeigen immer in einer mit Ihrer Marke abgestimmten Umgebung bereitgestellt werden, unabhängig davon, ob dies das Blockieren schädlicher Inhalte oder die Sicherstellung von Ausgaben in einem Kontext umfasst, der ein höheres Ergebnis gewährleistet.

>[!NOTE]
>
>[!DNL Oracle] wird sein Werbegeschäft bis zum 30. September 2024 einstellen, einschließlich aller Dienste von [!DNL Oracle Data Cloud] (früher [!DNL Grapeshot]).

Für das Thema-Targeting müssen Sie benutzerdefinierte Themensegmente direkt mit der Partnerplattform erstellen. Nachdem die Segmente erstellt wurden, können Sie für jede Platzierung ](/help/dsp/campaign-management/placements/placement-settings.md) im Abschnitt [!UICONTROL Audience Targeting] eine Segment-ID als Ziel angeben oder ausschließen. [ Für diese Funktion können zusätzliche Gebühren anfallen.

Um ein [!DNL Comscore] -Konto zu erstellen und benutzerdefinierte Themensegmente zu erstellen, können Sie eine Anmeldung für [!DNL Activation Segment Manager] unter [https://agents.comscore.com](https://agents.comscore.com) anfordern. Vollständige Anweisungen zum Einrichten benutzerdefinierter Segmente finden Sie im [[!DNL Comscore] Hilfezentrum](https://comscoreactivation.zendesk.com/hc/) . Gebühren für benutzerspezifische Segmente werden beim Erstellen in [!DNL Segment Manager] angezeigt.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png) ![Grapeshot-Logo](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP hat sich mit [!DNL DoubleVerify] zusammengeschlossen, um seine Targeting-Lösung für [!DNL Authentic Brand Safety] anzubieten, mit der Sie einen zentralisierten Satz von Markensicherheitsanforderungen erstellen können, um auf alle Ihre Bestellplattformen Zielgruppen für Konsistenz zu bilden.

Nachdem Sie ein Markensicherheitssegment mit dem erforderlichen Targeting für [!DNL DoubleVerify] erstellt haben, können Sie es in DSP verwenden, um Ihre Blockierungsregeln nach dem Gebot in allen Webumgebungen mit dem Pre-Gebot zu replizieren.

Sie können eine [!DNL DoubleVerify] Segment-ID für jeden Advertiser <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> angeben und dann optional [ [!UICONTROL Authentic Brand Safety] für jede Platzierung aktivieren oder deaktivieren](/help/dsp/campaign-management/placements/placement-settings.md). DSP stellt Ihr Konto für die Verwendung der Segment-ID in Rechnung.

Weitere Informationen zur Funktionalität erhalten Sie direkt bei [!DNL DoubleVerify] oder bei Ihrem Adobe-Account-Team.

![DoubleVerify logo](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
