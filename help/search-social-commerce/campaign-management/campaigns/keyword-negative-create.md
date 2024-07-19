---
title: Negative Suchbegriffe erstellen
description: Erfahren Sie, wie Sie negative Suchbegriffe für Suchkampagnen und Anzeigengruppen erstellen.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Negative Suchbegriffe erstellen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] und vorhandene [!DNL Baidu] Konten nur*

Sie können negative Suchbegriffe für eine Suchanzeigengruppe oder Kampagne erstellen, die auf die Suche oder das Display/native Netzwerk ausgerichtet ist. Negative Suchbegriffe geben keine Trigger-Anzeigen.

>[!NOTE]
>Sie können auch negative Suchbegriffe in den Einstellungen für [Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) erstellen und bearbeiten.

>[!TIP]
>Um viele negative Suchbegriffe gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") und klicken Sie dann auf **[!UICONTROL Campaign]** , um negative Suchbegriffe auf Kampagnenebene zu erstellen, oder auf **[!UICONTROL Ad Group]** , um negative Suchbegriffe auf Anzeigengruppenebene zu erstellen.

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die negativen Suchbegriffe ein. Verwenden Sie die folgende Syntax ohne Minuszeichen (`-`):

   * Negative breite Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)

   * Negative Wortgruppenübereinstimmung: `"keyword"`

   * Negative exakte Übereinstimmung: `[keyword]`

   Trennen Sie mehrere Werte durch Kommas oder geben Sie sie in separate Zeilen ein. Sie können bis zu 2000 negative Keywords in einem Vorgang eingeben oder einfügen. Siehe auch die folgenden Anforderungen und Einschränkungen:

   * Maximale Zeichenlängen: [!DNL Baidu]: 30 Einzelbyte- oder 15 Doppelbyte-Zeichen; [!DNL Microsoft Advertising]: 100 Einzelbyte- oder 50 Doppelbyte-Zeichen; [!DNL Google Ads] und [!DNL Yahoo! Japan Ads]: 80 Einzelbyte- oder 40 Doppelbyte-Zeichen.

   * [!DNL Baidu] erlaubt nur einen Übereinstimmungstyp pro Suchbegriff pro Anzeigengruppe. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.

   * [!DNL Google Ads]: Jeder Suchbegriff darf aus höchstens 10 Wörtern bestehen und nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Jeder Suchbegriff kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind. Jeder [!DNL Yandex ad group] kann maximal 200 Suchbegriffe enthalten.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über Suchbegriffe](keyword-about.md)
>* [Bidable Suchbegriffe verwalten](keyword-manage.md)
>* [Ändern des Status von Suchbegriffen und negativen Suchbegriffen](keyword-status-edit.md)
