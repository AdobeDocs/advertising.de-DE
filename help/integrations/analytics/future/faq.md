---
title: Häufig gestellte Fragen
description: xxx
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Häufig gestellte Fragen xxx

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/14214
Standardmäßig meldet Adobe Analytics alle erfassten Ereignisse in jedem Bericht. &quot;[!UICONTROL Unspecified]&quot;-Ereignisse stellen Formularabschlussereignisse dar, die nicht mit dem Adobe Advertising verbunden waren. Im Bericht der Anzeigenplattform würden beispielsweise organische Konversionen oder Konversionen, die von einer E-Mail-Kampagne gesteuert werden, in „Nicht angegeben“ fallen.

Sie können den Filter verwenden, um nicht angegebene Ereignisse aus Berichten zu entfernen, indem Sie das Häkchen der Option „Nicht angegebene Ereignisse einschließen (keine)“ entfernen. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/24323
Positionieren Sie Analytics-Ereignis-Tags an denselben Stellen wie die Ad Cloud-Pixel, um sicherzustellen, dass XXX übereinstimmen.

## Anrede

https://adobeadcloud.zendesk.com/agent/tickets/24323

F.: Bei der internen Sicherheitsüberprüfung wurden bestimmte Funktionen als Sicherheitsbedenken gekennzeichnet, die wir bei der Integration von Ad Cloud in unsere bestehende Adobe Analytics-Installation aktiviert hatten.

Die fragliche Integration erfolgt zwischen AdCloud und Adobe Audience Manager. Diese Funktion erhöht die Übereinstimmungsrate für die Besucher-ID zwischen AdCloud und Adobe Audience Manager. Dazu sendet sie Netzwerkanfragen an pagead.l.doubleclick.net, star-mini.c10r.facebook.com und pug88000nf.pubmatic.com, um festzustellen, ob diese Services über eine vorhandene ID für den Besucher verfügen, die genutzt werden kann. Dies sind die Netzwerkanfragen, die als Sicherheitsrisiko gekennzeichnet wurden und für alle Site-Besucher auftreten.

Unser Prüfer bittet uns, diese Funktion zu deaktivieren. Was passiert, wenn wir diese Netzwerkanfragen blockieren?

A: Wir haben mit unserem Produkt geprüft und erwähnt, dass die betreffenden Pixel dazu dienen, die Cookie-Übereinstimmungsraten zwischen Ad Cloud, bestimmten Inventar-/SSP-Partnern (in Bezug auf DSP) und AAM zu erhöhen.  Wenn sie entfernt werden, sieht der Kunde möglicherweise eine verringerte Übereinstimmungsrate zwischen AAC/AAM und den Inventarpartnern, für die die entsprechenden Pixel vorgesehen sind, erwartet jedoch nicht, dass sie erheblich ist.

Für Ad Cloud Search wird zwar die Experience Cloud-Organisations-ID des Werbetreibenden für MathWorks eingerichtet, aber unser Produktteam sieht MathWorks-Setup nicht, um Zielgruppen in Ad Cloud zu aktivieren. Verwenden Sie Adobe Audience Manager zum Senden von Zielgruppen an die Ad Cloud-Suche? Andernfalls hat das Entfernen dieser Elemente keine Auswirkungen auf den aktuellen Workflow. Die AAM-Kundenunterstützung kann beim Entfernen dieser Pixel helfen, wenn Sie nicht möchten, dass sie ausgelöst werden.

