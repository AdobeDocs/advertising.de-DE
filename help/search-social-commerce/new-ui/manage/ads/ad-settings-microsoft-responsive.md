---
title: Responsive Anzeigeneinstellungen [!DNL Microsoft Advertising]
description: Verweisen Sie auf die Einstellungen für  [!DNL Microsoft Advertising]  Anzeigen.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# Einstellungen für responsive Anzeigen (Zielgruppe) [!DNL Microsoft Advertising]

Das responsive Anzeigenformat ist für bildbasierte, videobasierte und verbundene videobasierte TV-Zielgruppenanzeigen auf dem [!DNL Microsoft Audience Network] verfügbar. Das Anzeigennetzwerk stellt responsive Anzeigen dynamisch zusammen und verwendet dabei die effektivsten Kombinationen aus Anzeigenelementen.

## [!UICONTROL Basic Settings]

*Nur neue Anzeigen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### Videoanzeigen

**[!UICONTROL Videos]:** Die URL einer Videoanzeige.

**[!UICONTROL Status]:** Der Anzeigenstatus: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

### Bildanzeigen)

>[!NOTE]
>
>Das Werbenetzwerk erstellt automatisch Anzeigen für Zielgruppenkampagnen, die mit einem Händler-Center-Store über die Produktinformationen des Stores und das Benutzer-Targeting auf Anzeigengruppenebene verknüpft sind. Sie müssen keine Anzeigen manuell erstellen.

**[!UICONTROL Images]:** Bis zu 15 JPEG- oder PNG-Bilder für die Anzeige. Mindestens ein Bild mit einem Seitenverhältnis von 1,91:1 einschließen. Siehe die zulässigen Seitenrationen und Dimensionen für [Zielgruppen-Anzeigenbilder](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Für Zielgruppenanzeigen schneidet [!DNL Microsoft Advertising] dieses Bild automatisch für alle möglichen Seitenverhältnisse zu.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** Der Unternehmensname mit maximal 25 Zeichen. Sie kann in Anzeigenformaten verwendet werden, die nur für Aufrufe verfügbar sind.

**[!UICONTROL Short Headlines]:** Mindestens drei und bis zu 15 kurze Überschriften mit jeweils mindestens einem Wort und maximal 30 Zeichen.

**[!UICONTROL Long Headlines]:** Mindestens drei und bis zu fünf lange Überschriften mit jeweils maximal 90 Zeichen.

**[!UICONTROL Ad Text]:** Mindestens zwei und bis zu vier Beschreibungen mit mindestens einem Wort und höchstens 90 Zeichen.

**[!UICONTROL Status]:** Der Anzeigenstatus: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Anzeigen verwalten](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
