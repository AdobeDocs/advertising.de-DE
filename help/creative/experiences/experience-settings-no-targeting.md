---
title: Einstellungen für nicht zielgerichtete Erlebnisse
description: Siehe Beschreibungen aller Einstellungen für Anzeigenerlebnisse ohne Targeting mit Entscheidungsbaum.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: f4d83da98f89313624e038fd1d8f0fedcf802cc4
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---

# Einstellungen für nicht zielgerichtete Erlebnisse

*Geschlossene Beta-Version*

## [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Schreibgeschützt für vorhandene Erlebnisse) Der Werbetreibende, der Gebote für die in das Erlebnis eingeschlossenen Kreativen abgibt. Nachdem Sie das Erlebnis gespeichert haben, können Sie den Advertiser nicht mehr ändern.

**[!UICONTROL Experience Name]:** Ein eindeutiger Name für das Erlebnis. **Tipp:** Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie das Erlebnis als Anzeige in Advertising DSP oder einer anderen DSP verwenden.

**[!UICONTROL Creative Library]:** (Schreibgeschützt für vorhandene Erlebnisse) Eine einzelne Kreativbibliothek, die für das Erlebnis verwendet werden soll. Nachdem Sie das Erlebnis gespeichert haben, können Sie die Bibliothek nicht mehr ändern.

## [!UICONTROL Default creatives]

**\[Angegebene Standardkreative\]:** Die Standardbildkreativen, die verwendet werden, wenn ein Browser keine dem Erlebnis zugewiesenen Kreativen anzeigen kann, z. B. wenn der Browser nicht JavaScript aktiviert ist oder der Anzeigenserver die Anzeige aufgrund von Verzögerungen nicht personalisieren kann. Schließen Sie pro Anzeigengröße, für die das Erlebnis gilt, ein kreatives Bild ein. Ihre Auswahl bestimmt die kreativen Größen, die für das Erlebnis verwendet werden können. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

Für Erlebnisse ohne Targeting mit Entscheidungsbäumen können Sie die standardmäßigen Kreativen mit Kreativen derselben Größe in [!UICONTROL Tag Manager] überschreiben.<!-- verify -->

* Um ein Standardkreativ mit verschiedenen Dimensionen hinzuzufügen, klicken Sie auf **[!UICONTROL + Add Sizes]**, aktivieren Sie im rechten Bereich die Kontrollkästchen neben den einzelnen Kreativen, die hinzugefügt werden sollen, und klicken Sie dann auf **[!UICONTROL Add Creatives]**.

* Um ein Standardkreativ zu löschen, halten Sie den Cursor über die kreative Miniaturansicht und klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen").

* Um alle standardmäßigen Kreativen zu löschen, klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen") **[!UICONTROL Delete all]**.

* Um den Kreativbereich auf der rechten Seite ein- oder auszublenden, klicken Sie ![Anzeigen/Ausblenden](/help/creative/assets/hide-show-creatives.png "Anzeigen/Ausblenden") oben rechts im rechten Bereich.

## [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Schreibgeschützt für vorhandene Erlebnisse) Trifft nicht zu, wenn Sie die Zielgruppenbestimmung nicht mithilfe eines Entscheidungsbaums aktivieren möchten; deaktivieren Sie diese Option.

**[!UICONTROL Dynamic ads]:** (Schreibgeschützt für vorhandene Erlebnisse) Gibt an, dass das Erlebnis dynamische Anzeigen enthält. **Hinweis:** Ein Erlebnis kann entweder alle Standardanzeigen oder alle dynamischen Anzeigen enthalten.

**[!UICONTROL Language Targeting]:** (Erlebnisse nur mit Standardanzeigen; optional; schreibgeschützt für vorhandene Erlebnisse) Überprüft die Browser-Spracheinstellungen des Benutzers und zeigt ein Kreativ in der angegebenen Sprache an, wenn ein Kreativ in dieser Sprache verfügbar ist. Wenn kein Kreativ in der im Browser angegebenen Sprache verfügbar ist, wird stattdessen die [!UICONTROL Preferred language] verwendet. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

**[!UICONTROL Preferred language]:** (Erlebnisse nur mit Standardanzeigen; schreibgeschützt für vorhandene Erlebnisse) Die Sprache für alle aus dem Erlebnis erstellten Anzeigen, es sei denn, [!UICONTROL Language Targeting] ist aktiviert. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

## [!UICONTROL Advanced]

**Datenübergabe:** (Nur Erlebnisse mit dynamischen Anzeigen; optional) Um Benutzende auf der Grundlage bestimmter Schlüssel-Wert-Paare anzusprechen, die DSP, Publisher oder Partner in Echtzeit nach der Impression übergeben. Es können bis zu fünf Datenübergabeschlüssel (Parameter) angegeben werden.<!-- May move this to just within the decision tree. -->

Wenn Sie später ein Anzeigen-Erlebnis-Tag für eine bestimmte kreative Größe erstellen, wird jeder Schlüssel, der in diesem Feld angegeben ist, als Makro im -Tag angehängt. Sie müssen den Wert für jedes Schlüssel-Wert-Paar innerhalb des Tags eingeben, bevor Sie das Tag als Anzeige in Ihrer DSP implementieren.

**Radius:** (Nur Erlebnisse mit dynamischen Anzeigen; optional) Ein Radius von einer US-Postleitzahl, die in der zu zielenden Feed-Datei angegeben ist; wählen Sie einen Radius von 0 Meilen bis 200 Meilen aus. Die Feed-Datei, die zur Erstellung der dynamischen Anzeigen für das Erlebnis verwendet wird, muss eine [!UICONTROL ZIP] Spalte <!-- or a user-named column mapped to a ZIP column -->, die für jede Produktzeile in der Datei einen Wert enthält. Beispielsweise kann eine Anzeige für ein in 95110 verfügbares Produkt im Umkreis von 10 Meilen für Benutzende im Umkreis von 10 Meilen von 95110 angezeigt werden (bestimmt durch die IP-Adresse des/r Benutzenden).

**RT Pixel:** (Erlebnisse nur mit dynamischen Anzeigen; optional) Ein [!UICONTROL Creative] Retargeting-Pixel zum potenziellen Targeting. Wenn Sie das Targeting innerhalb des Entscheidungsbaums einrichten, können Sie eine Ebene von RT-Pixel-Zielknoten einbeziehen und das Pixel angeben, das für jeden Knoten anvisiert werden soll, sowie die erforderlichen Werte für die Attribute des Pixels, die vorhanden sein müssen, um die Kreativen in den zugewiesenen kreativen Bundles anzuzeigen. Wenn Sie in diesem Feld kein Pixel angeben, können Sie dennoch eines innerhalb des Entscheidungsbaums angeben.&lt;!— Von R: „Das RT-Pixel sollte über die Inhaltsauswahl in der dynamischen Anzeigeneinrichtung sein“ — klären Sie auf. Ich sehe „Datapass“ (ein Wort) in den dynamischen Anzeigeneinstellungen, aber ich bin mir nicht sicher, wie diese Einstellung und diese Erlebnisebene zusammenarbeiten. —>

**[!UICONTROL Label]:** <!-- should be "Labels" --> (Optional) Alle [!DNL Creative] Kennzeichnungen, die auf das Erlebnis angewendet werden sollen. Sie können Erlebnisse in der Ansicht Erlebnisse nach <!-- sic --> filtern.

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
