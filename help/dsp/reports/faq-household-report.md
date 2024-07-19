---
title: Häufig gestellte Fragen zu Haushalts-Berichten
description: Erfahren Sie mehr über die Reichweite, Häufigkeit und Konversionsdaten von Haushalten, einschließlich der Unterschiede zwischen den Haushaltsberichten und anderen Berichten sowie über die Fehlerbehebung.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Haushalts-Berichten

## Der Bericht [!UICONTROL Household Reach & Frequency]

### Inwiefern unterscheiden sich [!UICONTROL Household Reach & Frequency] -Berichte von anderen benutzerspezifischen Berichten?

Der Bericht [!UICONTROL Household Reach & Frequency] misst die Reichweite, Impression und Häufigkeit in verschiedenen Dimensionen auf Haushaltsebene basierend auf der IP-Adresse. Die anderen benutzerdefinierten Berichte werden auf Geräte- oder Cookie-Ebene generiert.

Selbst wenn beispielsweise eine Impression an drei Geräte innerhalb eines Haushalts bereitgestellt wird, ist die Metrik Einzelhaushalt erreicht eine.

#### Unterstützte Dimensionen

Der Bericht [!UICONTROL Household Reach & Frequency] unterstützt die [folgenden Dimensionen](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign]&quot; &quot;[!UICONTROL Package]&quot;, &quot;[!UICONTROL Placement]&quot;, &quot;[!UICONTROL Site/Apps]&quot; (die keinen Zugriff auf Überschneidungsmetriken bieten), &quot;[!UICONTROL Media Type]&quot;, &quot;[!UICONTROL Feed Type]&quot;, &quot;[!UICONTROL Device]&quot;, &quot;[!UICONTROL Publisher]&quot;, &quot;[!UICONTROL Audience]&quot;, &quot;12}&quot;und vom Benutzer erstellte Platzierung. [!UICONTROL Tags].&quot; |[!UICONTROL Creative Length]

#### Unterstützte Metriken

Zu den [verfügbaren Metriken](/help/dsp/reports/report-columns.md) gehören:

* Überlagerungsmetriken: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] und [!UICONTROL Unique Household (Overlap)].

  Überlagerungsmetriken sind die Werte, die nur für die gemeldete Dimension oder Kombination von Dimensionen und nicht für andere Dimensionen auftreten. <!-- For example, it might show the ?? -->

* Nicht überlappende Metriken: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] und [!UICONTROL Unique Household Reached]

Konversionsmetriken und benutzerdefinierte Ziele werden nicht unterstützt.

### Was ist der Unterschied zwischen den Metriken zur Überschneidung und zur Nichtüberschneidung?

Die folgende Abbildung zeigt drei Metriken (Einzelhaushalt erreicht, Inkrementelle Haushalte erreicht und inkrementelle Haushalte (Überlappung)) für drei Kampagnen (A, B und C).

![Abbildung der Metriken zur Haushaltstaxüberschneidung](/help/dsp/assets/household-overlap-metrics-illustration.png "Abbildung der Metriken zur Haushaltstaxüberschneidung")

* Einzelhaushalte erreicht (Gesamt) liefert die von jeder Kampagne erreichte Unique HousVom-Haushalt oder die Gesamtfläche jedes Kreises. In der Abbildung wurde der Einzelhaushalt erreicht durch A = Inkrementelle Haushalte erreicht durch A + (A+B) + (A+C) +(A+B+C) +(A+C)

* Inkrementelle Erreichbarkeit des Haushalts ist der Einzelhaushalt, der nur durch eine Kampagne erreicht wird. In dieser Zahl sind die von A, B, C erreichten inkrementellen Haushalte der von A, B bzw. C erreichte inkrementelle Haushalt.

* Inkrementelle Haushalte (Überlappung) sind die individuellen Haushalte, die durch die Kampagne oder Kombination von Kampagnen erreicht werden. In der Abbildung ist der inkrementelle Haushalt, der von A, C erreicht wurde, A+C.

### Workflow

Führen Sie die normalen Schritte aus, um [einen benutzerdefinierten Bericht zu erstellen](report-create.md).

Der Bericht [!UICONTROL Household Reach & Frequency] kann nur eine Dimension enthalten. Sie kann auch entweder a) Metriken nach beliebigen Dimensionen überlappen, mit Ausnahme von Site/Apps oder b) nicht überlappende Metriken, aber nicht beides.

### Welche Einschränkungen gibt es im Bericht [!UICONTROL Household Reach & Frequency]?

Berichte mit Überlagerungsmetriken geben Schnittmengen von bis zu drei Werten aus. Wenn Sie beispielsweise die Metrik &quot;[!UICONTROL Unique Household (Overlap)]&quot;für 10 Platzierungen verwenden, können Sie die Unique Houses sehen, die durch individuelle Platzierungen, durch eine Kombination zweier Platzierungen erreichte gemeinsame Haushalte und durch Kombinationen aus drei Platzierungen erreichte gemeinsame Haushalte erreicht wurden. Sie können keine allgemeinen Haushalte sehen, die durch vier oder mehr Platzierungen erreicht wurden.

Bei anderen Dimensionen als Kampagne, Paket oder Platzierung unterstützt der Bericht bis zu 10 Werte in jeder Dimension. Um beispielsweise einen [!UICONTROL Unique Household Reached] -Bericht für die Dimension [!UICONTROL Audience] zu generieren, sollte die Anzahl der eindeutigen Zielgruppen kleiner als oder gleich 10 sein. Wenn Sie mehr als 10 eindeutige Zielgruppen einbeziehen, wird ein leerer Bericht generiert.

