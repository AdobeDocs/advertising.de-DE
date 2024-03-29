---
title: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising
description: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: fb0634643e40b67e50461823f976a93129e2f038
workflow-type: tm+mt
source-wordcount: '3217'
ht-degree: 0%

---

# Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising

*Advertiser mit nur Adobe Advertising-Adobe Analytics-Integration*

Werbetreibende mit [!DNL Analytics for Advertising] <!-- (A4AdC) --> Integration verfolgen bezahlte Werbung über Adobe Advertising und Adobe Analytics. Wenn Sie Medien, Kampagnen und Kanäle über mehrere Systeme verfolgen, stimmen nur selten dieselben Datensätze aus verschiedenen Systemen vollständig überein. In diesem Dokument wird erläutert, wie Sie erwarten sollten, dass Daten für Medien, die über Adobe Advertising gehandelt werden, mit Daten in den verschiedenen Systemen verglichen werden, in denen die Medien verfolgt werden [!DNL Analytics].

>[!NOTE]
>
>Dieses Dokument konzentriert sich auf Adobe Advertising und Analytics, aber viele der Schlüsselpunkte können auch auf andere Tracking-Lösungen übertragen werden.

## Unterschiede bei der Zuordnung in ähnlichen Berichten

### Potenziell unterschiedliche Lookback-Fenster und Attributionsmodelle

Die [!DNL Analytics for Advertising] -Integration verwendet zwei Variablen ([!DNL eVars] oder [!DNL rVars] \[reserviert [!DNL eVars]]\), um die [EF ID und AMO ID](ids.md). Diese Variablen werden mit einem einzelnen Lookback-Fenster (dem Zeitpunkt, innerhalb dessen Clickthroughs und Durchsichten zugeordnet werden) und einem Attributionsmodell konfiguriert. Sofern nicht anders angegeben, sind die Variablen so konfiguriert, dass sie mit dem standardmäßigen Klick-Lookback-Fenster auf Advertiser-Ebene und dem Attributionsmodell auf Adobe Advertising übereinstimmen.

Lookback-Fenster und Attributionsmodelle können jedoch in beiden Analytics konfiguriert werden (über die [!DNL eVars]) und in Adobe Advertising. Darüber hinaus ist das Attributionsmodell in Adobe Advertising nicht nur auf Advertiser-Ebene (zur Angebotsoptimierung), sondern auch innerhalb einzelner Datenansichten und Berichte konfigurierbar (nur zu Berichtszwecken). Eine Organisation könnte beispielsweise das Gleichheitsverteilungsattributionsmodell zur Optimierung verwenden, aber die Letztkontakt-Attribution für Berichte in Advertising DSP verwenden oder [!DNL Advertising Search, Social, & Commerce]. Wenn Sie Attributionsmodelle ändern, ändert sich die Anzahl der zugeordneten Konversionen.

Wenn ein Reporting-Lookback-Fenster oder Attributionsmodell in einem Produkt und nicht im anderen geändert wird, zeigen dieselben Berichte aus jedem System unterschiedliche Daten an:

