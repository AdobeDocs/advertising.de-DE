---
title: Verwalten von Feed-Vorlagen
description: Erfahren Sie, wie Sie eine Anzeigenvorlage für Bestandsdaten-Feeds erstellen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Erstellen, Klonen oder Bearbeiten einer Feed-Vorlage

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Sie können suchmaschinenspezifische Anzeigenvorlagen erstellen, mit denen Ihre Bestandsdaten verarbeitet werden können. Erstellen Sie separate Vorlagen für Text und erweiterte Textanzeigen, responsive Suchanzeigen, [!DNL Google Ads] Shopping-Anzeigen und [!DNL Microsoft Advertising] Shopping-Anzeigen.

Sie können Vorlagen nicht nur von Grund auf neu erstellen, sondern auch neue Vorlagen erstellen, indem Sie vorhandene Vorlagen klonen.

Nachdem Sie eine Vorlage erstellt oder geklont und mit einer Daten-Feed-Datei verknüpft haben, können Sie die Daten in der Datei über die Vorlage übertragen, um Kampagnendaten und Kontostruktur zu erstellen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Vorlage von Grund auf neu zu erstellen, klicken Sie auf **[!UICONTROL Create/Clone]** in der Symbolleiste über der Datentabelle und wählen Sie dann das entsprechende Anzeigennetzwerk aus.

   * So klonen Sie eine vorhandene Vorlage:

      1. Aktivieren Sie das Kontrollkästchen neben der Vorlage, die Sie kopieren möchten.

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create/Clone]** und wählen Sie dann das entsprechende Anzeigennetzwerk aus.
   * (Um eine vorhandene Vorlage zu bearbeiten) Klicken Sie neben dem Vorlagennamen auf ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungen anzeigen/bearbeiten").


