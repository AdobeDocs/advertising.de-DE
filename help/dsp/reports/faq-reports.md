---
title: Häufig gestellte Fragen zu benutzerdefinierten Berichten
description: Erfahren Sie mehr über benutzerspezifische Berichte, einschließlich Haushaltsberichten und Konversionspfadanalyseberichten.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# Häufig gestellte Fragen zu benutzerdefinierten Berichten

## Haushaltsberichte

### Der [!UICONTROL Household Reach & Frequency]

#### Wie unterscheiden sich [!UICONTROL Household Reach & Frequency] Berichte von anderen benutzerdefinierten Berichten?

Der [!UICONTROL Household Reach & Frequency] Bericht misst Reichweite, Impression und Häufigkeit in verschiedenen Dimensionen auf Haushaltsebene basierend auf der IP-Adresse. Die anderen benutzerdefinierten Berichte werden auf Geräte- oder Cookie-Ebene generiert.

Selbst wenn beispielsweise eine Impression drei Geräten in einem Haushalt bereitgestellt wird, ist die Metrik Unique Household Reached eine solche.

##### Unterstützte Dimensionen

Der [!UICONTROL Household Reach & Frequency]-Bericht unterstützt die [folgenden Dimensionen](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign]&quot;, &quot;[!UICONTROL Package]&quot;, &quot;[!UICONTROL Placement]&quot;, &quot;[!UICONTROL Site/Apps]&quot; (das keinen Zugriff auf Überschneidungsmetriken bietet), &quot;[!UICONTROL Media Type]&quot;, &quot;[!UICONTROL Feed Type]&quot;, &quot;[!UICONTROL Device]&quot;, &quot;[!UICONTROL Publisher]&quot;, &quot;[!UICONTROL Audience]&quot;, &quot;[!UICONTROL Creative Length]&quot; und die von Benutzenden erstellte Platzierung &quot;[!UICONTROL Tags].“ |

##### Unterstützte Metriken

Zu [verfügbaren Metriken](/help/dsp/reports/report-columns.md) gehören:

* Überschneidungsmetriken: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] und [!UICONTROL Unique Household (Overlap)].

  Überschneidungsmetriken sind die Werte, die nur für die gemeldete Dimension oder Kombination von Dimensionen auftreten, nicht aber für andere Dimensionen. <!-- For example, it might show the ?? -->

* Metriken ohne Überschneidung: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] und [!UICONTROL Unique Household Reached]

Konversionsmetriken und benutzerdefinierte Ziele werden nicht unterstützt.

#### Was ist der Unterschied zwischen den Metriken Überschneidung und Nicht-Überschneidung?

Die folgende Abbildung zeigt drei Metriken (Eindeutiger Haushalt erreicht, Inkrementeller Haushalt erreicht und Inkrementeller Haushalt (Überschneidung)) für drei Kampagnen (A, B und C).

![Abbildung der Haushaltsüberschneidungsmetriken](/help/dsp/assets/household-overlap-metrics-illustration.png " Abbildung der Haushaltsüberschneidungsmetriken")

* Unique Household Reached (Total): Gibt den Unique Household an, der von jeder der Kampagnen erreicht wird, oder die Gesamtfläche jedes der Kreise. In der Abbildung: Einzelner Haushalt erreicht durch A = Inkrementeller Haushalt erreicht durch A + (A+B) + (A+C) + (A+B+C)

* Inkrementeller Haushalt erreicht ist der eindeutige Haushalt, der nur durch eine Kampagne erreicht wurde. In der Abbildung sind die inkrementellen Haushalte, die durch A, B, C erreicht werden, die inkrementellen Haushalte, die durch A, B bzw. C erreicht werden.

* Inkrementeller Haushalt (Überschneidung) ist der eindeutige Haushalt, der von der Kampagne oder einer Kombination von Kampagnen erreicht wird. In der Abbildung ist der inkrementelle Haushalt, der durch A erreicht wird, C gleich A+C.

#### Workflow

Führen Sie die üblichen Schritte aus, um [einen benutzerdefinierten Bericht zu erstellen](report-create.md).

Der [!UICONTROL Household Reach & Frequency] kann nur eine Dimension enthalten. Sie kann auch entweder a) Metriken mit Überschneidungen nach einer beliebigen Dimension außer Site/Apps oder b) Metriken ohne Überschneidungen, aber nicht beides enthalten.

#### Welche Einschränkungen hat der [!UICONTROL Household Reach & Frequency] Bericht?

