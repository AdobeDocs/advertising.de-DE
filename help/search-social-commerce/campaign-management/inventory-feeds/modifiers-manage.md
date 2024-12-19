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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Modifikatoren sind Adjektive oder Adverbien, die einem Satz hinzugefügt oder daraus entfernt werden können, ohne die grundlegende Satzstruktur zu ändern. Sie können Gruppen von Modifikatoren erstellen, die als Variablen in verschiedenen Datenfeldern in Feed-Datenvorlagen verwendet werden können. Indem Sie Modifikatoren in Felder, Schlüsselwörter, Basis-URLs und Anzeigen der Kontostruktur (Kampagne und Anzeigengruppe) einbeziehen, erstellen Sie einen Wert für jeden zugehörigen Modifikatorwert. Wenn Sie beispielsweise eine Modifikatorgruppenvariable in einer Anzeigenüberschrift verwenden und die Modifikatorgruppe drei Modifikatoren („billig“, „Rabatt“ und „erschwinglich„) enthält, werden drei separate Anzeigen für jede Datenzeile im Daten-Feed erstellt - eine für jeden Modifikator. Wenn Sie eine Modifikatorgruppe mit mehreren Werten in die Basis-URL für eine Anzeigengruppe aufnehmen, wird für jede der resultierenden Basis-URLs ein Schlüsselwortsatz erstellt.

Jede Modifikatorgruppe kann beliebig viele Modifikatoren enthalten. Jede Vorlage kann nur eine Modifikatorgruppe verwenden.

## Erstellen einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Create]**.

1. Geben Sie die Einstellungen der Modifikatorgruppe an:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (einer pro Zeile).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Bearbeiten einer Modifikatorgruppe

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Klicken Sie in der Liste der Modifikatorgruppen auf den Namen der Modifikatorgruppe.

1. Bearbeiten Sie die Einstellungen der Modifikatorgruppe:

   **[!UICONTROL Name]:** Der Name der Modifikatorgruppe.

   **[!UICONTROL Modifiers]:** Die Modifikatorwerte für die Gruppe (einer pro Zeile).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Modifikatorgruppen löschen

>[!IMPORTANT]
>
>Wenn Sie eine Modifikatorgruppe löschen, entfernen Sie alle Variablen für diese Modifikatorgruppe (als `<modifier_group_name>` bezeichnet) aus den Feldern der vorhandenen Vorlagen. Wenn Sie versuchen, Daten mithilfe von Variablen für nicht vorhandene Modifikatoren über eine Vorlage zu propagieren, schlägt der Vorgang fehl1.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Modifiers]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Modifikatorgruppe, die Sie löschen möchten.

1. Klicken Sie über der Liste der Modifikatorgruppen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]**.

1. (Falls erforderlich) [Entfernen Sie Verweise auf den Modifikator](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) aus allen entsprechenden Vorlagen.

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Verwalten von Anzeigenvorlagen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
