---
title: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising
description: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Advertiser mit der Integration [!DNL Analytics for Advertising] <!-- (A4AdC) --> verfolgen bezahlte Werbung über Adobe Advertising und Adobe Analytics. Wenn Sie Medien, Kampagnen und Kanäle über mehrere Systeme verfolgen, stimmen nur selten dieselben Datensätze aus verschiedenen Systemen vollständig überein. In diesem Dokument wird erläutert, wie Sie erwarten sollten, dass Daten für Medien, die über Adobe Advertising gehandelt werden, mit Daten in den verschiedenen Systemen verglichen werden, in denen die Medien innerhalb von [!DNL Analytics] verfolgt werden.

>[!NOTE]
>
>Dieses Dokument konzentriert sich auf Adobe Advertising und Analytics, aber viele der Schlüsselpunkte können auch auf andere Tracking-Lösungen übertragen werden.

## Unterschiede bei der Zuordnung in ähnlichen Berichten

### Potenziell unterschiedliche Lookback-Fenster und Attributionsmodelle

Die Integration von [!DNL Analytics for Advertising] verwendet zwei Variablen ([!DNL eVars] oder [!DNL rVars] \[reserviert [!DNL eVars]]\), um die [EF ID und AMO ID](ids.md) zu erfassen. Diese Variablen werden mit einem einzelnen Lookback-Fenster (dem Zeitpunkt, innerhalb dessen Clickthroughs und Durchsichten zugeordnet werden) und einem Attributionsmodell konfiguriert. Sofern nicht anders angegeben, sind die Variablen so konfiguriert, dass sie mit dem standardmäßigen Klick-Lookback-Fenster auf Advertiser-Ebene und dem Attributionsmodell auf Adobe Advertising übereinstimmen.

Lookback-Fenster und Attributionsmodelle können jedoch sowohl in Analytics (über den [!DNL eVars]) als auch in Adobe Advertising konfiguriert werden. Darüber hinaus ist das Attributionsmodell in Adobe Advertising nicht nur auf Advertiser-Ebene (zur Angebotsoptimierung), sondern auch innerhalb einzelner Datenansichten und Berichte konfigurierbar (nur zu Berichtszwecken). Ein Unternehmen kann beispielsweise das Gleichheitsverteilungsattributionsmodell zur Optimierung verwenden, aber die Letztkontakt-Attribution für Berichte in Advertising DSP oder [!DNL Advertising Search, Social, & Commerce] verwenden. Wenn Sie Attributionsmodelle ändern, ändert sich die Anzahl der zugeordneten Konversionen.

Wenn ein Reporting-Lookback-Fenster oder Attributionsmodell in einem Produkt und nicht im anderen geändert wird, zeigen dieselben Berichte aus jedem System unterschiedliche Daten an:

