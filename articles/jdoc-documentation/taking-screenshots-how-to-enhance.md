<!-- Filename: Taking_Screenshots_%E2%80%93_How_To_Enhance / Display title: Taking Screenshots - How to Enhance -->

## How to take screenshots

A screenshot can be taken very easily in current operating systems using
the system's own tools. In most cases, all you need to do is press the
"PrintScreen" key on the keyboard (if available) to save the entire
screen. Additional keys such as "Alt" or "Ctrl" may be used to define
partial areas.

Careful post-processing is needed to produce high-quality images. The
sample images in this tutorial were prepared with
<a href="https://www.gimp.org" class="external text" target="_blank"
rel="nofollow noreferrer noopener">GIMP</a> Version 2.10.24, an open
source image editor.

## Five easy steps to get high quality screenshots

The choice of which tool to use for the following steps is mainly up to
the JDoc author. Care should be taken to ensure that the application has
the functions/features as described below.

Moreover, it is **important** to proceed through the processing steps
described here in sequence.

1.  Take/Load image
2.  Crop image (if necessary)
3.  Scale image (if necessary)
4.  Apply Filter: Unsharp Mask (essential)
5.  Saving as PNG (recommended)

## Taking a screenshot

For Windows and MacOS, in addition to the system tools, there are a lot
of extra tools promising to make taking screenshots more convenient than
it is possible with the system tools. However, the quality of the raw
screenshot data with these tools is not any better than with the system
tools. The handling of the system tools is explained on the pages for <a
href="https://support.microsoft.com/en-us/windows/use-snipping-tool-to-capture-screenshots-00246869-1843-655f-f220-97299b865f6b"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">Windows</a> and
<a href="https://support.apple.com/en-us/HT201361" class="external text"
target="_blank" rel="nofollow noreferrer noopener">MacOS</a>. For Linux,
there are numerous free tools that can capture screenshots. Ask your
favourite search engine with the terms "screen capture tool linux" to
find an app of your choice, suitable for your distribution.

The chosen tool should be able to capture any part of the screen and
have a screen magnifier for an accurate selection. Any application that
can transfer the screenshot to the clipboard or save it in PNG format is
also preferable. The widely used image format JPG or JPEG is less
suitable because their data compression is not lossless.

In the Joomla! documentation (and the JHelp pages), four image widths
are common.

- **800px** for the overview at the top of the page
- **600px** for larger sections (e.g. various tabs)
- **400px** for general subareas
- **265px** for smaller subareas or details

However, it is **not a good idea** to reduce the screenshot exactly to
the required page width after loading the image. Experience has shown
that a 25% larger image width is recommended (800px → 1000px). Smaller
deviations are insignificant. Files that are too large do not bring
better quality, they only eat up storage space.

Care must be taken to ensure that the screenshot made (after cropping)
has at least one of the desired image widths (+25%) as mentioned above.

**Warning**: It is absolutely necessary to avoid enlarging a screenshot
that is too small using the scaling function. This will result in a loss
of quality that cannot be fixed. The Adobe Photoshop documentation says
succinctly:

*For best results when you produce a smaller image, downsample and apply
the Unsharp Mask filter. To produce a larger image, rescan the image at
a higher resolution.*

If you have already defined the precise image area when taking the
screenshot, you can skip the next step.

## Cropping the Image

If the captured image is larger than necessary it should be cropped
after loading it into an image editing tool.

**Tip:** If the created screenshots are temporarily stored in the
clipboard and further editing is to be done with Gimp, the following
shortcut "Shift+Ctrl+V" (or "Cmd+V" with macOS) helps to import the data
into Gimp immediately.

### Using the Crop Tool

If the screenshot still contains superfluous border areas, the image
should first be cropped to the desired image section using the crop
function. When choosing the final cropping area, it is a poorer choice
if the boundary is a white area. Then the viewer cannot see the edges of
the picture against the white background of the side. In professional
image editing, we like to avoid such a situation and either place a
slight shadow under the image or give the image area a minimal colour
tone.

<img
src="https://docs.joomla.org/images/thumb/8/80/Tutorial_Screenshots_Crop_Tool.png/400px-Tutorial_Screenshots_Crop_Tool.png"
decoding="async"
srcset="https://docs.joomla.org/images/8/80/Tutorial_Screenshots_Crop_Tool.png 1.5x"
data-file-width="518" data-file-height="418" width="400" height="323"
alt="Gimp Crop Tool" />

To open the Crop Tool, click the icon with the mouse pointer.

