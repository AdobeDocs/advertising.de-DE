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
source-git-commit: c62a18194544bcbe98117b86eccb1b5e2740999c
workflow-type: tm+mt
source-wordcount: 1804
ht-degree: 0%

---

# Einrichten von Datenerfassung, Datenübertragung und Reporting

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

*Nur Werbetreibende ohne [!DNL Analytics for Advertising]*

Die folgenden Aufgaben sind erforderlich, um Daten über die [Adobe Experience Platform nativ zwischen Adobe Advertising und Customer Journey Analytics  [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). Die Datenübertragung und -zuordnung beginnt nach dem Launch. Es sind keine historischen Daten enthalten.

1. (Web-Analyst Ihres Unternehmens; optional) ([&#x200B; historische Daten für AMO-IDs und EF-IDs &#x200B;](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Dieser Schritt gilt nur für Werbetreibende mit [!DNL Analytics for Advertising].

2. (Site-Admin Ihres Unternehmens für Adobe Experience Platform) [Richten Sie die Datenerfassung in Experience Platform ein und implementieren Sie Konversionsverfolgungstags](#data-collection).

3. (Website-Administrator Ihres Unternehmens für Customer Journey Analytics) [Erstellen Sie eine Verbindung zu Ihren Experience Platform-Datensätzen in Customer Journey Analytics](#dataset-connection).

4. (Web-Analyst Ihres Unternehmens) [Einrichten von Datenansichten in Customer Journey Analytics](#cja-data-views).

5. (Web-Analyst Ihres Unternehmens) [Einrichten von Berichten und Visualisierungen in Customer Journey Analytics Workspace](#cja-reports).

Die folgenden Abschnitte enthalten die detaillierten Verfahren, die die für die Integration erforderlichen Aufgaben und Einstellungen enthalten, aber nicht alle in den Workflows verfügbaren Funktionen erläutern. Vollständige Informationen finden Sie in den verknüpften Ressourcen .

## Einrichten der Datenerfassung in Adobe Experience Platform und auf Ihrer Website {#data-collection}

Die folgenden Aufgaben sind erforderlich, um die Datenerfassung in Experience Platform einzurichten und Konversionsverfolgungstags zu implementieren. Der Site-Administrator Ihres Unternehmens für Experience Platform kann diese Aufgaben ausführen, aber die IT-Abteilung Ihres Unternehmens muss möglicherweise bei der Bereitstellung von Tracking-Tags helfen.

### Erfassen und Senden von Daten aus Adobe Advertising an Experience Platform Edge Network als Datensatz

Dieses Verfahren umfasst das Erstellen eines Schemas. Sie können stattdessen optional ein vorhandenes Schema bearbeiten. In diesem Fall müssen Sie keinen Datensatz oder Datenstrom erstellen.

1. Definieren Sie [&#x200B; Experience Platform ein &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) für die Daten, die Sie mit dem Experience-Datenmodell (XDM) erfassen möchten.

   * Wählen Sie in der [!UICONTROL Schema Details] **[!UICONTROL Experience Event]** als Basisklasse für das Schema zur Erfassung von Site-Ereignissen aus. Benennen Sie Ihr Schema und klicken Sie auf **[!UICONTROL Finish]**.

   * Fügen Sie im linken Bereich die Feldergruppe [Adobe Advertising Cloud ExperienceEvent Full Extension) hinzu](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) um Adobe Advertising-spezifische Felder hinzuzufügen. Schließen Sie mindestens das Objekt „conversionDetails“ mit den Eigenschaften &quot;`trackingCode`&quot; und &quot;`trackingIdentities`&quot; ein, zu denen die [AMO ID und EF ID“ &#x200B;](ids.md). Die anderen Felder sind optional.

   * (Optional) Fügen Sie bei Bedarf zusätzliche Feldergruppen hinzu, um zusätzliche Datenfelder mit Adobe Advertising-Daten zu verbinden.

   **Hinweis:** Sie können mehrere Schemata erstellen, aber Sie können nur ein Schema pro Datensatz und Datenstrom verwenden, was Sie in den folgenden Schritten erstellen werden.

1. [Erstellen eines Datensatzes](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basierend auf dem Schema zum Speichern und Verwalten der Erfassung von Ereignisdaten. Dies ist Ihr *Ereignisdatensatz*. Wenn Sie ein vorhandenes Schema mit einem Datensatz bearbeiten, können Sie diesen Schritt überspringen.

   * Wählen Sie die zu **[!UICONTROL Create dataset from schema]** Option aus und wählen Sie Ihr Schema aus.

     Basierend auf Ihrem Ereignisdatensatz erstellt Adobe Advertising zwei zusätzliche Datensätze: 1\) einen *Zusammenfassungsdatensatz* mit den zugehörigen Zusammenfassungsdaten (z. B. Klicks und Impressionen) und 2\) einen *Lookup-Datensatz* (mit Dimensionen/Klassifizierungsmetadaten, z. B. Adobe Advertising-Kampagnenname). Daten für die Datensätze werden täglich in Experience Platform ausgefüllt.

   >[!TIP]
   >
   >Erstellen Sie zuerst einen Platzhalter-Ereignisdatensatz, um den Datenfluss zu validieren, bevor Sie einen Produktionsdatensatz verwenden.

1. [Erstellen eines Datenstroms](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) um anzugeben, wohin Daten von Ihrer Website oder Ihrer App gesendet werden sollen und wie die eingehenden Daten verarbeitet werden sollen.

   * Wählen Sie als [!UICONTROL Mapping schema] Ihr Schema aus.

   * Fügen Sie die Services hinzu und aktivieren Sie sie `Adobe Advertising` und `Adobe Experience Platform` Sie sie zum Datenstrom.

     Der [!UICONTROL Adobe Advertising]-Service ermöglicht die Zuordnung von Werbegefährdungen zur Payload und die [!UICONTROL Adobe Experience Platform] ermöglicht es der Edge Network, den Datensatz zu speichern und an Adobe Advertising weiterzuleiten.

   * Wählen Sie als [!UICONTROL Event dataset] Ihren Ereignis-Datensatz aus.

     Jeder Datenstrom kann Daten in nur einen Datensatz einfügen.

### Senden der Website-Daten Ihres Unternehmens an Ihren Experience Platform-Datenstrom

Verwenden Sie die Adobe Experience Platform Web SDK-Erweiterung in Adobe Tags , um die Website-Daten Ihres Unternehmens an Ihren Experience Platform-Datenstrom zu senden.

>[!NOTE]
>
>Es werden nur Adobe-Tags unterstützt. Für eigenständige Experience Platform Web SDK (`alloy.js`) oder Tag-Manager von Drittanbietern wird kein Support bereitgestellt.

1. Verwenden Sie Experience Platform [Tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (früher als [!DNL Launch] bezeichnet), um ein JavaScript-Tag zu generieren, um die Website-Daten Ihres Unternehmens an den Datenstrom zu senden.

   * Erstellen Sie eine Tag-Eigenschaft als Container für die Tag-Konfiguration.

   * Installieren Sie für Ihre Eigenschaft [die Erweiterung &quot;Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) aus dem Erweiterungskatalog.

     Diese Erweiterung sendet Daten aus Ihren Web-Eigenschaften über die Experience Platform Edge Network an Adobe CX Enterprise.

     Verwenden Sie nicht die Adobe Advertising-Erweiterung.

   * Erstellen Sie einen [benutzerdefinierten Web-SDK-Build](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * Aktivieren Sie im Abschnitt [!UICONTROL Custom build components] die Komponente **Advertising**.

        Diese Komponente enthält den gesamten JavaScript-Code, der für Adobe Advertising im -Tag benötigt wird, und ist sowohl für Kunden von Advertising DSP als auch Advertising Search, Social und Commerce erforderlich. Die Komponente fügt außerdem eine Einstellung &quot;Advertising&quot; in Tag-Regeln hinzu (die optional sind), um zu definieren, wie Werbedaten für die Attributionsmessung verwendet werden.

        Sie können bei Bedarf optional zusätzliche Komponenten aktivieren.

      * Im [!UICONTROL SDK Instances] Abschnitt:

         * Wählen Sie in den [!UICONTROL Datastreams] Einstellungen den Datenstrom aus, der für jede Ihrer Web-Umgebungen (Produktion, Staging, Entwicklung) verwendet werden soll.

         * (Nur Organisationen mit Adobe Advertising DSP) Aktivieren Sie in den [[!UICONTROL Adobe Advertising] Einstellungen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) die Option **[!UICONTROL Adobe Advertising DSP]** , um das View-Through-Tracking zuzulassen, und geben Sie die Werbetreibenden an, für die das View-Through-Tracking aktiviert werden soll. Sie können optional IDs aus universellen IDs erfassen, indem Sie die ID5-Partner-ID Ihres Unternehmens und/oder den Pfad zum [!DNL LiveRamp RampID] JavaScript-Code Ihres Unternehmens (ats.js) hinzufügen.

           Wenn Ihre Advertiser nicht aufgeführt sind, geben Sie die Advertiser-ID für jeden Advertiser ein. Fragen Sie bei Bedarf Ihr Adobe Account Team nach den IDs.

         * Speichern Sie den Build.

   * (Optional) [Erstellen Sie nach &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) Regeln, um zu bestimmen, wann Web SDK Daten an Edge Network senden soll.

      * Verwenden Sie für `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` Aktionen die Einstellung [[!UICONTROL Advertising] &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising), um festzulegen, wie Werbedaten für die Attributionsmessung verwendet werden. Diese Einstellung ist hilfreich, wenn die Regel eine Sequenz mehrerer Aktionen enthält und nur verfügbar ist, wenn Sie die Komponente &quot;[!UICONTROL Advertising]&quot; für die benutzerdefinierte Build-Komponente ausgewählt haben.

   * Erstellen Sie [Datenelemente](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) nach Bedarf, um Variablen auf Ihrer Website der Struktur des zuvor erstellten XDM-Schemas zuzuordnen.

1. [Veröffentlichen Sie das &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) in einer Testumgebung, in der Sie die Entwicklung von Tags iterieren können.

1. [Überprüfen Sie die Aktivität für jeden Ihrer drei Datensätze](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets) um den Versand zu validieren.

1. [Veröffentlichen Sie das Tag in Ihrer Live-Produktionsumgebung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Möglicherweise muss die IT-Abteilung Ihres Unternehmens oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

## Erstellen einer Verbindung zu Ihren Experience Platform-Datensätzen in Customer Journey Analytics {#dataset-connection}

Führen Sie diese Schritte aus, um Adobe Advertising-Daten aus Ihren Experience Platform-Datensätzen in Customer Journey Analytics abzurufen. Der Site-Administrator Ihres Unternehmens für Customer Journey Analytics kann diese Aufgaben ausführen.

Sie können optional auch eine vorhandene Verbindung mit denselben Informationen bearbeiten.

1. Erstellen oder [&#x200B; Sie in Customer Journey Analytics eine Verbindung, &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) Ihre Experience Platform-Datensätze und -Schemata enthält.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Bestätigen Sie, dass die richtige Sandbox ausgewählt ist.

   * Berechnen Sie die durchschnittliche Anzahl der täglichen Ereignisse (unter 1 Million für die meisten Organisationen).

   * Fügen Sie Ihren Experience Platform-Ereignismetriken-Datensatz (Typ: `Event`), Ihren <!-- Adobe Advertising -->-Ereigniszusammenfassungsmetriken-Datensatz (Typ: `Event`) und Ihren <!-- Adobe Advertising -->-Dimensions-Datensatz (Klassifizierungen/Metadaten) (Typ: `Lookup`) hinzu.

     Ihr Team hat den Ereignisdatensatz erstellt, und Adobe Advertising hat die Zusammenfassungs- und Dimensionsdatensätze basierend auf Ihrem Ereignisdatensatz erstellt.

     Sie können bei Bedarf optional zusätzliche Datensätze einbeziehen.

   * Konfigurieren Sie die Datensatzeinstellungen:

      * Für die [!UICONTROL Event Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * Einstellung **[!UICONTROL Use primary identity namespace]:** aktivieren

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:** Aktivieren der Einstellung

      * Ordnen Sie für die [!UICONTROL Lookup Dataset] den Dimensions-Datensatz dem Ereignis-Datensatz zu:

         * **[!UICONTROL Key]** (das Feld, das als Schlüssel für den Dimensions-Datensatz verwendet werden soll): `Tracking Code` (das mit dem `trackingCode` Feld im Schema identisch ist).

         * **[!UICONTROL Matching key]** (das als übereinstimmender Schlüssel für den Ereignis-Datensatz zu verwendende Feld): `Tracking Code (Event datasets)`.<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->

         * **[!UICONTROL Import all new data]:** Aktivieren der Einstellung

      * Für die [!UICONTROL Metrics Dataset]:

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:** Wert bestätigen

         * **[!UICONTROL Import all new data]:** Aktivieren der Einstellung

1. Stellen Sie innerhalb von drei Stunden sicher, dass die Daten in Customer Journey Analytics verfügbar sind.

   1. Navigieren Sie in Customer Journey Analytics zu **[!UICONTROL Connections]** und wählen Sie Ihre Verbindung aus.

   2. Überprüfen Sie in der Liste der angezeigten Datensätze, ob der Bericht &quot;[!UICONTROL Number of Records]&quot; anzeigt, dass Daten hinzugefügt wurden.

## Einrichten von Datenansichten in Customer Journey Analytics {#cja-data-views}

Erstellen Sie in Customer Journey Analytics eine oder mehrere Datenansichten, um die Metriken und Dimensionen für das Reporting zu definieren. Ein Web-Analyst kann diese Aufgaben ausführen.

1. Erstellen Sie [&#x200B; Customer Journey Analytics eine &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Konfigurieren Sie die Ansicht so, dass sie die folgenden Informationen enthält.

   * Wenn Sie über ein Adobe Analytics-Konto verfügen, verwenden Sie die [!UICONTROL Time Zone] für Ihr [!DNL Analytics]-Konto im Abschnitt [!UICONTROL Calendar] der Registerkarte [!UICONTROL Configure] .

   * Auf der Registerkarte [!UICONTROL Components] :

      * Fügen Sie Ihren Lookup-Datensatz (mit Dimensionen/Klassifizierungsdaten), Ihren Ereignis-Datensatz (mit Ihren Daten auf Ereignisebene) und Ihren Zusammenfassungs-Datensatz (mit Ihren anderen Metriken, z. B. Klicks) hinzu.

      * Wählen Sie Metriken aus Ihrem Ereignis-Datensatz und Ihrem Lookup-Datensatz aus, die in die Datenansicht aufgenommen werden sollen.

      * Suchen Sie nach &quot;[!UICONTROL Tracking Code]&quot; (was Teil des Ereignis-Datensatzes mit dem Schemapfad `_experience.adcloud.conversionDetails.trackingCode` ist). <!-- and do what with it? Add it? Or is that what you --> Legen Sie **[!UICONTROL Persistence]** auf *[!UICONTROL Most Recent]* fest.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Einrichten von Berichten und Visualisierungen in Customer Journey Analytics Workspace {#cja-reports}

Gehen Sie in Customer Journey Analytics Workspace wie folgt vor, um Berichte und Visualisierungen zu konfigurieren. Ein Web-Analyst kann diese Aufgaben ausführen.

1. [Erstellen eines Projekts](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace, um Berichte und Visualisierungen basierend auf den Dimensionen und Metriken zu erstellen, die in der Datenansicht konfiguriert wurden.

Sie können sowohl Zusammenfassungsmetriken als auch Ereignisdaten mithilfe derselben Dimension in einer Freiformtabelle klassifizieren.

1. (Wenn Sie Daten aus [!DNL Google Ads] oder [!DNL Microsoft Advertising] haben) Erstellen Sie einen Bericht mit vom Publisher verfolgten Konversionen mithilfe von Feldern für Anzeigennetzwerkspezifische Metriken, die als `googleConversions` und `microsoftConversions` gruppiert sind.

>[!TIP]
>
>Zusammenfassungsereignisse fügen in der Regel eine kleine Menge zusätzlicher Daten zu Berichten hinzu, z. B. einige zusätzliche Ereignisse, eine zusätzliche Sitzung pro Tag oder eine zusätzliche Person pro Bericht. Diese Ergänzungen sind im Vergleich zu standardmäßigen Web-Ereignissen vernachlässigbar. Sie können diese zusätzlichen zusammenfassenden Ereignisdaten jedoch herausfiltern, indem Sie Daten für die Platzhalter-Personen-ID `00000000-0000-0000-0000-000000000000` ausschließen.
>![Beispiel für den Ausschluss von Daten mit einer Personen-ID](/help/integrations/assets/cja-report-with-person-id.png "Beispiel für den Ausschluss von Daten mit einer Personen-ID")

![Wie Ihre Datensätze in Customer Journey Analytics angezeigt werden können](/help/integrations/assets/cja-report-example.png "Wie Ihre Datensätze in Customer Journey Analytics angezeigt werden können")

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* [Voraussetzungen](prerequisites.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Handbuch zu Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Benutzerhandbuch für Adobe Analytics-Benutzer](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
