---
title: Erstellen eines einfachen Berichts oder erweiterten Berichts
description: Erfahren Sie, wie Sie einen benutzerdefinierten einfachen oder erweiterten Bericht erstellen.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Erstellen eines einfachen Berichts oder erweiterten Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Report]**, halten Sie den Cursor über **[!UICONTROL Basic Reports]** oder **[!UICONTROL Advanced Reports]** und klicken Sie dann auf den Berichtstyp [4}.](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)

1. (Optional) Ändern Sie im Fenster [!UICONTROL Report Settings] die standardmäßigen [Berichtseinstellungen](basic-advanced-report-settings.md):

   1. (Optional) Geben Sie einen benutzerdefinierten Namen für den Bericht und die Vorlage ein (wenn Sie den Bericht als Vorlage speichern).

   1. (Optional) Um die Berichtseinstellungen als Vorlage zu speichern, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Save as template]**.

   1. (Optional) Wählen Sie auf der Registerkarte **[!UICONTROL Basic Settings]** eine vorhandene Berichtsvorlage aus, um die Standardeinstellungen für den Bericht zu verwenden oder zu ändern.

   1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Columns tab]**&quot;und ändern Sie die Standardspalten im Bericht.

      Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im richtigen Währungsformat anzuzeigen (jedoch ohne Währungssymbole im CSV- und TSV-Format), fügen Sie die Spalte &quot;[!UICONTROL Currency]&quot; zum Bericht hinzu. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, sind beliebige &quot;[!UICONTROL Total]&quot;-Geldwerte die Summe aller Zahlen in der Spalte, unabhängig von der Währung.

   1. (Optional; nur [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] und [!UICONTROL Label Classification Report]) Klicken Sie auf die Registerkarte **[!UICONTROL Classifications]** und begrenzen Sie die Berichtsergebnisse, sodass nur bestimmte Beschriftungsklassifizierungen enthalten sind.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Advanced Filters]** und ändern Sie die erweiterten Standardoptionen.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Attribution]** und ändern Sie die standardmäßige Zuordnungsregel.

   1. (Optional) Klicken Sie auf den Tab **[!UICONTROL Scheduling and Delivery]** und ändern Sie die standardmäßigen Zeitplan- und Bereitstellungsoptionen.

1. (Optional, sofern verfügbar) Klicken Sie auf &quot;**[!UICONTROL Preview]**&quot;, um eine Vorschau der ersten 50 Zeilen des Berichts anzuzeigen. Klicken Sie abschließend auf **[!UICONTROL Back]** , um zur Seite mit den Berichtseinstellungen zurückzukehren.

   >[!NOTE]
   >
   >Die Vorschau -Schaltfläche ist für alle einfachen und erweiterten Berichte mit Ausnahme der [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] und [!UICONTROL Transaction Report] verfügbar.

1. Klicken Sie auf **[!UICONTROL Create]**.

Wenn Sie keinen Berichtsplan festgelegt haben, wird der Bericht sofort ausgeführt. Andernfalls wird er gemäß dem festgelegten Zeitplan ausgeführt. Der Berichtsname wird der [[!UICONTROL Latest Reports] Ansicht](/help/search-social-commerce/reports/report-about.md) hinzugefügt. Wenn Sie den Bericht als Vorlage gespeichert haben, wird er auch zur [[!UICONTROL Templates] Ansicht](/help/search-social-commerce/reports/report-about.md) hinzugefügt. Wenn der Bericht abgeschlossen ist, kann die Datei geöffnet oder gespeichert werden. Vorlagen sind sofort verfügbar.

Wenn Sie E-Mail-Adressen zur Benachrichtigung eingegeben haben, erhält jeder Empfänger eine Benachrichtigung, wenn der Berichtsauftrag abgeschlossen ist oder fehlschlägt. Dies basiert auf den [konfigurierten Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md) des Benutzers für Berichte.

>[!MORELIKETHIS]
>
>* [Über grundlegende und erweiterte Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Grundlegende und erweiterte Berichtseinstellungen](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Berichtsspalten für grundlegende und erweiterte Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Berichte löschen](/help/search-social-commerce/reports/management/report-delete.md)
