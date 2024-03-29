---
title: Über Anzeigen-Management in Advertising DSP
description: Erfahren Sie mehr über die Anzeigenverwaltung.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 9073400eb26957c63378bee90929009fcc82f78f
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Über Anzeigen-Management in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP unterstützt die Bereitstellung von Anzeigen über Werbeanzeigen von Drittanbietern (z. B. Google, Flashspeak oder Sizmek) für verschiedene Anzeigentypen und den direkten Asset-Upload für native Display-Anzeigen. Sie können Drittanbieter-Tags einzeln oder stapelweise hochladen. Massen-Uploads verwenden Partner-Tag-Arbeitsblätter oder eine Massen-Tag-Vorlage.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Sobald Ihre Anzeigen eingerichtet sind, fügen Sie jede Anzeige einer Platzierung hinzu, die die Targeting-Parameter (Geo, Zielgruppe, Gerät und Inventar-Targeting) enthält, die steuern, wie Ihre Kampagne bereitgestellt wird. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

## Verfügbare Anzeigentypen {#ad-types}

Alle folgenden Anzeigentypen sind in DSP verfügbar. Vollständige Spezifikationen für jeden Anzeigentyp finden Sie im Abschnitt [Anzeigenspezifikationen](ad-specs.md).

* **Audioanzeigen (nur Drittanbieter)**: Audioanzeigen spielen zwischen Inhalten auf digitalen Herausgeberseiten und können als Audiodateien oder zusammen mit begleitenden Bannern eigenständig ausgeführt werden. Audio wird am besten verwendet, um das Markenbewusstsein zu fördern und unterwegs mit Zielgruppen zu interagieren. Zu den wichtigsten Leistungsindikatoren für Audio gehören [!UICONTROL Completion Rate] und [!UICONTROL Cost per Completion].

* **Display-Anzeigen (nur Drittanbieter)**: Display-Anzeigen sind animierte oder statische Bilder, die in Webbrowsern oder Apps angezeigt werden. Wenn Sie auf die Werbeeinheit klicken, gelangt der Benutzer zu einer Marken-Site oder auf eine Microsite. Die Anzeige eignet sich am besten, um effiziente CPMs zu fördern, die Nachrichtenzuordnung zu erhöhen, zusätzliche Marken- oder Produktkontaktpunkte hinzuzufügen und Benutzer im Kauftrichter nach unten zu treiben. Zu den wichtigsten Leistungsindikatoren für die Anzeige gehören [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]und [!UICONTROL Cost per Conversion]. DSP unterstützt eine Vielzahl von Anzeigengrößen für Anzeigenbanner.

* **Mobile Anzeigen (nur Drittanbieter)**: Mobile Anzeigen können im Pre-Roll-Video (VAST, MRAID) oder im standardmäßigen Anzeigeformat vorliegen. Mobile Pre-Roll-Videos können automatisch abgespielt oder per Klick abgespielt werden. Sie eignen sich am besten, um Besucher über mehrere Bildschirme zu erreichen. Die mobile Standardanzeige ist ein statisches Bild, das in mobilen Webbrowsern oder in Apps angezeigt wird und am besten dazu dient, digitale Videokäufe zu ergänzen, die Nachrichtenzuordnung zu fördern und zusätzliche Branding- oder Produkt-Touchpoints hinzuzufügen. Mobile Anzeigen können auch als Vollbild-Übernahmen oder als mobile Zwischenräume verwendet werden, bei denen es sich um mobile Anzeigen mit hoher Wirkung im Vollbildmodus handelt, die am besten dazu dienen, das Markenbewusstsein für mobile Zielgruppen zu entwickeln und Konversionen zu fördern.

