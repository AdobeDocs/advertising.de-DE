---
title: Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising
description: Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Werbetreibende mit der [!DNL Analytics for Advertising] <!-- (A4AdC) -->-Integration verfolgen bezahlte Werbung über Adobe Advertising und Adobe Analytics. Wenn Sie Medien, Kampagnen und Kanäle über mehrere Systeme verfolgen, stimmen dieselben Datensätze aus verschiedenen Systemen nur selten vollständig überein. In diesem Dokument wird erläutert, wie Sie Daten für Medien, die über Adobe Advertising nachverfolgt werden, mit Daten in den verschiedenen Systemen vergleichen sollten, in denen die Medien innerhalb von [!DNL Analytics] nachverfolgt werden.

>[!NOTE]
>
>Dieses Dokument konzentriert sich auf Adobe Advertising und Analytics, aber viele der Schlüsselpunkte sind auch auf andere Tracking-Lösungen übertragbar.

## Attributionsunterschiede in ähnlichen Berichten

### Potenziell verschiedene Lookback-Fenster und Attributionsmodelle

Die [!DNL Analytics for Advertising]-Integration verwendet zwei Variablen ([!DNL eVars] oder [!DNL rVars] \[reservierte [!DNL eVars]]\), um die [EF-ID und AMO-ID](ids.md) zu erfassen. Diese Variablen werden mit einem einzigen Lookback-Fenster (der Zeit, in der Clickthroughs und View-Throughs zugeordnet werden) und einem Attributionsmodell konfiguriert. Sofern nicht anders angegeben, sind die Variablen so konfiguriert, dass sie mit dem standardmäßigen Klick-Lookback-Fenster auf Advertiser-Ebene und dem Attributionsmodell in Adobe Advertising übereinstimmen.

Lookback-Fenster und Attributionsmodelle können jedoch sowohl in Analytics (über die [!DNL eVars]) als auch in Adobe Advertising konfiguriert werden. Darüber hinaus ist das Attributionsmodell in Adobe Advertising nicht nur auf Advertiser-Ebene (zur Angebotsoptimierung), sondern auch innerhalb einzelner Datenansichten und Berichte (nur zu Berichtszwecken) konfigurierbar. Beispielsweise kann ein Unternehmen es vorziehen, zur Optimierung das Attributionsmodell für die gleichmäßige Verteilung zu verwenden, aber für Berichte in Advertising DSP oder [!DNL Advertising Search, Social, & Commerce] die Attribution Letztkontakt . Durch das Ändern von Attributionsmodellen ändert sich die Anzahl der zugeordneten Konversionen.

Wenn ein Reporting-Lookback-Fenster oder ein Attributionsmodell in einem Produkt geändert wird und nicht im anderen, zeigen dieselben Berichte aus jedem System unterschiedliche Daten:

