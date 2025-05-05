---
title: Adobe Advertising-IDs verwendet von [!DNL Analytics]
description: Adobe Advertising-IDs verwendet von [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1762'
ht-degree: 0%

---

# Von [!DNL Analytics] verwendete Adobe Advertising-IDs

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

*Gilt für Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising verwendet zwei IDs zur Leistungsüberwachung auf der Site: die *EF ID* und die *AMO ID*.

Wenn eine Ad-Impression auftritt, erstellt Adobe Advertising die AMO ID- und EF ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, die Website betritt, ohne auf eine Anzeige zu klicken, ruft [!DNL Analytics] diese Werte von Adobe Advertising über den [!DNL Analytics for Advertising] JavaScript-Code auf. Für View-Through-Traffic generiert [!DNL Analytics] eine zusätzliche ID (`SDID`), mit der die EF-ID und die AMO-ID [!DNL Analytics] zugeordnet werden. Für Clickthrough-Traffic werden diese IDs mithilfe der Abfragezeichenfolgen-Parameter `ef_id` und `s_kwcid` (für die AMO-ID) in die Landingpage-URL aufgenommen.

Adobe Advertising unterscheidet anhand der folgenden Kriterien zwischen einem Clickthrough- oder einem View-Through-Eintrag auf der Website:

* Ein Viewthrough-Eintrag wird erfasst, wenn ein Benutzer die Website besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] zeichnet eine Durchsicht auf, wenn zwei Bedingungen erfüllt sind:

   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] oder [!DNL Search, Social, & Commerce] Anzeige während des [Click-Lookback-Fensters](#lookback-a4adc).

   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während des Impression[Lookback-Fensters gesehen](#lookback-a4adc). Der letzte Impression wird als Durchsicht weitergegeben.

* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen auftritt:

   * Die URL enthält eine EF-ID und eine AMO-ID, die von Adobe Advertising zur Landingpage-URL hinzugefügt wurden.

   * Die URL enthält keine Trackingcodes, aber der Adobe Advertising JavaScript-Code erkennt innerhalb der letzten zwei Minuten einen Klick.

![Ansichtsbasierte [!DNL Analytics]-Integration von Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Ansichtsbasierte [!DNL Analytics] von Adobe Advertising*

![Adobe Advertising-Klick-URL-basierte [!DNL Analytics]-Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: URL-basierte [!DNL Analytics]-Integration für Adobe Advertising*

## Adobe Advertising EF-IDs

Die EF ID ist ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Werbeunterbrechung zu verknüpfen. Die EF-ID wird in der Dimension [eine [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) oder [!DNL rVar] (reservierte [!DNL eVar]) (Adobe Advertising-EF-ID) gespeichert und verfolgt jeden Anzeigenklick oder jede Offenlegung auf individueller Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel für die Übermittlung von [!DNL Analytics] an Adobe Advertising zur Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

### EF-ID-Format

>[!NOTE]
>
>Bei EF-IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics]-Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf die Adobe Advertising-Gebote und -Berichte aus, hat jedoch keine Auswirkungen auf das Adobe Advertising-Reporting in [!DNL Analytics].

#### [!DNL Google Ads] Suchanzeigen

```
{gclid}:G:s
```

Dabei gilt:

* `gclid` ist die [!DNL Google Click ID] (GCLID).
* `s` ist der Netzwerktyp („s“ für Suche).

#### [!DNL Microsoft Advertising] Suchanzeigen

```
{msclkid}:G:s
```

Dabei gilt:

* `msclkid` ist die [!DNL Microsoft Click ID] (MSCLKID).
* `s` ist der Netzwerktyp („s“ für Suche).

#### Anzeigen und Suchanzeigen in anderen Suchmaschinen anzeigen

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

Dabei gilt:

* &lt;*Adobe Advertising-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. UhKVaAAABCkJ0mDt). Wird auch als &quot;*ID“*.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTT-HHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19:25:33).

* &lt;*channel type*> ist der Kanaltyp, der für das Klicken oder Belichten verantwortlich ist:

   * `d` für einen Klick auf eine DSP-Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP-Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Such-Clickthrough).

Beispiel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Die EF-ID Dimension in [!DNL Analytics]

In [!DNL Analytics] Berichten können Sie EF ID-Daten finden, indem Sie nach der Dimension &quot;[!UICONTROL EF ID]&quot; suchen und die [!UICONTROL EF ID Instance] verwenden.

EF-IDs unterliegen dem Limit von 500.000 eindeutigen Kennungen in Analysis Workspace. Sobald der 500k-Wert erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Titel &quot;[!UICONTROL Low Traffic]&quot; gemeldet. Aufgrund der Möglichkeit fehlender Berichterstellungstreue werden die EF-IDs nicht klassifiziert und sollten nicht für Segmente oder Berichte in [!DNL Analytics] verwendet werden.

## Adobe Advertising AMO-IDs {#amo-id}

Die AMO ID verfolgt jede einzelne Anzeigenkombination auf einer weniger detaillierten Ebene und wird für die [!DNL Analytics] Datenklassifizierung und Aufnahme von Werbemetriken (wie Impressionen, Klicks und Kosten) aus Adobe Advertising verwendet. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) oder rVar-Dimension (AMO-ID) gespeichert und ausschließlich für das Reporting in [!DNL Analytics] verwendet.

Die AMO-ID wird auch als `s_kwcid` bezeichnet, was manchmal als &quot;[!DNL squid]&quot; ausgesprochen wird.

### Möglichkeiten zur Implementierung der AMO-ID {#amo-id-implement}

