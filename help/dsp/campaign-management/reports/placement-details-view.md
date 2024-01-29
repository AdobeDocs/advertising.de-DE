---
title: Anzeigen von Sites, Anzeigen, Häufigkeit und Inventardetails für eine Platzierung
description: Erfahren Sie, wie Sie die zielgerichteten Sites, Anzeigen, Häufigkeit und Inventardaten für eine Platzierung anzeigen.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Anzeigen von Sites, Anzeigen, Häufigkeit und Inventardetails für eine Platzierung

Für jede Platzierung können Sie [Öffnen einer (Detailansicht) [!UICONTROL Inspector])](placement-details-view.md), die alle zielgerichteten Sites, Anzeigen und Angebote in einer Platzierung auflistet. Sie enthält auch Frequenzdaten für die Platzierung. Sie können die Daten optional von einem beliebigen Tab exportieren.

![placement Inspector](/help/dsp/assets/placement-inspector.png)

## Informationen in der Platzierung [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Alle Sites, auf denen die Platzierung Impressionen gehabt hat.

  Die [!UICONTROL Sites] Registerkarte enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und eine [!UICONTROL Exclude] in jeder Zeile, damit Sie eine Site schnell aus der Platzierung ausschließen können.

* **[!UICONTROL Ads]:** Alle Anzeigen in der Platzierung.

  Die [!UICONTROL Ads] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Pause] (sodass Sie eine Anzeige schnell anhalten können).

* **[!UICONTROL Frequency]:** Daten für jede Anzeigenfrequenzebene für die Platzierung, einschließlich:
   * die Häufigkeit der Anzeige (z. B. &quot;1&quot;für alle Instanzen, in denen Benutzer eine Anzeige einmal gesehen haben);
   * die geschätzte eindeutige Anzahl von Geräten/Browsern oder Personen (je nach spezifiziertem [!UICONTROL Cross Device Level] für die Kampagne), die Impressionen auf der festgelegten Frequenzebene erhalten haben
   * die geschätzte Anzahl von Impressionen auf der angegebenen Frequenzebene
   * die geschätzte Durchschnittshäufigkeit für das angegebene Frequenzniveau. Dieser Wert ist gleich (Geschätzte Impressionen)/(Geschätzte Individuen).

* **[!UICONTROL Inventory]:** Informationen zu allen Angeboten, die auf die Platzierung ausgerichtet sind.

  Die [!UICONTROL Inventory] -Registerkarte ermöglicht die schnelle Fehlerbehebung, indem Leistungsstatistiken angezeigt werden, z. B. [!UICONTROL Auctions], [!UICONTROL Bids], und [!UICONTROL Win Rate]. Die Registerkarte enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, sowie Schnellaktionsschaltflächen in jeder Zeile, einschließlich [!UICONTROL Edit], [!UICONTROL View Report], und [[!UICONTROL Auction Insights] für weitere Fehlerbehebung](/help/dsp/inventory/private-deal-auction-insights.md).

## Öffnen Sie die [!UICONTROL Placement Inspector]

1. Öffnen Sie die Platzierungsansicht für die übergeordnete Kampagne oder das übergeordnete Paket:

   * Alle Platzierungen innerhalb der übergeordneten Kampagne anzeigen:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf **[!UICONTROL Placements]** Registerkarte.

   * Zeigen Sie alle Platzierungen innerhalb des übergeordneten Pakets an:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf **[!UICONTROL Packages]** Registerkarte.

      1. Klicken Sie auf den Namen des übergeordneten Pakets.

1. Halten Sie den Cursor über die Platzierungszeile und klicken Sie auf **[!UICONTROL More]** und klicken Sie dann auf eine Option:

   * Um alle Sites anzuzeigen, auf die die Platzierung ausgerichtet ist, klicken Sie auf **[!UICONTROL Sites]**.

   * Um alle Anzeigen in der Platzierung anzuzeigen, klicken Sie auf **[!UICONTROL Ads]**.

   * Um die Frequenzdaten für die Platzierung anzuzeigen, klicken Sie auf **[!UICONTROL Frequency]**.

   * Um alle Angebote anzuzeigen, die die Platzierung als Ziel hat, klicken Sie auf **[!UICONTROL Inventory]**.

1. (Optional) [Spaltenansicht ändern](campaign-data-views-manage.md#column-view-change) nach Bedarf, um die erforderlichen Metriken anzuzeigen.

1. (Optional) Um die Daten auf einer beliebigen Registerkarte zu exportieren, klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") oben rechts und klicken Sie dann auf **[!UICONTROL Export]**.

   Die Daten werden als Bericht im XLSM-Format im standardmäßigen Download-Ordner des Browsers gespeichert.

## Fehlerbehebung beim Inventar

| Problem | Mögliche Ursache | Maßnahmen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Der Herausgeber hat nicht damit begonnen, Angebotsanfragen zu senden. | Wenden Sie sich an den Herausgeber, um den Deal zu aktivieren. |
| | Das Geschäft wurde falsch eingerichtet, z. B. durch Eingabe einer falschen externen Deal-ID. | Bestätigen Sie die Geschäftsdetails und bearbeiten Sie den Deal. |
| [!UICONTROL Auctions but no Bids] | Das Platzierungs-Targeting stimmt nicht mit den eingehenden Angebotsanfragen für den Deal überein. <br><br> Eine Platzierung könnte beispielsweise auf eine Region ausgerichtet sein, die für den Deal nicht infrage kommt. | Bearbeiten Sie die Platzierungsziele nach Bedarf, um Targeting-Inkongruenzen zu vermeiden. |
| | Die Platzierung verfügt nicht über eine aktive Anzeige mit dem erforderlichen Medientyp für das Geschäft. | Erstellen Sie eine Anzeige mit dem richtigen Medientyp und fügen Sie sie an die Platzierung an. |
| | Die Platzierung hat kein angemessenes Budget. | Erhöhen Sie das Platzierungsbudget, um Gebote für eingehende Anforderungen zu ermöglichen. |
| | Die Platzierungs-Flugdaten überschneiden sich nicht mit den Impressions-Sendedaten für den Deal. | Bearbeiten Sie bei Bedarf die Flugdaten der Platzierung. |
| [!UICONTROL Low Win Rate] | Das Höchstgebot der Platzierung (Untergrenze oder Festbetrag) liegt unter dem für das Geschäft erforderlichen Minimum. | Erhöhen Sie die [!UICONTROL Max Bid] nach Bedarf. |
| | Die Platzierung verwendet Filter vor dem Angebot, die das Angebot einschränken. | Verringern Sie die Schwellenwerte der Filter vor dem Angebot, um mehr Gebote zu ermöglichen. |
| | Das Zielgruppen-Targeting für die Platzierung ist zu restriktiv. | Überprüfen Sie, ob die angegebenen Zielgruppen über ausreichend aktive Benutzer verfügen, und erweitern Sie die Zielgruppe nach Möglichkeit. |

>[!MORELIKETHIS]
>
>* [Arten von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
>* [Datenansichten Ihrer Kampagne verwalten](campaign-data-views-manage.md)
