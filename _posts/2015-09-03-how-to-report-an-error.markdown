---
layout: post
title: "How to report a bug"
date: 2015-09-03T00:45:01+02:00
---

In case you had bad user experience with Xpiks (crash, failure, unexpected behavior) you can report it and it will be fixed as soon as possible taking into account it's severity.

<br />

To report an error, please do the following steps:

<h3>1. Open <a href="{{ site.url }}/support/">Support page</a>, post a new topic there</h3>

<h3>2. Describe what do you observe and why it's a bug</h3>

Please take care to describe not only what is not working but also why do you think it's a bug. Screenshots and any other information about what have you done before is very helpful.

<h3>3. Attach diagnostic logs</h3>

This is very important for us to fix the issue. Please find the logs and attach them. In order to find the logs through Xpiks, go to _Tools -> Advanced -> Show logs_. There you can click **Reveal logfile**.

Please select correct logs and attach them to the topic in Support section.

If you cannot open logs location from Xpiks, you can find the on disk in one of the following locations:

- on Windows they should be at `C:/Users/USERNAME/AppData/Roaming/Xpiks/` directory
- on OS X they should be at `~/Library/Application Support/Xpiks/` directory
- on Linux they should be at `~/.local/share/xpiks/` directory

In case you're a developer and you have technical information about the issue, you're welcome to create a ticket at <a href="https://github.com/Ribtoks/xpiks/issues">Github Issues</a>.
