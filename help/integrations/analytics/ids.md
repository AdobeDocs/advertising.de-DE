---
title: Von  [!DNL Analytics] verwendete Adobe Advertising-IDs
description: Von  [!DNL Analytics] verwendete Adobe Advertising-IDs
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dc99c7b6d1383fdc4a3b7fb59bfded0cec6b917a
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 0%

---

# Von [!DNL Analytics] verwendete Adobe Advertising-IDs

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

*Gilt für Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising verwendet zwei IDs für die On-site-Leistungsverfolgung: die *EF ID* und die *AMO ID*.

Wenn eine Ad-Impression auftritt, erstellt Adobe Advertising die AMO-ID- und EF-ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, auf die Site gelangt, ohne auf eine Anzeige zu klicken, ruft [!DNL Analytics] diese Werte von der Adobe Advertising über den JavaScript-Code [!DNL Analytics for Advertising] auf. Für Durchsichts-Traffic generiert [!DNL Analytics] eine zusätzliche ID (`SDID`), die zum Zuordnen der EF ID und AMO ID in [!DNL Analytics] verwendet wird. Für Clickthrough-Traffic werden diese IDs mithilfe der Abfragezeichenfolgenparameter `ef_id` und `s_kwcid` (für die AMO-ID) in die URL der Landingpage aufgenommen.

Adobe Advertising unterscheidet unter Verwendung der folgenden Kriterien zwischen einem Clickthrough- oder Durchsichtseintrag auf der Website:

