<!-- Filename: Source_Data / Display title: Source Data -->

## Methods of Use

You need to think carefully about how you intend to use Jdocmanual. The
alternatives:

* Download source data updates From GitHub from time with no personal editing
of the source data. You can download with Git or using a ZIP file.
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
format (GFM) in four GitHub repositories. Ancillary data used for importing the
data into Jdocmanual are stored in txt or ini files. The first level structure
of each repository is like this:

```
cefjdemos-data-jdm-help
    /articles
    /images
    /LICENCE
    /README.md
```

## Jdocmanual and Local Site Structue

The local cloned repositories need to be in a folder named `manuals` and with
the short name of the repository, as follows:

```
/manuals
    /developer
    /docs
        /articles
            /de
            /en
                /jdoc-documentation
                /jdoc-help
                /jdoc-reference
                /jdoc-translation
                /jdocmanual
                    changelog.md
                    edit-article-in-jdocmanual.md
                    edit-in-vscode.md
                    ...
                    source-data.md
                menu-headings.ini
            ...
            /ru
            articles-index.txt
            menu-index.txt
        /images
            /en
                /jdocmanual
                    jdocmanual-article-edit.png
                    ...
                    jdocmanual.png
    /help
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

## Image Sizes

During the article build process, each original image leads to the creation of
six additional images at resolutions of 320, 768 and 1200 pixels wide in png or
jpg format, depending on the original, and webp format. The image links in the
markdown files are replaced with picture tags that allow the browser to
select the image most appropriate for the device resolution and capabilities.
Original screenshots should be saved in png format.

## Local Location of Sources

Each of the developer, documenter, help and user folders is a separate
repository. The manuals folder must be somewhere in your file space but not in
your web tree. For example `/home/username/data/manuals`.

The data originally came from the Joomla Documentation MediaWiki site. The
conversion process was rather tortuous and not so easily repeated! An important
feature of the conversion is that many of the links to article images, mostly
Joomla screenshots, have been retained in the article files. So Jdocmanual is
using images delivered from docs.joomla.org. In due course that may change.

## Data Management

This is a complex problem! You may have set up Jdocmanual on a personal
development server using localhost. Or you may be using a shared hosting
server with no command line access or a VPS with full server access. Also,
you may or may not be familiar with `git` and working with others to
maintain a Git repository.

Jdocmanual has an internal editing system that allows you to modify your
sources, perhaps with the help of others. However, that may put you out of
sync with the GitHub repo. For the moment let us assume you just want to
obtain the original source data and update your local copy from time to
time. The original sources on GitHub are in the following repositories:

- https://github.com/ceford/cefjdemos-data-jdm-developer
- https://github.com/ceford/cefjdemos-data-jdm-docs
- https://github.com/ceford/cefjdemos-data-jdm-help
- https://github.com/ceford/cefjdemos-data-jdm-user

### Clone with git

If you can install git on your computer, do so. It is free, fast and useful.
If not, go on to the next Download ZIP section. If you visit any of
the data sources listed above you will see a green button labelled `Code`.
From the dropdown list select the `Clone using the web URL.` copy symbol.

In a terminal window, change to your manuals folder and use the git clone
command. That will create a folder named `cefjdemos-data-jdm-docs`. You need
to rename that folder to its short name, `docs`.  For example:
```bash
cd /home/username/data/manuals
git clone https://github.com/ceford/cefjdemos-data-jdm-docs.git
mv cefjdemos-data-jdm-docs docs
```
To update your local repo at any time in the future you can change into
that folder and issue a git command:
```bash
cd /home/username/data/manuals/docs
git pull
```
Then build your articles and menus again.

### Download ZIP

If you don't have git, quite likely on shared hosting, you can download a
ZIP file from that green button on GitHub. Save the ZIP in your `manuals`
folder and unzip it there. It will have a long filename, such as
`cefjdemos-data-jdm-docs` that you need to rename to its short form, `docs`.
Then delete the ZIP file. You can download a new ZIP file from time to time
and unpack it in the same way to keep your data up to data with the original
repository. Then build your articles and menus again.

**Warning:** If you make changes with the Jdocmanual editor tools they will
be overwritten by the new download.

## Using the CLI

Jdocmanual has a command line interface to allow automation of update tasks.
For example, to update the user Manual you could issues the following commands:
```bash
cd /home/username/data/manuals/user
git pull
cd /path/to/joomla/root/cli
php joomla.php jdocmanual:action buildarticles user all
php joomla.php jdocmanual:action buildmenus user all
```
You could call these commands from a shell script and use a cron job to update
your site, perhaps once a week or once a day. If using shell script you need
to use the full path to the php executable because the command line version
of php may differ from that used by your web server.
