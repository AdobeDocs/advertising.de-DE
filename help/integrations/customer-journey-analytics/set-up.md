---
title: Einrichten von Datenerfassung, Datenübertragung und Reporting
description: Erfahren Sie, wie Sie die Datenerfassung, Datenübertragung und Berichterstellung einrichten.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1792
ht-degree: 0%

---

# Einrichten von Datenerfassung, Datenübertragung und Reporting

*Beta-Funktion*

Die folgenden Aufgaben sind erforderlich, um Advertising Cloud-Daten in Customer Journey Analytics anzuzeigen.

1. (Web-Analyst Ihres Unternehmens; optional) ([&#x200B; historische Daten für AMO-IDs und EF-IDs &#x200B;](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Dieser Schritt gilt nur für Werbetreibende mit [!DNL Analytics for Advertising].

1. (Site-Admin Ihres Unternehmens für Adobe Experience Platform) [Richten Sie die Datenerfassung in Experience Platform ein und implementieren Sie Konversionsverfolgungstags](#data-collection).

1. (Website-Administrator Ihres Unternehmens für Customer Journey Analytics) [Erstellen Sie eine Verbindung zu Ihren Experience Platform-Datensätzen in Customer Journey Analytics](#dataset-connection).

1. (Web-Analyst Ihres Unternehmens) [Einrichten von Datenansichten in Customer Journey Analytics](#cja-data-views).

1. (Web-Analyst Ihres Unternehmens) [Einrichten von Berichten und Visualisierungen in Customer Journey Analytics Workspace](#cja-reports).

Die folgenden Abschnitte enthalten die detaillierten Verfahren, die die für die Integration erforderlichen Aufgaben und Einstellungen enthalten, aber nicht alle in den Workflows verfügbaren Funktionen erläutern. Vollständige Informationen finden Sie in den verknüpften Ressourcen .

## Einrichten der Datenerfassung in Adobe Experience Platform und auf Ihrer Website {#data-collection}

Die folgenden Aufgaben sind erforderlich, um die Datenerfassung in Experience Platform einzurichten und Konversionsverfolgungstags zu implementieren. Der Site-Administrator Ihres Unternehmens für Experience Platform kann diese Aufgaben ausführen, aber die IT-Abteilung Ihres Unternehmens muss möglicherweise bei der Bereitstellung von Tracking-Tags helfen.

### Erfassen und Senden von Daten aus Adobe Advertising an Experience Platform Edge Network als Datensatz

1. Definieren Sie [&#x200B; Experience Platform ein &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) für die Daten, die Sie mit dem Experience-Datenmodell (XDM) erfassen möchten.

   * Wählen Sie in der [!UICONTROL Schema Details] **[!UICONTROL Experience Event]** als Basisklasse für das Schema zur Erfassung von Site-Ereignissen aus. Benennen Sie Ihr Schema und klicken Sie auf **[!UICONTROL Finish]**.

   * Fügen Sie im linken Bereich die Feldergruppe [Adobe Advertising Cloud ExperienceEvent Full Extension) hinzu](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) um Adobe Advertising-spezifische Felder hinzuzufügen. Schließen Sie mindestens das Objekt „conversionDetails“ mit den Eigenschaften &quot;`trackingCode`&quot; und &quot;`trackingIdentities`&quot; ein, zu denen die [AMO ID und EF ID“ &#x200B;](ids.md). Die anderen Felder sind optional.

   * (Optional) Fügen Sie bei Bedarf zusätzliche Feldergruppen hinzu, um zusätzliche Datenfelder mit Adobe Advertising-Daten zu verbinden.

   **Hinweis:** Sie können mehrere Schemata erstellen, aber Sie können nur ein Schema pro Datensatz und Datenstrom verwenden, was Sie in den folgenden Schritten erstellen werden.

1. [Erstellen eines Datensatzes](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basierend auf dem Schema zum Speichern und Verwalten der Erfassung von Ereignisdaten.

   * Wählen Sie die zu **[!UICONTROL Create dataset from schema]** Option aus und wählen Sie Ihr Schema aus.

     Adobe Advertising erstellt zusätzliche Datensätze für die zugehörigen Zusammenfassungsmetrikdaten (z. B. Konversionswerte) und Suchdaten (Dimensionen/Klassifizierungsmetadaten, z. B. den Adobe Advertising-Kampagnennamen) basierend auf Ihrem Ereignisdatensatz. Daten für die Datensätze werden täglich in Experience Platform ausgefüllt.

1. [Erstellen eines Datenstroms](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) für das Schema

   * Wählen Sie als [!UICONTROL Mapping schema] Ihr Schema aus.

   * Fügen Sie die Services hinzu und aktivieren Sie sie `Adobe Advertising` und `Adobe Experience Platform` Sie sie zum Datenstrom.

     Diese Services ermöglichen es Edge Network, den Datensatz zu speichern und an Adobe Advertising weiterzuleiten.

   * Wählen Sie als [!UICONTROL Event dataset] Ihren Datensatz aus.

     Jeder Datenstrom kann Daten in nur einen Datensatz einfügen.

### Senden der Website-Daten Ihres Unternehmens an Ihren Experience Platform-Datenstrom

1. Verwenden Sie Experience Platform [Tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (früher als [!DNL Launch] bezeichnet), um ein JavaScript-Tag zu generieren, um die Website-Daten Ihres Unternehmens an den Datenstrom zu senden.

   * Erstellen Sie eine Tag-Eigenschaft als Container für die Tag-Konfiguration.

   * Installieren Sie für Ihre Eigenschaft [die Erweiterung &quot;Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) aus dem Erweiterungskatalog.

     Diese Erweiterung sendet Daten aus Ihren Web-Eigenschaften über die Experience Platform Edge Network an Adobe CX Enterprise.

     Verwenden Sie nicht die Adobe Advertising-Erweiterung.

   * Erstellen Sie einen [benutzerdefinierten Web-SDK-Build](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * Aktivieren Sie im Abschnitt [!UICONTROL Custom build components] die Komponente **Advertising**.

        Diese Komponente enthält den gesamten JavaScript-Code, der für Adobe Advertising im -Tag benötigt wird. Außerdem wird eine &quot;Advertising&quot;-Einstellung in Tag-Regeln hinzugefügt (die optional sind), um zu definieren, wie Werbedaten für die Attributionsmessung verwendet werden.

        Sie können bei Bedarf optional zusätzliche Komponenten aktivieren.

      * Im [!UICONTROL SDK Instances] Abschnitt:

         * Wählen Sie in den [!UICONTROL Datastreams] Einstellungen den Datenstrom aus, der für jede Ihrer Web-Umgebungen (Produktion, Staging, Entwicklung) verwendet werden soll.

         * (Nur Organisationen mit Adobe Advertising DSP) Aktivieren Sie in den [[!UICONTROL Adobe Advertising] Einstellungen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) die Option **[!UICONTROL Adobe Advertising DSP]** , um das View-Through-Tracking zuzulassen, und geben Sie die Werbetreibenden an, für die das View-Through-Tracking aktiviert werden soll. Optional können Sie IDs aus universellen IDs erfassen.

           Wenn Ihre Advertiser nicht aufgeführt sind, geben Sie die Advertiser-ID für jeden Advertiser ein.

         * Speichern Sie den Build.

   * (Optional) [Erstellen Sie nach &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) Regeln, um zu bestimmen, wann Web SDK Daten an Edge Network senden soll.

      * Verwenden Sie für `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` Aktionen die Einstellung [[!UICONTROL Advertising] &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising), um festzulegen, wie Werbedaten für die Attributionsmessung verwendet werden. Diese Einstellung ist hilfreich, wenn die Regel eine Sequenz mehrerer Aktionen enthält und nur verfügbar ist, wenn Sie die Komponente &quot;[!UICONTROL Advertising]&quot; für die benutzerdefinierte Build-Komponente ausgewählt haben.

   * Erstellen Sie [Datenelemente](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) nach Bedarf, um Variablen auf Ihrer Website der Struktur des zuvor erstellten XDM-Schemas zuzuordnen.

1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.

1. Validate delivery of the datasets, and then [publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Your organization&#39;s IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization&#39;s site administrator for Customer Journey Analytics can perform these tasks.

1. In Customer Journey Analytics, [create a connection](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) that includes your Experience Platform datasets and schema.

   **Note:** Currently, you must send data for all DSP and Search, Social, &amp; Commerce accounts to a single Experience Platform instance and sandbox.

   * Add your Experience Platform event (metrics) dataset, summary (metrics) dataset, and dimensions (classifications/metadata) dataset.

     Your team created the event dataset, and Adobe Advertising created the summary and dimensions datasets based on your event dataset.

     You can optionally include additional datasets as needed.

   * Map the dimensions dataset to the events dataset:

      1. Open the settings for the dimension dataset.

         The heading on the settings page is &quot;[!UICONTROL Lookup Dataset],&quot; which indicates that you can join your dimensions dataset with one of your metric-specific datasets.

      1. In the [!UICONTROL Adobe Advertising Dimensions] section, map the dimensions dataset to the events dataset:

         1. For the [!UICONTROL Key] field, select the field to use as the key for the dimensions dataset: `Adobe Advertising ID` (which is same as the `trackingCode` field in the schema).

         1. For the [!UICONTROL Matching key] field, select the field to use as the matching key for the events dataset. The available field names include the dataset name in parentheses. For example, if you&#39;re mapping your dimensions dataset to your events dataset, select `Tracking Code (Event datasets)`.

         Later, you&#39;ll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).

1. After a couple of hours, verify that the data is available in Customer Journey Analytics.

   1. In Customer Journey Analytics, go to **[!UICONTROL Connections]** and select your connection.

   1. In the list of data sets displayed, verify that the &quot;[!UICONTROL Number of Records]&quot; report shows that data was added.

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. A web analyst can perform these tasks.

1. In Customer Journey Analytics, [create a data view](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure the view to include the following information.

   * If you have an Adobe Analytics account, use the [!UICONTROL Time Zone] for your [!DNL Analytics] account in the [!UICONTROL Calendar] section of the [!UICONTROL Configure] tab.

   * On the [!UICONTROL Components] tab:

      * Add your dimensions, events, and summary datasets.

      * Choose metrics from your events (metrics) dataset and your dimensions (classifications/metadata) dataset to include in the data view.

        You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).

      * Join the events dataset to the summary dataset, which isn&#39;t yet joined to anything:

         * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

           For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.

           You&#39;ll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).

            * In the [!UICONTROL Lookup] section of the derived rule builder:

               * For the **[!UICONTROL Value]** field, select &quot;[!UICONTROL Tracking Code]&quot; from the metrics summary dataset.

               * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as &quot;Adobe Advertising Classification&quot;).

               * For the **[!UICONTROL Matching Key]** field, select &quot;[!UICONTROL Tracking Code]&quot; from the classification dataset.

               * For the **[!UICONTROL Values to return]** field, select the dimension (such as &quot;[!UICONTROL Adobe Advertising Campaign]&quot;)&quot; from the classification dataset.

           The derived field name is appended with &quot;(DF)&quot;, such as `Adobe Advertising Campaign(DF)`.

         * For each derived field:

            * In the [!UICONTROL Included components] section, add the derived field.

              Two names are now listed for the same dimension (for example, &quot;Adobe Advertising Campaign(DF)&quot; (the derived field) and &quot;Adobe Advertising Campaign&quot; (the field in the summary dataset)).

            * Select the dimension in the summary dataset (such as &quot;Adobe Advertising Campaign&quot;) and edit the settings for the dataset.

              The settings open on the right.

               * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

               * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with &quot;(DF),&quot; such as &quot;Adobe Advertising Campaign(DF)&quot;).

               * Wählen Sie die zu **[!UICONTROL Hide in reporting]** Option aus, wodurch der abgeleitete Feldname in Workspace ausgeblendet wird.

## Einrichten von Berichten und Visualisierungen in Customer Journey Analytics Workspace {#cja-reports}

Gehen Sie in Customer Journey Analytics Workspace wie folgt vor, um Berichte und Visualisierungen zu konfigurieren. Ein Web-Analyst kann diese Aufgaben ausführen.

1. [Erstellen eines Projekts](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace, um Berichte und Visualisierungen basierend auf den Dimensionen und Metriken zu erstellen, die in der Datenansicht konfiguriert wurden.

1. (Wenn Sie Daten aus [!DNL Google Ads] oder [!DNL Microsoft Advertising] haben) Erstellen Sie einen Bericht mit vom Publisher verfolgten Konversionen mithilfe von Feldern für Anzeigennetzwerkspezifische Metriken, die als `googleConversions` und `microsoftConversions` gruppiert sind.

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* [Voraussetzungen](prerequisites.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Handbuch zu Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Benutzerhandbuch für Adobe Analytics-Benutzer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
