---
title: Benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
source-git-commit: 6dba85185789c365bd72787eb0fa16ef90bf6b9e
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das das Optimierungsziel verwendet &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; muss ein benutzerdefiniertes Ziel enthalten, das zum Erreichen des übergeordneten Optimierungsziels beiträgt. Sie können benutzerdefinierte Ziele erstellen als *Ziele* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Jedes benutzerdefinierte Ziel besteht aus einer oder mehreren Konversionsmetriken und den relativen Gewichtungen dieser Metriken. Die verfügbaren Konversionsmetriken enthalten alle Metriken, die mit dem Adobe Advertising-Konversionspixel und über Adobe Analytics verfolgt werden.

Angenommen, drei Konversionsmetriken sind für ein bestimmtes Paket in einer Ihrer Kampagnen relevant: &quot;PDF-Download“ im Wert von 20 USD, „E-Mail-Anmeldung“ im Wert von 30 USD und „Bestellbestätigung“ im Wert von 40 USD. Wenn Sie eine Gewichtung anhand des einmaligen Geldwerts der Kundenaktion angeben möchten, wären die relativen Gewichtungen der Metriken 1, 1,5 und 2.

Einmal [Erstellen eines benutzerdefinierten Ziels](#custom-goal-create), Sie können [Einem Paket zuweisen](/help/dsp/campaign-management/packages/package-settings.md) für das Reporting und die algorithmische Optimierung mit Adobe Sensei.

## Erstellen eines benutzerdefinierten Ziels {#custom-goal-create}

Um ein benutzerdefiniertes Ziel zu erstellen, muss das DSP-Konto mit einem verknüpft sein. [!DNL Search, Social, & Commerce] Konto mit derselben Adobe Experience Cloud-Organisations-ID aus dem [!DNL Search, Social, & Commerce] Client-Einstellungen. Wenn Ihr DSP-Konto nicht mit einem verknüpft ist [!DNL Search, Social, & Commerce] Account, dann kontaktieren Sie Ihr Adobe Account Team.

1. Anmelden bei [!DNL Advertising Search, Social, & Commerce] at (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) oder (alle anderen Benutzer) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Suchen Sie die Metrik und stellen Sie Folgendes sicher **[!UICONTROL Show in UI and Reports]** ist für die Metrik aktiviert.

      >[!NOTE]
      >
      >* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Namenskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`

   1. Wenn die Metrik keinen Wert in der **[!UICONTROL Display Name]** -Spalte verwenden, dann in die Zelle klicken, den Anzeigenamen eingeben und auf Folgendes klicken **[!UICONTROL Apply].**

1. Erstellen Sie das benutzerdefinierte Ziel als *Ziel*:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Klicken Sie in der Symbolleiste auf ![Erstellen](/help/dsp/assets/create-search-ui.png "Erstellen").

   1. Geben Sie die Zieleinstellungen ein, einschließlich der zugehörigen Metriken und ihrer relativen numerischen Gewichtung für nicht mobile Geräte und Mobilgeräte, und speichern Sie dann das Ziel.

      Mindestens eine Metrik muss den Metriktyp aufweisen *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Namenskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`
      >* [!DNL Analytics] Dimensionen und Segmente sind nicht für die Adobe Advertising-Optimierung verfügbar.

      >[!TIP]
      >
      >Um eine optimale Leistung zu erzielen, müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens zehn Konversionen pro Tag umfassen. Ist dies nicht der Fall, empfiehlt es sich, dem Ziel zusätzliche unterstützende Konversionsmetriken hinzuzufügen, z. B. Produktseiten oder Anwendungsstarts. Siehe [Best Practices zum Erstellen eines benutzerdefinierten Ziels](#custom-goal-best-practices) für Richtlinien.

In den DSP-Paketeinstellungen für Pakete, die das Optimierungsziel verwenden &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],“ der Zielname ist jetzt im [!UICONTROL Custom Goals] Liste. Wenn Sie das Ziel als benutzerdefiniertes Ziel für ein Paket auswählen, wird die [!UICONTROL Conversion Metric] Die Liste enthält alle Zielmetriken für das Ziel.

## Best Practices zum Erstellen eines benutzerdefinierten Ziels {#custom-goal-best-practices}

### Benutzerdefinierte Ziele mit einer einzelnen Metrik

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzelne Konversionsmetrik abzielen.

#### Beispiel für eine Kampagne mit dem &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]„Optimierungsziel

Wenn Ihr Kampagnenziel der Umsatz ist ([!UICONTROL Highest Return on Ad Spend (ROAS)]), und der Umsatz aus allen Gerätetypen ist für Sie gleichermaßen wichtig, dann schließen Sie &quot;[!UICONTROL Revenue]Metrik &quot; mit einer Nicht-Mobilgerät-Gewichtung (für Konversionen von einem Nicht-Mobilgerät) von einer (1) und einer Mobile-Gewichtung (für Konversionen von einem Mobilgerät) von einer (1). Metriktyp auswählen *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine Gewichtung für Mobilgeräte oder Nicht-Mobilgeräte von 1 (1) entspricht einem Wert von 1 (1) für jeden nachverfolgten Umsatz in Höhe von 1 USD.
>
> Beispielsweise wird eine Konversion von 250 $ bei einer nicht mobilen Gewichtung von 1 (1) als 250 $ für Konversionen gemeldet. Wenn der Konversionsmetrik eine Nicht-Mobilgerät-Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 USD von einem Nicht-Mobilgerät als 125 USD in Adobe Advertising (Konversion von 250 USD * 0,5) gemeldet [!UICONTROL Non-mobile Weight] = 125 $).

