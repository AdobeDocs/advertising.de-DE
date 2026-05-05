---
title: Benutzerdefinierte Ziele verwalten
description: Erfahren Sie, wie Sie die Erfolgsereignisse definieren, die Ihnen beim Erreichen der Optimierungsziele auf Paketebene helfen.
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# Benutzerdefinierte Ziele verwalten

*Verfügbar für DSP-Konten, die mit Search-, Social- und Commerce-Konten verknüpft sind*

Ziele definieren die Erfolgsereignisse, die ein Advertiser festlegt, um seine Geschäftsziele zu erreichen. Ziele sind für DSP-Pakete als &quot;[&quot; ](/help/dsp/campaign-management/packages/package-settings.md). Jedes Paket, das das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; verwendet, muss ein benutzerdefiniertes Ziel enthalten, um zum Erreichen des übergeordneten Optimierungsziels beizutragen.

Ein Ziel besteht aus den zu verfolgenden und zu optimierenden Metriken (Eigenschaften) und den relativen Gewichtungen dieser Metriken. Jedes Ziel kann Folgendes umfassen:

* **[!UICONTROL Goal]Metriken** die die primären Erfolgsmetriken eines Advertisers darstellen. Sie beinhalten in der Regel zentrale Geschäftsergebnisse für ein Paket, z. B. Umsatz, Leads oder Umsatz. Jedes Ziel muss mindestens eine Zielmetrik haben.

* Optionale **[!UICONTROL Assist]Metriken** die die Zielmetriken unterstützen, vorhersagen, vorausgehen oder dazu beitragen. Beispiele sind Interaktionsmetriken wie Testfahrten und Testsendungen.

  Sie können [!DNL Adobe AI] die automatische Zuweisung und Aktualisierung von gewichteten Assist-Ereignissen ermöglichen, um Ihre Zielereignisse zu maximieren. Wenn Sie lieber Ihre eigenen gewichteten Assist-Metriken zuweisen möchten, kann DSP optional Assist-Metriken auf der Grundlage früherer Leistungsdaten aus Adobe Advertising und Adobe Analytics empfehlen. Sie können auswählen, ob Sie die Empfehlungen anwenden möchten oder nicht.

Alle Änderungen an den Zieloptionen werden auf Feldebene verfolgt und in einem Änderungsprotokoll aufgeführt.

>[!PREREQUISITES]
>
>Bevor Sie Ziele erstellen können, muss das DSP-Konto mit einem Search-, Social- und Commerce-Konto mit derselben Adobe Experience Cloud-Organisations-ID verknüpft sein, auch wenn Sie kein Kunde von Search, Social und Commerce sind. Wenn Ihr DSP-Konto nicht mit einem [!DNL Search, Social, & Commerce]-Konto verknüpft ist, wenden Sie sich an Ihr Adobe-Konto-Team.

>[!NOTE]
>
>* Advertising Search, Social und Commerce verwenden ebenfalls Ziele. Jedes Portfolio von Search, Social und Commerce muss ein Ziel haben, damit die Optimierungsfunktion Klick- und Umsatzmodelle für das Portfolio erstellen kann.
>* Sie können dasselbe Ziel für mehrere DSP-Pakete und/oder mehrere Search-, Social- und Commerce-Portfolios verwenden.

## Verfügbare Metriken

Sie können eine der folgenden Komponenten in Ihre Ziele einbeziehen:

* Metriken, die Adobe Advertising mithilfe des [Adobe Advertising-Konversionsverfolgungspixels](/help/search-social-commerce/tracking/conversion-tracking-advertising.md) verfolgt.

* (Advertisers mit [!DNL Adobe Analytics for Advertising]) [Konversions- und Site-Interaktionsmetriken wurden aus Adobe Analytics synchronisiert](/help/integrations/analytics/overview.md).

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## Zielstatus

