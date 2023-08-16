---
title: Advertising DSP Makros
description: Referenzieren Sie die verfügbaren Makros für das allgemeine Tracking und zur Verfolgung von Klicks auf Display-Anzeigen von Drittanbietern.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: bb404dd1ff2fda5e37435ac892e2a0f6beba0b33
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Advertising DSP Makros

Ein Makro ist ein kurzer Befehl oder Kurzbefehl für eine Anweisung und folgt normalerweise dem Format `${MACRO_NAME}`. Makros, die in kreativen Code- oder Clickthrough-URLs enthalten sind, werden in eine längere Code-Zeichenfolge umgewandelt, die der Anzeigenserver verstehen kann. Der DSP Adserver führt Makros aus, wenn die Anzeige bereitgestellt oder angeklickt wird.

Anzeigenserver-Makros sind nützlich, um wichtige Informationen an DSP- oder Drittanbieter-Anzeigenserver zu übergeben. Makros werden am häufigsten während des Handels mit kreativem Drittanbieter- und benutzerdefiniertem Code oder Metadaten (z. B. Pixeln von Drittanbietern) verwendet.

Sie können ein Makro an einer beliebigen Stelle, z. B. in einem VAST-Tag, in einer beliebigen URL oder in einem DSP- oder Drittanbieter-Ereignispixel, manuell einfügen. Jeder DSP Client und Partner verfügt jedoch über ein anderes Anzeigen-Tag-Format, und die Makros sollten entsprechend an verschiedenen Stellen im Tag eingefügt werden. Jedes Mal, wenn Sie mit einem neuen Kunden oder Partner arbeiten, fragen Sie ihn nach der Dokumentation, wo die Makros in die Anzeigen-Tags eingefügt werden sollen, die für den DSP verwendet werden.

## Allgemeine Tracking-Makros

Verwenden Sie allgemeine Tracking-Makros für alle Anzeigen- und Tag-Typen, um bei Bedarf bestimmte Daten zurückzugeben.

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | Die Konto-ID. | integer |
| `${TM_AD_ID}` | Der Anzeigenschlüssel (adKey). | Zeichenfolge |
| `${TM_AD_ID_NUM}` | Die Anzeigen-ID. | integer |
| `${TM_ADVERTISER_ID}` | Die Advertiser-ID. | integer |
| `${TM_CAMPAIGN_ID}` | Der Kampagnenschlüssel. | Zeichenfolge |
| `${TM_CAMPAIGN_ID_NUM}` | Die Kampagnen-ID. | integer |
| ` ${TM_CLICK_URL}` | Die Umleitungs-URL, mit der Werbeserver Anzeigenklicks verfolgen und zählen können. Wenn die Anzeige bereitgestellt wird und der Benutzer darauf klickt, wird das Makro aktiviert und der Klick aufgezeichnet und zu Berichtszwecken gezählt. | Zeichenfolge |
| ` ${TM_CLICK_URL_URLENC}` | Die kodierte Umleitungs-URL, mit der Werbeserver Anzeigenklicks verfolgen und zählen können. Wenn die Anzeige bereitgestellt wird und der Benutzer darauf klickt, wird das Makro aktiviert und der Klick aufgezeichnet und zu Berichtszwecken gezählt. Verwenden Sie dieses Makro nur, wenn Sie Werbeanzeigen von Drittanbietern erstellen und Ihr Anbieter URL-Kodierung erfordert. | Zeichenfolge |
| `${TM_FEED_ID}` | Der Schlüssel für die Medienplatzierung (feedKey). | Zeichenfolge |
| `${TM_FEED_ID_NUM}` | Die ID für die Medienplatzierung. | integer |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Der Site-Schlüssel für die Platzierung. Erforderlich für [!DNL AppsFlyer] Klicktracker für Anzeigen zur Installation mobiler Apps.<!-- should map to placement_site_key column of placement_site table --> | Zeichenfolge |
| `${TM_PLACEMENT_ID}` | Der Platzierungsschlüssel (cpKey). | Zeichenfolge |
| `${TM_PLACEMENT_ID_NUM}` | Die Platzierungs-ID. | integer |
| `${TM_RANDOM}` | Cachebuster: eine Zufallszahl zwischen 1 und 1000000. | long |
| `${TM_SESSION_ID}` | Die ID der Sitzung, die einem einzelnen Abruf des Anzeigen-Tags entspricht. | Zeichenfolge |
| `${TM_SITE_DOMAIN_URLENC}` | Die Seiten-Subdomäne, die von der URL in der Gebotsanfrage geparst wurde; URL-kodiert. Nicht unterstützt für In-Banner- und Click-to-Play-Anzeigen. | Zeichenfolge |
| ` ${TM_SITE_NAME}` | Der Site-Name für die Platzierung. | Zeichenfolge |
| `${TM_SITE_URL_URLENC}` | Die in der Angebotsanforderung übergebene URL, URL-kodiert. Nicht unterstützt für In-Banner- und Click-to-Play-Anzeigen. | Zeichenfolge |
| `${TM_SITE_ID_NUM}` | Die Site-ID für die Platzierung. | integer |
| `${TM_TIMESTAMP}` | Der Unix-Zeitstempel, der angibt, wie viele Sekunden seit Mitternacht (00:00 UTC) am 1. Januar 1970 vergangen sind. | long |
| ` ${TM_VIDEO_DURATION}` | Die Dauer des Anzeigenvideos in Sekunden. | integer |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Mobile-spezifische Makros

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) Die Plattform-ID, die dem Betriebssystem des Geräts entspricht:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` wenn die Plattform keine der oben genannten ist</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Der Gerätemodellname, URL-kodiert. | Zeichenfolge |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Die Umgebung, in der die Anzeige bereitgestellt wurde:<ul><li>`a` = Mobile App</li><li>`b` = mobile Website</li></ul> | string (`a` oder `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) Die Plattform-ID, die dem Betriebssystem des Geräts entspricht:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` wenn die Plattform keine der oben genannten ist</li></ul> | Zeichenfolge |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Der Gerätetyp, auf dem die Anzeige als Viewer angezeigt wurde:<ul><li>`TAB` = Tablet</li><li>`PHN` = mobile</li><li>`computer` = computer</li></ul> | Zeichenfolge |
| `${UOO}` | ([!DNL Nielsen]) Gibt an, ob der Benutzer das Anzeigen-Tracking deaktiviert hat:<ul><li>`1` (DNT-Markierung = 1) = Benutzer hat sich vom Anzeigen-Tracking abgemeldet</li><li>`0` (DNT-Markierung = 0) = Benutzer hat sich für das Anzeigen-Tracking entschieden</li></ul> | integer (`0` oder `1`) |
| `${TM_BUNDLE}` | Die [!DNL iOS] oder [!DNL Android] App Store-Bundle-ID. Beispiele: com.zynga.wwf2.free oder id804379658 | Zeichenfolge |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` gibt an, ob der Bieter feststellt, dass die Angebotsanforderung aus dem Ursprung der Europäischen Union stammt und die Durchsetzung der DSGVO erfordert:<ul><li>`1` = Die DSGVO sollte durchgesetzt werden</li><li>`0` = Die DSGVO sollte nicht durchgesetzt werden</li></ul>`gdpr_consent=${GDPR_CONSENT}` ist der Zustimmungswert, der vom Versorgungspartner in der eingehenden Gebotsanfrage übergeben wird:<ul><li>In den meisten Fällen handelt es sich um eine base64url-kodierte Zustimmungszeichenfolge oder ein daisybit (Beispiel: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMBkIDIgM0AgOJXAnQA)</li><li>`0` = keine Zustimmung</li><li>`1` = Einverständnis</li></ul> | daisybit oder integer |

