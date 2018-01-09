---
layout: post
title: "How to report a bug"
date: 2015-09-03T00:45:01+02:00
---

In case you had bad user experience with Xpiks (crash, failure, unexpected behavior) you can report it and it will be fixed as soon as possible taking into account it's severity.

To report a bug, please do the following steps:

<h3>1. Open <a href="{{ site.url }}/support/">Support page</a>, post a new topic there</h3>

<h3>2. Describe what do you observe and why it's a bug</h3>

Please take care to describe not only what is not working but also why do you think it's a bug. _Screenshots_ and any other information about what have you done before is very helpful.

<h3>3. Attach diagnostic logs</h3>

Xpiks logs diagnostic information while it works so this information can help later to fix an issue if there will be any. This information usually is crucial to include when you report a bug. Please find these diagnostic logs and attach them. 

In order to find the logs through Xpiks, go to _Tools -> Advanced -> Show logs_. 

<p>
  <img alt="Show logs" src="{{site.url}}/images/posts/show-logs-menu.png" class="small-12 large-12" />
</p>

There you can click **Reveal logfile**. This will open logs directory in the file manager (e.g. Finder or Explorer) and select logfile from the current session in Xpiks.

<p>
  <img alt="Reveal logfile" src="{{site.url}}/images/posts/reveal-logs.png" class="small-12 large-12" />
</p>

If it was _past session_ when you experienced problems then select _other file_ than is currently selected. Each logfile has a date and a time in the name of file so it helps to select a logfile from the session when you experienced issues with Xpiks. It might help to sort files by date. _If you're not sure which logs to choose, get few of them._

<p>
  <img alt="Select logfile" src="{{site.url}}/images/posts/select-logfile.png" class="small-12 large-12" />
</p>

If you cannot open logs location from Xpiks, you can find the on disk in one of the following locations:

- on Windows they should be at `%AppData%/Roaming/Xpiks/` directory
- on OS X they should be at `~/Library/Application Support/Xpiks/` directory
- on Linux they should be at `~/.local/share/xpiks/` directory

In case you're a developer and you have technical information about the issue, you're welcome to create a ticket at <a href="https://github.com/Ribtoks/xpiks/issues">Github Issues</a>.
