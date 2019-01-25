---
layout: default
---

## Definition: Resolution etc

#### By [Andar](https://forums.rpgmakerweb.com/index.php?members/andar.11882/), 7 Aug 2015

<br/>
Since there is some confusion over terms in the current discussion about the feature preview of RMMV, I'll provide a bit of background into terms like Resolution, Screen Size and so on.

<br/>
Basically when talking about resolution in its technical definition, we're talking about values like 300 dpi - Dots Per Inch. That is what resolution really is.<br/>
Screen Size is usually meant as the pixels total on the screen - values like 800x600 or 1920x1080 are screen sizes.<br/>
And then there is the Monitor size - you know, the device on your desktop that you're looking at? That is usually measured in inches (or whatever value is used in your country.

So basically Screen Size (in pixels) divided by Monitor size (in inches) gets you the resolution (in pixels per inch, or more usually dots per inch).

<br/>
However, back in the old days (pre-Windows and the first window versions) there was not much choice in monitor dimensions - for technical and monetary reasons most people had the same size-monitors, usually 14" (rarely 15") simply because larger monitors were too expensive and smaller monitors a pain for the eyes.<br/>
At the same time, the available screen size as provided by the grafics cards went up fast - there was a time when eight colors (NOT 8 Bit colors =256 colors, but really eight colors) at 320x240 was state of the art and only months later a new grafics card could get you the increadibly screen size of 640x480...

But because the monitors didn't change, what changed was both the screen size and the resolution. And more and more often the users called the screen size the "resolution", until even technical people were forced to call it that to be understood.<br/>
That is how the names and numbers got confused originally.

However, the formula is still valid. Screen size divided by physical size is the resolution, and the physical size (while a lot more varied now depending on the device) is still a fixum - you don't exchange your monitors depending on what games you play, or do you?

So if you now watch an RM game in fullscreen, increasing the screen size will not only make the resolution higher, it will also make the tiles smaller - unless you also increase the tilesize.

If we use tiles as a calculation instead of pixels, that will still be the screen size. Both RMVXA and RMMV have default screen sizes of 17x13 tiles - which is the same on your monitor in full screen.<br/>
However, because VXA has 32x32 pixels per tile and MV has 48x48 pixels per tile, that same size on the physical monitor results in a higher resolution for MV. It now has 48 pixels per tile instead of 32 pixels per tile, allowing the artist to get more details into the tiles.

<br/>
This change from 32x32 to 48x48 is directly the higher resolution everyone wanted (even if some people confused it and wanted higher screen size). And it is also an absolute neccessity to allow for higher screen sizes, because with higher screen sizes (which are possible by plugin as Degica confirmed with testing of a 1920x1080-plugin) the events and sprites would otherwise get too small to be playable.

[back](./)
