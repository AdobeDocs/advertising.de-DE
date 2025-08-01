---
title: Einstellungen für nicht zielgerichtete Erlebnisse
description: Siehe Beschreibungen aller Einstellungen für Anzeigenerlebnisse ohne Targeting mit Entscheidungsbaum.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 0%

---

# Einstellungen für nicht zielgerichtete Erlebnisse

*Geschlossene Beta-Version*

## [!UICONTROL Experience basics]

**[!UICONTROL Ad Type]:** (Schreibgeschützt für vorhandene Erlebnisse) Der Typ der in dem Erlebnis enthaltenen Anzeigen: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* oder *[!UICONTROL Video]*. Nachdem Sie das Erlebnis gespeichert haben, können Sie den Anzeigentyp nicht mehr ändern.

**[!UICONTROL Advertiser]:** (Schreibgeschützt für vorhandene Erlebnisse) Der Werbetreibende, der Gebote für die in das Erlebnis eingeschlossenen Kreativen abgibt. Nachdem Sie das Erlebnis gespeichert haben, können Sie den Advertiser nicht mehr ändern.

**[!UICONTROL Experience Name]:** Ein eindeutiger Name für das Erlebnis. **Tipp** Verwenden Sie einen Namen, den Sie leicht finden können, wenn Sie das Erlebnis als Anzeige in Advertising DSP oder einer anderen DSP verwenden.

**[!UICONTROL Creative Library]:** (Schreibgeschützt für vorhandene Erlebnisse) Eine einzelne Kreativbibliothek, die für das Erlebnis verwendet werden soll. Nachdem Sie das Erlebnis gespeichert haben, können Sie die Bibliothek nicht mehr ändern.

## [!UICONTROL Default creatives]

**\[Angegebene Standardkreative\]:** Die Standardkreativen, die verwendet werden, wenn ein Browser keine dem Erlebnis zugewiesenen Kreativen anzeigen kann, z. B. wenn der Browser nicht JavaScript aktiviert ist oder der Anzeigenserver die Anzeige aufgrund von Verzögerungen nicht personalisieren kann. Geben Sie für standardmäßige Anzeigeerlebnisse pro Anzeigengröße, für die das Erlebnis gilt, ein kreatives Bild an. Schließen Sie für standardmäßige Videoerlebnisse pro Anzeigengröße, für die das Erlebnis gilt, ein kreatives Video ein. Ihre Auswahl bestimmt die kreativen Größen, die für das Erlebnis verwendet werden können.

Für Erlebnisse ohne Targeting mit Entscheidungsbäumen können Sie die standardmäßigen Kreativen mit Kreativen derselben Größe in [!UICONTROL Tag Manager] überschreiben.

* Um ein Standardkreativ mit verschiedenen Dimensionen hinzuzufügen, klicken Sie auf **[!UICONTROL + Add Sizes]**, aktivieren Sie im rechten Bereich die Kontrollkästchen neben den einzelnen Kreativen, die hinzugefügt werden sollen, und klicken Sie dann auf **[!UICONTROL Add Creatives]**.

* Um ein Standardkreativ zu löschen, halten Sie den Cursor über die kreative Miniaturansicht und klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen").

* Um alle standardmäßigen Kreativen zu löschen, klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen") **[!UICONTROL Delete all]**.

* Um den Kreativbereich auf der rechten Seite ein- oder auszublenden, klicken Sie ![Anzeigen/Ausblenden](/help/creative/assets/hide-show-creatives.png "Anzeigen/Ausblenden") oben rechts im rechten Bereich.

## [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Schreibgeschützt für vorhandene Erlebnisse) Trifft nicht zu, wenn Sie die Zielgruppenbestimmung mithilfe eines Entscheidungsbaums nicht aktivieren. Lassen Sie diese Option deaktiviert. **Hinweis** Wenn Sie ein Erlebnis ohne Targeting gespeichert haben, können Sie die Zielgruppenbestimmung später nicht mehr hinzufügen.

