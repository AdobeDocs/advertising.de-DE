---
title: Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle
description: Erfahren Sie mehr über die Schritte, die Sie ausführen müssen, bevor Sie eine [!DNL Google Analytics] Datenquelle.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle

Bevor Sie eine [!DNL Google Analytics] Datenquelle: Sie müssen den Abfragezeichenfolgenparameter &quot;ef_id&quot;für Search, Social und Commerce als Primärschlüssel festlegen, aus dem Daten übergeben werden sollen [!DNL Google Analytics] zu &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;. Richten Sie den Primärschlüssel für jede [!DNL Google Analytics] Konto- und Eigenschaftskombination, für die Sie Daten synchronisieren möchten. Möglicherweise müssen andere Mitarbeiter in Ihrer Organisation diese Aufgaben ausführen. Weitere Informationen finden Sie unten.

Wenn die Landingpage-URLs für Ihre Anzeigen oder Suchbegriffe keine Umleitungen für Suche, Social und Commerce enthalten, fügen Sie sie zuerst hinzu.

## Voraussetzung 1: Implementieren Sie ein Search-, Social- und Commerce-Token ( Abfragezeichenfolgenparameter &quot;ef_id&quot;) in die URLs der Landingpage für alle zutreffenden Werbekonten

Klicken Sie bei jeder gebührenpflichtigen Suche nach den entsprechenden Kampagnen auf eine eindeutige `ef_id` muss generiert und als Abfragezeichenfolge an die Landingpage-URL angehängt werden, z. B. `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, wobei `&ef_id=abcde:123456789:s` das angehängte Symbol ist, `ef_id` Schlüssel und `ef_id` -Wert. Um eine ef_id einzuschließen, müssen die entsprechenden Anzeigennetzwerkkonten und -kampagnen über die Variable [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; und [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Für bestehende Konten und Kampagnen ist die ef_id wahrscheinlich bereits implementiert.

Wenn die ef_id nicht enthalten ist, bitten Sie Ihr Adobe Account Team um Hilfe.

Wenn alle Voraussetzungen erfüllt sind, wird die `ef_id` wird als Primärschlüssel zur Übergabe von Daten aus [!DNL Google Analytics] zu &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;.

## Voraussetzung 2: Erfassen Sie das Search-, Social- und Commerce-Token ( Abfragezeichenfolgenparameter &quot;ef_id&quot;) in einer benutzerdefinierten Dimension für jede relevante [!DNL Google Analytics] property

Wiederholen Sie die folgenden Schritte für jede [!DNL Google Analytics] Konto- und Eigenschaftskombination, für die Sie Daten synchronisieren möchten. Siehe [[!DNL Google Analytics] Dokumentation zum Erstellen und Implementieren benutzerdefinierter Dimensionen](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) Hilfe zu diesen Aufgaben.

1. In [!DNL Google Analytics]erstellen Sie eine benutzerdefinierte Dimension mit dem Namen`ef_id`&quot;. Legen Sie den Umfang der Dimension auf [!DNL User]und legen Sie die Dimension auf &quot;aktiv&quot;fest.

   >[!NOTE]
   >
   >Für diese Voraussetzung ist eine Bearbeitungsberechtigung für die entsprechenden Eigenschaften erforderlich.

1. Aktualisieren Sie Ihre [!DNL Google Analytics] Trackingcode , um den Wert des Abfragezeichenfolgenparameters ef_id zu erfassen, wenn er in der URL der Landingpage vorhanden ist, und ihn in der benutzerdefinierten Dimension ef_id zu speichern.

   >[!NOTE]
   >
   >Die ef_id sollte sich nur in Landingpage-URLs befinden.

   Wenn die Landingpage-URL beispielsweise `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, dann den Wert der Dimension ef_id in [!DNL Google Analytics] is `abcde:123456789:s`.

   >[!NOTE]
   >
   >Diese Voraussetzung sollte von einem qualifizierten Entwickler erfüllt werden.

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen](data-source-configure.md)
>* [Bearbeiten von [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbar [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)

