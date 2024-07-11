---
title: Benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: ef732108b248995a6b321e991fa122caaa40e2fe
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 0%

---

# Benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das das Optimierungsziel verwendet &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; muss ein benutzerdefiniertes Ziel enthalten, um das Gesamtoptimierungsziel zu erreichen. Sie können benutzerdefinierte Ziele als *Ziele* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Jedes benutzerdefinierte Ziel (Ziel) besteht aus einer oder mehreren Konversionsmetriken und den relativen Gewichtungen dieser Metriken. Für DSP benutzerdefinierten Ziele werden nur Gewichtungen berücksichtigt, die nicht für Mobilgeräte gelten. Zu den verfügbaren Konversionsmetriken gehören alle Metriken, die mit dem Adobe Advertising-Konversionspol und über Adobe Analytics verfolgt werden.

Angenommen, drei Konversionsmetriken sind für ein bestimmtes Kampagnenkit relevant: &quot;PDF-Download&quot;im Wert von 20 USD, &quot;E-Mail-Anmeldung&quot;im Wert von 30 USD und &quot;Auftragsbestätigung&quot;im Wert von 40 USD. Wenn Sie Gewichtung gemäß dem einmaligen Geldwert der Kundenaktion geben möchten, beträgt das relative Gewicht der Metriken 1, 1,5 und 2.

Einmal [Erstellen eines benutzerdefinierten Ziels](#custom-goal-create), können Sie [Zuweisen zu einem Paket](/help/dsp/campaign-management/packages/package-settings.md) für die Berichterstellung und algorithmische Optimierung mit Adobe Sensei.

Gewichtungsempfehlungen werden automatisch für DSP zugeordneten Metriken in Zielen generiert und können alle Gewichtungsempfehlungen mit einem Klick anwenden. Alle Gewichtsänderungen an Zielen mit dem Präfix &quot;ADSP_&quot;werden in DSP innerhalb von zwei Tagen algorithmisch angewendet. Weitere Informationen zu Gewichtungsempfehlungen finden Sie im Kapitel &quot;Optimierungshandbuch&quot;zu &quot;Neue Ziele (Beta)&quot;, das in Search, Social und Commerce verfügbar ist.

## Benutzerdefiniertes Ziel erstellen {#custom-goal-create}

Um ein benutzerdefiniertes Ziel zu erstellen, muss das DSP Konto mit einem [!DNL Search, Social, & Commerce] -Konto mit derselben Adobe Experience Cloud-Organisations-ID aus der [!DNL Search, Social, & Commerce] Clienteinstellungen. Wenn Ihr DSP-Konto nicht mit einem [!DNL Search, Social, & Commerce] und dann Ihr Adobe-Account-Team kontaktieren.

1. Anmelden bei [!DNL Advertising Search, Social, & Commerce] unter (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) oder (alle anderen Benutzer) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Suchen Sie die Metrik und stellen Sie sicher, dass **[!UICONTROL Show in UI and Reports]** für die Metrik aktiviert ist.

      >[!NOTE]
      >
      >* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Benennungskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`

   1. Wenn die Metrik keinen Wert im **[!UICONTROL Display Name]** und klicken Sie dann in die Zelle, geben Sie den Anzeigenamen ein und klicken Sie auf **[!UICONTROL Apply].**

1. Erstellen Sie das benutzerdefinierte Ziel als *Ziel*:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Klicken Sie in der Symbolleiste auf ![Erstellen](/help/dsp/assets/create-search-ui.png "Erstellen").

   1. Geben Sie die Zieleinstellungen, einschließlich der zugehörigen Metriken, und ihre relative numerische Gewichtung für Nicht-Mobilgeräte ein und speichern Sie dann das Ziel. Beachten Sie Folgendes:

      * Bei Zielen, die für Advertising DSP-Pakete verwendet werden, muss dem Zielnamen &quot;ADSP_&quot;vorangestellt werden, z. B. &quot;ADSP_Registrierungen&quot;. Beim Präfix wird nicht zwischen Groß- und Kleinschreibung unterschieden.

      * Nur Metriken einschließen, die DSP zugeordnet sind. Alle Metriken, die Search, Social und Commerce oder einem anderen Anzeigennetzwerk zugeordnet sind, werden ignoriert.

      * Mindestens eine Metrik muss den Metriktyp aufweisen *[!UICONTROL Goal]*.

      * DSP verwendet die nicht mobile Gewichtung für alle Anzeigen. Alle angegebenen Mobilgewichte werden ignoriert.

      >[!NOTE]
      >
      >* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Benennungskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`
      >* [!DNL Analytics] -Dimensionen und -segmente stehen nicht zur Adobe Advertising-Optimierung zur Verfügung.

      >[!TIP]
      >
      >Für eine optimale Leistung müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens zehn Konversionen pro Tag umfassen. Andernfalls empfiehlt es sich, dem Ziel zusätzliche unterstützende Konversionsmetriken wie Produktseiten oder Anwendungsstarts hinzuzufügen. Siehe [Best Practices zum Erstellen eines benutzerdefinierten Ziels](#custom-goal-best-practices) für Leitlinien.

In den DSP Paketeinstellungen für Pakete, die das Optimierungsziel verwenden &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot;wird der Objektname jetzt im [!UICONTROL Custom Goals] Liste. Wenn Sie das Ziel als benutzerdefiniertes Ziel für ein Paket auswählen, wird die [!UICONTROL Conversion Metric] enthält alle Zielmetriken für das Ziel.

## Best Practices zum Erstellen eines benutzerdefinierten Ziels {#custom-goal-best-practices}

### Benutzerdefinierte Ziele mit einer einzelnen Metrik

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzige Konversionsmetrik abzielen.

#### Beispiel für eine Kampagne mit dem[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;Optimierungsziel

Wenn Ihr Kampagnenziel Umsatz ist ([!UICONTROL Highest Return on Ad Spend (ROAS)]), und der Umsatz aus allen Gerätetypen ist für Sie gleichermaßen wichtig. Schließen Sie dann die[!UICONTROL Revenue]&quot; Metrik mit einer nicht mobilen Gewichtung (für Konversionen von einem nicht mobilen Gerät) von einer (1) und einer mobilen Gewichtung (für Konversionen von einem Mobilgerät) von einer (1). Metriktyp auswählen *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine mobile oder nicht mobile Gewichtung von 1 (1) entspricht einem Wert von 1 (1) für jeden verfolgten Umsatz von 1 USD.
>
> Beispielsweise wird eine Konversion von 250 USD mit einer Gewichtung von 1 (1) ohne Mobilgeräte für Konversionen als 250 USD gemeldet. Wenn der Konversionsmetrik eine nicht mobile Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 USD von einem nicht mobilen Gerät als 125 USD in Adobe Advertising ( 250 USD Konversion * 0,5) gemeldet. [!UICONTROL Non-mobile Weight] = 125 USD).

#### Beispiel für eine Kampagne mit dem[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;Optimierungsziel

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) ist und nur ein Erfolgsereignis erforderlich ist (z. B. &quot;Antragsversand&quot;), schließen Sie diese eine Metrik ein und geben Sie den Metriktyp als *[!UICONTROL Goal]*. Als Best Practice wird empfohlen, sowohl das nicht mobile als auch das mobile Gewicht auf 1 (1) festzulegen.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine mobile oder nicht mobile Gewichtung von 1 (1) entspricht einem Wert von 1 (1) für jede verfolgte Konversion. Wenn z. B. 10 Konvertierungen von Antragssendungen verfolgt werden, werden 10 Konversionen von Antragsübermittlungen gemeldet. Wenn der Konversionsmetrik jedoch ein nicht mobiles Gewicht von 0,5 zugewiesen wird, werden die 10 nicht mobilen Konversionen als fünf (5) in Adobe Advertising (10 Konversionen * 0,5) gemeldet. [!UICONTROL Non-mobile Weight] = 5).

