---
title: Fehlerbehebung bei der Leistung
description: Referenzieren Sie allgemeine Leistungsprobleme und finden Sie Informationen zur Fehlerbehebung.
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Fehlerbehebung bei der Leistung

| Problem | Mögliche Ursache | Maßnahmen |
| --- | --- | --- |
| Keine Ausgaben für Platzierung | Die Platzierung umfasst keine Anzeigen und/oder die Anzeigen sind nicht aktiv. | Stellen Sie sicher, dass alle erwarteten Anzeigen an die Platzierung angehängt und genehmigt und aktiv sind.<br><br>Überprüfen Sie außerdem, ob die Platzierung einen benutzerdefinierten Anzeigenzeitplan enthält, der die Flugzeit für jede Anzeige einschränken kann. Um den Anzeigenzeitplan für eine Platzierung in der Platzierungsansicht anzuzeigen, klicken Sie auf  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** neben dem Platzierungsnamen. |
|  | Die betroffenen Daten liegen nicht innerhalb der konfigurierten Flugdaten. | Vergewissern Sie sich, dass die Flugdaten auf der Kampagnen-, Paket- und Platzierungsebene der &#x200B; gültig sind. |
|  | Das Budgetziel wurde erreicht und/oder ist nicht hoch genug. | Prüfen Sie die Budgeteinstellungen auf Kampagnen-, Paket- und Platzierungsebene. |
|  | Das Konto hat nicht genug Geld. | Um zu sehen, ob Ihr Konto ausreichend finanziert ist, gehen Sie zu **[!UICONTROL Settings]>[!UICONTROL Account]** und sehen Sie sich die Menge an [!UICONTROL Usable Funds]. Wenn Sie weitere Mittel benötigen, wenden Sie sich an Ihren [!DNL Adobe] Account-Team. |
|  | Es ist kein Inventar verfügbar. | Überprüfen Sie, ob die angegebenen Inventarquellen ([!UICONTROL Public], [!UICONTROL Private]oder [!UICONTROL On Demand]) sind:<ul><li>Richtig einrichten.</li><li>Aktiv und Versand durch Auktionen.</li><li>Kompatibel mit dem entsprechenden Anzeigen- und Platzierungstyp.</li></ul><br>Wenn alle Inventarquellen gültig und aktiv sind, sollten Sie nach Möglichkeit zusätzliche oder alle Inventarquellen ansprechen. |
|  | Es sind keine Benutzer verfügbar. | Vergewissern Sie sich, dass die angegebenen Zielgruppen genügend aktive Benutzer enthalten. Wenn nicht, erweitern Sie die Ziele, indem Sie weitere Zielgruppen hinzufügen. |
| Geringe Ausgaben für Platzierung | Die [!UICONTROL Non Bids] im Abschnitt zur Platzierungsdiagnose werden mögliche Gründe angezeigt, aus denen die Platzierung kein Angebot abgegeben hat. | [Überprüfen Sie die [!UICONTROL Non Bids] Bericht](/help/dsp/campaign-management/reports/placement-diagnostics.md) , um zu verstehen, warum die Platzierung nicht geboten hat.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | Die Platzierung verwendet [Vorab-Angebotsfilter](/help/dsp/campaign-management/placements/placement-settings.md) die Gebotsbeschränkung. | Verringern Sie die Schwellenwerte für Filter vor dem Angebot um 5 %, um das Gleichgewicht von Ausgaben und Leistung zu beurteilen. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Filter vor dem Gebot, Geos, Bestand und Zielgruppen, Gebote und Ausgaben kumulativ einschränken kann. |
|  | Die Platzierung hat eine niedrige Gewinnrate. | Erhöhen Sie die [!UICONTROL Max Bid] um die Gewinnrate zu erhöhen.<br><br><b>HINWEIS:</b> Die Lagerpreise variieren je nach Targeting der Platzierung.<br><br>Eine Gewinnquote von 10 % gilt als gesund. |
|  | Es ist nur eine geringe Anzahl von Beständen verfügbar. | Richten Sie nach Möglichkeit zusätzliche oder alle Inventarquellen ein.<br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Filter vor dem Gebot, Geos, Bestand und Zielgruppen, Gebote und Ausgaben kumulativ einschränken kann. |
|  | Es ist nur eine geringe Anzahl von Benutzern verfügbar. | Vergewissern Sie sich, dass die angegebenen Zielgruppen genügend aktive Benutzer enthalten. Wenn nicht, erweitern Sie die Ziele, indem Sie weitere Zielgruppen hinzufügen.<br><br>Beachten Sie, dass die Verwendung mehrerer Platzierungsziele, wie z. B. Filter vor dem Gebot, Geos, Bestand und Zielgruppen, Gebote und Ausgaben kumulativ einschränken kann. |
|  | Das Paket enthält eine große Anzahl aktiver Platzierungen. | Reduzieren Sie entweder die Anzahl der aktiven Platzierungen innerhalb des Pakets oder erhöhen Sie das Gesamtbudget des Pakets.<br><br>Wenn das Paket viele Platzierungen, aber nicht genügend Budget enthält, können DSP möglicherweise nicht genügend Budget für jede Platzierung zuweisen. Jede Platzierung sollte die Möglichkeit haben, mindestens 2 USD pro Tag zu verbringen. Wenn Ihr Paket beispielsweise ein Budget von 10 USD/Tag hat, sollten Sie am besten fünf oder weniger Platzierungen einbeziehen. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)