* **Beispiel für Diskrepanzen, die durch verschiedene Lookback-Fenster verursacht werden:**

  Angenommen, Adobe Advertising verfügt über ein 60-tägiges Klick-Lookback-Fenster und [!DNL Analytics] verfügt über ein 30-Tage-Lookback-Fenster. Angenommen, ein Benutzer besucht die Site über eine von Adobe Advertising getrackte Anzeige, verlässt die Site und kehrt dann an Tag 45 zurück und konvertiert sie. Adobe Advertising ordnet die Konversion dem ersten Besuch zu, da die Konversion innerhalb des 60-Tage-Lookback-Fensters stattgefunden hat. [!DNL Analytics]kann die Konversion jedoch nicht dem ersten Besuch zuordnen, da die Konversion erfolgte, nachdem das 30-Tage-Lookback-Fenster abgelaufen war. In diesem Beispiel würde Adobe Advertising eine höhere Anzahl von Konversionen melden als [!DNL Analytics] würde.

  ![Beispiel einer Konvertierung, die in Adobe Advertising, aber nicht [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Beispiel für Diskrepanzen, die durch verschiedene Attributionsmodelle verursacht werden:**

  Angenommen, ein Benutzer interagiert mit drei verschiedenen Adobe Advertising-Anzeigen, bevor er konvertiert, wobei der Umsatz der Konversionstyp ist. Wenn ein Adobe Advertising-Bericht für die Attribution ein Gleichheitsverteilungsmodell verwendet, wird der Umsatz gleichmäßig über alle Anzeigen verteilt. Wenn [!DNL Analytics] verwendet jedoch das Attributionsmodell des letzten Kontakts, wird der Umsatz der letzten Anzeige zugeordnet. Im folgenden Beispiel ordnet Adobe Advertising jeder der drei Anzeigen einen Umsatz von 10 USD des erfassten Umsatzes zu, während [!DNL Analytics] ordnet der letzten vom Benutzer gesehenen Anzeige den Umsatz von 30 USD zu. Beim Vergleich von Berichten aus Adobe Advertising und [!DNL Analytics]können Sie erwarten, dass Sie die Auswirkungen der unterschiedlichen Attribution sehen.

  ![Verschiedene Adobe Advertising zurechenbare Einnahmen und [!DNL Analytics] basierend auf verschiedenen Attributionsmodellen](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Es empfiehlt sich, dieselben Lookback-Fenster und Attributionsmodelle sowohl in Adobe Advertising als auch in [!DNL Analytics]. Arbeiten Sie bei Bedarf mit Ihrem Adobe-Account-Team zusammen, um die aktuellen Einstellungen zu ermitteln und die Konfigurationen zu synchronisieren.

Diese Konzepte gelten für alle anderen Kanäle wie Kanäle, die unterschiedliche Lookback-Fenster oder Attributionsmodelle verwenden.

#### Verschiedene Lookback-Fenster für das Durchsichts-Tracking {#impression-lookback}

Unter Adobe Advertising basiert die Attribution auf Klicks und Impressionen und Sie können verschiedene Lookback-Fenster für Klicks und Impressionen konfigurieren. In [!DNL Analytics]Die Attribution basiert jedoch auf Clickthroughs und Durchsichten und Sie haben nicht die Möglichkeit, verschiedene Attributionsfenster für Clickthroughs und Durchsichten festzulegen. Die Verfolgung für jeden beginnt beim ersten Site-Besuch. Eine Impression kann am selben Tag oder mehreren Tagen vor dem Eintreten einer Durchsicht auftreten. Dies kann sich auf den Beginn des Attributionsfensters in den einzelnen Systemen auswirken.

In der Regel treten die meisten Durchsichtskonversionen schnell genug auf, sodass beide Systeme Gutschriften zuweisen. Einige Konversionen können jedoch außerhalb des Adobe Advertising Impression-Lookback-Fensters, aber innerhalb der [!DNL Analytics] Lookback-Fenster; solche Konversionen werden der Durchsicht in [!DNL Analytics] aber nicht für die Impression in Adobe Advertising.

Im folgenden Beispiel wird angenommen, dass einem Besucher an Tag 1 eine Anzeige bereitgestellt wurde, an Tag 2 einen Durchsichtsbesuch (d. h. einen Besuch der Landingpage der Anzeige, ohne zuvor auf die Anzeige zu klicken) durchgeführt und an Tag 45 konvertiert wurde. In diesem Fall verfolgt Adobe Advertising den Benutzer von den Tagen 1 bis 14 (mit einem 14-tägigen Lookback). [!DNL Analytics] den Benutzer von den Tagen 2 bis 61 (mit einem 60-tägigen Lookback) verfolgt und die Konversion an Tag 45 der Anzeige in [!DNL Analytics] aber nicht innerhalb von Adobe Advertising.

![Beispiel einer Durchsichtskonversion, die in [!DNL Analytics] aber nicht Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Eine weitere Ursache für Diskrepanzen besteht darin, dass Sie im Adobe Advertising Viewthrough-Konvertierungen eine benutzerdefinierte *Durchsichtsgewicht* , der relativ zur Gewichtung ist, die einer klickbasierten Konversion zugeordnet ist. Die standardmäßige Durchsichtsgewichtung beträgt 40 %, d. h. eine Durchsichtskonversion wird als 40 % des Werts einer klickbasierten Konversion gezählt. [!DNL Analytics] bietet keine solche Gewichtung von Durchsichtsumrechnungen. Beispielsweise eine Bestellung mit einem Umsatz von 100 USD in [!DNL Analytics] wird auf 40 USD an Adobe Advertising abgezinst, wenn Sie die standardmäßige Durchsichtsgewichtung verwenden - eine Differenz von 60 USD.

Berücksichtigen Sie diese Unterschiede beim Vergleich von Durchsichtskonversionen zwischen Adobe Advertising und [!DNL Analytics] Berichte.

#### Verfügbare Attributionsmodelle

| Adobe Advertising Attribution | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] Zuordnung |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Nicht verwenden* |
| [!UICONTROL Weight Last Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL J-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Inverse-J] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Custom] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Participation] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Algorithmic] | Nicht zutreffend |

