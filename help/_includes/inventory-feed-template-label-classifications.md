---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---
# Text und Vorlage - Label Classifications

**\[Komponente\] [!UICONTROL Label Classifications] > \[Kennzeichnungsklassifizierung und -wert\]:** (Optional) Werte für bis zu fünf vorhandene Kennzeichnungsklassifizierungen, die den verschiedenen Kampagnenkomponenten zugewiesen werden sollen, die mithilfe der Vorlage erstellt oder bearbeitet werden. Beschriftungswerte werden von untergeordneten Entitäten übernommen (einschließlich später erstellter untergeordneter Entitäten). Daher müssen Sie keine Werte für untergeordnete Entitäten eingeben, es sei denn, Sie möchten die übernommenen Werte überschreiben. Kennzeichnungsklassifizierungen für Produktgruppen werden auf die Ebene der Einheit (mit der höchsten Granularität) angewendet.

Für jede Kampagnenkomponente, der Sie Kennzeichnungsklassifizierungen zuweisen möchten:

1. Aktivieren Sie das Kontrollkästchen neben **\[Komponente\][!UICONTROL Label Classifications]**.

1. Konfigurieren Sie die Klassifizierungswerte für die Kennzeichnung für die Vorlage:

   * Gehen Sie für jede Kennzeichnungsklassifizierung und jeden Wert, der der Komponente zugewiesen werden soll, wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Add Label Classification]**.

      1. Wählen Sie die vorhandene Kennzeichnungsklassifizierung aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

         Die maximale Länge für jeden Wert beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

         Um einen Spaltennamen als dynamischen Parameter für einen Beschriftungsklassifizierungswert einzufügen, klicken Sie auf das Eingabefeld (das zweite Feld) und dann auf einen Spaltennamen in der Spaltenliste.

         Pro Kampagnenkomponente kann nur ein Wert enthalten sein. Beispielsweise kann eine Kampagne „Farbe=Rot“, aber nicht „Farbe=Rot“ und „Farbe=Blau“ haben.

   * Um einen vorhandenen Kennzeichnungswert zu ändern, wählen Sie einen neuen Wert aus oder geben Sie ihn ein.

   * Um einen vorhandenen Kennzeichnungswert zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Wert.
