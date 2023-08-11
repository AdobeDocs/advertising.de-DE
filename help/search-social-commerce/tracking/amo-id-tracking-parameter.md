---
title: Der Tracking-Parameter AMO ID (s_kwcid)
description: Erfahren Sie mehr über den Tracking-Parameter, der zum Freigeben von Adobe Advertising-Daten für Adobe Analytics verwendet wird.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
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

Informationen zu den AMO-ID-Formaten für DSP und Suche, Social und Commerce finden Sie unter &quot;[Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Verwalten von Anzeigen-Netzwerkkonten](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Baidu-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Kampagneneinstellungen für Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Kampagneneinstellungen für Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex-Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