* **Beispiel für Diskrepanzen, die durch verschiedene Lookback-Fenster verursacht werden:**

  Angenommen, Adobe Advertising hat ein 60-tägiges Klick-Lookback-Fenster und [!DNL Analytics] ein 30-tägiges Lookback-Fenster. Angenommen, ein Benutzer kommt über eine Adobe Advertising-verfolgte Anzeige auf die Website, verlässt sie und kehrt dann an Tag 45 zurück und konvertiert. Adobe Advertising ordnet die Konversion dem ursprünglichen Besuch zu, da die Konversion innerhalb des 60-tägigen Lookback-Fensters stattgefunden hat. [!DNL Analytics] kann die Konversion jedoch nicht dem ersten Besuch zuordnen, da die Konversion nach Ablauf des 30-tägigen Lookback-Fensters stattgefunden hat. In diesem Beispiel meldet Adobe Advertising eine höhere Anzahl von Konvertierungen als [!DNL Analytics].

  ![Beispiel einer Konversion, die in Adobe Advertising, aber nicht [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png) zugeordnet wird

* **Beispiel für Diskrepanzen, die durch verschiedene Attributionsmodelle verursacht werden:**

  Angenommen, ein Benutzer interagiert vor der Konvertierung mit drei verschiedenen Adobe Advertising-Anzeigen, wobei Umsatz als Konversionstyp dient. Wenn ein Adobe Advertising-Bericht ein gleichmäßiges Verteilungsmodell für die Attribution verwendet, wird der Umsatz gleichmäßig auf alle Anzeigen verteilt. Wenn [!DNL Analytics] jedoch das Attributionsmodell Letztkontakt verwendet, ordnet sie den Umsatz der letzten Anzeige zu. Im folgenden Beispiel ordnet Adobe Advertising von den erfassten 30 USD Umsatz jeder der drei Anzeigen sogar 10 USD zu, während [!DNL Analytics] alle 30 USD Umsatz der letzten Anzeige zuordnet, die der Benutzer gesehen hat. Wenn Sie Berichte von Adobe Advertising und [!DNL Analytics] vergleichen, können Sie davon ausgehen, dass sich die unterschiedliche Attribution auf Sie auswirkt.

  ![Unterschiedlicher Umsatz, der Adobe Advertising und [!DNL Analytics] auf der Grundlage verschiedener Attributionsmodelle zugeordnet wird](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Es empfiehlt sich, dieselben Lookback-Fenster und Attributionsmodelle sowohl auf Adobe Advertising als auch auf [!DNL Analytics] zu verwenden. Arbeiten Sie nach Bedarf mit Ihrem Adobe-Account-Team zusammen, um die aktuellen Einstellungen zu ermitteln und die Konfigurationen synchron zu halten.

Dieselben Konzepte gelten für alle anderen Kanäle wie , die verschiedene Lookback-Fenster oder Attributionsmodelle verwenden.

#### Verschiedene Lookback-Fenster für View-Through-Tracking {#impression-lookback}

Beim Adobe Advertising basiert die Attribution auf Klicks und Impressionen, und Sie können verschiedene Lookback-Fenster für Klicks und für Impressionen konfigurieren. In [!DNL Analytics] basiert die Attribution jedoch auf Clickthroughs und View-Through-Ansichten, und Sie haben nicht die Möglichkeit, verschiedene Attributionsfenster für Clickthroughs und View-Through-Ansichten festzulegen. Das Tracking für jeden beginnt beim ersten Site-Besuch. Eine Impression kann am selben Tag oder mehrere Tage vor der Durchführung einer Datenansicht auftreten und der Zeitpunkt kann sich auf die Startposition des Attributionsfensters in jedem System auswirken.

In der Regel erfolgen die meisten View-Through-Konversionen schnell genug, damit beide Systeme Gutschriften zuweisen. Einige Konvertierungen können jedoch außerhalb des Adobe Advertising-Impression-Lookback-Fensters, aber innerhalb des [!DNL Analytics]-Lookback-Fensters auftreten. Solche Konvertierungen werden der Durchsicht in [!DNL Analytics], aber nicht der Impression in Adobe Advertising zugeschrieben.

Angenommen, im folgenden Beispiel wurde einem Besucher eine Anzeige an Tag 1 geschaltet, er hat am Tag 2 einen Durchsichtsbesuch durchgeführt (d. h. die Landingpage der Anzeige besucht, ohne zuvor auf die Anzeige geklickt zu haben) und am Tag 45 konvertiert. In diesem Fall würde Adobe Advertising den Benutzer von Tag 1 bis Tag 14 verfolgen (unter Verwendung eines 14-tägigen Lookbacks), [!DNL Analytics] würde den Benutzer von Tag 2 bis Tag 61 verfolgen (unter Verwendung eines 60-tägigen Lookbacks) und die Konversion an Tag 45 würde der Anzeige innerhalb von [!DNL Analytics], aber nicht innerhalb von Adobe Advertising zugeschrieben werden.

![Beispiel für eine Durchsichtskonvertierung, die in [!DNL Analytics], aber nicht in Adobe Advertising zugeordnet wird](/help/integrations/assets/a4adc-viewthrough-example.png)

Eine weitere Ursache für Diskrepanzen besteht darin, dass Sie bei Adobe Advertising Durchsichtskonversionen eine benutzerdefinierte *Durchsichtsgewichtung“ zuweisen können,* der Gewichtung entspricht, die einer Klick-basierten Konvertierung zugewiesen wurde. Die standardmäßige View-Through-Gewichtung beträgt 40 %, was bedeutet, dass eine View-Through-Konvertierung als 40 % des Werts einer Click-basierten Konvertierung gezählt wird. [!DNL Analytics] bietet keine solche Gewichtung von View-Through-Konversionen. So wird beispielsweise ein in [!DNL Analytics] erfasster Umsatzauftrag im Wert von 100 USD auf 40 USD in Adobe Advertising reduziert, wenn Sie das standardmäßige Durchsichtsgewicht verwenden - eine Differenz von 60 USD.

Beachten Sie diese Unterschiede beim Vergleich von View-Through-Konversionen zwischen Adobe Advertising- und [!DNL Analytics].

#### Verfügbare Attributionsmodelle

| Adobe Advertising Attribution | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] Zuordnung |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Verwenden Sie nicht* |
| [!UICONTROL Weight Last Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL J-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Inverse-J] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Custom] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Participation] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Algorithmic] | Nicht zutreffend |

