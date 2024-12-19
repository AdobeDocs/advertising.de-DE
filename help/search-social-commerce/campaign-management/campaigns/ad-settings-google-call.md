---
title: '[!DNL Google Ads] Anzeigeneinstellungen nur für Aufrufe'
description: Verweisen Sie auf die Einstellungen  [!DNL Google Ads]  Anzeigen, die nur aufgerufen werden können.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] Anzeigeneinstellungen nur für Aufrufe

Sie können für Kampagnen, die das Such-Netzwerk verwenden, Textanzeigen erstellen, die nur auf Anruf verfügbar sind.

Search, Social und Commerce verfolgen nur aufrufbezogene Anzeigen mithilfe des Suffix und der Tracking-Vorlage auf Kontoebene. Sie können jedoch optional das Tracking auf Kontoebene in [!DNL Google Ads] Manager auf Anzeigenebene überschreiben.

Siehe [!DNL Google Ads] Hilfe zu [Anzeigenbeschränkungen pro Konto](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Der Name des Unternehmens. Die maximale Länge beträgt 25 Zeichen oder 12 Doppelbyte-Zeichen.

**[!UICONTROL Country]:** (Optional) Das Land, in dem das Unternehmen seinen Sitz hat.

**[!UICONTROL Phone Number]:** Die Telefonnummer für das Unternehmen. Beispiele: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Die erste und zweite Zeile des Hauptteils der Anzeige. Die maximale Länge für jede Zeile beträgt 35 Zeichen oder 17 Doppelbyte-Zeichen.

Die Schlüsselwortersetzungs-Syntax zählt nicht zur maximalen Länge. Beispiel: &quot;`{Description1: Free Account Analysis!}`&quot; wird als 22 Zeichen behandelt (nur der Teil „Kostenlose Kontoanalyse\!„).

>[!NOTE]
>
>Die Beschreibungsfelder dürfen keine Telefonnummern enthalten.

**[!UICONTROL Display URL]:** Die in der Anzeige angezeigte URL. Die Anzeige-URL muss mit einer Domain übereinstimmen, die mit Ihrem Unternehmen verknüpft ist, aber die Anzeige sendet keine Personen zu einer Landingpage.

Die maximale Länge beträgt 35 Einzelbyte- oder 17 Doppelbyte-Zeichen. Die Schlüsselwortersetzungs-Syntax zählt nicht zur maximalen Länge. Beispiel: &quot;`{DisplayURL: example.com}`&quot; wird als 11 Zeichen behandelt (nur der Teil „example.com„).

**[!UICONTROL Verification URL]:** (Optional) Eine Webseite, auf der die Telefonnummer für Ihre Anzeige als Text angezeigt wird, damit [!DNL Google Ads] überprüfen können, ob die Telefonnummer gültig ist. Sie muss dieselbe Domain wie die Anzeige-URL der Anzeige haben.

**[!UICONTROL Is Tracked]:** Aktiviert die Anrufverfolgung und Nur-Anruf-Konversionen.

**[!UICONTROL Count calls as phone call conversions]:** (Wenn &quot;[!UICONTROL Is Tracked]&quot; ausgewählt ist; optional) Attributiert alle Anrufe, die aus der Anzeige resultieren, einer bestimmten Art der Telefonanrufkonvertierung, wenn eine angegeben wird. Andernfalls erstellt [!DNL Google Ads] eine standardmäßige Konvertierungsaktion mit dem Namen &quot;[!UICONTROL Calls from ads]&quot;, sobald sie mindestens eine Konvertierung aus Ihren Weiterleitungsnummern aufzeichnet und ihr dann Aufrufe zuordnet.

**[!UICONTROL Count Action]:** (Wenn &quot;[!UICONTROL Count calls as phone call conversions]&quot; ausgewählt ist; optional) Die vorhandene Konversionsaktion, der Aufrufe zugeordnet werden.

Sie können Konversionsaktionen in [!DNL Google Ads] erstellen und verwalten.

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Über Anzeigen](ad-about.md)
>* [Anzeigen verwalten](ad-manage.md)
>* [[!DNL Google Ads] Erweiterte Einstellungen für dynamische Suchanzeigen](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Einstellungen für responsive Suchanzeigen](ad-settings-google-rsa.md)
