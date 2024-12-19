---
title: Advertising DSP-Makros
description: Verweisen Sie auf die verfügbaren Makros für das allgemeine Tracking und das Tracking von Klicks auf Display-Anzeigen von Drittanbietern.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Advertising DSP-Makros

Ein Makro ist ein kurzer Befehl oder eine Abkürzung für eine Anweisung und folgt normalerweise dem `${MACRO_NAME}`. Im Kreativ-Code enthaltene Makros oder Clickthrough-URLs werden zu einer längeren Code-Zeichenfolge erweitert, die der Anzeigen-Server versteht. Der DSP-Werbeserver führt Makros aus, wenn die Anzeige geschaltet oder angeklickt wird.

Werbeserver-Makros sind nützlich, um wichtige Informationen an DSP oder Werbeserver von Drittanbietern weiterzugeben. Makros werden am häufigsten während des Handels mit kreativem Code oder Metadaten von Drittanbietern und deren Bearbeitung verwendet (z. B. Pixel von Drittanbietern).

Sie können ein Makro manuell an einer beliebigen Stelle einfügen, z. B. in einem VAST-Tag, in einer beliebigen URL oder in einem DSP- oder Ereignispixel eines Drittanbieters. Jeder DSP-Client und -Partner hat jedoch ein anderes Tag-Format für die Anzeige, und die Makros sollten entsprechend an verschiedenen Stellen im Tag eingefügt werden. Fragen Sie bei jeder Arbeit mit einem neuen Client oder Partner nach der Dokumentation, wo die Makros in die Anzeigen-Tags eingefügt werden können, die DSP-Traffic unterstützen.

## Allgemeine Tracking-Makros

