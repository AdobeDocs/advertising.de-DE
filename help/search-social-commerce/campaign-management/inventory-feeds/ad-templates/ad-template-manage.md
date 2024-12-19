---
title: Verwalten von Anzeigenvorlagen für Inventar-Feeds
description: Erfahren Sie mehr über die Verwaltung von Anzeigenvorlagen, mit denen Ihre Inventardaten zur Verwaltung der Kontostruktur und zur Bereitstellung dynamischer Anzeigen verarbeitet werden können.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Verwalten von Anzeigenvorlagen für Inventar-Feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Löschaktionen) und nur [!DNL Yandex] Konten*

Vor oder nach dem Hochladen von Daten können Sie suchmaschinenspezifische Anzeigenvorlagen erstellen, über die Ihre Daten verarbeitet werden können. Sie können Vorlagen für Textanzeigen und erweiterte/erweiterte Textanzeigen, [!DNL Google Ads] und [!DNL Microsoft Advertising] responsive Suchanzeigen sowie für [!DNL Google Ads] und [!DNL Microsoft Advertising] Shopping-Anzeigen erstellen.

Sie können jede Vorlage mit einer Feed-Datei, [!DNL Google Merchant Center] Konto oder [!DNL Microsoft Merchant Center] Konto verknüpfen und mehrere Vorlagen mit derselben Feed-Datei oder demselben Konto verknüpfen. Eine Anzeigenvorlage kann Variablen enthalten, die durch tatsächliche Datenspalten aus einer hochgeladenen Datei oder einem Konto ersetzt werden. In den meisten Fällen können die Variablen auch [eine Modifikatorgruppe](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) enthalten, die Sie in „Suche“, „Social“ und &quot;Commerce&quot; einrichten, um mehrere Anzeigen, Keywords, Kampagnen oder Anzeigengruppen für jede anwendbare Zeile in der Datendatei zu erstellen. Mit den Vorlagenoptionen können Sie entweder eine neue Kontostruktur (Kampagnen, Anzeigengruppen, Keywords) für die Anzeigen erstellen oder die Anzeigen der vorhandenen Kontostruktur zuordnen.

Zusätzlich zur Erstellung neuer Vorlagen von Grund auf können Sie optional neue Vorlagen erstellen, indem Sie vorhandene klonen und bearbeiten.

Nachdem Sie eine Vorlage erstellt und mit einer Daten-Feed-Datei oder einem Händlerkonto verknüpft haben, können Sie die Daten in der Datei über die Vorlage weitergeben, um Kampagnendaten und Kontostruktur zu erstellen. Optional können Sie eine Bulksheet-Datei zur Überprüfung oder zur sofortigen Veröffentlichung im Werbenetzwerk erstellen.

Jede Vorlage kann aktiviert, angehalten oder gelöscht werden. Feed-Daten können nur durch aktive Vorlagen automatisch weitergegeben werden. Sie können Daten jedoch manuell über eine pausierte Vorlage weitergeben.

## Erstellen, Klonen oder Bearbeiten einer Feed-Vorlage

Erstellen Sie separate Vorlagen für Text- und erweiterte/erweiterte Textanzeigen, responsive Suchanzeigen, [!DNL Google Ads] Shopping-Anzeigen und [!DNL Microsoft Advertising] Shopping-Anzeigen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine neue Vorlage zu erstellen, klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create/Clone]** und wählen Sie dann das entsprechende Anzeigennetzwerk aus.

   * So klonen Sie eine vorhandene Vorlage:

      1. Aktivieren Sie das Kontrollkästchen neben der Vorlage, die Sie kopieren möchten.

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create/Clone]** und wählen Sie dann das entsprechende Werbenetzwerk aus.

   * (So bearbeiten Sie eine vorhandene Vorlage) Klicken Sie neben dem Vorlagennamen auf ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungen anzeigen/bearbeiten").

