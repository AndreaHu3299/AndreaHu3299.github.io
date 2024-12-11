---
layout: post
title: Adding more bibles to 精读圣经
date: 2024-12-11T13:23:00.000Z
---
* [Installing 精读圣经](#installing-精读圣经)
* [Adding bible versions](#adding-bible-versions)

  * [Android](#android)
  * [iOS](#ios)
* [Downloads](#downloads)

  * [Request for translations](#request-for-translations)

精读圣经 is a great bible reading tool that provides many functionality, like multiple bible translations, commentary, etc. But it doesn't provide a very extensive list of bible translations, such as NIV english or dutch versions.

This tutorial will teach you how to add your preferred bible versions to 精读圣经 and possibly other content like commentary.

## Installing 精读圣经

If you don't have 精读圣经 yet, you can download it here: <https://a1189.icu/>.

## Adding bible versions

精读圣经 uses SQLite .db database files to store the bible translations with a specific table structure and metadata structure. This means that as long as you have a .db file of the bible version you want, it can be added to 精读圣经, though it will most probably need some tweaking.

### Android

Requirements:

* Internet connection
* Files app to move files in the phone

Steps:

1. Download the .db file of the bible you want to add to 精读圣经, preferably do this directly on your (Android) phone. In the [downloads](#downloads) section I have provided the .db files that I have already manually converted which are compatible with 精读圣经.
2. Move the .db file(s) to the /bibles folder inside the 精读圣经 storage folder, which in most cases is `Internal storage/Android/data/com.cz.bible2/files/精读圣经/bibles`

   * If you can't find this folder, you can always open the 精读圣经 app and in the settings page it will tell you where the storage location is under the text 储存位置. The /bibles folder should already contain other .db bibles translations that have been downloaded via the app itself.
3. Restart the app for the . So close the app completely via the app drawer and reopen it. If everything worked well, you should be able to see and add your new bible translation.

### iOS

Adding translations to iOS is a bit more involved as it is not possible to easily access the application's folders and files. But luckily the developers of 精读圣经 have though about this and provided a way to share files for 精读圣经 from one device to another. We will be leveraging this feature to add more translations.

Requirements:

* You'll need another Android phone which already has the translation you want. If you don't have this, ask for a friend with Android phone to help you with this.

Steps:

1. Make sure that both iOS and Android device are connected to the same network. You can:

   * Connect both to the same wifi network
   * Enable hotspot network on of the devices and have the other connect to it. The hotspot device doesn't need to open 3g/4g/5g for this to work.
2. On the iOS device

   * Open the 精读圣经 app, then press the top-left menu button, then `数据传输`.
   * At the bottom, enable the checkbox `接收数据` and keep 本机资源存在时 to `跳过`.
   * Press `开始服务`. This will start a server on the phone and allow it to receive files.
   * Most probably the text in the middle will show "检测到多个IP..." and a list of multiple IPs. Find the one that starts with `192.168`, we will use it in the next steps.
3. On the Android device

   * Open the 精读圣经 app, then press the top-left menu button, then `数据传输`.
   * At the top, press the tab for `客户端`.
   * Press and choose the `发送模式`
   * Type the IP address we found beforehand in the input box (e.g. `192.168.2.6`).
   * In the folder view below, open the folder `译本`, then tick all the translations that you want to transfer over.
   * Once ready, press `发送` and if all goes smoothly, the selected translations will be transferred over to the iOS device.
4. Restart the 精读圣经 app on iOS to see the new bible translations.

## Downloads

* English

  * [NIV](https://andreahu3299.github.io/public/NIV11.db) (New International Version)
* Dutch

  * [DUTSV](https://andreahu3299.github.io/public/dutsv.db) (Dutch Statenvertaling)

### Request for translations

If the above list doesn't contain the bible version that you want to use, then please reach out to me for the specific translation you want. Then if possible, I'll make a 精读圣经 compatible .db file of it available for download.