Der Parameter wird den Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Wenn die Server-seitige Einfügefunktion implementiert ist.

   * DSP-Kunden: Der Pixel-Server hängt den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer eine Display-Anzeige mit dem Adobe Advertising-Pixel aufruft.

   * Kunden aus den Bereichen Suche, Social Media und Commerce:

      * Bei [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit aktivierter [!UICONTROL Auto Upload] für das Konto oder die Kampagne fügt der Pixel-Server den Parameter s_kwcid automatisch an die Suffixe der Landingpage an, wenn ein Endbenutzer bzw. eine Endbenutzerin auf eine Anzeige mit dem Pixel &quot;Adobe Advertising&quot; klickt.

      * Für andere Werbenetzwerke oder [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit deaktivierter [!UICONTROL Auto Upload]-Einstellung fügen Sie den Parameter manuell zu Ihren [Anlagenparametern auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

* Wenn die Server-seitige Einfügefunktion nicht implementiert ist:

   * DSP-Kunden: Der [JavaScript](javascript.md)Code zeichnet automatisch Clickthroughs und Viewthroughs auf. Wenn ein Browser keine Cookies von Drittanbietern unterstützt, können Sie weiterhin Klick-basierte Konversionen für die folgenden Anzeigentypen verfolgen:

      * Fügen Sie für [!DNL Flashtalking]-Anzeigen-Tags manuell zusätzliche Makros pro &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) ein. **Hinweis:** Dieses Verfahren ist nicht erforderlich, wenn Ihr Unternehmen eine direkte Partnerschaft mit [!DNL Flashtalking] unterhält und Sie in der Dokumentation zum [!DNL Flashtalking]-Support unter [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) Datenweiterleitungs-Makros zum Tracking der `s_kwcid`- und `ef_id` verwenden.

      * Fügen Sie für [!DNL Google Campaign Manager 360]-Anzeigen-Tags manuell zusätzliche Makros pro &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md) ein.

   * Kunden aus den Bereichen Suche, Social Media und Commerce:

      * Fügen Sie für ([!DNL Google Ads] und [!DNL Microsoft Advertising]) Anzeigen manuell den AMO-ID-Parameter zu Ihren Landingpage-Suffixen hinzu, idealerweise auf [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} es sei denn, es ist ein anderes Tracking für einzelne Kontokomponenten erforderlich.

      * Für Anzeigen in allen anderen Werbenetzwerken fügen Sie den AMO-ID-Parameter manuell zu Ihren [Append-Parametern auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

Wenden Sie sich an Ihr Adobe-Accountteam, um die Server-seitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu ermitteln.

### AMO-ID-Formate {#amo-id-formats}

#### AMO-ID-Format für [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

Dabei gilt:

* `AC` zeigt den Anzeigekanal an.

* `{TM_AD_ID}` ist der von Adobe Advertising generierte alphanumerische Anzeigenschlüssel. Sie wird als eindeutige Kennung für eine Anzeige verwendet und dient als Schlüssel zur Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics].

* `{TM_PLACEMENT_ID}` ist der von Adobe Advertising generierte alphanumerische Platzierungsschlüssel. Sie wird als eindeutige Kennung für eine Platzierung verwendet und dient als Schlüssel zur Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics].

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-ID-Formate für Search-, Social- und Commerce-Anzeigen {#amo-id-format-search}

Die Parameter variieren je nach Anzeigennetzwerk, aber die folgenden Parameter sind für alle gleich:

* `AL` gibt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen ist.

* `{sid}` wird durch die numerische ID für das Werbenetzwerkkonto des Werbetreibenden ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für *,* 87 *für [!DNL Naver],* 888 *für [!DNL Baidu],* 90[!DNL Yandex] für *,* 94[!DNL Yahoo! Japan Ads], *105für* (nicht mehr unterstützt), oder [!DNL Yahoo! Display Network]106[!DNL Yahoo Native] ** [!DNL Pinterest] (nicht mehr unterstützt).

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
>In der Zwischenzeit funktionieren die Legacy-Formate wie folgt weiter:
>* Suchkampagnen:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Einkaufskampagnen (mit [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Audience Network-Kampagnen:
>  `s_kwcid=AL!{userid}!10!{AdId}`

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

### AMO ID Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der [!UICONTROL AMO ID] Dimension suchen und die [!UICONTROL AMO ID Instances] Metrik verwenden. Die Dimension [!UICONTROL AMO ID] enthält alle erfassten AMO-ID-Werte, während die Metrik [!UICONTROL AMO ID Instances] angibt, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise viermal auf dieselbe Suchanzeige geklickt wurde, Analytics jedoch sieben Site-Einträge nachverfolgt hat, wären [!UICONTROL AMO ID Instances] sieben (7) und [!UICONTROL Clicks] vier (4).

Für Reporting- oder Auditing-Vorgänge innerhalb von [!DNL Analytics] ist die Best Practice, die AMO-ID zusammen mit der entsprechenden -Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[-Through-Datenvalidierung für [!DNL Analytics for Advertising]](data-variances.md#data-validation) in „Erwartete Datenvarianzen zwischen [!DNL Analytics] und Adobe Advertising&quot;.

## Über Analytics Classifications

[!DNL Analytics] ist eine [Klassifizierung](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=de) ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Adobe Advertising kategorisiert Adobe Advertising-Rohdaten mithilfe von Klassifizierungen, sodass Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagne). Klassifizierungen bilden die Grundlage des Adobe Advertising-Reportings in [!DNL Analytics] und können mit den AMO-Metriken wie [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] und [!UICONTROL AMO Clicks] sowie mit benutzerdefinierten und standardmäßigen Onsite-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] und [!UICONTROL Revenue] verwendet werden.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](data-variances.md)
