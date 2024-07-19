---
title: Klick-Tracking-URL generieren
description: Erfahren Sie, wie Sie manuell eine Klick-Tracking-URL für Suche, Social und Commerce generieren.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Generieren einer Klick-Tracking-URL für Search, Social und Commerce mithilfe des Tools Tracking-URLs

*Advertiser mit nur Adobe Advertising-Konversions-Tracking*

Informationen dazu, wann Sie eine Klick-Tracking-URL manuell generieren und implementieren müssen, finden Sie unter &quot;[Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;.

>[!NOTE]
>
>Diese Funktion implementiert die Tracking-Vorlage oder Ziel-URL nicht in das relevante Anzeigenkonto.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Wählen Sie das Konto für das Werbenetzwerk aus der Liste aus.

   ([!DNL Google Ads] Keywords; Text, Installation mobiler Apps und dynamische Suchanzeigen; Platzierungen; Sitelinks; und Produktgruppen) Trackingtags für das Feld der Tracking-Vorlage werden angezeigt. Sie enthalten keine Anlagenparameter auf Kontoebene. Fahren Sie mit Schritt 4 fort.

   Geben Sie für alle anderen Typen von Tags Informationen ein, um ein Tag zu generieren.

1. (Bei Bedarf) Erstellen Sie ein Tag:

   1. Geben Sie die Landingpages mit Sitelinks oder Produktnamen auf eine der folgenden Arten an:

      * Geben Sie eine Datei mit den Informationen an, indem Sie den vollständigen Pfad und den Dateinamen eingeben oder auf **[!UICONTROL Browse]** klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. Die Datei muss eine tabulatorgetrennte Textdatei mit einem Element pro Zeile im folgenden Format sein:

         * (Kreative, Standardanzeigen) `**landing_page**`

           wobei `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           wobei `sitelink` der Sitelink-Name und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

         * ([!DNL Google Merchant Center] Produktgruppen und [!DNL Microsoft Advertising] Produktanzeigen) `product name <tab> ** <tab> landing_page`

           wobei `product name` der Produktname und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

      * Geben Sie im Eingabefeld ein Element pro Zeile im folgenden Format ein:

         * (Kreative, Standardanzeigen) `landing_page`

           wobei `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink**landing_page`

           wobei `sitelink` der Sitelink-Name und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] Produktgruppen und [!DNL Microsoft Advertising] Produktanzeigen) `product name**landing_page`

           wobei `product name` der Produktname und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: Acme PR208**http://www.example.com/travel.html

   1. Klicken Sie auf **[!UICONTROL Generate Tracking URLs]**.

1. (Optional) Kopieren Sie die URLs (beginnend mit &quot;http&quot;oder &quot;https&quot;) von der Bildschirm- oder Ausgabeseite und implementieren Sie sie in das Such- oder Social-Konto.

Geben Sie bei Konten mit Ziel-URLs die Werte in die entsprechenden Felder [!UICONTROL Base URL] ein.

Geben Sie bei Konten mit finalen URLs den Wert auf dem Bildschirm in das entsprechende Feld [!UICONTROL Tracking Template] ein. Sie müssen einen Parameter für die endgültige URL nach dem Parameter `&url=` hinzufügen (z. B. `{lpurl}`). Verwenden Sie für [!DNL Yahoo! Japan Ads] -Konten den Parameter `{lpurl}`. Eine Liste der Parameter [!DNL Google Ads] und [!DNL Microsoft Advertising] zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348) (siehe die Parameter &quot;Nur Tracking-Vorlage&quot;im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;) und in der [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Dekodieren einer Klick-Tracking-URL für Suche, Social und Commerce](click-tracking-url-decode.md)
