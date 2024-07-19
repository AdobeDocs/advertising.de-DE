---
title: Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle
description: Erfahren Sie mehr über die Schritte, die Sie ausführen müssen, bevor Sie eine [!DNL Google Analytics] Datenquelle konfigurieren.
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Voraussetzungen für die Konfiguration einer [!DNL Google Analytics]-Datenquelle

Bevor Sie eine [!DNL Google Analytics] -Datenquelle einrichten können, müssen Sie den Abfragezeichenfolgenparameter &quot;ef_id&quot;von Search, Social und Commerce als Primärschlüssel einrichten, um Daten von [!DNL Google Analytics] an Search, Social und Commerce zu übergeben. Richten Sie den Primärschlüssel für jede [!DNL Google Analytics] -Konto- und Eigenschaftskombination ein, für die Sie Daten synchronisieren möchten. Möglicherweise müssen andere Mitarbeiter in Ihrer Organisation diese Aufgaben ausführen. Weitere Informationen finden Sie unten.

Wenn die Landingpage-URLs für Ihre Anzeigen oder Suchbegriffe nicht bereits Umleitungen in Search, Social und Commerce enthalten, fügen Sie sie zuerst hinzu.

## Voraussetzung 1: Implementieren Sie ein Search-, Social- und Commerce-Token ( Abfragezeichenfolgenparameter &quot;ef_id&quot;) in die Landingpage-URLs für alle anwendbaren Werbekonten

Bei jedem Paid-Search-Klick für die relevanten Kampagnen muss ein eindeutiger `ef_id` generiert und als Abfragezeichenfolge an die URL der Landingpage angehängt werden, wobei `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s` der Wert für das angehängte Symbol, den Schlüssel `ef_id` und den Wert für `ef_id` ist. `&ef_id=abcde:123456789:s` Um eine ef_id einzuschließen, müssen die entsprechenden Anzeigennetzwerkkonten und -kampagnen die [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; und die [!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot; aufweisen.

Für bestehende Konten und Kampagnen ist die ef_id wahrscheinlich bereits implementiert.

Wenn die ef_id nicht enthalten ist, bitten Sie Ihr Adobe-Account-Team um Hilfe.

Wenn alle Voraussetzungen erfüllt sind, wird `ef_id` als Primärschlüssel verwendet, um Daten von [!DNL Google Analytics] an Search, Social und Commerce zu übergeben.

## Voraussetzung 2: Erfassen des Such-, Social- und Commerce-Tokens ( Abfragezeichenfolgenparameter &quot;ef_id&quot;) in einer benutzerdefinierten Dimension für jede relevante [!DNL Google Analytics]-Eigenschaft

Wiederholen Sie die folgenden Aufgaben für jede [!DNL Google Analytics] -Konto- und -Eigenschaftskombination, für die Sie Daten synchronisieren möchten. Hilfe zu diesen Aufgaben finden Sie in der [[!DNL Google Analytics] Dokumentation zum Erstellen und Implementieren benutzerdefinierter Dimensionen](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) .

1. Erstellen Sie in [!DNL Google Analytics] eine benutzerdefinierte Dimension mit dem Namen &quot;`ef_id`&quot;. Legen Sie den Umfang der Dimension auf &quot;[!DNL User]&quot;fest und setzen Sie die Dimension auf &quot;aktiv&quot;.

   >[!NOTE]
   >
   >Für diese Voraussetzung ist eine Bearbeitungsberechtigung für die entsprechenden Eigenschaften erforderlich.

1. Aktualisieren Sie Ihren [!DNL Google Analytics]-Trackingcode, um den Wert des Abfragezeichenfolgenparameters ef_id zu erfassen, wenn er in der URL der Landingpage vorhanden ist, und ihn in der benutzerdefinierten Dimension ef_id zu speichern.

   >[!NOTE]
   >
   >Die ef_id sollte sich nur in Landingpage-URLs befinden.

   Wenn die Landingpage-URL beispielsweise `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf` ist, ist der Wert der Dimension ef_id in [!DNL Google Analytics] `abcde:123456789:s`.

   >[!NOTE]
   >
   >Diese Voraussetzung sollte von einem qualifizierten Entwickler erfüllt werden.

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung von [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Konfigurieren einer [!DNL Google Analytics] Ansicht als Datenquelle](data-source-configure.md)
>* [Bearbeiten einer [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren einer  [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
