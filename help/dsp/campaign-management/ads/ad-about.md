---
title: Über die Anzeigenverwaltung in Advertising DSP
description: Erfahren Sie mehr über die Anzeigenverwaltung.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Über die Anzeigenverwaltung in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP unterstützt die Bereitstellung von Anzeigen über Werbeanzeigen von Drittanbietern (z. B. Google, Flashspeak oder Sizmek) für verschiedene Anzeigentypen und den direkten Asset-Upload für native Display-Anzeigen. Sie können Drittanbieter-Tags einzeln oder stapelweise hochladen. Massen-Uploads verwenden Partner-Tag-Arbeitsblätter oder eine Massen-Tag-Vorlage.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Nachdem Sie Ihre Anzeigen eingerichtet haben, fügen Sie jede Anzeige einer oder mehreren Platzierungen hinzu, die die Targeting-Parameter (z. B. Geografie, Zielgruppe, Gerät und Inventar-Targeting) enthalten, die steuern, wie Ihre Kampagne bereitgestellt wird. Sie müssen eine Anzeige an eine Platzierung anhängen, um mit der Ausführung der Anzeige beginnen zu können.

## Verfügbare Anzeigentypen {#ad-types}

Alle folgenden Anzeigentypen sind in DSP verfügbar. Vollständige Spezifikationen für jeden Anzeigentyp finden Sie in den [Anzeigenspezifikationen](ad-specs.md).

* **Audioanzeigen (nur Drittanbieter)**: Audioanzeigen werden zwischen Inhalten auf digitalen Herausgeberseiten wiedergegeben und können eigenständig als Audiodateien oder zusammen mit begleitenden Bannern ausgeführt werden. Audio wird am besten verwendet, um das Markenbewusstsein zu fördern und unterwegs mit Zielgruppen zu interagieren. Zu den wichtigsten Leistungsindikatoren für Audio gehören [!UICONTROL Completion Rate] und [!UICONTROL Cost per Completion].

* **Display-Anzeigen (nur Drittanbieter)**: Display-Anzeigen sind animierte oder statische Bilder, die in Webbrowsern oder Apps angezeigt werden. Wenn Sie auf die Werbeeinheit klicken, gelangt der Benutzer zu einer Marken-Site oder auf eine Microsite. Die Anzeige eignet sich am besten, um effiziente CPMs zu fördern, die Nachrichtenzuordnung zu erhöhen, zusätzliche Marken- oder Produktkontaktpunkte hinzuzufügen und Benutzer im Kauftrichter nach unten zu treiben. Die wichtigsten Leistungsindikatoren für die Anzeige sind [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] und [!UICONTROL Cost per Conversion]. DSP unterstützt eine Vielzahl von Anzeigengrößen für Anzeigenbanner.

* **Mobile Anzeigen (nur Drittanbieter)**: Mobile Anzeigen können im Pre-Roll-Video (VAST, MRAID) oder im standardmäßigen Anzeigeformat vorliegen. Mobile Pre-Roll-Videos können automatisch abgespielt oder per Klick abgespielt werden. Sie eignen sich am besten, um Besucher über mehrere Bildschirme zu erreichen. Die mobile Standardanzeige ist ein statisches Bild, das in mobilen Webbrowsern oder in Apps angezeigt wird und am besten dazu dient, digitale Videokäufe zu ergänzen, die Nachrichtenzuordnung zu fördern und zusätzliche Branding- oder Produkt-Touchpoints hinzuzufügen. Mobile Anzeigen können auch als Vollbild-Übernahmen oder als mobile Zwischenräume verwendet werden, bei denen es sich um mobile Anzeigen mit hoher Wirkung im Vollbildmodus handelt, die am besten dazu dienen, das Markenbewusstsein für mobile Zielgruppen zu entwickeln und Konversionen zu fördern.

