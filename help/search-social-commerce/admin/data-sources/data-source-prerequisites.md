---
title: Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle
description: Erfahren Sie mehr über die Schritte, die Sie vor der Konfiguration einer Datenquelle  [!DNL Google Analytics]  müssen.
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle

Bevor Sie eine [!DNL Google Analytics] Datenquelle einrichten können, müssen Sie den Abfragezeichenfolgenparameter „ef_id“ für Search, Social und Commerce als Primärschlüssel festlegen, um Daten von [!DNL Google Analytics] an Search, Social und Commerce zu übergeben. Richten Sie den Primärschlüssel für jedes [!DNL Google Analytics] Konto und jede Eigenschaftskombination ein, für die Sie Daten synchronisieren möchten. Andere Personen in Ihrer Organisation müssen diese Aufgaben möglicherweise ausführen. Weitere Informationen finden Sie unten.

Wenn die Landingpage-URLs für Ihre Anzeigen oder Keywords noch keine Weiterleitungen aus den Bereichen Suche, Social und Commerce enthalten, fügen Sie sie zuerst hinzu.

## Voraussetzung 1: Implementieren eines Search-, Social- und Commerce-Tokens („ef_id“-Abfragezeichenfolgenparameter) in den Landingpage-URLs für alle anwendbaren Werbekonten

Bei jedem Klick auf die Paid Search für die entsprechenden Kampagnen muss ein eindeutiger `ef_id` generiert und als Abfragezeichenfolge an die Landingpage-URL angehängt werden, z. B. `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, wobei `&ef_id=abcde:123456789:s` das Anhangsymbol, `ef_id` und `ef_id` Wert ist. Um eine ef_id einzuschließen, müssen die relevanten Konten und Kampagnen des Werbenetzwerks die [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; und die [!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot; aufweisen.

Bei bestehenden Konten und Kampagnen ist die ef_id wahrscheinlich bereits implementiert.

Wenn die ef_id nicht enthalten ist, bitten Sie Ihr Adobe-Account-Team um Hilfe.

Wenn alle Voraussetzungen erfüllt sind, wird die `ef_id` als Primärschlüssel verwendet, um Daten von [!DNL Google Analytics] an Search, Social und Commerce zu übergeben.

## Voraussetzung 2: Erfassen Sie das Token Search, Social und Commerce („ef_id“-Abfragezeichenfolgenparameter) in einer benutzerdefinierten Dimension für jede relevante [!DNL Google Analytics]

Wiederholen Sie die folgenden Aufgaben für jede Kombination aus [!DNL Google Analytics] und Eigenschaft, für die Sie Daten synchronisieren möchten. Siehe [[!DNL Google Analytics] Dokumentation zum Erstellen und Implementieren benutzerdefinierter Dimensionen](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) für Hilfe bei diesen Aufgaben.

1. Erstellen Sie [!DNL Google Analytics] eine benutzerdefinierte Dimension mit dem Namen &quot;`ef_id`&quot;. Legen Sie den Umfang der Dimension auf [!DNL User] und die Dimension auf Aktiv fest.

   >[!NOTE]
   >
   >Diese Voraussetzung erfordert die Berechtigung zum Bearbeiten für die entsprechenden Eigenschaften.

1. Aktualisieren Sie Ihren [!DNL Google Analytics]-Trackingcode, um den Wert des Abfrageparameters „ef_id“ zu erfassen, wenn er in der Landingpage-URL vorhanden ist, und speichern Sie ihn in der benutzerdefinierten Dimension „ef_id“.

   >[!NOTE]
   >
   >Die ef_id sollte nur in Landingpage-URLs angegeben werden.

   Wenn beispielsweise die Landingpage-URL `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf` ist, wird der Wert der Dimension ef_id in [!DNL Google Analytics] `abcde:123456789:s`.

   >[!NOTE]
   >
   >Diese Voraussetzung sollte von einem qualifizierten Entwickler erfüllt werden.

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare  [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
