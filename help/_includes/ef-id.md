---
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Adobe Advertising EF-IDs

## Adobe Advertising EF-IDs

Die EF ID ist ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Anzeigenbelichtung auf individueller Browser- oder Geräteebene zu verknüpfen. EF-IDs dienen hauptsächlich als Schlüssel zum Senden von [!DNL Analytics] und Customer Journey Analytics-Daten an Adobe Advertising für die Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

[!DNL Analytics] wird die EF-ID in der Dimension [eine [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) oder [!DNL rVar] (reservierte [!DNL eVar]) (Adobe Advertising EF ID) gespeichert.

Bei Customer Journey Analytics wird die EF-ID in der `trackingIdentities`-Eigenschaft des `conversionDetails`-Objekts gespeichert, das Teil der [[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) ist.

### EF ID-Formate {#ef-id-formats}

>[!NOTE]
>
>Bei EF-IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics]- oder Customer Journey Analytics-Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf die Gebote und das Reporting von Adobe Advertising aus, hat jedoch keine Auswirkungen auf das Reporting von Adobe Advertising in [!DNL Analytics] oder Customer Journey Analytics.

#### [!DNL Google Ads] Suchanzeigen

```
{gclid}:G:s
```

Dabei gilt:

* `gclid` ist die [!DNL Google Click ID] (GCLID).
* `s` ist der Netzwerktyp („s“ für Suche).

#### [!DNL Microsoft Advertising] Suchanzeigen

```
{msclkid}:G:s
```

Dabei gilt:

* `msclkid` ist die [!DNL Microsoft Click ID] (MSCLKID).
* `s` ist der Netzwerktyp („s“ für Suche).

#### Anzeigen und Suchanzeigen in anderen Suchmaschinen anzeigen

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

Dabei gilt:

* &lt;*Adobe Advertising-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. UhKVaAAABCkJ0mDt). Wird auch als &quot;*ID“*.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTT-HHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19:25:33).

* &lt;*channel type*> ist der Kanaltyp, der für das Klicken oder Belichten verantwortlich ist:

   * `d` für einen Klick auf eine DSP-Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP-Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Such-Clickthrough).

Beispiel `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
