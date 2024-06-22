<!-- Filename: How_to_take_Screenshots_for_Joomla_Documentation / Display title: How to take Screenshots for Joomla Documentation -->

## Introduction

If you are writing documentation for Joomla! you will need to take
screen shots to illustrate the features you are attempting to explain.
Indeed, there is a good chance you have already captured some screens
and you are looking for specifications or advice. This tutorial covers
some tools, procedures and recommendations that you can adapt for your
own platform and experience. As ever, *there’s more than one way to skin
a cat*.

There are plenty of tools available to capture a screen and for
processing the captured images. This tutorial is based on the Firefox
browser for most screen capture and GIMP for image processing. GIMP is
also needed for capturing dynamic screen elements that cannot be
captured with Firefox, for example the screen capture dialogue itself.
They are both free and cross-platform (Windows, Mac and Linux). If you
want to use something else just look for tools with similar
functionality. Installation is not covered here: there is a good chance
you will know how to do that.

Keep in mind there are two distinct types of Joomla! documentation:

- **Tutorials** occupy the width of a browser window, limited by the
  max-width style, but full screen images are typically displayed at 800
  pixels in width.
- **Help Screens** are displayed in an iframe 700 pixels wide so the
  displayed image is a little smaller to allow for some padding.

### CSS pixels versus display pixels

In the above statements the width in pixels means the width as used in
CSS. Some display screens use one display pixel per CSS pixel but others
use more. Macintosh Retina screens use 2 so the ratio is 2x. Other
devices use different ratios with 1.3x, 1.5x, 2.0x and 3.0x being
common. The default is 1.0x.

**Why this matters:** if an image is available in multiple sizes
declared in a srcSet then the client will download the most appropriate
version for its display resolution, giving a better image in the same
space. For example, if an image is 800 CSS pixels wide then a client
with a 2x screen resolution will download the 1600 pixel wide version of
the image if it is available or, if not available, the largest image
less than 1600 pixels wide. A client with a 1x screen resolution will
download the 800 pixel wide version.

## Capture

### Firefox

Right click on the screen you wish to capture and select the **Take
Screenshot** item from the popup-menu.

<img
src="https://docs.joomla.org/images/8/8c/Taking-screenshots-firefox-popupmenu-en.png"
decoding="async" data-file-width="243" data-file-height="253"
width="243" height="253" alt="Firefox Screenshot popup menu" />

That produces an overlay dialog that allows selection of the whole
screen, **or** the whole page including any portions above and below the
visible part, **or** individual block elements such as div, h and p,
**or** a user defined area. Just move the **+** pointer around and see
how the potential selection changes.

Here is an example where the filter bar of the Articles page has been
selected:

<img
src="https://docs.joomla.org/images/thumb/a/a4/Taking-screenshots-firefox-screenshot-dialog-en.png/800px-Taking-screenshots-firefox-screenshot-dialog-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/a/a4/Taking-screenshots-firefox-screenshot-dialog-en.png 1.5x"
data-file-width="1000" data-file-height="567" width="800" height="454"
alt="Firefox Screenshot dialog" />

You can adjust the size of the selected area by dragging the corner or
side marker bubbles. To select the whole visible screen select the
**Save visible** box at the top right of the screen.

Select the **Copy** button to copy the selected image to the clipboard.
It is then a simple matter to switch to GIMP and use Edit -\> Paste as
-\> New Image for the next stage of processing.

### Google Chrome

A not so friendly sequence of keyboard commands:

1.  In Google Chrome press Ctrl + Shift + I if you're on a PC, or
    Command + Option + I if you're on a Mac.
2.  Next, press Ctrl + Shift P if you're on a PC, or Command + Shift P
    on a Mac.
3.  Type Screenshot to see the four available options. Select the one
    you want and press enter.

You will be prompted to save the screenshot file.

There are several screenshot extensions for Chrome that are more
convenient. Search for one that suits you.

### Mac Safari

Press and hold these keys together: Shift, Command, 3 to take a full
screen or Shift, Command, 4 to define an area to capture. In the latter
case the pointer changes to a camera icon which can be dragged to define
the area to capture. The screenshot is saved to the desktop. More
information:
<a href="https://support.apple.com/en-us/HT201361" class="external free"
target="_blank"
rel="nofollow noreferrer noopener">https://support.apple.com/en-us/HT201361</a>

## Crop

If you have saved your screenshot to a file you need to open it in GIMP.
If it has been copied to the clipboard use **Edit -\> Paste as -\> New
Image**. Remember that full screen screenshots do not need to be
cropped.

To select an area to illustrate some feature in the documentation select
the **Crop** tool. Then click and drag to define the area of interest.
The area can be adjusted with the side and corner grab handles, which
are marked as boxes. It can also be refined with the **Tool Options** to
specify exact size and position. The Auto Shrink button can be used to
trim excess background colour.

The following example shows an Edit drop-down list selected in the open
state for documentation:

<img
src="https://docs.joomla.org/images/thumb/0/05/Taking-screenshots-gimp-crop-en.png/800px-Taking-screenshots-gimp-crop-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/0/05/Taking-screenshots-gimp-crop-en.png 1.5x"
data-file-width="1000" data-file-height="660" width="800" height="528"
alt="GIMP Crop Tool" />

## The Joomla Document Server

Before scaling your image to an optimum size for storage and
transmission you should know how the Joomla Document Server handles your
image on upload. Suppose you upload an image that is 2880 pixels wide:
the Server will store that image and create smaller versions at 800, 320
and 120 pixels wide for use by the Server image management screen. When
a link is created to use that image at 800 CSS pixels wide the server
will create two additional versions at 1200 and 1600 pixels wide for use
by client screens that have 1.5 and 2.0 screen pixels per CSS pixel. If
you create a link and specify a width of 600px then the Server will
create copies at 900 and 1200 pixels wide. These copies are permanently
stored.

