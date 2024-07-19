---
title: Anzeigeeinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Display-Anzeigen.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Anzeigeeinstellungen

Die folgenden Einstellungen gelten für standardmäßige Display-Anzeigen.

## [!UICONTROL Ad Options]

### Allgemein

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der von Ihnen erstellte Anzeigentyp, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann. Der Standardwert ist *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (wie z. B. Holiday Product Preview: 300x250 Gamer&quot;).

**\[Ad Source\]**: (schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Nur Anzeigen von Drittanbietern) Gibt an, dass die Anzeige eine erweiterbare Banneranzeige ist. Die zugehörigen Erweiterungsparameter bestimmen, welcher Bestand gekauft werden soll. Stellen Sie daher sicher, dass er das Anzeigenverhalten widerspiegelt.

**[!UICONTROL Expansion Method]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Gibt an, ob das Banner um *[!UICONTROL Click]* oder *[!UICONTROL Rollover]* erweitert wird.

**[!UICONTROL Expansion Directions]:** (Nur erweiterbare Banner von Drittanbietern) Die Richtung, in der sich die Anzeige erweitert: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* oder *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Der zertifizierte Anbieter, für den die Anzeige verfügbar ist: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* oder *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Nur Anzeigen von Drittanbietern) Die URL des kreativen Drittanbieter-Assets. Alle Parameter [timestamp] und [[timestamp]] werden durch tatsächliche Werte ersetzt.

**[!UICONTROL Final Display Code]:** (Nur Werbeanzeigen von Drittanbietern) Die URL für das kreative Asset von Drittanbietern, wobei ggf. die erforderlichen [Advertising DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) eingefügt werden.

**[!UICONTROL Ad Size]:** Die Breite und Höhe der Anzeige. Dabei muss es sich um eine [unterstützte standardmäßige Anzeigegröße ](ad-specs.md) handeln. Sie können die Anzeigengröße manuell eingeben, bevor Sie die Anzeige hochladen oder eine [!UICONTROL Display Code] eingeben. Wenn Sie die Anzeigengröße nicht eingeben, werden die Dimensionen der hochgeladenen Anzeige oder des Anzeigen-Tags automatisch als schreibgeschützt eingegeben.

>[!IMPORTANT]
>
> Die in den Feldern Breite und Höhe deklarierte Anzeigengröße wird mit den eingehenden Angebotsanfragen abgeglichen. Möglicherweise treten Versandprobleme auf, wenn die Dimensionen der Anzeige nicht mit der deklarierten Anzeigengröße übereinstimmen.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen. **Tipp:** Informationen zum Bearbeiten der Tracking-Pixel von Drittanbietern für mehrere Anzeigen in einer Platzierung auf einmal mithilfe der [!UICONTROL Ad Tools]-Ansicht finden Sie unter &quot;[Verfolgungspixel von Drittanbietern an Anzeigen an eine Platzierung anhängen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, durch das das Pixel ausgelöst wird. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* oder *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Auflisten der mit einer Anzeige verknüpften Platzierungen](ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
