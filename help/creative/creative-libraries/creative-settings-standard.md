---
title: Creative-Einstellungen
description: Informationen zu xxxx.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '2100'
ht-degree: 0%

---

# Creative-Einstellungen

Die Einstellungen variieren je nach Kreativtyp.

Wenn Sie mehrere Kreative gleichzeitig bearbeiten:

* Sie können die Einstellungen für jeden Kreativen gleichzeitig oder einzeln bearbeiten. Standardmäßig werden alle ausgewählten Kreativen ausgewählt. Alle von Ihnen angegebenen Einstellungen gelten für alle ausgewählten Kreativen. Um die Einstellungen für bestimmte Kreative zu bearbeiten, heben Sie die Auswahl aller nicht zutreffenden Kreativen auf, bevor Sie die Felder bearbeiten. Wiederholen Sie den Vorgang für weitere Kreative, falls erforderlich.

* Einige Einstellungen werden auf alle ausgewählten Kreativen angewendet.

## Flexible Kreativeinstellungen für HTML5 {#creative-settings-flexible-html5}

### Registerkarte „Details“

**Creative-Name:** Der Name des Kreativen. Standardmäßig wird der Vorlagenname oder der hochgeladene Dateiname verwendet, Sie können den Namen jedoch ändern. Für mehrere Kreative können Sie die einzelnen Kreativnamen bearbeiten. **Tipp:** Fügen Sie die Anzeigengröße in den Kreativnamen ein und verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie den Kreativen in ein Erlebnis einbeziehen.

**Language:** Die Standardsprache für jede Anzeige, mit der Sie die Kreativen verknüpfen. Wenn Sie mehrere Kreative hochladen oder bearbeiten, wird auf jeden ausgewählten Kreativen derselbe Wert angewendet.

**Creative-Größe:** (Schreibgeschützt für bestehende Kreative) Die Dimensionen der Kreativen. Wenn im Kreativ enthaltene Bilder größer sind als die angegebene Größe, werden sie entsprechend skaliert.

**[!UICONTROL Click Tags]:** Die Variablen, die Klick-Tracking-Weiterleitungen aus den enthaltenen Bannerwerbung ermöglichen. Die Variablennamen und entsprechenden Landingpage-URLs werden aus der hochgeladenen Kreativeinheit gefüllt. Sie können jedoch die Standard-URLs ändern. Für mehrere Kreative können Sie die einzelnen Klick-Tags bearbeiten.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Titel:** (Optional) Alle Beschriftungen, die auf alle ausgewählten Kreativen angewendet werden sollen. Sie können Kreative nach Label in verschiedenen Ansichten innerhalb von [!DNL Creative] filtern und die [!UICONTROL Creative Label] Dimension in die [!UICONTROL Custom Creative Report] einbeziehen.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue Kennzeichnung zu erstellen, die auf die Kreativen angewendet werden soll, öffnen Sie die Liste, klicken Sie auf **+ Kennzeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

### Registerkarte „Attribute“

**\[Alle für das Kreativ-Element geltenden Standardattribute für Inhalte\]:** Die Standardattributnamen und -werte werden aus der flexiblen Kreativ-Einheit gefüllt. Sie können die Werte jedoch optional ändern.

>[!NOTE]
>
>Sie können auch den Standardwert für jedes kreative Attribut durch einen benutzerdefinierten Wert ersetzen, wenn Sie das Kreative in ein Erlebnis einbeziehen. Durch Bearbeiten der Attribute in einem Erlebnis wird eine Variante des übergeordneten Kreativen erstellt.

