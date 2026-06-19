---
title: Negative Keywords erstellen
description: Erfahren Sie, wie Sie negative Keywords für Suchkampagnen und Anzeigengruppen erstellen.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/NjLsCcI2-1kWIAfZOv4-IJytuPKUfQWO0OG7ptEDe9w
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 0%

---

# Negative Keywords erstellen

Nur *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] und vorhandene [!DNL Baidu] Konten*

Sie können negative Keywords für eine Suchanzeigengruppe oder Kampagne erstellen, die auf die Suche oder das Display/native Netzwerk abzielt. Negative Keywords führen nicht zu Trigger-Anzeigen.

>[!NOTE]
>Sie können auch negative Keywords in den [Anzeigengruppeneinstellungen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) erstellen und bearbeiten.

>[!TIP]
>Um viele negative Keywords gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") und klicken Sie dann auf **[!UICONTROL Campaign]** , um auf Kampagnenebene negative Keywords oder **[!UICONTROL Ad Group]** zu erstellen, um auf Anzeigengruppenebene negative Keywords zu erstellen.

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Negative Keywords eingeben. Verwenden Sie die folgende Syntax ohne Minuszeichen (`-`):

   * Negative weit gefasste Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)

   * Negative Übereinstimmung der Phrasen: `"keyword"`

   * Negative exakte Übereinstimmung: `[keyword]`

   Trennen Sie mehrere Werte durch Kommas oder geben Sie sie in separate Zeilen ein. Sie können bis zu 2000 negative Keywords in einem Vorgang eingeben oder einfügen. Siehe auch die folgenden Anforderungen und Einschränkungen:

   * Maximale Zeichenlängen: [!DNL Baidu]: 30 Einzelbyte oder 15 Doppelbyte; [!DNL Microsoft Advertising]: 100 Einzelbyte oder 50 Doppelbyte; [!DNL Google Ads] und [!DNL LY Ads]: 80 Einzelbyte oder 40 Doppelbyte.

   * [!DNL Baidu] ist nur ein Übereinstimmungstyp pro Keyword pro Anzeigengruppe zulässig. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.

   * [!DNL Google Ads]: Jedes Keyword darf nicht mehr als 10 Wörter umfassen und nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Jedes Keyword kann maximal sieben Wörter enthalten, ausschließlich Stoppwörter. Jede [!DNL Yandex ad group] kann maximal 200 Keywords enthalten.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über Keywords](keyword-about.md)
>* [Angebotsfähige Schlüsselwörter verwalten](keyword-manage.md)
>* [Ändern des Status von Keywords und negativen Keywords](keyword-status-edit.md)
