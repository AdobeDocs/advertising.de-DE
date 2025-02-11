---
title: Einstellungen für zielgerichtete Erlebnisse
description: Siehe Beschreibungen aller Einstellungen für zielgerichtete Anzeigenerlebnisse.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 40a8afc7ec8d880137493118efb122778704eb8c
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Einstellungen für zielgerichtete Anzeigen-Erlebnisse

*Geschlossene Beta-Version*

## [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Schreibgeschützt für vorhandene Erlebnisse) Der Advertiser, der für die in dem Erlebnis enthaltenen Kreativ- und Zielkombinationen bietet. Nachdem Sie das Erlebnis gespeichert haben, können Sie den Advertiser nicht mehr ändern.

**[!UICONTROL Experience Name]:** Ein eindeutiger Name für das Erlebnis. **Tipp:** Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie das Erlebnis als Anzeige in Advertising DSP oder einer anderen DSP verwenden.

**[!UICONTROL Creative Library]:** (Schreibgeschützt für vorhandene Erlebnisse) Eine einzelne Kreativbibliothek, die für das Erlebnis verwendet werden soll. Nachdem Sie das Erlebnis gespeichert haben, können Sie die Bibliothek nicht mehr ändern.

## [!UICONTROL Default creatives]

**\[Angegebene Standardkreative\]:** Die Standardbildkreativen, die verwendet werden, wenn ein Browser keine dem Erlebnis zugewiesenen Kreativen anzeigen kann, z. B. wenn der Browser nicht JavaScript aktiviert ist oder der Anzeigenserver die Anzeige aufgrund von Verzögerungen nicht personalisieren kann. Schließen Sie pro Anzeigengröße, für die das Erlebnis gilt, ein kreatives Bild ein. Ihre Auswahl bestimmt die kreativen Größen, die für das Erlebnis verwendet werden können.<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

Für Erlebnisse mit Entscheidungsbaum-Targeting können Sie die standardmäßigen Kreativen mit Kreativ-Bundles überschreiben, die Kreative derselben Größe aus dem Entscheidungsbaum enthalten.<!-- verify -->

* Um ein Standardkreativ mit verschiedenen Dimensionen hinzuzufügen, klicken Sie auf **[!UICONTROL + Add Sizes]**, aktivieren Sie im rechten Bereich die Kontrollkästchen neben den einzelnen Kreativen, die hinzugefügt werden sollen, und klicken Sie dann auf **[!UICONTROL Add Creatives]**.

* Um ein Standardkreativ zu löschen, halten Sie den Cursor über die kreative Miniaturansicht und klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen").

* Um alle standardmäßigen Kreativen zu löschen, klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen") **[!UICONTROL Delete all]**.

* Um den Kreativbereich auf der rechten Seite ein- oder auszublenden, klicken Sie ![Anzeigen/Ausblenden](/help/creative/assets/hide-show-creatives.png "Anzeigen/Ausblenden") oben rechts im rechten Bereich.

## [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Schreibgeschützt für vorhandene Erlebnisse) Aktiviert das kreative Targeting mithilfe eines Entscheidungsbaums und der automatischen Tag-Erstellung. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

**[!UICONTROL Dynamic ads]:** (Schreibgeschützt für vorhandene Erlebnisse) Gibt an, dass das Erlebnis dynamische Anzeigen enthält. **Hinweis:** Ein Erlebnis kann entweder alle Standardanzeigen oder alle dynamischen Anzeigen enthalten. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

**[!UICONTROL Language Targeting]:** (Erlebnisse nur mit Standardanzeigen; optional; schreibgeschützt für vorhandene Erlebnisse) Überprüft die Browser-Spracheinstellungen des Benutzers und zeigt ein Kreativ in der angegebenen Sprache an, wenn ein Kreativ in dieser Sprache verfügbar ist. Wenn kein Kreativ in der im Browser angegebenen Sprache verfügbar ist, wird stattdessen die [!UICONTROL Preferred language] verwendet.

Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

**[!UICONTROL Preferred language]:** (Erlebnisse nur mit Standardanzeigen; schreibgeschützt für vorhandene Erlebnisse) Die Sprache für alle aus dem Erlebnis erstellten Anzeigen, es sei denn, [!UICONTROL Language Targeting] ist aktiviert. Nachdem Sie das Erlebnis gespeichert haben, können Sie diese Einstellung nicht mehr ändern.

## [!UICONTROL Advanced]

**Datenübergabe:** (Schreibgeschützt für vorhandene Erlebnisse; optional) Um Benutzende auf der Grundlage bestimmter Schlüssel-Wert-Paare anzusprechen, die DSP, Publisher oder Partner in Echtzeit bei einer Impression übergeben. Es können bis zu fünf Datenübergabeschlüssel (Parameter) angegeben werden. Wenn Sie die Zielgruppenbestimmung im Entscheidungsbaum einrichten, können Sie eine Ebene von Daten einbeziehen, um Zielknoten zu übergeben, und die Werte angeben, die für jeden Knoten anvisiert werden sollen. Wenn Sie beim Erstellen des Erlebnisses keinen Schlüssel in diesem Feld angeben, können Sie trotzdem einen Schlüssel in der Entscheidungsstruktur angeben.<!-- May move this to just within the decision tree.  -->

Jeder Schlüssel wird in der Anzeige als Makro angehängt
-Tag, das Sie generieren können, um es als Anzeige in Ihrer DSP zu implementieren.

