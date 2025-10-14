---
title: Benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; verwendet, muss ein benutzerdefiniertes Ziel enthalten, um zum Erreichen des übergeordneten Optimierungsziels beizutragen. Sie können benutzerdefinierte Ziele als *Ziele* in [!DNL Advertising Search, Social, & Commerce] erstellen. Dem Namen jedes Ziels für DSP muss „ADSP_“ vorangestellt werden.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Jedes benutzerdefinierte Ziel (Ziel) besteht aus einer oder mehreren Konversionsmetriken und den relativen Gewichtungen dieser Metriken. Die verfügbaren Konversionsmetriken umfassen alle Metriken, die mit dem Adobe Advertising-Konversionspixel und über Adobe Analytics verfolgt werden. Für benutzerdefinierte DSP-Ziele werden nur Gewichtungen außer Mobilgeräten berücksichtigt, sie werden jedoch für alle Anzeigentypen verwendet.

Angenommen, drei Konversionsmetriken sind für ein bestimmtes Paket in einer Ihrer Kampagnen relevant: &quot;PDF-Download“ im Wert von 20 USD, „E-Mail-Anmeldung“ im Wert von 30 USD und „Bestellbestätigung“ im Wert von 40 USD. Wenn Sie eine Gewichtung anhand des einmaligen Geldwerts der Kundenaktion angeben möchten, wären die relativen Gewichtungen der Metriken 1, 1,5 und 2.

