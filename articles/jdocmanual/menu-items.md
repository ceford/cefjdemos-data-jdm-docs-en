<!-- Filename: Menu_Items / Display title: Menu Items -->

## Menu Structure

In Jdocmanual the menu structure is set by a file named `menu-index.txt` located in the root of the `manual-name/en` folder, for example `user/en/menu-index.txt`. The storage structure for markdown files is designed for simplicity in finding articles and has only one sub-folder level. The menu structure can be completely different. For example, the Joomla! Programmers Documentation menu is the same as that used for the [site generated using Docusaurus](https://manual.joomla.org).

Example extract:

```
heading=introduction=Introduction
docus=introduction=index.md
...
heading=get-started=Get Started
docus=get-started=index.md
docus=get-started=technical-requirements.md

heading-1=ide=IDE
docus=get-started=ide-index.md

heading-2=phpstorm=PhpStorm
docus=get-started=ide-phpstorm-index.md
docus=get-started=ide-phpstorm-debugging.md

close-1-headings
...
heading-2=js-library=Joomla JavaScript Library
docus=general-concepts=javascript-js-library-index.md
docus=general-concepts=javascript-js-library-core.md
docus=general-concepts=javascript-js-library-editors.md
docus=general-concepts=javascript-js-library-joomla-dialog.md
docus=general-concepts=javascript-js-library-modal-content-select.md

close-2-headings

docus=general-concepts=mail.md
docus=general-concepts=menus-menuitems.md
...
```

## Menu Headings

The English menu headings are taken either from the `heading=` line in the English `menu-index.txt` file or from another file named `menu-headings.ini` located in the `en/articles` folder. Each language has such a file to facilitate translation of headings, for example `user/de/articles/menu-headings.ini` contains the German translations of the English menu headings:

```ini
getting-started=Einstieg
articles=Artikel
articles-access=Artikel - Zugang
articles-metadata=Artikel - Metadaten
banners=Banner
command-line-interface=Befehlszeilenschnittstelle
configuration=Aufbau
contacts=Kontakte
...
```

When a heading is added to a manual it needs to be translated into each of the languages in which the manual is available. If a translated heading is not found a warning message is displayed during the build process and the English heading is used. 

All of the menu structure comes from the English original. It is not possible to add menu headings or menu items that do not exist in English.

## New Menu Item

To create a new menu item for a new article you need to select the `Menu Stashes` list and select the Manual you are working on. The stash is a list of headings and articles in English. The list controls which articles appear and in which order. You just need to enter a code line for the new item. The code lines look like this:

```
; Source for menu build - heading and item order.
; heading=heading=English Heading
; manual=heading=filename

heading=jdocmanual=Jdocmanual
docs=jdocmanual=introduction-to-jdocmanual.md
docs=jdocmanual=source-data.md
docs=jdocmanual=article-edit.md
docs=jdocmanual=article-new.md
```
Note that the `Preview` tab shows the menu. The menu itself does not work!

When you are satisfied, enter an explanatory `Commit Message`` in the `Comments`` tab and then `Commit` the changes.

The changes will be committed and the Menu updated. You will now be able to view your new article in the Manual view.

## Menu Item Order

The order of menu items is set by the order of lines seen in the stash. To change the order just cut and paste a line into a new position.