* **Beispiel für Diskrepanzen, die durch verschiedene Lookback-Fenster verursacht werden:**

  Angenommen, Adobe Advertising verfügt über ein 60-tägiges Klick-Lookback-Fenster und [!DNL Analytics] über ein 30-tägiges Lookback-Fenster. Angenommen, ein Benutzer besucht die Site über eine von Adobe Advertising getrackte Anzeige, verlässt die Site und kehrt dann an Tag 45 zurück und konvertiert sie. Adobe Advertising ordnet die Konversion dem ersten Besuch zu, da die Konversion innerhalb des 60-Tage-Lookback-Fensters stattgefunden hat. [!DNL Analytics] kann die Konversion jedoch nicht dem ersten Besuch zuordnen, da die Konversion nach Ablauf des 30-Tage-Lookback-Fensters erfolgte. In diesem Beispiel meldet Adobe Advertising eine höhere Anzahl von Konversionen als [!DNL Analytics].

  ![Beispiel einer Konvertierung, die in Adobe Advertising, aber nicht in [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Beispiel für Diskrepanzen, die durch verschiedene Attributionsmodelle verursacht werden:**

  Angenommen, ein Benutzer interagiert mit drei verschiedenen Adobe Advertising-Anzeigen, bevor er konvertiert, wobei der Umsatz der Konversionstyp ist. Wenn ein Adobe Advertising-Bericht für die Attribution ein Gleichheitsverteilungsmodell verwendet, wird der Umsatz gleichmäßig über alle Anzeigen verteilt. Wenn [!DNL Analytics] jedoch das Attributionsmodell des letzten Kontakts verwendet, ordnet es den Umsatz der letzten Anzeige zu. Im folgenden Beispiel ordnet Adobe Advertising jeder der drei Anzeigen einen Umsatz von 10 USD des Umsatzes von 30 USD zu, während [!DNL Analytics] alle 30 USD des Umsatzes der letzten Anzeige zuordnet, die der Benutzer gesehen hat. Wenn Sie Berichte aus Adobe Advertising und [!DNL Analytics] vergleichen, können Sie die Auswirkungen der unterschiedlichen Attribution erwarten.

  ![Verschiedener Umsatz, der Adobe Advertising und [!DNL Analytics] basierend auf verschiedenen Attributionsmodellen zugeordnet wurden](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Es empfiehlt sich, dieselben Lookback-Fenster und Attributionsmodelle sowohl in Adobe Advertising als auch in [!DNL Analytics] zu verwenden. Arbeiten Sie bei Bedarf mit Ihrem Adobe-Account-Team zusammen, um die aktuellen Einstellungen zu ermitteln und die Konfigurationen zu synchronisieren.

Diese Konzepte gelten für alle anderen Kanäle wie Kanäle, die unterschiedliche Lookback-Fenster oder Attributionsmodelle verwenden.

#### Verschiedene Lookback-Fenster für das Durchsichts-Tracking {#impression-lookback}

Unter Adobe Advertising basiert die Attribution auf Klicks und Impressionen und Sie können verschiedene Lookback-Fenster für Klicks und Impressionen konfigurieren. In [!DNL Analytics] basiert die Attribution jedoch auf Clickthroughs und Durchsichten und Sie haben nicht die Möglichkeit, verschiedene Attributionsfenster für Clickthroughs und Durchsichten festzulegen. Die Verfolgung für jeden beginnt beim ersten Site-Besuch. Eine Impression kann am selben Tag oder mehreren Tagen vor dem Durchsicht auftreten. Außerdem kann sich die Zeit auf den Start des Attributionsfensters in den einzelnen Systemen auswirken.

In der Regel treten die meisten Durchsichtskonversionen schnell genug auf, sodass beide Systeme Gutschriften zuweisen. Einige Konversionen können jedoch außerhalb des Adobe Advertising-Impression-Lookback-Fensters, aber innerhalb des [!DNL Analytics]-Lookback-Fensters auftreten. Solche Konversionen werden der Durchsicht in [!DNL Analytics] zugeordnet, nicht jedoch der Impression in Adobe Advertising.

Im folgenden Beispiel nehmen wir an, dass einem Besucher an Tag 1 eine Anzeige gezeigt wurde, an Tag 2 einen Durchsichtsbesuch durchgeführt hat (d. h. die Landingpage der Anzeige besucht hat, ohne zuvor auf die Anzeige geklickt zu haben) und an Tag 45 konvertiert wurde. In diesem Fall verfolgt Adobe Advertising den Benutzer von den Tagen 1 bis 14 (mit einem 14-tägigen Lookback), [!DNL Analytics] verfolgt den Benutzer von den Tagen 2 bis 61 (mit einem 60-tägigen Lookback) und die Konversion an Tag 45 wird der Anzeige innerhalb von [!DNL Analytics], jedoch nicht innerhalb von Adobe Advertising zugeordnet.

![Beispiel einer Durchsichtskonversion, die in [!DNL Analytics], aber nicht in Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png) zugeordnet ist

Eine weitere Ursache für Diskrepanzen ist, dass Sie in Adobe Advertising Viewthrough-Konvertierungen eine benutzerdefinierte *Durchsichtsgewichtung* zuweisen können, die relativ zur Gewichtung ist, die einer klickbasierten Konvertierung zugeordnet ist. Die standardmäßige Durchsichtsgewichtung beträgt 40 %, d. h. eine Durchsichtskonversion wird als 40 % des Werts einer klickbasierten Konversion gezählt. [!DNL Analytics] bietet keine solche Gewichtung von Durchsichtskonversionen. So wird z. B. eine in [!DNL Analytics] erfasste Bestellung von 100 USD auf 40 USD in der Adobe Advertising abgezinst, wenn Sie die standardmäßige Durchsichtsgewichtung verwenden - eine Differenz von 60 USD.

Berücksichtigen Sie diese Unterschiede beim Vergleich von Durchsichtskonversionen zwischen Adobe Advertising- und [!DNL Analytics] -Berichten.

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
>Bei der linearen Zuordnung ordnet [!DNL Analytics] Erfolgsereignisse gleichmäßig allen [!DNL eVar] -Werten innerhalb eines einzelnen Besuchs zu. Verwenden Sie daher die lineare Zuordnung mit dem Ablauf [!DNL eVar] von &quot;Besuch&quot;. Für die Werbung führt die Verwendung der linearen Attribution jedoch zu einer Zuordnung, die nicht wirklich linear ist, und zu weniger als idealen Berichten. Wenn ein Besucher beispielsweise mit drei Anzeigen interagiert, bevor er in drei separate Besuche konvertiert, wird nur die beim letzten Besuch angezeigte Anzeige der Konversion und nicht allen drei Anzeigen zugeordnet.
>
>Darüber hinaus verhindert der Wechsel von &quot;Linear&quot;zur Umrechnungszuordnung die Anzeige von historischen Daten, was zu falsch angegebenen Daten in Berichten führen kann. Beispielsweise kann die lineare Zuordnung den Umsatz auf eine Reihe verschiedener [!DNL eVar] -Werte aufteilen. Wenn Sie die Zuordnung zu &quot;Zuletzt verwendet&quot;ändern, werden 100 % dieses Umsatzes mit dem letzten Einzelwert verknüpft. Dieser Zusammenhang kann zu falschen Schlüssen führen.
>
>Um Verwirrung zu vermeiden, macht [!DNL Analytics] historische Daten in der Berichterstellungsoberfläche nicht verfügbar. Sie können die historischen Daten anzeigen, wenn Sie die Einstellung &quot;[!DNL eVar]&quot;zurück zur ursprünglichen Zuordnungseinstellung ändern. Sie sollten jedoch die Zuordnungseinstellungen für [!DNL eVar] nicht ändern, nur um auf historische Daten zuzugreifen. Adobe empfiehlt die Verwendung eines neuen [!DNL eVar] -Zeichens, wenn Sie eine neue Zuordnungseinstellung für bereits aufgezeichnete Daten anwenden möchten, anstatt die Zuordnungseinstellungen für einen [!DNL eVar] zu ändern, der bereits über eine beträchtliche Menge historischer Daten verfügt.

Eine Liste der [!DNL Analytics]-Attributionsmodelle und ihrer Definitionen finden Sie unter [https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models).

Wenn Sie bei [!DNL Search, Social, & Commerce] angemeldet sind, können Sie eine Liste finden

* (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alle anderen Benutzer) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Ereignisdatumszuordnung in Adobe Advertising

Unter Adobe Advertising können Sie Konversionsdaten entweder nach dem zugehörigen Klickdatum/Ereignisdatum (dem Datum des Klick- oder Impressionsereignisses) oder nach dem Transaktionsdatum (Konversionsdatum) melden. Das Konzept der Berichterstellung für Klickdaten/Ereignisdaten existiert nicht in [!DNL Analytics]. Alle in [!DNL Analytics] verfolgten Konversionen werden nach Transaktionsdatum gemeldet. Daher kann dieselbe Konversion mit unterschiedlichen Daten in Adobe Advertising und [!DNL Analytics] gemeldet werden. Betrachten Sie beispielsweise einen Benutzer, der am 1. Januar auf eine Anzeige klickt und am 5. Januar konvertiert. Wenn Sie die Konversionsdaten nach Ereignisdatum in Adobe Advertising anzeigen, wird die Konversion am 1. Januar gemeldet, als der Klick erfolgte. In [!DNL Analytics] wird dieselbe Konversion am 5. Januar gemeldet.

![Beispiel einer Konvertierung, die unterschiedlichen Datumsangaben zugeordnet wurde](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

Mit [[!DNL Analytics Marketing Channels] reporting](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) können Sie Regeln konfigurieren, um verschiedene Marketing-Kanäle basierend auf unterschiedlichen Aspekten der Trefferinformationen zu identifizieren. Sie können Adobe Advertising-verfolgte Kanäle ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] und [!UICONTROL Paid Search]) als [!DNL Marketing Channels] verfolgen, indem Sie den Abfragezeichenfolgenparameter `ef_id` verwenden, um den Kanal zu identifizieren. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Obwohl die [!DNL Marketing Channels] -Berichte Adobe Advertising-Kanäle verfolgen können, stimmen die Daten aus verschiedenen Gründen nicht mit den Adobe Advertising-Berichten überein. Weitere Informationen finden Sie in den folgenden Abschnitten.

>[!NOTE]
>
> Die folgenden Kernkonzepte gelten auch für jedes kanalübergreifende Tracking, das Kampagnen umfasst, die nicht im Adobe Advertising verfolgt werden, z. B. die Variable [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (auch als Dimension &quot;Trackingcode&quot;oder &quot;[!DNL eVar] 0&quot;bezeichnet) und das benutzerdefinierte Tracking mit [!DNL eVar].

### Potenziell unterschiedliche Attributionsmodelle in [!DNL Marketing Channels]

Die meisten [!DNL Marketing Channels] -Berichte werden mit der [!UICONTROL Last Touch] -Attribution konfiguriert, für die dem letzten erkannten Marketing-Kanal 100 % des Konversionswerts zugewiesen werden. Die Verwendung verschiedener Attributionsmodelle für die Berichte [!DNL Marketing Channels] und Adobe Advertising führt zu Diskrepanzen bei den zugeordneten Konversionen.

### Ein potenziell unterschiedliches Lookback-Fenster in [!DNL Marketing Channels]

Das Lookback-Fenster für [!DNL Marketing Channels] kann angepasst werden. Unter Adobe Advertising ist das Klick-Lookback-Fenster konfigurierbar, obwohl es häufig ein festes 60-Tage-Fenster gibt. Wenn die beiden Produkte unterschiedliche Lookback-Fenster verwenden, können Sie Datendiskrepanzen erwarten.

### Verschiedene Kanalzuordnung in [!DNL Marketing Channels]

Adobe Advertising-Berichte erfassen nur gebührenpflichtige Medien, die über Adobe Advertising weitergeleitet werden (gebührenpflichtige Suche nach [!DNL Advertising Search, Social, & Commerce] Anzeigen und Anzeige für Advertising DSP-Anzeigen), während [!DNL Marketing Channels] -Berichte alle digitalen Kanäle verfolgen können. Dies kann zu einer Diskrepanz im Kanal führen, für den eine Konversion zugeordnet wird.

Beispielsweise haben Paid Search- und natürliche Suchkanäle oft eine symbiotische Beziehung, in der jeder Kanal den anderen unterstützt. Der Bericht [!DNL Marketing Channels] weist einige Konversionen der kostenlosen Suche zu, die von Adobe Advertising nicht verfolgt wird, da die kostenlose Suche nicht verfolgt wird.

Betrachten wir auch einen Kunden, der eine Display-Anzeige anzeigt, auf eine Paid-Search-Anzeige klickt, in eine E-Mail-Nachricht klickt und dann eine Bestellung von 30 USD aufgibt. Selbst wenn Adobe Advertising und [!DNL Marketing Channels] beide das Attributionsmodell des letzten Kontakts verwenden, wird die Konversion trotzdem den beiden unterschiedlich zugeordnet. Adobe Advertising hat keinen Zugriff auf den Kanal [!UICONTROL Email], daher würde die gebührenpflichtige Suche für die Konversion angerechnet. [!DNL Marketing Channels] hat jedoch Zugriff auf alle drei Kanäle, sodass [!UICONTROL Email] für die Konversion gutgeschrieben wird.

![Beispiel für eine andere Konversionszuordnung in Adobe Advertising im Vergleich zu [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Weitere Informationen dazu, warum die Metriken variieren können, finden Sie unter &quot;[Warum Kanaldaten zwischen Adobe Advertising und  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) variieren können&quot;.

## Datenunterschiede in Adobe Analytics [!DNL Paid Search Detection]

Mit der Funktion [Legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) in [!DNL Analytics] können Unternehmen [ Regeln definieren, um gebührenpflichtigen und kostenlosen Suchverkehr zu verfolgen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html). Die [!DNL Paid Search Detection] -Regeln verwenden sowohl eine Abfragezeichenfolge als auch die Referrer-Domäne, um den Paid-Search-Traffic und den kostenlosen Suchverkehr zu identifizieren. Die [!DNL Paid Search Detection] -Berichte sind Teil der größeren Gruppe von [Suchmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) -Berichten, die entweder ablaufen, wenn ein bestimmtes Ereignis (z. B. ein Warenkorb zur Kasse) eintritt oder der Besuch endet.

Im Folgenden finden Sie die Benutzeroberfläche zum Erstellen eines [!DNL Paid Search Detection] -Regelsatzes:

![Beispiel einer in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png) festgelegten Regel zur Erkennung gebührenpflichtiger Suchvorgänge

Die resultierenden [!DNL Paid Search Detection] Berichte enthalten die Berichte [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] und [!UICONTROL Natural Search Keywords].

Beachten Sie die folgenden beiden Einschränkungen bei Daten in [!DNL Paid Search Detection] -Berichten:

* Die Berichte [!UICONTROL Paid Search Keywords] und [!UICONTROL Natural Search Keywords] zeigen die Suchabfragen an, die durch die verweisenden URLs identifiziert werden, nicht die Suchbegriffe, für die Benutzer Gebote abgeben. Adobe Advertising- und [!DNL Analytics]-Berichte zeigen die eigentlichen Suchbegriffe an. Daher erwarten Sie nicht, dass sie sich an den Berichten zu den Suchbegriffen [!DNL Paid Search Detection] ausrichten.

* Bei der ursprünglichen Erstellung der Funktion [!DNL Paid Search Detection] war die ursprüngliche Suchabfrage (die Zeichenfolge der Zeichen, die der Benutzer in der Suchleiste der Suchmaschine eingegeben hat) für Advertiser über die verweisende URL leichter verfügbar. Heute verschleiern Suchmaschinen die Suchabfrage weitgehend, und die [!DNL Paid Search Detection]-Suchbegriffberichte sind von begrenztem Wert, da die meisten Abfragedaten unter &quot;Nicht angegeben&quot;fallen.

  Mit [!DNL Analytics for Advertising] können Advertiser weiterhin gebührenpflichtige Suchbegriffe in [!DNL Analytics] nachverfolgen. Die verweisende Domäne informiert die Suchmaschine darüber, welche Suchmaschine den Traffic verursacht hat. Da die Advertiser-spezifischen Kontoinformationen nicht an die Referrer-Domäne gebunden sind, wird der gesamte Traffic unter der Suchmaschine aufgeführt. Werbetreibende mit mehreren Konten in derselben Suchmaschine sollten für kontospezifische Berichte auf Adobe Advertising oder [!DNL Analytics] Berichterstellung verweisen.

### Warum konfigurieren Sie [!DNL Paid Search Detection]?

Die [!DNL Paid Search Detection] -Berichte ermöglichen es Ihnen, den natürlichen Suchtraffic in den [[!DNL Analytics Marketing Channels] Berichten](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) zu identifizieren. Die Trennung von Paid Search-Traffic und kostenlosem Suchverkehr ist eine hervorragende Möglichkeit, den Wert zu verstehen, den die natürliche Suche für das gesamte Marketing-Ökosystem bringt.

## Validierung von Clickthrough-Daten für [!DNL Analytics for Advertising] {#data-validation}

Für Ihre Integration sollten Sie Ihre Clickthrough-Daten validieren, um sicherzustellen, dass alle Seiten auf Ihrer Site Clickthroughs ordnungsgemäß verfolgen.

In [!DNL Analytics] ist es am einfachsten, das [!DNL Analytics for Advertising]-Tracking zu validieren, Instanzen mit Klicks zu vergleichen, indem eine berechnete Metrik &quot;AMO-ID-Instanzen mit Klicks&quot;verwendet wird, die wie folgt berechnet wird:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] gibt an, wie oft [AMO-IDs](ids.md) auf der Site verfolgt werden. Jedes Mal, wenn auf eine Anzeige geklickt wird, wird der URL der Landingpage ein AMO-ID-Parameter (`s_kwcid`) hinzugefügt. Die Anzahl von [!UICONTROL AMO ID Instances] entspricht daher der Anzahl der Klicks und kann anhand der tatsächlichen Anzeigenklicks überprüft werden. In der Regel wird eine Übereinstimmungsrate von 85 % für [!DNL Search, Social, & Commerce] und eine Übereinstimmungsrate von 30 % für [!DNL DSP] Traffic angezeigt (wenn gefiltert, um nur Clickthrough-Rate für [!UICONTROL AMO ID Instances] einzuschließen). Der Unterschied in den Erwartungen zwischen Suche und Anzeige lässt sich durch das erwartete Traffic-Verhalten erklären. Die Suche erfasst die Absicht, und daher möchten Benutzer in der Regel auf die Suchergebnisse aus ihrer Abfrage klicken. Benutzer, die eine Anzeige oder Online-Videoanzeige sehen, klicken mit höherer Wahrscheinlichkeit unbeabsichtigt auf die Anzeige und springen dann entweder von der Site aus oder verlassen das neue Fenster, das geladen wird, bevor die Seitenaktivität verfolgt wird.

In Adobe Advertising-Berichten können Sie Instanzen auf ähnliche Weise mit Klicks vergleichen, indem Sie die Metrik &quot;[!UICONTROL EF ID Instances]&quot; anstelle von [!UICONTROL AMO ID Instances] verwenden:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Obwohl Sie eine hohe Übereinstimmungsrate zwischen der AMO-ID und der EF-ID erwarten sollten, sollten Sie nicht mit einer 100-%-Parität rechnen, da AMO-ID und EF-ID verschiedene Daten grundsätzlich verfolgen. Dieser Unterschied kann zu leichten Unterschieden bei den Gesamtwerten [!UICONTROL AMO ID Instances] und [!UICONTROL EF ID Instances] führen. Wenn sich die Gesamtsumme von [!UICONTROL AMO ID Instances] in [!DNL Analytics] um mehr als 1% von [!UICONTROL EF ID Instances] in Adobe Advertising unterscheidet, wenden Sie sich für Hilfe an Ihr Adobe-Account-Team.

Weitere Informationen zur AMO-ID und zur EF ID finden Sie unter [Von Analytics verwendete Adobe Advertising-IDs](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Beheben von Unterschieden zwischen Klicks und Instanzen

Wenn das Verhältnis zwischen [!UICONTROL EF ID Instances] und Klicks unter 85 % liegt, überprüfen Sie Folgendes:

* Vermissen Sie das Klick-Tracking für das Konto oder auf einer beliebigen Unterebene oder haben Sie doppeltes Klick-Tracking (z. B. auf Konto- und Kampagnenebene)?

  Laden Sie in Search, Social und Commerce [ein Bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) für das Konto herunter, um die Tracking-URLs zu überprüfen.

  In [!DNL Analytics] können Sie außerdem feststellen, ob die AMO-ID und die EF IF konsistent mit einer berechneten Metrik &quot;[!DNL AMO ID] to [!DNL EF ID]&quot; angehängt werden, die wie folgt berechnet wird:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Ein Wert größer als 100 % zeigt an, dass mehr EF-IDs als AMO-IDs fehlen.

* Verfügt die Landingpage über ein Ladeproblem, sodass die AMO-ID und die EF-ID nicht erfasst werden?

* Wird die Landingpage-URL so umgeleitet, dass die AMO-ID und die EF-ID verloren gehen?

* Verwenden alle Landingpages die konfigurierte Report Suite?

>[!NOTE]
>
>Theoretisch ist es möglich, dass eine Instanz mehrere Klicks hat. Stellen Sie sicher, dass Sie auf verschiedenen Geräten (z. B. Desktop, Mobilgerät und Tablet) nach Klicks suchen.

## Vergleichen von Datensätzen in [!DNL Analytics for Advertising] mit Adobe Advertising

Die [AMO-ID](ids.md) (Abfragezeichenfolgenparameter s_kwcid) wird für die Berichterstellung in [!DNL Analytics] verwendet, und die [EF ID](ids.md) (Abfragezeichenfolgenparameter ef_id) wird für die Berichterstellung in Adobe Advertising verwendet. Da es sich um unterschiedliche Werte handelt, kann ein Wert beschädigt oder nicht zur Landingpage hinzugefügt werden.

Angenommen, wir haben die folgende Landingpage:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

wobei die EF-ID &quot;`test_ef_id`&quot;und die AMO-ID &quot;`test_amo_id`&quot;lautet.

Wenn eine Site-seitige Umleitung erfolgt, könnte die URL wie folgt enden:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

wobei die EF-ID &quot;`test_ef_id`&quot;und die AMO-ID &quot;`test_amo_id#redirectAnchorTag`&quot;lautet.

In diesem Beispiel fügt das Hinzufügen des Anker-Tags der AMO-ID unerwartete Zeichen hinzu, was zu einem Wert führt, den Analytics nicht erkennt. Diese AMO-ID würde nicht klassifiziert und die mit ihr verknüpften Konversionen fielen in [!DNL Analytics] -Berichten unter &quot;[!UICONTROL unspecified]&quot;oder &quot;[!UICONTROL none]&quot;.

Glücklicherweise sind Probleme wie dieses häufig, führen aber normalerweise nicht zu einem hohen Prozentsatz an Diskrepanzen. Wenn Sie jedoch eine große Diskrepanz zwischen AMO-IDs in [!DNL Analytics] und EF-IDs in Adobe Advertising feststellen, wenden Sie sich an Ihr Adobe-Account-Team, um Hilfe zu erhalten.

## Andere Metrikaspekte

### Unterschied zwischen Klicks und Besuchen {#clicks-vs-visits}

Sie scheinen identisch zu sein, Klicks und Besuche stellen jedoch unterschiedliche Daten dar:

* **Klick:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Besuch:** [!DNL Analytics] definiert einen [Besuch](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) als eine Reihe von Seitenansichten eines Benutzers, die anhand eines von mehreren Kriterien enden, z. B. einer 30-minütigen Inaktivität.

Ein Klick kann definitionsgemäß zu mehreren Besuchen führen.

Betrachten Sie das folgende Beispiel: Benutzer 1 und Benutzer 2 greifen beide durch Klicken auf eine Adobe Advertising-Anzeige auf eine Site zu. Benutzer 1 zeigt vier Seiten an und verlässt den Tag, sodass der erste Klick zu einem Besuch führt. Benutzer 2 zeigt zwei Seiten an, verlässt das Mittagessen 45 Minuten, gibt zwei weitere Seiten zurück, zeigt zwei weitere Seiten an und verlässt es dann. In diesem Fall führt der erste Klick zu zwei Besuchen.

![Beispiel des Unterschieds zwischen Klicks und Besuchen](/help/integrations/assets/a4adc-visits-example.png)

### Unterschied zwischen Klicks und Clickthroughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klicks und Clickthroughs sind zwei verschiedene Metriken:

* **Klick:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Clickthroughs:** [!DNL Analytics] zeichnet einen Clickthrough auf, wenn der Besucher auf die Ziel-Website gelangt, die Landingpage geladen und die [!DNL Analytics] -Anfrage am unteren Rand der Seite die Daten an [!DNL Analytics] sendet.

Klicks und Clickthroughs können aufgrund versehentlicher Anzeigenklicks stark voneinander abweichen. Wir haben festgestellt, dass es sich bei den meisten Klicks auf Display-Anzeigen um versehentliche Klicks handelt und dass diese versehentlichen Besucher vor dem Laden der Landingpage auf die Schaltfläche &quot;Zurück&quot;klicken, sodass [!DNL Analytics] keine Clickthroughs aufzeichnen kann. Dies gilt insbesondere für Anzeigen, bei denen ein versehentlicher Klick wahrscheinlicher ist, wie mobile Anzeigen, Videoanzeigen und Anzeigen, die den Bildschirm ausfüllen und geschlossen werden müssen, bevor der Benutzer die Seite anzeigen kann.

Auf Mobilgeräten geladene Sites führen aufgrund niedrigerer Bandbreiten oder verfügbarer Verarbeitungsleistung auch weniger zu Clickthroughs, sodass das Laden von Landingpages länger dauert. Es ist nicht ungewöhnlich, dass 50-70 % der Klicks zu keinen Clickthroughs führen. In mobilen Umgebungen kann der Unterschied bis zu 90 % betragen, da die Kombination aus einem langsameren Browser und der höheren Wahrscheinlichkeit besteht, dass der Benutzer versehentlich auf die Anzeige klickt, während er durch die Seite scrollt oder versucht, die Anzeige zu schließen.

Die Klickdaten können auch in Umgebungen aufgezeichnet werden, in denen Clickthroughs nicht mit den aktuellen Tracking-Mechanismen aufgezeichnet werden können (z. B. Klicks in oder von einer mobilen App) oder bei denen der Advertiser nur einen Tracking-Ansatz implementiert hat (z. B. beim Viewthrough-JavaScript-Ansatz verfolgen Browser, die Drittanbieter-Cookies blockieren, Klicks, jedoch keine Clickthroughs). Ein Hauptgrund, warum Adobe empfiehlt, sowohl die Klick-URL-Tracking- als auch die Viewthrough-JavaScript-Tracking-Ansätze bereitzustellen, besteht darin, die Abdeckung verfolgbarer Clickthroughs zu maximieren.

### Verwenden von Adobe Advertising-Traffic-Metriken für Dimensionen ohne Adobe Advertising

Adobe Advertising stellt Analytics [werbespezifische Traffic-Metriken und die zugehörigen Dimensionen von  [!DNL DSP] und  [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md) zur Verfügung. Die von der Adobe Advertising bereitgestellten Metriken gelten nur für die angegebenen Adobe Advertising-Dimensionen und die Daten sind nicht für andere Dimensionen in [!DNL Analytics] verfügbar.

Wenn Sie beispielsweise die Metriken [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] nach Konto anzeigen, die eine Adobe Advertising-Dimension sind, werden die Gesamtwerte [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] nach Konto angezeigt.

![Beispiel für Adobe Advertising-Metriken in einem Bericht mit einer Adobe Advertising-Dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Wenn Sie jedoch die Metriken [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] nach einer On-Page-Dimension (z. B. Seite) anzeigen, für die Adobe Advertising keine Daten bereitstellt, sind die Metriken [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] für jede Seite null (0).

![Beispiel für Adobe Advertising-Metriken in einem Bericht mit einer nicht unterstützten Dimension](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Verwenden von [!UICONTROL AMO ID Instances] als Ersatz für Klicks ohne Adobe Advertising-Dimensionen

Da Sie [!UICONTROL AMO Clicks] nicht mit On-site-Dimensionen verwenden können, sollten Sie ein Äquivalent zu Klicks finden. Sie sind möglicherweise versucht, Besuche als Ersatz zu verwenden, doch sind sie nicht die beste Option, da jeder Besucher mehrere Besuche haben kann. (Siehe &quot;[Unterschied zwischen Klicks und Besuchen](#clicks-vs-visits)&quot;.) Stattdessen empfehlen wir die Verwendung von &quot;[!UICONTROL AMO ID Instances]&quot;, d. h. die Häufigkeit, mit der die AMO-ID erfasst wird. Auch wenn [!UICONTROL AMO ID Instances] nicht genau mit [!UICONTROL AMO Clicks] übereinstimmt, sind sie die beste Option zur Messung des Klickverkehrs auf der Site. Weitere Informationen finden Sie unter &quot;[Clickthrough-Datenvalidierung für [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Beispiel von [!UICONTROL AMO ID Instances] anstelle von [!UICONTROL Adobe Advertising Clicks] für eine nicht unterstützte Dimension](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Warum Daten zwischen Adobe Advertising und  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) variieren können