**[!UICONTROL Language Targeting]:** (Erlebnisse nur mit Standardanzeigen; optional; schreibgeschützt für vorhandene Erlebnisse) Überprüft die Browser-Spracheinstellungen des Benutzers und zeigt ein Kreativ in der angegebenen Sprache an, wenn ein Kreativ in dieser Sprache verfügbar ist. Wenn kein Kreativ in der im Browser angegebenen Sprache verfügbar ist, wird stattdessen die [!UICONTROL Preferred language] verwendet. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

**[!UICONTROL Preferred language]:** (Erlebnisse nur mit Standardanzeigen; schreibgeschützt für vorhandene Erlebnisse) Die Sprache für alle aus dem Erlebnis erstellten Anzeigen, es sei denn, [!UICONTROL Language Targeting] ist aktiviert. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

## [!UICONTROL Advanced]

**Datenübergabe:** (Nur Erlebnisse mit dynamischen Anzeigen; optional) Um Benutzende auf der Grundlage bestimmter Schlüssel-Wert-Paare anzusprechen, die der DSP, Publisher oder Partner in Echtzeit bei Impressionen übergibt (z. B. SKU=01234567890123 oder Cart=empty). Es können bis zu fünf Datenübergabeschlüssel (Parameter) angegeben werden.<!-- May move this to just within the decision tree. -->

Wenn Sie ein Anzeigen-Erlebnis-Tag für eine bestimmte kreative Größe erstellen, wird jeder Schlüssel, der in diesem Feld angegeben ist, als Makro im -Tag angehängt. Geben Sie den Wert für jedes Schlüssel-Wert-Paar innerhalb des Tags ein, bevor Sie das Tag als Anzeige in Ihre DSP implementieren.

**Radius:** (Nur Erlebnisse mit dynamischen Anzeigen; optional) Ein Radius von einer US-Postleitzahl, die in der zu zielenden Feed-Datei angegeben ist; wählen Sie einen Radius von 0 Meilen bis 200 Meilen aus. Die Feed-Datei, die zur Erstellung der dynamischen Anzeigen für das Erlebnis verwendet wird, muss eine [!UICONTROL ZIP] Spalte <!-- or a user-named column mapped to a ZIP column -->, die für jede Produktzeile in der Datei einen Wert enthält. Beispielsweise kann eine Anzeige für ein in 95110 verfügbares Produkt im Umkreis von 10 Meilen für Benutzende im Umkreis von 10 Meilen von 95110 angezeigt werden (bestimmt durch die IP-Adresse des/r Benutzenden).

**RT Pixel:** (Erlebnisse nur mit dynamischen Anzeigen; optional) Ein [!UICONTROL Creative] Retargeting-Pixel zum potenziellen Targeting. Wenn Sie das Targeting innerhalb des Entscheidungsbaums einrichten, können Sie eine Ebene von RT-Pixel-Zielknoten einbeziehen. Für jeden Knoten geben Sie das anzusprechende Pixel und die Werte für die Attribute des Pixels an, die erforderlich sind, um die Kreativen in den zugewiesenen kreativen Bundles anzuzeigen. Wenn Sie in diesem Feld kein Pixel angeben, können Sie trotzdem eines innerhalb der Entscheidungsstruktur angeben.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> (Optional) Alle [!DNL Creative] Kennzeichnungen, die auf das Erlebnis angewendet werden sollen. Sie können Erlebnisse in der Ansicht Erlebnisse nach Beschriftung filtern und die Dimension [!UICONTROL Experience Label] in die [!UICONTROL Custom Creative Report] einbeziehen.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue anzuwendende Kennzeichnung zu erstellen, öffnen Sie die Liste, klicken Sie auf **+ Bezeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

**[!UICONTROL Impression Tracking URL]:** (Optional) Eine Impression-Tracking-URL eines Drittanbieters, die für jede aus dem Erlebnis erstellte Anzeige an die Landingpage-URL angehängt werden soll. Sie können bis zu fünf URLs einschließen. Um eine zusätzliche URL hinzuzufügen, klicken Sie auf ![Symbol](/help/creative/assets/create.png) **[!UICONTROL Add More] und geben Sie die URL ein.

