---
title: Generieren eines einfachen Berichts oder erweiterten Berichts
description: Erfahren Sie, wie Sie einen benutzerdefinierten Basis- oder erweiterten Bericht erstellen.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Generieren eines einfachen Berichts oder erweiterten Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** oder **[!UICONTROL Advanced Reports]** und klicken Sie dann auf [Berichtstyp](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Optional) Ändern Sie im [!UICONTROL Report Settings] die Standardeinstellungen [Berichteinstellungen](basic-advanced-report-settings.md):

   1. (Optional) Geben Sie einen benutzerdefinierten Namen für den Bericht und für die Vorlage ein (wenn Sie den Bericht als Vorlage speichern).

   1. (Optional) Um die Berichtseinstellungen als Vorlage zu speichern, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Save as template]**.

   1. (Optional) Wählen Sie auf der Registerkarte **[!UICONTROL Basic Settings]** eine vorhandene Berichtsvorlage aus, um die standardmäßigen Grundeinstellungen für den Bericht zu verwenden oder zu ändern.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Columns tab]** und ändern Sie die Standardspalten im Bericht.

      Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im richtigen Währungsformat (aber ohne Währungssymbole im CSV- und TSV-Format) anzuzeigen, fügen Sie dem Bericht die Spalte &quot;[!UICONTROL Currency]&quot; hinzu. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, sind alle &quot;[!UICONTROL Total]&quot; Geldwerte die Summe aller Zahlen in der Spalte, unabhängig von der Währung.

   1. (Optional, nur [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] und [!UICONTROL Label Classification Report]) Klicken Sie auf die Registerkarte **[!UICONTROL Classifications]** und beschränken Sie die Berichtsergebnisse auf bestimmte Kennzeichnungsklassifizierungen.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Advanced Filters]** und ändern Sie die erweiterten Standardoptionen.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Attribution]** und ändern Sie die standardmäßige Zuordnungsregel.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Scheduling and Delivery]** und ändern Sie die standardmäßigen Zeitplan- und Versandoptionen.

1. (Optional, falls verfügbar) Klicken Sie auf &quot;**[!UICONTROL Preview]**&quot;, um eine Vorschau für die ersten 50 Zeilen des Berichts anzuzeigen. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Back]** , um zur Seite mit den Berichtseinstellungen zurückzukehren.

   >[!NOTE]
   >
   >Die Schaltfläche Vorschau ist für alle grundlegenden und erweiterten Berichte verfügbar, mit Ausnahme der Berichte [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] und [!UICONTROL Transaction Report].

1. Klicken Sie auf **[!UICONTROL Create]**.

Wenn Sie keinen Berichtszeitplan angegeben haben, wird der Bericht sofort ausgeführt. Andernfalls wird er gemäß dem angegebenen Zeitplan ausgeführt. Der Berichtsname wird der [[!UICONTROL Latest Reports] hinzugefügt](/help/search-social-commerce/reports/report-about.md). Wenn Sie den Bericht als Vorlage gespeichert haben, wird er auch der [[!UICONTROL Templates] hinzugefügt](/help/search-social-commerce/reports/report-about.md). Nach Fertigstellung des Berichts kann die Datei geöffnet oder gespeichert werden. Vorlagen sind sofort verfügbar.

Wenn Sie E-Mail-Adressen zur Benachrichtigung eingegeben haben, erhält jeder Empfänger eine Benachrichtigung, wenn der Berichtsvorgang abgeschlossen wurde oder fehlschlägt, basierend auf den [konfigurierten Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md) für Berichte.

>[!MORELIKETHIS]
>
>* [Über grundlegende und erweiterte Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Allgemeine und erweiterte Berichtseinstellungen](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Berichtsspalten für einfache und erweiterte Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Berichte löschen](/help/search-social-commerce/reports/management/report-delete.md)
