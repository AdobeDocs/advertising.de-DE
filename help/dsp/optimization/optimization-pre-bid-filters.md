---
title: Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung
description: Verweisen Sie auf die verfügbaren Filter auf Platzierungsebene vor dem Angebot und sehen Sie, wie sie verwendet werden.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung

| Vorab-Angebotsfilter | Beschreibung | Verwendung dieses Filters |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Legt einen minimalen Prognoseschwellenwert für die Wahrscheinlichkeit fest, dass eine Auktion zu einem Clickthrough führen kann. Wenn Sie beispielsweise den Schwellenwert auf 0,1 % setzen, bieten Sie bei Auktionen nur Angebote, bei denen die prognostizierte Wahrscheinlichkeit eines Klicks größer oder gleich 0,1 % ist.<br><br><b>Hinweis:</b> Filter werden vor Optimierungszielen angewendet. Daher können sehr strenge Filter Ausgaben verhindern. | Verwenden Sie diese Option, wenn Sie ein KPI-Mindestziel für die Clickthrough-Rate (CTR) haben und Ihr Budget nicht ausgeben möchten, wenn die CTR unter dem Schwellenwert liegt. Dieser Filter kann sehr restriktiv sein, daher ist es wichtig, realistische Ziele festzulegen. Je nach anderen Einschränkungen der Platzierung ist ein Ziel von 0,03-0,07 % im Allgemeinen ein guter Ausgangspunkt. Sie können dies bei Bedarf auf Site-Ebene optimieren, um die Metriken zu verbessern.<br><br>Wenn Ihr Ziel darin besteht, eine minimale CTR und den bestmöglichen CPM zu erreichen, wird empfohlen, einen [!UICONTROL Click Through Rate] -Filter mit dem Optimierungsziel &quot;[!UICONTROL Lowest CPM]&quot;zu kombinieren. Wenn Ihr Ziel ein maximaler CPM ohne echten Nutzen für eine Übererfüllung und eine minimale CTR ist, kann es angemessener sein, einen [!UICONTROL Click Through Rate] -Filter mit dem Optimierungsziel &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; zu koppeln. |
| [!UICONTROL 100% Completion Rate] | Legt eine erforderliche minimale Abschlussrate fest, die erfüllt sein muss, bevor Sie ein Angebot für eine Impression abgeben. | Verwenden Sie diesen Filter, wenn das Hauptziel der Kampagne die Abschlussraten sind. Faktor in anderen Targeting-Parametern, aber 65% ist der empfohlene Anfangsprozentsatz. |
| [!UICONTROL Player Size - Adobe] | Legt eine erforderliche minimale Player-Größe mithilfe von Daten aus DSP fest. Sie können ein Angebot für eine Impression abgeben, wenn der Schwellenwert [!UICONTROL Player Size] erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie mit Daten aus DSP ein Inventar für den vollständigen Episode-Player bereitstellen. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Legt eine erforderliche minimale Player-Größe mithilfe von Daten aus [!DNL Moat] oder [!DNL Integral Ad Science] ([!DNL IAS]) fest. Sie können ein Angebot für eine Impression abgeben, wenn der Schwellenwert [!UICONTROL Player Size] erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie mit plattformweiten [!DNL Moat] - oder [!DNL IAS] -Daten ein Inventar für den vollständigen Episode-Player bereitstellen.<br><br><b>Hinweis:</b> Verwenden Sie diesen Filter nur, wenn die Kampagne für die Verwendung von [!DNL Moat] - oder [!DNL IAS] -Daten konfiguriert ist. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Legt einen erforderlichen Mindestprozentsatz für die Sichtbarkeit mithilfe DSP Sichtbarkeitszahlen und Messungen fest. Sie können ein Angebot für eine Impression erstellen, wenn der angegebene Schwellenwert erreicht ist.<br><br><b>Notizen:</b><ul><li>Wenn die [!UICONTROL Viewability Sensitivity] -Einstellung der Kampagne &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot; ist, wird der Standard für die Sichtbarkeitsmessung (MRC) für die Kampagne verwendet. [!DNL Media Rating Council] Wenn die Einstellung [!UICONTROL Viewability Sensitivity] &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;lautet, wird der Standard für die Sichtbarkeitsmessung für die Kampagne verwendet.[!DNL GroupM]</li><li>Adobe-Messdefinitionen unterscheiden sich von Drittanbieterdefinitionen, sodass es geringfügige Diskrepanzen mit Drittanbieterdaten geben kann.</li></ul> | Es empfiehlt sich, das Optimierungsziel und alle Filtereinstellungen vor dem Angebot mit der Einstellung [!UICONTROL Viewability Sensitivity] der Kampagne abzugleichen. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimierungsziele und deren Verwendung](optimization-goals.md)
