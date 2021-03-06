---
layout: post
title: "Shutterstock changes vector upload rules"
date: 2019-07-13T14:45:21-08:00
---

<p>
  <img alt="Adobe" src='{{< misc/rel "/images/posts/vector-rules/adobe-photoshop-data-desk-693892.jpg" >}}' class="small-12 large-12" />
</p>

Vector illustrations submission process to microstocks is usually different than for photos. Majority of the microstock websites like Shutterstock, Depositphotos, Adobe Stock and others required to submit vector files (EPS or AI) together with preview (JPG) for that vector. If you wanted to get your metadata (like keywords, description) automatically read by the microstock website you had to embed it into the preview. From now on, this is not the case for Shutterstock.

New rules deprecate use of the preview so you only need to submit a vector file (EPS or AI). Shutterstock will accept vector files up to 100 MB and bounding box restrictions from 4 to 25 MP. They will generate a preview on their own and they will attempt to read metadata from the vector.

Many contributors expressed their dislike of the new rules in the [Shutterstock forum thread](https://forums.submit.shutterstock.com/topic/96928-shutterstock-has-made-uploading-vectors-easier-than-ever/). Main concerns are the quality of the autogenerated preview and 100MB size restrictions. Apparently it is quite difficult to create a 4MP (minimum) bounding box and fit into less than 100MB of the total filesize. To address these concerns Shutterstock created a [how-to](https://www.shutterstock.com/contributorsupport/articles/en_US/kbat02/Best-Practice-Recommendations-for-Saving-EPS-Files?l=en_US) for saving EPS files so they would fit the requirements.

Another important aspect of uploading only vector files is metadata embedding. Previously you could embed EXIF, IPTC or XMP metadata to preview and it will be auto-attached to the vector file. From now on it will not be so simple. You can only attach IPTC and XMP metadata to EPS files of version 10 and above. EPS 8 does not allow metadata embedding.

Fortunately since release 1.5.3 [Xpiks supports direct metadata embedding]({% post_url 2019-06-20-xpiks-153-release %}) to vectors so you can upload them same way as before. If you will add vector with preview to Xpiks, it will embed metadata both to vector and to preview so your uploads will work both with microstocks that require a preview pair and ones that don't.

Many believe Shutterstock made this change because of the constant issues with pairing vectors and previews in their previous system. Many contributors reported that when uploading vector and preview Shutterstock will fail to process them as vector-preview pair and will only show preview as a photo upload. Other microstock websites like Adobe Stock or Depositphotos solve this problem by requiring vector and preview be archieved together. It is not clear why Shutterstock did not go this way (it's way easier than to generate previews on their own) but now it is reasonable to expect other microstock to follow Shutterstock approach.
