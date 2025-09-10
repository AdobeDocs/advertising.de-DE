---
source-git-commit: 56c27461cf0e1d7111de9d35d9e38fa980af4c52
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---
# EF ID-Formate

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
