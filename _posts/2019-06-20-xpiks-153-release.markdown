---
layout: post
title: "Xpiks 1.5.3 released"
date: 2019-06-20T21:24:43-08:00
published: false
---

It is my pleasure to announce that Xpiks 1.5.3 has been released! It incorporates a year long of improvements, small features and bugfixes. While all efforts in the development were mostly concentrated around Xpiks 1.6 major release, some recent events forced release of a smaller update in 1.5 branch. Major one was that [Shutterstock changed vector upload requirements](https://forums.submit.shutterstock.com/topic/96928-shutterstock-has-made-uploading-vectors-easier-than-ever/) and others considerably smaller issues in Xpiks.

## Vectors

Major change in Xpiks 1.5.3 is full vector support without preview. Now you can open, add metadata and upload vectors without need to have a preview for it.

<p>
  <img alt="Vector" src="{{site.url}}/images/posts/xpiks-153-overview/vector.png" class="small-12 large-12" />
</p>

If Xpiks cannot find a preview, it will show artwork thumbnail as black. However, you still can add metadata to the vector and Xpiks will embed it into vector same way as it works with images. If you have vector+preview pair, Xpiks will write metadata to both of them so they will be accepted to other microstocks as before.

Also Xpiks now allows uploading vectors without previews (inside zip archives or standalone) which should allow to upload to Shutterstock and other stocks with similar requirements without issues.

## Preset groups

Since introduction of presets in Xpiks it became one of the users' favorite features. After introducing preset groups in version 1.5 Xpiks lacked one obvious feature: preset group management. This release adds such functionality.

<p>
  <img alt="Preset groups" src="{{site.url}}/images/posts/xpiks-153-overview/preset-groups.png" class="small-12 large-12" />
</p>

<br />

## Manage dictionaries

Also Xpiks has translation dictionaries support but before this release you could only add new dictionaries. Now you can also manage existing and add new from a separate dialog.

## Range selection

Small but so asked for improvement in Xpiks. Now you can select multiple images with `Shift + mouse click` in main window.

<p>
  <img alt="Multiselect" src="{{site.url}}/images/posts/xpiks-153-overview/multiselect.gif" class="small-12 large-12" />
</p>

<br />

## Keywords suggestion changes

Fotolia [has been acquired by Adobe Stock](https://blog.fotolia.com/us/2018/11/05/fotolia-members-welcome-to-adobe-stock/) and recently they discontinued different developer APIs that transitioned under Adobe. In this release Xpiks switches to Adobe Stock keywords suggestion and disables Fotolia.

Also iStock/Getty images discontinued API for developers so Xpiks will not provide keywords suggestion from iStock anymore.

## Combined editing

Combined editing is a fastrack that allows you to apply changes to multiple files at the same time. There's an important enchancement made to it in order to prevent accidental rewrites. Now if you combine several artworks that have different title and description, by default Xpiks will use [partial changes]({{site.url}}/tutorials/batch-partial/) to only append new keywords. Title and Description will be disabled.

<p>
  <img alt="Combined" src="{{site.url}}/images/posts/xpiks-153-overview/combined.png" class="small-12 large-12" />
</p>

<br />

## Smaller changes

* Shutterstock keywords suggestion now also includes editorial images
* Fixed issue in CSV format to be compatible with Shutterstock
* FTP upload speed improved
* Removed warnings about duplicates in Title and Description
* Fixed thumbnails loading from end in keywords suggestion
* Artwork navigation shortcuts changed in single editing view

## What's next

We will continue working on Xpiks 1.6 which will come with plugins support allowing extending Xpiks functionality and enabling other developers to create Xpiks extensions. Also implementing ever growing list of TODO items in Xpiks is a priority because of continuous user feedback from support channel and forums.