Berichte mit Überschneidungsmetriken geben Schnittpunkte von bis zu drei Werten aus. Wenn Sie beispielsweise die Metrik [!UICONTROL Unique Household (Overlap)] für 10 Platzierungen verwenden, sehen Sie die eindeutigen Haushalte, die von einzelnen Platzierungen erreicht werden, die gemeinsamen Haushalte, die durch eine Kombination aus zwei beliebigen Platzierungen erreicht werden, und die gemeinsamen Haushalte, die durch Kombinationen aus drei beliebigen Platzierungen erreicht werden. Es sind keine gemeinsamen Haushalte zu sehen, die mit vier oder mehr Platzierungen erreicht werden.

Für andere Dimensionen als Kampagne, Paket oder Platzierung unterstützt der Bericht bis zu 10 Werte in jeder Dimension. Um beispielsweise einen [!UICONTROL Unique Household Reached] für die Dimension [!UICONTROL Audience] zu generieren, sollte die Anzahl der eindeutigen Zielgruppen kleiner oder gleich 10 sein. Wenn Sie mehr als 10 eindeutige Zielgruppen einbeziehen, wird ein leerer Bericht generiert.

#### Warum unterscheiden sich die Werte für Häufigkeit und eindeutige Reichweite zwischen meinen [!UICONTROL Custom]-Berichten und dem [!UICONTROL Household Reach & Frequency]-Bericht?

Diese Metriken in [!UICONTROL Household] Berichten werden anhand der tatsächlichen Anzahl von IP-Adressen berechnet, während die Metriken im [!UICONTROL Custom] Bericht geschätzte Zahlen verwenden, die mithilfe von Modellen berechnet wurden. Die Abweichung sollte jedoch weniger als 10 % betragen.

#### Wie konfiguriere ich den Bericht für die [!UICONTROL Placement Tags] Dimension?

Um Tags für die Platzierung zu erstellen, [öffnen Sie die Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-edit.md) und geben Sie Werte in das Feld [Platzierungs-Tags“ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md).

Wenn eine Platzierung mehrere Tags enthält, betrachtet der Bericht die gesamte Zeichenfolge als ein Tag. Der Bericht enthält eine Zeile für jede eindeutige Zeichenfolge.

### Der [!UICONTROL Household Conversions]

#### Welche Attributionsmethoden werden in [!UICONTROL Household Conversions] Bericht unterstützt?

Es werden zwei Arten von Attributionsmethoden unterstützt:

* [!UICONTROL Unique]: Zählt, wie oft ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Konversionspfad war.

* [!UICONTROL Multi-Touch Attribution (MTA)]: Verteilt die Gutschrift für jede Konversion auf der Grundlage der Häufigkeit des Auftretens des Dimensionswerts (z. B. eines Geräts oder einer Platzierung) auf dem Pfad zur Konversion. Wenn beispielsweise vor der Konversion insgesamt 10 Impressions vorhanden waren, davon 8 auf CTV und 2 auf Mobile, werden 80 % der Credits (0,8) auf CTV-Bildschirme und 0,2 auf Mobile übertragen.

#### Inwiefern unterscheidet sich das Reporting über Haushaltskonversionen vom CTV-View-Through-Reporting in Adobe Analytics?

* [!DNL Analytics] zeigt der [!DNL CTV View-Through Conversion] die Anzahl der Konversionen an, bei denen eine CTV-Impression der letzte Touchpoint vor der Konversion war. Im Gegensatz dazu zeigt der DSP [!UICONTROL Household Conversions]-Bericht die Anzahl der eindeutigen Haushalte an, die zu einem beliebigen Zeitpunkt innerhalb des definierten Lookback-Fensters vor der Konversion einem CTV-Impression ausgesetzt waren.

* [!DNL Analytics] weist die Attributionslogik Konversionen ausschließlich dem letzten Touchpoint aus Adobe Advertising zu. Im Gegensatz dazu unterstützt der DSP [!UICONTROL Household Conversions]-Bericht zusätzliche Attributionsmodelle, *[!UICONTROL Unique]* und *[!UICONTROL Multi-Touch Attribution (MTA)]*.

* [!DNL Analytics] Berichtsdaten sind besonders nützlich, um nach Marketing-Kanälen, Site-Interaktionsmetriken usw. zu analysieren. Der DSP-[!UICONTROL Household Conversions] bietet detailliertere Einblicke, da Konversionsdaten nach verschiedenen Dimensionen wie Medientyp und Publisher aufgeteilt werden können.

### [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] Berichte im Vergleich zu Daten aus [!DNL Advanced Measurement Services]

