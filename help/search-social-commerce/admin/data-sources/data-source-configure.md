---
title: Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle
description: Erfahren Sie, wie Sie eine Datenquelle über eine  [!DNL Google Analytics]  konfigurieren.
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Konfigurieren einer [!DNL Google Analytics] als Datenquelle

*Nur Agenturadministratoren, Agenturkontomanager, Adobe-Kontomanager und Administratoren*

Sie können für jede Kombination aus Konto, Eigenschaft und Ansicht eine [!DNL Google Analytics] Datenquelle erstellen.

Um Metriken für mehrere Eigenschaften oder für mehrere Ansichten für eine einzelne Eigenschaft zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein.

1. [Führen Sie alle Voraussetzungen für die Integration des  [!DNL Google Analytics] -Kontos ](data-source-prerequisites.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Aktivieren Sie im Dialogfeld [!UICONTROL Deployment Prerequisites] das Kontrollkästchen, um zu bestätigen, dass die erforderliche benutzerdefinierte Dimension „ef_id“ im [!DNL Google Analytics] implementiert ist, und klicken Sie dann auf **[!UICONTROL Continue]**.

   Einige Voraussetzungen wurden möglicherweise von anderen Rollen in Ihrer Organisation erfüllt. Wenden Sie sich bei Fragen zu den Voraussetzungen an Ihr Adobe-Account-Team.

1. Geben Sie die [Datenquelleneinstellungen“ ](data-source-settings.md):

   1. Gehen Sie im Abschnitt **[!UICONTROL Connect to [!DNL Google Analytics]]** wie folgt vor.

      1. Geben Sie die numerische ID für das [!DNL Google Analytics] ein.

      1. Geben Sie die E-Mail-Adresse ein, die für den Zugriff auf Daten aus dieser Datenquelle verwendet werden soll. Die E-Mail-Adresse muss bei einem [!DNL Google]-Konto registriert sein und über die Berechtigung zum Lesen und Analysieren für das [!DNL Google Analytics]-Konto verfügen. Siehe [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Um sicherzustellen, dass in Adobe Advertising nur bestimmte [!DNL Google Analytics] und Ansichten verfügbar sind, melden Sie sich mit einer E-Mail-Adresse an, die nur Zugriff auf diese Eigenschaften und Ansichten hat.

         >[!NOTE]
         >
         >Wenn Sie später das Passwort für dieses E-Mail-Konto ändern, werden alle offenen Verbindungen zum E-Mail-Konto geschlossen. Um mit der Synchronisierung von Daten fortzufahren, kehren Sie zu dieser Seite zurück und [erneut authentifizieren](data-source-reauthenticate.md).

      1. Aktivieren Sie das Kontrollkästchen, um Adobe Advertising zu autorisieren, auf Metriken für das Konto zuzugreifen.

      1. Klicken Sie auf **[!UICONTROL Authenticate]**.

   1. Geben Sie im Abschnitt [!UICONTROL Account Details] die Eigenschaft und die Ansicht für die zu importierenden Metriken an. Geben Sie außerdem die benutzerdefinierte Dimension an, die mit dem Wert des Abfragezeichenfolgenparameters „ef_id“ aufgefüllt wird.

   1. Geben Sie im Abschnitt [!UICONTROL Import Metrics] die Metriken an, die in die Feeds aufgenommen werden sollen.

      Sie können keine [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] oder [!UICONTROL Session Duration] entfernen, die automatisch eingeschlossen werden. Sie können bis zu 16 zusätzliche gültige Metriken oder Metriken ohne Daten hinzufügen.

      >[!WARNING]
      >
      >[!DNL Google Analytics] ermöglicht bis zu 10 Metriken in einem einzigen Daten-Feed. Search, Social und Commerce können bis zu zwei Feeds mit insgesamt 20 Metriken unterstützen, aber die Verwendung eines zweiten Feeds verdoppelt Ihre API-Aufrufe an [!DNL Google Analytics]. Wenn Sie viele Metriken haben, wählen Sie nur die Metriken aus, die Sie in Zielen zur Optimierung verwenden möchten. Weitere Informationen finden Sie [Kontingente und Aufrufbeschränkungen für API-Anfragen an [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Geben Sie im Abschnitt [!UICONTROL Metric Tag] den Namen des Tags ein, das für die Datenquelle an jede Metrik angehängt werden soll.

1. Klicken Sie oben rechts auf **[!UICONTROL Post]**.

   Die Datenquelle heißt „AccountName > PropertyName > ViewName“ und wird automatisch aktiviert. Informationen zum Anhalten der Datenquelle finden Sie unter &quot;[ eines Feeds aus einer Data Source](data-source-pause.md).

   Die Metriken sind am nächsten Tag nach Abschluss der täglichen Datensynchronisation verfügbar, die um 05:00 Uhr in der Zeitzone des Advertisers beginnt. Sobald die Metriken verfügbar sind, sind sie unter [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) sichtbar. Jede neue Konversionsmetrik trägt den Namen &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, wobei „backEndMetricName“ der von der API verwendete Metrikname ist. Der Anzeigename für jede neue Konversionsmetrik lautet &quot;`friendlyMetricName_ga:MetricTag`&quot;, wobei „friendlyMetricName“ der Metrikname ist, der in [!DNL Google Analytics] angezeigt wird, und „MetricTag“ der in den Datenquelleneinstellungen definierte [!UICONTROL Metric Tag] ist.

   Sie können die Metriken direkt zu Kampagnen- und Portfolioverwaltungsansichten, Berichten und Optimierungszielen hinzufügen.

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare  [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