1. Legen Sie die Einstellungen für [Text-Anzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] Shopping-Anzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) oder [[!DNL Microsoft Advertising] Shopping-Anzeigenvorlage](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) fest:

   1. Geben Sie oben im Fenster Vorlageneinstellungen den Namen der Vorlage und das entsprechende Konto an.

      Wenn Sie eine vorhandene Vorlage klonen, benennen Sie die neue Vorlage um, damit die Anzeigen, die aus der neuen Vorlage erstellt werden, nicht mit Anzeigen verknüpft werden, die aus der Quellvorlage erstellt werden.

   1. (Optional) Geben Sie in der linken Spalte die Produkt-Feed-Datei oder das Händlerkonto an, deren Daten über die Vorlage weitergegeben werden:

      * (Für Produkt-Feed-Dateien) Um eine zuvor hochgeladene Datei auszuwählen, klicken Sie auf ![Nach-unten](/help/search-social-commerce/assets/arrow-down-dropdown.png "Pfeil") und wählen Sie eine Datei aus der Liste der verfügbaren Feed-Dateien aus. Um eine neue Datei hochzuladen, geben Sie die Datei entweder durch Eingabe des vollständigen Pfads und Dateinamens an oder durch Klicken auf **[!UICONTROL Browse]**, um die Datei auf Ihrem Gerät oder Netzwerk zu suchen, und klicken Sie dann auf **[!UICONTROL Upload]**.

      * (Für ein synchronisiertes Händlerkonto) Wählen Sie den Kontonamen aus.

      Die Spalten für die ausgewählte Datei oder das ausgewählte Konto werden angezeigt.

   1. Geben Sie auf der Registerkarte **[!UICONTROL Account Structure]** die Einstellungen für die Kontostruktur an.

   1. (Nur Textanzeigen) Klicken Sie auf die Registerkarte **[!UICONTROL Keywords]** und geben Sie die Keyword-Einstellungen an.

   1. (Nur Text- und responsive Suchanzeigen) Klicken Sie auf die Registerkarte **[!UICONTROL Ads]** und führen Sie einen der folgenden Schritte aus:

      >[!NOTE]
      >
      >* Sie können bis zu vier Anzeigenvariantenvorlagen pro Standardtext-Anzeigenvorlage, fünf Anzeigenvariantenvorlagen pro erweiterter/erweiterter Text-Anzeigenvorlage und drei Anzeigenvariantenvorlagen pro responsiver Suchanzeigenvorlage einbeziehen.
      >* Jede Anzeigengruppe kann bis zu drei aktivierte responsive Suchanzeigen enthalten.
      >* Sie können keine vorhandenen Standardtextanzeigen-Varianten bearbeiten, und vorhandene Vorlagen generieren keine Standardtextanzeigen mehr.
      >* Wenn Sie eine Anzeigenvariantenvorlage ändern, können bestehende Anzeigen gelöscht und neue erstellt werden, wenn Sie Daten über die Vorlage weitergeben ([ nach Anzeigentyp und Anzeigennetzwerk](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Gehen Sie wie folgt vor, um eine Anzeigenvariante hinzuzufügen:

         1. Klicken Sie auf **[!UICONTROL Add Ad Variation]** , um eine Textanzeige zu erstellen, **[!UICONTROL Add ETA Variation]**, um eine erweiterte/erweiterte Textanzeige zu erstellen, oder **[!UICONTROL Add RSA Variation]**, um eine responsive Textanzeige zu erstellen.

            Nachdem Sie den Anzeigentyp angegeben haben, können Sie nur diesen Anzeigentyp mit der Vorlage erstellen.

         1. Geben Sie die Anzeigeneinstellungen an.

            Bei responsiven Suchanzeigen können Sie 3-15 Überschriften und 2-4 Beschreibungen einfügen.

         1. (Optional) Um alle alternativen Anzeigenkopie-Felder mit Text aus den ursprünglichen Anzeigenkopie-Feldern vorauszufüllen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Prefill]**.

         1. (Optional) Um einer Anzeige einen weiteren Satz von Anzeigenkopien hinzuzufügen, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximale Länge überschreitet, sobald dynamische Parameter während der Übertragung durch Daten ersetzt werden, klicken Sie auf **[!UICONTROL Add Alternate]** und fügen Sie dann die alternativen Werte hinzu.

            >[!NOTE]
            >
            >* Wenn die Option [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und Sie können sie nach Bedarf bearbeiten.
            >* Nur die Anzeigenkopie-Felder, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die ursprünglichen Beschreibungen. Achten Sie daher darauf, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
            >* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.
            >* Für jedes Anzeigenkopie-Feld können bis zu vier Alternativen angegeben werden.

         * Gehen Sie wie folgt vor, um eine Anzeigenvariante zu bearbeiten:

            1. Bearbeiten Sie die Anzeigeneinstellungen.

               Bei responsiven Suchanzeigen können Sie 3-15 Überschriften und 2-4 Beschreibungen einfügen.

            1. (Optional) Um alle alternativen Anzeigenkopie-Felder mit Text aus den ursprünglichen Anzeigenkopie-Feldern vorauszufüllen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Prefill]**.

            1. (Optional) Um einer Anzeige einen weiteren Satz von Anzeigenkopien hinzuzufügen, der verwendet werden kann, wenn eine der Zeilen in der ursprünglichen Anzeigenkopie die maximale Länge überschreitet, sobald dynamische Parameter während der Übertragung durch Daten ersetzt werden, klicken Sie auf **[!UICONTROL Add Alternate]** und fügen Sie dann die alternativen Werte hinzu.

               >[!NOTE]
               >
               >* Wenn die Option [!UICONTROL Prefill] ausgewählt ist, werden die alternativen Felder mit den ursprünglichen Feldern vorausgefüllt und Sie können sie nach Bedarf bearbeiten.
               >* Nur die Anzeigenkopie-Felder, die die maximale Länge überschreiten, werden durch den alternativen Wert ersetzt. Wenn beispielsweise nur eine ursprüngliche Überschrift oder ein Titel zu lang ist, verwendet die generierte Anzeigenvariante die alternative Überschrift oder den alternativen Titel und die ursprünglichen Beschreibungen. Achten Sie daher darauf, dass die alternative Anzeigenkopie in Kombination mit der ursprünglichen Anzeigenkopie sinnvoll ist.
               >* Wenn die ursprüngliche Anzeigenkopie die Längenanforderungen der Suchmaschine erfüllt, wird die alternative Anzeigenkopie verworfen.
               >* Für jedes Anzeigenkopie-Feld können bis zu vier Alternativen angegeben werden.

         * Um eine Anzeigenvariante zu entfernen, klicken Sie auf **[!UICONTROL Remove ETA Variation]** (für erweiterte/erweiterte Textanzeigen) oder **[!UICONTROL Remove RSA Variation]** (für responsive Suchanzeigen) neben der Anzeigenvariante.

   1. (Nur Shopping-Vorlagen) Klicken Sie auf die Registerkarte **[!UICONTROL Product Groups]** und geben Sie dann Informationen zu den Produktgruppen an, die Sie ansprechen möchten.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Feed Filters]** und geben Sie dann an, welche Zeilen in der Feed-Datei weitergegeben werden sollen.

   1. (Optional) Klicken Sie auf die **[!UICONTROL Label Classifications tab]** und geben Sie dann die Klassifizierungswerte für die Bezeichnung an, die den verschiedenen erstellten Kampagnenkomponenten zugewiesen werden sollen:

      1. Aktivieren Sie das Kontrollkästchen neben **[!DNL \[Component\] Label Classifications]**.

      1. Gehen Sie für jede Kennzeichnungsklassifizierung, die der Komponente zugewiesen werden soll, wie folgt vor:

         1. Klicken Sie auf **[!UICONTROL Add Label Classification]**.

         1. Wählen Sie die Kennzeichnungsklassifizierung aus und wählen Sie dann entweder einen vorhandenen Wert aus oder geben Sie einen neuen Wert ein.