Für erweiterte Berichte zur häuslichen Reichweite und Häufigkeit von Konversionen kann das [[!DNL Strategic Advertising Consulting] Team](/help/dsp/introduction/advanced-measurement-services.md) hochgradig anpassbare Berichte zusammen mit ganzheitlichen strategischen Empfehlungen bereitstellen. Weitere Informationen zu [!DNL Advanced Measurement Services] erhalten Sie von Ihrem Adobe Account Team.

#### Warum sollte ich die Berichte [!DNL Advanced Measurement Services] und [!UICONTROL Household Reach & Frequency] verwenden, wenn ich [!UICONTROL Household Conversions] bereits verwende?

Die [!UICONTROL Household Reach & Frequency]- und [!UICONTROL Household Conversions] ermöglichen es Kunden, die Reichweite, Häufigkeit und Konversionsmetriken auf Haushaltsebene autonom in Echtzeit abzurufen.

#### Kann ich sowohl den [!UICONTROL Household Reach & Frequency]- als auch den [!UICONTROL Household Conversions]-Bericht und -[!DNL Advanced Measurement Services] verwenden?

Der ideale Anwendungsfall besteht darin, sowohl den [!UICONTROL Household] Bericht als auch die [!DNL Advanced Measurement Services] Reporting- und Beratungsdienste gemeinsam zu verwenden. Betrachten Sie den [!UICONTROL Household]-Bericht als transaktional, als Information für die tägliche Optimierung und [!DNL Advanced Measurement Services] als strategischer, als Information für ganzheitliche Erkenntnisse und Erkenntnisse im Zusammenhang mit übergeordneten Geschäftszielen.

## Konversionspfad-Analyseberichte

### Wie lässt sich der Konversionsbericht mit den Berichten vergleichen, die von [!DNL Advanced Measurement Services] und Adobe Analytics Analysis Workspace erstellt wurden?

| | Pfad zum Konversionsbericht | Advanced Measurement Services hat keine Auswirkungen auf das Suchberichterstellung | Berichte in Analysis Workspace |
| --- | --- | --- |---|
| Kundennutzen | Erstellen Sie einen benutzerdefinierten Self-Service-Bericht, um zu verstehen, welche Pfade der Anzeigen-Journey zu mehr Konversionen geführt haben, um die Optimierung zu optimieren | Den Einfluss der CTV-Taktik (Connected TV) auf Suchklicks verstehen | Machen Sie sich mit dem Einfluss Ihrer ganzheitlichen Adobe Advertising-Investition neben anderen Marketing-Kanälen auf Suchklicks vertraut |
| Haushaltsebene | Ja | Ja | Nein |
| Wird CTV unterstützt? | Ja | Ja | Ja |
| Attributionsmethode | Das Last-Touch-Ereignis (Impression oder Klick) muss sich im Lookbook-Fenster befinden. | Eindeutig | Letztkontakt |
| | Interaktionspunkte, die mehr als 30 Tage vor dem Letztkontakt-Ereignis liegen, werden für den Konversionspfad berücksichtigt. | (CTV erhält eine Gutschrift, unabhängig davon, wo die CTV-Exposition im Pfad des Benutzers auftritt) | (CTV wird angerechnet, wenn die Impression das letzte Ereignis im Lookback-Fenster ist UND es keinen gebührenpflichtigen Klick aus anderen Formaten vor oder nach der CTV-Exposition gibt) |
| Berichtsebene | körnig | körnig | umfassend |
| | (Kanaltyp, Creative/Anzeige, Keyword, Pfade, Länge, Zeit bis zur Konversion) | (CTV-Taktik, CTV-App/Publisher) | (Adobe Advertising und andere Marketing-Kanäle) |
| Marketing-Kanäle | DSP + Search (aus Search, Social und Commerce) | DSP + Search (aus Search, Social und Commerce) | Marketing-Kanäle, die nicht von der Adobe Advertising-Clickthrough-EF-ID verfolgt werden (z. B. organische Suche, organische soziale Medien, E-Mail und Tochterunternehmen) |
| Konversionsmetriken werden unterstützt | Mit dem Adobe Advertising-Ereignispixel (AMO-ID) und Adobe Analytics-Tracking verfolgte Metriken | Klicks (keine Konversionen) | Mit Adobe Analytics-Tracking verfolgte Metriken |

Weitere Informationen über den Halo-Effekt von Advanced Measurement Services für Suchberichte finden Sie unter [Advanced Measurement Services](/help/dsp/introduction/advanced-measurement-services.md).

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Erstellen eines benutzerdefinierten Berichts](/help/dsp/reports/report-create.md)
>* [Benutzerdefinierten Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
