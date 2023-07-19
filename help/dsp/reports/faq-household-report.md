---
title: Häufig gestellte Fragen zu Haushalts-Berichten
description: Erfahren Sie mehr über die Reichweite, Häufigkeit und Konversionsdaten von Haushalten, einschließlich der Unterschiede zwischen den Haushaltsberichten und anderen Berichten sowie über die Fehlerbehebung.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: ae6028d7dc9b35906e4abcd727b84b169e5594b1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Haushalts-Berichten

## Die [!UICONTROL Household Reach & Frequency] Bericht

### Wie sind [!UICONTROL Household Reach & Frequency] Berichte unterscheiden sich von anderen benutzerspezifischen Berichten?

Die [!UICONTROL Household Reach & Frequency] -Bericht misst die Reichweite, Impressionen und Häufigkeit in verschiedenen Dimensionen auf Haushaltsebene basierend auf der IP-Adresse. Die anderen benutzerdefinierten Berichte werden auf Geräte- oder Cookie-Ebene generiert.

Selbst wenn beispielsweise eine Impression an drei Geräte innerhalb eines Haushalts bereitgestellt wird, ist die Metrik Einzelhaushalt erreicht eine.

#### Unterstützte Dimensionen

Die [!UICONTROL Household Reach & Frequency] unterstützt [folgende Dimensionen](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign], &quot;[!UICONTROL Package], &quot;[!UICONTROL Placement], &quot;[!UICONTROL Site/Apps]&quot;(die keinen Zugriff auf Überlagerungsmetriken bietet), &quot;[!UICONTROL Media Type], &quot;[!UICONTROL Feed Type], &quot;[!UICONTROL Device], &quot;[!UICONTROL Publisher], &quot;[!UICONTROL Audience], &quot;[!UICONTROL Creative Length],&quot;und vom Benutzer erstellte Platzierung &quot;[!UICONTROL Tags].&quot; |

#### Unterstützte Metriken

Die [verfügbare Metriken](/help/dsp/reports/report-columns.md) include:

* Überlagerungsmetriken: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]und [!UICONTROL Unique Household (Overlap)].

  Überlagerungsmetriken sind die Werte, die nur für die gemeldete Dimension oder Kombination von Dimensionen und nicht für andere Dimensionen auftreten. <!-- For example, it might show the ?? -->

* Nicht überlappende Metriken: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]und [!UICONTROL Unique Household Reached]

Konversionsmetriken und benutzerdefinierte Ziele werden nicht unterstützt.

### Was ist der Unterschied zwischen den Metriken zur Überschneidung und zur Nichtüberschneidung?

Die folgende Abbildung zeigt drei Metriken (Einzelhaushalt erreicht, Inkrementelle Haushalte erreicht und inkrementelle Haushalte (Überlappung)) für drei Kampagnen (A, B und C).

![Abbildung von Metriken zur Haushaltsüberschneidung](/help/dsp/assets/household-overlap-metrics-illustration.png "Abbildung von Metriken zur Haushaltsüberschneidung")

* Einzelhaushalte erreicht (Gesamt) liefert die von jeder Kampagne erreichte Unique HousVom-Haushalt oder die Gesamtfläche jedes Kreises. In der Abbildung wurden Einzelhaushalte erreicht durch A = Inkrementelle Haushalte erreicht durch A + (A+B) + (A+C) + (A+B+C) +(A+C+C)

* Inkrementelle Erreichbarkeit des Haushalts ist der Einzelhaushalt, der nur durch eine Kampagne erreicht wird. In dieser Zahl sind die von A, B, C erreichten inkrementellen Haushalte der von A, B bzw. C erreichte inkrementelle Haushalt.

* Inkrementelle Haushalte (Überlappung) sind die individuellen Haushalte, die durch die Kampagne oder Kombination von Kampagnen erreicht werden. In der Abbildung ist der inkrementelle Haushalt, der von A, C erreicht wurde, A+C.

### Workflow

Führen Sie die normalen Schritte aus, um [benutzerspezifischen Bericht erstellen](report-create.md).

Die [!UICONTROL Household Reach & Frequency] kann nur eine Dimension enthalten. Sie kann auch entweder a) Metriken nach beliebigen Dimensionen überlappen, mit Ausnahme von Site/Apps oder b) nicht überlappende Metriken, aber nicht beide.

### Was sind einige Einschränkungen der [!UICONTROL Household Reach & Frequency] Bericht?

Berichte mit Überlagerungsmetriken geben Schnittmengen von bis zu drei Werten aus. Wenn Sie beispielsweise die Metrik [!UICONTROL Unique Household (Overlap)] für 10 Platzierungen können Sie die individuellen Haushalte sehen, die durch individuelle Platzierungen erreicht werden, gemeinsame Haushalte, die durch eine Kombination zweier Praktika erreicht werden, und allgemeine Haushalte, die durch Kombinationen von drei Platzierungen erreicht werden. Sie können keine allgemeinen Haushalte sehen, die durch vier oder mehr Platzierungen erreicht wurden.

