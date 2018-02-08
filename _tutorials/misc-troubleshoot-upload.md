---
title: "Troubleshoot upload"
topic: "miscellaneous"
order: 2
---

Quality of FTP upload in Xpiks depends very much not only on well-tested Xpiks code, but also on your local internet provider, microstocks websites which update and break their services frequently and many other fragile things. In case you have any connectivity issues it is important to detect where does the error originate: locally or on the FTP server side.

Xpiks allows you to better understand what is going on with detailed upload logging. You can turn it on in _Upload_ section of _Settings_. Please keep in mind that **enabling detailed logging makes your upload slower** so please don't forget to **turn it off after** the experiment.

<p>
  <img alt="Upload settings" src="{{site.url}}/images/tutorials/miscellaneous/upload-settings.png" class="small-12 large-12" />
</p>

<br />

Usually you would need to do the following:

* turn on _Detailed logging_ for uploading
* try to upload some files (this will generate enough logs to troubleshoot networking)
* turn off _Detailed logging_ for uploading

Later in order to understand what happens, you can open <a href="{{site.url}}/tutorials/misc-diagnostic-logs/">diagnostic logs</a>, but it is better to <a href="{{site.url}}/2015/09/03/how-to-report-an-error/">submit a support ticket</a> and get help from professional.

Please keep in mind that Xpiks strips all sensitive data like passwords from detailed FTP logging. Read more about <a href="{{site.url}}/2016/01/13/ftp-and-security/">FTP security in blog</a>.
