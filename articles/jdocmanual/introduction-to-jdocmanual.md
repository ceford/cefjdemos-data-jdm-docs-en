<!-- Filename: Introduction_to_Jdocmanual / Display title: Introduction to Jdocmanual -->

## About Jdocmanual

Jdocmanual is a Joomla component designed to display articles organised for
convenience with an Index to all articles at the left, the selected article
content in the centre and a list of headings in the article to the right. Each
collection of articles constitutes a Manual, of which there can be any number.

The content of each article is stored in Markdown format. Four Joomla Manuals
are available for demonstration purposes: ***Joomla User Manual***,
***Joomla Developer Manual***, ***Joomla Help Screens*** and ***Joomla
Documenter Manual***. The content of the articles came from the Joomla
Documentation site Joomla 4 and Joomla 5 articles. They can be displayed in
any language for which a translation is available.

## The Manual View

Jdocmanual has a default Manual view for the Administrator and a Site view
using the same code. This is the Administrator view:

![manual view](../../../en/images/jdocmanual/jdocmanual.png "The Jdocmanual Manual View")

### Manual and Language Selection

**Select Manual:** The list of manuals available is kept in a database table
with standard list and edit views.

**Index Language:** The index to the left can be displayed in a different
language from the content to the right. This is useful for problem solving
and checking on the translation status of articles. It does not require a
Multilingual site!

**Page Language:** If the article is NOT available in the selected language
it will be displayed in English. The index title link will be in English. At
the moment there are 8 languages available but few articles have been
translated.

**Actions:** There is an option to `Toogle Joomla Menu` to hide or show the
left Administrator menu so the full screen width can be used for article
display. There is also an option to `Update HTML` of the current Manual from
the Markdown source. That is related to how data is processed and stored for
delivery to the end user.

Try it: https://jdocmanual.org/
