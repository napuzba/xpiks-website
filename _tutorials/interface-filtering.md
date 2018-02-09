---
title: "Filtering"
topic: "interface"
order: 6
---

List of artworks in the <a href="{{site.url}}/tutorials/interface-mainview/">main view</a> can get really large if you add many directories. That's why Xpiks supports filtering them so you can see only part of all items.

### Directories filtering

First and simpliest filtering you can apply is _directory filtering_. You can just click on a directory name in _Files and Folders_ tab and Xpiks will show artworks only from that directory. Multiselect is also supported.

<p>
  <img alt="Directories filter" src="{{site.url}}/images/posts/xpiks-15-overview/directories-filter.gif" class="small-12 large-12" />
</p>

<br />

### Artworks filtering

#### Common

What is more important you can search or filter through all opened artworks.

<p>
  <img alt="Artworks filter" src="{{site.url}}/images/tutorials/interface/filter-whereis.gif" class="small-12 large-12" />
</p>

<br />

Xpiks will try to find matches of what you entered in this field in every artwork and fitler out artworks which don't have matches. And how to match what you have typed in there is controlled in Settings:

<p>
  <img alt="Search settings" src="{{site.url}}/images/tutorials/interface/settings-search.png" class="small-12 large-12" />
</p>

<br />

If you check _[Search match all terms]_ and you will enter few words inside search field, Xpiks will look for matches of *all* words in every artwork's metadata. If this is unchecked, Xpiks will look for *any* match in metadata.

_[Search by path]_ option allows you also to match filepath of each artwork to what you have typed in the search field.

#### Special

Except ordinary search through artworks Xpiks supports different special terms.

Usually Xpiks searches for case-insensitive matches. But if you enter "!" (exclamation mark) before a word, Xpiks will look for *exact* match of this word _in Keywords_.

<p>
  <img alt="Search settings" src="{{site.url}}/images/tutorials/interface/exact-search.gif" class="small-12 large-12" />
</p>

<br />

Also you can type in **special keywords** inside Search field. Those special keywords are `x:empty`, `x:modified`, `x:selected`, `x:vector` and `x:image`.

For example, if you enter `x:empty` Xpiks will show you artworks which don't have any metadata filled in or if you enter `x:modified` Xpiks will show you artworks which are modified but not saved.

<p>
  <img alt="Search modified" src="{{site.url}}/images/tutorials/interface/search-xmodified.gif" class="small-12 large-12" />
</p>

<br />