>[!NOTE]
>
>Bei der linearen Zuordnung [!DNL Analytics] Erfolgsereignisse gleichmäßig auf alle [!DNL eVar] Werte innerhalb eines einzelnen Besuchs verteilt. Verwenden Sie daher die lineare Zuordnung mit einem [!DNL eVar] von „Besuch“. In der Werbung führt die Verwendung der linearen Attribution jedoch zu einer nicht wirklich linearen Zuordnung und zu weniger als idealen Berichten. Wenn ein Besucher beispielsweise mit drei Anzeigen interagiert, bevor er sie in drei separate Besuche konvertiert, wird nur die beim letzten Besuch angesehene Anzeige der Konversion zugeordnet und nicht alle drei Anzeigen.
>
>Außerdem wird durch den Wechsel der Konversionszuordnung zu oder von „Linear“ verhindert, dass historische Daten angezeigt werden, was in Berichten zu falsch angegebenen Daten führen kann. Beispielsweise kann bei der linearen Zuordnung der Umsatz auf eine Reihe verschiedener [!DNL eVar] aufgeteilt werden. Wenn Sie die Zuordnung auf „Zuletzt verwendet“ ändern, werden 100 % dieses Umsatzes mit dem neuesten Einzelwert verknüpft. Dieser Zusammenhang kann zu falschen Schlussfolgerungen führen.
>
>Um Verwirrung zu vermeiden, macht [!DNL Analytics] historische Daten in der Reporting-Oberfläche nicht verfügbar. Sie können die historischen Daten anzeigen, wenn Sie die [!DNL eVar] wieder auf die ursprüngliche Zuordnungseinstellung zurücksetzen. Sie sollten jedoch [!DNL eVar] Zuordnungseinstellungen nicht ändern, nur um auf historische Daten zuzugreifen. Adobe empfiehlt die Verwendung eines neuen [!DNL eVar], wenn Sie eine neue Zuordnungseinstellung für bereits aufgezeichnete Daten anwenden möchten, anstatt die Zuordnungseinstellungen für einen [!DNL eVar] zu ändern, der bereits über eine erhebliche Menge an historischen Daten verfügt.

Eine Liste [!DNL Analytics] Attributionsmodelle und ihrer Definitionen finden Sie unter [https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models).

Wenn Sie bei [!DNL Search, Social, & Commerce] angemeldet sind, finden Sie eine Liste

* (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alle anderen Benutzer) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Ereignisdatumsattribution in Adobe Advertising

Im Adobe Advertising können Sie Konversionsdaten entweder nach dem zugehörigen Klickdatum/Ereignisdatum (dem Datum des Klick- oder Impressionsereignisses) oder nach dem Transaktionsdatum (Konversionsdatum) melden. Das Konzept der Berichterstellung für Klick-/Ereignisdaten existiert nicht in [!DNL Analytics]. Alle in [!DNL Analytics] nachverfolgten Konversionen werden nach Transaktionsdatum gemeldet. Daher kann dieselbe Konversion mit unterschiedlichen Daten in Adobe Advertising und [!DNL Analytics] gemeldet werden. Angenommen, ein Benutzer klickt am 1. Januar auf eine Anzeige und konvertiert am 5. Januar. Wenn Sie die Konversionsdaten nach Ereignisdatum in Adobe Advertising anzeigen, wird die Konversion am 1. Januar gemeldet, als der Klick erfolgte. In [!DNL Analytics] wird dieselbe Konversion am 5. Januar gemeldet.