* **Native Display-Anzeigen (nur Erstanbieter)**: Native Anzeigen werden im standardmäßigen Anzeigeformat unterstützt. Native Anzeigen beinhalten eine Überschrift und/oder einen Titel, eine Beschreibung, ein Logo und ein Bild. Die Anzeigenelemente werden so kombiniert und gerendert, dass sie dem Seitenstil des Herausgebers entsprechen, sodass die Anzeige mit dem organischen Inhalt des Herausgebers verschmolzen und die Interaktion erhöht wird. Native Inhalte werden am besten für Markenbewusstsein und zur Steigerung der Zielgruppenansichten und Interaktionsraten mit Viewer-freundlicher Werbung verwendet. Wichtige Leistungsindikatoren umfassen [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]und [!UICONTROL Cost Per Conversion].

* **Pre-Roll-Anzeigen (nur Drittanbieter)**: Pre-Roll-Anzeigen (VAST und VPAID) werden vor Premium-Videoinhalten angezeigt und bieten ein interaktives, ansprechendes Benutzererlebnis. Pre-Roll-Videos können interaktiv sein, Rich-Media-Funktionen enthalten und Überlagerungen, Rollover und Aktionsaufrufe enthalten. Zu den wichtigsten Leistungsindikatoren für Pre-Roll-Videoanzeigen gehören [!UICONTROL Video Completion Rate] und [!UICONTROL Viewability Rate].

* **Angeschlossene TV-Anzeigen (nur Drittanbieter)**: Angeschlossene TV-Anzeigen werden vor und während Premium-TV-Videoinhalten angezeigt. Alle angeschlossenen TV-Inventare werden auf TV-Geräten ausgeführt, d. h. das Video wird automatisch in einer Bildschirmumgebung mit schlankem Hintergrund wiedergegeben, die die Betrachter nicht überspringen können. Angeschlossenes Fernsehen ist das beste digitale Videoformat für Fernsehwerbung. Wichtige Leistungsindikatoren für Connected TV sind: [!UICONTROL Completion Rate].

* **Universelle Videoanzeigen (nur Drittanbieter)**: Mit universellen Videoanzeigen können Sie das Video-Inventar aus Desktop-, Mobil- und vernetzten TV-Umgebungen für VPAID- und VAST-Bestände mithilfe einer einzigen Videoplatzierung abrufen. Sie kombinieren alle Funktionen von vernetzten TV-, Pre-Roll- und mobilen Pre-Roll-Anzeigen und werden vor und während des Videoinhalts angezeigt. Zu den wichtigsten Leistungsindikatoren für universelle Videos gehören [!UICONTROL Completion Rate] und [!UICONTROL Viewability Rate].

   Universelle Videoanzeigen können nur an universelle Videoplatzierungen angehängt werden.

   Siehe[Häufig gestellte Fragen zu universellen Videos](/help/dsp/campaign-management/faq-universal-video.md)&quot; für weitere Informationen zu universellen Videoanzeigen.

## Genehmigungen DSP Anzeigen

Wenn Sie eine Anzeige erstellen, DSP sie für vertrauliche Kategorien überprüft, klicken Sie auf URL-Funktion und zeigen Sie eine Vorschau des Renderings an.

Zunächst wird ein roter Punkt im [!UICONTROL Status] Spalte. Der Überprüfungsprozess dauert normalerweise 24 bis 48 Stunden. Eine fehlerhafte Anzeige kann jedoch länger als 48 Stunden den Status &quot;Ausstehend&quot;aufweisen, sodass Sie Zeit haben, Fehler zu beheben, bevor die Anzeige abgelehnt wird. Abgelehnte Anzeigen enthalten einen Grund für die Ablehnung.

Wenn DSP eine Anzeige genehmigt, wird in der Spalte Status ein grüner Punkt angezeigt.

![Validierungsanzeiger in [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Ihre Werbeanzeige wird nur bereitgestellt, wenn sowohl DSP als auch die SSP die Kreativinhalte genehmigt haben. Jeder SSP hat seine eigenen Genehmigungsanforderungen und -prozesse.

>[!MORELIKETHIS]
>
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-multiple.md)
>* [Anzeigenspezifikationen](ad-specs.md)

