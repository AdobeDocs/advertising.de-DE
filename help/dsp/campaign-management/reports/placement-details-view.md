---
title: Anzeigen der Sites, Anzeigen, Häufigkeit und Inventardetails für eine Platzierung anzeigen
description: Erfahren Sie, wie Sie die Zielseiten, Anzeigen, Häufigkeit und Inventardaten für eine Platzierung anzeigen.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Anzeigen der Sites, Anzeigen, Häufigkeit und Inventardetails für eine Platzierung anzeigen

Für jede Platzierung können Sie [eine (Detailansicht-[!UICONTROL Inspector]) öffnen](placement-details-view.md) in der alle Zielseiten, Anzeigen und Angebote einer Platzierung aufgelistet sind. Es enthält auch Häufigkeitsdaten für die Platzierung. Sie können optional die Daten aus jeder Registerkarte exportieren.

![Placement Inspector](/help/dsp/assets/placement-inspector.png)

## Informationen im [!UICONTROL Inspector] Platzierung {#placement-inspector}

* **[!UICONTROL Sites]:** Alle Seiten, auf denen die Platzierung Impressionen hatte.

  Die Registerkarte [!UICONTROL Sites] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, sowie eine Schaltfläche [!UICONTROL Exclude] in jeder Zeile, damit Sie eine Site schnell aus der Platzierung ausschließen können.

* **[!UICONTROL Ads]:** Alle Anzeigen in der Platzierung.

  Die Registerkarte [!UICONTROL Ads] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, sowie Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Pause] (sodass Sie eine Anzeige schnell anhalten können).

* **[!UICONTROL Frequency]:** Daten für jede Anzeigenhäufigkeitsstufe für die Platzierung, einschließlich:
   * Die Anzeigenhäufigkeit (z. B. „1“ für alle Instanzen, in denen Benutzende eine Anzeige einmal gesehen haben)
   * Die geschätzte eindeutige Anzahl der Geräte/Browser oder Personen (je nach dem angegebenen [!UICONTROL Cross Device Level] für die Kampagne), die Impressionen auf der angegebenen Häufigkeitsstufe erhalten haben
   * Die geschätzte Anzahl von Impressionen auf der angegebenen Häufigkeitsstufe
   * Die geschätzte durchschnittliche Häufigkeit für die angegebene Häufigkeitsstufe. Dieser Wert ist gleich (Geschätzte Impressions)/(Geschätzte eindeutige Werte).

* **[!UICONTROL Inventory]:** Informationen zu allen Angeboten, die von der Platzierung angesprochen werden.

  Die Registerkarte [!UICONTROL Inventory] ermöglicht eine schnelle Fehlerbehebung durch die Anzeige von Leistungsstatistiken wie [!UICONTROL Auctions], [!UICONTROL Bids] und [!UICONTROL Win Rate]. Die Registerkarte enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, sowie Schnellaktionsschaltflächen in jeder Zeile, einschließlich [!UICONTROL Edit], [!UICONTROL View Report] und [[!UICONTROL Auction Insights] für weitere Fehlerbehebungen](/help/dsp/inventory/private-deal-auction-insights.md).

## [!UICONTROL Placement Inspector] öffnen

1. Öffnen Sie die Ansicht Platzierungen für die übergeordnete Kampagne oder das übergeordnete Paket:

   * Alle Platzierungen innerhalb der übergeordneten Kampagne anzeigen:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Placements]** .

   * Alle Platzierungen innerhalb des übergeordneten Pakets anzeigen:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Packages]** .

      1. Klicken Sie auf den Namen des übergeordneten Pakets.

1. Halten Sie den Cursor über der Platzierungszeile, klicken Sie auf **[!UICONTROL More]** und klicken Sie dann auf eine Option:

   * Um alle Websites anzuzeigen, die Ziel der Platzierung sind, klicken Sie auf **[!UICONTROL Sites]**.

   * Um alle Anzeigen in der Platzierung anzuzeigen, klicken Sie auf **[!UICONTROL Ads]**.

   * Um Häufigkeitsdaten für die Platzierung anzuzeigen, klicken Sie auf **[!UICONTROL Frequency]**.

   * Um alle Angebote anzuzeigen, auf die sich die Platzierung bezieht, klicken Sie auf **[!UICONTROL Inventory]**.

1. (Optional) [Ändern Sie die Spaltenansicht](campaign-data-views-manage.md#column-view-change) nach Bedarf, um die erforderlichen Metriken anzuzeigen.

1. (Optional) Um die Daten auf einer beliebigen Registerkarte zu exportieren, klicken ![ oben rechts auf Mehr](/help/search-social-commerce/assets/more.png "Mehr") und anschließend auf **[!UICONTROL Export]**.

   Die Daten werden im Standard-Download-Ordner Ihres Browsers als Bericht im XLSM-Format gespeichert.

## Fehlerbehebung bei Inventar

| Problem | Mögliche Ursache | Zu ergreifende Maßnahmen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Der Publisher hat nicht begonnen, Angebotsanfragen zu senden. | Kontaktieren Sie den Publisher, um den Deal zu aktivieren. |
| | Der Abschluss wurde falsch eingerichtet, z. B. durch Eingabe einer falschen externen Angebots-ID. | Bestätigen Sie die Details des Angebots und bearbeiten Sie es. |
| [!UICONTROL Auctions but no Bids] | Die Platzierungs-Zielgruppenbestimmung stimmt nicht mit den eingehenden Angebotsanfragen für den Deal überein. <br><br> Beispielsweise könnte eine Platzierung auf eine Geografie abzielen, die nicht für den Abschluss infrage kommt. | Bearbeiten Sie die Platzierungsziele nach Bedarf, um Zielgruppenabweichungen zu vermeiden. |
| | Für die Platzierung ist keine aktive Anzeige mit dem erforderlichen Medientyp für das Angebot vorhanden. | Erstellen Sie eine Anzeige mit dem richtigen Medientyp und fügen Sie sie der Platzierung hinzu. |
| | Die Platzierung verfügt nicht über ein angemessenes Budget. | Erhöhen Sie das Platzierungsbudget, um Gebote für eingehende Anfragen zuzulassen. |
| | Die Termine für die Platzierungen und Flüge überschneiden sich nicht mit den Impression-Lieferterminen für den Deal. | Bearbeiten Sie die Flugdaten der Platzierung nach Bedarf. |
| [!UICONTROL Low Win Rate] | Das maximale Gebot der Platzierung (Untergrenze oder Festbetrag) liegt unter dem Mindestgebot, das vom Abschluss gefordert wird. | Erhöhen Sie bei Bedarf die [!UICONTROL Max Bid] der Platzierung. |
| | Die Platzierung verwendet Pre-Bid-Filter, die die Gebotsabgabe einschränken. | Verringern Sie die Schwellenwerte der Pre-Bid-Filter, um mehr Gebote zu ermöglichen. |
| | Zielgruppen-Targeting für die Platzierung ist zu restriktiv. | Überprüfen Sie, ob die angegebenen Zielgruppenziele genügend aktive Benutzer haben, und erweitern Sie die Zielgruppe nach Möglichkeit. |

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
>* [Campaign-Datenansichten verwalten](campaign-data-views-manage.md)
