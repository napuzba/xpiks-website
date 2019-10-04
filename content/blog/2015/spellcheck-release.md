---
layout: post
title: "Second stable release of Xpiks is out!"
date: 2015-12-19T20:55:24+02:00
---

Today I announce release of Xpiks 1.1! Main two features of this release are spell checking and speed improvements. So now you can check spelling in description, title and keywords using en_US dictionary available from LibreOffice suite. Also Xpiks will suggest you corrections for words with bad spelling. What about speed is that I optimized visual and loading parts so now Xpiks should work faster with large collections of artworks! Also I've implemented a lot of small requests from actual users.

As usual, small changelog:

**Major features** of this release:

- Automatic spell checking and suggestion for all metadata
- Automatic checking for updates
- Added plain text mode for keywords editing
- Speed improvements with large collections
- Editing of separate keywords
- Improvements for UI of some popups on large monitors
- Improvements on keywords pasting
- Exact search terms parsing (with exclamation mark before word like "!man")

Also, a lot of small UI issues and glitches were fixed!

Known issues:

- Xpiks proposes spell suggestions for all words with errors, what creates duplicates if one word has been used several times in metadata (keywords, title, description)
- On systems with two monitors menu with recent directories opens on another monitor (it's QT issue fixed in QT 5.6)
