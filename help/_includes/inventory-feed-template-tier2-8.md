---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Ebene 2: Tier 8-Felder in Shopping-Anzeigenvorlagen

**[!UICONTROL Tier  2 - Tier 8]:** (Wenn Sie Produktgruppen-Stufen hinzufügen) Ein Produktattributtyp, nach dem Produkte ausgewählt werden sollen, sowie die Qualifizierungskriterien für den ausgewählten Attributtyp (z. B. Brand=Acme oder Condition=New). Die Werte werden hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wählen Sie einen Attributtyp aus und geben Sie die Qualifikationskriterien ein. Folgende Zeichen sind verboten: `[ ] < > >>` (zwei aufeinander folgende &quot;Größer als&quot;-Zeichen), die verwendet werden, um Spaltennamen in der Vorlage, Modifikatornamen in der Vorlage und Tier-Trennzeichen in der [!UICONTROL Parent Product Grouping] in Bulksheets.

Sie können bis zu acht Stufen (Ebenen) von Produktgruppen einbeziehen, darunter &quot;[!UICONTROL All Products]&quot; (Ebene 1). Jede Ebene kann mehrere Produktgruppen enthalten, sie muss jedoch denselben Attributtyp aufweisen (z. B. &quot;Bedingung&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] nur) Die möglichen Werte für [!UICONTROL Channel] are &quot;[!UICONTROL Local]&quot; oder &quot;[!UICONTROL Online],&quot;und die möglichen Werte für [!UICONTROL ChannelExclusivity] are &quot;[!UICONTROL SingleChannel]&quot; und &quot;[!UICONTROL MultiChannel].&quot;
>* Wenn Sie eine zweite (untergeordnete) Produktgruppe für eine Anzeigengruppe aus der [!UICONTROL Product Groups] im [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] Ansicht, eine andere Produktgruppe namens[!UICONTROL Everything Else],&quot;wird automatisch mit dem standardmäßigen Anzeigengruppenangebot erstellt. Verwenden von Inventar-Feed-Vorlagen jedoch &quot;[!UICONTROL Everything Else]&quot;Produktgruppen sind ausgeschlossen.
>* Wenn Sie mehrere Ebenen einschließen und für die letzte (höchst nummerierte) Ebene kein Wert verfügbar ist, wird die nächsthöhere Ebene als bidbare Produktgruppe verwendet. Wenn Sie z. B. fünf Stufen einschließen und für Ebene 5 kein Wert verfügbar ist, wird Ebene 4 als bidable Produktgruppe (Einheit) verwendet. Wenn jedoch für eine mittlere Ebene kein Wert verfügbar ist, wird die Zeile ignoriert. Wenn Sie beispielsweise fünf Ebenen angeben und Ebene 5 einen Wert hat, Ebene 4 jedoch nicht, wird Zeile 4 ignoriert.