![Beispiel einer Konversion, die unterschiedlichen Daten zugeordnet wird](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] Reporting](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) ermöglicht die Konfiguration von Regeln zur Identifizierung verschiedener Marketing-Kanäle auf der Grundlage unterschiedlicher Aspekte von Trefferinformationen. Sie können von Adobe Advertising verfolgte Kanäle ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] und [!UICONTROL Paid Search]) nach [!DNL Marketing Channels] verfolgen, indem Sie den `ef_id` Abfragezeichenfolgenparameter verwenden, um den Kanal zu identifizieren. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> können die [!DNL Marketing Channels]-Berichte zwar Adobe Advertising-Kanäle verfolgen, die Daten stimmen jedoch aus verschiedenen Gründen möglicherweise nicht mit den Adobe Advertising-Berichten überein. Weitere Informationen finden Sie in den folgenden Abschnitten.

>[!NOTE]
>
> Die folgenden Kernkonzepte gelten auch für das Multi-Channel-Tracking, das Kampagnen beinhaltet, die nicht im Adobe Advertising verfolgt werden, wie die [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html)-Variable (auch als Dimension „Trackingcode“ oder &quot;[!DNL eVar] 0“ bezeichnet) und das benutzerdefinierte [!DNL eVar]-Tracking.

### Potenziell verschiedene Attributionsmodelle in [!DNL Marketing Channels]

Die meisten [!DNL Marketing Channels] Berichte sind mit [!UICONTROL Last Touch] Attribution konfiguriert, für die dem zuletzt erkannten Marketing-Kanal 100 % des Konversionswerts zugewiesen werden. Die Verwendung unterschiedlicher Attributionsmodelle für die [!DNL Marketing Channels] Berichte und das Adobe Advertising von Berichten führt zu Diskrepanzen bei den zugeordneten Konversionen.

### Ein potenziell anderes Lookback-Fenster in [!DNL Marketing Channels]

Das Lookback-Fenster für [!DNL Marketing Channels] kann angepasst werden. Beim Adobe Advertising ist das Click-Lookback-Fenster konfigurierbar, obwohl ein festes 60-Tage-Fenster üblich ist. Wenn die beiden Produkte unterschiedliche Lookback-Fenster verwenden, können Datendiskrepanzen auftreten.

### Attribution verschiedener Kanäle in [!DNL Marketing Channels]

Adobe Advertising-Berichte erfassen nur bezahlte Medien, die über Adobe Advertising gehandelt werden (Paid Search nach [!DNL Advertising Search, Social, & Commerce]-Anzeigen und Display für Advertising DSP-Anzeigen), während [!DNL Marketing Channels]-Berichte alle digitalen Kanäle verfolgen können. Dies kann zu einer Diskrepanz im Kanal führen, für den eine Konversion zugeordnet wird.

Paid Search- und natürliche Suchkanäle haben beispielsweise oft eine symbiotische Beziehung, bei der jeder Kanal dem anderen hilft. Der [!DNL Marketing Channels] Bericht ordnet einige Konversionen zu einer natürlichen Suche zu, die Adobe Advertising nicht nachverfolgt, da die natürliche Suche nicht verfolgt wird.

Denken Sie auch an einen Kunden, der eine Display-Anzeige anzeigt, auf eine Paid-Search-Anzeige klickt, auf eine E-Mail-Nachricht klickt und dann eine 30-USD-Bestellung aufgibt. Selbst wenn Adobe Advertising und [!DNL Marketing Channels] beide das Attributionsmodell Letztkontakt verwenden, wird die Konversion weiterhin jedem anders zugeordnet. Adobe Advertising hat keinen Zugriff auf den [!UICONTROL Email]-Kanal, sodass die Paid Search-Suche für die Konversion angerechnet wird. [!DNL Marketing Channels] hat jedoch Zugriff auf alle drei Kanäle, sodass es [!UICONTROL Email] für die Konversion gutschreiben würde.

