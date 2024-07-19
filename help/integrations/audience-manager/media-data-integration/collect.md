---
title: Erfassen von Klick- und Impressionsdaten aus Advertising DSP-Kampagnen
description: Erfahren Sie, wie Sie Cookie-basierte Impressions- und Klickereignisse aus Advertising DSP-Anzeigen mit Audience Manager-Pixeln erfassen.
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Erfassen von Medienbelichtungsdaten aus Advertising DSP-Kampagnen

*Advertiser nur mit Advertising DSP*

*Advertiser mit nur einer Adobe Advertising-Adobe Audience Manager-Integration*

In diesem Dokument wird beschrieben, wie Sie Advertising DSP-Anzeigen taggen, um Cookie-basierte Impressions- und Klickereignisse mithilfe von Audience Manager-Pixeln zu erfassen, sowie zusätzliche Aufgaben, die zur Verwendung der Daten erforderlich sind.

Die Ereignispixel erfassen keine Ereignisse, die in Cookie-losen Umgebungen wie mobilen Apps und vernetztem TV (CTV) auftreten.

## Schritt 1: Einrichten einer Data Source in Audience Manager {#set-up-data-source}

Erstellen Sie in Audience Manager eine [Datenquelle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) für die DSP Impressions- und Klickdaten. Schließen Sie die Datenquellen-ID [in jedes Ereignis-Tag](#implement-dsp-pixels) ein, damit alle verfolgten Ereignisse der Datenquelle zugeordnet werden.

>[!NOTE]
> Es ist möglich, alle Impressions- und Klickdaten für Werbekampagnen zu erfassen, die auf mehreren DSP in einer Datenquelle ausgeführt werden.

## Schritt 2: Implementieren von Impression und Klicken auf Ereignispixel auf Webseiten {#implement-dsp-pixels}

Advertiser können Ereignis-Tags für ihre eigenen Marken erstellen und implementieren. Wenden Sie sich bei Bedarf an Ihren Adobe Audience Manager-Berater oder Ihr Adobe-Account-Team, um Support zu erhalten.

>[!NOTE]
>
>Wenn Ihr Unternehmen das [!DNL Analytics]-Tracking verwendet, ist möglicherweise kein Klick-Tracking für Audience Manager erforderlich. Adobe Analytics erfasst Klicksignale und kann diese über die [serverseitige Weiterleitung](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) an den Audience Manager senden.

### Pixel-Syntax

Die Ereignispixel müssen die folgenden Parameter enthalten.

**Impression-Tracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionalen zusätzlichen Parametern](#parameters) mit dem Präfix `&`

**Klick-Tracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionalen zusätzlichen Parametern](#parameters) mit dem Präfix `&`

Dabei gilt:

* `[Audience Manager customer domain]` ist der Domänenname, der Impressions- oder Klickereignisse an [!DNL Adobe] sendet.

* `[source id]` ist die ID für die [Datenquelle](#set-up-data-source), in der Sie DSP Impressions- und Klickdaten verfolgen.

* `[redirect URL]` ist die doppelt kodierte Umleitungs-URL. Wenn Sie ein Online-Kodierungs-Tool wie www.urlencoder.org verwenden, führen Sie die Zeichenfolge über den Kodierer aus und kodieren Sie das Ergebnis neu.

* `${TM_CAMPAIGN_ID_NUM}` ist die numerische Kampagnen-ID in DSP. Wenn Sie eine einzelne Kampagnen-ID hartcodieren möchten, anstatt das DSP-Makro zu verwenden, suchen Sie die ID in den Kampagneneinstellungen.

* Jedem [Parameter](#key-value-pairs) wird `&` vorangestellt und liegt im Format `d_parameter=parameter_id` vor, wobei `parameter` durch das Schlüssel-Wert-Paar für das neue Feld ersetzt wird. Beispiel: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parameter als Schlüssel-Wert-Paare {#parameters}

**Format:** `d_parameter=parameter_id`

    wobei:
    
    * dem Parameter das Präfix &quot;&amp;`
    
    * &quot;Parameter&quot;vorangestellt wird durch das Schlüssel-Wert-Paar für das neue Feld ersetzt
    
    Beispiel: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Beide Pixeltypen können zusätzliche Parameter wie *Schlüssel-Wert-Paare* enthalten, um Eigenschaften zu erfassen oder Kampagnen-Metadaten (z. B. einen Platzierungsnamen oder einen Kampagnennamen) für andere Berichte bereitzustellen. Ein Schlüssel-Wert-Paar besteht aus zwei verwandten Elementen: einem *Schlüssel*, der eine Konstante ist, die den Datensatz definiert, und einem *Wert*, der eine Variable ist, die zum Satz gehört.

Im Schlüssel-Wert-Paar kann die Wertvariable entweder eine fest codierte ID oder ein *macro* sein. Hierbei handelt es sich um eine kleine Einheit aus eigenständigem Code, der dynamisch durch die entsprechenden Werte ersetzt wird, wenn das Anzeigen-Tag zum Kampagnen- und Benutzertracking geladen wird. Für kampagnenbezogene Parameter können Sie mit [DSP Makros](/help/dsp/campaign-management/macros.md) anstelle von Audience Manager-Makros Kampagnenattribute zusammen mit den entsprechenden Impressions- oder Klickdaten an den Audience Manager senden, wobei ein einzelnes Pixel für alle Anzeigen verwendet wird. Die DSP Makros, die Sie in Ihre Ereignispixel einfügen, müssen geeignete Werte für die Schlüssel-Wert-Paare sein, die Sie in die Pixel einschließen. Beispielsweise würden Sie für den Schlüssel `d_placement` das DSP Makro `${TM_PLACEMENT_ID_NUM}` als Wert verwenden, um die vom Adobe Advertising-Makro generierten Platzierungs-IDs zu erfassen.

Eine Liste der Makros, die von Audience Manager für Impressionsereignispixel unterstützt werden, finden Sie unter &quot;[Erfassen von Kampagnenimpressionsdaten über Pixelaufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)&quot;.

Eine Liste der Makros, die Audience Manager für Klickereignis-Pixel unterstützt, finden Sie unter &quot;[Erfassen von Kampagnen-Klickdaten über Pixelaufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)&quot;.

>[!TIP]
>
>* Die Best Practice besteht darin, die Kampagnen-, Platzierungs-, Kreativ- (Anzeigen) und Site-IDs einzubeziehen, damit Sie die Kampagnenattribute verwenden können, um Audience Manager-Eigenschaften zu erstellen.
>* Zur Erstellung von Audience Optimization-Berichten sind zusätzliche Parameter erforderlich.
>* Ersetzen Sie in den Schlüssel-Wert-Paaren die Werte durch die relevanten [DSP Makros](/help/dsp/campaign-management/macros.md) , damit Sie in allen Kampagnen ein Pixel für alle Anzeigen verwenden können. Ändern Sie beispielsweise `d_campaign=[%campaignID%]`in `d_campaign=${TM_CAMPAIGN_ID_NUM}`, um vom Adobe Advertising-Makro generierte Kampagnen-IDs zu erfassen.
>* Sie können bei Bedarf eigene Parameter mit fest programmierten Werten erstellen. Beispiel: `d_DSP=AdCloud`

Beispiel eines Impression-Ereignispixel:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Hinzufügen der Pixel

#### Impression-Tracking-Pixel

Fügen Sie allen Anzeigen in Ihren [!DNL DSP]-Kampagnen ein Pixel für das Impression-Ereignis-Tracking hinzu. Sie können dies an einer der folgenden Stellen tun:

* Auf Platzierungsebene, die das Pixel standardmäßig auf alle Anzeigen in der Platzierung anwendet. Fügen Sie im Abschnitt Tracking der Platzierungseinstellungen das Pixel im Feld [[!UICONTROL Event pixels]](/help/dsp/campaign-management/placements/placement-settings.md) hinzu.

* Auf Anzeigenebene, die alle Ereignispixel auf Platzierungsebene überschreibt. Erstellen Sie in den Anzeigeneinstellungen ein Ereignispixel auf der Registerkarte [!UICONTROL Pixel]](/help/dsp/campaign-management/ads/ad-edit.md).[

* (Für Anzeigen auf einem Drittanbieter-Anzeigenserver) Auf Anzeigenebene innerhalb des Werbeservers.

#### Klick-Tracking-Pixel

Fügen Sie innerhalb des Anzeigen-Servers das Clickevent-Pixel (mit angehängter kodierter URL) an der Stelle ein, an der Sie normalerweise die Clickthrough-URL der Anzeige einfügen.

## Schritt 3: Aufgaben nach der Implementierung

Sobald die Ereignis-Tags implementiert sind, fließen die Daten in die Datenerfassungsserver des Audience Managers. Führen Sie die folgenden Aufgaben aus, bevor Sie die Daten in Berichten verwenden können.

### Erstellen eines [!DNL Amazon S3]-Buckets und einer Daten-Source

Sobald sich Ihre Daten auf den Audience Manager-Servern befinden, müssen Sie einen [!DNL Amazon Simple Storage Service] -Bucket ([!DNL Amazon S3]) und dann eine Datenquelle erstellen, an die alle Pixeldaten gesendet werden. Wenden Sie sich an Ihren Audience Manager-Berater oder an die [Kundenunterstützung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html), wenn Sie Support benötigen.

### Erstellen von Audience Manager-Eigenschaften und -Segmenten

Ihre Ereignisdaten fließen als [nicht verwendete Signale](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html) in den Audience Manager. Erstellen Sie manuell [regelbasierte Eigenschaften](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) aus den erfassten Daten und dann [Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) mit diesen Eigenschaften, bevor Sie die Daten in Berichten verwenden können.

Beispieleigenschaft, mit der Benutzerdaten für Benutzer gefüllt werden, die einem bestimmten kreativen Element in DSP ausgesetzt sind:

1. Identifizieren Sie das Ereignis als &quot;`d_event = imp`&quot;.
1. Identifizieren Sie die kreative ID in der DSP Kampagne und ordnen Sie sie dann der Eigenschaft als `d_creative=[Creative ID]` zu.

![Erstellungsbildschirm einer Eigenschaft](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP Makros](/help/dsp/campaign-management/macros.md)
>* [Überblick über das Senden von DSP-Expositionsdaten an Adobe Audience Manager](overview.md)
>* [Anwendungsfälle](use-cases.md)
