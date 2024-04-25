---
title: Klick-Tracking-URL generieren
description: Erfahren Sie, wie Sie manuell eine Klick-Tracking-URL für Suche, Social und Commerce generieren.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: a4d892b413dde26a96f03c797991c4df17da7562
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Generieren einer Klick-Tracking-URL für Search, Social und Commerce mithilfe des Tools Tracking-URLs

*Advertiser mit nur Adobe Advertising-Konversions-Tracking*

Informationen dazu, wann Sie eine Klick-Tracking-URL manuell generieren und implementieren müssen, finden Sie unter[Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Diese Funktion implementiert die Tracking-Vorlage oder Ziel-URL nicht in das relevante Anzeigenkonto.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Wählen Sie das Konto für das Werbenetzwerk aus der Liste aus.

   ([!DNL Google Ads] Suchbegriffe; Text, Installation mobiler Apps und dynamische Suchanzeigen; Platzierungen; Sitelinks; und Produktgruppen) Trackingtags für das Feld Tracking-Vorlage werden angezeigt. Sie enthalten keine Anlagenparameter auf Kontoebene. Fahren Sie mit Schritt 4 fort.

   Geben Sie für alle anderen Typen von Tags Informationen ein, um ein Tag zu generieren.

1. (Bei Bedarf) Erstellen Sie ein Tag:

   1. Geben Sie die Landingpages mit Sitelinks oder Produktnamen auf eine der folgenden Arten an:

      * Geben Sie eine Datei mit den Informationen an, indem Sie den vollständigen Pfad und Dateinamen eingeben oder auf **[!UICONTROL Browse]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen. Die Datei muss eine tabulatorgetrennte Textdatei mit einem Element pro Zeile im folgenden Format sein:

         * (Kreative, Standardanzeigen) `**landing_page**`

           where `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] Sitelinks) `sitelink <tab> ** <tab> landing_page`

           where `sitelink` ist der Sitelink-Name und `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

         * ([!DNL Google Merchant Center] Produktgruppen [!DNL Microsoft® Advertising] Produktanzeigen) `product name <tab> ** <tab> landing_page`

           where `product name` ist der Produktname und `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Die Datei kann bis zu 10.000 Zeilen enthalten.

      * Geben Sie im Eingabefeld ein Element pro Zeile im folgenden Format ein:

         * (Kreative, Standardanzeigen) `landing_page`

           where `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] Sitelinks) `sitelink**landing_page`

           where `sitelink` ist der Sitelink-Name und `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] Produktgruppen [!DNL Microsoft® Advertising] Produktanzeigen) `product name**landing_page`

           where `product name` ist der Produktname und `landing_page` ist eine gültige Landingpage-URL oder Basis-URL.

           Beispiel: Acme PR208**http://www.example.com/travel.html

   1. Klicks **[!UICONTROL Generate Tracking URLs]**.

1. (Optional) Kopieren Sie die URLs (beginnend mit &quot;http&quot;oder &quot;https&quot;) von der Bildschirm- oder Ausgabeseite und implementieren Sie sie in das Such- oder Social-Konto.

Geben Sie für Konten mit Ziel-URLs die Werte in der entsprechenden [!UICONTROL Base URL] -Felder.

Geben Sie bei Konten mit finalen URLs den Wert auf dem Bildschirm in die entsprechende [!UICONTROL Tracking Template] -Feld. Sie müssen einen Parameter für die endgültige URL nach der `&url=` -Parameter (z. B. `{lpurl}`). Für [!DNL Yahoo! Japan Ads] Konten, den Parameter verwenden `{lpurl}`. Für eine Liste von [!DNL Google Ads] und [!DNL Microsoft® Advertising] Parameter, die die endgültigen URLs in Tracking-Vorlagen angeben, finden Sie unter [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348) (siehe Parameter &quot;Nur Tracking-Vorlage&quot; im Abschnitt &quot;Verfügbar&quot;) [!DNL ValueTrack] Parameter&quot;) und der [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Über die Tools zum Erstellen und Dekodieren von Tracking-Tags](tracking-tools-about.md)
>* [Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Dekodieren einer Klick-Tracking-URL für Suche, Social und Commerce](click-tracking-url-decode.md)
