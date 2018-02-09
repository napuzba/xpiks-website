---
title: "Diagnostic logs"
topic: "miscellaneous"
order: 1
---

Bugs are inevitable for applications of any size. Exactly for this reason most of them write "diagnostic logs" in order to investigate issues after they happen (postmortem analysis). Xpiks is no different in this regard and it also creates such logs.

Every user of Xpiks can also see them

![Logs menu]({{ "/images/tutorials/miscellaneous/show-logs.png" | absolute_url }})
*Logs are available from the _Tools -> Advanced_ menu*

You will see many colorful lines of text of different components which report their state inside Xpiks (interface, actions, backups, upload and many many others)

![Logs dialog]({{ "/images/tutorials/miscellaneous/logs-dialog.png" | absolute_url }})
*Logs dialog*

**Usually there's only one reason to open this dialog** - if you need to attach the logs along with the [report through Xpiks Support]({{site.url}}/2015/09/03/how-to-report-an-error/). Then you can click _Reveal logfile_ button (see image above) and find the file you need.