Bei anderen Dimensionen als Kampagne, Paket oder Platzierung unterstützt der Bericht bis zu 10 Werte in jeder Dimension. Um beispielsweise eine [!UICONTROL Unique Household Reached] Bericht für [!UICONTROL Audience] -Dimension, sollte die Anzahl der eindeutigen Zielgruppen kleiner als oder gleich 10 sein. Wenn Sie mehr als 10 eindeutige Zielgruppen einbeziehen, wird ein leerer Bericht generiert.

### Warum unterscheiden sich die Häufigkeit und die individuellen Reichweitenwerte zwischen [!UICONTROL Custom] und [!UICONTROL Household Reach & Frequency] Bericht?

Diese Metriken in [!UICONTROL Household] -Berichte werden anhand der tatsächlichen Anzahl der IP-Adressen berechnet, während die Metriken in der [!UICONTROL Custom] -Bericht verwenden geschätzte Zahlen, die anhand von Modellen berechnet werden. Die Diskrepanz sollte jedoch unter 10 % liegen.

### Wie konfiguriere ich den Bericht für die [!UICONTROL Placement Tags] Dimension?

So erstellen Sie Tags für die Platzierung: [Platzierungseinstellungen öffnen](/help/dsp/campaign-management/placements/placement-edit.md) und geben Sie Werte in die [Feld für Platzierungs-Tags](/help/dsp/campaign-management/placements/placement-settings.md).

Wenn eine Platzierung mehrere Tags enthält, betrachtet der Bericht die gesamte Zeichenfolge als ein Tag. Der Bericht enthält eine Zeile für jede eindeutige Zeichenfolge.

## Die [!UICONTROL Household Conversions] Bericht

### Welche Arten von Attributionsmethoden werden unterstützt in [!UICONTROL Household Conversions] Bericht?

Es werden zwei Arten von Attributionsmethoden unterstützt:

* Eindeutig: Zählt, wie oft sich ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Weg zur Konversion befunden hat.

* MTA (Multi-Touch-Attribution): Verteilt die Gutschrift jeder Konversion basierend auf der Häufigkeit des Auftretens des Dimensionswerts (z. B. ein Gerät oder eine Platzierung) auf dem Pfad zur Konversion. Wenn es beispielsweise insgesamt 10 Impressionen vor der Konvertierung gab, mit 8 bei CTV und 2 bei Mobile, werden 80 % der Gewichtung (0,8) an CTV-Bildschirme und 0,2 an Mobile vergeben.

### Inwiefern unterscheiden sich die Berichte zur Konversion aus Haushalten von den CTV-Durchsichtsberichten in Adobe Analytics?

CTV-Durchsichtsdaten in [!DNL Analytics] ist eingeschaltet [!DNL Analytics] -Tracking und verwenden die Haushaltskonversionsdaten Daten, die mithilfe des Adobe Advertising-Konversions-Tracking erfasst wurden. Darüber hinaus wird die DSP Attributionslogik in [!DNL Analytics] verwendet nur das letzte Ereignis, aber die Konversionsberichte der Haushalte unterstützen zwei verschiedene Attributionsmethoden: Eindeutig und MTA.

### Kann ich CTV-Durchsichtsdaten in beiden anzeigen? [!DNL Analytics for Advertising] und in benutzerspezifischen Berichten?

Advertiser ohne [!DNL Analytics for Advertising] kann nur den Haushaltskonversionsbericht für Haushaltskonversionsberichte verwenden.

Wenn Ihr Unternehmen [!DNL Analytics for Advertising]verwenden Sie beide Berichtstypen zusammen. Während CTV-Durchsichtsberichte für eine umfassende Kanalanalyse, das Site-Verhalten usw. geeignet sind, bieten benutzerdefinierte Berichte eine granulare Ansicht (mit Daten, die nach Medientyp, Herausgebern usw. aufgeschlüsselt sind), um die Faktoren anzuzeigen, die zu Konversionsraten führen.

## [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] Berichte vs. Daten aus [!DNL Advanced Measurement Services]

Für erweiterte Berichte zur budgetbasierten Reichweite und Häufigkeit oder Konversionen wird die Variable [[!DNL Strategic Advertising Consulting] Team](/help/dsp/introduction/advanced-measurement-services.md) kann hochgradig anpassbare Berichte zusammen mit ganzheitlichen strategischen Empfehlungen bereitstellen. Weitere Informationen finden Sie unter [!DNL Advanced Measurement Services], wenden Sie sich an Ihr Adobe Account Team.

### Wenn ich bereits verwende [!DNL Advanced Measurement Services], warum sollte ich die [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] Berichte?

Die [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] -Berichte ermöglichen es Kunden, die Reichweite, Häufigkeit und Konversionsmetriken auf Haushaltsebene in Echtzeit unabhängig abzurufen.

### Kann ich beide [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] Berichte und [!DNL Advanced Measurement Services]?

Der optimale Anwendungsfall besteht darin, beide [!UICONTROL Household] und [!DNL Advanced Measurement Services] Reporting- und Beratungsleistungen. Beachten Sie die [!UICONTROL Household] als Transaktionsnachrichten zu melden, um die täglichen Optimierungen zu unterstützen, und [!DNL Advanced Measurement Services] als strategischere, die ganzheitliche Lehren und Übernahmen mit übergeordneten Geschäftszielen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
