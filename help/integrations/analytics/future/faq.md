---
title: FAQs
description: xxx
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Häufig gestellte Fragen xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214
Standardmäßig meldet Adobe Analytics alle erfassten Ereignisse in jedem Bericht. &quot;[!UICONTROL Unspecified]&quot;-Ereignisse stellen Formularfertigungs-Ereignisse dar, die nicht mit Adobe Advertising verbunden waren. Im Bericht &quot;Anzeigenplattform&quot;würden organische Konversionen oder Konversionen, die von einer E-Mail-Kampagne gesteuert werden, beispielsweise in &quot;nicht angegeben&quot;fallen.

Sie können den Filter verwenden, um nicht angegebene Ereignisse aus Berichten zu entfernen, indem Sie das Häkchen mit der Option &quot;Nicht angegeben einschließen (keine)&quot;entfernen. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323
Platzieren Sie Analytics-Ereignis-Tags an denselben Stellen wie die Ad Cloud-Pixel, um sicherzustellen, dass die XXX übereinstimmen.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

F: Während unserer internen Sicherheitsprüfung wurden bestimmte Funktionen als Sicherheitsbedenken gekennzeichnet, die wir aktiviert haben, als wir Ad Cloud in unsere bestehende Adobe Analytics-Installation integriert haben.

Die fragliche Integration erfolgt zwischen AdCloud und Adobe Audience Manager. Diese Funktion erhöht die Übereinstimmungsrate für die Besucher-ID zwischen AdCloud und Adobe Audience Manager. Dazu sendet er Netzwerkanfragen an pagead.l.doubleclick.net, star-mini.c10r.facebook.com und pug88000nf.pubmatic.com, um zu ermitteln, ob diese Dienste über eine vorhandene ID für den Besucher verfügen, die genutzt werden kann. Dies sind die Netzwerkanfragen, die als Sicherheitsrisiko gekennzeichnet wurden und für alle Site-Besucher auftreten.

Unser Prüfer bittet uns, diese Funktion zu deaktivieren. Was passiert, wenn wir diese Netzwerkanfragen blockieren?

A: Wir haben mit unserem Produkt geprüft und darauf hingewiesen, dass die betreffenden Pixel dazu dienen, die Cookie-Übereinstimmungsraten zwischen Ad Cloud, bestimmten Bestandspartnern/SSP (in Bezug auf DSP) und AAM zu erhöhen.  Wenn sie entfernt werden, kann der Kunde eine verringerte Übereinstimmungsrate zwischen AAC/AAM und den Inventarpartnern sehen, für die die entsprechenden Pixel bestimmt sind, aber er würde nicht erwarten, dass sie wesentlich sind.

Bei der Ad Cloud-Suche sehen wir, dass die Experience Cloud-Organisations-ID des Advertisers für Mathworks eingerichtet ist. Unser Produktteam sieht jedoch keine Mathworks-Einrichtung, um Zielgruppen in Ad Cloud zu aktivieren. Verwenden Sie Adobe Audience Manager zum Senden von Zielgruppen an die Ad Cloud-Suche? Andernfalls hat das Entfernen dieser Fehler keine Auswirkungen auf den aktuellen Workflow. AAM Kundenunterstützung kann beim Entfernen dieser Pixel helfen, wenn Sie nicht möchten, dass sie ausgelöst werden.

