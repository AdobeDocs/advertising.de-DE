---
title: Der Tracking-Parameter s_kwcid
description: Erfahren Sie mehr über den Tracking-Parameter, mit dem Adobe Advertising-Daten für Adobe Analytics freigegeben werden.
source-git-commit: a9e23de134274d8f5004a908853c4132300b84e8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Der Tracking-Parameter s_kwcid

*Advertiser mit nur einer Adobe-Advertising-Adobe Analytics-Integration*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertising gibt Daten zu Ihren Kampagnen mithilfe von Adobe Analytics frei `s_kwcid` -Parameter anhängen, der aus Anzeigenkanal- und Anzeigen-Netzwerkelementen besteht. Der Parameter wird Ihren Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen)<!--; the only option for Advertising DSP-->) Die serverseitige s_kwcid-Funktion ist implementiert.

  Für [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten mit [!UICONTROL Auto Upload] Wenn diese Einstellung für das Konto oder die Kampagne aktiviert ist, hängt der Pixelserver den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer auf eine Anzeige klickt <!-- click a search ad or views a display ad --> mit dem Adobe Advertising-Pixel.

  für andere Werbenetzwerke oder [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten mit [!UICONTROL Auto Upload] Wenn diese Einstellung deaktiviert ist, fügen Sie den Parameter manuell zu Ihren Anlagenparametern auf Kontoebene hinzu, die ihn an Ihre Basis-URLs anhängen.

* <!-- (Search, Social, & Commerce only) -->Die serverseitige s_kwcid-Funktion ist nicht implementiert und Sie müssen den Parameter s_kwcid manuell zu Ihrem ([!DNL Google Ads] und [!DNL Microsoft Advertising]) Einstiegsseitensuffixe oder (andere Anzeigennetzwerke) -Parameter auf Kontoebene anhängen.

Wenden Sie sich an Ihr Adobe Account Team, um die serverseitige s_kwcid-Funktion zu implementieren oder die beste Option für Ihr Unternehmen zu bestimmen.

## s_kwcid-Format für Anzeigen DSP

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

wobei:

* `AC` zeigt den Anzeigekanal an.

* `{TM_AD_ID}` ist der alphanumerische Anzeigenschlüssel.

* `{TM_PLACEMENT_ID}` ist der alphanumerische Platzierungsschlüssel.

## s_kwcid-Formate für Such-, Social- und Commerce-Anzeigen

Die Parameter variieren je nach Anzeigennetzwerk, doch die folgenden Parameter sind für alle gemeinsam:

* `AL` zeigt den Suchkanal an. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` ist eine eindeutige Benutzer-ID, die dem Advertiser zugewiesen wird.

* `{sid}` wird durch die numerische ID des Anzeigennetzwerkkontos des Werbetreibenden ersetzt: *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver], *88* für [!DNL Baidu], *90* für [!DNL Yandex], *94* für [!DNL Yahoo! Japan Ads], *105* für [!DNL Yahoo Native] (veraltet) oder *106* für [!DNL Pinterest] (nicht mehr unterstützt).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Dazu gehören auch Einkaufskampagnen mit [!DNL Google Merchant Center].

* Konten, die das neueste s_kwcid-Format verwenden, das Berichte auf Kampagnen- und Anzeigengruppenebene für Kampagnen zur Leistungssteigerung sowie Entwürfe und Experimentkampagnen unterstützt:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle anderen Konten:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Für dynamische Suchanzeigen: {keyword} mit dem automatischen Ziel gefüllt.
>* Wenn Sie das Tracking für [!DNL Google] Shopping-Anzeigen, ein Produkt-ID-Parameter, `{adwords_producttargetid}`wird vor dem Suchbegriffparameter eingefügt. Der Produkt-ID-Parameter wird nicht im [!DNL Google Ads] Tracking-Parameter auf Kontoebene und Kampagnenebene.
>* Informationen zur Verwendung des neuesten s_kwcid-Trackingcodes finden Sie unter &quot;[Aktualisieren Sie den s_kwcid-Trackingcode für eine [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;

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
