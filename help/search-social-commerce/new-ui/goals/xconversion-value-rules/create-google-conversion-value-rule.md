---
title: Erstellen  [!DNL Google Ads]  Konversionswertregel
description: Erfahren Sie, wie Sie  [!DNL Google Ads] -/Konversionswertregeln erstellen.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Erstellen einer [!DNL Google Ads] Konversionswertregel

Sie können Konversionswertregeln auf Konto- und Kampagnenebene in [!DNL Google Ads] Konten erstellen, für die Konversionen auf individueller Kontoebene oder darunter verfolgt werden. Sie können keine Regeln für Konten mit kontoübergreifenden Konversionen erstellen, die auf Master-Kontoebene verfolgt werden.

Jede Regel umfasst bis zu zwei Bedingungen sowie die Konversionswertanpassung, die angewendet werden soll, wenn die Bedingungen erfüllt sind. Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten.

Für jede Kampagne können mehrere Regeln auf Kampagnenebene erstellt werden. [!DNL Google Ads] bietet jedoch noch nicht die Möglichkeit, neue Regeln auf Kontoebene außerhalb des [!DNL Google Ads]-Editors zu erstellen, wenn bereits eine Regel auf Kontoebene vorhanden ist. Um zusätzliche Regeln auf Kontoebene zu erstellen, melden Sie sich direkt bei [!DNL Google Ads] an und verwenden Sie den [!DNL Google Ads].

**Hinweis** Konversionswertregeln auf Kampagnenebene überschreiben die Regeln auf Kontoebene, und auf eine Konversion kann nur eine Regel angewendet werden. Weitere Informationen finden Sie unter [wie [!DNL Google Ads] bestimmt, welche Regel auf eine Konversion angewendet wird, wenn die Konversion die Bedingungen für mehrere Regeln erfüllt](https://support.google.com/google-ads/answer/10520348).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Standardmäßig ist die Registerkarte **[!UICONTROL Campaign]** ausgewählt, um alle Regeln auf Kampagnenebene anzuzeigen.

1. (Optional) Um stattdessen eine Regel auf Kontoebene zu erstellen, klicken Sie auf die Registerkarte **[!UICONTROL Account]** .

1. Klicken Sie in der Symbolleiste auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").<!-- Upload newer icon -->

1. Wählen Sie das Werbenetzwerk und das Konto aus. Wählen Sie für Regeln auf Kampagnenebene auch die Kampagne aus. Klicken Sie dann auf **[!UICONTROL Next]**.

1. Konfigurieren Sie [Einstellungen für Konversionsregeln](google-conversion-value-rule-settings.md).

   Sie müssen eine primäre Bedingung und eine Wertanpassung konfigurieren. Sie können optional eine sekundäre Bedingung konfigurieren.

   Innerhalb einer Bedingung werden mehrere Ziele oder Ausschlüsse mit dem booleschen Operator ODER verbunden, sodass jede Option zum Initiieren einer Wertanpassung erfüllt sein kann. Wenn Sie eine sekundäre Bedingung einbeziehen, wird die sekundäre Bedingung mit dem booleschen Operator ALL mit der primären Bedingung verbunden, sodass beide Bedingungen erfüllt sein müssen, um eine Wertanpassung zu initiieren. Beispiel: Wenn \[Standort Algerien ODER Tunesien\] UND \[Gerät ist Mobil ODER Tablet\] ist, fügen Sie 1.5 hinzu.

   **Hinweis:** Alle Regeln in einem Konto müssen denselben Typ von primären und (optionalen) sekundären Bedingungen verwenden. Wenn beispielsweise Regel 1 die primäre Bedingung „Zielgruppe“ und die sekundäre Bedingung „Standort“ enthält, müssen alle anderen Regeln im Konto die primäre Bedingung „Zielgruppe“ aufweisen. Wenn die anderen Regeln eine sekundäre Bedingung enthalten, muss sie „Standort“ lauten.

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über [!DNL Google Ads] Konversionswertregeln](about-google-conversion-value-rules.md)
>* [Bearbeiten  [!DNL Google Ads]  Konversionswertregel](edit-google-conversion-value-rule.md)
>* [Ändern des Status  [!DNL Google Ads]  Konversionswertregel](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] Regeleinstellungen für Konversionswerte](google-conversion-value-rule-settings.md)

