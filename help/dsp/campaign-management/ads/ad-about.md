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

DSP unterstützt die Bereitstellung von Anzeigen über Ad-Serving-Tags von Drittanbietern (wie Google, Flashtalking oder Sizmek) für verschiedene Anzeigentypen und den direkten Asset-Upload für native Display-Anzeigen. Sie können Drittanbieter-Tags einzeln oder stapelweise hochladen. Massen-Uploads verwenden Partner-Tag-Blätter oder eine Massen-Tag-Vorlage.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Hängen Sie nach der Einrichtung Ihrer Anzeigen jede Anzeige an eine oder mehrere Platzierungen an, die die Zielgruppenbestimmungsparameter (wie Geografie, Zielgruppe, Gerät und Inventar-Targeting) enthalten, die steuern, wie Ihre Kampagne Ergebnisse liefert. Sie müssen eine Anzeige an eine Platzierung anhängen, um mit der Ausführung der Anzeige zu beginnen.

## Verfügbare Anzeigentypen {#ad-types}

Alle folgenden Anzeigentypen sind in DSP verfügbar. Die vollständigen Spezifikationen für jeden Anzeigentyp finden Sie unter [Anzeigenspezifikationen](ad-specs.md).

* **Audioanzeigen (nur von Drittanbietern)**: Audioanzeigen werden zwischen Inhalten auf digitalen Publisher-Sites wiedergegeben und können eigenständig als Audiodateien oder zusammen mit begleitenden Bannern ausgeführt werden. Audio wird am besten verwendet, um das Markenbewusstsein zu steigern und mit Zielgruppen unterwegs zu interagieren. Zu den wichtigsten Leistungsindikatoren für Audio gehören [!UICONTROL Completion Rate] und [!UICONTROL Cost per Completion].

* **Display-Anzeigen (nur Drittanbieter)**: Display-Anzeigen sind animierte oder statische Bilder, die in Webbrowsern oder in Apps angezeigt werden. Durch Klicken auf die Werbeeinheit gelangt der Benutzer zu einer gebrandeten Website oder Microsite. Display eignet sich am besten, um effiziente CPMs zu fördern, die Nachrichtenzuordnung zu verbessern, zusätzliche Marken- oder Produkt-Touchpoints hinzuzufügen und Benutzer den Einkaufstrichter hinunter zu bringen. Zu den wichtigsten Leistungsindikatoren für die Anzeige gehören [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] und [!UICONTROL Cost per Conversion]. DSP unterstützt eine Vielzahl von Anzeigengrößen für Anzeigenbanner.

* **Mobile Anzeigen (nur Drittanbieter)**: Mobile Anzeigen können im Pre-Roll-Video- (VAST, MRAID) oder Standard-Anzeigeformat vorliegen. Mobile Pre-Roll-Videos können automatisch oder per Klick wiedergegeben werden und eignen sich am besten, um Viewer über mehrere Bildschirme zu erreichen. Bei der standardmäßigen Mobilgeräteanzeige handelt es sich um ein statisches Bild, das in mobilen Webbrowsern oder in Apps angezeigt wird. Es wird am besten verwendet, um digitale Videoeinkäufe zu ergänzen, die Nachrichtenverknüpfung zu fördern und zusätzliche Branding- oder Produkt-Touchpoints hinzuzufügen. Mobile Anzeigen können auch als Vollbild-Übernahmen oder als mobile Zwischenräume fungieren, bei denen es sich um leistungsstarke Mobile-Anzeigen im Vollbildmodus handelt, die am besten verwendet werden, um Markenbewusstsein für mobile Zielgruppen zu entwickeln und Konversionen zu fördern.

