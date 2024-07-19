---
title: Verwalten von Modifikatoren
description: Erfahren Sie, wie Sie Modifikatoren für Ihre Anzeigenvorlagen für Inventardaten-Feeds konfigurieren und verwalten.
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Verwalten von Modifikatoren

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Modifikatoren sind Adjektive oder Adverbien, die zu einem Satz hinzugefügt oder daraus entfernt werden können, ohne die grundlegende Satzstruktur zu ändern. Sie können Gruppen von Modifikatoren erstellen, die in verschiedenen Datenfeldern in Feed-Datenvorlagen als Variablen verwendet werden. Indem Sie Modifikatoren in die Kontostruktur (Kampagnen- und Anzeigengruppen)-Felder, Suchbegriffe, Basis-URLs und Anzeigen einfügen, erstellen Sie für jeden zugehörigen Modifikatorwert einen Wert. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe drei Modifikatoren enthält (&quot;billig&quot;, &quot;rabatt&quot;und &quot;bezahlbar&quot;), werden für jede Datenzeile im Daten-Feed drei separate Anzeigen erstellt - eine für jeden Modifikator. Wenn Sie eine Modifikatorgruppe mit mehreren Werten in die Basis-URL für eine Anzeigengruppe aufnehmen, wird für jede der resultierenden Basis-URLs ein Satz Suchbegriffe erstellt.

Jede Modifikatorgruppe kann beliebig viele Modifikatoren enthalten. Jede Vorlage kann nur eine Modifikatorgruppe verwenden.

## Erstellen einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Create]**.

1. Geben Sie die Einstellungen für die Modifikatorgruppe an:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (1 pro Zeile).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie in der Liste der Modifikatorgruppen auf den Namen der Modifikatorgruppe.

1. Bearbeiten Sie die Einstellungen der Modifikatorgruppe:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (1 pro Zeile).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Modifikatorgruppen löschen

>[!IMPORTANT]
>
>Wenn Sie eine Modifikatorgruppe löschen, entfernen Sie alle Variablen für diese Modifikatorgruppe (mit der Bezeichnung &quot;`<modifier_group_name>`&quot;) aus den Feldern vorhandener Vorlagen. Wenn Sie versuchen, Daten über eine Vorlage mit Variablen für nicht vorhandene Modifikatoren zu übertragen, schlägt der Auftrag fehl1.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Modifikatorgruppe, die Sie löschen möchten.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]**.

1. (Falls erforderlich) [Entfernen Sie Verweise auf den Modifikator](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) aus allen zutreffenden Vorlagen.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
