---
title: Zuweisen von Classification-Werten zu Kontokomponenten aus Kampagnenverwaltungsansichten
description: Erfahren Sie, wie Sie Classification-Werte Kontokomponenten zuweisen.
exl-id: 7e55d7d8-5e12-409b-ad5d-c53cbf24c7c9
feature: Search Label Classifications
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Zuweisen von Classification-Werten zu Kontokomponenten aus Kampagnenverwaltungsansichten

Sie können Classification-Werte für die folgenden Suchentitäten aus den Ansichten der Kampagnenverwaltung zuweisen und entfernen: Kampagne, Anzeigengruppe, Suchbegriff, Anzeige, Platzierung, Produktgruppe auf Einheitsebene und dynamisches Suchziel. Bei Bedarf können Sie während des Zuweisungsprozesses Classifications und Classification-Werte erstellen. Jede Beschriftungsklassifizierung kann bis zu 2000 Werte aufweisen.

Jede Entität kann einen Beschriftungswert pro Classification haben. Shoes_Campaign kann beispielsweise den Farbwert &quot;red&quot;und den Geo-Wert &quot;Los Angeles&quot;haben, aber nicht mehrere Werte für Color oder Geo.

Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die vererbten Werte überschreiben.

>[!NOTE]
>
>Ihre Suchbegriffe und Werbetexte für einige Werbenetzwerke und Kampagnentypen sind [nicht veränderlich](/help/search-social-commerce/campaign-management/faqs-campaigns.md), was bedeutet, dass die Bearbeitung dieser Elemente die vorhandene Entität löscht und eine neue erstellt. Wenn eine vorhandene Entität auf diese Weise gelöscht wird, wird die Titel-Classification der neuen Entität nicht zugewiesen.

1. Klicks **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** und wählen Sie dann die Ansicht der Kontokomponente aus.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um Werte einer einzelnen Entität zuzuweisen) Halten Sie den Cursor über den Entitätsnamen, klicken Sie auf ![Menüschaltfläche](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüschaltfläche")und wählen Sie **[!UICONTROL Classification]**.

   * (So weisen Sie einer oder mehreren Entitäten Werte zu) Gehen Sie wie folgt vor:

      * Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

        Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Klicken Sie in der Symbolleiste über der Datentabelle auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr")und klicken Sie anschließend auf **[!UICONTROL Classification]**.

1. Im [!UICONTROL Assignment Details]führen Sie einen der folgenden Schritte aus:

   * Um vorhandene Klassifizierungswerte in neue Werte zu ändern, wählen Sie **[!UICONTROL Set To]**.

     Die maximale Länge pro Wert beträgt 100 Zeichen. Sie kann ASCII- und Nicht-ASCII-Zeichen enthalten.

   * Um bestimmte Classification-Werte zuzuweisen, ohne vorhandene Werte zu entfernen, wählen Sie **[!UICONTROL Assign]**.

   * Um bestimmte, aktuell zugewiesene Classification-Werte zu entfernen, wählen Sie **[!UICONTROL Remove]**.

     Wenn Sie einen Classification-Wert entfernen, stehen für die angegebenen Kontokomponenten keine Berichtsdaten für den Wert mehr zur Verfügung.

   * Um bestimmte Classification-Werte zu löschen, wählen Sie **[!UICONTROL Delete]**.

     Wenn Sie einen Classification-Wert löschen, steht er nicht mehr für die zukünftige Verwendung zur Verfügung und Berichtsdaten stehen für den Wert nicht mehr zur Verfügung. Alle Zuweisungen zwischen den Werten und bestimmten Kontokomponenten werden entfernt, die Kontokomponenten werden jedoch nicht gelöscht.

1. Führen Sie für jeden zutreffenden Classification-Wert folgende Schritte aus:

   1. Im **[!UICONTROL Classification]** geben Sie den Classification-Namen an:

      * Um eine vorhandene Classification zu verwenden, klicken Sie auf den Classification-Namen, um sie zu erweitern.

      * Um eine Classification zu erstellen, klicken Sie auf [!UICONTROL +]. Geben Sie im Eingabefeld den Classification-Namen ein und klicken Sie auf ![Speichern](/help/search-social-commerce/assets/select.png "Speichern") , um die Classification sofort zu speichern.

        Der Name muss aus [ASCII-Zeichen 32-126](https://www.asciitable.com/)und die maximale Länge 27 Einzelbyte-Zeichen beträgt.

   1. Im **[!UICONTROL Value Name]** geben Sie den Namen des Werts an:

      * Um einen vorhandenen Wert zu verwenden, klicken Sie auf den Wertnamen, um ihn auszuwählen.

      * Um einen Wert zu erstellen, klicken Sie auf [!UICONTROL +]. Geben Sie im Eingabefeld den Wert ein und klicken Sie auf ![Speichern](/help/search-social-commerce/assets/select.png "Speichern") , um den Wert sofort zu speichern.

        Die maximale Länge beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

1. (Optional) Geben Sie zusätzliche Details ein:

   1. Weiter zu **[!UICONTROL Additional Details]** klicken ![Öffnen](/help/search-social-commerce/assets/chevron-up.png "Öffnen") , um die Details zu erweitern.

   1. Optionale Eingabe **[!UICONTROL Project Name]** und/oder optional **[!UICONTROL Description]**.

1. Klicken **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über Beschriftungsklassifizierungen](classification-about.md)
>* [Erstellen einer Bezeichnungsklassifizierung](classification-create.md)
>* [Zuweisen von Classification-Werten zu Kontokomponenten mithilfe von Bulksheets](classification-values-assign-bulksheets.md)
>* [Entfernen von Beschriftungs-Classification-Werten aus Kontokomponenten](classification-values-remove.md)
>* [Löschen von Bezeichnungsklassifizierungswerten](classification-values-delete.md)
>* [Beschriftungsklassifizierungen löschen](classification-delete.md)