Verwenden Sie allgemeine Tracking-Makros für alle Anzeigen- und Tag-Typen, um bestimmte Daten nach Bedarf zurückzugeben.

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | Die Konto-ID. | Ganzzahl |
| `${TM_AD_ID}` | Der Anzeigenschlüssel (adKey). | Zeichenfolge |
| `${TM_AD_ID_NUM}` | Die Werbe-ID. | Ganzzahl |
| `${TM_ADVERTISER_ID}` | Die Werbekunden-ID. | Ganzzahl |
| `${TM_CAMPAIGN_ID}` | Der Kampagnenschlüssel. | Zeichenfolge |
| `${TM_CAMPAIGN_ID_NUM}` | Die Kampagnen-ID. | Ganzzahl |
| ` ${TM_CLICK_URL}` | Die Umleitungs-URL, mit der Anzeigen-Server Anzeigenklicks verfolgen und zählen können. Wenn der Benutzer bei der Auslieferung der Anzeige darauf klickt, wird das Makro aktiviert und der Klick aufgezeichnet und zu Berichtszwecken gezählt. | Zeichenfolge |
| ` ${TM_CLICK_URL_URLENC}` | Die kodierte Umleitungs-URL, mit der Anzeigen-Server Anzeigenklicks verfolgen und zählen können. Wenn der Benutzer bei der Auslieferung der Anzeige darauf klickt, wird das Makro aktiviert und der Klick aufgezeichnet und zu Berichtszwecken gezählt. Verwenden Sie dieses Makro nur, wenn Sie Anzeigen von Drittanbietern erstellen und Ihr Anbieter eine URL-Codierung erfordert. | Zeichenfolge |
| `${TM_FEED_ID}` | Der Schlüssel für die Medienplatzierung (feedKey). | Zeichenfolge |
| `${TM_FEED_ID_NUM}` | Die ID für die Medienplatzierung. | Ganzzahl |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Der Site-Schlüssel für die Platzierung. Erforderlich für [!DNL AppsFlyer] Klick-Tracker zur Installation von Anzeigen in Mobile Apps.<!-- should map to placement_site_key column of placement_site table --> | Zeichenfolge |
| `${TM_PLACEMENT_ID}` | Der Platzierungsschlüssel (cpKey). | Zeichenfolge |
| `${TM_PLACEMENT_ID_NUM}` | Die Platzierungs-ID. | Ganzzahl |
| `${TM_RANDOM}` | Cachebuster: eine zufällige Zahl zwischen 1 und 1000000. | lang |
| `${TM_SESSION_ID}` | Die ID der Sitzung, die einem einzelnen Abrufen des Anzeigen-Tags entspricht. | Zeichenfolge |
| `${TM_SITE_DOMAIN_URLENC}` | Die Subdomain der Seite, die von der URL in der Angebotsanfrage geparst wird; URL-kodiert. Nicht unterstützt für In-Banner-, Klick-to-Play-Anzeigen. | Zeichenfolge |
| ` ${TM_SITE_NAME}` | Der Site-Name für die Platzierung. | Zeichenfolge |
| `${TM_SITE_URL_URLENC}` | Die in der Angebotsanfrage übergebene URL (URL-kodiert). Nicht unterstützt für In-Banner-, Klick-to-Play-Anzeigen. | Zeichenfolge |
| `${TM_SITE_ID_NUM}` | Die Site-ID für die Platzierung. | Ganzzahl |
| `${TM_TIMESTAMP}` | Der Unix-Zeitstempel, der die Anzahl der Sekunden angibt, die seit Mitternacht (00:00 UTC) am 1. Januar 1970 verstrichen sind. | lang |
| ` ${TM_VIDEO_DURATION}` | Die Dauer des Anzeigenvideos in Sekunden. | Ganzzahl |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Mobile-spezifische Makros

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) Die Plattform-ID, die dem Betriebssystem des Geräts entspricht:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other`, wenn die Plattform keine der oben genannten Funktionen aufweist</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Der Gerätemodellname, URL-kodiert. | Zeichenfolge |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Die Umgebung, in der die Anzeige geschaltet wurde:<ul><li>`a` = Mobile App</li><li>`b` = mobile Website</li></ul> | Zeichenfolge (`a` oder `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) Die Plattform-ID, die dem Betriebssystem des Geräts entspricht:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other`, wenn die Plattform keine der oben genannten Funktionen aufweist</li></ul> | Zeichenfolge |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Der Gerätetyp, auf dem die Anzeige angezeigt wurde:<ul><li>`TAB` = Tablette</li><li>`PHN` = mobil</li><li>`computer` = Computer</li></ul> | Zeichenfolge |
| `${UOO}` | ([!DNL Nielsen]) Ob der Benutzer das Anzeigen-Tracking abgelehnt hat oder nicht:<ul><li>`1` (DNT-Flag = 1) = der Benutzer hat das Anzeigen-Tracking abgelehnt</li><li>`0` (DNT-Flag = 0) = der Benutzer hat sich für das Anzeigen-Tracking entschieden</li></ul> | Ganze Zahl (`0` oder `1`) |
| `${TM_BUNDLE}` | Die Bundle-ID des [!DNL iOS] oder [!DNL Android] App Store. Beispiele: com.zynga.wwf2.free oder id804379658 | Zeichenfolge |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` gibt an, ob der Bieter feststellt, dass die Angebotsanfrage aus der Europäischen Union stammt und eine Durchsetzung der DSGVO erfordert:<ul><li>`1` = Die DSGVO sollte durchgesetzt werden</li><li>`0` = Die DSGVO sollte nicht durchgesetzt werden</li></ul>`gdpr_consent=${GDPR_CONSENT}` ist der Einverständniswert, der vom Übermittlungspartner in der eingehenden Angebotsanfrage übergeben wird:<ul><li>In den meisten Fällen handelt es sich um eine base64url-kodierte Einverständniszeichenfolge, oder Daisybit (Beispiel: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = kein Einverständnis</li><li>`1` = Einverständnis</li></ul> | Daisybit oder Integer |

{style="table-layout:auto"}

## Klicken Sie auf Makros für Display-Anzeigen von Drittanbietern

Um Klicks auf Anzeigen mit Display-Tags von Drittanbietern genau zu verfolgen, erfordert DSP ein Display-Klick-Makro. Es ist nur eine Version des Makros erforderlich. Das entsprechende Makro hängt vom Typ des Tags ab.

| Makro | Ersatzbeschreibung | Typ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | Die Umleitungs-URL, mit der Anzeigen-Server Anzeigenklicks in der Plattform verfolgen und zählen können. | Zeichenfolge |
| `${TM_CLICK_URL_URLENC}` | Die Umleitungs-URL, die es Anzeigen-Servern ermöglicht, die URL-Codierung benötigen, um Anzeigenklicks in der Plattform zu verfolgen und zu zählen. | Zeichenfolge |

{style="table-layout:auto"}

DSP fügt automatisch Display-Klick-Makros in ein Display-Tag eines Drittanbieters ein, wenn Sie:

* Exportieren von Anzeigen-Tags aus einer Ad-Server-<!-- [Needs PM confirmation.] -->
* Massen-Upload von [!DNL Flashtalking]- oder [!DNL Google DoubleClick for Advertisers]-Anzeigen-Tags direkt in DSP

Wenn beim Erstellen einer Display-Anzeige ein Klick-Makro fehlt, zeigt DSP eine Warnmeldung an, die Sie auffordert, das entsprechende Display-Klick-Makro manuell in den richtigen Bereich des Tags einzufügen.

## Makros [!DNL Analytics for Advertising]

Weitere Makros, die speziell für [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Kunden verfügbar sind, finden Sie unter [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) und [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md).

## Fehlerbehebung bei Makro-Fehlern

Wenn Sie Makros zu Ihrem Code hinzufügen, stellen Sie sicher, dass Sie die exakte Syntax des Makros verwenden. Bei der Validierung der Makros prüft DSP, ob das Makro genau mit einem der gültigen Makros übereinstimmt.

Fehler werden erzeugt, wenn am Anfang oder Ende des Makronamens Zeichen fehlen. Beispielsweise wird eine Fehlermeldung angezeigt, wenn:

* Sie vergessen eines oder mehrere der Zeichen am Anfang des Makronamens, z. B. `${`. Wenn Sie die vollständige Syntax nicht angeben, wird der Eintrag nicht als gültiges Makro erkannt.
* Das Makro endet nicht mit einem gültigen Zeichensatz, z. B. `}`.

>[!MORELIKETHIS]
>
>* [Audio-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Einstellungen für verbundene TV-Werbeanzeigen](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Anzeigeneinstellungen anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Mobile-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Native Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Pre-roll-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Einstellungen für universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