* **Native Display-Anzeigen (nur Erstanbieter)**: Native Anzeigen werden im standardmäßigen Anzeigeformat unterstützt. Native Anzeigen beinhalten eine Überschrift und/oder einen Titel, eine Beschreibung, ein Logo und ein Bild. Die Anzeigenelemente werden so kombiniert und gerendert, dass sie dem Seitenstil des Herausgebers entsprechen, sodass die Anzeige mit dem organischen Inhalt des Herausgebers verschmolzen und die Interaktion erhöht wird. Native Inhalte werden am besten für Markenbewusstsein und zur Steigerung der Zielgruppenansichten und Interaktionsraten mit Viewer-freundlicher Werbung verwendet. Die wichtigsten Leistungsindikatoren sind [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] und [!UICONTROL Cost Per Conversion].

* **Pre-Roll-Anzeigen (nur Drittanbieter)**: Pre-Roll-Anzeigen (VAST und VPAID) werden vor Premium-Videoinhalten angezeigt und bieten ein interaktives, ansprechendes Viewer-Erlebnis. Pre-Roll-Videos können interaktiv sein, Rich-Media-Funktionen enthalten und Überlagerungen, Rollover und Aktionsaufrufe enthalten. Die wichtigsten Leistungsindikatoren für Pre-Roll-Videoanzeigen sind [!UICONTROL Video Completion Rate] und [!UICONTROL Viewability Rate].

* **Connected TV Ads (nur Drittanbieter)**: Connected TV-Anzeigen werden vor und während Premium-TV-Videoinhalten angezeigt. Alle angeschlossenen TV-Inventare werden auf TV-Geräten ausgeführt, d. h. das Video wird automatisch in einer Bildschirmumgebung mit schlankem Hintergrund wiedergegeben, die die Betrachter nicht überspringen können. Angeschlossenes Fernsehen ist das beste digitale Videoformat für Fernsehwerbung. Die wichtigsten Leistungsindikatoren für Connected TV sind [!UICONTROL Completion Rate].

* **Universelle Videoanzeigen (nur bei Drittanbietern)**: Mit universellen Videoanzeigen können Sie das Videomaterial aus Desktop-, Mobil- und vernetzten TV-Umgebungen für VPAID- und VAST-Inventare mithilfe einer einzigen Videoplatzierung gezielt ausrichten. Sie kombinieren alle Funktionen von vernetzten TV-, Pre-Roll- und mobilen Pre-Roll-Anzeigen und werden vor und während des Videoinhalts angezeigt. Die wichtigsten Leistungsindikatoren für universelle Videos sind [!UICONTROL Completion Rate] und [!UICONTROL Viewability Rate].

  Universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

  Weitere Informationen zu universellen Videoanzeigen finden Sie unter &quot;[FAQs Info über universelle Videos](/help/dsp/campaign-management/faq-universal-video.md)&quot;.

## Genehmigungen DSP Anzeigen

Wenn Sie eine Anzeige erstellen, DSP sie für vertrauliche Kategorien überprüft, klicken Sie auf URL-Funktion und zeigen Sie eine Vorschau des Renderings an.

Zunächst zeigt die Spalte &quot;[!UICONTROL Status]&quot;der Anzeige einen roten Punkt an. Der Überprüfungsprozess dauert normalerweise 24 bis 48 Stunden. Eine fehlerhafte Anzeige kann jedoch länger als 48 Stunden den Status &quot;Ausstehend&quot;aufweisen, sodass Sie Zeit haben, Fehler zu beheben, bevor die Anzeige abgelehnt wird. Abgelehnte Anzeigen enthalten einen Grund für die Ablehnung.

Wenn DSP eine Anzeige genehmigt, wird in der Spalte Status der Anzeige ein grüner Punkt angezeigt.

![Genehmigungsanzeiger in der Spalte [!UICONTROL Status]](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Ihre Werbeanzeige kann nur bereitgestellt werden, wenn sowohl DSP als auch die SSP die Kreativinhalte genehmigt haben. Jeder SSP hat seine eigenen Genehmigungsanforderungen und -prozesse.

>[!MORELIKETHIS]
>
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-multiple.md)
>* [Anzeigenspezifikationen](ad-specs.md)
