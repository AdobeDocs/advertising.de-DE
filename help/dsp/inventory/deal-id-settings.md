---
title: Manuelle Deal ID-Einstellungen
description: Siehe Beschreibungen der Einstellungen für manuell eingegebene Angebots-IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Manuelle Deal ID-Einstellungen

| Abschnitt | Parameter | Beschreibung | Erforderlich | Bearbeitbar |
|---------|-----------|-------------|----------|----------|
| [Angebotsdetails] | [!UICONTROL Deal name] | Der Name zur Identifizierung Ihres [!UICONTROL Deal ID] in Advertising DSP. Geben Sie einen Namen ein oder wählen Sie **[!UICONTROL Auto-name]** aus, damit DSP einen Namen basierend auf den Abschlussdetails generieren kann.<br><br>Beispiel für einen automatisch generierten Namen: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
| | [!UICONTROL External deal ID] | Die ID, die von Ihrem Publisher und dem SSP zur Identifizierung dieses Deals verwendet wird. | Ja | Nein |
| | [!UICONTROL Publisher] | Der Name des Herausgebers, der dieses Inventar verkauft. | Ja | Nein |
| | [!UICONTROL SSP] | Die anbieterseitige Plattform (SSP), über die dieses Geschäft läuft. | Ja | Nein |
| | [!UICONTROL Media type] | Die Art der Medien, die durch diesen Deal gekauft wurden: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* oder *[!UICONTROL Publisher Managed]*. Die Optionen variieren je nach SSP.<br><br> Wenn der Deal mehrere Medientypen zulässt, wählen Sie beim Erstellen des Deals den Medientyp für die Standardplatzierung aus. Später können Sie den Wert ändern oder einfach [eine neue Platzierung mit dem zusätzlichen Medientyp anhängen](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nein |
| | [!UICONTROL Deal type] | Die Verpflichtungs- und Preisstruktur des Geschäfts:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Sie und der Publisher haben sich nicht auf eine feste Anzahl von Impression-Sendungen festgelegt. Der Deal legt den Mindestpreis für den Bestand fest, obwohl der CPM je nach Marktbedingungen schwanken und steigen kann.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Sie und der Publisher haben sich nicht auf eine feste Anzahl von Impression-Sendungen festgelegt. Die Preise werden zu einem festen ausgehandelten Satz festgelegt.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Sie und der Publisher haben sich auf eine vordefinierte Anzahl von Impressionen, Zielgruppenbestimmung, Flugdaten und Festpreis geeinigt.<br><br><b>Hinweis</b> Für garantierte -Angebote sind die Flugdaten und eine bestimmte Anzahl von Impressionen im Abschnitt [!UICONTROL Tracking] erforderlich. Sie müssen auch eine standardmäßige programmgesteuert garantierte Platzierung (PG) für den Abschluss erstellen, und Sie können den Abschluss stattdessen auch für andere Platzierungen verwenden.</li></ul> | Ja | Nein |
| | [!UICONTROL CPM] | Die ausgehandelten Kosten pro 1000 Aufrufe (CPM). | Ja | Ja |
| | [Währung] | Die Währung für den Deal.<br><br>Alle SSPs akzeptieren Angebote in USD. Wenn der SSP die Währung für Ihr DSP-Konto akzeptiert, ist diese Währung ebenfalls verfügbar. | Ja | Nein |
| | [!UICONTROL Billing method] | Alle Angebots-IDs werden [!DNL Adobe] finanziert und fakturiert. DSP bezahlt alle verfügbaren Medienanbieter auf Nutzungsbasis, verwaltet Abweichungen von den Anbietern und sendet eine konsolidierte Rechnung an das Konto. Für diese Option fallen zusätzliche Gebühren an, wie auf der Tarifkarte des Kontos angegeben. | Ja | Nein |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Die E-Mail-Adresse für das Benutzerkonto, das auf das Angebot zugreifen kann. | Nein | Ja |
| | [!UICONTROL Advertisers that can access this deal] | Die spezifischen Advertiser im Konto, die auf dieses Angebot zugreifen können.<br><br><b>Hinweis:</b> Sie können den Deal für Werbetreibende in zusätzlichen Konten über die [!UICONTROL Deals] freigeben. Klicken Sie in der Angebotszeile auf **[!UICONTROL #]**, klicken Sie auf **[!UICONTROL share]** und geben Sie das Angebot dann für eine E-Mail-Adresse frei. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Das Start- und Enddatum für Traffic, der dieses Angebot verwendet. Diese Daten dienen nur zur Nachverfolgung und wirken sich nicht auf den Versand von Anzeigen aus.<br><br><b>Tipp:</b> In der Ansicht [!UICONTROL Inventory] > [!UICONTROL Deals] wird in der Spalte [!UICONTROL Pacing & Budget] angezeigt, wie sich das Angebot dem angegebenen Flugdatum und Impressionsziel entwickelt. Wenn der Versand zu langsam oder zu schnell erfolgt, wenden Sie sich an Ihren Publisher, um anzupassen, wie viel Volumen er über den Abschluss sendet. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |
| | [!UICONTROL Impressions] | (Optional für nicht garantierte Angebote) Die geschätzte Anzahl von Impressions, die Sie mit diesem Angebot erwarten. Dieser Wert dient nur zu Tracking-Zwecken. Der Herausgeber steuert die Bereitstellung und den Versand. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Details zur Angebots-ID manuell erstellen](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Über den privaten Bestand](private-inventory-about.md)
