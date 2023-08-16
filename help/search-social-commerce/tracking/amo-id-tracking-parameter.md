---
title: Der Tracking-Parameter AMO ID (s_kwcid)
description: Erfahren Sie mehr über den Tracking-Parameter, mit dem Adobe Advertising-Daten für Adobe Analytics freigegeben werden.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Der Tracking-Parameter AMO ID (s_kwcid)

*Advertiser nur mit Adobe Advertising-Adobe Analytics-Integration*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising gibt Daten zu Ihren Kampagnen mithilfe des AMO ID-Anlagenparameters, der auch als `s_kwcid` -Parameter, der aus Anzeigenkanal- und Anzeigennetzwerkspezifischen Elementen besteht.

Der Parameter wird Ihren Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Die serverseitige Einfügefunktion ist implementiert.

   * DSP: Der Pixelserver hängt den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer eine Display-Anzeige mit dem Adobe Advertising-Pixel anzeigt.

   * Kunden von Search, Social und Commerce:

      * Für [!DNL Google Ads] und [!DNL Microsoft® Advertising] Konten mit [!UICONTROL Auto Upload] Wenn für das Konto oder die Kampagne aktiviert ist, hängt der Pixelserver den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer auf eine Anzeige mit dem Adobe Advertising-Pixel klickt.

      * für andere Werbenetzwerke oder [!DNL Google Ads] und [!DNL Microsoft® Advertising] Konten mit [!UICONTROL Auto Upload] Wenn diese Einstellung deaktiviert ist, fügen Sie den Parameter manuell zu Ihren Anlagenparametern auf Kontoebene hinzu, die ihn an Ihre Basis-URLs anhängen.

* Die serverseitige Einfügefunktion ist nicht implementiert:

   * DSP Kunden:

      * Für [!DNL Flashtalking] Anzeigen-Tags, manuelles Einfügen zusätzlicher Makros pro[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Für [!DNL Google Campaign Manager 360] Anzeigen-Tags, manuelles Einfügen zusätzlicher Makros pro[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Kunden von Search, Social und Commerce:

      * Für ([!DNL Google Ads] und [!DNL Microsoft® Advertising]) hinzufügen, fügen Sie den AMO ID-Parameter manuell zu den Suffixen Ihrer Landingpage hinzu.

      * Fügen Sie bei Anzeigen in allen anderen Werbenetzwerken den Parameter AMO ID manuell zu Ihren Anlagenparametern auf Kontoebene hinzu, die ihn an Ihre Basis-URLs anhängen.

Wenden Sie sich an Ihr Adobe Account Team, um die serverseitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu bestimmen.

Informationen zu den AMO-ID-Formaten für DSP und Suche, Social und Commerce finden Sie unter &quot;[Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Suchen, Social und Commerce) [Verwalten von Anzeigen-Netzwerkkonten](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Suchen, Social und Commerce) [Baidu-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Suchen, Social und Commerce) [Kampagneneinstellungen für Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Suchen, Social und Commerce) [Einstellungen für Microsoft® Advertising-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Suchen, Social und Commerce) [Yahoo! Kampagneneinstellungen für Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Suchen, Social und Commerce) [Yandex-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
