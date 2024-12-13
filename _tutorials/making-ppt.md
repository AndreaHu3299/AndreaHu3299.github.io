---
layout: post
title: Making PPT with standard notation
date: 2024-12-11T00:35:00.000Z
---

- [1. Prerequisites](#1-prerequisites)
- [2. Why we're doing this](#2-why-were-doing-this)
- [3. Overview](#3-overview)
- [4. Find suitable standard notation score of the song](#4-find-suitable-standard-notation-score-of-the-song)
  - [4.1. Possible scenarios](#41-possible-scenarios)
- [5. Score recognition and clean up](#5-score-recognition-and-clean-up)
  - [5.1. Possible scenarios](#51-possible-scenarios)
- [6. Adding lyrics](#6-adding-lyrics)
- [7. Prettyfying the score](#7-prettyfying-the-score)
  - [7.1. Possible cases:](#71-possible-cases)
- [8. Save and export](#8-save-and-export)
- [9. Inverting png colors](#9-inverting-png-colors)
- [10. Done!](#10-done)


## 1. Prerequisites

Please download and install these before proceeding:

- [Audiveris](https://github.com/Audiveris/audiveris/releases)
- [Musescore 4](https://musescore.org/en/download)
  - [Custom lilyrics plugin](https://andreahu3299.github.io/public/Lilyrics-custom.zip).
  - Plugin installation instructions [here](https://musescore.org/en/handbook/4/plugins#manage). You can skip to point 4.
  - Make sure you enable the plugin once it's installed. See [here](https://musescore.org/en/handbook/4/plugins#enable-disable).
- (Optional) Photo editing software (just to do invert the colors from black to white). This can be achieved using Windows' or macOS's own photo viewing app, but you can use tools like photoshop or GIMP (free) if you prefer.

## 2. Why we're doing this

Before we start, it's good to know what we're dealing with and why we are doing this.

As a church we had a need to add standard notation to our Powerpoint presentation of the worship songs we were singing so that the congregation could sing it regardless of being familiar with the songs or not.
So we initially took scores found online and cropped it and aligned it above our lyrics in Powerpoint, but this didn't look nice and the scores usually broke up the lyrics sentence, so it would make following along the score a bit unnatural and distracting.

For this reason we sought a way to make pretty and readable lyrics with score in our presentations. Which is what this tutorial will be teaching you.

## 3. Overview

The idea is to end up with transparent images (.png images) of the lyric and standard notation above it so that they can be directly added to a powerpoint without further editing or alignment.

To do so we first need the standard notation melody of the song, so that we can then add the lyrics to it. Luckily, you can find the standard notation scores of most worship songs online and all we need to do is to convert into a digital format that we can edit and add lyrics to.

This is where the **Audiveris** app comes in, it is a free OMR [(Optical Music Recognition)](https://en.wikipedia.org/wiki/Optical_music_recognition) software that can recognise images of scores, tweak them (if the recognition isn't perfect) and convert them into a MusicXML (.mxl) file so that we can use **Musescore 4** to add lyrics to it. Obviously these two aren't the only tools that can do what they do, but because we're using them for church and not commercial purpose, they were the best free ones that met our needs. You can substitute these software with other ones of your preference.

## 4. Find suitable standard notation score of the song

To make the process of recognising the score smoother, it is important that we start with a good initial score image. For this you can search the title of your worship song online (e.g. Google) followed by 歌谱 or 五线谱 or score and choose one that meets the most of these criteria:

 * Prefer single melody instead of multi-voice (else you'll have to remove the other voices, thus more work).
 * Prefer high resolution (else Audiveris might not recognise it at all, though some lower resolution scores can still work well if the lines and notes are clear).
 * Prefer not photographed or scanned images, these make it harder for Audiveris to recognise (best are the computer generated scores).
 * Prefer dark colors and solid notes (if the lines are greyish and fuzzy, they will also make it harder for Audiveris).
 * Prefer horizontally aligned score lines (else you'll need to align them manually).

### 4.1. Possible scenarios

* If the image is not really straight
  * use your image editing tool of choice to rotate it so that all the horizontal lines are horizontally straigh (you can use the ruler tool to make it easier how much to rotate to).
* If the image is grayish
  * use your image editing tool of choice to increase the contrast or even better, to move the blacks (left bar) of the image histogram to the right until most grey pixels look black.

## 5. Score recognition and clean up

After you have chosen an image best matches the previous criteria, you can load it in Audiveris or drag it onto an open Audiveris window.

1. Open the score image into Audiveris.
2. Convert the score by pressing the "Transcribe the whole book" button
3. Fix wrong recognitions (See possible scenarios)
4. Remove all extra symbols/wrongly interpreted symbols
5. Save .omr and export to .mxl

### 5.1. Possible scenarios
* Missing lines
* 

## 6. Adding lyrics

Open .mxl in musescore 4 and save right away to .mscz
5. Fix measure lines so that they concide with singing lines
  1. Load in custom style
  2. If the song repeats multiple times, the entire score has to be copied multiple times over new pages.

## 7. Prettyfying the score

Paste in lyrics using the lilypond lyrics plugin
  1. Take lyrics and paste them in the `lyrics` field of the space adder tool. Then click `Run` and you should have the spaced out version of the lyrics, which is a good starting point for the lyrics plugin.
  2. Add `_` after characters that span two or more notes. Note: legato/tie notes of the same pitch don't need this.
  3. Tips: you can keep the lyrics popup open and make fixes and paste as you go. But the score should be fixed already.
  4. At the end when everything looks aligned, copy the final lyrics and save it somewhere // TODO
  5. Adjust text size if too big, always stay between 20 to 24. Prefer bigger, but has to be readable.
   6.
### 7.1. Possible cases:
  1. levando where the measure only has one beat or less than the defined time signature. Right click on measure and open measure properties. Then reduce the amount of beats to what is needed.

## 8. Save and export
  1. Save the musescore projet as a .mscz file.
  2. Export the scores as png
    1. Only export "Final" part, choose `PNG` export format and click export. Make sure the transparent background option is enabled (it should be by default).
    2. This will generate a png for each page of the score. Save it with the name of the song, if there are multiple pages, Musescore will save it as multiple pngs with a -n appended at the end.

## 9. Inverting png colors
Because the exported pngs from Musescore are black, we need to inver the color so that they become white and stand out on our PPT background.
  1. Open your photo editing software of preference or the online tool, then upload the images and invert the colors. This will make the blacks into whites.

## 10. Done!
Now you have all the pngs that can be dragged into the presentation directly and resized to the width of the slide.
