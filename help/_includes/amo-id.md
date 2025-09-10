---
source-git-commit: 2b719e00418010b1f8e21b8956ad55b2ffc7dee1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---
# Adobe Advertising AMO-IDs

## Adobe Advertising AMO-IDs {#amo-id}

Die AMO ID verfolgt jede einzelne Anzeigenkombination auf einer weniger detaillierten Ebene und wird für die [!DNL Analytics] und Customer Journey Analytics-Datenklassifizierung und die Aufnahme von Werbemetriken (wie Impressionen, Klicks und Kosten) aus Adobe Advertising verwendet.

[!DNL Analytics] wird die AMO-ID in einer [eVar- oder ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)-Dimension (AMO-ID) gespeichert.

Bei Customer Journey Analytics wird die AMO-ID in der `trackingCode`-Eigenschaft des `conversionDetails`-Objekts gespeichert, das Teil der [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ist.

Die AMO-ID wird auch als `s_kwcid` bezeichnet, was manchmal als &quot;[!DNL squid]&quot; ausgesprochen wird.

### AMO-ID-Formate {#amo-id-formats}

#### AMO-ID-Format für [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

Dabei gilt:

* `AC` zeigt den Anzeigekanal an.

* `{TM_AD_ID}` ist der von Adobe Advertising generierte alphanumerische Anzeigenschlüssel. Sie wird als eindeutige Kennung für eine Anzeige verwendet und dient als Schlüssel zur Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics]- und Customer Journey Analytics-Dimensionen.

* `{TM_PLACEMENT_ID}` ist der von Adobe Advertising generierte alphanumerische Platzierungsschlüssel. Sie wird als eindeutige Kennung für eine Platzierung verwendet und dient als Schlüssel zur Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics]- und Customer Journey Analytics-Dimensionen.

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-ID-Formate für Search-, Social- und Commerce-Anzeigen {#amo-id-format-search}

Die Parameter variieren je nach Anzeigennetzwerk, aber die folgenden Parameter sind für alle gleich:

* `AL` gibt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen ist.

* `{sid}` wird durch die numerische ID für das Werbenetzwerkkonto des Werbetreibenden ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver], *888* für [!DNL Baidu], *90* für [!DNL Yandex], *94*, [!DNL Yahoo! Japan Ads]105für *(nicht mehr unterstützt), oder* 106[!DNL Yahoo Native] ** [!DNL Pinterest] (nicht mehr unterstützt).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

Dabei gilt:

* `{creative}` ist die eindeutige numerische ID des Werbenetzwerks für den Kreativen.
* `{placement}` ist die Website, auf die die Anzeige geklickt wurde.
* `{keywordid}` ist die eindeutige numerische ID des Werbenetzwerks für das Keyword, das die Anzeige ausgelöst hat.

##### [!DNL Google Ads]

Dazu gehören Shopping-Kampagnen mit [!DNL Google Merchant Center].

* Konten, die das neueste AMO ID-Format verwenden, das Reporting auf Kampagnen- und Anzeigengruppenebene für Kampagnen, Entwürfe und Experimente sowie Kampagnen mit dem Typ „Performance Max“ unterstützt:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle anderen Konten:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

Dabei gilt:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` ist die [!DNL Google Ads] eindeutige numerische ID für den Kreativen.
* `{matchtype}` ist der „matchType“-Wert des Keywords, das die Anzeige ausgelöst hat: &quot;`e`&quot; für „exact“, &quot;`p`&quot; für „phrase“ oder &quot;`b`&quot; für „broad“.
* `{placement}` ist der Domain-Name der Website, auf die die Anzeige geklickt wurde. Für Anzeigen in auf Platzierungen ausgerichteten Kampagnen und für Anzeigen in auf Keywords ausgerichteten Kampagnen, die auf Inhalts-Sites angezeigt werden, ist ein -Wert verfügbar.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgt ist: `g` für [!DNL Google] Suche (nur für auf Keywords zielende Anzeigen), `s` für einen Suchpartner (nur für auf Keywords zielende Anzeigen) oder `d` für das Display-Netzwerk (entweder für auf Keywords zielende oder auf Platzierungen zielende Anzeigen).
* `{product_partition_id}` ist die eindeutige numerische ID des Werbenetzwerks für die mit Produktanzeigen verwendete Produktgruppe.
* `{keyword}` ist entweder das spezifische Keyword, das Ihre Anzeige ausgelöst hat (auf Such-Sites), oder das am besten übereinstimmende Keyword (auf Inhalts-Sites).
* `{campaignid}` ist die eindeutige numerische ID des Werbenetzwerks für die Kampagne.
* `{adgroupid}` ist die eindeutige numerische ID des Anzeigennetzwerks für die Anzeigengruppe.

>[!NOTE]
>
>* Bei dynamischen Suchanzeigen wird {keyword} mit dem automatischen Targeting gefüllt.
>* Wenn Sie Tracking für [!DNL Google] Shopping-Anzeigen generieren, wird ein Produkt-ID-Parameter `{adwords_producttargetid}` vor dem Schlüsselwortparameter eingefügt. Der Produkt-ID-Parameter wird nicht in den Tracking-Parametern auf Konto- und Kampagnenebene auf [!DNL Google Ads] angezeigt.
>* Informationen zur Verwendung des neuesten AMO-ID-Trackingcodes finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für ein  [!DNL Google Ads] -](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* All campaign types:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

Dabei gilt:

* `{AdId}` ist die eindeutige numerische ID des Werbenetzwerks für den Kreativen.
* `{OrderItemId}` ist die numerische ID des Werbenetzwerks für das Keyword .
* `{CampaignId}` ist die eindeutige numerische ID des Werbenetzwerks für die Kampagne.
* `{AdGroupId}` ist die eindeutige numerische ID des Werbenetzwerks für die Anzeigengruppe.

>[!NOTE]
>
> Für Konten mit Kampagnen ohne die [!UICONTROL Auto Upload]-Tracking-Option, die noch nicht in das neue Format migriert wurden, aktualisieren Sie manuell jedes Landingpage-Suffix, um das obige Format aufzunehmen.
> &#x200B;>In der Zwischenzeit funktionieren die Legacy-Formate wie folgt weiter:
>* Suchkampagnen:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Einkaufskampagnen (mit [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Audience Network-Kampagnen:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

Dabei gilt:

* `{creative}` ist die eindeutige numerische ID des Werbenetzwerks für den Kreativen.
* `{matchtype}` ist der „matchType“-Wert des Keywords, das die Anzeige ausgelöst hat: &quot;`be`&quot; für „exact“, &quot;`bp`&quot; für „phrase“ oder &quot;`bb`&quot; für „broad“.
* `{network}` gibt das Netzwerk an, von dem aus der Klick erfolgte: `n` für native oder `s` für die Suche.
* `{keyword}` ist das Keyword, das Ihre Anzeige ausgelöst hat.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

Dabei gilt:

* `{ad_id}` ist die eindeutige numerische ID des Werbenetzwerks für den Kreativen.
* `{source_type}` ist der Typ der Site, auf der die Anzeige angezeigt wurde: *b* für die Suche, *c* für den Kontext (Inhalt) oder *ct* für die Kategorie.
* `{phrase_id}` ist die numerische ID des Werbenetzwerks für das Keyword .
