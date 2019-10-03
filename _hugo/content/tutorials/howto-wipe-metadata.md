---
title: "Wipe all metadata"
topic: "howto"
order: 2
---

Xpiks can help you in clearing literally ALL metadata which is contained in files. For example, for photos such metadata could be tags, date, geolocation, camera model information, lens ets.

If you would be using <a href="https://sno.phy.queensu.ca/~phil/exiftool/">exiftool</a> to do the job, this would be equal to a command `exiftool -all= myphoto.jpg`.

With Xpiks it's possible to do it for multiple files at once. This is desturctive operation with almost no way to restore, so Xpiks will ask you not once but twice to confirm.

<p>
  <img alt="Wipe all metadata" src='{{< misc/rel "/images/tutorials/howto/wipe-metadata.gif" >}}' class="small-12 large-12" />
</p>

<br />

Also Xpiks does not clear your edits inside the app. That means that while actual files do not contain any metadata anymore, _Title_, _Description_ and _Keywords_ inside Xpiks will be left inact so you will be able to save them later.