In a document containing an image link the Server substitutes the link
text with an image srcSet link that looks like this:

This is actually for an original image saved at 1440 pixels wide so no
1600px wide version was created. The Server will never upsize an image.
The link gives the default image source as the 800 pixel wide version.
It also offers the 1200 pixel wide version for clients with 1.5 screen
pixels per CSS pixel and the original 1440 pixel wide image for clients
with a 2.0x ratio. The browser will accept the largest image it can use
and itself resize it to fit its allocated space. CSS styles tell the
browser to resize the image to the full width of its container or to the
maximum size of the image, whichever is smaller.

## Scale

Scaling an image amounts to a choice between display quality and
consumption of disk space and network bandwidth, even for images that
are to be displayed at 800 pixels wide. Here is a comparison of file
sizes for a Global Configuration screen captured at at 2880 pixels wide
and uploaded to the Document Server:

2880: 261Kb; 1600px: 205Kb; 1200px: 143Kb; 800px: 81Kb.

The 2880 pixel wide version will only ever be used if you forget to
include 800px in the image link. You will see that immediately and fix
it. The 800px wide version looks rather poor on 2x resolution screens.
Also, you may wish to expand the size of a page or Help screen to get a
better view. So you may upload a higher resolution: 1000, 1200 or even
1440 (174Kb) wide would all give a reasonable compromise between file
size and resource use. Anything larger would be a waste!

### Full Screen Images

Most of the images used in Help screens for Joomla! Version 3 are about
1000 pixels wide so you can scale full screen images to that width if
you wish.

The following illustration shows a screenshot of the Joomla! 4
Administrator Dashboard ready to be rescaled. Notice the original size
in GIMP title bar (2880x1482) and the scale dialog with width set to
1000. The aspect ratio is fixed so the height adjusts automatically.

<img
src="https://docs.joomla.org/images/thumb/1/1e/Taking-screenshots-gimp-scale-en.png/800px-Taking-screenshots-gimp-scale-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/1/1e/Taking-screenshots-gimp-scale-en.png 1.5x"
data-file-width="1000" data-file-height="677" width="800" height="542"
alt="GIMP Scale Dialog" />

The **Quality Interpolation** choice between **Linear**, **Cubic** and
**NoHalo** seems to make no material difference for Joomla! 4
Administrator screenshot images.

For comparison, here are the file sizes saved in png format at different
resolutions, width in pixels:

- 2880 - 252Kb
- 1000 - 99Kb
- 800 - 72Kb

### Part Screen Images

Some screens that need to be documented have excessive white space. For
example, the **Articles: Edit** screen **Options** tab has full width
drop-down lists and text entry boxes. In this case the browser window
can be narrowed until just before the form tabs turn into horizontal
bars. Taking the screenshot at this size and then scaling the final
image to 600px wide gives satisfactory results.

<img
src="https://docs.joomla.org/images/d/db/Taking-screenshots-article-edit-options.png"
decoding="async" data-file-width="600" data-file-height="476"
width="600" height="476" alt="The Article: Edit Options tab" />

Full screen images at 600 or 800 pixels wide only display general
layout. The text in menus and buttons is hard to read. So showing a
small area image at the CSS resolution gives better results. The
following image shows an area of interest scaled to the CSS resolution:

<img
src="https://docs.joomla.org/images/f/ff/Taking-screenshots-gimp-original-scale.png"
decoding="async" data-file-width="217" data-file-height="374"
width="217" height="374" alt="Small image at CSS resolution" />

Note that the width setting is not included in the image link.

**Tip:** If captured on a device with 2x resolution just divide the
captured width by 2.

## Enhance

### Sharpen

See <a
href="https://docs.joomla.org/Taking_Screenshots_%E2%80%93_How_To_Enhance"
class="external text" target="_blank" rel="noreferrer noopener">Taking
Screenshots - How To Enhance</a>

### Frame and Caption

If you wish to add some padding and a caption to an image you can do
this by including frame\|caption in the image link options. Example:

<img
src="https://docs.joomla.org/images/f/ff/Taking-screenshots-gimp-original-scale.png"
class="thumbimage" decoding="async" data-file-width="217"
data-file-height="374" width="217" height="374" /> Small image at
original scale

For more on how to do this, see
<a href="https://www.mediawiki.org/wiki/Help:Images"
class="external free" target="_blank"
rel="nofollow noreferrer noopener">https://www.mediawiki.org/wiki/Help:Images</a>

**Note:** The thumbinner style is missing from the Wiki style sheet. It
sets margins to auto and padding. This note to be removed on Wiki
upgrade.

## Save

Screenshot images of pages that do not contain photographs should be
saved in png format. If a screenshot contains one or more photographs it
may be saved in jpg format. You can save the image in each format and
then look at the file sizes and quality. If the image adequately
illustrates the point you wish to make then choose the smaller file.

In GIMP select **File -\> Export As** and then select a folder and
suitable filename to save the final image. You can use any name when
saving the image on your own computer. However, it is well to be aware
of the Joomla! image naming guidelines, which suggest:

--.

So for example the image file name used in the documentation could be:

j4x-admin-article-edit-cmscontent-dropdown-en.png

For more information, see [JDOC:Image naming
guidelines](https://docs.joomla.org/JDOC:Image_naming_guidelines "JDOC:Image naming guidelines").

The en part of the filename is for the original English version of the
screenshot. It allows a translator to substitute another language code
for a new version of the image in a different language.
