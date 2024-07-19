---
title: Benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 290eea50fe3c52a534ad6ab4fcf6d857b13230aa
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot;oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;verwendet, muss ein benutzerdefiniertes Ziel enthalten, um das Gesamtoptimierungsziel zu erreichen. Sie können benutzerdefinierte Ziele als *Ziele* in [!DNL Advertising Search, Social, & Commerce] erstellen. Dem Namen jedes Ziels für DSP muss &quot;ADSP_&quot;vorangestellt werden.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Jedes benutzerdefinierte Ziel (Ziel) besteht aus einer oder mehreren Konversionsmetriken und den relativen Gewichtungen dieser Metriken. Zu den verfügbaren Konversionsmetriken gehören alle Metriken, die mit dem Adobe Advertising-Konversionspol und über Adobe Analytics verfolgt werden. Für DSP benutzerspezifischen Ziele werden nur nicht mobile Gewichtungen berücksichtigt, die jedoch für alle Anzeigentypen verwendet werden.

Angenommen, drei Konversionsmetriken sind für ein bestimmtes Kampagnenkit relevant: &quot;PDF-Download&quot;im Wert von 20 USD, &quot;E-Mail-Anmeldung&quot;im Wert von 30 USD und &quot;Auftragsbestätigung&quot;im Wert von 40 USD. Wenn Sie Gewichtung gemäß dem einmaligen Geldwert der Kundenaktion geben möchten, beträgt das relative Gewicht der Metriken 1, 1,5 und 2.