>[!NOTE]
>
>für die lineare Zuordnung [!DNL Analytics] Erfolgsereignisse gleichmäßig über alle [!DNL eVar] -Werte innerhalb eines einzelnen Besuchs verwenden, verwenden Sie daher die lineare Zuordnung mit einer [!DNL eVar] Ablauf von &quot;Besuch&quot;. Für die Werbung führt die Verwendung der linearen Attribution jedoch zu einer Zuordnung, die nicht wirklich linear ist, und zu weniger als idealen Berichten. Wenn ein Besucher beispielsweise mit drei Anzeigen interagiert, bevor er in drei separate Besuche konvertiert, wird nur die beim letzten Besuch angezeigte Anzeige der Konversion und nicht allen drei Anzeigen zugeordnet.
>
>Darüber hinaus verhindert der Wechsel von &quot;Linear&quot;zur Umrechnungszuordnung die Anzeige von historischen Daten, was zu falsch angegebenen Daten in Berichten führen kann. Beispielsweise kann die lineare Zuordnung den Umsatz auf verschiedene [!DNL eVar] -Werte. Wenn Sie die Zuordnung zu &quot;Zuletzt verwendet&quot;ändern, werden 100 % dieses Umsatzes mit dem letzten Einzelwert verknüpft. Dieser Zusammenhang kann zu falschen Schlüssen führen.
>
>Um Verwirrung zu vermeiden, [!DNL Analytics] macht historische Daten in der Berichterstellungsoberfläche nicht verfügbar. Sie können die historischen Daten anzeigen, wenn Sie die [!DNL eVar] zurück zur ursprünglichen Zuordnungseinstellung, obwohl Sie nicht ändern sollten [!DNL eVar] Zuordnungseinstellungen, um einfach auf historische Daten zuzugreifen. Adobe empfiehlt die Verwendung eines neuen [!DNL eVar] wenn Sie eine neue Zuordnungseinstellung für bereits aufgezeichnete Daten anwenden möchten, anstatt die Zuordnungseinstellungen für [!DNL eVar] die bereits über eine beträchtliche Menge historischer Daten verfügen.