1. Speichern Sie die Vorlage:

   * Um die Vorlage einfach zu speichern, klicken Sie auf **[!UICONTROL Save]** und dann erneut auf **[!UICONTROL Save]**.

   * Um die Vorlage zu speichern und die angegebene Datendatei weiterzugeben, klicken Sie auf **[!UICONTROL Save]** und anschließend auf **[!UICONTROL Save & Propagate]**.

## Ändern des Status von Feed-Vorlagen

Sie können jede pausierte Daten-Feed-Vorlage aktivieren oder jede aktive Daten-Feed-Vorlage pausieren.

>[!NOTE]
>
>Sie können Daten manuell über eine pausierte Vorlage weitergeben, Daten werden jedoch nicht automatisch weitergegeben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Aktivieren Sie das Kontrollkästchen neben jeder Vorlage, deren Status Sie ändern möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Change Status]** und dann auf **[!UICONTROL Activate]** oder **[!UICONTROL Pause]**.

## Feed-Vorlagen löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

1. Aktivieren Sie das Kontrollkästchen neben jeder Vorlage, die Sie löschen möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Über die Automatisierung der Anzeigenverwaltung mithilfe von Inventar-Feeds](../inventory-feeds-about.md)
>* [Einstellungen für Textanzeigen und responsive Suchanzeigen-Vorlagen](template-text-rsa.md)
>* [[!DNL Google Ads] Einstellungen für Shopping-Anzeigen-Vorlagen](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] Einstellungen für Shopping-Anzeigen-Vorlagen](template-microsoft-shopping.md)
>* [Verbreiten von Feed-Daten über Vorlagen](../feed-data-propagate.md)
