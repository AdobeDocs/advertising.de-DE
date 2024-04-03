---
title: Von verwendete Adobe Advertising-IDs [!DNL Analytics]
description: Von verwendete Adobe Advertising-IDs [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 9374f5ef6aaff1f638022bc878c7af190e31888f
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# Von verwendete Adobe Advertising-IDs [!DNL Analytics]

*Advertiser mit nur Adobe Advertising-Adobe Analytics-Integration*

*Anwendbar auf Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising verwendet zwei IDs für das On-site-Performance-Tracking: die *EF ID* und *AMO-ID*.

Wenn eine Ad-Impression auftritt, erstellt Adobe Advertising die AMO-ID- und EF-ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, auf die Site gelangt, ohne auf eine Anzeige zu klicken, [!DNL Analytics] ruft diese Werte von Adobe Advertising über auf. [!DNL Analytics for Advertising] JavaScript-Code. Für Durchsichts-Traffic: [!DNL Analytics] generiert eine zusätzliche ID (`SDID`), das zum Zuordnen der EF ID und AMO ID zu verwendet wird [!DNL Analytics]. Für Clickthrough-Traffic werden diese IDs mithilfe der `ef_id` und `s_kwcid` (für die AMO-ID) Abfragezeichenfolgenparameter.

Adobe Advertising unterscheidet unter Verwendung der folgenden Kriterien zwischen einem Clickthrough- oder Durchsichtseintrag auf der Website:

* Ein Durchsichtseintrag wird erfasst, wenn ein Benutzer die Site besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] erfasst eine Durchsicht, wenn zwei Bedingungen erfüllt sind:

   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] oder [!DNL Search, Social, & Commerce] Anzeige während der [Lookback-Fenster](#lookback-a4adc).

   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während der [Impression-Lookback-Fenster](#lookback-a4adc). Die letzte Impression wird als Durchsicht übergeben.

* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen eintritt:

   * Die URL enthält eine EF ID und eine AMO ID, die von Adobe Advertising zur Landingpage-URL hinzugefügt wurden.

   * Die URL enthält keine Trackingcodes, aber der Adobe Advertising-JavaScript-Code erkennt innerhalb der letzten zwei Minuten einen Klick.

![Adobe Advertising-Ansicht-basiert [!DNL Analytics] Integration](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Adobe Advertising-Ansicht-basiert [!DNL Analytics] Integration*

![Adobe Advertising klickt auf URL-basiert [!DNL Analytics] Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: Adobe Advertising-Klick URL-basiert [!DNL Analytics] Integration*

## Adobe Advertising EF IDs

Die EF-ID ist ein eindeutiges Token, mit dem Adobe Advertising Aktivitäten mit einem Online-Klick oder einer Anzeige verknüpft. Die EF ID wird in [ein [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder [!DNL rVar] (reserviert [!DNL eVar]) (Adobe Advertising EF ID) und verfolgt jeden Anzeigenklick oder jede Anzeige auf der Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel zum Senden [!DNL Analytics] Daten an Adobe Advertising zur Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

### EF ID Format

>[!NOTE]
>
>Bei EF IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics] -Implementierung erzwingt das URL-Tracking in Kleinbuchstaben. Anschließend erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf Adobe Advertising-Gebote und -Berichte aus, hat jedoch keine Auswirkungen auf die Adobe Advertising-Berichterstellung innerhalb von [!DNL Analytics].

#### [!DNL Google Ads] Suchanzeigen

```
{gclid}:G:s
```

wobei:

* `gclid` ist die [!DNL Google Click ID] (GCLID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### [!DNL Microsoft Advertising] Suchanzeigen

```
{msclkid}:G:s
```

wobei:

* `msclkid` ist die [!DNL Microsoft Click ID] (MSCLKID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### Anzeigen und Suchanzeigen in anderen Suchmaschinen anzeigen

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

wobei:

* &lt;*Adobe Advertising-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. &quot;ÄhKVaAAABCkJ0mDt&quot;). Auch als *Surfer-ID*.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTDDHHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19):25:33).

* &lt;*Kanaltyp*> ist der Kanaltyp, der für den Klick oder die Belichtung verantwortlich ist:

   * `d` für einen Klick auf eine DSP Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Durchsuchen-Clickthrough).

Beispiel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Die EF ID-Dimension in [!DNL Analytics]

In [!DNL Analytics] Berichte, können Sie EF ID-Daten finden, indem Sie nach der [!UICONTROL EF ID] Dimension und unter Verwendung der [!UICONTROL EF ID Instance] Metrik.

EF-IDs unterliegen in Analysis Workspace der Grenze von 500.000 eindeutigen Kennungen. Sobald der Wert von 500.000 erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Elementtitel gemeldet.[!UICONTROL Low Traffic].&quot; Da die Möglichkeit besteht, dass die Berichtstreue fehlt, werden die EF-IDs nicht klassifiziert und sollten Sie sie nicht für Segmente oder Berichte in [!DNL Analytics].

## Adobe Advertising AMO-IDs {#amo-id}

Die AMO-ID verfolgt jede eindeutige Anzeigenkombination auf einer weniger detaillierten Ebene und wird für [!DNL Analytics] Datenklassifizierung und Erfassung von Werbemetriken (wie Impressionen, Klicks und Kosten) von Adobe Advertising. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder rVar-Dimension (AMO-ID) und wird ausschließlich für die Berichterstellung in [!DNL Analytics].

Die AMO-ID wird auch als `s_kwcid`, der manchmal als &quot;[!DNL the squid].&quot;

### Methoden zur Implementierung der AMO-ID {#amo-id-implement}

Der Parameter wird Ihren Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Wenn die serverseitige Einfügefunktion implementiert ist.

   * DSP: Der Pixelserver hängt den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer eine Display-Anzeige mit dem Adobe Advertising-Pixel anzeigt.

   * Kunden von Search, Social und Commerce:

      * Für [!DNL Google Ads] und [!DNL Microsoft® Advertising] Konten mit [!UICONTROL Auto Upload] Wenn für das Konto oder die Kampagne aktiviert ist, hängt der Pixelserver den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer auf eine Anzeige mit dem Adobe Advertising-Pixel klickt.

      * für andere Werbenetzwerke oder [!DNL Google Ads] und [!DNL Microsoft® Advertising] Konten mit [!UICONTROL Auto Upload] Einstellung deaktiviert festlegen, fügen Sie den Parameter manuell zu Ihrer [Anlagenparameter auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, die sie an Ihre Basis-URLs anhängen.

* Wenn die serverseitige Einfügefunktion nicht implementiert ist:

   * DSP Kunden: Die [JavaScript-Code](javascript.md) erfasst automatisch Clickthroughs und Durchsichten. Wenn ein Browser keine Drittanbieter-Cookies unterstützt, können Sie trotzdem klick-basierte Konversionen für die folgenden Anzeigentypen verfolgen:

      * Für [!DNL Flashtalking] Anzeigen-Tags, manuelles Einfügen zusätzlicher Makros pro[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Für [!DNL Google Campaign Manager 360] Anzeigen-Tags, manuelles Einfügen zusätzlicher Makros pro[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Kunden von Search, Social und Commerce:

      * Für ([!DNL Google Ads] und [!DNL Microsoft® Advertising]) Anzeigen hinzufügen, fügen Sie den AMO ID-Parameter manuell zu den Suffixen Ihrer Landingpage hinzu, idealerweise bei der [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich.

      * Fügen Sie bei Anzeigen in allen anderen Werbenetzwerken den Parameter AMO ID manuell zu Ihrem [Anlagenparameter auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, die sie an Ihre Basis-URLs anhängen.

Wenden Sie sich an Ihr Adobe Account Team, um die serverseitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu bestimmen.

### AMO-ID-Formate {#amo-id-formats}

#### AMO-ID-Format für [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

wobei:

* `AC` zeigt den Anzeigekanal an.

* `{TM_AD_ID}` ist der von der Adobe Advertising generierte alphanumerische Anzeigenschlüssel. Sie wird als eindeutige ID für eine Anzeige verwendet und dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

* `{TM_PLACEMENT_ID}` ist der von der Adobe Advertising generierte alphanumerische Platzierungsschlüssel. Sie wird als eindeutige Kennung für eine Platzierung verwendet und dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-ID-Formate für Such-, Social- und Commerce-Anzeigen {#amo-id-format-search}

Die Parameter variieren je nach Anzeigennetzwerk, doch die folgenden Parameter sind für alle gemeinsam:

* `AL` zeigt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen wird.

* `{sid}` wird durch die numerische ID des Anzeigennetzwerkkontos des Werbetreibenden ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver], *88* für [!DNL Baidu], *90* für [!DNL Yandex], *94* für [!DNL Yahoo! Japan Ads], *105* für [!DNL Yahoo Native] (veraltet) oder *106* für [!DNL Pinterest] (nicht mehr unterstützt).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

wobei:

* `{creative}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativelement.
* `{placement}` ist die Website, auf der auf die Anzeige geklickt wurde.
* `{keywordid}` ist die eindeutige numerische ID des Anzeigennetzwerks für den Suchbegriff, der die Anzeige ausgelöst hat.

##### [!DNL Google Ads]

Dazu gehören auch Einkaufskampagnen mit [!DNL Google Merchant Center].

* Konten, die das neueste AMO-ID-Format verwenden, das Berichte auf Kampagnen- und Anzeigengruppenebene für Kampagnen- und Experimentkampagnen zur Leistungssteigerung unterstützt:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle anderen Konten:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

wobei:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` ist die [!DNL Google Ads] eindeutige numerische ID für das Kreativ.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `e` exakt, `p` für Wortgruppe oder `b` für einen breiten Bereich.
* `{placement}` ist der Domänenname der Website, auf der auf die Anzeige geklickt wurde. Ein Wert ist für Anzeigen in platzierungszielgerichteten Kampagnen und für Anzeigen in auf Suchbegriffe ausgerichteten Kampagnen verfügbar, die auf Inhalts-Sites angezeigt werden.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte: `g` für [!DNL Google] Suche (nur für Anzeigen mit Keyword-Targeting), `s` für einen Suchpartner (nur für Anzeigen mit Keyword-Targeting) oder `d` für das Display-Netzwerk (für Anzeigen mit Keyword oder Platzierungszielgruppe).
* `{product_partition_id}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Produktgruppe, die mit Produktanzeigen verwendet wird.
* `{keyword}` ist entweder der spezifische Suchbegriff, der Ihre Anzeige ausgelöst hat (auf Suchseiten) oder der beste Suchbegriff (auf Inhalts-Sites).
* `{campaignid}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Kampagne.
* `{adgroupid}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Anzeigengruppe.

>[!NOTE]
>
>* Für dynamische Suchanzeigen: {keyword} mit dem automatischen Ziel gefüllt.
>* Wenn Sie das Tracking für [!DNL Google] Shopping-Anzeigen, ein Produkt-ID-Parameter, `{adwords_producttargetid}`wird vor dem Suchbegriffparameter eingefügt. Der Produkt-ID-Parameter wird nicht im [!DNL Google Ads] Tracking-Parameter auf Kontoebene und Kampagnenebene.
>* Informationen zur Verwendung des neuesten AMO-ID-Trackingcodes finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für eine [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Suchkampagnen:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Shopping-Kampagnen (mit [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Zielgruppennetzwerkkampagnen:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

wobei:

* `{AdId}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativelement.
* `{OrderItemId}` ist die numerische ID des Anzeigennetzwerks für den Suchbegriff.
* `{CriterionId}` ist die numerische ID des Anzeigennetzwerks für die Produktgruppe, die mit Produktanzeigen verwendet wird.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

wobei:

* `{creative}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativelement.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `be` exakt, `bp` für Wortgruppe oder `bb` für einen breiten Bereich.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte: `n` für native oder `s` für die Suche.
* `{keyword}` ist das Keyword, das Ihre Anzeige ausgelöst hat.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

wobei:

* `{ad_id}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativelement.
* `{source_type}` ist der Typ der Website, auf der die Anzeige angezeigt wurde: *b* für die Suche, *c* für Kontext (Inhalt) oder *ct* für Kategorie.
* `{phrase_id}` ist die numerische ID des Anzeigennetzwerks für den Suchbegriff.

### AMO-ID-Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der [!UICONTROL AMO ID] Dimension und unter Verwendung der [!UICONTROL AMO ID Instances] Metrik. Die [!UICONTROL AMO ID] -Dimension enthält alle erfassten AMO-ID-Werte, während die [!UICONTROL AMO ID Instances] gibt an, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise dieselbe Suchanzeige viermal angeklickt wurde, Analytics jedoch sieben Site-Einträge verfolgt hat, wird [!UICONTROL AMO ID Instances] wäre sieben (7) und [!UICONTROL Clicks] wäre vier (4).

Für alle Berichte oder Prüfungen innerhalb von [!DNL Analytics]Best Practice ist, die AMO-ID zusammen mit der entsprechenden Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[Validierung von Clickthrough-Daten für [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;in &quot;Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising.&quot;

## Informationen zu Analytics Classifications

In [!DNL Analytics], a [Classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) ist ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Adobe Advertising kategorisiert die Adobe Advertising von Rohdaten mithilfe von Klassifizierungen, damit Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagnen). Klassifizierungen bilden die Grundlage für Adobe Advertising-Reporting in [!DNL Analytics] und kann mit den AMO-Metriken verwendet werden, z. B. [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions], und [!UICONTROL AMO Clicks]sowie mit benutzerspezifischen und standardmäßigen On-site-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], und [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)
