---
source-git-commit: 8c36de7ffe73f86a4e78f11e38cd84fa59134833
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---
# Adobe Advertising EF-IDs

## Adobe Advertising EF-IDs

Die EF ID ist ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Werbeunterbrechung zu verknüpfen. Die EF-ID wird in der Dimension [eine [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) oder [!DNL rVar] (reservierte [!DNL eVar]) (Adobe Advertising-EF-ID) gespeichert und verfolgt jeden Anzeigenklick oder jede Offenlegung auf individueller Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel für die Übermittlung von [!DNL Analytics] an Adobe Advertising zur Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

### EF-ID-Format

>[!NOTE]
>
>Bei EF-IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics]-Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf die Adobe Advertising-Gebote und -Berichte aus, hat jedoch keine Auswirkungen auf das Adobe Advertising-Reporting in [!DNL Analytics].

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
