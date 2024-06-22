<!-- Filename: JDOC:Image_naming_guidelines / Display title: Image naming guidelines -->

The image naming guidelines are to give documentation contributors a set
guidelines about naming an uploaded image file *not used* by Joomla
[Help screens](https://docs.joomla.org/Help_screens "Help screens").

These guidelines are not absolute but for informative purposes. They
should only be used as a reference for helping contributors form a good
image file name.

Naming an image for use in Joomla documentation is not difficult once
you understand how the images are processed and stored. Some of the
benefits of Mediawiki's method of image storage are an

- image history,
- extra image data,
- and easy image updating.

## Naming an Uploaded Image

The Mediawiki software allows uploaded images to be named by [2
methods](https://docs.joomla.org/JHelp:Image_uploading "JHelp:Image uploading").

### Uploading an image directly

Image is not referenced in a page but will be used. The default name of
the image will be the "local" (name in your file system) but it may be
changed before the actual upload.

### Clicking on a red link

Image is referenced in a page already with an image link such as

<img src="https://docs.joomla.org/images/f/fb/Name_of_the_image-en.png"
class="thumbborder" decoding="async" data-file-width="252"
data-file-height="56" width="252" height="56"
alt="Name of the image-en.png" />

Of the two methods, the later method is the easiest method to use.

## Naming Pattern Suggestions

Image names should consist of an underscore or hyphenated separated list
of descriptive words. Think of them as a summary description of the
image.

### Suggested Formats For Joomla Images

It would be very beneficial if the first part of any Joomla image refers
to it's version. This allows someone to instantly know what version of
Joomla is connected to the image. Example: `j3x`. There is no need to
insert the .(dot) in the version, please omit it.

```text
<jver>-<admin>-<view>.<extension('png' | 'jpg' | 'jpeg' | 'gif')>
``````

#### Joomla Image Examples

A screenshot of Joomla 3.x administrator's view of the article manager
could be written as:

```text
j3x_admin_content_article_manager_articles.png
```

A screenshot of Joomla 3.x site's (frontend) view of the log in module
could be written as:

```text
j3x_site_protostar_log_in_module.png
```

### Suggested Formats For non-Joomla Images

Common sense and a descriptive summary should be the guide for
non-Joomla images. Again, use the underscore \_ or hyphen - to separate
the summary. For images of people, please use the person's name. For
images of software or website's, please include them within reason.

#### Non-Joomla Image Examples

GitHub pull request, the Firefox Firebug tool, or these other examples
could be written as:

```text
    github-pull-request-how-to.png
    eclipse_indigo_interface_egit_browsing_veiw.png
    joomla-event-Nov-2013-John-Smith.png
    firefox_addon_firebug_colour_picker.png
```

They are short, descriptive and inform the viewer looking at the image
call what the image is quickly.

## Localisation of Image Names

In preparation for documentation localisation, how to address images of
different languages needs to be addressed. As documentation becomes
localised, it is necessary to let user's and the Documentation Working
Group identify images in another language quickly. Please do not use a
native language as a file name description. Instead, add a trailing
two-letter language code to the end of your file description before you
upload the image in the 'base' language description.

Translators of Joomla! Documentation should read: [Localising
Images](https://docs.joomla.org/JDOC:Localising_Images "Special:MyLanguage/JDOC:Localising Images").
Translators will find detailed information about translating images.
Here is the base examples:

```text
    <jver>-<admin>-<view>-<language code>.<extension('png' | 'jpg' | 'jpeg' | 'gif')>
```
Taking some of the examples from above:

```text
    j3x_admin_content_article_manager_articles_es.png
```

A screenshot of Joomla 3.x site's (frontend) view of the log in module
could be written as:

```text
    j3x_site_protostar_log_in_module_fr.png
```