<img
src="https://docs.joomla.org/images/thumb/5/57/Tutorial_Screenshots_Crop_Tool_selection.png/800px-Tutorial_Screenshots_Crop_Tool_selection.png"
decoding="async"
srcset="https://docs.joomla.org/images/5/57/Tutorial_Screenshots_Crop_Tool_selection.png 1.5x"
data-file-width="1158" data-file-height="259" width="800" height="179"
alt="Gimp Crop Tool Selection" />

Move the mouse pointer to a corner or to a side line. By keeping the
left mouse button pressed, the selection area can be changed.
<a href="https://docs.gimp.org/2.10/en/gimp-tool-crop.html"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">The Gimp Online Manual</a> gives a
full description on how to use up the option.

<img
src="https://docs.joomla.org/images/thumb/9/94/Tutorial_Screenshots_Crop_Tool_selection2.png/400px-Tutorial_Screenshots_Crop_Tool_selection2.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/9/94/Tutorial_Screenshots_Crop_Tool_selection2.png/600px-Tutorial_Screenshots_Crop_Tool_selection2.png 1.5x, https://docs.joomla.org/images/9/94/Tutorial_Screenshots_Crop_Tool_selection2.png 2x"
data-file-width="712" data-file-height="430" width="400" height="242"
alt="Gimp Crop Tool Selection Detail" />

**Tip:** If the screen view is enlarged (here 800%) the selection can be
fixed with pixel accuracy.

## Scaling the Image

This step is only needed if the screenshot is much too large (i.e. more
than 25-30% above the nominally required width).

A small example should explain the reason:  
Let's assume we need an image that is 800px wide and 1000px high on our
page. The uncompressed colour file (3 channels RGB, 8-bit each) is about
2.29 MB. If we use the slightly larger file (1000px x 1250px) for
quality reasons, the file size increases to 3.58 MB. But if we take a
screenshot in double width and height (1600px x 2000px), the file size
grows to an incredible 9.16 MB. Even at the highest compression level,
this file will be displayed noticeably slower on the web.

### Using the Scale Image Option

<img
src="https://docs.joomla.org/images/thumb/9/92/Tutorial_Screenshots_Scale_Image.png/363px-Tutorial_Screenshots_Scale_Image.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/9/92/Tutorial_Screenshots_Scale_Image.png/544px-Tutorial_Screenshots_Scale_Image.png 1.5x, https://docs.joomla.org/images/9/92/Tutorial_Screenshots_Scale_Image.png 2x"
data-file-width="580" data-file-height="480" width="363" height="300"
alt="Gimp open Scale Image" />   <img
src="https://docs.joomla.org/images/thumb/f/f6/Tutorial_Screenshots_Scale_Image_Set.png/356px-Tutorial_Screenshots_Scale_Image_Set.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/f/f6/Tutorial_Screenshots_Scale_Image_Set.png/534px-Tutorial_Screenshots_Scale_Image_Set.png 1.5x, https://docs.joomla.org/images/f/f6/Tutorial_Screenshots_Scale_Image_Set.png 2x"
data-file-width="581" data-file-height="490" width="356" height="300"
alt="Gimp Scale Image Setting" />

To open the image scale option, click on **Image → Scale Image** in the
menu. Do **not use** the Scale Icon in the Toolbox.

The "Scale Image" dialogue in the right-hand image allows the size of an
image to be changed. The new width is set in the Width field. As long as
the chain icon is not deactivated, the appropriate height is calculated
automatically. The setting for quality should be kept unchanged.
<a href="https://docs.gimp.org/2.10/en/gimp-image-scale.html"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">The Gimp Online Manual</a> gives a
full description on how to use up the option.

## Applying Filters: Unsharp Mask

This is the most tricky step. It requires careful adjustment, which may
vary slightly depending on the motif, monitor, operating system and
browser. With the help of the example pictures below, however, you can
quickly find the optimal setting for your own system.

### How to access

- Select **Filters **→** Enhance **→** Sharpen (Unsharp Mask)** to open
  the filter settings dialogue.

Three parameters are adjusted, of which only one should really be varied
after the basic configuration. However, it is easy to exaggerate the
filter effect and then destroy the quality. The "Threshold" slider must
only have a higher value than "0" in special cases. The "Radius" control
must be operated very sensitively, and "Amount" is often in the right
place in a mid-position.

<img
src="https://docs.joomla.org/images/thumb/4/41/Tutorial_Screenshots_unsharp_mask_setting.png/800px-Tutorial_Screenshots_unsharp_mask_setting.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/4/41/Tutorial_Screenshots_unsharp_mask_setting.png/1200px-Tutorial_Screenshots_unsharp_mask_setting.png 1.5x, https://docs.joomla.org/images/4/41/Tutorial_Screenshots_unsharp_mask_setting.png 2x"
data-file-width="1406" data-file-height="740" width="800" height="421"
alt="Gimp settings Unsharp Mask" />

