---
layout: post
title: Adding more bibles to 精读圣经
date: 2024-12-11T00:35:00.000Z
---
精读圣经 is a great bible reading tool that provides many functionality, like multiple bible translations, commentary, etc. But it doesn't provide a very extensive list of bible translations, such as NIV english or dutch versions.

This tutorial will teach you how to add your preferred bible versions to 精读圣经 and possibly other content like commentary.

## Installing 精读圣经

If you don't have 精读圣经 yet, you can download it here: <https://a1189.icu/>.

## Adding bible versions[](https://a1189.icu/)

精读圣经 uses SQLite .db database files to store the bible translations, this means that as long as you have a .db file of the bible version you want, it can be added to 精读圣经.

> Currently this tutorial is meant for Android only! If I figure out a way to do so for iOS, I will add it to this page

First you need to download the .db file of the bible you want to add to 精读圣经, preferably do this directly on your (Android) phone. I will provide the link to some of the db files that work already for me and that I have already manually converted:

* [NIV](https://andreahu3299.github.io/public/NIV11.db) (English New International Version)
* [DUTSV](https://andreahu3299.github.io/public/dutsv.db) (Dutch Statenvertaling)

Then you need to move the .db bible files to the bibles folder inside the 精读圣经 storage folder, which in most cases is

`Internal storage/Android/data/com.cz.bible2/files/精读圣经/bibles`

If you can't find this folder, you can always open the 精读圣经 app and in the settings page it will tell you where the storage location is under the text 储存位置. The /bibles folder should already contain other .db bibles translations that have been downloaded via the app itself.

Once you have moved the .db file in here, you'll need to restart the app for it to load it in. So close the app completely via the app drawer and reopen it. If everything worked well, you should be able to add your new translation via the .

## I want more versions!

If the above list doesn't contain the bible version that you want to use, then please reach out to me for the specific translation you want. Then if possible, I'll make a 精读圣经 compatible .db file of it available for download.
