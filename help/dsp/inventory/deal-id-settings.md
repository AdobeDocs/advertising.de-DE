---
title: Manuelle Deal-ID-Einstellungen
description: Siehe Beschreibungen der Einstellungen für manuell eingegebene Angebots-IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Manuelle Deal-ID-Einstellungen

| Abschnitt | Parameter | Beschreibung | Erforderlich | Bearbeitbar |
|---------|-----------|-------------|----------|----------|
| [Details des Angebots] | [!UICONTROL Deal name] | Der Name, der Ihre [!UICONTROL Deal ID] in Advertising DSP angibt. Geben Sie einen Namen ein oder wählen Sie **[!UICONTROL Auto-name]** aus, damit DSP einen Namen basierend auf den Details des Deals generieren kann.<br><br>Beispiel eines automatisch generierten Namens: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
| | [!UICONTROL External deal ID] | Die von Ihrem Herausgeber und der SSP verwendete ID zur Identifizierung dieses Geschäfts. | Ja | Nein |
| | [!UICONTROL Publisher] | Der Name des Herausgebers, der diesen Bestand verkauft. | Ja | Nein |
| | [!UICONTROL SSP] | Die angebotsseitige Plattform (Supply Side Platform, SSP), über die diese Transaktion läuft. | Ja | Nein |
| | [!UICONTROL Media type] | Der Medientyp, der durch diesen Deal gekauft wurde: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* oder *[!UICONTROL Publisher Managed]*. Die Optionen variieren je nach SSP.<br><br> Wenn das Geschäft mehrere Medientypen zulässt, wählen Sie beim Erstellen des Geschäfts den Medientyp für die Standardplatzierung aus. Später können Sie den Wert ändern oder einfach [eine neue Platzierung mit dem zusätzlichen Medientyp ](deal-id-attach-placements.md) anhängen.<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nein |
| | [!UICONTROL Deal type] | Die Deal-Zusage und die Preisstruktur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Sie und der Herausgeber haben sich nicht an eine feste Anzahl von Impressions-Sendungen gebunden. In der Vereinbarung wird der Mindestpreis für das Inventar festgelegt, obwohl der CPM je nach Marktbedingungen schwanken und steigen kann.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Sie und der Herausgeber haben sich nicht an eine feste Anzahl von Impressions-Sendungen gebunden. Die Preisfestsetzung erfolgt zu einem vereinbarten Festpreis.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Sie und der Herausgeber haben eine vordefinierte Anzahl von Impressionen, Targeting, Flugdaten und Festpreisen vereinbart.<br><br><b>Hinweis: </b> Für garantierte Angebote sind Flugdaten und eine bestimmte Anzahl von Impressionen im Abschnitt [!UICONTROL Tracking] erforderlich. Sie müssen außerdem eine standardmäßige Platzierung mit programmgesteuerter Garantie (PG) für den Deal erstellen, und Sie können den Deal optional für andere Platzierungen verwenden.</li></ul> | Ja | Nein |
| | [!UICONTROL CPM] | Die ausgehandelten Kosten pro 1000 Impressionen (CPM). | Ja | Ja |
| | [Währung] | Die Währung für das Geschäft.<br><br>Alle SSPs akzeptieren Geschäfte in USD. Wenn der SSP die Währung für Ihr DSP-Konto akzeptiert, ist diese Währung ebenfalls verfügbar. | Ja | Nein |
| | [!UICONTROL Billing method] | Alle Deal-IDs werden durch [!DNL Adobe] finanziert und -fakturiert. DSP zahlt alle verfügbaren Medienanbieter basierend auf der Nutzung, verwaltet Diskrepanzen mit den Anbietern und sendet eine konsolidierte Rechnung an das Konto. Für diese Option fallen zusätzliche Gebühren an, wie auf der Kreditkarte des Kontos angegeben. | Ja | Nein |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Die E-Mail-Adresse für das Benutzerkonto, das auf den Deal zugreifen kann. | Nein | Ja |
| | [!UICONTROL Advertisers that can access this deal] | Die spezifischen Advertiser im Konto, die auf diesen Deal zugreifen können.<br><br><b>Hinweis:</b> Sie können den Deal für Advertiser in zusätzlichen Konten über die Ansicht [!UICONTROL Deals] freigeben. Klicken Sie in der Zeile &quot;Deal&quot;auf **[!UICONTROL #]**, klicken Sie auf **[!UICONTROL share]** und geben Sie dann den Deal für eine E-Mail-Adresse frei. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Die Start- und Enddaten für Traffic, der diesen Deal verwendet. Diese Daten dienen nur zu Tracking-Zwecken und wirken sich nicht auf die Anzeigenbereitstellung aus.<br><br><b>Tipp:</b> In der Ansicht [!UICONTROL Inventory] > [!UICONTROL Deals] zeigt die Spalte [!UICONTROL Pacing & Budget] an, wie der Deal zum festgelegten Flugdatum und Impressionsziel gelangt. Wenn der Versand zu kurz oder zu schnell verläuft, wenden Sie sich an Ihren Herausgeber, um die Menge anzupassen, die durch den Deal gesendet wird. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: nein | Ja |
| | [!UICONTROL Impressions] | (Optional für nicht garantierte Angebote) Die geschätzte Anzahl der Impressionen, die Sie mit diesem Deal erwarten. Dieser Wert dient nur zu Tracking-Zwecken. Der Herausgeber steuert die Anzeigenbereitstellung. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: nein | Ja |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Über den privaten Bestand](private-inventory-about.md)
