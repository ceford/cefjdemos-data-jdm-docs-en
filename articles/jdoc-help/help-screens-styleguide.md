<!-- Filename: Help4.x:Help_screens_styleguide / Display title: Help screens styleguide -->

<a href="https://docs.joomla.org/Help4.x:Help_screens"
class="mw-redirect" title="Help4.x:Help screens">Return to Joomla! 4.x
Help Screen Wiki Page</a>

This is a work in progress and should be used as a guideline for
creating Help screens for **Joomla 3.x**. The help screens which exist
on the Joomla! Docs Wiki are being accessed by every Joomla!
installation using the default help system. By following this
styleguide, the Joomla! Project can offer consistency throughout the
help screens to allow for easier navigation.

If you have a question, please post in on the associated talk page of
the help screen by clicking the ***Discussion*** tab at the top of the
help screen page.

## Help Screen Page Layout

### Description

Each and every help screen should have a "**Description**" section. This
goes into more detail about what the screen does and is used in help
screen tables throughout this wiki. <a
href="https://docs.joomla.org/Menu_Management#Menu_Management_Help_Screens"
class="mw-redirect" title="Menu Management">Here is an use example</a>.

There is no specific format to this section because the description
should be in direct correlation with the purpose and functionality of
the screen. There may be subsections to the description that describe
more specific details. Try to keep the description short and to the
point, if the description is long then consider using bullet points to
summarise it.

## How to Access

Each and every help screen should have a "**How to access**" section
that gives the steps required to reach the screen that is being
described. This might be redundant because a user must be on the
administrator screen in order to have retrieved the help screen.
Remember, the help screens can be retrieved in a number of different
ways. For example, someone using a search engine to find out how to do
something might come across a help screen on the wiki without ever
having accessed the help system.

Here's an example:

<table>

<tbody>
<tr class="odd">
<td><ul>
<li>Click the Article Manager icon in the <a
href="https://docs.joomla.org/Help4.x:Site_Control_Panel"
title="Special:MyLanguage/Help4.x:Site Control Panel">Control
Panel</a></li>
<li>Select <strong>Content → Article Manager</strong> from the drop-down
menu of the <em><strong>Joomla! Administrator Panel</strong></em>.</li>
<li>Click the <strong>Article</strong> link while viewing the <a
href="https://docs.joomla.org/Help4.x:Components_Content_Categories"
class="mw-redirect"
title="Help4.x:Components Content Categories">Category Manager</a> or <a
href="https://docs.joomla.org/Help4.x:Content_Featured_Articles"
class="mw-redirect" title="Help4.x:Content Featured Articles">Featured
Articles</a> in the left, upper sidebar.</li>
</ul></td>
</tr>
</tbody>
</table>

\*Note:

- If the way to reach the screen is from another screen then the name of
  that screen should be a link to its help screen.
- You "click" on buttons, including toolbar buttons, but you "select"
  menu items. Consistent use of this terminology should help users.
