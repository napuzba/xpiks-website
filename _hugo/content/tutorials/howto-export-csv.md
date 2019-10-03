---
title: "Export CSV"
topic: "howto"
order: 3
---

You can export artworks' metadata to a <a href="https://en.wikipedia.org/wiki/Comma-separated_values">CSV file</a> with Xpiks. Mostly this is required for uploading video files to microstocks but you may also use it to send metadata to another person or for backup.

This functionality is available from main menu _Edit -> Selected artworks -> Export to CSV_ as well as from the actions toolbar in the <a href='{{< misc/rel "/tutorials/interface-mainview/" >}}'>main window</a>.

<p>
  <img alt="CSV export" src='{{< misc/rel "/images/tutorials/howto/basic-csv-scheme.gif" >}}' class="small-12 large-12" />
</p>

<br />

CSV scheme is a list of column names and values that will be written there when the export will actually happen. Look at this example:

<p>
  <img alt="CSV export example" src='{{< misc/rel "/images/tutorials/howto/csv-scheme-xpiks.png" >}}' class="small-12 large-12" />
</p>

<br />

Here we instruct Xpiks to export 4 files' metadata to CSV with 3 columns:

* column "My Filename" and value _Filename_ (e.g. actual name of the artwork file) written into that column
* column "My Description" and _Description_ of each artwork written there
* column "My Keywords" and _Keywords_ of each artwork written there

You can check the result of the export in Finder:

<p>
  <img alt="CSV export result" src='{{< misc/rel "/images/tutorials/howto/numbers-csv-result.png" >}}' class="small-12 large-12" />
</p>

<br />

As you can see, 4 files are exported to CSV with each column having previously defined values.

If you need Xpiks to create a column with no value inside (for you to fill it in later) you can select _Empty_ property for export scheme. Xpiks will create a column and leave value empty for each artwork you will export.

<p>
  <img alt="CSV custom column" src='{{< misc/rel "/images/tutorials/howto/csv-custom-field.png" >}}' class="small-12 large-12" />
</p>

<br />

### Video upload

Keep in mind that you have to use property **[UploadFilename]** instead of [Filename] for video files upload and CSV generation. Some microstocks have issues with filenames that contain spaces or special characters. During upload Xpiks normalizes the filename (replaces special characters) so you will upload without troubles. But since the uploaded filename will be different, you will need to use same names in CSV in order for it to be accepted.
