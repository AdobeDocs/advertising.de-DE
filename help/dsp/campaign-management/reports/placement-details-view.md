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

Für jede Platzierung können Sie [einen (Detailansicht [!UICONTROL Inspector])](placement-details-view.md) öffnen, der alle Targeting-Sites, Anzeigen und Angebote in einer Platzierung auflistet. Sie enthält auch Frequenzdaten für die Platzierung. Sie können die Daten optional von einem beliebigen Tab exportieren.

![placement Inspector](/help/dsp/assets/placement-inspector.png)

## Informationen in der Platzierung [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Alle Sites, auf denen die Platzierung Impressionen gehabt hat.

  Die Registerkarte [!UICONTROL Sites] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und eine Schaltfläche [!UICONTROL Exclude] in jeder Zeile, damit Sie eine Site schnell von der Platzierung ausschließen können.

* **[!UICONTROL Ads]:** Alle Anzeigen in der Platzierung.

  Die Registerkarte &quot;[!UICONTROL Ads]&quot;enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Pause] (damit Sie eine Anzeige schnell anhalten können).

* **[!UICONTROL Frequency]:** Daten für jede Anzeigenfrequenzebene für die Platzierung, einschließlich:
   * die Häufigkeit der Anzeige (z. B. &quot;1&quot;für alle Instanzen, in denen Benutzer eine Anzeige einmal gesehen haben);
   * die geschätzte eindeutige Anzahl von Geräten/Browsern oder Personen (je nach dem für die Kampagne festgelegten [!UICONTROL Cross Device Level] ), die Impressionen auf der festgelegten Frequenzebene erhalten haben
   * die geschätzte Anzahl von Impressionen auf der angegebenen Frequenzebene
   * die geschätzte Durchschnittshäufigkeit für das angegebene Frequenzniveau. Dieser Wert ist gleich (Geschätzte Impressionen)/(Geschätzte Individuen).

* **[!UICONTROL Inventory]:** Informationen über alle Angebote, die auf die Platzierung ausgerichtet sind.

  Die Registerkarte [!UICONTROL Inventory] ermöglicht die schnelle Fehlerbehebung, indem Leistungsstatistiken wie [!UICONTROL Auctions], [!UICONTROL Bids] und [!UICONTROL Win Rate] angezeigt werden. Die Registerkarte enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, einschließlich [!UICONTROL Edit], [!UICONTROL View Report] und [[!UICONTROL Auction Insights] für die weitere Fehlerbehebung](/help/dsp/inventory/private-deal-auction-insights.md).

## Öffnen Sie die [!UICONTROL Placement Inspector]

1. Öffnen Sie die Platzierungsansicht für die übergeordnete Kampagne oder das übergeordnete Paket:

   * Alle Platzierungen innerhalb der übergeordneten Kampagne anzeigen:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Placements]** .

   * Zeigen Sie alle Platzierungen innerhalb des übergeordneten Pakets an:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

      1. Klicken Sie auf den Namen der Kampagne.

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Packages]** .

      1. Klicken Sie auf den Namen des übergeordneten Pakets.

1. Halten Sie den Cursor über die Platzierungszeile, klicken Sie auf **[!UICONTROL More]** und klicken Sie dann auf eine Option:

   * Um alle Sites anzuzeigen, auf die die Platzierung ausgerichtet ist, klicken Sie auf **[!UICONTROL Sites]**.

   * Um alle Anzeigen in der Platzierung anzuzeigen, klicken Sie auf **[!UICONTROL Ads]**.

   * Klicken Sie auf &quot;**[!UICONTROL Frequency]**&quot;, um die Frequenzdaten für die Platzierung anzuzeigen.

   * Klicken Sie auf **[!UICONTROL Inventory]**, um alle Angebote anzuzeigen, auf die die Platzierung ausgerichtet ist.

1. (Optional) [Ändern Sie die Spaltenansicht](campaign-data-views-manage.md#column-view-change) nach Bedarf, um die erforderlichen Metriken anzuzeigen.

1. (Optional) Um die Daten auf einer beliebigen Registerkarte zu exportieren, klicken Sie oben rechts auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und dann auf **[!UICONTROL Export]**.

   Die Daten werden als Bericht im XLSM-Format im standardmäßigen Download-Ordner des Browsers gespeichert.

## Fehlerbehebung beim Inventar

| Problem | Mögliche Ursache | Maßnahmen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Der Herausgeber hat nicht damit begonnen, Angebotsanfragen zu senden. | Wenden Sie sich an den Herausgeber, um den Deal zu aktivieren. |
| | Das Geschäft wurde falsch eingerichtet, z. B. durch Eingabe einer falschen externen Deal-ID. | Bestätigen Sie die Geschäftsdetails und bearbeiten Sie den Deal. |
| [!UICONTROL Auctions but no Bids] | Das Platzierungs-Targeting stimmt nicht mit den eingehenden Angebotsanfragen für den Deal überein. <br><br> Beispielsweise könnte eine Platzierung auf eine geografische Region ausgerichtet sein, die nicht für den Deal infrage kommt. | Bearbeiten Sie die Platzierungsziele nach Bedarf, um Targeting-Inkongruenzen zu vermeiden. |
| | Die Platzierung verfügt nicht über eine aktive Anzeige mit dem erforderlichen Medientyp für das Geschäft. | Erstellen Sie eine Anzeige mit dem richtigen Medientyp und fügen Sie sie an die Platzierung an. |
| | Die Platzierung hat kein angemessenes Budget. | Erhöhen Sie das Platzierungsbudget, um Gebote für eingehende Anforderungen zu ermöglichen. |
| | Die Platzierungs-Flugdaten überschneiden sich nicht mit den Impressions-Sendedaten für den Deal. | Bearbeiten Sie bei Bedarf die Flugdaten der Platzierung. |
| [!UICONTROL Low Win Rate] | Das Höchstgebot der Platzierung (Untergrenze oder Festbetrag) liegt unter dem für das Geschäft erforderlichen Minimum. | Erhöhen Sie den Wert [!UICONTROL Max Bid] der Platzierung nach Bedarf. |
| | Die Platzierung verwendet Filter vor dem Angebot, die das Angebot einschränken. | Verringern Sie die Schwellenwerte der Filter vor dem Angebot, um mehr Gebote zu ermöglichen. |
| | Das Zielgruppen-Targeting für die Platzierung ist zu restriktiv. | Überprüfen Sie, ob die angegebenen Zielgruppen über ausreichend aktive Benutzer verfügen, und erweitern Sie die Zielgruppe nach Möglichkeit. |

>[!MORELIKETHIS]
>
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](campaign-reports-about.md)
>* [Verwalten der Datenansichten Ihrer Kampagne](campaign-data-views-manage.md)