* **Native Display-Anzeigen (nur Erstanbieter)**: Native Anzeigen werden im Standard-Anzeigeformat unterstützt. Native Anzeigen enthalten eine Überschrift und/oder einen Titel, eine Beschreibung, ein Logo und ein Bild. Die Anzeigenelemente werden kombiniert und gerendert, sodass sie dem Seitenstil des Herausgebers entsprechen. Die Anzeige fügt sich somit in den organischen Inhalt des Herausgebers ein und steigert die Interaktion. Native wird am besten zur Markenwahrnehmung und zur Steigerung der Zuschaueransichts- und Interaktionsraten mit schauerfreundlicher Werbung verwendet. Zu den wichtigsten Leistungsindikatoren gehören [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] und [!UICONTROL Cost Per Conversion].

* **Pre-roll-Anzeigen (nur Drittanbieter)**: Pre-roll-Anzeigen (VAST und VPAID) werden vor Premium-Videoinhalten angezeigt und bieten ein immersives, ansprechendes Zuschauererlebnis. Pre-Roll-Videos können interaktiv sein, Rich-Media-Funktionen enthalten und Überlagerungen, Rollover und Aktionsaufrufe enthalten. Zu den wichtigsten Leistungsindikatoren für Pre-roll-Videoanzeigen gehören [!UICONTROL Video Completion Rate] und [!UICONTROL Viewability Rate].

* **Connected TV-Anzeigen (nur Drittanbieter)**: Verbundene TV-Anzeigen werden vor und während Premium-TV-Videoinhalten angezeigt. Der gesamte verbundene TV-Bestand wird auf TV-Geräten ausgeführt, d. h. Videos werden automatisch in einer lean-back-Vollbildumgebung wiedergegeben, die Zuschauer nicht überspringen können. Connected TV ist das digitalste Videoformat, das TV-Werbespots am nächsten kommt. Zu den wichtigsten Leistungsindikatoren für Connected TV gehören [!UICONTROL Completion Rate].

* **Universelle Videoanzeigen (nur von Drittanbietern)**: Mit universellen Videoanzeigen können Sie den Videobestand von Desktop-, Mobile- und verbundenen TV-Umgebungen für VPAID- und VAST-Inventar über eine einzige Videoplatzierung auswählen. Sie kombinieren alle Funktionen von Connected TV, Pre-Roll- und Mobile Pre-Roll-Anzeigen und werden vor und während Videoinhalten angezeigt. Zu den wichtigsten Leistungsindikatoren für universelle Videos gehören [!UICONTROL Completion Rate] und [!UICONTROL Viewability Rate].

  Universelle Videoanzeigen können nur an Platzierungen für universelle Videos angehängt werden.

  Weitere Informationen [ universellen Videoanzeigen finden Sie ](/help/dsp/campaign-management/faq-universal-video.md) „FAQs zu universellen“.

## DSP-Anzeigengenehmigungen

Wenn Sie eine Anzeige erstellen, prüft die DSP diese auf sensible Kategorien, klickt auf URL-Funktionen und zeigt eine Vorschau für das Rendering an.

Zunächst zeigt die [!UICONTROL Status] der Anzeige einen roten Punkt an. Der Überprüfungsprozess dauert normalerweise 24-48 Stunden. Eine beschädigte Anzeige kann jedoch länger als 48 Stunden den Status „Ausstehend“ aufweisen, sodass Sie Zeit haben, Fehler zu beheben, bevor die Anzeige abgelehnt wird. Abgelehnte Werbeanzeigen enthalten einen Grund für die Ablehnung.

Wenn DSP eine Anzeige genehmigt, wird in der Spalte Status der Anzeige ein grüner Punkt angezeigt.

![Genehmigungsindikator in [!UICONTROL Status] Spalte](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Ihre Anzeige kann nur geschaltet werden, wenn sowohl DSP als auch SSP die Kreativität genehmigt haben. Jeder SSP hat seine eigenen Genehmigungsanforderungen und -prozesse.

>[!MORELIKETHIS]
>
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Erstellen Sie mehrere Anzeigen von Drittanbietern](ad-create-multiple.md)
>* [Anzeigenspezifikationen](ad-specs.md)