The image above shows the optimal settings (with Gimp 2.10.24) on this
system for this screenshot. In a different environment and with other
screenshots, the optimal values will differ slightly.
<a href="https://docs.gimp.org/2.10/en/gimp-filter-unsharp-mask.html"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">The Gimp Online Manual</a> gives a
full description on how to set up the filter.

**Tip:** Have you noticed the yellow marked area? Click on the **+**
button (right-hand side) to save the current settings with your
individual name.

**Tip:** An image can always be best analysed in the 100% view (see the
status bar in the above illustration, at the bottom of the figure).

**Note:** Other image editors partly use very different names for the
sliders. The values are also defined quite differently. Which slider
leads to which result - only a look in the corresponding manual will
help.

**The following image samples are intended to demonstrate the effect of
a bad setting with regard to the image display. Check the colour coded
parts of the images to see the effect of the different filter
settings.** The evaluation is made easier if the images are viewed in
their original size (by clicking the figure).

<img
src="https://docs.joomla.org/images/thumb/9/9b/Tutorial_Screenshots_unsharp_mask_demo1.png/597px-Tutorial_Screenshots_unsharp_mask_demo1.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/9/9b/Tutorial_Screenshots_unsharp_mask_demo1.png/896px-Tutorial_Screenshots_unsharp_mask_demo1.png 1.5x, https://docs.joomla.org/images/thumb/9/9b/Tutorial_Screenshots_unsharp_mask_demo1.png/1194px-Tutorial_Screenshots_unsharp_mask_demo1.png 2x"
data-file-width="1867" data-file-height="544" width="597" height="174"
alt="Tutorial Screenshots unsharp mask demo1.png" />

**Left:** The raw data file  
**Right:** The settings shown above were used.

<img
src="https://docs.joomla.org/images/thumb/5/5a/Tutorial_Screenshots_unsharp_mask_demo2.png/900px-Tutorial_Screenshots_unsharp_mask_demo2.png"
decoding="async"
srcset="https://docs.joomla.org/images/thumb/5/5a/Tutorial_Screenshots_unsharp_mask_demo2.png/1350px-Tutorial_Screenshots_unsharp_mask_demo2.png 1.5x, https://docs.joomla.org/images/thumb/5/5a/Tutorial_Screenshots_unsharp_mask_demo2.png/1800px-Tutorial_Screenshots_unsharp_mask_demo2.png 2x"
data-file-width="2808" data-file-height="544" width="900" height="174"
alt="Tutorial Screenshots unsharp mask demo2.png" />

**Left:** The "Threshold" slider is increased too much - causes light
parts of the image (green marking) not to be processed.  
**Middle:** The "Amount" slider is too high - this creates a clearly
visible outline around the font (red and magenta marking).  
**Right:** The "Radius" slider is set too high - this creates a
so-called "black eye" effect (magenta marking).

## Saving the Image

It sounds obvious, but is often ignored:

- Better image quality is often only possible with larger files.
- Large files demand more bandwidth to load quickly and consume valuable
  disk space.

Therefore, it is important to find the best possible compromise between
these two requirements. An important factor influencing the size of the
file is the number of pixels an image contains and has already been
mentioned above. The raw version of image files can quickly exceed 10
MB. Therefore, it is necessary to compress the data when saving. **The
PNG format compresses loss-free.** It is the first choice for the
application needed here.

**Tip:** There is a special procedure with Gimp when files are to be
saved after editing. The usual way to save a file in PNG format with
"Save" or "Save as" does not allow any other image format than XCF.
However, Gimp has implemented a very elegant way via "Export as". The
big advantage with this way is that the edits are not saved in the
original raw file, but only in the export file. See the <a
href="https://docs.gimp.org/2.10/en/gimp-images-out.html#save-export-image"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">Gimp Online Manual</a> for details.

## Related Information

For more detailed information on special cases, see the [Taking
Screenshots
FAQ](https://docs.joomla.org/JDOC:Taking_Screenshots_FAQ "Special:MyLanguage/JDOC:Taking Screenshots FAQ"),
(currently under construction).

[Image naming
guidelines](https://docs.joomla.org/JDOC:Image_naming_guidelines "Special:MyLanguage/JDOC:Image naming guidelines")

[Localising
Images](https://docs.joomla.org/JDOC:Localising_Images "Special:MyLanguage/JDOC:Localising Images")
