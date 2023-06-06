---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Beschriftungsklassifizierungen

**\[Komponente\] [!UICONTROL Label Classifications] > \[Beschriftungsklassifizierung und Wert\]:** (Optional) Werte für bis zu fünf vorhandene Bezeichnungsklassifizierungen, die den verschiedenen Kampagnenkomponenten zugewiesen werden, die mit der Vorlage erstellt oder bearbeitet werden. Beschriftungswerte werden von untergeordneten Entitäten vererbt (einschließlich untergeordneten Entitäten, die später erstellt werden). Daher müssen Sie keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die vererbten Werte überschreiben. Beschriftungsklassifizierungen für Produktgruppen werden auf die Einheitenebene (am detailliertesten) angewendet.

Für jede Kampagnenkomponente, der Sie Beschriftungsklassifizierungen zuweisen möchten:

1. Klicken Sie auf das Kontrollkästchen neben **\[Komponente\][!UICONTROL Label Classifications]**.

1. Konfigurieren Sie die Titel-Classification-Werte für die Vorlage:

   * Führen Sie für jede Beschriftungsklassifizierung und jeden Wert, der der Komponente zugewiesen werden soll, folgende Schritte aus:

      1. Klicken **[!UICONTROL Add Label Classification]**.

      1. Wählen Sie die vorhandene Beschriftungs-Classification aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

         Die maximale Länge pro Wert beträgt 100 Zeichen. Sie kann ASCII- und Nicht-ASCII-Zeichen enthalten.

         Um einen Spaltennamen als dynamischen Parameter für einen Beschriftungs-Classification-Wert einzufügen, klicken Sie in das Eingabefeld (das zweite Feld) und dann auf einen Spaltennamen in der Spaltenliste.

         Sie können pro Kampagnenkomponente nur einen Wert pro Classification einbeziehen. Eine Kampagne kann beispielsweise &quot;Color=Red&quot;haben, jedoch nicht &quot;Color=Red&quot;und &quot;Color=Blue&quot;.
   * Um einen vorhandenen Beschriftungs-Classification-Wert zu ändern, wählen Sie einen neuen Wert aus oder geben Sie einen neuen ein.

   * Um einen vorhandenen Beschriftungs-Classification-Wert zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Wert.
