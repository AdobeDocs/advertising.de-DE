---
title: Markensicherheit und Medienqualität
description: Erfahren Sie mehr über die Funktionen für Markensicherheit und Medienqualität.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Markensicherheit und Medienqualität

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP bietet eine Reihe von Funktionen zum Markenschutz, mit denen sichergestellt werden kann, dass jede Ihrer Kampagnen echte Benutzende in einer markensicheren Umgebung erreicht.

Unser Betrugsüberwachungsteam arbeitet eng mit branchenführenden Partnern wie der [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] und [!DNL WhiteOps] zusammen, um das Inventar auf unserer Plattform sorgfältig zu kuratieren. Durch die proaktive Verwaltung unseres Angebots stellt DSP sicher, dass alle Werbetreibenden auf der Plattform vor nicht menschlichem Traffic geschützt sind (Bots, Crawler, Datencenter-Traffic und Betrug) und nur in markensicheren Kontexten liefern.

Neben der Bereitstellung eines zentralen Qualitätsmanagements glauben wir daran, Werbetreibenden die Möglichkeit zu geben, die Kontrollen zu entwerfen, die mit ihrer Marke übereinstimmen. DSP bietet Integrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39], sodass jeder Werbetreibende das gewünschte Maß an Betrugsschutz, kontextbezogener Filterung und Keyword-Targeting auswählen kann.

## Qualitätsinitiativen

### Inventarüberprüfung mit [!DNL Ads.txt] Support

