---
title: HTML5 Creative Specification
description: Verweisen Sie auf die Kreativspezifikation HTML5 für Advertising Creative.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# HTML5 Creative Specification für Advertising Creative

In diesem Dokument werden die Anforderungen und die API-Unterstützung für HTML5-Kreative in [!DNL Creative] beschrieben. Die API ermöglicht die Entwicklung von HTML5-Kreativen, deren Attribute zum Zeitpunkt der kreativen Bereitstellung konfiguriert werden können.

## Umfang

[!DNL Creative] unterstützt HTML5-Banner mit nicht-Rich-Media-Kreativen, die innerhalb festgelegter Seitengrenzen angezeigt werden. Sie können die folgenden Arten von HTML5-Kreativen verwenden:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** Unterstützt bis zu 5 Landingpage-URLs, die während der kreativen Erstellung und des Traffics konfiguriert werden können.

* **Flexibles HTML5:** Unterstützt bis zu 5 Landingpage-URLs, die während der kreativen Erstellung und des Traffics konfiguriert werden können, und ermöglicht auch das Ändern von Kreativattributen während der kreativen Erstellung und des Traffics.

## Anforderungen

### Anforderungen an Ordner und Komprimierung

* Das Kreativ-Tool muss in einer ZIP-Datei (.ZIP-Format) verpackt sein. Verschachtelte ZIP-Dateien werden nicht unterstützt. Daher sollten Sie im äußeren komprimierten Ordner keinen komprimierten Ordner einschließen.

* Die ZIP-Datei muss mindestens eine HTML-Datei enthalten - die Haupt-HTML-Anzeigedatei -, die einen Verweis auf die [!DNL Creative] JavaScript-Bibliothek enthält. Die HTML-Hauptdatei kann sich entweder im Stammordner oder in einem Unterordner befinden.

* Die Haupt-HTML-Datei kann beliebig benannt werden, sofern sie keine Sonderzeichen enthält. `index.html` wird jedoch empfohlen.

* Alle unterstützenden Assets, die zum Rendern des endgültigen Kreativinhalts benötigt werden, müssen sich entweder im selben Ordner wie die HTML-Anzeigedatei oder in Unterordnern im Hauptordner befinden.

* Schließen Sie keine Dateien in das Kreativ-Tool ein, auf die für dieses Kreativ-Tool nicht verwiesen wird.

### Einbinden der Advertising Creative-JavaScript-Datei

Die HTML-Hauptdatei - und keine anderen Dateien - müssen einen Verweis auf die JavaScript-`AMOLibrary.js` enthalten. Rufen Sie die Datei in der ersten Zeile des `<head>` Abschnitts mit der folgenden Adresse auf:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Diese Datei enthält Funktionen, mit denen sichergestellt wird, dass das lokale Testen von Exit-Ereignissen problemlos erfolgt.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5 Creative Requirements

#### Unterstützung für Clickthrough-URLs in statischem HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registriert die Clickthrough-URLs und die zugehörigen Parameter, die zum Verweisen auf jede URL verwendet werden (als `clickTag` bezeichnet). Dies informiert den [!DNL Creative]-Anzeigen-Server darüber, wo Klick-Tracking hinzugefügt werden soll. Mit dieser API können Sie bis zu fünf Klick-Tag-Variablen mit jeweils einer entsprechenden Landingpage-URL registrieren.

>[!NOTE]
>
>Die statischen URLs, die Sie in die kreative HTML5-Datei aufnehmen, werden nur zu lokalen Testzwecken verwendet und werden überschrieben. Wenn Sie eine HTML5-Kreativseite hochladen, definieren Sie die standardmäßige Landingpage für jede `clickTag`. Wenn Sie einem Werbeerlebnis eine hochgeladene kreative HTML5 zuweisen, können Sie optional die standardmäßige Landingpage für jede `clickTag`-Variable überschreiben und [!DNL Creative] beim Speichern des Erlebnisses Klick-Tracking zu den URLs hinzufügen.

###### Parameter

* `clkVar` - Der Name der Click-Variablen (normalerweise „clickTag„), in doppelte Anführungszeichen gesetzt.

* `clkUrl` - Die Landingpage-URL für diese Klick-Variable, eingeschlossen in doppelten Anführungszeichen.

###### Nutzung

Rufen Sie `amo.registerClick()` im `<head>` Abschnitt der HTML-Hauptdatei auf.

###### Beispiel

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Trigger des Exit-Ereignisses, das den Benutzer zur für die `clickTag` konfigurierten Landingpage weiterleitet. Während des lokalen Tests warnt diese Funktion Entwickler, ob die URL, die an die Funktion übergeben wird, registriert wurde.

###### Parameter

* `clkTag` - Der Name der Klickvariablen, die Sie verwenden, um die Landingpage-URL mithilfe der `amo.registerClick()` zuzuweisen, eingeschlossen in einfachen Anführungszeichen.

* `event` - (Optional) Das JavaScript-Klick-Ereignisobjekt. Dadurch werden die Koordinaten der Klicks aufgezeichnet, die zur weiteren Analyse der kreativen Leistung verwendet werden können.

###### Nutzung

Rufen Sie `amo.onAdClick()` im `<body>` Abschnitt der HTML-Hauptdatei auf.

###### Beispiele

`amo.onAdClick('clickTag')` ODER `amo.onAdClick('clickTag',clickEvt)`

### Flexible HTML5-Kreativanforderungen