Die Ansicht [!UICONTROL Settings] > [!UICONTROL Custom Objectives] zeigt den Status der einzelnen Ziele an. Werte können Folgendes beinhalten:

* *[!UICONTROL Waiting]*: Das Ziel befindet sich in einem Entwurfsstatus, bis Empfehlungen generiert werden.

* *[!UICONTROL Active]*: Das Ziel ist gespeichert und nutzbar.

## Empfehlungsstatus

* *[!UICONTROL Not Initiated]*: Es wurde keine Empfehlung angefordert.

* *[!UICONTROL Generating]*: Es werden Empfehlungen generiert.

* *[!UICONTROL Ready]*: Empfehlungen können angewendet werden.

* *[!UICONTROL Error]*: Empfehlungen konnten nicht generiert werden.

## Erstellen eines Ziels

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

1. Geben Sie die [Zieleinstellungen](#custom-objective-settings) ein.

   Bei der Auswahl von „Automated Bidding“ können Sie dem Ziel Eigenschaften (Metriken) als &quot;[!UICONTROL Goal]&quot; Metriken zuweisen. Bei benutzerdefinierten Geboten können Sie Eigenschaften entweder als &quot;[!UICONTROL Goal]&quot; oder als gewichtete &quot;[!UICONTROL Assist]&quot; Metriken zuweisen, Sie müssen jedoch mindestens eine Zielmetrik einbeziehen.

   Die Beschriftungen „Ziel“ und „Unterstützung“ wirken sich nicht auf die Optimierung aus. Nur die Gewichtungen der eingeschlossenen Metriken beeinflussen die Optimierung.

1. (Ziele mit benutzerdefinierter Gebotsabgabe; optional) Klicken Sie auf &quot;**[!UICONTROL Generate]**&quot; im unteren Abschnitt, um die empfohlenen Hilfemetriken auf der Grundlage vergangener Leistungsdaten zu generieren. Klicken Sie in der **[!UICONTROL Generate Recommendation]** auf **[!UICONTROL Generate]**.

   Die Generierung empfohlener Metriken kann bis zu 20 Minuten dauern. Während die Empfehlungen generiert werden, wird der Status des benutzerdefinierten Ziels *[!UICONTROL Waiting]*. Sobald die Empfehlungen generiert wurden, können Sie &quot;[ empfohlenen Assist-Ereignisse anzeigen und ](#view-apply-recommendations)&quot;.

1. (Wenn Sie keine Empfehlungen generiert haben) Klicken Sie oben rechts auf **[!UICONTROL Save]**.

In den [DSP](/help/dsp/campaign-management/packages/package-settings.md)Paketeinstellungen für Pakete, die das Optimierungsziel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; verwenden, ist der Zielname jetzt in der [!UICONTROL Custom Goals]-Liste enthalten. Wenn Sie das Ziel als benutzerdefiniertes Ziel für ein Paket auswählen, enthält die [!UICONTROL Conversion Metric] alle Zielmetriken für das Ziel.

## Bearbeiten eines Ziels

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Klicken Sie in der Zeile auf **…*** > **[!UICONTROL Edit]**.

1. Ändern Sie eine der [Zieleinstellungen](#custom-objective-settings).

1. (Wenn Empfehlungen verfügbar sind; optional) Anzeigen und optional Anwenden von empfohlenen Metriken:

   1. Klicken Sie im unteren Abschnitt auf **[!UICONTROL View Recommendations]**.

   1. Um eine Empfehlung anzuwenden, führen Sie einen der folgenden Schritte aus:

      * Klicken Sie **[!UICONTROL Apply]** neben der Empfehlung auf.

      * Passen Sie die Empfehlung manuell an und klicken Sie dann neben der Empfehlung auf **[!UICONTROL Apply]** .

   1. Klicken Sie auf **[!UICONTROL Close]** , um die [!UICONTROL Recommendations] zu schließen.

   Änderungen werden wirksam, nachdem die Zieleinstellungen synchronisiert wurden.

1. (Ziele mit benutzerdefinierter Gebotsabgabe; optional) Um empfohlene Hilfsmetriken auf der Grundlage vergangener Leistungsdaten zu generieren, klicken Sie auf **[!UICONTROL Generate]** im unteren Abschnitt. Klicken Sie in der **[!UICONTROL Generate Recommendation]** auf **[!UICONTROL Generate]**.

   Die Generierung empfohlener Metriken kann bis zu 20 Minuten dauern. Während die Empfehlungen generiert werden, wird der Status des benutzerdefinierten Ziels *[!UICONTROL Waiting]*. Sobald die Empfehlungen generiert wurden, können Sie &quot;[ empfohlenen Assist-Ereignisse anzeigen und ](#view-apply-recommendations)&quot;.

1. (Wenn Sie keine neuen Empfehlungen generiert haben) Klicken Sie oben rechts auf **[!UICONTROL Save]**.

## Anzeigen und Anwenden empfohlener Hilfereignisse {#view-apply-recommendations}

*Ziele mit benutzerdefinierter Gebotsabgabe*

Sie können Empfehlungen anzeigen und optional anwenden, wenn der Zielstatus *[!UICONTROL Active]* und die [!UICONTROL Recommendation Status] *[!UICONTROL Ready]* ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Klicken Sie in der Zeile auf **…*** > **[!UICONTROL Edit]**.

1. Klicken Sie im unteren Abschnitt auf **[!UICONTROL View Recommendations]**.

1. (Optional) Führen Sie einen der folgenden Schritte aus, um eine Empfehlung anzuwenden:

   * Klicken Sie **[!UICONTROL Apply]** neben der Empfehlung auf.

   * Passen Sie die Empfehlung manuell an und klicken Sie dann neben der Empfehlung auf **[!UICONTROL Apply]** .

1. Klicken Sie auf **[!UICONTROL Close]** , um die [!UICONTROL Recommendations] zu schließen.

1. Klicken Sie oben rechts auf **[!UICONTROL Save]**.

   Änderungen werden wirksam, nachdem die Zieleinstellungen synchronisiert wurden.

## Anzeigen des Änderungsprotokolls für ein benutzerdefiniertes Ziel

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Klicken Sie in der Zeile auf **…*** > **[!UICONTROL Change Log]**.

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Benutzerdefinierte Zieleinstellungen {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Abschnitt | Parameter | Beschreibung |
|---------|-----------|-------------|
| Grundlegende Details | AMOClient | Die eindeutige Adobe Advertising-ID des Werbetreibenden. |
| Grundlegende Details | Name des Ziels | Der Name des Ziels.<br><br>Alle Zielnamen für Advertising DSP müssen mit dem Präfix „ADSP_“ versehen werden (nicht von Schreibweise abhängig), z. B. „ADSP_Registrations“. Verwenden Sie einen Namen, der leicht zu identifizieren ist, wenn Sie ihn einem Paket zuweisen möchten. |
|  | Beschreibung | (Optional) Eine Beschreibung des Ziels. Die Beschreibung wird angezeigt, wenn Sie den Cursor über den Namen in der Liste Benutzerdefinierte Ziele halten. Wenn Sie keine Beschreibung angeben, wird stattdessen der Zielname wiederholt. |
| Gebotsstrategie |  | Die Angebotsstrategie des Ziels, die die Ereignistypen bestimmt, die Sie konfigurieren können:<ul><li><b>[!UICONTROL Automated Bidding]:</b> Weisen Sie dem Ziel Eigenschaften (Metriken) als [!DNL goal] Metriken zu. [!DNL Adobe AI] weist automatisch gewichtete Assist-Ereignisse zu und aktualisiert diese, um mithilfe eines ausgewogenen Ansatzes von funnel Ihre Zielereignisse zu maximieren.</li><li><b>[!UICONTROL Custom Bidding]:</b> Richten Sie Ihre eigene Gebotsstrategie ein, indem Sie Eigenschaften entweder als &quot;[!DNL goal]&quot; oder als gewichtete &quot;[!DNL assist]&quot; Ereignisse zuweisen. Verwenden Sie diese erweiterte Option für vordefinierte Strategien.</li></ul>Wenn Sie die Bid-Strategie ändern, werden alle zuvor ausgewählten Metriken gelöscht. |
| Eigenschaften | [!UICONTROL Available Metrics] | Alle für den Advertiser nachverfolgten Metriken. Um eine Metrik als Ziel hinzuzufügen, klicken Sie <b>[!UICONTROL Goal]</b> neben dem Metriknamen. (Nur [!UICONTROL Custom Bidding]) Um eine Metrik hinzuzufügen, die die zugewiesenen Zielmetriken unterstützt, klicken Sie <b>[!UICONTROL Assist]</b> neben dem Namen der Metrik.<br><br><b>Anmerkungen:</b> [!DNL Analytics] benutzerdefinierten Ereignisse folgen dieser Namenskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid.` [!DNL Analytics] Dimensionen und Segmente stehen für die Adobe Advertising-Optimierung nicht zur Verfügung.<br><br><b>Tipp:</b> Um die Leistung zu optimieren, müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens zehn Konversionen pro Tag umfassen. Ist dies nicht der Fall, empfiehlt es sich, dem Ziel zusätzliche unterstützende Konversionsmetriken hinzuzufügen, z. B. Produktseiten oder Programmstarts. Richtlinien finden [ unter „Best Practices zum Erstellen eines benutzerdefinierten ](#custom-goal-best-practices)&quot;. |
|  | Selected Metrics | Der Name jeder im Ziel enthaltenen Konversionsmetrik. Führen Sie einen der folgenden Schritte aus:<ul><li>Um eine Metrik als Ziel hinzuzufügen, klicken Sie in der Spalte [!UICONTROL Available Metrics] auf <b>[!UICONTROL Goal]</b> neben dem Metriknamen.</li><li>(Nur [!UICONTROL Custom Bidding]) Um eine Metrik hinzuzufügen, die die zugewiesenen Zielmetriken unterstützt, klicken Sie in der Spalte [!UICONTROL Available Metrics] neben dem Metriknamen auf <b>[!UICONTROL Assist]</b> . Geben Sie dann die numerische Gewichtung der Metrik relativ zu anderen Metriken im Ziel ein. Die Gewichtung muss zwischen 0,001 und 1 liegen und kann Dezimalstellen enthalten. Die Standardgewichtung ist 1.</li><li>(Nur Strategie [!UICONTROL Custom Bidding]) Um die Gewichtung einer Hilfsmetrik zu bearbeiten, klicken Sie in das Feld und geben Sie die numerische Gewichtung der Metrik relativ zu anderen Metriken im Ziel ein. Die Gewichtung muss größer als null (0) sein und kann Dezimalstellen enthalten. Die Standardgewichtung ist 1.</li><li>Um eine Metrik aus dem Ziel zu entfernen, halten Sie den Cursor über den Namen der Metrik und klicken Sie auf **[!UICONTROL X]**./li></ul>**Hinweise:**<ul><li>Stellen Sie sicher, dass die verschiedenen Metriken und ihre Gewichtungen relativ sinnvoll sind. Sie können beispielsweise eine Zählung nicht direkt mit einem Dollarbetrag vergleichen.</li><li>Große relative Änderungen zwischen den Zielgewichtungen können zu temporärer Volatilität der Leistung führen, sodass die Leistung nach der Änderung überwacht wird.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Optimierungsziele und ihre Verwendung](/help/dsp/optimization/optimization-goals.md)
>* [Best Practices für benutzerdefinierte Ziele](/help/dsp/optimization/custom-goal.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Konversionen verwalten](/help/dsp/admin/conversion-metrics-manage.md)