[[!DNL Ads.txt], das für steht [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) ist eine Initiative der [!DNL Interactive Advertising Bureau] ([!DNL IAB]) vom Juni 2017 zur Erleichterung der ordnungsgemäßen Darstellung von Beständen auf dem freien Markt und zur Bekämpfung von illegalen Quellen von Traffic und Domain-Spoofing. Teilnehmende Verlage und Distributoren erklären öffentlich, welche Unternehmen zum Verkauf ihres digitalen Inventars berechtigt sind, und geben die Art dieser Beziehungen an, indem sie eine `ads.txt` Seite auf der obersten Ebene der Domain (z. B. `example.com/ads.txt`) führen.

DSP unterstützt [!DNL ads.txt], indem es die `ads.txt` jedes Herausgebers liest und Ihnen die Möglichkeit gibt, nur bei verifizierten [!DNL ads.txt] zu kaufen. Indem wir beispielsweise die Verkäufer, die wir beim Zugriff auf `nytimes.com` sehen, mit der `ads.txt`-Datei der New York Times abgleichen, können wir identifizieren, welche legitim sind und welche nicht, und wir blockieren die Übeltäter, wenn die Platzierung so konfiguriert ist, dass sie nur von verifizierten Verkäufern kaufen. <!-- can we actually mention NY Times? -->

Sie können standardmäßige [!DNL ads.txt] für jeden Advertiser festlegen <!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> dann optional [die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md) um:

* Kaufen Sie Inventar nur von autorisierten Direktverkäufern einer Domain

* Kaufen Sie Inventar nur bei autorisierten Direktverkäufern und Wiederverkäufern einer Domain

* Priorisieren Sie den Kauf von Beständen von autorisierten Direktverkäufern und Wiederverkäufern einer Domain

* Bestand von allen Verkäufern kaufen

### Überwachung von Plattformbetrug

DSP hat leistungsstarke interne Tools und Systeme entwickelt, um Betrugsfälle plattformübergreifend zu verwalten, und arbeitet dabei mit führenden Branchenanbietern wie [!DNL Whiteops] und [!DNL Integral Ad Science] zusammen.

Darüber hinaus arbeitet Adobe eng mit [!DNL IAB] und [!DNL TAG] zusammen, um eine robuste, dem Branchenstandard entsprechende Betrugssperre zu gewährleisten, um unsere Werbetreibenden zu schützen. Dabei kommen Tools wie [!DNL ads.txt] (siehe vorherigen Abschnitt), die [!DNL IAB] Bots- und Spiders-Liste und die [!DNL TAG] Datacenter IP-Liste zum Einsatz.

Durch unseren mehrdimensionalen Qualitätsansatz überwacht unser Team Anomalien und ungültige Traffic-Muster und stellt sicher, dass weniger als 3 % ungültiger Traffic auf geschütztem Inventar vorhanden ist. Verdächtige Inventare - einschließlich Inventare auf bestimmten Domains oder von bestimmten Herausgebern oder Verkäufern - werden sofort auf der gesamten Plattform blockiert.

### Bestandszuordnung, Tiering und Kategorisierung

Inventar-Mapping ist der detaillierte Überprüfungs- und Onboarding-Prozess, der für alle neuen Inventare erforderlich ist, bevor sie zu unserer Plattform hinzugefügt werden. Dieser Prozess soll die Sicherheit und Qualität aller DSP-Bestände gewährleisten.

* **Zuordnung:** Unser Inventar-Team prüft jede Domain sorgfältig und bewertet Aspekte wie:

   * Markensicherheit

   * Prüfung des Anzeigentyps

   * Allgemeine Inhalte, doppelte Domains und Bereitstellung falscher Anzeigen

* **Tiering** Wir untersuchen die Markenpräsenz im gesamten Ökosystem ganzheitlich, um Inventar über verschiedene Ebenen zu klassifizieren. Sie können [Ihre Platzierungen](/help/dsp/campaign-management/placements/placement-settings.md) auf diese Ebenen ausrichten, um die gewünschte Reichweite zu erreichen:

   * **[!UICONTROL T1]** — Marken- und international anerkannte Websites

   * **[!UICONTROL T2]** - Tolle Websites, die aktuell und aktuell sind, keine benutzergenerierten Inhalte enthalten und denen es in der Regel an globaler Anerkennung mangelt

   * **[!UICONTROL T3]** - Benutzergenerierte Inhalte und Nischeninhalte

* **Site-Kategorisierung:** Um das einfache Targeting und Blockieren von Inhalten zu gewährleisten, versehen wir jede Eigenschaft mit einer DSP-definierten Site-Kategorie, die auf dem Inhalt der Eigenschaft basiert. Sie können [&#x200B; diese Site-Kategorien für jede Platzierung basierend &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md) den Platzierungszielen auswählen oder ausschließen.

### Umfassende Unterstützung für Site-Blockierung

DSP bietet sowohl eine Liste global blockierter Websites als auch die Möglichkeit, benutzerdefinierte Listen blockierter Websites für Werbetreibende und Konten zu erstellen.

#### Liste der global blockierten DSP-Websites {#global-blocked-sites}

DSP verwaltet eine Liste global blockierter Websites, auf denen Anzeigen als unsicher eingestuft werden. Diese Liste enthält Websites mit anstößigen Inhalten (wie Hass oder Terror) und Websites, die mit Bots, gefälschten Pre-Roll-Inhalten, nicht übereinstimmenden Domains und anderen betrügerischen Aktivitäten infiziert sind.

Im Rahmen unserer Initiative zur Markensicherheit, um Aktivitäten auszumerzen, die Werbetreibende betrügen, werden alle Websites mit den Maßnahmen in der Liste der blockierten Websites des Diagramms gescreent. Alle Websites, die die Markensicherheitsprüfungen nicht bestehen, werden der Liste global blockierter Websites hinzugefügt. Da DSP diese Liste dynamisch verwaltet, können Websites basierend auf der neuesten Sicherheitsanalyse für Marken jederzeit in der Liste wechseln oder davon abweichen.

Wenn Sie eine Site als Platzierungsziel in die Liste global blockierter Sites aufnehmen, wird die Site mit einem roten Ausrufezeichen (!) gekennzeichnet. Dies bedeutet, dass Anzeigen nicht auf der gekennzeichneten Site ausgeführt werden.

>[!NOTE]
>
>Sie können optional die globale Liste der blockierten Websites für Standardanzeigenanzeigen umgehen, die an ein vertrauenswürdiges privates Angebot angehängt sind, indem Sie die Option &quot;[!UICONTROL Allow unscreened sites]&quot; in den [Platzierungseinstellungen“ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md). Bei Bedarf kann das Adobe-Account-Team optional auch die Website-Blockierung für einen öffentlichen Deal (auf Auktionsebene) in den Publisher-Einstellungen für den Deal deaktivieren.

#### Blockierte Sites-Listen auf Konto- und Advertiser-Ebene

Benutzer können auch Listen für blockierte Websites auf Konto- und Advertiser-Ebene verwalten<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> die automatisch für alle Platzierungen verwendet werden. Die Blockierte-Sites-Liste auf niedrigerer Ebene wird zusätzlich zur Liste global blockierte Sites angewendet.

## Integrationen von Drittanbietern

### Kontextbezogene Filterung

Mit der kontextuellen Filterung können Sie Anzeigenchancen basierend auf dem Kontext der Seite, auf der die Anzeige erscheinen soll, ansprechen oder blockieren. Adobe bietet kontextbezogene Filterung über Integrationen mit führenden Anbietern in der Branche: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Beispiele für aktuelle Filter sind [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] und [!UICONTROL G-rated Sites].

Sie können für jeden Advertiser standardmäßige kontextuelle Filtersteuerelemente festlegen <!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> dann optional [die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). Bei Verwendung dieser Funktion können zusätzliche Gebühren anfallen.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png) ![Integrales Ad-Science-Logo](/help/dsp/assets/ias-logo.png) ![Peer39-Logo](/help/dsp/assets/peer39-logo.png)

### Sperren von Betrug vor dem Bid

Nutzen Sie unsere Drittanbieterintegrationen mit [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39], um nicht-menschlichen Traffic aus Ihren Kampagnen zu blockieren. Diese Integrationen bieten branchenführende Funktionen zum Sperren von Angeboten, um sowohl allgemeinen als auch komplexen ungültigen Traffic (GIVT und SIVT) in Ihren Kampagnen zu minimieren.

Sie können für jeden Werbetreibenden standardmäßige Steuerelemente zum Blockieren von Betrug vor Angeboten festlegen <!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> dann optional [die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). Bei Verwendung dieser Funktion können zusätzliche Gebühren anfallen.

Weitere Informationen zur Funktionalität erhalten Sie direkt von Ihrem bevorzugten Anbieter oder von Ihrem Adobe-Account-Team.

![DoubleVerify Logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science Logo](/help/dsp/assets/ias-logo.png) ![Peer39 logo](/help/dsp/assets/peer39-logo.png)

### Sichtbarkeit vor Gebot {#pre-bid-viewability}

Mit Pre-Bid-Sichtbarkeitsfiltern, die von unseren branchenführenden Partnern [!DNL DoubleVerify] und [!DNL Integral Ad Science] unterstützt werden, können Werbetreibende sicherstellen, dass ihre Kampagnen die gewünschten Sichtbarkeitsleistungsziele im gesamten Video- und Display-Inventar erfüllen.

Sie können für jeden Advertiser standardmäßige Sichtbarkeitsfilter festlegen <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> dann optional [die Einstellungen für jede Platzierung anpassen](/help/dsp/campaign-management/placements/placement-settings.md). Bei Verwendung dieser Funktion können zusätzliche Gebühren anfallen.

![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png) ![Integrales Ad-Science-Logo](/help/dsp/assets/ias-logo.png)

### Zielgruppenbestimmung und Messung der Aufmerksamkeit

[!DNL Adobe's] Partnerschaft mit [!DNL Adelaide] bietet Werbetreibenden Unterstützung für die Adelaide-Metrik &quot;[!DNL Attention Units]&quot;, die die Medienqualität anhand von Eye-Tracking-, Belichtungs- und Ergebnisdaten misst.

[Zielgruppenbestimmung auf Platzierungs-Ebene vor Angeboten](/help/dsp/campaign-management/placements/placement-settings.md) ermöglicht es Werbetreibenden, bestimmte Aufmerksamkeitsstufen anzusprechen, um die Kundeninteraktion zu verbessern.

Darüber hinaus können Advertiser das [Tracking für die [!UICONTROL Attention Score]-Metrik auf Platzierungsebene](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (die gewichtete durchschnittliche Anzahl der [!DNL Attention Units] über Impressionen hinweg) für jede Kampagne aktivieren, um zu verstehen, welche Platzierungstaktiken die besten Geschäftsergebnisse erzielen.

Für jede einzelne Funktion fallen zusätzliche Gebühren an.

### Themen-Targeting

Mit DSP-Themen-Targeting können Sie Keyword-Listen durch die Nutzung unserer branchenführenden kontextuellen [!DNL Comscore] ansprechen oder blockieren. Mit dem Thema-Targeting können Sie sicherstellen, dass Ihre Anzeigen immer in einer Umgebung geschaltet werden, die Ihrer Marke entspricht, unabhängig davon, ob dies die Blockierung schädlicher Inhalte oder die Sicherstellung von Ausgaben in einem Kontext umfasst, der ein besseres Ergebnis gewährleistet.

Beim Themen-Targeting müssen Sie benutzerdefinierte Themensegmente direkt mit der Partnerplattform erstellen. Nachdem die Segmente erstellt wurden, können Sie [für jede Platzierung eine Segment-ID im [!UICONTROL Audience Targeting] Abschnitt ansprechen oder &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md). Für diese Funktion können zusätzliche Gebühren anfallen.

Um ein [!DNL Comscore] Konto zu erstellen und benutzerdefinierte Themensegmente zu erstellen, können Sie unter [https://agents.comscore.com eine Anmeldung zur [!DNL Activation Segment Manager] anfordern](https://agents.comscore.com). Vollständige Anweisungen [[!DNL Comscore]  Einrichten benutzerdefinierter Segmente finden Sie &#x200B;](https://comscoreactivation.zendesk.com/hc/) Hilfezentrum . Gebühren für benutzerdefinierte Segmente sind in [!DNL Segment Manager] sichtbar, während Sie sie erstellen.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP ist eine Partnerschaft mit [!DNL DoubleVerify] eingegangen, um seine [!DNL Authentic Brand Safety] Targeting-Lösung anzubieten, mit der Sie eine Reihe zentralisierter Anforderungen an die Markensicherheit erstellen können, die auf allen Ihren Einkaufsplattformen zur Konsistenz berücksichtigt werden.

Nachdem Sie ein [!DNL DoubleVerify] Markensegment mit der erforderlichen Zielgruppenbestimmung erstellt haben, können Sie es in DSP verwenden, um Ihre Blockierungsregeln nach Angebotsabgabe mit Pre-Bid in Web-Umgebungen zu replizieren.

Sie können für jeden Advertiser eine [!DNL DoubleVerify] Segment-ID <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> und dann optional [Aktivieren oder Deaktivieren von [!UICONTROL Authentic Brand Safety] für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). DSP stellt Ihrem Konto die Nutzung für die Segment-ID in Rechnung.

Weitere Informationen zu Funktionen erhalten Sie direkt bei [!DNL DoubleVerify] oder bei Ihrem Adobe-Account-Team.

![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