- For ease of rendering the right arrow( **→** ), **This
  pointing **→** at that** see the
  {{[rarr](https://docs.joomla.org/Template:Rarr "Template:Rarr")}}
  template for use. It was designed to make help screen **How to
  Access** instructions easy to write.

### Screenshot

Screenshot showing the overall look of the screen.

\*Notes:

- Screenshot images can be any width, but larger images should have the
  \|800px added in the source.
- The filename should follow our
  <a href="https://docs.joomla.org/JDOC:Image_naming_convention"
  class="mw-redirect" title="JDOC:Image naming convention">standard naming
  conventions</a> for help screens.  
  **Help-3x-**
  **-screen-en.png**.  
  For example, a screenshot of the Article Manager screen would be
  **\[\[File:Help-3x--content-article-manager-screen-en.png\]\]**.
- The filename should always include a language code at the end of the
  name, for English -en is added.
- You can use either .png or .jpg files.

## Form Fields (by Tab)

### Details Tab

This section should only be included on help screens that describe
screens which include a form. This includes all the add/edit screens,
but also includes screens like [Help4.x:Site Global
Configuration](https://docs.joomla.org/Help4.x:Site_Global_Configuration "Help4.x:Site Global Configuration")
and modal popups like <a
href="https://docs.joomla.org/Help4.x:Components_Article_Manager_Options"
class="mw-redirect"
title="Help4.x:Components Article Manager Options">Help4.x:Components
Article Manager Options</a>.

### Other Tab Types

If fields are grouped into fieldsets or tabs then group the fields under
sub-headings.

### Column Headers

This section should only be included on help screens that describe
back-end manager screens; that is, where you have a list of items being
shown. This section should describe each of the list columns.

### List Filters

This section should only be included on help screens that describe
back-end manager screens; that is, where you have a list of items being
shown. This section should describe how to use the list filters to
filter the contents of the screen. See
<a href="https://docs.joomla.org/Screen.content.15#List_Filters"
class="mw-redirect"
title="Screen.content.15">Screen.content.15#List_Filters</a> for example
from 1.5.

### Options

This section should only be included on help screens where the screen
has an Options toolbar button which opens a modal options sub-screen. If
there are many options and the help screen would become excessively long
if they were to be described here, then link to a separate help screen
with an "\_Options" suffix. For example, see <a
href="https://docs.joomla.org/Help4.x:Components_Article_Manager_Options"
class="mw-redirect"
title="Help4.x:Components Article Manager Options">Components Article
Manager Options</a>.

Since the Options modal screen is usually tabbed you should add a
sub-section under this section for each tab. For example, if there is a
tab labelled "Editing Layout" then you should add a third-level heading
of that name and within that sub-section you should describe each of the
available fields. You should start each sub-section with a screenshot of
the appropriate Options panel.

### Toolbar

Obviously, this section should only be included on help screens where a
toolbar is present.

Describes the available buttons and their associated functions. Use
**chunks** here because many will be the same for different screens.
Best to provide a picture of the toolbar.

The first word should always be a verb and, unless it is an irregular
verb, it should also end in the letter "s". This means you should
structure the description as if you are using the word "this" as the
subject, but leave the subject out of the sentence. This will make the
sentence actually a sentence fragment. For instance:

- Instead of "To find buried treasures, click this button."
  - Say, "Finds buried treasures."
- Instead of "You can click this button to insert a picture of John
  Stamos into the current document."
  - Say, "Inserts a picture of John Stamos."
- Instead of "Inform yourself that a picture of John Stamos is the same
  thing as a buried treasure."
  - Say, "Informs you that a picture of John Stamos is the same thing as
    buried treasure."

Since many toolbars are the same across multiple screens, the image
filenaming convention for toolbars is aimed at making it easy to re-use
toolbar images wherever possible. Toolbar images should follow this
naming convention: Help-Toolbar-.png where is a '-' separated list of
the toolbar legends. Each word should be capitalised, spaces and '&'
removed. For example: Help30-Toolbar-New-Edit-Delete-Options-Help.png

### Batch Process

This section should only be included on help screens where the screen
has a batch process feature. For example, see
<a href="https://docs.joomla.org/Help4.x:Components_Banners_Categories"
class="mw-redirect"
title="Help4.x:Components Banners Categories">Help4.x:Components Banners
Categories</a>.

### Quick Tips

As the name suggests, this section should include tips, hints,
suggestions that can assist a user in performing tasks involving the
screen.

### Related Information

Generally this should be a list of links to further or related
information. All links should be to pages on this wiki. No external
links without very good reason.

## Notes for help screen editors

- [Layout of a typical Help
  Screen](https://docs.joomla.org/Help_screen_layout "Help screen layout")
- Overview of <a
  href="https://docs.joomla.org//docs.joomla.org/index.php?title=Special:Allpages&amp;namespace=136"
  class="external text" target="_blank" rel="noreferrer noopener">Help
  screen chunks</a>  
  For usage information and examples see the following templates:
  - {{[colheader](https://docs.joomla.org/Template:Colheader "Template:Colheader")\|Column
    name}} includes one of the *Help screen column header XYZ* chunks
  - {{<img src="https://docs.joomla.org/images/4/4d/Compat_icon_3_x.png"
    decoding="async" data-file-width="40" data-file-height="17" width="40"
    height="17" alt="Joomla 3.x" />
  - <img src="https://docs.joomla.org/images/4/4d/Compat_icon_3_x.png"
    decoding="async" data-file-width="40" data-file-height="17" width="40"
    height="17" alt="Joomla 3.x" />
  - {{[toolbaricon](https://docs.joomla.org/Template:Toolbaricon "Template:Toolbaricon")\|Action
    name}} is for *Help screen toolbar XYZ*
  - {{[cpanelicon](https://docs.joomla.org/Template:Cpanelicon "Template:Cpanelicon")\|Icon
    name}} is for *Help screen icon XYZ*
  - for proper categorisation read the instructions of
    [Template:cathelp](https://docs.joomla.org/Template:Cathelp "Template:Cathelp")
    <span class="small">(<a
    href="https://docs.joomla.org/index.php?title=Template_talk:Cathelp&amp;action=edit&amp;redlink=1"
    class="new" title="Template talk:Cathelp (page does not exist)">talk</a>,
    [backlinks](https://docs.joomla.org/Special:WhatLinksHere/Template:cathelp "Special:WhatLinksHere/Template:cathelp"),
    <a
    href="https://docs.joomla.org//docs.joomla.org/index.php?title=Template:Cathelp&amp;action=edit"
    class="external text" target="_blank" rel="noreferrer noopener">edit</a>)</span>
- [Content
  editors](https://docs.joomla.org/Content_editors "Content editors")
  - {{[Chunk30:TinyMCE](https://docs.joomla.org/Chunk30:TinyMCE "Chunk30:TinyMCE")}}
    for TinyMCE
  - {{[Chunk30:No
    editor](https://docs.joomla.org/Chunk30:No_editor "Chunk30:No editor")}}
    for No editor
- Did you notice a mistake or do think it's useful to add some extra
  information? You're welcome to modify the Help Screen. Please change
  the status of the modified Help Screen after you modified it:
  - Is the status at the moment 'Ready' or 'To be moved'? Change it to
    'Modified by \[name\]' (replace \[name\] for your username at the
    Joomla! Docs Wiki)
  - Is the status at the moment 'To be reviewed'? You don't have to
    change the status in that case.
- Image file naming convention:
  - help16-*\[menu system path separated by
    dashes\]*-*\[screenElementType\]*-en.png,jpg
    - Replace *\[menu system path separated by dashes\]* with the names
      of the menu items that you would need to select to get to the item
      you are taking a screenshot of. Separate menu items with a dash
      ( - ) and if the menu item name has more than one word in it, then
      separate the words with an underscore ( \_ ). Do not use spaces in
      your file name. Replace spaces with the underscore ( \_ )
      character.
    - Replace *\[screenElementType\]* with the type of the screen
      element that your picture contains. Screen element types are:
      - **screen** - This is a screenshot of the entire menu item
      - **toolbar** - This is a picture of the menu item's tool bar.
      - **menu** - This is a picture of the menu item's menu bar.
      - NOTE: As more screen element types are needed, add them to this
        style guide so that help documentation developers can refer to
        this guide and stay consistent.
    - Examples using the image naming convention:
      - A screenshot of the Extension Manager's "Discover" screen would
        be named: help16-extension_manager-discover-screen-en.png
      - A screenshot of the Extension Manager's "Discover" screen tool
        bar would be named:
        help16-extension_manager-discover-toolbar-en.png