{style="table-layout:auto"}

## Klicken Sie auf Makros für Display-Anzeigen von Drittanbietern

Um Klicks für Anzeigen mithilfe von Display-Tags von Drittanbietern genau zu verfolgen, DSP ein Klick-Makro für die Anzeige erforderlich. Es ist nur eine Version des Makros erforderlich. Das relevante Makro hängt vom Tag-Typ ab.

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | Die Umleitungs-URL, die es Adservern ermöglicht, Anzeigenklicks in der Plattform zu verfolgen und zu zählen. | Zeichenfolge |
| `${TM_CLICK_URL_URLENC}` | Die Umleitungs-URL, die Adservern ermöglicht, die URL-Codierung benötigen, um Anzeigenklicks in der Plattform zu verfolgen und zu zählen. | Zeichenfolge |

{style="table-layout:auto"}

DSP fügt automatisch Klick-Makros in einem Drittanbieter-Display-Tag ein, wenn Sie:

* Anzeigen-Tags von einem Adserver-Partner exportieren <!-- [Needs PM confirmation.] -->
* Massen-Upload [!DNL Flashtalking] oder [!DNL Google DoubleClick for Advertisers] Anzeigen-Tags direkt in DSP

Wenn beim Erstellen einer Display-Anzeige ein Klickmakro fehlt, zeigt DSP eine Warnmeldung an, in der Sie aufgefordert werden, das entsprechende Display-Klickmakro manuell in den richtigen Bereich des Tags einzufügen.

## [!DNL Analytics for Advertising] Makros

Für zusätzliche Makros, die speziell für [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Kunden, siehe[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md)&quot; und &quot;[Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

## Fehlerbehebung bei Makrofehlern

Wenn Sie Ihrem Code Makros hinzufügen, stellen Sie sicher, dass Sie die genaue Syntax des Makros verwenden. Bei der Validierung der Makros überprüft DSP, ob das Makro genau mit einem der gültigen Makros übereinstimmt.

Fehler werden generiert, wenn Zeichen am Anfang oder Ende des Makronamens fehlen. Beispielsweise wird eine Fehlermeldung angezeigt, wenn:

* Sie vergessen eines oder mehrere der Zeichen am Anfang des Makronamens, z. B. `${`. Wenn Sie nicht die vollständige Syntax angeben, wird der Eintrag nicht als gültiges Makro erkannt.
* Das Makro endet nicht mit einem gültigen Zeichensatz, z. B. `}`.

>[!MORELIKETHIS]
>
>* [Audio-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Einstellungen für Connected TV-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Anzeigeeinstellungen](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Einstellungen für mobile Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Native Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Pre-Roll-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Universelle Videoanzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
