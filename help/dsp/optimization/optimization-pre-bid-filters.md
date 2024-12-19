---
title: Pre-Bid-Filter auf Platzierungsebene und deren Verwendung
description: Verweisen Sie auf die verfügbaren Pre-Bid-Filter auf Platzierungsebene und sehen Sie sich an, wie sie verwendet werden.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Pre-Bid-Filter auf Platzierungsebene und deren Verwendung

| Pre-Bid-Filter | Beschreibung | Verwendung dieses Filters |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Legt einen minimalen Prognoseschwellenwert für die Wahrscheinlichkeit fest, dass eine Auktion zu einem Clickthrough führen kann. Wenn Sie beispielsweise den Schwellenwert auf 0,1 % festlegen, bieten Sie nur dann auf Auktionen, wenn die prognostizierte Wahrscheinlichkeit eines Klicks größer oder gleich 0,1 % ist.<br><br><b>Hinweis:</b> Filter werden vor den Optimierungszielen angewendet. Daher können sehr strenge Filter Ausgaben verhindern. | Verwenden Sie , wenn Sie ein minimales KPI-Ziel für die Clickthrough-Rate (CTR) haben und Ihr Budget nicht ausgeben möchten, wenn die CTR unter dem Schwellenwert liegt. Dieser Filter kann sehr restriktiv sein, daher ist es wichtig, realistische Ziele festzulegen. Je nach weiteren Einschränkungen der Platzierung ist ein Ziel von 03-,07% in der Regel ein guter Ausgangspunkt. Sie können dies nach Bedarf auf Site-Ebene optimieren, um die Metriken zu verbessern.<br><br>Wenn Sie eine minimale CTR und die bestmögliche CPM erreichen möchten, empfiehlt es sich, einen [!UICONTROL Click Through Rate] mit dem Optimierungsziel &quot;[!UICONTROL Lowest CPM]&quot; zu kombinieren. Wenn Sie ein Höchstmaß an CPM ohne wirklichen Nutzen für die Übererfüllung und ein Mindestmaß an CTR anstreben, ist die Kopplung eines [!UICONTROL Click Through Rate] mit dem Optimierungsziel &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; möglicherweise besser geeignet. |
| [!UICONTROL 100% Completion Rate] | Legt eine erforderliche Mindestabschlussrate fest, die erfüllt sein muss, bevor Sie ein Gebot für eine Impression abgeben. | Verwenden Sie diesen Filter, wenn das Hauptziel der Kampagne die Abschlussraten sind. Berücksichtigen Sie auch die anderen Zielgruppenbestimmungsparameter, doch 65 % sind der empfohlene Anfangsprozentsatz. |
| [!UICONTROL Player Size - Adobe] | Legt mithilfe von DSP-Daten eine erforderliche Mindestgröße für den Player fest. Sie können bei einer Impression bieten, wenn der [!UICONTROL Player Size] Schwellenwert erreicht wird. | Verwenden Sie , um sicherzustellen, dass Sie mit Daten aus DSP einen vollständigen Player-Bestand für die Folge bereitstellen. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Legt eine erforderliche Mindestgröße für den Player fest, indem Daten aus [!DNL Moat] oder [!DNL Integral Ad Science] ([!DNL IAS]) verwendet werden. Sie können bei einer Impression bieten, wenn der [!UICONTROL Player Size] Schwellenwert erreicht wird. | Verwenden Sie , um sicherzustellen, dass Sie einen vollständigen Player-Bestand für die Folge bereitstellen, indem Sie plattformweite [!DNL Moat]- oder [!DNL IAS] verwenden.<br><br><b>Hinweis:</b> Verwenden Sie diesen Filter nur, wenn die Kampagne für die Verwendung von [!DNL Moat]- oder [!DNL IAS] konfiguriert ist. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Legt einen erforderlichen Prozentsatz für die minimale Sichtbarkeit anhand der DSP-Sichtbarkeitszahlen und -messungen fest. Sie können ein Gebot für eine Impression abgeben, wenn der angegebene Schwellenwert erreicht wird.<br><br><b>Hinweise:</b><ul><li>Wenn die [!UICONTROL Viewability Sensitivity] der Kampagne &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot; ist, wird der Standard für die Sichtbarkeitsmessung im [!DNL Media Rating Council] (MRC) für die Kampagne verwendet. Wenn die [!UICONTROL Viewability Sensitivity] auf &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot; eingestellt ist, wird der Standard für die Messung der [!DNL GroupM] Sichtbarkeit für die Kampagne verwendet.</li><li>Adobe-Messdefinitionen unterscheiden sich von den Definitionen von Drittanbietern, sodass es zu geringfügigen Abweichungen bei den Daten von Drittanbietern kommen kann.</li></ul> | Es empfiehlt sich, das Optimierungsziel und alle Pre-Bid-Filtereinstellungen mit der [!UICONTROL Viewability Sensitivity] der Kampagne abzugleichen. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
