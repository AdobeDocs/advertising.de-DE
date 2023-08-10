---
title: Der Tracking-Parameter AMO ID (s_kwcid)
description: Erfahren Sie mehr über den Tracking-Parameter, der zum Freigeben von Adobe Advertising-Daten für Adobe Analytics verwendet wird.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Der Tracking-Parameter AMO ID (s_kwcid)

*Werbetreibende, die nur über eine Adobe Advertising-Adobe Analytics-Integration verfügen*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising gibt Daten zu Ihren Kampagnen mithilfe des AMO-ID-Anlagenparameters, der auch als `s_kwcid` -Parameter, der aus Anzeigenkanal- und Anzeigennetzwerkspezifischen Elementen besteht.

<!-- add everything below to IDs page -->

Der Parameter wird Ihren Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Die serverseitige Einfügefunktion ist implementiert.

  Für [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten mit [!UICONTROL Auto Upload] Wenn diese Einstellung für das Konto oder die Kampagne aktiviert ist, hängt der Pixelserver automatisch den AMO-ID-Parameter an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer auf eine Anzeige klickt <!-- click a search ad or views a display ad --> mit dem Adobe Advertising-Pixel.

  für andere Werbenetzwerke oder [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten mit [!UICONTROL Auto Upload] Wenn diese Einstellung deaktiviert ist, fügen Sie den Parameter AMO ID manuell zu Ihren Anlagenparametern auf Kontoebene hinzu, die ihn an Ihre Basis-URLs anhängen.

* <!-- (Search, Social, & Commerce only) -->Die serverseitige Einfügefunktion ist nicht implementiert und Sie müssen den AMO-ID-Parameter manuell zu Ihrer hinzufügen ([!DNL Google Ads] und [!DNL Microsoft Advertising]) Einstiegsseitensuffixe oder (andere Anzeigennetzwerke) -Parameter auf Kontoebene anhängen.

Wenden Sie sich an Ihr Adobe Account Team, um die serverseitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu bestimmen.

## AMO-ID-Format für Advertising DSP Anzeigen

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

wobei:

* `AC` zeigt den Anzeigekanal an.

* `{TM_AD_ID}` ist der alphanumerische Anzeigenschlüssel.

* `{TM_PLACEMENT_ID}` ist der alphanumerische Platzierungsschlüssel.

## AMO-ID-Formate für Such-, Social- und Commerce-Anzeigen

Die Parameter variieren je nach Anzeigennetzwerk, doch die folgenden Parameter sind für alle gemeinsam:

* `AL` zeigt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen wird.

* `{sid}` wird durch die numerische ID des Anzeigennetzwerkkontos des Werbetreibenden ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver], *88* für [!DNL Baidu], *90* für [!DNL Yandex], *94* für [!DNL Yahoo! Japan Ads], *105* für [!DNL Yahoo Native] (veraltet) oder *106* für [!DNL Pinterest] (nicht mehr unterstützt).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Dazu gehören auch Einkaufskampagnen mit [!DNL Google Merchant Center].

* Konten, die das neueste AMO-ID-Format verwenden, das Berichte auf Kampagnen- und Anzeigengruppenebene für Kampagnen- und Experimentkampagnen zur Leistungssteigerung unterstützt:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle anderen Konten:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Für dynamische Suchanzeigen: {keyword} mit dem automatischen Ziel gefüllt.
>* Wenn Sie das Tracking für [!DNL Google] Shopping-Anzeigen, ein Produkt-ID-Parameter, `{adwords_producttargetid}`wird vor dem Suchbegriffparameter eingefügt. Der Produkt-ID-Parameter wird nicht im [!DNL Google Ads] Tracking-Parameter auf Kontoebene und Kampagnenebene.
>* Informationen zur Verwendung des neuesten AMO-ID-Trackingcodes finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für eine [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Suchkampagnen:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Shopping-Kampagnen (mit [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Zielgruppennetzwerkkampagnen:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Verwalten von Anzeigen-Netzwerkkonten](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Baidu-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampagneneinstellungen für Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Kampagneneinstellungen für Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
