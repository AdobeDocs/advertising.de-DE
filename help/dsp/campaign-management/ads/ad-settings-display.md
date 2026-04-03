---
title: Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Display-Anzeigen.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
TQID: https://experienceleague.adobe.com/bcuGR2fzcwjvPcWisdQZBbU8vcaZhgW2qZPAXjV5ndM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Anzeigeneinstellungen

Die folgenden Einstellungen gelten für Standard-Display-Anzeigen.

## [!UICONTROL Ad Options]

### Einfach

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, dem die Anzeige angehängt werden kann. Standardwert ist *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Der Anzeigename. Der Asset-Titel wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads] und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. „Holiday Product Preview: 300x250 Gamer„).

**\[Ad Source\]**: (Schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Nur Anzeigen von Drittanbietern) Zeigt an, dass die Anzeige eine erweiterbare Banneranzeige ist. Die zugehörigen Erweiterungseinstellungen bestimmen, welches Inventar gekauft werden soll. Stellen Sie daher sicher, dass sie das Anzeigenverhalten widerspiegeln.

**[!UICONTROL Expansion Method]:** (Nur erweiterbare Banner-Anzeigen von Drittanbietern) Ob das Banner beim *[!UICONTROL Click]* oder *[!UICONTROL Rollover]* erweitert wird.

**[!UICONTROL Expansion Directions]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Die Richtung, in die die Anzeige erweitert wird: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* oder *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Der zertifizierte Anbieter, für den die Anzeige verfügbar ist: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* oder *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (nur Anzeigen von Drittanbietern) Die URL des Kreativ-Assets eines Drittanbieters. Alle [Zeitstempel] und [[Zeitstempel]]-Parameter werden durch die tatsächlichen Werte ersetzt.

**[!UICONTROL Final Display Code]:** (nur Anzeigen von Drittanbietern) Die URL für das Kreativ-Asset eines Drittanbieters, mit den erforderlichen [Advertising DSP-](/help/dsp/campaign-management/macros.md), falls zutreffend.

**[!UICONTROL Ad Size]:** Die Breite und Höhe der Anzeige. Es muss sich um eine [unterstützte Standard-Anzeigengröße](ad-specs.md) handeln. Sie können die Anzeigengröße manuell eingeben, bevor Sie die Anzeige hochladen, oder eine [!UICONTROL Display Code] eingeben. Wenn Sie die Anzeigengröße nicht eingeben, werden die Dimensionen der hochgeladenen Anzeige oder des Anzeigen-Tags automatisch als schreibgeschützt eingegeben.

>[!IMPORTANT]
>
> Die in den Feldern Breite und Höhe angegebene Anzeigengröße wird mit eingehenden Angebotsanfragen abgeglichen. Es kann zu Versandproblemen kommen, wenn die Dimensionen der Anzeige nicht mit der deklarierten Anzeigengröße übereinstimmen.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung in Advertising DSP](ad-about.md)
>* [Erstellen einer einzelnen Anzeige](ad-create.md)
>* [Platzierungen auflisten, die mit einer Anzeige verbunden sind](ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