#### Beispiel für eine Kampagne mit dem &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]„Optimierungsziel

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) sind und nur ein Erfolgsereignis erforderlich ist (z. B. „Antrag einreichen„), schließen Sie diese eine Metrik ein und geben Sie den Metriktyp als an *[!UICONTROL Goal]*. Es empfiehlt sich, sowohl das Gewicht für Mobilgeräte als auch das Gewicht für Mobilgeräte auf einen Wert festzulegen (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine Mobile-Gewichtung oder Nicht-Mobile-Gewichtung von Eins (1) entspricht einem Wert von Eins (1) für jede verfolgte Konversion. Wenn beispielsweise 10 Konversionen von Anwendungsübermittlungen verfolgt werden, werden 10 Konversionen von Anwendungsübermittlungen gemeldet. Wenn der Konversionsmetrik jedoch eine Nicht-Mobile-Gewichtung von 0,5 zugewiesen wird, werden die 10 Nicht-Mobile-Konversionen in Adobe Advertising als fünf (5) gemeldet (10 Konversionen * 0,5) [!UICONTROL Non-mobile Weight] = 5).

### Benutzerdefinierte Ziele mit mehreren Metriken

Es gibt zwei Szenarien, in denen Sie mehrere Metriken in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel hat mehrere Erfolgsereignisse. Vielleicht werben Sie für mehr als eine Onsite-Aktion (PDF-Download, Kontakt und E-Mail-Anmeldung), und alle Aktionen tragen zu Ihrem CPA-Ziel bei. Wenn das Ziel die drei separaten Metriken mit jeweils einer Gewichtung für Nicht-Mobilgeräte und Mobilgeräte von einem umfasst (1), [!DNL Adobe Sensei] Algorithmus behandelt jede der Metriken und Typen von Benutzergeräten mit gleicher Wichtigkeit. Wenn die verschiedenen Metriken und Gerätetypen unterschiedliche Kosten oder eine unterschiedliche Bedeutung haben, passen Sie ihre relativen Gewichtungen entsprechend an.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Die einzelne Konversionsmetrik in Ihrem benutzerdefinierten Ziel erreicht nicht das Minimum von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Dies kann aufgrund minimaler täglicher Paketausgaben oder einer begrenzten Anzahl natürlicher Konversionen auftreten. Durch Hinzufügen zusätzlicher unterstützender Metriken zum benutzerdefinierten Ziel können Sie den Schwellenwert von 10 Konversionen pro Tag erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, den Schwellenwert von 10/Tag zu erreichen, auch wenn jedes seiner Gewichtungen unter eins liegt (1). Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

  Wenn Sie einem benutzerdefinierten Ziel unterstützende Metriken hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und berücksichtigen Sie dabei die Anzahl der Datenpunkte. Auf diese Weise kann der Adobe Sensei-Algorithmus mehrere Metriken ausgleichen und für Ihr Ziel optimieren.

  Das folgende Beispielziel enthält drei Metriken mit jeweils einer anderen Nicht-Mobile-Gewichtung: Antragseinsendung = 1, Anwendungsstart = 0,1 und Advertiser-Landingpage = 0,01. Das bedeutet, dass jede Konversion von Mobile Apps über Nicht-Mobilgeräte denselben Wert für Ihr Unternehmen hat wie durchschnittlich 10 Konversionen von Mobile Apps von Nicht-Mobilgeräten und 100 Konversionen von Advertiser-Landingpages von Nicht-Mobilgeräten.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Wenn Sie stattdessen Landingpage-Besuche zu gleichen Teilen mit den eingereichten Anwendungen gewichten, könnte die natürlich höhere Anzahl von Landingpage-Besuchen Ihr Ziel übertreffen und zu Landingpage-Besuchen tendieren.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
