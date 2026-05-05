---
title: Best Practices für benutzerdefinierte Ziele
description: Erfahren Sie mehr über die Best Practices zur Definition benutzerdefinierter Ziele für Pakete, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# Best Practices für benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; verwendet, muss ein benutzerdefiniertes Ziel enthalten, um zum Erreichen des übergeordneten Optimierungsziels beizutragen. Sie können benutzerdefinierte Ziele als *[benutzerdefinierte Ziele“](/help/dsp/admin/custom-objectives-manage.md)*.

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Jedes benutzerdefinierte Ziel (Ziel) besteht aus einer oder mehreren zu verfolgenden und zu optimierenden Konversionsmetriken sowie den relativen Gewichtungen dieser Metriken. Sie können [einem Paket ein benutzerdefiniertes Ziel zuweisen](/help/dsp/campaign-management/packages/package-settings.md) für die Berichterstellung und algorithmische Optimierung mit [!DNL Adobe AI].

Informationen zum Erstellen und Verwalten benutzerdefinierter Ziele finden Sie unter [Verwalten benutzerdefinierter Ziele](/help/dsp/admin/custom-objectives-manage.md).

## Benutzerdefinierte Ziele mit einer einzelnen Metrik

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzelne Konversionsmetrik abzielen.

### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;

Wenn Ihr Kampagnenziel der Umsatz ([!UICONTROL Highest Return on Ad Spend (ROAS)]) ist und der Umsatz aus allen Gerätetypen für Sie gleich wichtig ist, dann beziehen Sie die Metrik &quot;[!UICONTROL Revenue]&quot; mit einer Gewichtung von 1 ein (1). Wählen Sie den Metriktyp *[!UICONTROL Goal]* aus.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine Gewichtung von 1 (1) entspricht einem Wert von 1 (1) für jeden Umsatz in Höhe von 1 USD, der für Display-Anzeigen auf einem beliebigen Gerät verfolgt wird. Beispielsweise wird eine $250-Konversion mit der Gewichtung eins (1) für -Konversionen als $250 gemeldet. Wenn der Konversionsmetrik eine Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 $ in Adobe Advertising als 125 $ gemeldet (Konversion von 250 $ * 0,5 [!UICONTROL weight] = 125 $).

### Beispiel für eine Kampagne mit dem Optimierungsziel &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) sind und nur ein Erfolgsereignis erforderlich ist (z. B. „Antrag einreichen„), beziehen Sie diese eine Metrik ein und geben Sie den Metriktyp als *[!UICONTROL Goal]* an. Es empfiehlt sich, die Gewichtung auf einen Wert (1) festzulegen.

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Eine Gewichtung von Eins (1) entspricht einem Wert von Eins (1) für jede Konvertierung, die für Display-Anzeigen auf einem beliebigen Gerät verfolgt wird. Wenn beispielsweise 10 Konversionen von Anwendungsübermittlungen verfolgt werden, werden 10 Konversionen von Anwendungsübermittlungen gemeldet. Wenn der Konversionsmetrik jedoch eine Gewichtung von 0,5 zugewiesen wird, werden die 10 Konversionen in Adobe Advertising als fünf (5) gemeldet (10 Konversionen * 0,5 [!UICONTROL weight] = 5).

## Benutzerdefinierte Ziele mit mehreren Metriken

Es gibt zwei Szenarien, in denen Sie mehrere Metriken in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel hat mehrere Erfolgsereignisse. Vielleicht werben Sie für mehr als eine Aktion auf der Site (PDF-Download, Kontakt und E-Mail-Anmeldung) und alle Aktionen tragen zu Ihrem CPA-Ziel bei. Wenn das Ziel die drei separaten Metriken mit jeweils einer Gewichtung von 1 umfasst, behandelt der [!DNL Adobe AI] Algorithmus jede der Metriken und die Typen der Benutzergeräte mit gleicher Wichtigkeit. Wenn die verschiedenen Metriken unterschiedliche Kosten oder eine unterschiedliche Bedeutung haben, passen Sie ihre relative Gewichtung entsprechend an.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* Die einzelne Konversionsmetrik in Ihrem benutzerdefinierten Ziel erreicht nicht das Minimum von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Niedrigere Konversionszahlen können aufgrund minimaler täglicher Paketausgaben oder einer begrenzten Anzahl natürlicher Konversionen auftreten. Durch Hinzufügen zusätzlicher unterstützender Metriken zum benutzerdefinierten Ziel können Sie den Schwellenwert von 10 Konversionen pro Tag erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, den Schwellenwert von 10/Tag zu erreichen, auch wenn jedes seiner Gewichtungen unter eins liegt (1). Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

  Wenn Sie einem benutzerdefinierten Ziel unterstützende Metriken hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und berücksichtigen Sie dabei die Anzahl der Datenpunkte. Auf diese Weise kann der [!DNL Adobe AI] Algorithmus mehrere Metriken ausgleichen und für Ihr Ziel optimieren.

  Das folgende Beispielziel enthält drei Metriken mit jeweils unterschiedlicher Gewichtung: Antragseinsendung = 1, Anwendungsstart = 0,1 und Advertiser-Landingpage = 0,01. Das bedeutet, dass jede Konvertierung einer Anwendung bei der Übermittlung denselben Wert für Ihr Unternehmen hat wie durchschnittlich 10 Konversionen beim Anwendungsstart und 100 Konversionen bei der Advertiser-Landingpage.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Wenn Sie stattdessen die Landingpage-Besuche zu gleichen Teilen auf die Antragseinreichungen gewichten, könnte die natürlich höhere Anzahl von Landingpage-Besuchen Ihr Ziel überfordern und die Optimierung der Landingpage-Besuche verfälschen.

>[!MORELIKETHIS]
>
>* [Benutzerdefinierte Ziele verwalten](/help/dsp/admin/custom-objectives-manage.md)
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
