---
title: Erfassen von Klick- und Impressionsdaten aus Advertising DSP Campaign
description: Erfahren Sie, wie Sie Cookie-basierte Impression- und Klickereignisse aus Advertising DSP-Anzeigen mithilfe von Audience Manager-Pixeln erfassen.
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Erfassen von Daten zur Medienexposition aus Advertising DSP-Kampagnen

*Nur Werbetreibende mit Advertising DSP*

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Audience Manager-Integration*

In diesem Dokument wird erläutert, wie Sie Advertising DSP-Anzeigen taggen können, um Cookie-basierte Impression- und Klickereignisse mit Audience Manager-Pixeln zu erfassen, und wie Sie zusätzliche Aufgaben ausführen, um die Daten zu verwenden.

Die Ereignispixel erfassen keine Ereignisse, die in Umgebungen ohne Cookies auftreten, z. B. in mobilen Apps und im vernetzten Fernsehen (CTV).

## Schritt 1: Einrichten einer Daten-Source in Audience Manager {#set-up-data-source}

Erstellen Sie im Audience Manager eine [Datenquelle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=de) für die DSP-Impression und klicken Sie auf Daten. Schließen Sie die Datenquellen-ID [in jedes Ereignis-](#implement-dsp-pixels) ein, sodass alle verfolgten Ereignisse der Datenquelle zugeordnet werden.

>[!NOTE]
> Sie haben die Möglichkeit, alle Impressions- und Klickdaten für Werbekampagnen, die auf mehreren DSP ausgeführt werden, in einer einzigen Datenquelle zu erfassen.

## Schritt 2: Implementieren von Impression- und Klick-Ereignis-Pixeln auf Webseiten {#implement-dsp-pixels}

Werbetreibende können Ereignis-Tags für ihre eigenen Marken erstellen und implementieren. Wenden Sie sich bei Bedarf an Ihren Adobe Audience Manager-Berater oder Ihr Adobe-Account-Team.

>[!NOTE]
>
>Wenn Ihr Unternehmen [!DNL Analytics]-Tracking verwendet, benötigen Sie möglicherweise kein Audience Manager-Klick-Tracking. Adobe Analytics erfasst Klicksignale und kann diese über die [Server-seitige Weiterleitung“ an &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=de) Audience Manager senden.

### Pixel-Syntax

Ereignispixel müssen die folgenden Parameter enthalten.

**Impression-Tracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionalen zusätzlichen Parametern](#parameters) mit dem Präfix `&`

**Klick-Tracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionalen zusätzlichen Parametern](#parameters) mit dem Präfix `&`

Dabei gilt:

* `[Audience Manager customer domain]` ist der Domain-Name, der Impression- oder Klickereignisse an [!DNL Adobe] sendet.

* `[source id]` ist die ID für die [Datenquelle“, in &#x200B;](#set-up-data-source) Sie DSP-Impressions- und Klickdaten verfolgen.

* `[redirect URL]` ist die doppelt kodierte Umleitungs-URL. Wenn Sie ein Online-Kodierungstool wie www.urlencoder.org verwenden, führen Sie die Zeichenfolge durch den Kodierer aus und kodieren Sie das Ergebnis erneut.

* `${TM_CAMPAIGN_ID_NUM}` ist die numerische Kampagnen-ID in DSP. Wenn Sie eine einzelne Kampagnen-ID fest kodieren möchten, anstatt das DSP-Makro zu verwenden, suchen Sie die ID in den Kampagneneinstellungen.

* Jedem [Parameter](#key-value-pairs) wird das Präfix `&` vorangestellt. Es hat das Format `d_parameter=parameter_id`, wobei `parameter` durch das Schlüssel-Wert-Paar für das neue Feld ersetzt wird. Beispiel: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parameter als Schlüssel-Wert-Paare {#parameters}

**format:** `d_parameter=parameter_id`

    Wobei:
    
    * dem Parameter das Präfix &quot;&amp;&quot; vorangestellt 
    
    * „parameter“ wird durch das Schlüssel-Wert-Paar für das neue Feld ersetzt
    
    Beispiel: &quot;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&quot;

Beide Pixeltypen können zusätzliche Parameter als *Schlüssel-Wert-Paare* enthalten, um Eigenschaften zu erfassen oder Kampagnenmetadaten (z. B. einen Platzierungs- oder Kampagnennamen) für andere Berichte bereitzustellen. Ein Schlüssel-Wert-Paar besteht aus zwei zusammenhängenden Elementen: einem *Schlüssel*, bei dem es sich um eine Konstante handelt, die den Datensatz definiert, und einem *Wert*, bei dem es sich um eine Variable handelt, die zum Satz gehört.

Im Schlüssel-Wert-Paar kann die Wertvariable entweder eine hartcodierte ID oder ein *Makro* sein. Dies ist eine kleine Einheit eigenständigen Codes, die dynamisch durch die entsprechenden Werte ersetzt wird, wenn das Anzeigen-Tag für das Kampagnen- und Benutzer-Tracking geladen wird. Für kampagnenbezogene Parameter können Sie [DSP-Makros](/help/dsp/campaign-management/macros.md) anstelle von Audience Manager-Makros verwenden, um Kampagnenattribute mit den zugehörigen Impressions- oder Klickdaten an den Audience Manager zu senden, wobei für alle Anzeigen ein einziges Pixel verwendet wird. Die DSP-Makros, die Sie in die Ereignispixel einfügen, müssen geeignete Werte für die Schlüssel-Wert-Paare sein, die Sie in die Pixel aufnehmen. Für den `d_placement` würden Sie beispielsweise die DSP-Makro-`${TM_PLACEMENT_ID_NUM}` als Wert verwenden, um die vom Adobe Advertising-Makro generierten Platzierungs-IDs zu erfassen.

Eine Liste der Makros, die Audience Manager für Impressionsereignis-Pixel unterstützt, finden Sie unter &quot;[&#x200B; von Campaign-Impressionsdaten über Pixel-Aufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=de#supported-key-value-pairs).

Eine Liste der Makros, die Audience Manager für Klick-Ereignispixel unterstützt, finden Sie unter &quot;[&#x200B; von Kampagnenklick-Daten über Pixelaufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=de).

>[!TIP]
>
>* Es empfiehlt sich, die Kampagnen-, Platzierungs-, Kreativ- (Anzeige-) und Site-IDs einzuschließen, damit Sie die Kampagnenattribute zum Erstellen von Audience Manager-Eigenschaften verwenden können.
>* Zum Erstellen von Audience Optimization-Berichten sind zusätzliche Parameter erforderlich.
>* Ersetzen Sie in den Schlüssel-Wert-Paaren die Werte durch die entsprechenden [DSP](/help/dsp/campaign-management/macros.md)Makros, damit Sie in allen Kampagnen ein einziges Pixel für alle Anzeigen verwenden können. Ändern Sie beispielsweise `d_campaign=[%campaignID%]`auf `d_campaign=${TM_CAMPAIGN_ID_NUM}`, um die vom Adobe Advertising-Makro generierten Kampagnen-IDs zu erfassen.
>* Sie können bei Bedarf eigene Parameter mit hartcodierten Werten erstellen. Beispiel: `d_DSP=AdCloud`

Beispiel für ein Impression-Ereignis-Pixel:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Hinzufügen der Pixel

#### Impression-Tracking-Pixel

Hängen Sie allen Anzeigen in Ihren [!DNL DSP]-Kampagnen ein Impression-Event-Tracking-Pixel an. Sie können dies an einem der folgenden Orte tun:

* Auf der Platzierungsebene, wodurch das Pixel standardmäßig auf alle Anzeigen in der Platzierung angewendet wird. Fügen Sie im Abschnitt Tracking der Platzierungseinstellungen das Pixel in das Feld [[!UICONTROL Event pixels] ein](/help/dsp/campaign-management/placements/placement-settings.md).

* Auf Anzeigenebene, wodurch alle Ereignispixel auf Platzierungsebene überschrieben werden. Klicken Sie in den [&#x200B; auf der Registerkarte [!UICONTROL Pixel] auf „Ereignis-Pixel erstellen](/help/dsp/campaign-management/ads/ad-edit.md).

* (Bei Anzeigen auf einem Werbeserver eines Drittanbieters) Auf Anzeigenebene innerhalb des Anzeigenservers.

#### Klick-Tracking-Pixel

Fügen Sie innerhalb des Anzeigenservers das Klick-Ereignis-Pixel (an das die kodierte URL angehängt ist) an der Stelle ein, an der Sie normalerweise die Clickthrough-URL der Anzeige einfügen.

## Schritt 3: Aufgaben nach der Implementierung

Sobald die Ereignis-Tags implementiert sind, fließen die Daten in die Datenerfassungs-Server des Audience Managers. Führen Sie die folgenden Aufgaben aus, bevor Sie die Daten in Berichten verwenden können.

### Erstellen eines [!DNL Amazon S3] Buckets und einer Daten-Source

Sobald sich Ihre Daten auf den Audience Manager-Servern befinden, müssen Sie einen [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) Bucket und dann eine Datenquelle erstellen, an die alle Pixeldaten gesendet werden. Wenden Sie sich an Ihren Audience Manager-Berater oder [Kundenunterstützung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=de), wenn Sie Unterstützung benötigen.

### Erstellen von Audience Manager-Eigenschaften und Segmenten

Ihre Ereignisdaten fließen als &quot;[&quot; in den Audience Manager &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=de). Erstellen Sie [&#x200B; aufgenommenen Daten manuell (](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=de) [) und &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=de) diese Eigenschaften dann (Segmente), bevor Sie die Daten in Berichten verwenden können.

Beispieleigenschaft, die Daten auf Benutzerebene für Benutzende ausfüllt, die einer bestimmten kreativen Aktivität in DSP ausgesetzt sind:

1. Ermitteln Sie das Ereignis als `d_event = imp`.
1. Identifizieren Sie die Kreativ-ID in der DSP-Kampagne und ordnen Sie sie dann wie `d_creative=[Creative ID]` dem Merkmal zu.

![Bildschirm zur Eigenschaftenerstellung](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP-Makros](/help/dsp/campaign-management/macros.md)
>* [Übersicht über das Senden von DSP Media Exposure-Daten an Adobe Audience Manager](overview.md)
>* [Anwendungsfälle](use-cases.md)