#### Unterstützung für Clickthrough-URLs in flexiblem HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registriert die Clickthrough-URLs und die zugehörigen Parameter, die zum Verweisen auf jede URL verwendet werden (als `clickTag` bezeichnet). Dies informiert den [!DNL Creative]-Anzeigen-Server darüber, wo Klick-Tracking hinzugefügt werden soll. Mit dieser API können Sie bis zu fünf Klick-Tag-Variablen mit jeweils einer entsprechenden Landingpage-URL registrieren.

>[!NOTE]
>
>Die statischen URLs, die Sie in die kreative HTML5-Datei aufnehmen, werden nur zu lokalen Testzwecken verwendet und werden überschrieben. Wenn Sie eine HTML5-Kreativseite hochladen, definieren Sie die standardmäßige Landingpage für jede `clickTag`. Wenn Sie einem Werbeerlebnis eine hochgeladene kreative HTML5 zuweisen, können Sie optional die standardmäßige Landingpage für jede `clickTag`-Variable überschreiben und [!DNL Creative] beim Speichern des Erlebnisses Klick-Tracking zu den URLs hinzufügen.

###### Parameter

* `clkVar` - Der Name der Click-Variablen (normalerweise „clickTag„), in doppelte Anführungszeichen gesetzt.

* `clkUrl` - Die Landingpage-URL für diese Klick-Variable, eingeschlossen in doppelten Anführungszeichen.

###### Nutzung

Rufen Sie `amo.registerClick()` im `<head>` Abschnitt der HTML-Hauptdatei auf.

###### Beispiel

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Trigger des Exit-Ereignisses, das den Benutzer zur für die `clickTag` konfigurierten Landingpage weiterleitet. Während des lokalen Tests warnt diese Funktion Entwickler, ob die URL, die an die Funktion übergeben wird, registriert wurde.

###### Parameter

* `clkTag` - Der Name der Klickvariablen, die Sie verwenden, um die Landingpage-URL mithilfe der `amo.registerClick()` zuzuweisen, eingeschlossen in einfachen Anführungszeichen.

* `event` - (Optional) Das JavaScript-Klick-Ereignisobjekt. Dadurch werden die Koordinaten der Klicks aufgezeichnet, die zur weiteren Analyse der kreativen Leistung verwendet werden können.

###### Nutzung

Rufen Sie `amo.onAdClick()` im `<body>` Abschnitt der HTML-Hauptdatei auf.

###### Beispiele

`amo.onAdClick('clickTag')` ODER `amo.onAdClick('clickTag',clickEvt)`

#### Unterstützung für kreative Attribute in flexiblem HTML5

##### `amo.registerAttribute(key, type, value)`

Definiert Attribute der Kreativen, die beim Erstellen von Kreativen oder Erlebnissen geändert werden können. Sie können bis zu 20 kreative Attribute definieren, die zum Zeitpunkt der Kreativ- oder Erlebniserstellung konfiguriert werden können.

>[!NOTE]
>
>Die in dieser Methode definierten Werte werden nur für die lokale Entwicklung verwendet und nicht in der Live-Schaltung von Anzeigen verwendet.

###### Parameter

* `key` - Der alphanumerische Name des Attributs. Sie muss mit einem Buchstaben beginnen.

* `type` - Der Typ des Attributs (`TEXT` oder `IMAGE`).

* `value` - Der Wert des Attributs für Tests. Bei Attributen des Typs `IMAGE` muss der Wert der relative Pfad zur Bilddatei sein.

###### Nutzung

Rufen Sie `amo.registerAttribute()` auf, um ein kreatives Attribut, einen Typ und einen Wert während des Tests im lokalen Modus zu registrieren. Alle Bilddateien, die als Beispielwerte verwendet werden, sollten zusammen mit dem hochgeladenen Paket in die ZIP-Datei gepackt werden.

##### `amo.attributes`

Ein JSON-Objekt zum Abfragen der Namen und Werte der Variablen des kreativen Attributs. Die Objektschlüssel sind die Attributnamen und die Werte sind die Werte dieser Attribute.

Im lokalen Testmodus sind die Schlüssel-Wert-Paare die Paare, die von der `amo.registerAttribute`-API registriert werden. Für die Produktion müssen die Namen und Werte der kreativen Attributvariablen zum Zeitpunkt der kreativen Erstellung und des Handels konfiguriert werden.

### Anforderungen an kreative Inhalte

Die meisten der in Advertising DSP verfügbaren Anzeigeaustauschprogramme haben die folgenden kreativen Anforderungen:

* Alle Anzeigenbilder müssen von einem festen Rahmen umgeben sein.

* Das Erweitern von Anzeigen ist nicht zulässig.

* Die Landingpage muss in einem neuen Fenster geöffnet werden.

* Die Landingpage-Domain und ihre Subdomains dürfen nicht länger als 35 Zeichen sein. **Hinweis:** Die endgültigen Landingpage-URLs werden in der DSP und nicht in den HTML5-Assets selbst definiert.

* Alle Haftungsausschlüsse in Bezug auf das Angebot einer Anzeige müssen in der Anzeige selbst enthalten sein und nicht nur auf der Landingpage.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Beispielinhalt als JSON-Objekt und -Array

### Beispielinhalt als JSON-Objekt

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Beispielinhalt als JSON-Array

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Beispiel für HTML5 Creative

### Beispiel für Ordnerstruktur (nach der Dekomprimierung)

* index.html

* /assets (Ordner)

   * bg.jpg (JPG-, PNG-, SVG- oder GIF-Bild)

### Beispiel einer HTML-Datei (index.html) für einfache HTML5-Kreative

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Beispiel einer HTML-Datei (index.html) für statische HTML5-Kreative

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-standard.md)
