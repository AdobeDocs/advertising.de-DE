---
title: Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen
description: Erfahren Sie, wie Sie eine Datenquelle über eine [!DNL Google Analytics] anzeigen.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen

*Agentenadministratoren, Agenturkontomanager, Adobe Account Manager und nur Administratoren*

Sie können eine Datenquelle pro [!DNL Google Analytics] Kombination aus Konto, Eigenschaft und Ansicht.

Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

1. [Führen Sie alle Voraussetzungen für die Integration der [!DNL Google Analytics] account](data-source-prerequisites.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Im [!UICONTROL Deployment Prerequisites] aktivieren Sie das Kontrollkästchen, um zu bestätigen, dass die erforderliche benutzerdefinierte Dimension &quot;ef_id&quot;im [!DNL Google Analytics] und klicken Sie auf **[!UICONTROL Continue]**.

   Einige Voraussetzungen wurden möglicherweise von anderen Rollen in Ihrer Organisation erfüllt. Wenden Sie sich bei Fragen zu den Voraussetzungen an Ihr Adobe Account Team.

1. Geben Sie die [Datenquelleneinstellungen](data-source-settings.md):

   1. Im **[!UICONTROL Connect to [!DNL Google Analytics]]** -Abschnitt, führen Sie die folgenden Schritte aus.

      1. Geben Sie die numerische ID für die [!DNL Google Analytics] -Konto.

      1. Geben Sie die E-Mail-Adresse ein, die für den Zugriff auf Daten aus dieser Datenquelle verwendet werden soll. Die E-Mail-Adresse muss bei einem [!DNL Google] und über &quot;Lesen und Analysieren&quot;-Berechtigungen für die [!DNL Google Analytics] -Konto. Siehe [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >So stellen Sie sicher, dass nur bestimmte [!DNL Google Analytics] -Eigenschaften und -Ansichten in Adobe Advertising verfügbar sind, melden Sie sich mit einer E-Mail-Adresse an, die nur Zugriff auf diese Eigenschaften und Ansichten hat.

         >[!NOTE]
         >
         >Wenn Sie später das Kennwort für dieses E-Mail-Konto ändern, werden alle offenen Verbindungen zum E-Mail-Konto geschlossen. Kehren Sie zu dieser Seite zurück und [reauthenticate](data-source-reauthenticate.md).

      1. Aktivieren Sie das Kontrollkästchen, um den Adobe Advertising für den Zugriff auf Metriken für das Konto zu autorisieren.

      1. Klicken **[!UICONTROL Authenticate]**.

   1. Im [!UICONTROL Account Details] -Abschnitt die Eigenschaft und Ansicht für die zu importierenden Metriken angeben. Geben Sie außerdem die benutzerdefinierte Dimension an, die mit dem Wert des Abfragezeichenfolgenparameters &quot;ef_id&quot;gefüllt wird.

   1. Im [!UICONTROL Import Metrics] geben Sie die Metriken an, die in die Feeds aufgenommen werden sollen.

      Sie können [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces]oder [!UICONTROL Session Duration], die automatisch eingeschlossen werden. Sie können bis zu 16 weitere gültige Metriken oder Metriken ohne Daten hinzufügen.

      >[!WARNING]
      >
      >[!DNL Google Analytics] erlaubt bis zu 10 Metriken in einem einzigen Daten-Feed. Search, Social und Commerce können bis zu zwei Feeds mit insgesamt 20 Metriken unterstützen. Die Verwendung eines zweiten Feeds verdoppelt jedoch Ihre API-Aufrufe auf [!DNL Google Analytics]. Wenn Sie viele Metriken haben, wählen Sie nur die Metriken aus, die Sie zur Optimierung in Zielen verwenden möchten. Weitere Informationen [Kontingente und Aufrufbeschränkungen für API-Anfragen an [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Im [!UICONTROL Metric Tag] geben Sie den Namen des Tags ein, das an jede Metrik für die Datenquelle angehängt werden soll.

1. Klicken Sie oben rechts auf **[!UICONTROL Post]**.

   Die Datenquelle heißt &quot;AccountName > PropertyName > ViewName&quot; und wird automatisch aktiviert. Informationen zum Anhalten der Datenquelle finden Sie unter[Feed aus einer Datenquelle anhalten](data-source-pause.md).&quot;

   Die Metriken sind am nächsten Tag nach Abschluss der täglichen Datensynchronisation verfügbar, die um 05:00 Uhr in der Zeitzone des Advertisers beginnt. Sobald die Metriken verfügbar sind, sind sie in [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Jede neue Konversionsmetrik erhält den Namen`ga:backEndMetricName_propertyID_viewID`,&quot;wobei &quot;backEndMetricName&quot;der von der API verwendete Metrikname ist. Der Anzeigename für jede neue Konversionsmetrik lautet &quot;`friendlyMetricName_ga:MetricTag`,&quot;wobei &quot;friendlyMetricName&quot;der Metrikname ist, der in [!DNL Google Analytics] und &quot;MetricTag&quot;ist der [!UICONTROL Metric Tag] definiert in den Datenquelleneinstellungen.

   Sie können die Metriken direkt zu Kampagnen-Management- und Portfoliomanagementansichten, Berichten und Optimierungszielen hinzufügen.

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Bearbeiten von [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbar [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