![Beispiel für eine andere Konversionszuordnung beim Adobe Advertising im Vergleich zum [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Weitere Informationen dazu, warum die Metriken variieren können, finden Sie unter &quot;[Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;.

## Datenunterschiede in Adobe Analytics [!DNL Paid Search Detection]

Mit der [Legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html)-Funktion in [!DNL Analytics] können Unternehmen [Regeln für das Tracking von Paid Search und Organic Search Traffic definieren](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) für bestimmte Suchmaschinen definieren. Die [!DNL Paid Search Detection]-Regeln verwenden sowohl eine Abfragezeichenfolge als auch die verweisende Domain, um Paid-Search-Traffic und natürlichen Suchverkehr zu identifizieren. Die [!DNL Paid Search Detection] Berichte sind Teil der größeren Gruppe von [Suchmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) Berichten, die entweder ablaufen, wenn ein bestimmtes Ereignis (z. B. ein Warenkorb-Checkout) eintritt oder der Besuch endet.

Im Folgenden finden Sie die Benutzeroberfläche zum Erstellen eines [!DNL Paid Search Detection] Regelsatzes:

![Beispiel einer Regel zur Erkennung gebührenpflichtiger Suchvorgänge in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Die resultierenden [!DNL Paid Search Detection] umfassen die Berichte [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] und [!UICONTROL Natural Search Keywords].

Beachten Sie die folgenden beiden Einschränkungen bei Daten in [!DNL Paid Search Detection]:

* Die [!UICONTROL Paid Search Keywords]- und [!UICONTROL Natural Search Keywords] zeigen die Suchabfragen an, die anhand der verweisenden URLs identifiziert wurden, nicht die Keywords, nach denen die Benutzer Gebote abgeben. Adobe Advertising- und [!DNL Analytics]-Berichte zeigen die eigentlichen Keywords an. Erwarten Sie daher nicht, dass sie mit den [!DNL Paid Search Detection] Keyword-Berichten übereinstimmen.

* Als die [!DNL Paid Search Detection]-Funktion ursprünglich erstellt wurde, war die ursprüngliche Suchabfrage (die Zeichenfolge, die der Benutzer in die Suchleiste in der Suchmaschine eingegeben hat) für Werbetreibende über die verweisende URL leichter verfügbar. Suchmaschinen verschleiern die Suchabfrage heutzutage weitgehend, und die Berichte mit den [!DNL Paid Search Detection] Keywords sind von begrenztem Wert, da die meisten Abfragedaten unter „Unspecified“ fallen.

  Mit [!DNL Analytics for Advertising] können Werbetreibende weiterhin bezahlte Keywords in [!DNL Analytics] verfolgen. Die verweisende Domain informiert die Engine und meldet, welche Suchmaschine den Traffic verursacht hat. Da die Advertiser-spezifischen Kontoinformationen nicht an die verweisende Domain gebunden sind, wird der gesamte Traffic unter der Suchmaschine aufgelistet. Werbetreibende mit mehreren Konten in derselben Suchmaschine sollten für kontospezifische Berichte auf Adobe Advertising oder [!DNL Analytics] verweisen.

### Warum [!DNL Paid Search Detection] konfigurieren?

Die [!DNL Paid Search Detection] Berichte ermöglichen es Ihnen, den natürlichen Suchdatenverkehr in den [[!DNL Analytics Marketing Channels] Berichten](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) zu identifizieren. Die Trennung von Paid Search-Traffic und natürlichem Such-Traffic ist eine hervorragende Möglichkeit, den Wert zu verstehen, den die natürliche Suche dem gesamten Marketing-Ökosystem bringt.

## Clickthrough-Datenvalidierung für [!DNL Analytics for Advertising] {#data-validation}

Für Ihre Integration sollten Sie Ihre Clickthrough-Daten validieren, um sicherzustellen, dass alle Seiten auf Ihrer Site Clickthroughs ordnungsgemäß verfolgen.

[!DNL Analytics] besteht eine der einfachsten Möglichkeiten zur Validierung [!DNL Analytics for Advertising] Tracking darin, Instanzen mithilfe einer berechneten Metrik „AMO ID Instances to Clicks“ mit Klicks zu vergleichen, die wie folgt berechnet wird:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] gibt an, wie oft [AMO-IDs](ids.md) auf der Website verfolgt werden. Jedes Mal, wenn auf eine Anzeige geklickt wird, wird ein AMO-ID-Parameter (`s_kwcid`) zur Landingpage-URL hinzugefügt. Die Anzahl der [!UICONTROL AMO ID Instances] entspricht daher der Anzahl der Klicks und kann anhand der tatsächlichen Anzeigenklicks validiert werden. Normalerweise liegt die Übereinstimmungsrate für [!DNL Search, Social, & Commerce] bei 85 % und für [!DNL DSP] Traffic bei 30 % (wenn gefiltert, sodass nur Clickthrough-[!UICONTROL AMO ID Instances] enthalten sind). Der Unterschied in den Erwartungen zwischen Suche und Anzeige kann durch das erwartete Traffic-Verhalten erklärt werden. Die Suchabsicht wird erfasst, weshalb Benutzende in der Regel beabsichtigen, in ihrer Abfrage auf die Suchergebnisse zu klicken. Benutzer, die eine Anzeige- oder Online-Videoanzeige sehen, klicken jedoch eher unbeabsichtigt auf die Anzeige und springen dann entweder von der Site zurück oder brechen das neue Fenster ab, das geladen wird, bevor die Seitenaktivität verfolgt wird.

Beim Adobe Advertising von Berichten können Sie Instanzen auf ähnliche Weise mit Klicks vergleichen, indem Sie die Metrik &quot;[!UICONTROL EF ID Instances]&quot; anstelle von [!UICONTROL AMO ID Instances] verwenden:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Erwarten Sie zwar eine hohe Übereinstimmungsrate zwischen der AMO-ID und der EF-ID, erwarten Sie jedoch keine 100-prozentige Parität, da die AMO-ID und die EF-ID grundsätzlich unterschiedliche Daten verfolgen. Dieser Unterschied kann zu geringfügigen Unterschieden bei der [!UICONTROL AMO ID Instances] und den [!UICONTROL EF ID Instances] führen. Wenn die [!UICONTROL AMO ID Instances] in [!DNL Analytics] jedoch um mehr als 1 % von der [!UICONTROL EF ID Instances] in Adobe Advertising abweicht, wenden Sie sich an Ihr Adobe-Account-Team, um Hilfe zu erhalten.

Weitere Informationen zur AMO-ID und EF-ID finden Sie unter [Adobe Advertising-IDs, die von Analytics verwendet werden](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Fehlerbehebung bei Unterschieden zwischen Klicks und Instanzen

Wenn das [!UICONTROL EF ID Instances]-Klicks-Verhältnis unter 85 % liegt, überprüfen Sie Folgendes:

* Fehlt Klick-Tracking für das Konto oder auf einer beliebigen Unterebene, oder gibt es doppeltes Klick-Tracking (z. B. sowohl auf Konto- als auch auf Kampagnenebene)?

  Klicken Sie unter Suche, Social und Commerce [Bulksheet herunterladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) auf das -Konto, um die Tracking-URLs zu überprüfen.

  Außerdem können Sie in [!DNL Analytics] sehen, ob die AMO-ID und die EF-IF konsistent angehängt werden, indem Sie eine berechnete Metrik vom Typ &quot;[!DNL AMO ID] zu [!DNL EF ID]&quot; verwenden, die wie folgt berechnet wird:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Ein Wert über 100 % zeigt an, dass mehr EF-IDs fehlen als AMO-IDs.

* Weist die Landingpage ein Ladeproblem auf, sodass die AMO-ID und die EF-ID nicht erfasst werden?

* Wird die Landingpage-URL umgeleitet, sodass die AMO-ID und die EF-ID verloren gehen?

* Verwenden alle Landingpages die konfigurierte Report Suite?

>[!NOTE]
>
>Theoretisch ist es möglich, dass eine Instanz mehrere Klicks hat. Prüfen Sie, ob Klicks auf verschiedenen Geräten (wie Desktop, Mobilgerät und Tablet) auftreten.

## Vergleichen von Datensätzen in [!DNL Analytics for Advertising] mit Datensätzen in Adobe Advertising

Die [AMO ID](ids.md) (s_kwcid-Abfragezeichenfolgenparameter) wird für das Reporting in [!DNL Analytics] verwendet, und die [EF ID](ids.md) (ef_id-Abfragezeichenfolgenparameter) wird für das Reporting in Adobe Advertising verwendet. Da es sich um unterschiedliche Werte handelt, kann es sein, dass ein Wert beschädigt ist oder nicht zur Landingpage hinzugefügt wird.

Angenommen, wir haben die folgende Landingpage:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

wobei die EF-ID &quot;`test_ef_id`&quot; und die AMO-ID &quot;`test_amo_id`&quot; lautet.

Wenn eine Site-seitige Umleitung erfolgt, könnte die URL wie folgt aussehen:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

wobei die EF-ID &quot;`test_ef_id`&quot; und die AMO-ID &quot;`test_amo_id#redirectAnchorTag`&quot; lautet.

In diesem Beispiel fügt das Hinzufügen des Anker-Tags der AMO-ID unerwartete Zeichen hinzu, was zu einem Wert führt, den Analytics nicht erkennt. Diese AMO-ID wird nicht klassifiziert, und die damit verbundenen Konversionen fallen in [!DNL Analytics] Berichten unter &quot;[!UICONTROL unspecified]&quot; oder &quot;[!UICONTROL none]&quot;.

Während solche Probleme häufig auftreten, führen sie glücklicherweise nicht zu einem hohen Prozentsatz an Diskrepanzen. Wenn Sie jedoch eine große Diskrepanz zwischen AMO-IDs in [!DNL Analytics] und EF-IDs in Adobe Advertising feststellen, wenden Sie sich an Ihr Adobe-Account-Team, um Hilfe zu erhalten.

## Weitere Überlegungen zur Metrik

### Unterschied zwischen Klicks und Besuchen {#clicks-vs-visits}

Sie scheinen analog zu sein, aber Klicks und Besuche stellen unterschiedliche Daten dar:

* **Klick:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Besuch:** [!DNL Analytics] definiert [Besuch](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) als eine Reihe von Seitenansichten durch einen Benutzer, die nach einem von mehreren Kriterien enden, z. B. 30 Minuten Inaktivität.

Definitionsgemäß kann ein Klick zu mehreren Besuchen führen.

Betrachten Sie das folgende Beispiel: Benutzer 1 und Benutzer 2 greifen beide auf eine Website zu, indem sie auf eine Adobe Advertising-Anzeige klicken. Benutzer 1 zeigt vier Seiten an und geht dann zum Tag, sodass der erste Klick zu einem Besuch führt. Benutzer 2 zeigt zwei Seiten an, geht für ein 45-minütiges Mittagessen, kehrt zurück, zeigt zwei weitere Seiten an und geht dann. In diesem Fall führt der erste Klick zu zwei Besuchen.

![Beispiel für den Unterschied zwischen Klicks und Besuchen](/help/integrations/assets/a4adc-visits-example.png)

### Der Unterschied zwischen Klicks und Clickthroughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klicks und Clickthroughs sind zwei verschiedene Metriken:

* **Klick:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Clickthroughs:** [!DNL Analytics] zeichnet einen Clickthrough auf, wenn der Besucher auf der Ziel-Website landet, die Landingpage geladen wird und die [!DNL Analytics] am Ende der Seite die Daten an [!DNL Analytics] sendet.

Klicks und Clickthroughs können aufgrund von versehentlichen Anzeigenklicks stark voneinander abweichen. Wir haben festgestellt, dass die meisten Klicks auf Display-Anzeigen zufällige Klicks sind und diese zufälligen Besucher vor dem Laden der Landingpage auf die Schaltfläche „Zurück“ klicken, sodass [!DNL Analytics] keinen Clickthrough aufzeichnen können. Dies gilt insbesondere für Anzeigen, bei denen ein versehentliches Klicken wahrscheinlicher ist, z. B. Mobile-Anzeigen, Videoanzeigen und Anzeigen, die den Bildschirm füllen und geschlossen werden müssen, bevor der Benutzer die Seite anzeigen kann.

Bei Sites, die auf Mobilgeräten geladen werden, ist die Wahrscheinlichkeit von Clickthroughs aufgrund geringerer Bandbreiten oder verfügbarer Verarbeitungsleistung ebenfalls geringer, was dazu führt, dass die Ladezeit von Landingpages länger dauert. Nicht selten führen 50-70 % der Klicks nicht zu Clickthroughs. In mobilen Umgebungen kann der Unterschied bis zu 90 % betragen, da der Browser langsamer ist und die Wahrscheinlichkeit höher ist, dass der Benutzer versehentlich auf die Anzeige klickt, während er durch die Seite scrollt oder versucht, die Anzeige zu schließen.

Die Klickdaten können auch in Umgebungen aufgezeichnet werden, in denen Clickthroughs nicht mit den aktuellen Tracking-Mechanismen aufgezeichnet werden können (z. B. Klicks, die in eine oder von einer mobilen App gehen) oder für die der Advertiser nur einen Tracking-Ansatz bereitgestellt hat (z. B. mit dem View-Through-JavaScript-Ansatz Browser, die Drittanbieter-Cookies blockieren, Klicks, aber keine Clickthroughs). Ein Hauptgrund dafür, dass Adobe empfiehlt, sowohl die Tracking-Ansätze für Klick-URLs als auch die View-Through-Tracking-Ansätze für JavaScript bereitzustellen, ist die Maximierung der Abdeckung nachverfolgbarer Clickthroughs.

### Verwenden von Adobe Advertising-Traffic-Metriken für Nicht-Adobe Advertising-Dimensionen

Adobe Advertising bietet Analytics [werbespezifische Traffic-Metriken und die zugehörigen Dimensionen von  [!DNL DSP]  und  [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Die von Adobe Advertising bereitgestellten Metriken gelten nur für die angegebenen Adobe Advertising-Dimensionen, und Daten sind nicht für andere Dimensionen in [!DNL Analytics] verfügbar.

Wenn Sie beispielsweise die [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] Metriken nach Konto anzeigen, bei denen es sich um eine Adobe Advertising-Dimension handelt, werden die [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] nach Konto angezeigt.

![Beispiel für das Adobe Advertising von Metriken in einem Bericht mithilfe einer Adobe Advertising-Dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Wenn Sie die [!UICONTROL Adobe Advertising Clicks]- und [!UICONTROL Adobe Advertising Cost] jedoch nach einer On-Page-Dimension anzeigen (z. B. Page), für die Adobe Advertising keine Daten bereitstellt, sind [!UICONTROL Adobe Advertising Clicks] und [!UICONTROL Adobe Advertising Cost] für jede Seite null (0).

![Beispiel für das Adobe Advertising von Metriken in einem Bericht mit einer nicht unterstützten Dimension](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Verwenden von [!UICONTROL AMO ID Instances] als Ersatz für Klicks mit Nicht-Adobe Advertising-Dimensionen

Da Sie keine [!UICONTROL AMO Clicks] mit Vor-Ort-Dimensionen verwenden können, sollten Sie ein Äquivalent zu Klicks finden. Sie könnten versucht sein, Besuche als Ersatz zu verwenden, aber sie sind nicht die beste Option, da jeder Besucher mehrere Besuche haben kann. (Siehe &quot;[ Unterschied zwischen Klicks und Besuchen](#clicks-vs-visits).“ Stattdessen wird die Verwendung von [!UICONTROL AMO ID Instances] empfohlen, also wie oft die AMO-ID erfasst wird. Obwohl [!UICONTROL AMO ID Instances] nicht genau mit [!UICONTROL AMO Clicks] übereinstimmen, sind sie die beste Option zur Messung des Klick-Traffics auf der Website. Weitere Informationen finden Sie unter &quot;[Click-Through-Datenvalidierung für [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Beispiel für [!UICONTROL AMO ID Instances] anstelle von [!UICONTROL Adobe Advertising Clicks] für eine nicht unterstützte Dimension](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Warum können die Daten zwischen Adobe Advertising und  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
