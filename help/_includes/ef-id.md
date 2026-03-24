---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# Adobe Advertising EF-IDs

## Adobe Advertising EF-IDs

Die EF ID ist ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Anzeigenbelichtung auf individueller Browser- oder Geräteebene zu verknüpfen. EF-IDs dienen hauptsächlich als Schlüssel zum Senden von [!DNL Analytics] und Customer Journey Analytics-Daten an Adobe Advertising für die Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

[!DNL Analytics] wird die EF-ID in der Dimension [eine [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder [!DNL rVar] (reservierte [!DNL eVar]) (Adobe Advertising EF ID) gespeichert.

Bei Customer Journey Analytics wird die EF-ID in der `trackingIdentities`-Eigenschaft des `conversionDetails`-Objekts gespeichert, das Teil der [[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) ist.

### EF ID-Formate {#ef-id-formats}

Siehe [Formate für EF ID-Dimensionselemente](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items) im Adobe Analytics-Komponentenhandbuch.

>[!NOTE]
>
>Bei EF-IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics]- oder Customer Journey Analytics-Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf die Gebote und das Reporting von Adobe Advertising aus, hat jedoch keine Auswirkungen auf das Reporting von Adobe Advertising in [!DNL Analytics] oder Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
