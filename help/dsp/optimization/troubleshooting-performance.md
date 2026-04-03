---
title: Fehlerbehebung bei der Leistung
description: Verweisen Sie auf häufige Leistungsprobleme und sehen Sie, wie Sie diese beheben können.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
TQID: https://experienceleague.adobe.com/CLEAjCOYzIKDaAbH4-mZxna7MK5jmpvaCjdhGScwzQs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Fehlerbehebung bei der Leistung

| Problem | Mögliche Ursache | Zu ergreifende Maßnahmen |
| --- | --- | --- |
| Keine Ausgaben für Platzierung | Die Platzierung umfasst keine Anzeigen und/oder die Anzeigen sind nicht aktiv. | Überprüfen Sie, ob alle erwarteten Anzeigen mit der Platzierung verbunden sowie genehmigt und aktiv sind.<br><br>Überprüfen Sie außerdem, ob die Platzierung einen benutzerdefinierten Anzeigenzeitplan enthält, der die Flugdauer für jede Anzeige begrenzen kann. Um den Anzeigenzeitplan für eine Platzierung in der Ansicht Platzierungen anzuzeigen, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** neben dem Platzierungsnamen. |
| | Die betroffenen Daten liegen nicht innerhalb der konfigurierten Flugdaten. | Überprüfen Sie, ob die Flugdaten auf Kampagnen-, Paket- und &#x200B; gültig sind. |
| | Das Budgetziel wurde erreicht und/oder ist nicht hoch genug. | Überprüfen Sie die Budgeteinstellungen auf der Kampagnen-, Paket- und Platzierungsebene. |
| | Das Konto ist nicht ausreichend finanziert. | Um zu sehen, ob Ihr Konto ausreichend finanziert ist, gehen Sie zu **[!UICONTROL Settings]** > **[!UICONTROL Account]** und sehen Sie sich die Höhe der [!UICONTROL Usable Funds] an. Wenn Sie mehr Mittel benötigen, wenden Sie sich an Ihr Adobe Account Team. |
| | Es ist kein Inventar verfügbar. | Überprüfen Sie, ob die angegebenen Inventarquellen ([!UICONTROL Public], [!UICONTROL Private] oder [!UICONTROL On Demand]):<ul><li>Korrektes Setup.</li><li>Aktiv und Versand durch Auktionen.</li><li>Kompatibel mit dem entsprechenden Anzeigen- und Platzierungstyp.</li></ul><br>Wenn alle Inventarquellen gültig und aktiv sind, sollten Sie nach Möglichkeit zusätzliche oder alle Inventarquellen auswählen. |
| | Es sind keine Benutzer verfügbar. | Vergewissern Sie sich, dass die angegebenen Zielgruppenziele genügend aktive Benutzer enthalten. Ist dies nicht der Fall, erweitern Sie die Ziele, indem Sie weitere Zielgruppen hinzufügen. |
| Geringe Platzierungsausgaben | Im [!UICONTROL Non Bids] Abschnitt des Berichts zur Platzierungsdiagnose werden mögliche Gründe dafür angezeigt, warum die Platzierung kein Angebot abgegeben hat. | [Überprüfen Sie den [!UICONTROL Non Bids]-](/help/dsp/campaign-management/reports/placement-diagnostics.md), um zu verstehen, warum die Platzierung kein Gebot abgegeben hat.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | Die Platzierung verwendet [Pre-Bid-Filter](/help/dsp/campaign-management/placements/placement-settings.md) die die Gebote einschränken. | Senken Sie die Schwellenwerte der Filter vor Gebotsabgabe um 5 %, um das Gleichgewicht zwischen Ausgaben und Leistung zu bewerten. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Pre-Bid-Filter, GeoS, Inventar und Zielgruppen, Gebote und Ausgaben kumulativ begrenzen kann. |
| | Die Platzierung hat eine niedrige Erfolgsquote. | Erhöhen Sie die [!UICONTROL Max Bid], um die Gewinnrate zu verbessern.<br><br><b>HINWEIS: </b> Inventarpreise können je nach Zielgruppenbestimmung der Platzierung variieren.<br><br>Eine Gewinnquote von 10 % gilt als gesund. |
| | Eine geringe Anzahl von Beständen ist verfügbar. | Wenn möglich, zusätzliche oder alle Inventarquellen auswählen.<br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Pre-Bid-Filter, GeoS, Inventar und Zielgruppen, Gebote und Ausgaben kumulativ begrenzen kann. |
| | Eine geringe Anzahl von Benutzern ist verfügbar. | Vergewissern Sie sich, dass die angegebenen Zielgruppenziele genügend aktive Benutzer enthalten. Ist dies nicht der Fall, erweitern Sie die Ziele, indem Sie weitere Zielgruppen hinzufügen.<br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Pre-Bid-Filter, GeoS, Inventar und Zielgruppen, Gebote und Ausgaben kumulativ begrenzen kann. |
| | Das Paket enthält eine große Anzahl aktiver Platzierungen. | Verringern Sie entweder die Anzahl aktiver Platzierungen innerhalb des Pakets oder erhöhen Sie das Gesamtbudget des Pakets.<br><br>Wenn das Paket viele Platzierungen, aber nicht genug Budget hat, kann DSP möglicherweise nicht genügend Budget für jede Platzierung zuweisen. Jede Platzierung sollte die Möglichkeit haben, mindestens 2 USD/Tag auszugeben. Wenn Ihr Paket beispielsweise über ein Budget von 10 USD/Tag verfügt, sollten Sie fünf oder weniger Platzierungen einbeziehen. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