Liste mit [!DNL Analytics] Attributionsmodelle und ihre Definitionen unter [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Wenn Sie angemeldet sind [!DNL Search, Social, & Commerce]finden Sie eine Liste

* (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alle anderen Benutzer) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Ereignisdatumszuordnung in Adobe Advertising

Unter Adobe Advertising können Sie Konversionsdaten entweder nach dem zugehörigen Klickdatum/Ereignisdatum (dem Datum des Klick- oder Impressionsereignisses) oder nach dem Transaktionsdatum (Konversionsdatum) melden. Das Konzept der Berichterstellung für Klick-/Ereignisdaten existiert nicht in [!DNL Analytics]; alle in verfolgten Konversionen [!DNL Analytics] werden nach Transaktionsdatum gemeldet. Daher kann dieselbe Konversion mit unterschiedlichen Daten in Adobe Advertising und [!DNL Analytics]. Betrachten Sie beispielsweise einen Benutzer, der am 1. Januar auf eine Anzeige klickt und am 5. Januar konvertiert. Wenn Sie die Konversionsdaten nach Ereignisdatum in Adobe Advertising anzeigen, wird die Konversion am 1. Januar gemeldet, wenn der Klick stattgefunden hat. In [!DNL Analytics]wird dieselbe Konversion am 5. Januar gemeldet.

![Beispiel einer Konvertierung, die unterschiedlichen Datumsangaben zugeordnet wurde](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] Berichterstellung](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) ermöglicht es Ihnen, Regeln zu konfigurieren, um verschiedene Marketing-Kanäle basierend auf unterschiedlichen Aspekten der Trefferinformationen zu identifizieren. Sie können Adobe Advertising-getrackte Kanäle ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], und [!UICONTROL Paid Search]) als [!DNL Marketing Channels] durch Verwendung von `ef_id` Abfragezeichenfolgenparameter zur Identifizierung des Kanals. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Auch wenn die Variable [!DNL Marketing Channels] -Berichte Adobe Advertising-Kanäle verfolgen können, stimmen die Daten aus verschiedenen Gründen nicht mit den Adobe Advertising-Berichten überein. Weitere Informationen finden Sie in den folgenden Abschnitten.

>[!NOTE]
>
> Die folgenden Kernkonzepte gelten auch für jedes kanalübergreifende Tracking, das Kampagnen umfasst, die nicht im Adobe Advertising verfolgt werden, z. B. die [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (auch als Dimension &quot;Trackingcode&quot;oder &quot;Trackingcode&quot;bezeichnet)[!DNL eVar] 0&quot;) und benutzerdefiniert [!DNL eVar] Tracking.

### Potenziell unterschiedliche Attributionsmodelle in [!DNL Marketing Channels]

Am meisten [!DNL Marketing Channels] -Berichte mit [!UICONTROL Last Touch] Attribution, für die dem letzten erkannten Marketing-Kanal 100 % des Konversionswerts zugewiesen werden. Verwenden verschiedener Attributionsmodelle für die [!DNL Marketing Channels] Berichte und Adobe Advertising-Berichte führen zu Diskrepanzen bei den zugeordneten Konversionen.

### Ein potenziell unterschiedliches Lookback-Fenster in [!DNL Marketing Channels]

Das Lookback-Fenster für [!DNL Marketing Channels] kann angepasst werden. Unter Adobe Advertising ist das Klick-Lookback-Fenster konfigurierbar, obwohl es häufig ein festes 60-Tage-Fenster gibt. Wenn die beiden Produkte unterschiedliche Lookback-Fenster verwenden, können Sie Datendiskrepanzen erwarten.

### Verschiedene Kanalzuordnung in [!DNL Marketing Channels]

Adobe Advertising-Berichte erfassen nur Paid Media, die über Adobe Advertising weitergeleitet werden (gebührenpflichtige Suche nach [!DNL Advertising Search, Social, & Commerce] Anzeigen und Anzeigen für Advertising DSP Anzeigen), während [!DNL Marketing Channels] Berichte können alle digitalen Kanäle verfolgen. Dies kann zu einer Diskrepanz im Kanal führen, für den eine Konversion zugeordnet wird.

Beispielsweise haben Paid Search- und natürliche Suchkanäle oft eine symbiotische Beziehung, in der jeder Kanal den anderen unterstützt. Die [!DNL Marketing Channels] -Bericht weist einige Konversionen der natürlichen Suche zu, die von Adobe Advertising nicht verfolgt wird, da die natürliche Suche nicht verfolgt wird.

