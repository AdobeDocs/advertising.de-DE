---
title: Generieren Sie eine [!DNL Advertising Insight]
description: Erfahren Sie, wie Sie eine [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Generieren Sie eine [!DNL Advertising Insight]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Klicken Sie auf den zu erzeugenden Einblick.

3. Geben Sie die Insight-Einstellungen an:

   1. (Einige Berichte; optional) Geben Sie die Datumsbereiche für den Einblick an.

   2. (Die meisten Erkenntnisse) Wählen Sie das zu analysierende Portfolio aus.

      Im Allgemeinen sind alle optimierten und aktiven Portfolios verfügbar, die aktive Kampagnen enthalten. Für einige Einblicke können Sie die Portfolioliste filtern, um **[!UICONTROL Only Optimized Portfolios]**.

      Für [!UICONTROL Day of Week] Einblicke, es sind nur Portfolios verfügbar, die über genügend Ausgaben verfügen und die auch in den letzten zwei Tagen für das Targeting ausgegeben wurden.

   3. ([!UICONTROL Event Path Beta] Nur Insight) Gehen Sie wie folgt vor:

      1. Wählen Sie die **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (um eine [!UICONTROL Channel Assist Report] oder [!UICONTROL Campaign Assist Report] und die Benutzerereignisse zur Analyse in verschiedene Gruppen einteilen) oder *[!UICONTROL Analyze classified events]* (um Ereignisgruppen hochzuladen und sie zum Generieren des Einblicks zu verwenden).

      1. Klicks **[!UICONTROL Select]** , um eine Datei im XLSX- und ZIP-Format (komprimiertes XLSX) zu suchen, und klicken Sie dann auf **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] Nur Insight) Gehen Sie wie folgt vor:

      1. Geben Sie die **[!UICONTROL Advertiser Name]** und **[!UICONTROL Account Name]**.

      1. Wählen Sie die **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* oder *[!UICONTROL United Kingdom]*) und der **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* oder *[!UICONTROL German]*).

      1. Klicks **[!UICONTROL Select]** , um nach Kampagnen-, Keyword- und Änderungsverlaufsberichten zu suchen, die für das Konto heruntergeladen wurden und aus dem [!DNL Google Ads] Webbenutzeroberfläche und eine Bulksheet-Datei, die für das Konto vom [!DNL Google Ads Editor] Anwendung. Klicken Sie anschließend auf **[!UICONTROL Upload]**.

         Alle Dateien müssen das Format CSV, TSV, TXT oder ZIP (komprimiertes CSV, TSV oder TXT) aufweisen.

   5. ([!UICONTROL Location Target Performance] Nur Einblicke; optional) Um die Daten täglich zu aggregieren, wählen Sie die **[!UICONTROL Time Aggregation]** von *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] Nur Insight) Gehen Sie wie folgt vor:

      1. Im **[!UICONTROL Step]** -Feld die Anzahl der Zielausgabenebenen oder -schritte angeben, die in den Einblick einbezogen werden sollen. Der Wert kann zwischen drei (3) und 100 liegen.

      1. Im **[!UICONTROL Type]** Wählen Sie den Simulationstyp aus:

         * *[!UICONTROL Optimized Multi-portfolio]*: Generiert eine einzige Simulation aus mehreren Portfolios mit demselben Ziel und derselben Währung.

         * *[!UICONTROL Individual Normalized]*: Erzeugt für jedes ausgewählte Portfolio eine individuelle Simulation. Die Portfolios können unterschiedliche Ziele und Währungen haben.

   7. ([!UICONTROL Portfolio Launch] Nur Insight; optional) Um ein Launch-Datum für die Zukunft festzulegen, geben Sie ein Datum in der **[!UICONTROL Optional Date]** -Feld.

   8. ([!UICONTROL Quality Score] nur Insight) Wählen Sie das entsprechende Anzeigennetzwerk aus.

   9. ([!UICONTROL Query Cross Matching] nur Insight) In der **[!UICONTROL Google Accounts]** -Menü das Konto aus.

4. Klicks **[!UICONTROL Generate Insight]**.

   Sie erhalten eine Benachrichtigung, wenn der Auftrag abgeschlossen ist oder aufgrund Ihrer [konfigurierte Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md) für [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [Info [!UICONTROL Advertising Insights]](insight-about.md)
>* [Anzeigen oder Speichern von [!DNL Advertising Insight]](insight-view-save.md)
>* [Löschen von [!DNL Advertising Insight]](insight-delete.md)
