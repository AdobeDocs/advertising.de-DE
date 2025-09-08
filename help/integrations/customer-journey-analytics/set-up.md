---
title: Einrichten von Datenerfassung, Datenübertragung und Reporting
description: Erfahren Sie, wie Sie die Datenerfassung, Datenübertragung und Berichterstellung einrichten.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 0b6a939a706d0e9155f9cc6335a947cc31192ac7
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# Einrichten von Datenerfassung, Datenübertragung und Reporting

*Beta-Funktion*

Die folgenden Aufgaben sind erforderlich, um Advertising Cloud-Daten in Customer Journey Analytics anzuzeigen.

1. (Web-Analyst Ihres Unternehmens; optional) ([ historische Daten für AMO-IDs und EF-IDs ](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Dieser Schritt gilt nur für Werbetreibende mit [!DNL Analytics for Advertising].

1. (Site-Admin Ihres Unternehmens für Adobe Experience Platform) [Richten Sie die Datenerfassung in Experience Platform ein und implementieren Sie Konversionsverfolgungstags](#data-collection).

1. (Website-Administrator Ihres Unternehmens für Customer Journey Analytics) [Erstellen Sie eine Verbindung zu Ihren Experience Platform-Datensätzen in Customer Journey Analytics](#dataset-connection).

1. (Web-Analyst Ihres Unternehmens) [Einrichten von Datenansichten in Customer Journey Analytics](#cja-data-views).

1. (Web-Analyst Ihres Unternehmens) [Einrichten von Berichten und Visualisierungen in Customer Journey Analytics Workspace](#cja-reports).

Die folgenden Abschnitte enthalten die detaillierten Verfahren, die die für die Integration erforderlichen Aufgaben und Einstellungen enthalten, aber nicht alle in den Workflows verfügbaren Funktionen erläutern. Vollständige Informationen finden Sie in den verknüpften Ressourcen .

## Einrichten der Datenerfassung in Adobe Experience Platform und auf Ihrer Website {#data-collection}

Die folgenden Aufgaben sind erforderlich, um die Datenerfassung in Experience Platform einzurichten und Konversionsverfolgungstags zu implementieren. Der Site-Administrator Ihres Unternehmens für Experience Platform kann diese Aufgaben ausführen, aber die IT-Abteilung Ihres Unternehmens muss möglicherweise bei der Bereitstellung von Tracking-Tags helfen.

### Erfassen und Senden von Daten aus Adobe Advertising an Experience Platform Edge Network als Datensatz

1. Definieren Sie [ Experience Platform ein ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) für die Daten, die Sie mit dem Experience-Datenmodell (XDM) erfassen möchten.

   * Wählen Sie in der [!UICONTROL Schema Details] **[!UICONTROL Experience Event]** als Basisklasse für das Schema zur Erfassung von Site-Ereignissen aus. Benennen Sie Ihr Schema und klicken Sie auf **[!UICONTROL Finish]**.

   * Fügen Sie im linken Bereich die Feldergruppen-`Adobe Advertising Cloud ExperienceEvent Full Extension` hinzu, um Adobe Advertising-spezifische Felder hinzuzufügen.<!-- Add link once published --> Schließen Sie mindestens das Objekt „conversionDetails“ mit den Eigenschaften &quot;`trackingCode`&quot; und &quot;`trackingIdentities`&quot; ein, zu denen die [AMO ID und EF ID“ ](ids.md). Die anderen Felder sind optional.

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

     Diese Erweiterung sendet Daten aus Ihren Web-Eigenschaften über die Experience Platform Edge Network an Experience Cloud.

     Verwenden Sie nicht die Adobe Advertising-Erweiterung.

   * Erstellen Sie einen benutzerdefinierten Web-SDK-Build:

      * Aktivieren Sie im Abschnitt [!UICONTROL Custom build components] die Komponente **Advertising**.

        Diese Komponente enthält den gesamten JavaScript-Code, der für Adobe Advertising im -Tag benötigt wird. Außerdem wird eine &quot;Advertising&quot;-Einstellung in Tag-Regeln hinzugefügt (die optional sind), um zu definieren, wie Werbedaten für die Attributionsmessung verwendet werden.

        Sie können bei Bedarf optional zusätzliche Komponenten aktivieren.

      * Im [!UICONTROL SDK Instances] Abschnitt:

         * Wählen Sie in den [!UICONTROL Datastreams] Einstellungen den Datenstrom aus, der für jede Ihrer Web-Umgebungen (Produktion, Staging, Entwicklung) verwendet werden soll.

         * (Nur Organisationen mit Adobe Advertising DSP) In den [!UICONTROL Adobe Advertising]:

            * Aktivieren Sie die **[!UICONTROL Adobe Advertising DSP]**, um das View-Through-Tracking zu aktivieren.

            * Geben Sie die Werbetreibenden an, für die das View-Through-Tracking aktiviert werden soll.

            * (Optional) Geben Sie die ID5-Partner-ID Ihres Unternehmens ein, um IDs zu erfassen.

            * (Optional) Geben Sie den Pfad zum [!DNL LiveRamp RampID] JavaScript-Code (ats.js) Ihres Unternehmens ein, um IDs zu erfassen.

         * Speichern Sie den Build.

   * (Optional) [Erstellen Sie nach ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) Regeln, um zu bestimmen, wann Web SDK Daten an Edge Network senden soll.

      * Definieren Sie für die [!UICONTROL Advertising], wie Werbedaten für die Attributionsmessung verwendet werden. Diese Einstellung ist hilfreich, wenn die Regel eine Sequenz mehrerer Aktionen enthält und nur verfügbar ist, wenn Sie die Komponente &quot;[!UICONTROL Advertising]&quot; für die benutzerdefinierte Build-Komponente ausgewählt haben. Zu den Optionen gehören:

        *Automatisch:* Ermöglicht die Verwendung von Werbedaten zur Messung der Anzeigenzuordnung in der aktuellen `sendEvent` auf der Grundlage von Daten im Cache. In diesem Fall wird das Anzeigenexpositionsereignis ausgelöst, wenn es die Chance erhält, und es ist möglicherweise nicht für das aktuelle Ereignis verfügbar. Wenn Sie beispielsweise ein Kaufcheckout-Ereignis auslösen und im Cache keine Daten zur Werbegefährdung verfügbar sind, wird das Checkout-Ereignis nicht der Werbegefährdung zugeordnet.

        *Warten:* Verzögert die Ausführung des Aufrufs, bis die Werbedaten erfolgreich vom Server abgerufen und aufgelöst wurden, was eine genaue Attributionsmessung gewährleistet. Beispielsweise können Sie warten, bis das Ereignis „Werbeaussetzung“ aufgelöst ist, bevor Sie ein Kaufkassenereignis auslösen. **Hinweis:** Das Auflösen von IDs kann je nach Browser und ID-Typ einige Sekunden dauern. Verwenden Sie diese Option, wenn die aktuelle `sendEvent` eine Verzögerung von einigen Sekunden aufweisen kann.

        *Deaktiviert:* (Standard) Schließt Werbedaten aus der ausgelösten Anfrage aus, sodass sie für die Attribution oder das zugehörige Tracking nicht verfügbar sind.

        *Datenelement bereitstellen:* Verwenden Sie ein Datenelement, um Werbedaten beim Laden der Seite ein- oder auszuschließen. Aufgelöste Werte für das Datenelement können `automatic`, `wait` und `disabled` sein. Siehe den nächsten Schritt.

     Wenn Sie keine Regel zum Konfigurieren einer `sendEvent` verwenden, werden die Werbedaten als separates Anreicherungsereignis für die Werbung gesendet.

   * Erstellen Sie [Datenelemente](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) nach Bedarf, um Variablen auf Ihrer Website der Struktur des zuvor erstellten XDM-Schemas zuzuordnen.

1. [Veröffentlichen Sie das ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) in einer Testumgebung, in der Sie die Entwicklung von Tags iterieren können.

1. Validieren Sie den Versand der Datensätze und [veröffentlichen Sie das Tag in Ihrer Live-Produktionsumgebung](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Möglicherweise muss die IT-Abteilung Ihres Unternehmens oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

## Erstellen einer Verbindung zu Ihren Experience Platform-Datensätzen in Customer Journey Analytics {#dataset-connection}

Führen Sie diese Schritte aus, um Adobe Advertising-Daten aus Ihren Experience Platform-Datensätzen in Customer Journey Analytics abzurufen. Der Site-Administrator Ihres Unternehmens für Customer Journey Analytics kann diese Aufgaben ausführen.

1. Erstellen Sie in Customer Journey Analytics [eine Verbindung](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) die Ihre Experience Platform-Datensätze und -Schemata enthält.

   **Hinweis** Derzeit müssen Sie Daten für alle DSP- und Search-, Social- und Commerce-Konten an eine einzige Experience Platform-Instanz und Sandbox senden.

   * Fügen Sie Ihren Experience Platform-Ereignis (Metriken)-Datensatz, Zusammenfassungsdatensatz (Metriken) und Dimensionen-Datensatz (Klassifizierungen/Metadaten) hinzu.

     Ihr Team hat den Ereignisdatensatz erstellt, und Adobe Advertising hat die Zusammenfassungs- und Dimensionsdatensätze basierend auf Ihrem Ereignisdatensatz erstellt.

     Sie können bei Bedarf optional zusätzliche Datensätze einbeziehen.

   * Ordnen Sie den Dimensions-Datensatz dem Ereignis-Datensatz zu:

      1. Öffnen Sie die Einstellungen für den Dimensionsdatensatz.

         Die Überschrift auf der Einstellungsseite lautet &quot;[!UICONTROL Lookup Dataset]&quot;. Dies bedeutet, dass Sie Ihren Dimensionsdatensatz mit einem Ihrer metrikspezifischen Datensätze verbinden können.

      1. Ordnen Sie im Abschnitt [!UICONTROL Adobe Advertising Dimensions] den Dimensions-Datensatz dem Ereignis-Datensatz zu:

         1. Wählen Sie für das [!UICONTROL Key] Feld das Feld aus, das als Schlüssel für den Dimensionsdatensatz verwendet werden soll: `Adobe Advertising ID` (dies entspricht dem `trackingCode` Feld im Schema).

         1. Wählen Sie für das Feld [!UICONTROL Matching key] das Feld aus, das als übereinstimmender Schlüssel für den Ereignis-Datensatz verwendet werden soll. Die verfügbaren Feldnamen enthalten den Datensatznamen in Klammern. Wenn Sie beispielsweise Ihren Dimensions-Datensatz Ihrem Ereignis-Datensatz zuordnen, wählen Sie `Tracking Code (Event datasets)` aus.

         Später ordnen Sie den Ereignis-Datensatz auch dem Zusammenfassungsdatensatz zu, wenn Sie Ihre Datenansicht(#cja-data-views) einrichten.

1. Überprüfen Sie nach einigen Stunden, ob die Daten in Customer Journey Analytics verfügbar sind.

   1. Navigieren Sie in Customer Journey Analytics zu **[!UICONTROL Connections]** und wählen Sie Ihre Verbindung aus.

   1. Überprüfen Sie in der Liste der angezeigten Datensätze, ob der Bericht &quot;[!UICONTROL Number of Records]&quot; anzeigt, dass Daten hinzugefügt wurden.

## Einrichten von Datenansichten in Customer Journey Analytics {#cja-data-views}

Erstellen Sie in Customer Journey Analytics eine oder mehrere Datenansichten, um die Metriken und Dimensionen für das Reporting zu definieren. Ein Web-Analyst kann diese Aufgaben ausführen.

1. Erstellen Sie [ Customer Journey Analytics eine ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Konfigurieren Sie die Ansicht so, dass sie die folgenden Informationen enthält.

   * Wenn Sie über ein Adobe Analytics-Konto verfügen, verwenden Sie die [!UICONTROL Time Zone] für Ihr [!DNL Analytics]-Konto im Abschnitt [!UICONTROL Calendar] der Registerkarte [!UICONTROL Configure] .

   * Auf der Registerkarte [!UICONTROL Components] :

      * Fügen Sie Ihre Dimensionen, Ereignisse und Zusammenfassungsdatensätze hinzu.

      * Wählen Sie Metriken aus Ihrem Ereignis-(Metrik-)Datensatz und Ihren Dimensionen-(Klassifizierungs-/Metadaten-)Datensatz aus, die in die Datenansicht aufgenommen werden sollen.

        Sie haben diese beiden Datensätze bereits in der Verbindung verbunden, die Sie im [ Verfahren erstellt ](#dataset-connection).

      * Verbinden Sie den Ereignis-Datensatz mit dem Zusammenfassungsdatensatz, der noch mit keinem Element verknüpft ist:

         * Erstellen Sie für jede Dimension mit Zusammenfassungsdaten, die in Customer Journey Analytics verfügbar sein soll[ ein abgeleitetes Feld](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

           Um beispielsweise Zusammenfassungsdaten für Kampagnen anzuzeigen, erstellen Sie ein abgeleitetes Feld für die `Adobe Advertising Campaign`.

           Sie verknüpfen die beiden Datensätze mithilfe der übereinstimmenden `trackingCode` (das Schemafeld für die Adobe Advertising-ID).

            * Im Abschnitt [!UICONTROL Lookup] des abgeleiteten Regel-Builders:

               * Wählen Sie für das Feld **[!UICONTROL Value]** die Option &quot;[!UICONTROL Tracking Code]&quot; aus dem Zusammenfassungsdatensatz der Metriken aus.

               * Wählen Sie für das Feld **[!UICONTROL Lookup dataset]** den Dimensions-Datensatz aus (z. B. &quot;Adobe Advertising-Klassifizierung„).

               * Wählen Sie für das **[!UICONTROL Matching Key]** Feld aus dem Klassifizierungsdatensatz &quot;[!UICONTROL Tracking Code]&quot; aus.

               * Wählen Sie für das Feld **[!UICONTROL Values to return]** die Dimension (z. B. &quot;[!UICONTROL Adobe Advertising Campaign]„) aus dem Klassifizierungsdatensatz aus.

           An den abgeleiteten Feldnamen wird „(DF)“ angehängt, z. B. `Adobe Advertising Campaign(DF)`.

         * Für jedes abgeleitete Feld:

            * Fügen Sie im Abschnitt [!UICONTROL Included components] das abgeleitete Feld hinzu.

              Zwei Namen werden jetzt für dieselbe Dimension aufgeführt (z. B. &quot;Adobe Advertising Campaign(DF)“ (das abgeleitete Feld) und &quot;Adobe Advertising Campaign“ (das Feld im Zusammenfassungsdatensatz)).

            * Wählen Sie die Dimension im Zusammenfassungsdatensatz aus (z. B. &quot;Adobe Advertising Campaign„) und bearbeiten Sie die Einstellungen für den Datensatz.

              Die Einstellungen werden auf der rechten Seite geöffnet.

               * Wählen Sie im Abschnitt Datengruppe Zusammenfassung die Option aus, die **[!UICONTROL Create grouping]** werden soll.

               * Wählen Sie für das **[!UICONTROL Dimension]** das abgeleitete Feld aus (an das „(DF)“ angehängt wird, z. B. &quot;Adobe Advertising Campaign(DF)„).

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
