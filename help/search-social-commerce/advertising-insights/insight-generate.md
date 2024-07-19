---
title: Generieren von  [!DNL Advertising Insight]
description: Erfahren Sie, wie Sie einen [!DNL Advertising Insight] erstellen.
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Generieren eines [!DNL Advertising Insight]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Klicken Sie auf den zu erzeugenden Einblick.

3. Geben Sie die Insight-Einstellungen an:

   1. (Einige Berichte; optional) Geben Sie die Datumsbereiche für den Einblick an.

   2. (Die meisten Erkenntnisse) Wählen Sie das zu analysierende Portfolio aus.

      Im Allgemeinen sind alle optimierten und aktiven Portfolios verfügbar, die aktive Kampagnen enthalten. Für einige Einblicke können Sie die Portfolioliste filtern, um **[!UICONTROL Only Optimized Portfolios]** einzuschließen.

      Für [!UICONTROL Day of Week] Einblicke sind nur Portfolios verfügbar, die über genügend Ausgaben verfügen und in den letzten zwei Tagen auch für das Targeting ausgegeben wurden.

   3. ([!UICONTROL Event Path Beta] nur insight) Gehen Sie wie folgt vor:

      1. Wählen Sie den Wert **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (um eine [!UICONTROL Channel Assist Report] oder [!UICONTROL Campaign Assist Report] hochzuladen und die Benutzerereignisse zur Analyse in verschiedene Gruppen zu klassifizieren) oder *[!UICONTROL Analyze classified events]* (um Ereignisgruppen hochzuladen und sie zum Generieren des Einblicks zu verwenden).

      1. Klicken Sie auf &quot;**[!UICONTROL Select]**&quot;, um eine Datei im XLSX- und ZIP-Format (komprimiertes XLSX) zu suchen, und klicken Sie dann auf &quot;**[!UICONTROL Upload]**&quot;.

   4. ([!UICONTROL Google Account Audit] nur insight) Gehen Sie wie folgt vor:

      1. Geben Sie die Werte **[!UICONTROL Advertiser Name]** und **[!UICONTROL Account Name]** ein.

      1. Wählen Sie die **[!UICONTROL Account Currency]**, die **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* oder die *[!UICONTROL United Kingdom]*) und die **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* oder *[!UICONTROL German]*) aus.

      1. Klicken Sie auf &quot;**[!UICONTROL Select]**&quot;, um nach Kampagnen-, Keyword- und Verlaufsberichten zu suchen, die über die Web-Benutzeroberfläche von [!DNL Google Ads] für das Konto heruntergeladen wurden, sowie nach einer Bulksheet-Datei, die von der Anwendung [!DNL Google Ads Editor] für das Konto heruntergeladen wurde. Klicken Sie dann auf **[!UICONTROL Upload]**.

         Alle Dateien müssen das Format CSV, TSV, TXT oder ZIP (komprimiertes CSV, TSV oder TXT) aufweisen.

   5. ([!UICONTROL Location Target Performance] Nur Einblicke; optional) Um die Daten täglich statt als Zusammenfassung zu aggregieren, wählen Sie den **[!UICONTROL Time Aggregation]** von *[!UICONTROL Daily]* aus.

   6. ([!UICONTROL Normalized Sim (Combined)] nur insight) Gehen Sie wie folgt vor:

      1. Geben Sie im Feld **[!UICONTROL Step]** die Anzahl der Zielausgabenebenen oder -schritte an, die in den Einblick einbezogen werden sollen. Der Wert kann zwischen drei (3) und 100 liegen.

      1. Wählen Sie im Feld **[!UICONTROL Type]** den Simulationstyp aus:

         * *[!UICONTROL Optimized Multi-portfolio]*: Generiert eine einzelne Simulation aus mehreren Portfolios mit demselben Ziel und derselben Währung.

         * *[!UICONTROL Individual Normalized]*: Erzeugt für jedes ausgewählte Portfolio eine individuelle Simulation. Die Portfolios können unterschiedliche Ziele und Währungen haben.

   7. ([!UICONTROL Portfolio Launch] Nur Insight; optional) Um ein Launch-Datum für die Zukunft festzulegen, geben Sie ein Datum im Feld **[!UICONTROL Optional Date]** an.

   8. ([!UICONTROL Quality Score] nur Insight) Wählen Sie das entsprechende Anzeigennetzwerk aus.

   9. ([!UICONTROL Query Cross Matching] Nur Insight) Wählen Sie im Menü **[!UICONTROL Google Accounts]** das Konto aus.

4. Klicken Sie auf **[!UICONTROL Generate Insight]**.

   Sie erhalten eine Benachrichtigung, wenn der Auftrag abgeschlossen ist oder aufgrund Ihrer [konfigurierten Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md) für [!UICONTROL Advertising Insights] fehlschlägt.

>[!MORELIKETHIS]
>
>* [Info [!UICONTROL Advertising Insights]](insight-about.md)
>* [Anzeigen oder Speichern von  [!DNL Advertising Insight]](insight-view-save.md)
>* [Löschen von an [!DNL Advertising Insight]](insight-delete.md)
