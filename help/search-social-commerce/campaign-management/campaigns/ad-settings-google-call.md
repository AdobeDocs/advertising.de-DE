---
title: "[!DNL Google Ads] Anzeigeneinstellungen, die nur aufgerufen werden können"
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] schreibgeschützte Anzeigen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] Anzeigeneinstellungen, die nur aufgerufen werden

Sie können reine Textanzeigen für Kampagnen erstellen, die das Suchnetzwerk verwenden.

In Search, Social und Commerce werden schreibgeschützte Anzeigen mit dem Suffix der Landingpage und der Tracking-Vorlage auf Kontoebene verfolgt. Optional können Sie jedoch das Tracking auf Kontoebene auf Anzeigenebene in [!DNL Google Ads] Manager.

Siehe [!DNL Google Ads] Hilfe für [Anzeigenbeschränkungen pro Konto](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Der Name des Unternehmens. Die maximale Länge beträgt 25 Zeichen oder 12 Doppelbyte-Zeichen.

**[!UICONTROL Country]:** (Optional) Das Land, in dem sich das Unternehmen befindet.

**[!UICONTROL Phone Number]:** Die Telefonnummer für das Unternehmen. Beispiele: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** Die erste und zweite Zeile des Hauptteils der Anzeige. Die maximale Länge pro Zeile beträgt 35 Zeichen oder 17 Doppelbyte-Zeichen.

Die Syntax für die Schlüsselwortersetzung zählt nicht zur maximalen Länge. Beispiel: &quot;`{Description1: Free Account Analysis!}`&quot; wird als 22 Zeichen behandelt (nur der Teil &quot;Kostenlose Kontoanalyse\!&quot;).

>[!NOTE]
>
>Die Beschreibungsfelder dürfen keine Telefonnummern enthalten.

**[!UICONTROL Display URL]:** Die in der Anzeige angezeigte URL. Die Anzeigen-URL muss mit einer Domäne übereinstimmen, die Ihrem Unternehmen zugeordnet ist, aber die Anzeige sendet keine Personen auf eine Landingpage.

Die maximale Länge beträgt 35 Einzelbyte- oder 17 Doppelbyte-Zeichen. Die Syntax für die Schlüsselwortersetzung zählt nicht zur maximalen Länge. Beispiel: &quot;`{DisplayURL: example.com}`&quot; wird als 11 Zeichen behandelt (nur der Teil &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Optional) Eine Webseite, auf der die Telefonnummer für Ihre Anzeige als Text angezeigt wird, sodass [!DNL Google Ads] kann überprüfen, ob die Telefonnummer gültig ist. Sie muss dieselbe Domäne wie die Anzeigen-URL der Anzeige haben.

**[!UICONTROL Is Tracked]:** Aktiviert das Tracking von Aufrufen und reine Konvertierungen von Aufrufen.

**[!UICONTROL Count calls as phone call conversions]:** (Wenn[!UICONTROL Is Tracked]&quot; ausgewählt ist; (optional) Ordnet alle Aufrufe, die aus der Anzeige resultieren, einem bestimmten Typ von Telefonanrufkonvertierung zu, wenn einer angegeben ist. Andernfalls [!DNL Google Ads] erstellt eine standardmäßige Konversionsaktion mit dem Namen[!UICONTROL Calls from ads]&quot;, sobald es mindestens eine Konversion aus Ihren Weiterleitungsnummern aufzeichnet und dann Aufrufe zuordnet.

**[!UICONTROL Count Action]:** (Wenn[!UICONTROL Count calls as phone call conversions]&quot; ausgewählt ist; optional) Die vorhandene Konversionsaktion, der Aufrufe zugeordnet werden.

Sie können Konversionsaktionen in [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Über Anzeigen](ad-about.md)
>* [Anzeigen verwalten](ad-manage.md)
>* [[!DNL Google Ads] erweiterte dynamische Suchanzeigeneinstellungen](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Einstellungen für responsive Suchanzeigen](ad-settings-google-rsa.md)

