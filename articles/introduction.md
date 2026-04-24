<!--
{
  "source": "",
  "title": "Introduction",
  "description": "Jdocmanual is a Joomla component designed for the display of multi-lingual technical information.", 
  "author": ""
}
-->

Jdocmanual is a Joomla component designed for the display of multi-lingual technical information. Source text is stored in Markdown format completely separate from the Joomla installation, which is used for content management and presentation. 

Although designed initially for Joomla documentation it can be used for any documentation that requires a layout with a list of Contents to the left, a Content area in the centre and a list of content Headings to the right. This is the layout used by the Mozilla Developer Network (MDN), Bootstrap and many others.

Large documentation sets may be divided into sections here termed Manuals. MDN has separate sections for HTML, JavaScript, CSS and more. Joomla has separate sections for Users, Developers and more.

## Jdocmanual Features

The following screenshot shows a user view:

![site example screenshot](../../en/images/introduction/00-site-example.png)

Notable features:

- The **Select Manual** button allows selection of any of the installed Manuals. There could be many!
- The **Page Language** button allows selection of any of the installed languages. If an article is not available in the selected language then the article will be delivered in the default language.
- The **Menu Language** allows the menu to appear in a different language from the page. This is incredibly useful to site maintainers who may not be multi-lingual.
- The **list of Articles** at the left is generated from a menu.json file located in the default language data set. Each language has a translation file for headings but the article titles are taken from the articles themselves.
- The article headings to the right are generated from the article content in the article language.

## Version 5

The latest version of Jdocmanual is not backwards compatible with previous versions. To improve usability the data has been restructured and the code revised. Users of older versions should uninstall the existing component, checkout the latest versions of the Joommla data sources and then install the latest version of Jdocmanual.