Sobald Sie eine URL eingeben, werden [verfügbaren Makros](/help/creative/creative-macros.md) und die Daten, mit denen sie ersetzt werden, weiter unten auf der Seite aufgeführt. Um eines der Makros in die URL einzufügen, halten Sie den Cursor über die Makrobeschreibung und klicken Sie auf ![In Zwischenablage kopieren](/help/creative/assets/copy-to-clipboard.png "In Zwischenablage kopieren") und fügen Sie das Makro dann an der gewünschten Stelle in das URL-Feld ein.

>[!NOTE]
>
>* [!DNL Creative] stellt der Landingpage-URL automatisch seine eigenen Impression-Tracking-Tags als Präfix voran.
>* Sie können diese URL für jeden Kreativen im Erlebnis überschreiben.
>* Sie können auch den Impression-Tracking-Code eines Drittanbieters für JavaScript im Feld [!UICONTROL Client JS] eingeben

**[!UICONTROL Click Tracking URL]:** (Optional) (Optional) Eine Klick-Tracking-URL eines Drittanbieters, die an die Landingpage-URL angehängt werden soll. Sie können bis zu fünf URLs einschließen. Um eine zusätzliche URL hinzuzufügen, klicken Sie auf ![Symbol](/help/creative/assets/create.png) **[!UICONTROL Add More]** und geben Sie die URL ein.

Sobald Sie eine URL eingeben, werden [verfügbaren Makros](/help/creative/creative-macros.md) und die Daten, mit denen sie ersetzt werden, weiter unten auf der Seite aufgeführt. Um eines der Makros in die URL einzufügen, halten Sie den Cursor über die Makrobeschreibung und klicken Sie auf ![In Zwischenablage kopieren](/help/creative/assets/copy-to-clipboard.png "In Zwischenablage kopieren") und fügen Sie das Makro dann an der gewünschten Stelle in das URL-Feld ein.

>[!NOTE]
>
>* [!DNL Creative] stellt der Landingpage-URL automatisch seine eigenen Impression-Tracking-Tags als Präfix voran.
>* Sie können diese URL für jedes kreative Element <!-- creative bundle for targeted experiences --> Erlebnis überschreiben.

**[!UICONTROL Client JS]:** (optional) eine der folgenden Möglichkeiten:

* (Wenn der Werbetreibende einen OBA-Compliance-Anbieter für die Anzeigen verwendet) JavaScript-Code, der auf die Anzeigenüberlagerung verweist, mit der Benutzende das Targeting im Online-Verhalten (OBA) deaktivieren können.

* Jeder JavaScript-Impression-Trackingcode eines Drittanbieters, der an die Landingpage angehängt werden soll. **Hinweis:** Sie können auch eine Impression-Tracking-URL eines Drittanbieters in das Feld [!UICONTROL Impression Tracking URL] eingeben.

>[!MORELIKETHIS]
>
>* [Erstellen eines Erlebnisses ohne Targeting mit einem Entscheidungsbaum](experience-create-no-targeting.md)
>* [Bearbeiten eines Erlebnisses ohne Targeting mit einem Entscheidungsbaum](experience-edit-no-targeting.md)
>* [Verfügbare Makros zum Tracking von URLs](/help/creative/creative-macros.md)
>* [Manuelles Erstellen eines Anzeigen-Tags für eine entsprechende Kreativgröße](experience-tag-create-manually.md)
>* [Zuweisen von Kreativen zu einem Anzeigen-Tag für Erlebnisse ohne Targeting](experience-tag-assign-creatives.md)
>* [Anpassen der Tracking-URLs für ein Erlebnis ohne Targeting](experience-tracking-urls-no-targeting.md)
>* [Passen Sie die kreative Optimierung und Planung für ein Erlebnis ohne Targeting an](experience-optimization-scheduling-no-targeting.md)
