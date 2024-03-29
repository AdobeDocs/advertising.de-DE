---
title: Verwalten von Modifikatoren
description: Erfahren Sie, wie Sie Modifikatoren für Ihre Anzeigenvorlagen für Inventardaten-Feeds konfigurieren und verwalten.
exl-id: ade1472d-10e3-454e-8095-c579b48cfc01
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Verwalten von Modifikatoren

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Modifikatoren sind Adjektive oder Adverbien, die zu einem Satz hinzugefügt oder daraus entfernt werden können, ohne die grundlegende Satzstruktur zu ändern. Sie können Gruppen von Modifikatoren erstellen, die in verschiedenen Datenfeldern in Feed-Datenvorlagen als Variablen verwendet werden. Indem Sie Modifikatoren in die Kontostruktur (Kampagnen- und Anzeigengruppen)-Felder, Suchbegriffe, Basis-URLs und Anzeigen einfügen, erstellen Sie für jeden zugehörigen Modifikatorwert einen Wert. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe drei Modifikatoren enthält (&quot;billig&quot;, &quot;rabatt&quot;und &quot;bezahlbar&quot;), werden für jede Datenzeile im Daten-Feed drei separate Anzeigen erstellt - eine für jeden Modifikator. Wenn Sie eine Modifikatorgruppe mit mehreren Werten in die Basis-URL für eine Anzeigengruppe aufnehmen, wird für jede der resultierenden Basis-URLs ein Satz Suchbegriffe erstellt.

Jede Modifikatorgruppe kann beliebig viele Modifikatoren enthalten. Jede Vorlage kann nur eine Modifikatorgruppe verwenden.

## Erstellen einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Create]**.

1. Geben Sie die Einstellungen für die Modifikatorgruppe an:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (1 pro Zeile).

1. Klicken **[!UICONTROL Save]**.

## Bearbeiten einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie in der Liste der Modifikatorgruppen auf den Namen der Modifikatorgruppe.

1. Bearbeiten Sie die Einstellungen der Modifikatorgruppe:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (1 pro Zeile).

1. Klicken **[!UICONTROL Save]**.

## Modifikatorgruppen löschen

>[!IMPORTANT]
>
>Wenn Sie eine Modifikatorgruppe löschen, entfernen Sie alle Variablen für diese Modifikatorgruppe (gekennzeichnet als `<modifier_group_name>`) aus den Feldern existierender Vorlagen. Wenn Sie versuchen, Daten über eine Vorlage mit Variablen für nicht vorhandene Modifikatoren zu übertragen, schlägt der Auftrag fehl1.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Modifikatorgruppe, die Sie löschen möchten.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Yes]**.

1. (Falls erforderlich) [Entfernen von Verweisen auf den Modifikator](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) aus allen anwendbaren Vorlagen.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
