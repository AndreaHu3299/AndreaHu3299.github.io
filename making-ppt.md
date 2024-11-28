---
layout: page
title: Making PPT
---

Tools:

- [Audiveris](https://audiveris.github.io/audiveris/_pages/install/README/)
- [Musescore 4](https://musescore.org/en/download)
- Photo editing software (just to do invert action to turn black to white)

> ⚠️ **If you are using mobile browser**: Be very careful here!

1. Find suitable standard notation score of the song
   1. preferably single melody instead of multi-voice.
   2. Prefer high resolution.
   3. Prefer not scanned images (so best to be computer generated scores).
   4. Prefer dark colors and solid notes.
   5. Prefer horizontally aligned score lines.
2. Image preparation
   1. If the image is a bit rotated, use an image editing tool to rotate it back or use the
3. Open the score image into Audiveris.
4. Convert the score
   1. Fix missing notes or wrong note length/type.
   2. Remove all extra symbols/wrongly interpreted symbols
5. Save .omr and export to .mxl
6. Open .mxl in musescore 4 and save right away to .mscz
7. Fix measure lines so that they concide with singing lines
   1. Load in custom style
   2. If the song repeats multiple times, the entire score has to be copied multiple times over new pages.
8. Paste in lyrics using the lilypond lyrics plugin
   1. Take lyrics and paste them in the `lyrics` field of the space adder tool. Then click `Run` and you should have the spaced out version of the lyrics, which is a good starting point for the lyrics plugin.
   2. Add `_` after characters that span two or more notes. Note: legato/tie notes of the same pitch don't need this.
   3. Tips: you can keep the lyrics popup open and make fixes and paste as you go. But the score should be fixed already.
   4. At the end when everything looks aligned, copy the final lyrics and save it somewhere // TODO
   5. Adjust text size if too big, always stay between 20 to 24. Prefer bigger, but has to be readable.
   6.
9. Save .mscz and export
   1. Only export "Final" part, choose `PNG` export format and click export. Make sure the transparent background option is enabled.
   2. This will generate a png for each page of the score.
10. Invert the scores
    1. Open your photo editing software of preference or the online tool, then upload the images and invert the colors. This will make the blacks into whites.
11. Done!

12. Possible cases:
    1. levando where the measure only has one beat or less than the defined time signature. Right click on measure and open measure properties. Then reduce the amount of beats to what is needed.