Informationen zu Attributen, die in vordefinierten Vorlagen verfügbar sind, finden Sie unter &quot;[Verfügbare flexible kreative Vorlagen](#flexible-creative-templates-available)&quot;.

### Registerkarte „Vorlage“

*Nur bestehende Kreative*

Die flexible HTML5-Vorlagendatei für Kreative.

Sie können optional die vorhandene Vorlage durch eine neue Vorlage ersetzen, die ein anderes Layout hat, aber denselben Satz von Attributnamen wie die ursprüngliche Vorlage hat. Die neue Vorlage muss im ZIP-Format mit maximal 2 MB vorliegen. Wenn sich der Kreative in einem Bundle befindet, verwenden alle Erlebnisse, die das Bundle verwenden, anschließend das Layout aus der neuen Vorlage.

Wenn Sie die Vorlage für ein übergeordnetes Kreativ mit untergeordneten Varianten aktualisieren, werden die Varianten mit allen Änderungen am Vorlagen-Layout aktualisiert, aber die Attributwerte für die Variante werden nicht geändert.

So ersetzen Sie die vorhandene Anzeigenvorlage:

1. Klicken Sie **Vorlage aktualisieren**.

1. Klicken Sie **Fortfahren**.

1. Geben Sie eine ZIP-Datei auf eine der folgenden Arten an:

   * Ziehen Sie eine Datei per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe &quot;[ Anzeigenspezifikationen](#flexible-ad-spec).

1. Bearbeiten Sie die neuen [flexiblen Einstellungen für HTML-Anzeigen](#flexible-ad-settings) nach Bedarf.

1. **[!UICONTROL Edit]** klicken

## HTML5 Creative-Einstellungen {#creative-settings-html5}

## Registerkarte „Details“

Für neue Kreative befinden sich die folgenden Einstellungen nicht auf einer benannten Registerkarte.

**Creative-Name:** Der Name des Kreativen. Bei neuen Kreativen wird standardmäßig der Dateiname verwendet, Sie können ihn jedoch ändern. Für mehrere Kreative können Sie die einzelnen Kreativnamen bearbeiten. **Tipp:** Fügen Sie die Anzeigengröße in den Kreativnamen ein und verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie den Kreativen in ein Erlebnis einbeziehen.

**Language:** Die Standardsprache für jede Anzeige, mit der Sie die Kreativen verknüpfen. Wenn Sie mehrere Kreative hochladen oder bearbeiten, wird auf jeden ausgewählten Kreativen derselbe Wert angewendet.

**Creative-Größe:** (Schreibgeschützt für bestehende Kreative) Die Dimensionen der Kreativen. Wenn im Kreativ enthaltene Bilder größer sind als die angegebene Größe, werden sie entsprechend skaliert.

**[!UICONTROL Click Tags]:** (nur für statische HTML5-Kreative) Die Variablen, die Klick-Tracking-Umleitungen aus den enthaltenen Bannerwerbung ermöglichen. Die Variablennamen und entsprechenden Landingpage-URLs werden aus der hochgeladenen Kreativeinheit gefüllt. Sie können jedoch die Standard-URLs ändern. Für mehrere Kreative können Sie die einzelnen Klick-Tags bearbeiten.

>[!NOTE]
>
>Wenn Sie Kreative in ein Erlebnis einbeziehen, können Sie den Standardwert für jedes der Klick-Tags durch eine benutzerdefinierte Landingpage-URL ersetzen, um eine Ableitung der kreativen Basis zu generieren.

**Landingpage-URL:** (Einfache HTML5-Kreative mit nur einer Landingpage) Die URL der standardmäßigen Landingpage für jede Anzeige, mit der Sie die Kreativen verknüpfen. Es muss eine gültige URL sein, die mit http:// oder https:// beginnt. Dazu können Tracking-Parameter von Drittanbietern oder [[!DNL Creative] Makros](/help/creative/creative-macros.md) für den eigenen Gebrauch gehören.

Wenn Sie einen Kreativen in ein Bundle aufnehmen und das Bundle einem Erlebnis zuweisen, können Sie für jeden Kreativen im Bundle optional die Landingpage-URL ändern sowie Impression- und Klick-Tracking-URLs und JavaScript hinzufügen. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Titel:** (Optional) Alle Beschriftungen, die auf alle ausgewählten Kreativen angewendet werden sollen. Sie können Kreative in [!DNL Creative] nach Label in verschiedenen Ansichten filtern.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue Kennzeichnung zu erstellen, die auf die Kreativen angewendet werden soll, öffnen Sie die Liste, klicken Sie auf **+ Kennzeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

### Registerkarte „Vorlage“

*Nur bestehende statische HTML5-Kreative*

Die HTML5-Vorlagendatei für den Kreativen.

Sie können optional die vorhandene Vorlage durch eine neue Vorlage ersetzen, die ein anderes Layout hat, aber denselben Satz von Attributnamen wie die ursprüngliche Vorlage hat. Die neue Vorlage muss im ZIP-Format mit maximal 2 MB vorliegen. Wenn sich der Kreative in einem Bundle befindet, verwenden alle Erlebnisse, die das Bundle verwenden, anschließend das Layout aus der neuen Vorlage.

Wenn Sie die Vorlage für ein übergeordnetes Kreativ mit untergeordneten Varianten aktualisieren, werden die Varianten mit allen Änderungen am Vorlagen-Layout aktualisiert, aber die Attributwerte für die Variante werden nicht geändert.

So ersetzen Sie die vorhandene Anzeigenvorlage:

1. Klicken Sie **Vorlage aktualisieren**.

1. Klicken Sie **Fortfahren**.

1. Geben Sie eine ZIP-Datei auf eine der folgenden Arten an:

   * Ziehen Sie eine Datei per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe [HTML-Anzeigenspezifikationen](html5-creative-specification.md).

1. Bearbeiten Sie die neuen [HTML5-Anzeigeneinstellungen ](#creative-settings-html5) Bedarf.

1. **[!UICONTROL Edit]** klicken

## Kreative Bildeinstellungen {#creative-settings-image}

**Creative-Name:** Der Name des Kreativen. Bei neuen Kreativen wird standardmäßig der Dateiname verwendet, Sie können ihn jedoch ändern. Bei mehreren Bildern können Sie die einzelnen kreativen Namen bearbeiten. **Tipp:** Verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie das Kreative in ein Erlebnis einbeziehen.

**Language:** Die Standardsprache für jede Anzeige, mit der Sie die Kreativen verknüpfen. Der gleiche Wert gilt für alle ausgewählten Bilder. Wenn Sie die Kreativen in ein Erlebnis einbeziehen, können Sie optional die Spracheinstellungen für das Erlebnis anpassen.

**Creative-Größe:** (Schreibgeschützt) Die Abmessungen der hochgeladenen Bilder.

**Landingpage-URL** Die URL der standardmäßigen Landingpage für jede Anzeige, mit der Sie die Kreativen verknüpfen. Die Landingpage-URL muss eine gültige URL sein, die mit http:// oder https:// beginnt. Dazu können Tracking-Parameter von Drittanbietern oder [[!DNL Creative] Makros](/help/creative/creative-macros.md) für den eigenen Gebrauch gehören. Der gleiche Wert gilt für alle ausgewählten Bilder.

Wenn Sie einen Kreativen in ein Bundle aufnehmen und dieses dann einem Erlebnis zuweisen, können Sie für jeden Kreativen im Bundle optional die Landingpage-URL ändern sowie Impression- und Klick-Tracking-URLs und JavaScript hinzufügen. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Titel:** (Optional) Alle Beschriftungen, die auf alle ausgewählten Kreativen angewendet werden sollen. Sie können Kreative in [!DNL Creative] nach Label in verschiedenen Ansichten filtern.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue Kennzeichnung zu erstellen, die auf die Kreativen angewendet werden soll, öffnen Sie die Liste, klicken Sie auf **+ Kennzeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

## Kreative Einstellungen von Drittanbietern {#creative-settings-third-party}

**JavaScriptCode:** Ein JavaScript-Tag (und optional ein alternatives Tag für Browser, die JavaScript nicht unterstützen), das auf das Kreativ-Tag auf dem Werbeserver des Drittanbieters verweist. Das Skript kann je nach Anzeigenserver variieren. Wenn Sie mehrere Kreative bearbeiten, wird auf jeden ausgewählten Kreativen derselbe Wert angewendet.

Alle [verfügbaren Makros](/help/creative/creative-macros.md) und die Daten, mit denen sie ersetzt werden, sind unter dem Eingabefeld aufgeführt. Um eines der Makros in das Tag einzufügen, halten Sie den Cursor über die Makrobeschreibung und klicken Sie auf ![In Zwischenablage kopieren](/help/creative/assets/copy-to-clipboard.png "In Zwischenablage kopieren") und fügen Sie dann das Bild an der gewünschten Stelle im Tag ein.

Wenn Sie dieses Kreativ in ein Erlebnis aufnehmen, das Sie als Anzeige aus einer DSP implementieren, verwendet die DSP die Informationen in diesem Tag, um die Anzeige anzuzeigen und Impressionen und Klicks darauf zu verfolgen. Der DSP überträgt das Tag dann an den Anzeigenaustausch. Wenn die Anzeige angezeigt und angeklickt wird, verfolgen der Anzeigenserver, der DSP und [!DNL Creative] die Ereignisse.

**[!UICONTROL Advertiser]:** (Schreibgeschützt) Der Advertiser, für den die Bibliothek verfügbar ist.

**Creative-Name:** Der Name des Kreativen. **Tipp:** Verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie das Kreative in ein Erlebnis einbeziehen.

**Creative-Größe:** (Schreibgeschützt für bestehende Anzeigen) Die Dimensionen der Kreativen. Für neue Kreative wählen Sie aus einer Liste von Standardanzeigengrößen.

**Language:** Die Standardsprache für jede Anzeige, mit der Sie die Kreativen verknüpfen.

**Landingpage-URL:** Die Landingpage-URL, die zur Validierung jeder Anzeige verwendet wird, mit der Sie die Kreativen verknüpfen. Der Drittanbieter-Anzeigenserver bestimmt die tatsächliche Landingpage für jede Anzeige.

**Titel:** (Optional) Alle Beschriftungen, die auf alle ausgewählten Kreativen angewendet werden sollen. Sie können Kreative in [!DNL Creative] nach Label in verschiedenen Ansichten filtern.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue Kennzeichnung zu erstellen, die auf die Kreativen angewendet werden soll, öffnen Sie die Liste, klicken Sie auf **+ Kennzeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

## Kreative Videoeinstellungen {#creative-settings-video}

**Creative Asset-Name:** Der Name des Kreativen. Bei neuen Kreativen wird standardmäßig der Dateiname verwendet, Sie können ihn jedoch ändern. Bei mehreren Bildern können Sie die einzelnen kreativen Namen bearbeiten. **Tipp:** Verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie das Kreative in ein Erlebnis einbeziehen.

**Dauer:** (Schreibgeschützt) Die Dauer des Videos, das automatisch ausgefüllt wird.

**Language:** Die Standardsprache für jede Anzeige, mit der Sie die Kreativen verknüpfen. Der gleiche Wert gilt für alle ausgewählten Bilder. Wenn Sie die Kreativen in ein Erlebnis einbeziehen, können Sie optional die Spracheinstellungen für das Erlebnis anpassen.

**Landingpage-URL** Die URL der standardmäßigen Landingpage für jede Anzeige, mit der Sie die Kreativen verknüpfen. Die Landingpage-URL muss eine gültige URL sein, die mit http:// oder https:// beginnt. Dazu können Tracking-Parameter von Drittanbietern oder [[!DNL Creative] Makros](/help/creative/creative-macros.md) für den eigenen Gebrauch gehören. Der gleiche Wert gilt für alle ausgewählten Bilder.

Wenn Sie einen Kreativen in ein Bundle aufnehmen und dieses dann einem Erlebnis zuweisen, können Sie für jeden Kreativen im Bundle optional die Landingpage-URL ändern sowie Impression- und Klick-Tracking-URLs und JavaScript hinzufügen. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Titel:** (Optional) Alle Beschriftungen, die auf alle ausgewählten Kreativen angewendet werden sollen. Sie können Kreative in [!DNL Creative] nach Label in verschiedenen Ansichten filtern.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue Kennzeichnung zu erstellen, die auf die Kreativen angewendet werden soll, öffnen Sie die Liste, klicken Sie auf **+ Kennzeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

>[!MORELIKETHIS]
>
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-standard.md)
>* [Standard-Kreative bearbeiten](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Verfügbare Makros zum Tracking von URLs](/help/creative/creative-macros.md)
