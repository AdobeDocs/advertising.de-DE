---
title: Erstellen einer Klick-Tracking-URL
description: Erfahren Sie, wie Sie manuell eine Klick-Tracking-URL für Search, Social und Commerce generieren.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Erstellen einer Klick-Tracking-URL für Search, Social und Commerce mit dem Tracking-URLs-Tool

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

Informationen dazu, wann Sie eine Klick-Tracking-URL manuell generieren und implementieren müssen, finden Sie unter &quot;[Wann und wie Sie Klick-Tracking-URLs generieren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;.

>[!NOTE]
>
>Diese Funktion implementiert die Tracking-Vorlage oder Ziel-URL nicht im entsprechenden Werbekonto.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Wählen Sie das Netzwerkkonto aus der Liste aus.

   ([!DNL Google Ads] Schlüsselwörter; Text, Installation von Mobile Apps und dynamische Suchanzeigen; Platzierungen; Sitelinks; und Produktgruppen) Tracking-Tags für das Feld Tracking-Vorlage werden angezeigt. Sie enthalten keine Append-Parameter auf Kontoebene. Fahren Sie mit Schritt 4 fort.

   Geben Sie für alle anderen Arten von Tags Informationen ein, um ein Tag zu generieren.

1. (Falls erforderlich) Tag erzeugen:

   1. Geben Sie die Landingpages mit Sitelinks oder Produktnamen auf Anforderung wie folgt an:

      * Geben Sie eine Datei an, die die Informationen enthält, indem Sie den vollständigen Pfad und Dateinamen eingeben oder auf **[!UICONTROL Browse]** klicken, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. Die Datei muss eine tabulatorgetrennte Textdatei mit einem Element pro Zeile im folgenden Format sein:

         * (Kreative, Standardanzeigen) `**landing_page**`

           wobei `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] Sitelinks) `sitelink <tab> ** <tab> landing_page`

           wobei `sitelink` der Sitelink-Name und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

         * ([!DNL Google Merchant Center] Produktgruppen und [!DNL Microsoft Advertising] Produktanzeigen) `product name <tab> ** <tab> landing_page`

           wobei `product name` der Produktname und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

      * Geben Sie in das Eingabefeld einen Artikel pro Zeile im folgenden Format ein:

         * (Kreative, Standardanzeigen) `landing_page`

           wobei `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] Sitelinks) `sitelink**landing_page`

           wobei `sitelink` der Sitelink-Name und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] Produktgruppen und [!DNL Microsoft Advertising] Produktanzeigen) `product name**landing_page`

           wobei `product name` der Produktname und `landing_page` eine gültige Landingpage-URL oder Basis-URL ist.

           Beispiel: Acme PR208**http://www.example.com/travel.html

   1. Klicken Sie auf **[!UICONTROL Generate Tracking URLs]**.

1. (Optional) Kopieren Sie die URLs (beginnend mit „http“ oder „https„) vom Bildschirm oder von der Ausgabeseite und implementieren Sie sie im Such- oder Social-Media-Konto.

Geben Sie für Konten mit Ziel-URLs die Werte in die entsprechenden [!UICONTROL Base URL] ein.

Geben Sie für Konten mit endgültigen URLs den Bildschirmwert in das entsprechende [!UICONTROL Tracking Template] ein. Sie müssen nach dem `&url=` Parameter einen Parameter für die endgültige URL hinzufügen (z. B. `{lpurl}`). Verwenden Sie für [!DNL Yahoo! Japan Ads] Konten den Parameter `{lpurl}`. Eine Liste der [!DNL Google Ads]- und [!DNL Microsoft Advertising] zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348) (siehe die Parameter „Nur Tracking-Vorlage“ im Abschnitt „Verfügbare [!DNL ValueTrack]„) und in der [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [Wann und wie Sie Klick-Tracking-URLs generieren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decodieren einer Klick-Tracking-URL für Search, Social und Commerce](click-tracking-url-decode.md)
