---
title: '''[!DNL Google Ads]''-Anzeigeneinstellungen nur für Aufrufe'
description: Verweisen Sie auf die Einstellungen für schreibgeschützte Anzeigen [!DNL Google Ads] .
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] Nur-Aufruf-Anzeigeneinstellungen

Sie können reine Textanzeigen für Kampagnen erstellen, die das Suchnetzwerk verwenden.

Search, Social und Commerce verfolgen reine Aufrufanzeigen anhand des Suffix der Landingpage und der Tracking-Vorlage auf Kontoebene. Optional können Sie jedoch das Tracking auf Kontoebene auf Anzeigenebene im [!DNL Google Ads] Manager überschreiben.

Weitere Informationen finden Sie in der Hilfe zu [!DNL Google Ads] für [Anzeigenbeschränkungen pro Konto](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Der Name des Unternehmens. Die maximale Länge beträgt 25 Zeichen oder 12 Doppelbyte-Zeichen.

**[!UICONTROL Country]:** (Optional) Das Land, in dem sich das Unternehmen befindet.

**[!UICONTROL Phone Number]:** Die Telefonnummer für das Unternehmen. Beispiele: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Die erste und zweite Zeile des Hauptteils der Anzeige. Die maximale Länge pro Zeile beträgt 35 Zeichen oder 17 Doppelbyte-Zeichen.

Die Syntax für die Schlüsselwortersetzung zählt nicht zur maximalen Länge. Beispielsweise wird &quot;`{Description1: Free Account Analysis!}`&quot;als 22 Zeichen behandelt (nur der Teil &quot;Kostenlose Kontoanalyse\!&quot;).

>[!NOTE]
>
>Die Beschreibungsfelder dürfen keine Telefonnummern enthalten.

**[!UICONTROL Display URL]:** Die in der Anzeige angezeigte URL. Die Anzeigen-URL muss mit einer Domäne übereinstimmen, die Ihrem Unternehmen zugeordnet ist, aber die Anzeige sendet keine Personen auf eine Landingpage.

Die maximale Länge beträgt 35 Einzelbyte- oder 17 Doppelbyte-Zeichen. Die Syntax für die Schlüsselwortersetzung zählt nicht zur maximalen Länge. Beispielsweise wird &quot;`{DisplayURL: example.com}`&quot;als 11 Zeichen behandelt (nur der Teil &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Optional) Eine Webseite, auf der die Telefonnummer für Ihre Anzeige als Text angezeigt wird, sodass [!DNL Google Ads] überprüfen kann, ob die Telefonnummer gültig ist. Sie muss dieselbe Domäne wie die Anzeigen-URL der Anzeige haben.

**[!UICONTROL Is Tracked]:** Aktiviert das Tracking von Aufrufen und reine Konvertierungen von Aufrufen.

**[!UICONTROL Count calls as phone call conversions]:** (Wenn &quot;[!UICONTROL Is Tracked]&quot; ausgewählt ist; optional) Ordnet alle Aufrufe, die aus der Anzeige resultieren, einem bestimmten Typ von Telefonanrufkonvertierung zu, wenn einer angegeben ist. Andernfalls erstellt [!DNL Google Ads] eine standardmäßige Konversionsaktion mit dem Namen &quot;[!UICONTROL Calls from ads]&quot;, sobald mindestens eine Konversion aus Ihren Weiterleitungsnummern aufgezeichnet wird, und ordnet dann Aufrufe zu.

**[!UICONTROL Count Action]:** (Wenn &quot;[!UICONTROL Count calls as phone call conversions]&quot; ausgewählt ist; optional) Die vorhandene Konversionsaktion, der Aufrufe zugeordnet werden.

Sie können Konversionsaktionen in [!DNL Google Ads] erstellen und verwalten.

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Über Anzeigen](ad-about.md)
>* [Anzeigen verwalten](ad-manage.md)
>* [[!DNL Google Ads] erweiterte Einstellungen der dynamischen Suchanzeige](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Einstellungen für responsive Suchanzeige](ad-settings-google-rsa.md)
