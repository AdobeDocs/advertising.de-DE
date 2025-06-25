---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Ebene 2 - Ebene 8-Felder in Shopping-Anzeigenvorlagen

**[!UICONTROL Tier  2 - Tier 8]:** (Wenn Sie Ebenen von Produktgruppen hinzufügen) Ein Produktattributtyp, mit dem Produkte ausgewählt werden, und die Kriterien für den ausgewählten Attributtyp (z. B. Brand=Acme oder Condition=New). Die Werte werden hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wählen Sie einen Attributtyp aus und geben Sie die Qualifizierungskriterien ein. Unzulässige Zeichen sind unter anderem: `[ ] < > >>` (zwei aufeinander folgende „größer als“-Zeichen), mit denen Spaltennamen in der Vorlage angegeben werden, Modifikatornamen in der Vorlage und Ebenentrennzeichen in der [!UICONTROL Parent Product Grouping] in Bulksheets.

Sie können bis zu acht Ebenen (Ebenen) von Produktgruppen einbeziehen, einschließlich &quot;[!UICONTROL All Products]&quot; (Ebene 1). Jede Ebene kann mehrere Produktgruppen enthalten, sie müssen sich jedoch auf denselben Attributtyp beziehen (z. B. „Bedingung„).

>[!NOTE]
>
>* (Nur [!DNL Google Ads]) Die möglichen Werte für [!UICONTROL Channel] sind &quot;[!UICONTROL Local]&quot; oder &quot;[!UICONTROL Online]&quot;, und die möglichen Werte für [!UICONTROL ChannelExclusivity] sind &quot;[!UICONTROL SingleChannel]&quot; und &quot;[!UICONTROL MultiChannel]&quot;.
>* Wenn Sie eine zweite (untergeordnete) Produktgruppe für eine Anzeigengruppe auf der Registerkarte [!UICONTROL Product Groups] in der Ansicht [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] erstellen, wird automatisch eine andere Produktgruppe namens &quot;[!UICONTROL Everything Else]&quot; mit dem Standardgebot für die Anzeigengruppe erstellt. Bei Verwendung von Inventar-Feed-Vorlagen sind jedoch &quot;[!UICONTROL Everything Else]&quot; Produktgruppen ausgeschlossen.
>* Wenn Sie mehrere Ebenen einbeziehen und für die endgültige (höchste) Ebene kein Wert verfügbar ist, wird die nächsthöhere Ebene als bidable-Produktgruppe verwendet. Beispiel: Wenn Sie fünf Ebenen einbeziehen und für Ebene 5 kein Wert verfügbar ist, wird Ebene 4 als bidable Produktgruppe (Einheit) verwendet. Wenn jedoch kein Wert für eine mittlere Ebene verfügbar ist, wird die Zeile ignoriert. Beispiel: Wenn Sie fünf Ebenen berücksichtigen und Ebene 5 einen Wert hat, Ebene 4 jedoch nicht, wird Zeile 4 ignoriert.
