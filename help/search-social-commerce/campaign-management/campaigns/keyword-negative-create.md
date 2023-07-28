---
title: Negative Suchbegriffe erstellen
description: Erfahren Sie, wie Sie negative Suchbegriffe für Suchkampagnen und Anzeigengruppen erstellen.
exl-id: 683e5395-cb65-4d7f-a981-7fc9f84d4192
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Negative Suchbegriffe erstellen

*[!DNL Baidu], [!DNL Google Ads] und [!DNL Microsoft® Advertising], und [!DNL Yahoo! Japan Ads] Nur Konten*

Sie können negative Suchbegriffe für eine Suchanzeigengruppe oder Kampagne erstellen, die auf die Suche oder das Display/native Netzwerk ausgerichtet ist. Negative Suchbegriffe geben keine Trigger-Anzeigen.

>[!NOTE]
>Sie können auch negative Suchbegriffe im [Anzeigengruppeneinstellungen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Um viele negative Suchbegriffe gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen")und klicken Sie anschließend auf **[!UICONTROL Campaign]** , um negative Suchbegriffe auf Kampagnenebene zu erstellen, oder **[!UICONTROL Ad Group]** , um negative Suchbegriffe auf Anzeigengruppenebene zu erstellen.

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und (falls zutreffend) die Anzeigengruppe aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die negativen Suchbegriffe ein. Verwenden Sie die folgende Syntax ohne Minuszeichen (`-`):

   * Negatives breites Match: `keyword` (nicht unterstützt von [!DNL Microsoft® Advertising])

   * Negative Wortgruppenübereinstimmung: `"keyword"`

   * Negative exakte Übereinstimmung: `[keyword]`

   Trennen Sie mehrere Werte durch Kommas oder geben Sie sie in separate Zeilen ein. Sie können bis zu 2000 negative Keywords in einem Vorgang eingeben oder einfügen. Siehe auch die folgenden Anforderungen und Einschränkungen:

   * Maximale Zeichenlängen: [!DNL Baidu]: 30 Einzelbyte- oder 15 Doppelbyte-Zeichen; [!DNL Microsoft® Advertising]: 100 Einzelbyte- oder 50 Doppelbyte-Zeichen; [!DNL Google Ads] und [!DNL Yahoo! Japan Ads]: 80 Einzelbyte- oder 40 Doppelbyte-Zeichen.

   * [!DNL Baidu] erlaubt nur einen Übereinstimmungstyp pro Suchbegriff pro Anzeigengruppe. Beispielsweise kann Anzeigengruppe 1 nicht beide `"keyword"` und `[keyword]`.

   * [!DNL Google Ads]: Jeder Suchbegriff darf maximal 10 Wörter enthalten und nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: Leerzeichen `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Jeder Suchbegriff kann maximal sieben Wörter enthalten, wobei Stoppwörter ausgeschlossen sind. Jeder [!DNL Yandex ad group] kann maximal 200 Keywords enthalten.

1. Klicken **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über Suchbegriffe](keyword-about.md)
>* [Bietbare Suchbegriffe verwalten](keyword-manage.md)
>* [Ändern des Status von Keywords und negativen Keywords](keyword-status-edit.md)