Nachdem Sie [benutzerdefiniertes Ziel erstellt haben](#custom-goal-create) können Sie es [einem Paket zuweisen](/help/dsp/campaign-management/packages/package-settings.md) für die Berichterstellung und algorithmische Optimierung mit Adobe Sensei verwenden.

Gewichtungsempfehlungen werden automatisch für DSP-zugeordnete Metriken in Zielen generiert und können mit einem Klick auf alle Gewichtungsempfehlungen angewendet werden. Alle Gewichtungsänderungen an Zielen mit dem Präfix „ADSP_“ werden in DSP innerhalb von zwei Tagen algorithmisch angewendet. Weitere Informationen zu Gewichtungsempfehlungen finden Sie im Kapitel Optimierungshandbuch unter „Ziele“, das in Search, Social und Commerce verfügbar ist.

## Erstellen eines benutzerdefinierten Ziels {#custom-goal-create}

Um ein benutzerdefiniertes Ziel zu erstellen, muss das DSP-Konto mit einem [!DNL Search, Social, & Commerce]-Konto mit derselben Adobe Experience Cloud-Organisations-ID aus den [!DNL Search, Social, & Commerce] Client-Einstellungen heraus verknüpft werden. Wenn Ihr DSP-Konto nicht mit einem [!DNL Search, Social, & Commerce]-Konto verknüpft ist, wenden Sie sich an Ihr Adobe-Konto-Team.

1. [Bei Advertising Search, Social und Commerce anmelden](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}.

1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]** > **[!UICONTROL Conversions]**.

      Die Ansicht Konvertierungen wird in einem neuen Browser oder auf einer neuen Browser-Registerkarte geöffnet.

   1. Suchen Sie die Metrik und stellen Sie sicher, dass **[!UICONTROL Show in UI and Reports]** für die Metrik aktiviert ist.

      >[!NOTE]
      >
      >* [!DNL Analytics] benutzerdefinierten Ereignisse folgen dieser Namenskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`

   1. Wenn die Metrik in der **[!UICONTROL Display Name]** keinen Wert hat, klicken Sie in die Zelle, geben Sie den Anzeigenamen ein und klicken Sie auf **[!UICONTROL Apply].**

1. [Erstellen Sie das benutzerdefinierte Ziel als *Ziel*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}. Beachten Sie Folgendes:

   * Bei Zielen, die für Advertising DSP-Pakete verwendet werden, muss der Zielname mit dem Präfix „ADSP_“ versehen werden, z. B. „ADSP_Registrations“. Beim Präfix wird nicht zwischen Groß- und Kleinschreibung unterschieden.

   * Nur Metriken einschließen, die DSP zugeordnet sind. Alle Metriken, die Search, Social und Commerce oder einem anderen Werbenetzwerk zugeordnet wurden, werden ignoriert.

   * Mindestens eine Metrik muss den Metriktyp *[!UICONTROL Goal]* aufweisen.

   * DSP verwendet für alle Anzeigen die Gewichtungen für Nicht-Mobilgeräte. Alle angegebenen Gewichtungen für Mobilgeräte werden ignoriert.

   >[!NOTE]
   >
   >* [!DNL Analytics] benutzerdefinierten Ereignisse folgen dieser Namenskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`
   >* [!DNL Analytics] Dimensionen und Segmente sind nicht für die Adobe Advertising-Optimierung verfügbar.

   >[!TIP]
   >
   >Um eine optimale Leistung zu erzielen, müssen die kombinierten Metriken im benutzerdefinierten Ziel (Objective) mindestens zehn Konversionen pro Tag umfassen. Ist dies nicht der Fall, empfiehlt es sich, dem Ziel zusätzliche unterstützende Konversionsmetriken hinzuzufügen, z. B. Produktseiten oder Programmstarts. Richtlinien finden [&#x200B; unter „Best Practices zum Erstellen eines benutzerdefinierten &#x200B;](#custom-goal-best-practices)&quot;.

In den DSP-Paketeinstellungen für Pakete, die das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; verwenden, ist der Zielname jetzt in der [!UICONTROL Custom Goals]-Liste enthalten. Wenn Sie das Ziel als benutzerdefiniertes Ziel für ein Paket auswählen, enthält die [!UICONTROL Conversion Metric] alle Zielmetriken für das Ziel.

## Best Practices zum Erstellen eines benutzerdefinierten Ziels {#custom-goal-best-practices}

### Benutzerdefinierte Ziele mit einer einzelnen Metrik

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzelne Konversionsmetrik abzielen.

#### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Wenn Ihr Kampagnenziel der Umsatz ([!UICONTROL Highest Return on Ad Spend (ROAS)]) ist und der Umsatz mit allen Gerätetypen für Sie gleich wichtig ist, dann beziehen Sie die Metrik &quot;[!UICONTROL Revenue]&quot; mit einer Nicht-Mobilgerät-Gewichtung von 1 ein (1). Die Mobilgerät-Gewichtung wird ignoriert. Wählen Sie den Metriktyp *[!UICONTROL Goal]* aus.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine Nicht-Mobilgerät-Gewichtung von 1 (1) entspricht einem Wert von 1 (1) für jeden Umsatz in Höhe von 1 USD, der für Display-Anzeigen auf jedem Gerät verfolgt wird. Beispielsweise wird eine $250-Konversion mit einer Nicht-Mobile-Gewichtung von 1 (1) für -Konversionen als $250 gemeldet. Wenn der Konversionsmetrik eine Nicht-Mobilgerät-Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 $ in Adobe Advertising als 125 $ gemeldet (250 $ Konversion * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) sind und nur ein Erfolgsereignis erforderlich ist (z. B. „Antrag einreichen„), beziehen Sie diese eine Metrik ein und geben Sie den Metriktyp als *[!UICONTROL Goal]* an. Es empfiehlt sich, für die Gewichtung nicht mobiler Geräte einen Wert (1) festzulegen. Die Gewichtung für Mobilgeräte wird dabei ignoriert.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine nicht mobile Gewichtung von eins (1) entspricht einem Wert von eins (1) für jede Konvertierung, die für Display-Anzeigen auf einem beliebigen Gerät verfolgt wird. Wenn beispielsweise 10 Konversionen von Anwendungsübermittlungen verfolgt werden, werden 10 Konversionen von Anwendungsübermittlungen gemeldet. Wenn der Konversionsmetrik jedoch eine Nicht-Mobile-Gewichtung von 0,5 zugewiesen wird, werden die 10 Konversionen in Adobe Advertising als fünf (5) gemeldet (10 Konversionen * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Benutzerdefinierte Ziele mit mehreren Metriken

Es gibt zwei Szenarien, in denen Sie mehrere Metriken in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel hat mehrere Erfolgsereignisse. Vielleicht werben Sie für mehr als eine Aktion auf der Site (PDF-Download, Kontakt und E-Mail-Anmeldung) und alle Aktionen tragen zu Ihrem CPA-Ziel bei. Wenn das Ziel die drei separaten Metriken umfasst, von denen jede eine nicht mobile Gewichtung (1) aufweist, behandelt der [!DNL Adobe Sensei]-Algorithmus jede der Metriken und Benutzergerätetypen mit derselben Bedeutung. Wenn die verschiedenen Metriken unterschiedliche Kosten oder eine unterschiedliche Bedeutung haben, passen Sie ihre relativen Gewichtungen entsprechend an.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Die einzelne Konversionsmetrik in Ihrem benutzerdefinierten Ziel erreicht nicht das Minimum von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Dies kann aufgrund minimaler täglicher Paketausgaben oder einer begrenzten Anzahl natürlicher Konversionen auftreten. Durch Hinzufügen zusätzlicher unterstützender Metriken zum benutzerdefinierten Ziel können Sie den Schwellenwert von 10 Konversionen pro Tag erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, den Schwellenwert von 10/Tag zu erreichen, auch wenn jedes seiner Gewichtungen unter eins liegt (1). Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

  Wenn Sie einem benutzerdefinierten Ziel unterstützende Metriken hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und berücksichtigen Sie dabei die Anzahl der Datenpunkte. Auf diese Weise kann der Adobe Sensei-Algorithmus mehrere Metriken ausgleichen und für Ihr Ziel optimieren.

  Das folgende Beispielziel enthält drei Metriken mit jeweils einer anderen Nicht-Mobile-Gewichtung: Antragseinsendung = 1, Anwendungsstart = 0,1 und Advertiser-Landingpage = 0,01. Das bedeutet, dass jede Konvertierung einer Anwendung bei der Übermittlung denselben Wert für Ihr Unternehmen hat wie durchschnittlich 10 Konversionen beim Anwendungsstart und 100 Konversionen bei der Advertiser-Landingpage.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Wenn Sie stattdessen Landingpage-Besuche zu gleichen Teilen auf die Antragseinreichungen gewichten, kann die natürlich höhere Anzahl von Landingpage-Besuchen Ihr Ziel überfordern und zu Landingpage-Besuchen führen.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