### Benutzerdefinierte Ziele mit mehreren Metriken

Es gibt zwei Szenarien, in denen Sie mehrere Metriken in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel umfasst mehrere Erfolgsereignisse. Vielleicht werben Sie beispielsweise für mehr als eine On-site-Aktion (PDF Download, Kontaktaufnahme und E-Mail-Anmeldung), und alle Aktionen tragen zu Ihrem CPA-Ziel bei. Wenn das Ziel die drei separaten Metriken mit jeweils einer nicht mobilen und mobilen Gewichtung von 1 (1) enthält, wird die [!DNL Adobe Sensei] -Algorithmus behandelt alle Metriken und Benutzergerätetypen mit gleicher Wichtigkeit. Wenn die verschiedenen Metriken und Gerätetypen unterschiedliche Kosten oder Bedeutung haben, passen Sie ihre relative Gewichtung entsprechend an.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Die einzelne Konversionsmetrik in Ihrem benutzerdefinierten Ziel erreicht nicht die Mindestanzahl von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Dies kann durch minimale tägliche Paketausgaben oder eine begrenzte Anzahl natürlicher Konversionen geschehen. Das Hinzufügen zusätzlicher unterstützender Metriken zum benutzerdefinierten Ziel kann Ihnen dabei helfen, den Schwellenwert von 10 Konversionen pro Tag zu erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, die Schwelle von 10 Tagen zu erreichen, selbst wenn jede seiner Gewichtungen unter 1 liegt. Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

  Wenn Sie einem benutzerdefinierten Ziel unterstützende Metriken hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und beachten Sie die Anzahl der Datenpunkte. Dadurch kann der Adobe Sensei-Algorithmus mehrere Metriken ausgleichen und Ihre Zielvorgabe optimieren.

  Das folgende Beispielziel umfasst drei Metriken mit jeweils einer anderen Gewichtung als Mobilgeräte: Application Submit = 1, Application Start = 0.1 und Advertiser Landingpage = 0.01. Das bedeutet, dass jede Submit-Konversion von Nicht-Mobilgeräten für Ihr Unternehmen denselben Wert hat wie durchschnittlich 10 Application Start-Konversionen von Nicht-Mobilgeräten und 100 Advertiser-Landingpage-Konversionen von Nicht-Mobilgeräten.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Wenn Sie stattdessen Landingpage-Besuche gleich den &quot;Application Submissions&quot;gewichten, könnte die natürlich höhere Anzahl von Landingpage-Besuchen Ihr Ziel überfordern und zu Landingpage-Besuchen verfälschen.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
