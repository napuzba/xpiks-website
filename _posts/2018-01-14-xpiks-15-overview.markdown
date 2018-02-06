---
layout: post
title: "Xpiks 1.5 overview"
date: 2018-01-14T21:01:10+02:00
---

I'm proud to announce Xpiks 1.5 release! This is a major release which took almost 10 month of development and testing. Mostly changes are focused on Video support and different improvements all over the app.

## Interface

Keeping in pace with <a href="{{site.url}}/2017/02/24/xpiks-14-detailed-features/">previous release</a> this one also brings many UI changes and improvements. Most notable ones are updated experience of <a href="{{site.url}}/tutorials/interface-mainview/">main actions</a>

<p>
  <img alt="Toolbar" src="{{site.url}}/images/tutorials/interface/mainview-toolbar.png" class="small-12 large-12" />
</p>

<br />

and improved experience with many dialogs with the lists

<p>
  <img alt="Upload view" src="{{site.url}}/images/tutorials/interface/upload.png" class="small-12 large-12" />
</p>

<br />

## Video

Yes, now you can edit and upload video files just as photos and vectors! You will see a small icon saying that it's video in the corner.

<p>
  <img alt="Video files support" src="{{site.url}}/images/posts/xpiks-15-overview/video-files.png" class="small-12 large-12" />
</p>

<br />

Although most microstocks do not read metadata from video files as of today, they will do that in not so distant future. Xpiks not only writes metadata to video files, but also it provides options to **export metadata CSV** (comma-separated values file) for microstocks which do not read it from video files. This functionality is available from main menu _Edit -> Selected artworks -> Export to CSV_ as well as from the actions toolbar in the main window.

<p>
  <img alt="CSV export" src="{{site.url}}/images/posts/xpiks-15-overview/csv-export.png" class="small-12 large-12" />
</p>

<br />

## Presets improvements

One of the huge improvements for presets is that now it's possible to categorize them to groups which will be visible in the context menu. You can read more about that in <a href="{{site.url}}/tutorials/presets-groups/">Preset Groups Tutorial</a>.

<p>
  <img alt="Presets groups" src="{{site.url}}/images/tutorials/presets/groups.gif" class="small-12 large-12" />
</p>

<br />

Also now you can autocomplete presets in keywords field when you type along with keywords or separately. You can read more about that in <a href="{{site.url}}/tutorials/presets-autocomplete/">Preset Autocomplete Tutorial</a>.

<br />

## Session management

Want to continue working where you left last time when you opened Xpiks? Now this is possible! Just turn it ON and Xpiks will reopen files that you worked with previously.

<p>
  <img alt="Session management" src="{{site.url}}/images/posts/xpiks-15-overview/session-restore.png" class="small-12 large-12" />
</p>

<br />

## Automatic import

Xpiks now also supports automatic import of metadata. So if you add files or folders, Xpiks imports metadata by default and you don't have to click "Import" each time. This is an experimental feature, but combined with session management it should really simplify work. If you don't want import to be automatic you can always turn it off in _Settings -> System -> Experimental settings_.

<br />

## Directories filtering

List of opened directories on the left has become more interactive now. You can easily filter files by clicking on the directory name. Multiselect is also available.

<p>
  <img alt="Directories filter" src="{{site.url}}/images/posts/xpiks-15-overview/directories-filter.gif" class="small-12 large-12" />
</p>

<br />

## Semantical duplicates

Some microstocks (like Shutterstock) usually cleanup your keywords in order to remove different duplicates like singular/plural forms of words. I'm happy to announce that Xpiks now is also capable of doing so! Though this is turned off by default, you can turn it on easily in the _Behavior_ tab in Settings. What is does is that it highlights duplicates as you type them in Title, Description and Keywords. You can read more in <a href="{{site.url}}/tutorials/keywords-duplicates">Duplicates section in Tutorials</a>.

<p>
  <img alt="Duplicates" src="{{site.url}}/images/posts/xpiks-15-overview/duplicates.png" class="small-12 large-12" />
</p>

<br />


## Translations

This release includes 4 new languages: _Hungarian_, _Indonesian_, _Polish_ and _Turkish_! Awesome people contributed to Xpiks translations at CrowdIn! So Xpiks is now available in 12 languages in total. <a href="https://crwd.in/xpiks">Click here</a> to translate Xpiks to Your language!

<p>
  <img alt="Translations" src="{{site.url}}/images/posts/xpiks-15-overview/translations.png" class="small-12 large-12" />
</p>

<br />

## Smaller improvements

Every release of Xpiks brings lots of smaller improvements and fixes which are usually not get highlighted in the reviews. But I decided to describe them as well because Xpiks 1.5 brings more of these than any release before.

#### Hotkeys to switch artwork in single editing mode

Now not only you can navigate through Title-Description-Keywords using keyboard, but also you can switch between artworks on bottom with keyboard only. Just press `Ctrl + Alt + Left/Right` (Cmd+Alt+Arrows on Mac) and you will go left or right.

#### Clearing ALL metadata from photos

Users have requested for Xpiks to be able to clear all metadata from photos and this feature got implemented in this release. Just go to _Tools -> Advanced -> Wipe all metadata from files_. Essentially this is equal to running Exiftool with `exiftool -all= foo.jpg`

#### Option to tweak upload priority for vectors

Some users have experienced problems with uploading vectors to Shutterstock when the metadata wasn't properly read from previews. But also some other users have found a workaround where they upload vectors first and only later previews and reportedly that made Shutterstock to read keywords correctly. This trick is available in Xpiks in _Advanced_ tab of Upload dialog where you can tick "Upload vectors before previews" checkbox.

#### Backups to single database

All previous versions of Xpiks have saved temporary backups in _.xpks_ files next to the artwork files. This version uses more "professional" approach and saves all backups in one database as you edit your files. Of course ultimately metadata is saved in images and videos, temporary backups are only for convenience. Also Xpiks removes old _.xpks_ files to cleanup after older versions.

#### Open all recent files

_Recent files_ menu got a small improvement: now you can open all recent files with one click. Also there's _Recent directories_ menu available.

#### Copy to QuickBuffer from keywords suggestion

Now you can copy artwork metadata to QuickBuffer straight from the Keywords Suggestion tool using right-click menu. This is useful if you would like to save Description, Title or Keywords of a specific artwork for later editing.
