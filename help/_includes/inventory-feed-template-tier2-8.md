---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Ebene 2: Tier 8-Felder in Shopping-Anzeigenvorlagen

**[!UICONTROL Tier  2 - Tier 8]:** (Wenn Sie Produktgruppen-Stufen hinzufügen) Ein Produktattributtyp, nach dem Produkte ausgewählt werden sollen, sowie die Qualifizierungskriterien für den ausgewählten Attributtyp (z. B. Brand=Acme oder Condition=New). Die Werte werden hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wählen Sie einen Attributtyp aus und geben Sie die Qualifikationskriterien ein. Folgende Zeichen sind verboten: `[ ] < > >>` (zwei aufeinander folgende &quot;Größer als&quot;-Zeichen), mit denen Spaltennamen in der Vorlage bestimmt werden, Modifikatornamen in der Vorlage und Tier-Trennzeichen in der Spalte [!UICONTROL Parent Product Grouping] in Bulksheets.

Sie können bis zu acht Stufen (Ebenen) von Produktgruppen einbeziehen, darunter &quot;[!UICONTROL All Products]&quot;(Ebene 1). Jede Ebene kann mehrere Produktgruppen enthalten, sie muss jedoch denselben Attributtyp aufweisen (z. B. &quot;Bedingung&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] only) Die möglichen Werte für [!UICONTROL Channel] sind &quot;[!UICONTROL Local]&quot; oder &quot;[!UICONTROL Online]&quot; und die möglichen Werte für [!UICONTROL ChannelExclusivity] sind &quot;[!UICONTROL SingleChannel]&quot; und &quot;[!UICONTROL MultiChannel]&quot;.
>* Wenn Sie eine zweite (untergeordnete) Produktgruppe für eine Anzeigengruppe über die Registerkarte [!UICONTROL Product Groups] in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] erstellen, wird automatisch eine weitere Produktgruppe mit der Bezeichnung &quot;[!UICONTROL Everything Else]&quot; mit dem standardmäßigen Anzeigengruppenangebot erstellt. Bei Verwendung von Inventar-Feed-Vorlagen sind jedoch &quot;[!UICONTROL Everything Else]&quot;-Produktgruppen ausgeschlossen.
>* Wenn Sie mehrere Ebenen einschließen und für die letzte (höchst nummerierte) Ebene kein Wert verfügbar ist, wird die nächsthöhere Ebene als bidbare Produktgruppe verwendet. Wenn Sie z. B. fünf Stufen einschließen und für Ebene 5 kein Wert verfügbar ist, wird Ebene 4 als bidable Produktgruppe (Einheit) verwendet. Wenn jedoch für eine mittlere Ebene kein Wert verfügbar ist, wird die Zeile ignoriert. Wenn Sie beispielsweise fünf Ebenen angeben und Ebene 5 einen Wert hat, Ebene 4 jedoch nicht, wird Zeile 4 ignoriert.
