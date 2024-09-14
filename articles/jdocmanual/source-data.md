<!-- Filename: Source_Data / Display title: Source Data -->

## Methods of Use

You need to think carefully about how you intend to use Jdocmanual. The
alternatives:

* Download source data updates From GitHub from time to time with no personal
editing of the source data. You can download with Git or using a ZIP file.
* Download updates with Git and resolve any conflicts with your own edits. For
this you can use a local clone of the original GitHub data sources.
* Download updates with Git and contribute your own edits to the original
source. For this you will need to fork the original sources on GitHub and
clone your fork locally. You will also need to create and checkout a Git branch
to use for a pull request later.

For the Jdocmanual site I use a local git clone of the GitHub repo, make any
changes using VSCodium or VScode and test locally on my laptop. I then push
the changes to the GitHub repository. On the Jdocmanual site I pull from
GitHub and rebuild the articles and menus.

Jdocmanual has an internal editing and revision control system and you may use
that if you wish.

## GitHub Storage Structure

The article data used by Jdocmanual are stored GitHub Flavoured Markdown
format (GFM) in GitHub repositories, one for each language in each manual.
Ancillary data used for importing the data into Jdocmanual are stored in
txt or ini files. The first level structure of each repository is like this:

```
cefjdemos-data-jdm-users-en
    /articles
    /images
    /LICENCE
    /README.md
```

The Manual is in the penultimate part of the name, users for the User manual in
the case illustrated above. The final part of the name is the language. The
en repository of each manual also contains two text files:

- **articles-index.txt** contains a list of articles in the manual.
- **menu-index.txt** contains the articles in menu order.

## Jdocmanual and Local Site Structue

The local cloned repositories need to be in a folder named `manuals` and with
the short name of the repository, as follows:

```
/manuals
    /developer
    /docs
    /help
        /en
            /articles
                /articles
                    list of articles in markdown format
                /banners
                    list of articles in markdown format
                ...
            /images
                /articles
                    list of images for articles in this section
                /banners
                    list of images for articles in this section
        /de
        ...
        /ru
    /user
```
The images folders are created as required for local images. The image names
should start with the folder they are in. Note that each cloned repository
folder contains a hidden `.git` folder for keeping track of changes using Git.

## Reason for Structure

This structure allows a local image in English (en), typically a screenshot,
to be shared by all translations. However, if a translation wishes to use a
screenshot in its language it is a simple matter to place a new screenshot
in the appropriate language folder and then change the language code part of
the image path, for example `en` to `de` for the German translation.

An automated script generates screenshots for the Help manual so they are
already available in each of its language repositories. Most original
screenshots are saved 1440 pixels wide in png format. A few are a little wider
to accommodate more columns in list views.

## Image Sizes

During the article build process, each original image leads to the creation of
six additional images at resolutions of 576, 768, 992 and 1200 pixels wide in
png or jpg format, depending on the original, and webp format. The image links
in the markdown files are replaced with picture tags that allow the browser to
select the image most appropriate for the device resolution and capabilities.

## Local Location of Sources

The manuals folder must be somewhere in your file space but not in
your web tree. For example `/home/username/data/manuals`.

The data originally came from the Joomla Documentation MediaWiki site. The
conversion process was rather tortuous and not so easily repeated! An important
feature of the conversion is that many of the links to article images, mostly
Joomla screenshots, have been retained in the article files. So Jdocmanual is
using images delivered from docs.joomla.org for Manuals other than the Help
Manual, which uses its own auto-generated images.

## Data Management

This is a complex problem! You may have set up Jdocmanual on a personal
development server using localhost. Or you may be using a shared hosting
server with no command line access or a VPS with full server access. Also,
you may or may not be familiar with `git` and working with others to
maintain a Git repository.

Jdocmanual has an internal editing system that allows you to modify your
sources, perhaps with the help of others. However, that may put you out of
sync with the GitHub repository. For the moment let us assume you just want to
obtain the original source data and update your local copy from time to
time. See the [Installation Notes](jdocmanual?article=docs/jdocmanual/installation-notes) page for more information.
