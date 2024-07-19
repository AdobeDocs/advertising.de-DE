---
title: Erstellen negativer Platzierungen
description: Erfahren Sie, wie Sie negative Platzierungen für [!DNL Google Ads] Kampagnen und Anzeigengruppen erstellen.
exl-id: 9cc2dd8d-5563-4e02-af8f-6181165494d8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Erstellen für [!DNL Google Ads] negative Platzierungen

*[!DNL Google Ads]nur Konten*

Sie können negative Platzierungen für eine [!DNL Google Ads] Anzeigengruppe in einer Kampagne erstellen, die auf das Display-Netzwerk ausgerichtet ist. Negative Platzierungen sind Sites im Display-Netzwerk, die keine Anzeigen Trigger haben.

>[!NOTE]
>Sie können auch negative Platzierungen in den Einstellungen für [Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) erstellen und bearbeiten.

>[!TIP]
>Um viele negative Platzierungen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") und dann auf **[!UICONTROL Campaign]** , um negative Platzierungen auf Kampagnenebene zu erstellen, oder auf **[!UICONTROL Ad Group]** , um negative Platzierungen auf Anzeigengruppenebene zu erstellen.

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die negativen Website-URLs ein.

   Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separate Zeilen ein. Gültige Formate sind:

   * Eine Website: Geben Sie eine gültige URL ein, z. B. www.example.com. Sehen Sie sich die zulässigen Formate unter &quot;Hinzufügen Ihrer Ausschluss-URLs&quot;unter https://support.google.com/google-ads/answer/2454012 an.

   * Ein Thema, eine Kategorie oder ein Dokument vertikal. Siehe [[!DNL Google Ads] Führungslinien](https://support.google.com/google-ads/editor/answer/30517) und eine [Liste aller Vertikalen](https://developers.google.com/adwords/api/docs/appendix/verticals). Beispiel: `category::Industries > Energy & Utilities > Oil & Gas`.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über Platzierungen](placement-about.md)
>* [Bidable Platzierungen verwalten](placement-manage.md)
>* [Ändern des Status von Platzierungen und negativen Platzierungen](placement-status-edit.md)
