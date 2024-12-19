---
title: Generieren eines [!DNL Advertising Insight]
description: Erfahren Sie, wie Sie eine  [!DNL Advertising Insight] erstellen.
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Generieren eines [!DNL Advertising Insight]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Klicken Sie auf den Einblick, den Sie generieren möchten.

3. Geben Sie die Insight-Einstellungen an:

   1. (Einige Berichte; optional) Geben Sie die Datumsbereiche für die Einblicke an.

   2. (Die meisten Erkenntnisse) Wählen Sie das zu analysierende Portfolio aus.

      Im Allgemeinen sind alle optimierten und aktiven Portfolios verfügbar, die aktive Kampagnen enthalten. Für einige Einblicke können Sie die Portfolioliste so filtern, dass sie **[!UICONTROL Only Optimized Portfolios]** enthält.

      Für [!UICONTROL Day of Week] Einblicke sind nur Portfolios verfügbar, die ausreichend Ausgaben aufweisen und die in den letzten zwei Tagen auch für Target ausgegeben wurden.

   3. (Nur [!UICONTROL Event Path Beta]) Führen Sie die folgenden Schritte aus:

      1. Wählen Sie die **[!UICONTROL Operation]** aus: *[!UICONTROL Extract events]* (zum Hochladen eines [!UICONTROL Channel Assist Report] oder einer [!UICONTROL Campaign Assist Report] und Klassifizieren der Benutzerereignisse in verschiedene Gruppen für die Analyse) oder *[!UICONTROL Analyze classified events]* (zum Hochladen von Ereignisgruppen und deren Verwendung zum Generieren der Erkenntnisse).

      1. Klicken Sie auf **[!UICONTROL Select]** , um eine Datei im XLSX- und ZIP-Format (komprimiertes XLSX-Format) zu suchen, und klicken Sie dann auf **[!UICONTROL Upload]**.

   4. (Nur [!UICONTROL Google Account Audit]) Führen Sie die folgenden Schritte aus:

      1. Geben Sie den **[!UICONTROL Advertiser Name]** und die **[!UICONTROL Account Name]** ein.

      1. Wählen Sie die **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* oder *[!UICONTROL United Kingdom]*) und die **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* oder *[!UICONTROL German]*) aus.

      1. Klicken Sie auf **[!UICONTROL Select]** , um die Kampagnen-, Keyword- und Änderungsverlaufsberichte zu suchen, die für das Konto von der [!DNL Google Ads]-Web-Benutzeroberfläche heruntergeladen wurden, sowie auf eine Bulksheet-Datei, die für das Konto von der [!DNL Google Ads Editor] heruntergeladen wurde. Klicken Sie dann auf **[!UICONTROL Upload]**.

         Alle Dateien müssen im CSV-, TSV-, TXT- oder ZIP-Format (komprimierte CSV-, TSV- oder TXT) vorliegen.

   5. (Nur [!UICONTROL Location Target Performance]; optional) Um die Daten täglich und nicht als Zusammenfassung zu aggregieren, wählen Sie die **[!UICONTROL Time Aggregation]** der *[!UICONTROL Daily]* aus.

   6. (Nur [!UICONTROL Normalized Sim (Combined)]) Führen Sie die folgenden Schritte aus:

      1. Geben Sie im Feld **[!UICONTROL Step]** die Anzahl der Zielausgabenebenen oder -schritte an, die in die Einblicke aufgenommen werden sollen. Der Wert kann zwischen drei (3) und 100 liegen.

      1. Wählen Sie im Feld **[!UICONTROL Type]** den Simulationstyp aus:

         * *[!UICONTROL Optimized Multi-portfolio]*: Erzeugt eine einzige Simulation über mehrere Portfolios mit demselben Ziel und derselben Währung.

         * *[!UICONTROL Individual Normalized]*: Erzeugt eine individuelle Simulation für jedes ausgewählte Portfolio. Die Portfolios können unterschiedliche Ziele und Währungen haben.

   7. (Nur [!UICONTROL Portfolio Launch] Einblick; optional) Um ein Launch-Datum in der Zukunft anzugeben, geben Sie ein Datum im Feld **[!UICONTROL Optional Date]** an.

   8. (Nur [!UICONTROL Quality Score]) Wählen Sie das entsprechende Werbenetzwerk aus.

   9. (Nur [!UICONTROL Query Cross Matching]) Wählen Sie im Menü **[!UICONTROL Google Accounts]** das -Konto aus.

4. Klicken Sie auf **[!UICONTROL Generate Insight]**.

   Sie erhalten eine Benachrichtigung, wenn der Auftrag abgeschlossen wurde oder fehlschlägt, basierend auf Ihren [ Benachrichtigungseinstellungen ](/help/search-social-commerce/notifications/notification-edit.md) der [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Über [!UICONTROL Advertising Insights]](insight-about.md)
>* [Anzeigen oder Speichern eines  [!DNL Advertising Insight]](insight-view-save.md)
>* [Löschen eines [!DNL Advertising Insight]](insight-delete.md)
