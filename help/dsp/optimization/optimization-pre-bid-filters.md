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
| [!UICONTROL Click Through Rate] | Legt einen minimalen Prognoseschwellenwert für die Wahrscheinlichkeit fest, dass eine Auktion zu einem Clickthrough führen kann. Wenn Sie beispielsweise den Schwellenwert auf 0,1 % setzen, bieten Sie bei Auktionen nur Angebote, bei denen die prognostizierte Wahrscheinlichkeit eines Klicks größer oder gleich 0,1 % ist.<br><br><b>Hinweis:</b> Filter werden vor Optimierungszielen angewendet. Daher können sehr strenge Filter Ausgaben verhindern. | Verwenden Sie diese Option, wenn Sie ein KPI-Mindestziel für die Clickthrough-Rate (CTR) haben und Ihr Budget nicht ausgeben möchten, wenn die CTR unter dem Schwellenwert liegt. Dieser Filter kann sehr restriktiv sein, daher ist es wichtig, realistische Ziele festzulegen. Je nach anderen Einschränkungen der Platzierung ist ein Ziel von 0,03-0,07 % im Allgemeinen ein guter Ausgangspunkt. Sie können dies bei Bedarf auf Site-Ebene optimieren, um die Metriken zu verbessern.<br><br>Wenn Ihr Ziel darin besteht, eine minimale CTR und den bestmöglichen CPM zu erreichen, wird empfohlen, eine [!UICONTROL Click Through Rate] mit dem Optimierungsziel filtern &quot;[!UICONTROL Lowest CPM].&quot; Wenn Ihr Ziel ein maximaler CPM ohne echten Nutzen für die Übererfüllung und ein minimaler CTR ist, dann paaren Sie eine [!UICONTROL Click Through Rate] mit dem Optimierungsziel filtern &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; besser geeignet sein. |
| [!UICONTROL 100% Completion Rate] | Legt eine erforderliche minimale Abschlussrate fest, die erfüllt sein muss, bevor Sie ein Angebot für eine Impression abgeben. | Verwenden Sie diesen Filter, wenn das Hauptziel der Kampagne die Abschlussraten sind. Faktor in anderen Targeting-Parametern, aber 65% ist der empfohlene Anfangsprozentsatz. |
| [!UICONTROL Player Size - Adobe] | Legt eine erforderliche minimale Player-Größe mithilfe von Daten aus DSP fest. Sie können einen Impression bei der [!UICONTROL Player Size] -Schwellenwert erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie mit Daten aus DSP ein Inventar für den vollständigen Episode-Player bereitstellen. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Legt eine erforderliche minimale Player-Größe mithilfe von Daten aus [!DNL Moat] oder [!DNL Integral Ad Science] ([!DNL IAS]). Sie können einen Impression bei der [!UICONTROL Player Size] -Schwellenwert erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie das Inventar des vollständigen Episode-Players mithilfe der plattformweiten Bereitstellung bereitstellen. [!DNL Moat] oder [!DNL IAS] Daten.<br><br><b>Hinweis:</b> Verwenden Sie diesen Filter nur, wenn die Kampagne für die Verwendung konfiguriert ist. [!DNL Moat] oder [!DNL IAS] Daten. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Legt einen erforderlichen Mindestprozentsatz für die Sichtbarkeit mithilfe DSP Sichtbarkeitszahlen und Messungen fest. Sie können ein Angebot für eine Impression erstellen, wenn der angegebene Schwellenwert erreicht ist.<br><br><b>Hinweise:</b><ul><li>Wenn die Kampagne [!UICONTROL Viewability Sensitivity] Einstellung ist[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot;dann die [!DNL Media Rating Council] (MRC) Der Standard zur Sichtbarkeitsmessung wird für die Kampagne verwendet. Wenn die Variable [!UICONTROL Viewability Sensitivity] Einstellung ist[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot;dann die [!DNL GroupM] Für die Kampagne wird der Standard für die Sichtbarkeitsmessung verwendet.</li><li>Adobe-Messdefinitionen unterscheiden sich von Drittanbieterdefinitionen, sodass es geringfügige Diskrepanzen mit Drittanbieterdaten geben kann.</li></ul> | Die Best Practice besteht darin, das Optimierungsziel und alle Filtereinstellungen vor dem Angebot mit der Kampagne [!UICONTROL Viewability Sensitivity] -Einstellung. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
