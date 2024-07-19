---
title: Konfigurieren einer [!DNL Google Analytics] Ansicht als Datenquelle
description: Erfahren Sie, wie Sie eine Datenquelle über eine [!DNL Google Analytics] Ansicht konfigurieren.
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Konfigurieren einer [!DNL Google Analytics] -Ansicht als Datenquelle

*Nur Agentur-Administratoren, Agenturkontomanager, Adobe-Account-Manager und Administratoren*

Sie können pro [!DNL Google Analytics] -Konto, -Eigenschaft und -Ansichtskombination eine Datenquelle erstellen.

Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

1. [Führen Sie alle Voraussetzungen für die Integration des [!DNL Google Analytics] Kontos](data-source-prerequisites.md) aus.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Aktivieren Sie im Dialogfeld [!UICONTROL Deployment Prerequisites] das Kontrollkästchen, um zu bestätigen, dass die erforderliche benutzerdefinierte Dimension &quot;ef_id&quot;im [!DNL Google Analytics]-Konto implementiert ist, und klicken Sie dann auf **[!UICONTROL Continue]**.

   Einige Voraussetzungen wurden möglicherweise von anderen Rollen in Ihrer Organisation erfüllt. Wenn Sie Fragen zu den Voraussetzungen haben, wenden Sie sich an Ihr Adobe-Account-Team.

1. Geben Sie die [Datenquelleneinstellungen](data-source-settings.md) ein:

   1. Gehen Sie im Abschnitt **[!UICONTROL Connect to [!DNL Google Analytics]]** wie folgt vor:

      1. Geben Sie die numerische ID für das [!DNL Google Analytics] -Konto ein.

      1. Geben Sie die E-Mail-Adresse ein, die für den Zugriff auf Daten aus dieser Datenquelle verwendet werden soll. Die E-Mail-Adresse muss bei einem [!DNL Google] -Konto registriert sein und über die Berechtigung &quot;Lesen und Analysieren&quot;für das [!DNL Google Analytics] -Konto verfügen. Weitere Informationen finden Sie in den [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Um sicherzustellen, dass nur bestimmte [!DNL Google Analytics]-Eigenschaften und -Ansichten in Adobe Advertising verfügbar sind, melden Sie sich mit einer E-Mail-Adresse an, die nur Zugriff auf diese Eigenschaften und Ansichten hat.

         >[!NOTE]
         >
         >Wenn Sie später das Kennwort für dieses E-Mail-Konto ändern, werden alle offenen Verbindungen zum E-Mail-Konto geschlossen. Um die Synchronisierung der Daten fortzusetzen, kehren Sie zu dieser Seite zurück und [authentifizieren Sie sich erneut](data-source-reauthenticate.md).

      1. Aktivieren Sie das Kontrollkästchen, um Adobe Advertising für den Zugriff auf Metriken für das Konto zu autorisieren.

      1. Klicken Sie auf **[!UICONTROL Authenticate]**.

   1. Geben Sie im Abschnitt [!UICONTROL Account Details] die Eigenschaft und Ansicht für die zu importierenden Metriken an. Geben Sie außerdem die benutzerdefinierte Dimension an, die mit dem Wert des Abfragezeichenfolgenparameters &quot;ef_id&quot;gefüllt wird.

   1. Geben Sie im Abschnitt [!UICONTROL Import Metrics] die Metriken an, die in die Feeds aufgenommen werden sollen.

      Sie können nicht [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] oder [!UICONTROL Session Duration] entfernen, die automatisch enthalten sind. Sie können bis zu 16 weitere gültige Metriken oder Metriken ohne Daten hinzufügen.

      >[!WARNING]
      >
      >[!DNL Google Analytics] erlaubt bis zu 10 Metriken in einem einzelnen Daten-Feed. Search, Social und Commerce können bis zu zwei Feeds mit insgesamt 20 Metriken unterstützen. Die Verwendung eines zweiten Feeds verdoppelt jedoch Ihre API-Aufrufe auf [!DNL Google Analytics]. Wenn Sie viele Metriken haben, wählen Sie nur die Metriken aus, die Sie zur Optimierung in Zielen verwenden möchten. Weitere Informationen zu [Kontingenten und Aufrufbeschränkungen für API-Anfragen an  [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Geben Sie im Abschnitt [!UICONTROL Metric Tag] den Namen des Tags ein, das an jede Metrik für die Datenquelle angehängt werden soll.

1. Klicken Sie oben rechts auf **[!UICONTROL Post]**.

   Die Datenquelle heißt &quot;AccountName > PropertyName > ViewName&quot; und wird automatisch aktiviert. Informationen zum Anhalten der Datenquelle finden Sie unter &quot;[Anhalten eines Feeds von einer Data Source](data-source-pause.md)&quot;.

   Die Metriken sind am nächsten Tag nach Abschluss der täglichen Datensynchronisation verfügbar, die um 05:00 Uhr in der Zeitzone des Advertisers beginnt. Sobald die Metriken verfügbar sind, sind sie in [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) sichtbar. Jede neue Konversionsmetrik erhält den Namen &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, wobei &quot;backEndMetricName&quot;der von der API verwendete Metrikname ist. Der Anzeigename für jede neue Konversionsmetrik ist &quot;`friendlyMetricName_ga:MetricTag`&quot;, wobei &quot;friendlyMetricName&quot;der Metrikname ist, der in [!DNL Google Analytics] angezeigt wird, und &quot;MetricTag&quot;der in den Datenquelleneinstellungen definierte [!UICONTROL Metric Tag].

   Sie können die Metriken direkt zu Kampagnen-Management- und Portfoliomanagementansichten, Berichten und Optimierungszielen hinzufügen.

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung von [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration einer  [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Bearbeiten einer [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren einer  [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
