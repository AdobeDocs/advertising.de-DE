---
title: Über Ihre Kreativbibliotheken
description: Erfahren Sie mehr über die Verwaltung der Kreativen, die Sie in Ihren Anzeigenerlebnissen verwenden werden.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# Über Ihre Kreativbibliotheken

*Closed Beta-Funktion*

Mit Ihren Kreativ-Bibliotheken können Sie alle Kreativen verwalten, die Sie für Ihre Werberlebnisse verwenden werden. Sie können mehrere Bibliotheken mit jeweils einer Reihe von Kreativen und *Kreativ-Bundles* erstellen, bei denen es sich um Kreativgruppen handelt, die Sie einem Erlebnis als eine Einheit hinzufügen können.

Ihre Bibliotheken können Folgendes enthalten:

* **Individuelle Kreative:** Sie können einzelne Kreative direkt in Anzeigenerlebnisse einbeziehen, für die keine Benutzerziele definiert sind. Sie können Ihre Kreativen auch verwenden, um Bundles zu erstellen, die Sie in zielgerichtete ([) Erlebnisse ](/help/creative/experiences/experience-about.md) können.

   * **Standard-Kreative** Sie können Kreative in [verschiedenen Formaten) hochladen ](#creative-creative-formats) verwalten. Für jeden Kreativen geben Sie die Standardsprache für jede Anzeige an, mit der Sie das Kreative verknüpfen, die Standardlandingpage, die geöffnet wird, wenn ein Benutzer auf eine Anzeige klickt, die die kreativen und optionalen Beschriftungen enthält, die als Filter in verschiedenen Ansichten innerhalb von [!DNL Creative] verwendet werden sollen.

   * **Dynamische Kreative:** (Nur für bestehende Adobe Advertising DCO-Kunden) Administratoren können dynamisch generierte Kreative erstellen, indem sie dynamische Variablen in einer Anzeigenvorlage den Werten in einer Feed-Datei zuordnen. Alle Benutzer können vorhandene dynamische Anzeigen in der Vorschau anzeigen, duplizieren und löschen.

* **Kreativ-Bundles:** Kreative in Bundles zusammen, die für mehrere Erlebnisse mit definierten Benutzerzielen verwendet werden können. Sie können *Standard-Bundles* erstellen, die aus Standardanzeigen und *dynamischen Bundles* bestehen, die aus dynamisch generierten Anzeigen bestehen.

## Unterstützte Kreativformate {#creative-creative-formats}

### Formate für Standard-Kreative

Sie können die folgenden Kreativtypen in den [unterstützten Kreativgrößen“ hinzufügen und ](creative-sizes.md).

>[!IMPORTANT]
>
>Auch wenn Sie HTMl5, Flexible HTML5 oder Kreative von Drittanbietern für Ihre Werbeeinblendungen verwenden möchten, müssen Sie für jede verwendete Kreativgröße auch Bildkreative hinzufügen.
>
>Für jedes Erlebnis ist ein Standardbild erforderlich, das für jede dem Erlebnis zugewiesene Kreativgröße erstellt wird. Die Standardbildkreative werden verwendet, wenn ein Browser nicht JavaScript-fähig ist oder wenn der Anzeigenserver die Anzeige aufgrund von Verzögerungen nicht personalisieren kann.

#### Flexible HTML5

Flexible HTML5-Kreative sind HTML5-Kreative mit allen Bildern und anderen Attributen als Standard-HTML-Tags, die Sie direkt in [!DNL Creative] bearbeiten können, entweder in einer Kreativbibliothek oder in einem individuellen Erlebnis (wodurch eine Variation des Original-Kreativs erstellt wird). Flexible HTML5-Kreative verwenden den Standard des Interactive Advertising Bureau (IAB) Technology Laboratory für ein [Anzeigenportfolio](https://flexibleads.iabtechlab.com/), bei dem die Anzeigenformatgrößen flexibel (statt fest) sind und auf dem Seitenverhältnis und dem Größenbereich der Anzeige basieren und bei dem die Anzeigenauflösung geräteübergreifend und auf Veröffentlichungs-Sites beibehalten wird.

Sie können <!-- either --> flexible HTML5-Kreative als ZIP-Dateien hochladen<!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->. Siehe [Spezifikationen für flexible HTML5-Kreative](html5-creative-specification.md).

<!-- Will flattening the view be possible in the MVP?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

Sie können optional die Standardwerte der Attribute ändern, die in einem flexiblen HTML5-Kreativ angegeben sind. Später können Sie benutzerdefinierte Werte für die Attribute innerhalb eines bestimmten Erlebnisses angeben, wodurch eine Variante des übergeordneten kreativen Elements erstellt wird.

#### HTML5-Kreative

Sie können einfache oder statische HTML5-Kreative mit allen angegebenen Attributen und Bildern als ZIP-Dateien hochladen. Sie können keine Attribute bearbeiten oder Bilder hinzufügen. Laden Sie stattdessen eine neue ZIP-Datei hoch, um ein neues Kreativprofil hinzuzufügen. Siehe [Spezifikationen für einfache und statische HTML5-Kreative](html5-creative-specification.md).

#### Image-Kreative

Sie können Bildkreative im GIF-, JPEG-, JPG- oder PNG-Format einbeziehen. Sie können <!--LATER:   images from your Adobe Experience Manager accounts or --> Bilder von Ihrem Gerät oder Netzwerk hochladen.

Für jedes Werbeerlebnis ist ein Standardbild erforderlich, das für jede dem Erlebnis zugewiesene Kreativgröße erstellt wird.

#### Kreative von Drittanbietern

Geben Sie JavaScript-Tracking-Tags für Kreative ein, die auf Werbe-Servern von Drittanbietern gehostet werden. Das Skript variiert je nach Anzeigenserver. Das folgende Beispiel:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Format für dynamische Anzeigen

Adminbenutzer können dynamisch generierte Kreative im statischen HTML5- und dynamischen HTML5-Format erstellen, indem sie dynamische Variablen in einer Anzeigenvorlage den Werten in einer Feed-Datei zuordnen. Dazu können auch Kreative aus alten Adobe Advertising Dynamic Creative Optimization (DCO)-Erlebnissen gehören.

## Die [!UICONTROL Creative Libraries]

Weitere [ zum Anpassen der einzelnen Ansichten finden ](/help/creative/introduction/customize-data-views.md) unter „Anpassen der Datenansichten“.

### Die [!UICONTROL Creative Libraries] Hauptansicht

Die [!UICONTROL Creative Libraries] Hauptansichten zeigt alle Ihre Kreativbibliotheken an. Die Daten für jede Bibliothek umfassen die Anzahl der Erlebnisse, denen die Bundles der Bibliothek zugewiesen sind, die Anzahl der Bundles, die Anzahl der Kreativen, die Anzahl der kreativen Größen, die Anzahl der Standardsprachziele, das Erstellungsdatum und das letzte Änderungsdatum für ein Element der Bibliothek. Der Tabellenmodus enthält auch eine Spalte für den Advertiser.

#### Verfügbare Aktionen

* Erstellen neuer Bibliotheken

* Für jede Kreativbibliothek gilt Folgendes:

   * Bibliotheksnamen bearbeiten

   * Öffnen Sie die Bibliothek , um die der Bibliothek zugewiesenen Kreativen und Bundles anzuzeigen

   * Bibliothek löschen

### Die [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

Auf der Registerkarte [!UICONTROL Standard Ads] werden alle von Ihnen erstellten Standard-Kreativen angezeigt. Die Daten für jeden Kreativen umfassen die Kreativgröße, den Kreativtyp und das Erstellungsdatum. Der Tabellenmodus enthält auch Spalten für die Standardsprache und die standardmäßige Landingpage.

##### Verfügbare Aktionen

* [Hinzufügen von Standard-Kreativen zu einer Bibliothek](creative-add-standard.md)

* [Bearbeiten von Standard-Kreativen](creative-edit-standard.md)

* [Vorschau eines Standard-Kreativen anzeigen](creative-preview.md)

* [Standard-Kreative zu Standard-Bundles hinzufügen und Standard-Kreative aus einem Standard-Bundle entfernen](creative-attach-detach-bundles.md)

* [Standardkreative duplizieren](creative-duplicate.md)

* [Standard-Kreative herunterladen](creative-download.md)

* [Standard-Kreative löschen](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

Auf der Registerkarte [!UICONTROL Dynamic Ads] werden alle dynamischen Kreativen angezeigt, die dynamisch für Ihre Kreativkataloge erstellt wurden, mit Ausnahme der dynamischen Kreativen, die Sie [ der Registerkarte [!UICONTROL Dynamic Ads] manuell ](creative-delete.md) haben. Wenn Sie [manuell dupliziert](creative-duplicate.md) alle dynamischen Kreativen seit der letzten Verarbeitung eines Katalogs enthalten, enthält die Liste der Kreativen für diesen Katalog auch die doppelten Kreativen.

Die Daten für jedes Kreativ umfassen den Kreativtyp, die Größe des Kreativs, die Anzahl der Kataloge, zu denen das Kreativ gehört, und das Erstellungsdatum. Der Tabellenmodus enthält auch Spalten für die Vorlage, mit der die kreative Seite generiert wurde, und die Anzahl der Angebote.

>[!NOTE]
>
>Bei jeder Verarbeitung eines Katalogs werden die Daten der vorhandenen dynamischen Kreativen für diesen Katalog aktualisiert.

##### Verfügbare Aktionen

Die Möglichkeit, dynamische Kreative zu erstellen und zu bearbeiten, ist derzeit nur für das Adobe-Account-Team verfügbar. Alle Benutzer können jedoch:

* [Vorschau für dynamische Kreative](creative-preview.md)

* [Dynamische Kreative zu dynamischen Paketen hinzufügen und dynamische Kreative aus einem dynamischen Paket entfernen](creative-attach-detach-bundles.md)

* [Dynamische Kreative duplizieren](creative-duplicate.md)

* [Dynamische Kreative löschen](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### Die Ansicht [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

Die [!UICONTROL Bundles] zeigt alle standardmäßigen und dynamischen Bundle-Container an. Sie können die Kreativnamen, die Kreativgrößen und die Sprachen der in den einzelnen Bundles enthaltenen Kreativen anzeigen.

#### Verfügbare Aktionen

* Hinzufügen von standardmäßigen und dynamischen Bundles zu einer Bibliothek

* Auflisten und Vorschau der Kreativen in einem Bundle

* Bundle-Namen bearbeiten

* Standard-Kreative zu Standard-Bundles hinzufügen und Standard-Kreative aus einem Standard-Bundle entfernen

* Bundles duplizieren

* Bundles löschen

>[!MORELIKETHIS]
>
>* [Verwalten von Kreativbibliotheken](/help/creative/creative-libraries/creative-library-manage.md)
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](creative-add-standard.md)
>* [Verwalten von kreativen Bundles](bundle-manage.md)
>* [Anpassen der Datenansichten](/help/creative/introduction/customize-data-views.md)