1. Geben Sie die Einstellungen für die [Textanzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] Shopping-Anzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)oder [[!DNL Microsoft Advertising] Shopping-Anzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Geben Sie oben im Fenster für die Vorlageneinstellungen den Vorlagennamen und das entsprechende Konto an.

      Wenn Sie eine vorhandene Vorlage klonen, benennen Sie die neue Vorlage so um, dass die aus der neuen Vorlage erstellten Anzeigen nicht mit Anzeigen verknüpft sind, die aus der Quellvorlage erstellt werden.

   1. (Optional) Geben Sie in der linken Spalte die Produkt-Feed-Datei oder das Händlercenter-Konto an, dessen Daten über die Vorlage weitergeleitet werden:

      * (Für Produkt-Feed-Dateien) Um eine zuvor hochgeladene Datei auszuwählen, klicken Sie auf ![Abwärtspfeil](/help/search-social-commerce/assets/arrow-down-dropdown.png "Abwärtspfeil") und wählen Sie eine Datei aus der Liste der verfügbaren Feed-Dateien aus. Um eine neue Datei hochzuladen, geben Sie die Datei an, indem Sie entweder den vollständigen Pfad und den Dateinamen eingeben oder auf **[!UICONTROL Browse]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen, und klicken Sie dann auf **[!UICONTROL Upload]**.

      * (Für ein synchronisiertes Händlerstatistikkonto) Wählen Sie den Kontonamen aus.

      Die Spalten für die ausgewählte Datei oder das ausgewählte Konto werden angezeigt.

   1. Im **[!UICONTROL Account Structure]** -Tab die Kontostruktureinstellungen festlegen.

   1. (Nur Textanzeigen) Klicken Sie auf die **[!UICONTROL Keywords]** und geben Sie die Suchbegriffeinstellungen an.

   1. (Nur Text und responsive Suchanzeigen) Klicken Sie auf die **[!UICONTROL Ads]** und führen Sie einen der folgenden Schritte aus:

      >[!NOTE]
      >
      >* Sie können bis zu vier Anzeigenvariationsvorlagen pro Standard-Textanzeigenvorlage, fünf Anzeigenvariationsvorlagen pro erweiterter/erweiterter Textanzeigenvorlage und drei Anzeigenvariationsvorlagen pro responsive Suchanzeigenvorlage einbeziehen.
      >* Jede Anzeigengruppe kann bis zu drei aktivierte responsive Suchanzeigen enthalten.
      >* Sie können vorhandene Varianten von Standardtextanzeigen nicht bearbeiten und vorhandene Vorlagen generieren keine Standardtextanzeigen mehr.
      >* Wenn Sie eine Anzeigenvariationsvorlage ändern, können vorhandene Anzeigen gelöscht und neue erstellt werden, wenn Sie Daten über die Vorlage propagieren. [je nach Anzeigentyp und Anzeigennetzwerk](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).


      * Gehen Sie wie folgt vor, um eine Anzeigenvariante hinzuzufügen:

         1. Klicken **[!UICONTROL Add Ad Variation]** um eine Textanzeige zu erstellen, **[!UICONTROL Add ETA Variation]** um eine erweiterte Textanzeige zu erstellen, oder **[!UICONTROL Add RSA Variation]** , um eine responsive Textanzeige zu erstellen.

            Nachdem Sie den Anzeigentyp festgelegt haben, können Sie nur diesen Anzeigentyp mit der Vorlage erstellen.

         1. Geben Sie die Anzeigeneinstellungen an.

            Für responsive Suchanzeigen können Sie 3 bis 15 Überschriften und 2 bis 4 Beschreibungen einfügen.

         1. (Optional) Wenn Sie alle alternativen Felder zum Kopieren von Anzeigen mit Text aus den Feldern zum Kopieren der ursprünglichen Anzeige vorab ausfüllen möchten, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Prefill]**.

         1. (Optional) Um einer Anzeige einen weiteren Satz von Anzeigenkopien hinzuzufügen, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximale Länge überschreitet, sobald dynamische Parameter bei der Propagierung durch Daten ersetzt werden, klicken Sie auf **[!UICONTROL Add Alternate]** und fügen Sie dann die alternativen Werte hinzu.

            >[!NOTE]
            >
            >* Wenn die Variable [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und können nach Bedarf bearbeitet werden.
            >* Nur die Werbetexte, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die ursprünglichen Beschreibungen. Stellen Sie daher sicher, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
            >* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.
            >* Sie können bis zu vier Alternativen für jedes Feld der Anzeigenkopie angeben.

         * Gehen Sie wie folgt vor, um eine Anzeigenvariante zu bearbeiten:

            1. Bearbeiten Sie die Anzeigeneinstellungen.

               Für responsive Suchanzeigen können Sie 3 bis 15 Überschriften und 2 bis 4 Beschreibungen einfügen.

            1. (Optional) Wenn Sie alle alternativen Felder zum Kopieren von Anzeigen mit Text aus den Feldern zum Kopieren der ursprünglichen Anzeige vorab ausfüllen möchten, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Prefill]**.

            1. (Optional) Um einer Anzeige einen weiteren Satz von Anzeigenkopien hinzuzufügen, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximale Länge überschreitet, sobald dynamische Parameter bei der Propagierung durch Daten ersetzt werden, klicken Sie auf **[!UICONTROL Add Alternate]** und fügen Sie dann die alternativen Werte hinzu.

               >[!NOTE]
               >
               >* Wenn die Variable [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und können nach Bedarf bearbeitet werden.
               >* Nur die Werbetexte, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die ursprünglichen Beschreibungen. Stellen Sie daher sicher, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
               >* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.
               >* Sie können bis zu vier Alternativen für jedes Feld der Anzeigenkopie angeben.

         * Um eine Anzeigenvariante zu entfernen, klicken Sie auf **[!UICONTROL Remove ETA Variation]** (für erweiterte/erweiterte Textanzeigen) oder **[!UICONTROL Remove RSA Variation]** (für responsive Suchanzeigen) daneben, sofern zutreffend.
   1. (Nur Shopping-Vorlagen) Klicken Sie auf die Schaltfläche **[!UICONTROL Product Groups]** und geben Sie dann Informationen zu den Produktgruppen an, die Sie als Ziel auswählen möchten.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Feed Filters]** und geben Sie dann an, welche Zeilen in der Feed-Datei propagiert werden sollen.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Label Classifications tab]** und geben Sie dann die Titel-Classification-Werte an, die den verschiedenen erstellten Kampagnenkomponenten zugewiesen werden sollen:

      1. Klicken Sie auf das Kontrollkästchen neben **[!DNL \[Component\] Label Classifications]**.

      1. Gehen Sie für jede Beschriftungsklassifizierung, die der Komponente zugewiesen werden soll, wie folgt vor:

         1. Klicken **[!UICONTROL Add Label Classification]**.

         1. Wählen Sie die Beschriftungs-Classification aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.





1. Speichern Sie die Vorlage:

   * Um die Vorlage einfach zu speichern, klicken Sie auf **[!UICONTROL Save]** und klicken Sie anschließend auf **[!UICONTROL Save]** erneut.

   * Um die Vorlage zu speichern und die angegebene Datendatei darüber zu übertragen, klicken Sie auf **[!UICONTROL Save]** und klicken Sie anschließend auf **[!UICONTROL Save & Propagate]**.

<!-- add more entries below -->

## Status von Feed-Vorlagen ändern

Sie können jede angehaltene Daten-Feed-Vorlage aktivieren oder jede aktive Daten-Feed-Vorlage anhalten.

>[!NOTE]
>
>Sie können Daten manuell über eine angehaltene Vorlage übertragen, aber die Daten werden nicht automatisch übertragen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Aktivieren Sie das Kontrollkästchen neben jeder Vorlage, deren Status Sie ändern möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Change Status]** und klicken Sie anschließend auf **[!UICONTROL Activate]** oder **[!UICONTROL Pause]**.

## Feed-Vorlagen löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

1. Aktivieren Sie das Kontrollkästchen neben den Vorlagen, die Sie löschen möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds](inventory-feeds-about.md)
>* [Workflow für die Verwaltung von Kampagnendaten mithilfe von Inventar-Feeds](inventory-feeds-workflow.md)

