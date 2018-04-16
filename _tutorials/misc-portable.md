---
title: "Portable Xpiks"
topic: "miscellaneous"
order: 3
---

Some users in Windows might want to make Xpiks more portable by having same settings and FTP credentials saved next to application rather than in computer local files. Now this became possible as of Xpiks 1.5.1.

You can launch Xpiks in "portable" mode by adding `--portable` argument to it. The easiest way to do it is to create a shortcut in Windows and launch Xpiks via Shortcut. Here's how to do it.

### Step 1. Create a shortcut

Right-click "Xpiks.exe" and select "Create shortcut". It will create a shortcut file next to the application.

<p>
  <img alt="Create shortcut" src="{{site.url}}/images/tutorials/miscellaneous/create-shortcut.png" class="small-12 large-12" />
</p>

<br />

### Step 2. Add `--portable` to arguments

Right-click shortcut file in Explorer and click "Properties". Add "--portable" (without quotes) inside `Target` field (don't forget to have a space between "Xpiks.exe" and `--portable`).

<p>
  <img alt="Create shortcut" src="{{site.url}}/images/tutorials/miscellaneous/portable-option.png" class="small-12 large-12" />
</p>

<br />

### Step 3. Open Xpiks via shortcut

Double click shortcut file to open Xpiks. Now Xpiks will store settings in the same directory where it is "installed". You will see a new directory called "settings".

<p>
  <img alt="Portable settings" src="{{site.url}}/images/tutorials/miscellaneous/settings-dir.png" class="small-12 large-12" />
</p>

<br />

Now every time you open Xpiks via this shortcut it will use settings from "settings" directory.