* Ein Durchsichtseintrag wird erfasst, wenn ein Benutzer die Site besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] zeichnet eine Durchsicht auf, wenn zwei Bedingungen erfüllt sind:

   * Der Besucher hat während des [Klick-Lookback-Fensters](#lookback-a4adc) keine Clickthroughs für eine [!DNL DSP] - oder [!DNL Search, Social, & Commerce] -Anzeige.

   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während des [Impression-Lookback-Fensters](#lookback-a4adc) gesehen. Die letzte Impression wird als Durchsicht übergeben.

* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen eintritt:

   * Die URL enthält eine EF ID und eine AMO ID, die von Adobe Advertising zur Landingpage-URL hinzugefügt wurden.

   * Die URL enthält keine Trackingcodes, aber der Adobe Advertising JavaScript-Code erkennt einen Klick innerhalb der letzten zwei Minuten.

![Adobe Advertising-ansichtsbasierte [!DNL Analytics] Integration](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Adobe Advertising-Ansichtsbasierte [!DNL Analytics] Integration*

![Adobe Advertising Klick auf URL-basierte [!DNL Analytics] Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: Adobe Advertising Klick auf URL-basierte [!DNL Analytics] Integration*

## Adobe Advertising EF IDs

Die EF-ID ist ein eindeutiges Token, mit dem Adobe Advertising Aktivitäten mit einem Online-Klick oder einer Anzeige verknüpft. Die EF ID wird in der Dimension [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder [!DNL rVar] (reservierte [!DNL eVar]) gespeichert (Adobe Advertising EF ID) und verfolgt jeden Anzeigenklick oder jede Anzeige auf der Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel zum Senden von [!DNL Analytics] -Daten an Adobe Advertising zur Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

### EF ID Format

>[!NOTE]
>
>Bei EF IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine Implementierung von [!DNL Analytics] das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf Adobe Advertising-Gebote und -Berichte aus, hat jedoch keine Auswirkungen auf die Adobe Advertising-Berichterstellung innerhalb von [!DNL Analytics].

#### [!DNL Google Ads] Suchanzeigen

```
{gclid}:G:s
```

wobei:

* `gclid` ist der [!DNL Google Click ID] (GCLID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### [!DNL Microsoft Advertising] Suchanzeigen

```
{msclkid}:G:s
```

wobei:

* `msclkid` ist der [!DNL Microsoft Click ID] (MSCLKID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### Anzeigen und Suchanzeigen in anderen Suchmaschinen anzeigen

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

wobei:

* &lt;*Adobe Advertising-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. &quot;ÄhKVaAAABCkJ0mDt&quot;). Auch *Surfer-ID* genannt.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTDDHHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19:25:33).

* &lt;*Kanaltyp*> ist der für den Klick oder die Belichtung verantwortliche Kanaltyp:

   * `d` für einen Klick auf eine DSP Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Suchklicks).

Beispiel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Die EF ID-Dimension in [!DNL Analytics]

In [!DNL Analytics] -Berichten können Sie EF-ID-Daten finden, indem Sie nach der Dimension [!UICONTROL EF ID] suchen und die Metrik [!UICONTROL EF ID Instance] verwenden.

EF-IDs unterliegen in Analysis Workspace der Grenze von 500.000 eindeutigen Kennungen. Sobald der Wert von 500.000 erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Elementtitel &quot;[!UICONTROL Low Traffic]&quot;gemeldet. Da die Möglichkeit besteht, dass die Berichttreue fehlt, werden die EF-IDs nicht klassifiziert und sollten Sie sie nicht für Segmente oder Berichte in [!DNL Analytics] verwenden.

## Adobe Advertising AMO-IDs {#amo-id}

Die AMO-ID verfolgt jede eindeutige Anzeigenkombination auf einer weniger detaillierten Ebene und wird für die [!DNL Analytics] -Datenklassifizierung und Erfassung von Werbedetriken (wie Impressionen, Klicks und Kosten) von Adobe Advertising verwendet. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) - oder rVar-Dimension (AMO-ID) gespeichert und wird ausschließlich für die Berichterstellung in [!DNL Analytics] verwendet.

Die AMO-ID wird auch als `s_kwcid` bezeichnet, was manchmal als &quot;[!DNL squid]&quot;ausgesprochen wird.

### Methoden zur Implementierung der AMO-ID {#amo-id-implement}

Der Parameter wird Ihren Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Wenn die serverseitige Einfügefunktion implementiert ist.

   * DSP: Der Pixelserver hängt den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer eine Display-Anzeige mit dem Adobe Advertising-Pixel anzeigt.

   * Kunden von Search, Social und Commerce:

      * Bei [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Konten mit aktivierter Einstellung [!UICONTROL Auto Upload] für das Konto oder die Kampagne hängt der Pixelserver den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer auf eine Anzeige mit dem Adobe Advertising-Pixel klickt.

      * Bei anderen Anzeigennetzwerken oder [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit deaktivierter Einstellung [!UICONTROL Auto Upload] fügen Sie den Parameter manuell zu Ihren angehängten Parametern auf [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

* Wenn die serverseitige Einfügefunktion nicht implementiert ist:

   * DSP Kunden: Der [JavaScript-Code](javascript.md) zeichnet Clickthroughs und Durchsichten automatisch auf. Wenn ein Browser keine Drittanbieter-Cookies unterstützt, können Sie trotzdem klick-basierte Konversionen für die folgenden Anzeigentypen verfolgen:

      * Fügen Sie für Anzeigen-Tags vom Typ &quot;[!DNL Flashtalking]&quot;manuell zusätzliche Makros pro &quot;[Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md)&quot;ein.

      * Fügen Sie für Anzeigen-Tags vom Typ &quot;[!DNL Google Campaign Manager 360]&quot;manuell zusätzliche Makros pro &quot;[Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;ein.

   * Kunden von Search, Social und Commerce:

      * Fügen Sie bei Anzeigen ([!DNL Google Ads] und [!DNL Microsoft Advertising]) den AMO-ID-Parameter manuell zu den Suffixen Ihrer Landingpage hinzu, idealerweise auf der [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, es sei denn, es ist ein anderes Tracking für einzelne Kontokomponenten erforderlich.

      * Fügen Sie bei Anzeigen in allen anderen Werbenetzwerken den AMO-ID-Parameter manuell zu Ihren [Anlagenparametern auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

Wenden Sie sich an Ihr Adobe Account Team, um die serverseitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu bestimmen.

### AMO-ID-Formate {#amo-id-formats}

#### AMO-ID-Format für [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

wobei:

* `AC` gibt den Anzeigekanal an.

* `{TM_AD_ID}` ist der von der Adobe Advertising generierte alphanumerische Anzeigenschlüssel. Sie wird als eindeutige ID für eine Anzeige verwendet und dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics] -Dimensionen.

* `{TM_PLACEMENT_ID}` ist der von der Adobe Advertising generierte alphanumerische Platzierungsschlüssel. Sie wird als eindeutige Kennung für eine Platzierung verwendet und dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics]-Dimensionen.

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-ID-Formate für Such-, Social- und Commerce-Anzeigen {#amo-id-format-search}

Die Parameter variieren je nach Anzeigennetzwerk, doch die folgenden Parameter sind für alle gemeinsam:

* `AL` gibt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen ist.

* `{sid}` wird durch die numerische ID für das Anzeigen-Netzwerkkonto des Advertisers ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver]. *88* für [!DNL Baidu], *90* für [!DNL Yandex], *94* für [!DNL Yahoo! Japan Ads], *105* für [!DNL Yahoo Native] (veraltet) oder *106{2 9} für [!DNL Pinterest] (nicht mehr unterstützt).*

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

wobei:

* `{creative}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativteam.
* `{placement}` ist die Website, auf der auf die Anzeige geklickt wurde.
* `{keywordid}` ist die eindeutige numerische ID des Anzeigennetzwerks für den Suchbegriff, der die Anzeige ausgelöst hat.

##### [!DNL Google Ads]

Dazu gehören Einkaufskampagnen mit [!DNL Google Merchant Center].

* Konten, die das neueste AMO-ID-Format verwenden, das Berichte auf Kampagnen- und Anzeigengruppenebene für Kampagnen- und Experimentkampagnen zur Leistungssteigerung unterstützt:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle anderen Konten:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

wobei:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` ist die eindeutige numerische ID [!DNL Google Ads] für den Kreativschaffenden.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `e` für exakt, `p` für eine Wortgruppe oder `b` für einen breiten Bereich.
* `{placement}` ist der Domänenname der Website, auf der auf die Anzeige geklickt wurde. Ein Wert ist für Anzeigen in platzierungszielgerichteten Kampagnen und für Anzeigen in auf Suchbegriffe ausgerichteten Kampagnen verfügbar, die auf Inhalts-Sites angezeigt werden.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte: `g` Suche nach [!DNL Google] Anzeigen (nur für Anzeigen mit Keyword-Targeting), `s` Suche nach einem Suchpartner (nur für Anzeigen mit Keyword) oder `d` Anzeige im Display-Netzwerk (für Anzeigen mit Keyword oder Platzierungszielgruppe).
* `{product_partition_id}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Produktgruppe, die mit Produktanzeigen verwendet wird.
* `{keyword}` ist entweder der spezifische Suchbegriff, der Ihre Anzeige ausgelöst hat (auf Suchseiten), oder der am besten übereinstimmende Suchbegriff (auf Inhalts-Sites).
* `{campaignid}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Kampagne.
* `{adgroupid}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Anzeigengruppe.

>[!NOTE]
>
>* Bei dynamischen Suchanzeigen wird {keyword} mit dem automatischen Ziel ausgefüllt.
>* Wenn Sie das Tracking für [!DNL Google] -Shopping-Anzeigen generieren, wird vor dem Suchbegriff-Parameter der Produkt-ID-Parameter `{adwords_producttargetid}` eingefügt. Der Parameter für die Produkt-ID wird nicht in den Tracking-Parametern auf Kontoebene und Kampagnenebene angezeigt.[!DNL Google Ads]
>* Informationen zur Verwendung des neuesten AMO-ID-Trackingcodes finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für ein [!DNL Google Ads] Konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)&quot;<!-- Update terminology there too. -->.

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Alle Kampagnentypen:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

wobei:

* `{AdId}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativteam.
* `{OrderItemId}` ist die numerische ID des Anzeigennetzwerks für den Suchbegriff.
* `{CampaignId}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Kampagne.
* `{AdGroupId}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Anzeigengruppe.

>[!NOTE]
>
>Alle Konten mit Kampagnen mit Leistungsmax wurden in das obige Format migriert. Bei Konten mit anderen Kampagnentypen werden die Suffixe Ihrer Landingpage so migriert, dass sie das neue s_kwcid-Format bis Anfang 2025 verwenden. In der Zwischenzeit funktionieren die Legacy-Formate wie folgt weiterhin:
>* Suchkampagnen:
>  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shopping-Kampagnen (mit [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`
>* Zielgruppennetzwerkkampagnen:
>  `s_kwcid=AL!{userid}!{sid}!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

wobei:

* `{creative}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativteam.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `be` für exakt, `bp` für eine Wortgruppe oder `bb` für einen breiten Bereich.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte: `n` für native Suche oder `s` für Suche.
* `{keyword}` ist das Keyword, das Ihre Anzeige ausgelöst hat.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

wobei:

* `{ad_id}` ist die eindeutige numerische ID des Anzeigennetzwerks für das Kreativteam.
* `{source_type}` ist der Typ der Site, auf der die Anzeige angezeigt wurde: *b* für die Suche, *c* für den Kontext (Inhalt) oder *ct* für die Kategorie.
* `{phrase_id}` ist die numerische ID des Anzeigennetzwerks für den Suchbegriff.

### AMO-ID-Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der Dimension [!UICONTROL AMO ID] suchen und die Metrik [!UICONTROL AMO ID Instances] verwenden. Die Dimension [!UICONTROL AMO ID] enthält alle erfassten AMO-ID-Werte, während die Metrik [!UICONTROL AMO ID Instances] angibt, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise dieselbe Suchanzeige viermal angeklickt wurde, Analytics jedoch sieben Site-Einträge verfolgt hat, wäre [!UICONTROL AMO ID Instances] sieben (7) und [!UICONTROL Clicks] vier (4).

Für alle Berichte oder Prüfungen innerhalb von [!DNL Analytics] ist es Best Practice, die AMO-ID zusammen mit der zugehörigen Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[Clickthrough-Datenvalidierung für [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;in &quot;Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising&quot;.

## Informationen zu Analytics Classifications

In [!DNL Analytics] ist eine [Klassifizierung](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Adobe Advertising kategorisiert die Adobe Advertising von Rohdaten mithilfe von Klassifizierungen, damit Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagnen). Klassifizierungen bilden die Grundlage für Adobe Advertising-Berichte in [!DNL Analytics] und können mit den AMO-Metriken wie [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] und [!UICONTROL AMO Clicks] sowie mit benutzerspezifischen und standardmäßigen On-site-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] und [!UICONTROL Revenue] verwendet werden.

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)
