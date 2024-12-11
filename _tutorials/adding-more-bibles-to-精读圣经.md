---
layout: post
title: Adding more bibles to 精读圣经
date: 2024-12-11T00:35:00.000Z
---

- [Installing 精读圣经](#installing-精读圣经)
- [Adding bible versions](#adding-bible-versions)
- [Downloads](#downloads)
  - [Request for translations](#request-for-translations)

精读圣经 is a great bible reading tool that provides many functionality, like multiple bible translations, commentary, etc. But it doesn't provide a very extensive list of bible translations, such as NIV english or dutch versions.

This tutorial will teach you how to add your preferred bible versions to 精读圣经 and possibly other content like commentary.

## Installing 精读圣经

If you don't have 精读圣经 yet, you can download it here: <https://a1189.icu/>.

## Adding bible versions

精读圣经 uses SQLite .db database files to store the bible translations with a specific table structure and metadata structure. This means that as long as you have a .db file of the bible version you want, it can be added to 精读圣经, though it will most probably need some tweaking.

> Currently this tutorial is meant for Android only! If I figure out a way to do so for iOS, I will add it to this page
 
First you need to download the .db file of the bible you want to add to 精读圣经, preferably do this directly on your (Android) phone. In the [downloads](#downloads) section I have provided the .db files that I have already manually converted.

Then you need to move the .db bible files to the bibles folder inside the 精读圣经 storage folder, which in most cases is

`Internal storage/Android/data/com.cz.bible2/files/精读圣经/bibles`

If you can't find this folder, you can always open the 精读圣经 app and in the settings page it will tell you where the storage location is under the text 储存位置. The /bibles folder should already contain other .db bibles translations that have been downloaded via the app itself.

Once you have moved the .db file in here, you'll need to restart the app for it to load it in. So close the app completely via the app drawer and reopen it. If everything worked well, you should be able to see and add your new bible translation.

## Downloads
* English
  * [NIV](https://andreahu3299.github.io/public/NIV11.db) (New International Version)
* Dutch
  * [DUTSV](https://andreahu3299.github.io/public/dutsv.db) (Dutch Statenvertaling)

### Request for translations

If the above list doesn't contain the bible version that you want to use, then please reach out to me for the specific translation you want. Then if possible, I'll make a 精读圣经 compatible .db file of it available for download.