Nachdem Sie [ ein benutzerdefiniertes Ziel ](#custom-goal-create) erstellt haben, können Sie es [einem Paket](/help/dsp/campaign-management/packages/package-settings.md) zuweisen, um die Berichterstellung und Algorithmusoptimierung mit Adobe Sensei durchzuführen.

Gewichtungsempfehlungen werden automatisch für DSP zugeordneten Metriken in Zielen generiert und können alle Gewichtungsempfehlungen mit einem Klick anwenden. Alle Gewichtsänderungen an Zielen mit dem Präfix &quot;ADSP_&quot;werden in DSP innerhalb von zwei Tagen algorithmisch angewendet. Weitere Informationen zu Gewichtungsempfehlungen finden Sie im Kapitel &quot;Optimierungshandbuch&quot;zu &quot;Neue Ziele (Beta)&quot;, das in Search, Social und Commerce verfügbar ist.

## Benutzerdefiniertes Ziel erstellen {#custom-goal-create}

Um ein benutzerdefiniertes Ziel zu erstellen, muss das DSP-Konto mit einem [!DNL Search, Social, & Commerce]-Konto mit derselben Adobe Experience Cloud-Organisations-ID aus den [!DNL Search, Social, & Commerce]-Clienteinstellungen verknüpft sein. Wenn Ihr DSP-Konto nicht mit einem [!DNL Search, Social, & Commerce] -Konto verknüpft ist, wenden Sie sich an Ihr Adobe-Account-Team.

1. Melden Sie sich bei [!DNL Advertising Search, Social, & Commerce] an unter (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) oder (alle anderen Benutzer) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Suchen Sie die Metrik und stellen Sie sicher, dass **[!UICONTROL Show in UI and Reports]** für die Metrik aktiviert ist.

      >[!NOTE]
      >
      >* [!DNL Analytics] benutzerspezifische Ereignisse folgen dieser Benennungsregel: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`

   1. Wenn die Metrik keinen Wert in der Spalte **[!UICONTROL Display Name]** hat, klicken Sie in die Zelle, geben Sie den Anzeigenamen ein und klicken Sie auf **[!UICONTROL Apply]**.

1. Erstellen Sie das benutzerdefinierte Ziel als *Ziel*:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Klicken Sie in der Symbolleiste auf ![Erstellen](/help/dsp/assets/create-search-ui.png "Erstellen") .

   1. Geben Sie die Zieleinstellungen, einschließlich der zugehörigen Metriken, und ihre relative numerische Gewichtung für Nicht-Mobilgeräte ein und speichern Sie dann das Ziel. Beachten Sie Folgendes:

      * Bei Zielen, die für Advertising DSP-Pakete verwendet werden, muss dem Zielnamen &quot;ADSP_&quot;vorangestellt werden, z. B. &quot;ADSP_Registrierungen&quot;. Beim Präfix wird nicht zwischen Groß- und Kleinschreibung unterschieden.

      * Nur Metriken einschließen, die DSP zugeordnet sind. Alle Metriken, die Search, Social und Commerce oder einem anderen Anzeigennetzwerk zugeordnet sind, werden ignoriert.

      * Mindestens eine Metrik muss den Metriktyp *[!UICONTROL Goal]* aufweisen.

      * DSP verwendet die nicht mobile Gewichtung für alle Anzeigen. Alle angegebenen Mobilgewichte werden ignoriert.

      >[!NOTE]
      >
      >* [!DNL Analytics] benutzerspezifische Ereignisse folgen dieser Benennungsregel: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`
      >* [!DNL Analytics] Dimensionen und Segmente stehen nicht zur Adobe Advertising-Optimierung zur Verfügung.

      >[!TIP]
      >
      >Für eine optimale Leistung müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens zehn Konversionen pro Tag umfassen. Andernfalls empfiehlt es sich, dem Ziel zusätzliche unterstützende Konversionsmetriken wie Produktseiten oder Anwendungsstarts hinzuzufügen. Richtlinien finden Sie unter [Best Practices zum Erstellen eines benutzerdefinierten Ziels](#custom-goal-best-practices) .

In den DSP Paketeinstellungen für Pakete, die das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot;oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;verwenden, ist der Objektname jetzt in der Liste [!UICONTROL Custom Goals] enthalten. Wenn Sie das Ziel als benutzerdefiniertes Ziel für ein Paket auswählen, enthält die Liste [!UICONTROL Conversion Metric] alle Zielmetriken für das Ziel.

## Best Practices zum Erstellen eines benutzerdefinierten Ziels {#custom-goal-best-practices}

### Benutzerdefinierte Ziele mit einer einzelnen Metrik

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzige Konversionsmetrik abzielen.

#### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Wenn Ihr Kampagnenziel Umsatz ([!UICONTROL Highest Return on Ad Spend (ROAS)]) ist und der Umsatz aus allen Gerätetypen für Sie gleichermaßen wichtig ist, fügen Sie die Metrik &quot;[!UICONTROL Revenue]&quot;mit einer nicht mobilen Gewichtung von 1 (1) hinzu. Die Mobilgewichtung wird ignoriert. Wählen Sie den Metriktyp *[!UICONTROL Goal]* aus.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine nicht mobile Gewichtung von 1 (1) entspricht einem Wert (1) für jeden $1 Umsatz, der für Display-Anzeigen auf jedem Gerät verfolgt wird. Beispielsweise wird eine Konversion von 250 USD mit einer Gewichtung von 1 (1) ohne Mobilgeräte für Konversionen als 250 USD gemeldet. Wenn der Konversionsmetrik eine nicht mobile Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 USD als 125 USD in Adobe Advertising gemeldet ($250 Konversion * 0,5 [!UICONTROL Non-mobile Weight] = $125).

#### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) ist und nur ein Erfolgsereignis erforderlich ist (z. B. &quot;Antragsversand&quot;), schließen Sie diese eine Metrik ein und geben Sie den Metriktyp als *[!UICONTROL Goal]* an. Die Best Practice besteht darin, die Gewichtung für Nicht-Mobilgeräte auf 1 festzulegen (1). Die Mobilgewichtung wird ignoriert.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine nicht mobile Gewichtung von 1 (1) entspricht einem Wert von 1 (1) für jede Konversion, die für Display-Anzeigen auf jedem Gerät verfolgt wird. Wenn z. B. 10 Konvertierungen von Antragssendungen verfolgt werden, werden 10 Konversionen von Antragsübermittlungen gemeldet. Wenn der Konversionsmetrik jedoch eine nicht mobile Gewichtung von 0,5 zugewiesen wird, werden die 10 Konversionen als fünf (5) in Adobe Advertising gemeldet (10 Konversionen * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Benutzerdefinierte Ziele mit mehreren Metriken

Es gibt zwei Szenarien, in denen Sie mehrere Metriken in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel umfasst mehrere Erfolgsereignisse. Vielleicht werben Sie beispielsweise für mehr als eine On-site-Aktion (PDF Download, Kontaktaufnahme und E-Mail-Anmeldung), und alle Aktionen tragen zu Ihrem CPA-Ziel bei. Wenn das Ziel die drei separaten Metriken mit jeweils einer nicht mobilen Gewichtung (1) enthält, behandelt der [!DNL Adobe Sensei] -Algorithmus jede Metrik und jeden Benutzergerätetyp mit gleicher Bedeutung. Wenn die verschiedenen Metriken unterschiedliche Kosten oder Bedeutung haben, passen Sie ihre relative Gewichtung entsprechend an.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Die einzelne Konversionsmetrik in Ihrem benutzerdefinierten Ziel erreicht nicht die Mindestanzahl von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Dies kann durch minimale tägliche Paketausgaben oder eine begrenzte Anzahl natürlicher Konversionen geschehen. Das Hinzufügen zusätzlicher unterstützender Metriken zum benutzerdefinierten Ziel kann Ihnen dabei helfen, den Schwellenwert von 10 Konversionen pro Tag zu erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, die Schwelle von 10 Tagen zu erreichen, selbst wenn jede seiner Gewichtungen unter 1 liegt. Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

  Wenn Sie einem benutzerdefinierten Ziel unterstützende Metriken hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und beachten Sie die Anzahl der Datenpunkte. Dadurch kann der Adobe Sensei-Algorithmus mehrere Metriken ausgleichen und Ihre Zielvorgabe optimieren.

  Das folgende Beispielziel umfasst drei Metriken mit jeweils einer anderen Gewichtung als Mobilgeräte: Application Submit = 1, Application Start = 0.1 und Advertiser Landingpage = 0.01. Das bedeutet, dass jede Konvertierung des Antragsversands denselben Wert für Ihr Unternehmen hat wie im Durchschnitt 10 Konversionen des Anwendungsbeginns und 100 Konversionen der Advertiser-Landingpage.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Wenn Sie stattdessen die Besuche von Landingpages gleich den Einstiegsseiten-Sendevorgängen gewichten, könnte die natürlich höhere Anzahl von Einstiegsseitenbesuchen Ihr Ziel überfordern und die Besuche von Landingpages verfälschen.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimierungsziele und deren Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