### Warum unterscheiden sich die Häufigkeit und die individuellen Reichweitenwerte zwischen meinen [!UICONTROL Custom] Berichten und dem [!UICONTROL Household Reach & Frequency] Bericht?

Diese Metriken in [!UICONTROL Household] -Berichten werden anhand der tatsächlichen Anzahl der IP-Adressen berechnet, während die Metriken im [!UICONTROL Custom] -Bericht geschätzte Zahlen verwenden, die anhand von Modellen berechnet wurden. Die Diskrepanz sollte jedoch unter 10 % liegen.

### Wie konfiguriere ich den Bericht für die Dimension &quot;[!UICONTROL Placement Tags]&quot;?

Um Tags für die Platzierung zu erstellen, öffnen Sie [die Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-edit.md) und geben Sie Werte in das Feld [Platzierungs-Tags](/help/dsp/campaign-management/placements/placement-settings.md) ein.

Wenn eine Platzierung mehrere Tags enthält, betrachtet der Bericht die gesamte Zeichenfolge als ein Tag. Der Bericht enthält eine Zeile für jede eindeutige Zeichenfolge.

## Der Bericht [!UICONTROL Household Conversions]

### Welche Arten von Attributionsmethoden werden im [!UICONTROL Household Conversions] -Bericht unterstützt?

Es werden zwei Arten von Attributionsmethoden unterstützt:

* [!UICONTROL Unique]: Zählt, wie oft sich ein Dimensionswert (z. B. ein Gerät oder eine Platzierung) auf dem Weg zur Konversion befunden hat.

* [!UICONTROL Multi-Touch Attribution (MTA)]: Verteilt die Gutschrift jeder Konversion basierend auf der Häufigkeit des Auftretens des Dimensionswerts (z. B. ein Gerät oder eine Platzierung) auf dem Pfad zur Konversion. Wenn es beispielsweise insgesamt 10 Impressionen vor der Konvertierung gab, mit 8 bei CTV und 2 bei Mobile, werden 80 % der Gewichtung (0,8) an CTV-Bildschirme und 0,2 an Mobile vergeben.

### Inwiefern unterscheiden sich die Berichte zur Konversion aus Haushalten von den CTV-Durchsichtsberichten in Adobe Analytics?

CTV-Durchsichtsdaten in [!DNL Analytics] werden durch [!DNL Analytics]-Tracking unterstützt, und die Konversionsdaten der Haushalte verwenden Daten, die mithilfe des Adobe Advertising-Konversions-Trackings erfasst wurden. Darüber hinaus verwendet die DSP Attributionslogik in [!DNL Analytics] nur das letzte Ereignis, aber die Konversionsberichte der Haushalte unterstützen zwei verschiedene Attributionsmethoden: Eindeutig und MTA.

### Kann ich CTV-Durchsichtsdaten sowohl in [!DNL Analytics for Advertising] als auch in benutzerdefinierten Berichten anzeigen?

Werbetreibende ohne [!DNL Analytics for Advertising] können nur den Haushaltskonversion-Bericht für Haushaltskonversionsberichte verwenden.

Wenn Ihr Unternehmen über [!DNL Analytics for Advertising] verfügt, verwenden Sie beide Berichtstypen zusammen. Während CTV-Durchsichtsberichte für eine umfassende Kanalanalyse, das Site-Verhalten usw. geeignet sind, bieten benutzerdefinierte Berichte eine granulare Ansicht (mit Daten, die nach Medientyp, Herausgebern usw. aufgeschlüsselt sind), um die Faktoren anzuzeigen, die zu Konversionsraten führen.

## [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] Berichte vs. Daten von [!DNL Advanced Measurement Services]

Für erweiterte Berichte zur budgetbasierten Reichweite und Häufigkeit oder Konversionen kann das [[!DNL Strategic Advertising Consulting] Team](/help/dsp/introduction/advanced-measurement-services.md) hochgradig anpassbare Berichte zusammen mit ganzheitlichen strategischen Empfehlungen bereitstellen. Weitere Informationen zu [!DNL Advanced Measurement Services] erhalten Sie von Ihrem Adobe-Account-Team.

### Wenn ich bereits [!DNL Advanced Measurement Services] verwende, warum sollte ich dann die Berichte [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] verwenden?

Mit den Berichten [!UICONTROL Household Reach & Frequency] und [!UICONTROL Household Conversions] können Kunden die Reichweite, Häufigkeit und Konversionsmetriken auf Haushaltsebene in Echtzeit autonom abrufen.

### Kann ich sowohl die [!UICONTROL Household Reach & Frequency] - als auch die [!UICONTROL Household Conversions] -Berichte und die [!DNL Advanced Measurement Services] verwenden?

Der optimale Anwendungsfall besteht darin, sowohl den Bericht [!UICONTROL Household] als auch die Berichterstellungs- und Beratungsdienste für [!DNL Advanced Measurement Services] gemeinsam zu verwenden. Betrachten Sie den [!UICONTROL Household] -Bericht als Transaktionsbericht, der als Leitfaden für tägliche Optimierungen dienen soll, und [!DNL Advanced Measurement Services] als strategischerer Bericht, der ganzheitliche Erkenntnisse und Übernahmen in Verbindung mit übergeordneten Geschäftszielen vermittelt.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