**Radius:** (Erlebnisse nur mit dynamischen Anzeigen; optional) Ein Benutzerradius, der anvisiert werden soll. Wählen Sie einen Radius von 0 Meilen bis 200 Meilen.<!-- Affect within the decision tree? -->

**RT Pixel:** (Schreibgeschützt für vorhandene Erlebnisse; optional) Ein [!UICONTROL Creative] Retargeting-Pixel zum potenziellen Targeting. Wenn Sie das Targeting innerhalb des Entscheidungsbaums einrichten, können Sie eine Ebene von RT-Pixel-Zielknoten einbeziehen und das Pixel angeben, das für jeden Knoten anvisiert werden soll, sowie die erforderlichen Werte für die Attribute des Pixels, die vorhanden sein müssen, um die Kreativen in den zugewiesenen kreativen Bundles anzuzeigen. Wenn Sie beim Erstellen des Erlebnisses kein Pixel in diesem Feld angeben, können Sie dennoch eines innerhalb der Entscheidungsstruktur angeben.<!-- May move this to just within the decision tree. -->

**Beschriftung:** <!-- should be "Labels" --> (Optional) Alle [!DNL Creative] Beschriftungen, die auf das Erlebnis angewendet werden sollen. Sie können Erlebnisse in der Ansicht Erlebnisse nach <!-- sic --> filtern.

* Um vorhandene Kennzeichnungen auszuwählen, klicken Sie ![Nach unten](/help/creative/assets/chevron-down.png "Nach unten") und aktivieren Sie das Kontrollkästchen neben den einzelnen Kennzeichnungen, die angewendet werden sollen.

* Um nach vorhandenen Kennzeichnungen zu suchen, geben Sie eine Textzeichenfolge innerhalb des Kennzeichnungsnamens ein.

* Um eine neue anzuwendende Kennzeichnung zu erstellen, öffnen Sie die Liste, klicken Sie auf **+ Bezeichnung hinzufügen** geben Sie einen neuen Kennzeichnungsnamen in das Feld [!UICONTROL Label] ein und klicken Sie dann auf **Erstellen**.

* Um eine Bezeichnung zu entfernen, deaktivieren Sie das Kontrollkästchen neben dem Namen der Bezeichnung.

**Impression-Tracking-URL:** (Optional) Eine Impression-Tracking-URL eines Drittanbieters, die für jede aus dem Erlebnis erstellte Anzeige an die Landingpage-URL angehängt werden soll. Sie können bis zu fünf URLs einschließen. Um eine zusätzliche URL hinzuzufügen, klicken Sie auf ![Symbol](/help/creative/assets/create.png) **[!UICONTROL Add More] und geben Sie die URL ein.

Sobald Sie eine URL eingeben, werden [verfügbaren Makros](/help/creative/creative-macros.md) und die Daten, mit denen sie ersetzt werden, weiter unten auf der Seite aufgeführt. Um eines der Makros in die URL einzufügen, halten Sie den Cursor über die Makrobeschreibung und klicken Sie auf ![In Zwischenablage kopieren](/help/creative/assets/copy-to-clipboard.png "In Zwischenablage kopieren") und fügen Sie das Makro dann an der gewünschten Stelle in das URL-Feld ein.

>[!NOTE]
>
>* [!DNL Creative] stellt der Landingpage-URL automatisch seine eigenen Impression-Tracking-Tags als Präfix voran.
>* Sie können [diese URL für jeden Kreativen im Erlebnis überschreiben](experience-tracking-urls-targeting.md).
>* Sie können auch den Impression-Tracking-Code eines Drittanbieters für JavaScript im Feld [!UICONTROL Client JS] eingeben

**Klick-Tracking-URL:** (Optional) (Optional) Eine Klick-Tracking-URL eines Drittanbieters, die an die Landingpage-URL angehängt werden soll. Sie können bis zu fünf URLs einschließen. Um eine zusätzliche URL hinzuzufügen, klicken Sie auf ![Symbol](/help/creative/assets/create.png) **[!UICONTROL Add More] und geben Sie die URL ein.

Sobald Sie eine URL eingeben, werden [verfügbaren Makros](/help/creative/creative-macros.md) und die Daten, mit denen sie ersetzt werden, weiter unten auf der Seite aufgeführt. Um eines der Makros in die URL einzufügen, halten Sie den Cursor über die Makrobeschreibung und klicken Sie auf ![In Zwischenablage kopieren](/help/creative/assets/copy-to-clipboard.png "In Zwischenablage kopieren") und fügen Sie das Makro dann an der gewünschten Stelle in das URL-Feld ein.

>[!NOTE]
>
>* [!DNL Creative] stellt der Landingpage-URL automatisch seine eigenen Impression-Tracking-Tags als Präfix voran.
>* Sie können [diese URL für jeden Kreativen im Erlebnis überschreiben](experience-tracking-urls-targeting.md).

**Client JS:** (optional) Eine der folgenden Aktionen:

* (Wenn der Werbetreibende einen OBA-Compliance-Anbieter für die Anzeigen verwendet) JavaScript-Code, der auf die Anzeigenüberlagerung verweist, mit der Benutzende das Targeting im Online-Verhalten (OBA) deaktivieren können.

* Jeder JavaScript-Impression-Trackingcode eines Drittanbieters, der an die Landingpage angehängt werden soll. **Hinweis:** Sie können auch eine Impression-Tracking-URL eines Drittanbieters in das Feld [!UICONTROL Impression Tracking URL] eingeben.

>[!MORELIKETHIS]
>
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Verfügbare Makros zum Tracking von URLs](/help/creative/creative-macros.md)