Betrachten wir auch einen Kunden, der eine Display-Anzeige anzeigt, auf eine Paid-Search-Anzeige klickt, in eine E-Mail-Nachricht klickt und dann eine Bestellung von 30 USD aufgibt. Auch wenn Adobe Advertising und [!DNL Marketing Channels] beide das Attributionsmodell des letzten Kontakts verwenden, wird die Konversion trotzdem unterschiedlich zugeordnet. Adobe Advertising hat keinen Zugriff auf die [!UICONTROL Email] -Kanal, sodass die gebührenpflichtige Suche für die Konversion angerechnet wird. [!DNL Marketing Channels]hat jedoch Zugriff auf alle drei Kanäle, sodass [!UICONTROL Email] für die Konvertierung.

![Beispiel für eine andere Konversionszuordnung in Adobe Advertising im Vergleich zu [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Weitere Informationen dazu, warum die Metriken variieren können, finden Sie unter[Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Datenunterschiede in Adobe Analytics [!DNL Paid Search Detection]

Die [veraltet [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) Funktion in [!DNL Analytics] ermöglicht es Unternehmen, [Definition von Regeln zur Verfolgung von Paid- und organischem Suchverkehr](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) für bestimmte Suchmaschinen. Die [!DNL Paid Search Detection] -Regeln verwenden sowohl eine Abfragezeichenfolge als auch die Referrer-Domäne, um den gebührenpflichtigen und kostenlosen Suchverkehr zu identifizieren. Die [!DNL Paid Search Detection] -Berichte sind Teil der größeren Gruppe von [Suchmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) Berichte, die ablaufen, wenn ein bestimmtes Ereignis (z. B. ein Warenkorb zur Kasse) eintritt oder der Besuch endet.

Im Folgenden finden Sie die Benutzeroberfläche zum Erstellen einer [!DNL Paid Search Detection] Regelsatz:

![Beispiel für eine Regel zur Erkennung von Paid Search, die in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Das Ergebnis [!DNL Paid Search Detection] -Berichte umfassen die [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], und [!UICONTROL Natural Search Keywords] Berichte.

Beachten Sie die beiden folgenden Einschränkungen bei Daten in [!DNL Paid Search Detection] Berichte:

* Die [!UICONTROL Paid Search Keywords] und [!UICONTROL Natural Search Keywords] Berichte zeigen die Suchabfragen an, die durch die verweisenden URLs identifiziert werden, nicht die Suchbegriffe, für die Benutzer Gebote abgeben. Adobe Advertising und [!DNL Analytics] Berichte zeigen die tatsächlichen Suchbegriffe an, erwarten Sie daher nicht, dass sie sich an der [!DNL Paid Search Detection] Suchbegriffberichte.

* Wenn die Variable [!DNL Paid Search Detection] -Funktion erstellt wurde, war die ursprüngliche Suchabfrage (die Zeichenfolge der Zeichen, die der Benutzer in die Suchleiste der Suchmaschine eingegeben hat) für Advertiser über die verweisende URL leichter verfügbar. Heute verschleiern Suchmaschinen die Suchabfrage und die [!DNL Paid Search Detection] Suchbegriffberichte sind von begrenztem Wert, da die meisten Abfragedaten unter &quot;Nicht angegeben&quot;fallen.

  Mit [!DNL Analytics for Advertising], können Advertiser weiterhin gebührenpflichtige Suchbegriffe in [!DNL Analytics]. Die verweisende Domäne informiert die Suchmaschine darüber, welche Suchmaschine den Traffic verursacht hat. Da die Advertiser-spezifischen Kontoinformationen nicht an die Referrer-Domäne gebunden sind, wird der gesamte Traffic unter der Suchmaschine aufgeführt. Werbetreibende mit mehreren Konten in derselben Suchmaschine sollten auf Adobe Advertising oder [!DNL Analytics] Berichterstellung für kontospezifische Berichte.

### Warum konfigurieren [!DNL Paid Search Detection]?

Die [!DNL Paid Search Detection] Berichte ermöglichen es Ihnen, den natürlichen Suchverkehr in der [[!DNL Analytics Marketing Channels] Berichte](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Die Trennung von Paid Search-Traffic und kostenlosem Suchverkehr ist eine hervorragende Möglichkeit, den Wert zu verstehen, den die natürliche Suche für das gesamte Marketing-Ökosystem bringt.

## Validierung von Clickthrough-Daten für [!DNL Analytics for Advertising] {#data-validation}

Für Ihre Integration sollten Sie Ihre Clickthrough-Daten validieren, um sicherzustellen, dass alle Seiten auf Ihrer Site Clickthroughs ordnungsgemäß verfolgen.

In [!DNL Analytics], eine der einfachsten Methoden zur Validierung von [!DNL Analytics for Advertising] Tracking ist der Vergleich von Klicks mit Instanzen mithilfe eines &quot;Klicks zu [!UICONTROL AMO ID Instances]&quot;berechnete Metrik, die wie folgt berechnet wird:

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] die Anzahl der [AMO-IDs](ids.md) werden auf der Site verfolgt. Jedes Mal, wenn auf eine Anzeige geklickt wird, wird eine AMO-ID (`s_kwcid`) wird der Landingpage-URL hinzugefügt. Die Anzahl [!UICONTROL AMO ID Instances]entspricht daher der Anzahl der Klicks und kann anhand der tatsächlichen Anzeigenklicks überprüft werden. Normalerweise wird eine Übereinstimmungsrate von 80 % für [!DNL Search, Social, & Commerce] und eine Übereinstimmungsrate von 30 % für [!DNL DSP] Traffic (wenn gefiltert, um nur Clickthrough einzuschließen) [!UICONTROL AMO ID Instances]). Der Unterschied in den Erwartungen zwischen Suche und Anzeige lässt sich durch das erwartete Traffic-Verhalten erklären. Die Suche erfasst die Absicht, und daher möchten Benutzer in der Regel auf die Suchergebnisse aus ihrer Abfrage klicken. Benutzer, die eine Anzeige oder Online-Videoanzeige sehen, klicken mit höherer Wahrscheinlichkeit unbeabsichtigt auf die Anzeige und springen dann entweder von der Site aus oder verlassen das neue Fenster, das geladen wird, bevor die Seitenaktivität verfolgt wird.

In Adobe Advertising-Berichten können Sie Klicks auf ähnliche Weise mit Instanzen vergleichen, indem Sie die[!UICONTROL ef_id_instances]&quot; metric anstelle von [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Obwohl Sie eine hohe Übereinstimmungsrate zwischen der AMO-ID und der EF-ID erwarten sollten, erwarten Sie keine 100-%-Parität, da AMO-ID und EF-ID verschiedene Daten grundsätzlich verfolgen. Dieser Unterschied kann zu leichten Unterschieden in der Gesamtsumme führen [!UICONTROL AMO ID Instances] und [!UICONTROL EF ID Instances]. Wenn die Summe [!UICONTROL AMO ID Instances] in [!DNL Analytics] unterscheidet sich von [!UICONTROL EF ID Instances] in Adobe Advertising um mehr als 1%, wenden Sie sich jedoch an Ihr Adobe-Account-Team, um Hilfe zu erhalten.

Weitere Informationen zur AMO-ID und zur EF ID finden Sie unter [Von Analytics verwendete Adobe Advertising-IDs](ids.md).

Im Folgenden finden Sie ein Beispiel für einen Arbeitsbereich zum Verfolgen von Klicks zu Instanzen.

![Beispiel eines Arbeitsbereichs zum Verfolgen von Klicks zu Instanzen](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Vergleichen von Datensätzen in [!DNL Analytics for Advertising] Versus in Adobe Advertising

Die [AMO-ID](ids.md) (s_kwcid-Abfragezeichenfolgenparameter) wird für die Berichterstellung in [!DNL Analytics]und die [EF ID](ids.md) wird für die Berichterstellung in Adobe Advertising verwendet. Da es sich um unterschiedliche Werte handelt, kann ein Wert beschädigt oder nicht zur Landingpage hinzugefügt werden.

Angenommen, wir haben die folgende Landingpage:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

wobei die EF-ID &quot;`test_ef_id`&quot; und die AMO-ID lautet &quot;.`test_amo_id`.&quot;

Wenn eine Site-seitige Umleitung erfolgt, könnte die URL wie folgt enden:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

wobei die EF-ID &quot;`test_ef_id`&quot; und die AMO-ID lautet &quot;.`test_amo_id#redirectAnchorTag`.&quot;

In diesem Beispiel fügt das Hinzufügen des Anker-Tags der AMO-ID unerwartete Zeichen hinzu, was zu einem Wert führt, den Analytics nicht erkennt. Diese AMO-ID würde nicht klassifiziert und die mit ihr verknüpften Konversionen würden unter &quot;[!UICONTROL unspecified]&quot; oder &quot;[!UICONTROL none]&quot;in [!DNL Analytics] Berichte.

Glücklicherweise sind Probleme wie dieses häufig, führen aber normalerweise nicht zu einem hohen Prozentsatz an Diskrepanzen. Wenn Sie jedoch eine große Diskrepanz zwischen AMO-IDs in [!DNL Analytics] und EF-IDs in Adobe Advertising, wenden Sie sich für Hilfe an Ihr Adobe-Account-Team.

## Andere Metrikaspekte

### Unterschied zwischen Klicks und Besuchen {#clicks-vs-visits}

Sie scheinen identisch zu sein, Klicks und Besuche stellen jedoch unterschiedliche Daten dar:

* **Klicken Sie auf:** [!DNL DSP] oder die Suchmaschine erfasst einen Klick, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Besuch:** [!DNL Analytics] definiert eine [Besuch](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) als eine Reihe von Seitenansichten durch einen Benutzer, die gemäß einem von mehreren Kriterien enden, z. B. 30 Minuten Inaktivität.

Ein Klick kann definitionsgemäß zu mehreren Besuchen führen.

Betrachten Sie das folgende Beispiel: Benutzer 1 und Benutzer 2 greifen beide durch Klicken auf eine Adobe Advertising-Anzeige auf eine Site zu. Benutzer 1 zeigt vier Seiten an und verlässt den Tag, sodass der erste Klick zu einem Besuch führt. Benutzer 2 zeigt zwei Seiten an, verlässt das Mittagessen 45 Minuten, gibt zwei weitere Seiten zurück, zeigt zwei weitere Seiten an und verlässt es dann. In diesem Fall führt der erste Klick zu zwei Besuchen.

![Beispiel für den Unterschied zwischen Klicks und Besuchen](/help/integrations/assets/a4adc-visits-example.png)

### Unterschied zwischen Klicks und Clickthroughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klicks und Clickthroughs sind zwei verschiedene Metriken:

* **Klicken Sie auf:** [!DNL DSP] oder die Suchmaschine erfasst einen Klick, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Clickthroughs:** [!DNL Analytics] erfasst einen Clickthrough, wenn der Besucher auf die Ziel-Website gelangt, die Landingpage geladen wird und die [!DNL Analytics] -Anfrage am Ende der Seite sendet die Daten an [!DNL Analytics].

Klicks und Clickthroughs können aufgrund versehentlicher Anzeigenklicks stark voneinander abweichen. Wir haben festgestellt, dass es sich bei den meisten Klicks auf Display-Anzeigen um versehentliche Klicks handelt, und dass diese versehentlichen Besucher vor dem Laden der Landingpage auf die Zurück-Schaltfläche klicken. [!DNL Analytics] Clickthrough kann nicht aufgezeichnet werden. Dies gilt insbesondere für Anzeigen, bei denen ein versehentlicher Klick wahrscheinlicher ist, wie mobile Anzeigen, Videoanzeigen und Anzeigen, die den Bildschirm ausfüllen und geschlossen werden müssen, bevor der Benutzer die Seite anzeigen kann.

Auf Mobilgeräten geladene Sites führen aufgrund niedrigerer Bandbreiten oder verfügbarer Verarbeitungsleistung auch weniger zu Clickthroughs, sodass das Laden von Landingpages länger dauert. Es ist nicht ungewöhnlich, dass 50-70 % der Klicks zu keinen Clickthroughs führen. In mobilen Umgebungen kann der Unterschied bis zu 90 % betragen, da die Kombination aus einem langsameren Browser und der höheren Wahrscheinlichkeit besteht, dass der Benutzer versehentlich auf die Anzeige klickt, während er durch die Seite scrollt oder versucht, die Anzeige zu schließen.

Die Klickdaten können auch in Umgebungen aufgezeichnet werden, in denen Clickthroughs nicht mit den aktuellen Tracking-Mechanismen aufgezeichnet werden können (z. B. Klicks in oder von einer mobilen App) oder bei denen der Advertiser nur einen Tracking-Ansatz implementiert hat (z. B. beim JavaScript-Ansichtsansatz verfolgen Browser, die Drittanbieter-Cookies blockieren, Klicks, jedoch keine Clickthroughs). Ein wichtiger Grund, warum Adobe empfiehlt, sowohl die Klick-URL-Tracking- als auch die Durchsichts-JavaScript-Tracking-Ansätze bereitzustellen, besteht darin, die Abdeckung verfolgbarer Clickthroughs zu maximieren.

### Verwenden von Adobe Advertising-Traffic-Metriken für Dimensionen ohne Adobe Advertising

Adobe Advertising bietet Analytics mit [werbespezifische Traffic-Metriken und die zugehörigen Dimensionen aus [!DNL DSP] und [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Die von der Adobe Advertising bereitgestellten Metriken gelten nur für die angegebenen Adobe Advertising-Dimensionen, und die Daten sind nicht für andere Dimensionen in [!DNL Analytics].

Wenn Sie beispielsweise die [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] Metriken nach Konto, bei dem es sich um eine Adobe Advertising-Dimension handelt, sehen Sie die Gesamtsumme [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] nach Konto.

![Adobe Advertising-Metriken in einem Bericht mit einer Adobe Advertising-Dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Wenn Sie jedoch die [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] Metriken nach einer On-Page-Dimension (z. B. Seite), für die Adobe Advertising keine Daten bereitstellt, dann wird die [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] für jede Seite ist null (0).

![Adobe Advertising-Metriken in einem Bericht mit einer nicht unterstützten Dimension](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Verwenden [!UICONTROL AMO ID Instances] als Ersatz für Klicks mit Nicht-Adobe Advertising-Dimensionen

Da Sie nicht [!UICONTROL AMO Clicks] mit On-site-Dimensionen verwenden, sollten Sie ein Äquivalent zu Klicks finden. Sie sind möglicherweise versucht, Besuche als Ersatz zu verwenden, doch sind sie nicht die beste Option, da jeder Besucher mehrere Besuche haben kann. (Siehe[Unterschied zwischen Klicks und Besuchen](#clicks-vs-visits).&quot; Stattdessen wird empfohlen, [!UICONTROL AMO ID Instances]: Häufigkeit, mit der die AMO-ID erfasst wird. while [!UICONTROL AMO ID Instances] will not match [!UICONTROL AMO Clicks] genau sind sie die beste Option zur Messung des Klickverkehrs auf der Site. Weitere Informationen finden Sie unter &quot;[Validierung von Clickthrough-Daten für [!DNL Analytics for Advertising]](#data-validation).&quot;

![Beispiel für [!UICONTROL AMO ID Instances] anstelle von [!UICONTROL Adobe Advertising Clicks] für eine nicht unterstützte Dimension](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising von Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Warum können Daten zwischen Adobe Advertising und variieren [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
