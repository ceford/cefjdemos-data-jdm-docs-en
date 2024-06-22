<!-- Filename: JDOC:Page_Markup_for_Translation / Display title: Page Markup for Translation -->

## Introduction

This article contains an outline of the page creation process:

1.  Entering text.
2.  Mark-up for Translation.
3.  Translation.

Its purpose is to help original content creators make good copy that is
easy to translate into languages other than English. For newcomers there
is quite a lot to read:

- [How to
  Contribute](https://docs.joomla.org/JDOC:How_to_Contribute_to_Joomla!_Documentation "Special:MyLanguage/JDOC:How to Contribute to Joomla! Documentation")
  explains how to create a User Account and create a User Page. Please
  try some personal content creation before taking on a public document.
- [Policies_and_guidelines](https://docs.joomla.org/JDOC:Policies_and_guidelines "Special:MyLanguage/JDOC:Policies and guidelines")
  has links to:
  - <a
    href="https://developer.joomla.org/en-gb-user-interface-text-guidelines/introduction.html"
    class="external text" target="_blank" rel="noreferrer noopener">Text
    Guidelines</a>
  - <a
    href="https://github.com/joomla/user-interface-text/blob/master/words2watch.md"
    class="external text" target="_blank"
    rel="nofollow noreferrer noopener">Words to Watch</a>
- [Page Translation
  Explained](https://docs.joomla.org/JDOC:Page_Translation_Explained "Special:MyLanguage/JDOC:Page Translation Explained")

You will need to come back to these documents from time to time!

## Page Creation

Source pages must be in British English!

A page is created from a URL pointing to a non-existant page, either
from a link in an existing page, which would appear in red to indicate
it does not exist, or from typing in the browser URL bar. Example:

    Here is my personal information: [[User:myusername | My User Page]]
     
    Or copy and past this into your browser URL bar:
     
    https://docs.joomla.org/User:myusername But please use your own Username!

Notice the `User:` part of the URL. It is a Namespace declaration that
helps classify the Joomla Documentation. The Namespaces you should be
aware of are J4.x:, Help4.x:, User: and Main: (which is omitted). See
[Namespaces](https://docs.joomla.org/JDOC:Namespaces "Special:MyLanguage/JDOC:Namespaces")
for the complete list.

Before a new page is created you will be asked to confirm that you wish
to create it. Once confirmed, a new empty page is opened in a text
editor. The page is actually created on first save from the editor.

Warning: You cannot delete a page you have created! You cannot erase the
history of changes you have made! You can mark a page for deletion but
there is no automated process to implement deletions.

Warning: You may see pages with a terminating language code, such as
`Example_Page/en`. You must never create such a page. The versions with
a terminating language code are created by the translation mechanism.

## Entering Content

The Joomla documentation site uses MediaWiki software with a custom
appearance. The editor uses wiki markup that you need to become familiar
with. The wiki editor window provides some help with buttons to create
headings, bold and italic text, lists and so on:

<img
src="https://docs.joomla.org/images/thumb/0/07/Jdoc-editor-en.png/800px-Jdoc-editor-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/0/07/Jdoc-editor-en.png 1.5x"
data-file-width="1000" data-file-height="772" width="800" height="618"
alt="Jdoc-editor-en.png" />

Take some time to familiarise yourself with the editor features. The
**Advanced**, **Special characters** and **Help** links reveal mutually
exclusive drop-down panels with extra information. The various buttons
either enclose selected text with structure or create an empty
placeholder structure.

Start by adding a wiki template at the top of the edit screen to
indicate it is in use:

    {{inuse}}

When creating content you should not use any html or other non-wiki
markup unless absolutely necessary. Paragraphs should be separated by
blank lines. It is always a good idea to preview changes before saving.
You will more easily spot your own spelling or grammatical errors. When
you save any changes please provide a brief summary of what has changed.
This will be seen in the History and will help maintainers and
translators.

If you need to include images or links please read the information on
naming conventions:

- [Image naming
  guidelines](https://docs.joomla.org/JDOC:Image_naming_guidelines "Special:MyLanguage/JDOC:Image naming guidelines")
- [Translating
  Links](https://docs.joomla.org/JDOC:Translating_Links "Special:MyLanguage/JDOC:Translating Links")

## Prepare for Translation

When your page is complete and you have checked it for spelling, grammar
and words2watch you may consider it ready for others to use. At that
stage a person responsible for translation markup will add these lines
at the top of the document, or you can do it yourself:

```markdown
<noinclude><languages /></noinclude>
<translate>
```

And these lines at the bottom of the document:

```markdown
<noinclude>
    [[Category:Tutorials{{#translation:}}]]
    [[Category:xxx]]
</noinclude>
</translate>
```

Where xxx is a relevant Category for this document. There can be any
number of categories but using more than one or two eventually becomes
counterproductive.

**Important:** earlier documents have `translate` tags on almost every
natural break. This is actually a lot of work, often done wrongly and
not necessary. However, if your are working on an existing document with
many translation tags you have no option but to follow suit for any new
blocks of text that you add.

### Check spacing

With single opening and closing `translate` tags at the top and bottom
of the document, translation block markers will be added on blank lines.
So individual paragraphs will be separate translation units. List blocks
could also be translation units. If there is a short paragraph following
a heading they can be kept together as a translation unit by having no
blank like following the heading.

### Images

Images are probably best treated as translation units with a blank line
above and below. Avoid using small images if you can as they may be
difficult to reproduce in translation, for example images of buttons or
drop-down lists.

### Links

Read the documentation on [Translating
Links](https://docs.joomla.org/JDOC:Translating_Links "Special:MyLanguage/JDOC:Translating Links").

In documents other than Help pages, internal links should precede the
document name with S:MyLanguage/ or Special:MyLanguage/ like this:

    [[S:MyLanguage/JDOC:Translating_Links | Translating Links]]

This ensures that a linked page will be in the user's preferred language
if the page is available in that language. Otherwise the link will be to
the version of the page in English.

In Help pages, the `S:MyLanguage/` construction does not work. In that
case a specific language code must be added to the document name:

    [[S:MyLanguage/Help4.x:Site_Global_Configuration/en | Global Configuration]]

The translator should only change `/en` to another language code if the
page is known to exist in that language.

## Mark for Translation

When a document is ready for translation, a line at the top will
indicate one or more of several possible actions:

- Translate this page
- Mark this page for translation
- This page has changes since it was last marked for translation (with a
  link to the changes and a link to remark the changes)

The Page Translation screen shows how the document is segmented into
translation units:

<img
src="https://docs.joomla.org/images/thumb/d/d8/Special-page-translation-en.png/800px-Special-page-translation-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/d/d8/Special-page-translation-en.png 1.5x"
data-file-width="1000" data-file-height="508" width="800" height="406"
alt="Special-page-translation-en.png" />

And scrolling down shows where any changes may have been made. The
following illustration shows correction of a typographical error. As
this is unlikely to have propagated into any translation it is not
necessary to invalidate existing translations:

<img
src="https://docs.joomla.org/images/thumb/3/31/Special-page-translation-change-en.png/800px-Special-page-translation-change-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/3/31/Special-page-translation-change-en.png 1.5x"
data-file-width="1000" data-file-height="343" width="800" height="274"
alt="Special-page-translation-change-en.png" />

Down at the bottom of the page is a button to
`Mark this version for translation`. The person who does the translation
marking will check this page to see that the segmentation is appropriate
for the document and if necessary make changes before clicking the
button.

When marked for translation, a robot places translation marker tags in
the page source. They look like this:

```markdown
    == Introduction == <!--T:2-->
```

If you make changes later you should leave these tags alone. Changing or
removing the tags will corrupt the translations. You do not add any
similar tags yourself. The robot does it all.

## Translation

When ready for translation, a translator can select the
`Translate this page` link and then select a language to translate into.
The following screenshot shows the top part of the page for translation
from English to German:

<img
src="https://docs.joomla.org/images/thumb/4/4c/Special-page-translation-german-en.png/800px-Special-page-translation-german-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/4/4c/Special-page-translation-german-en.png 1.5x"
data-file-width="1000" data-file-height="508" width="800" height="406"
alt="Special-page-translation-german-en.png" />

If a segment has not been translated the right hand box will be empty.
Here is an example where content translation has just started:

<img
src="https://docs.joomla.org/images/thumb/c/ce/Special-page-translation-german-introduction-en.png/800px-Special-page-translation-german-introduction-en.png"
decoding="async"
srcset="https://docs.joomla.org/images/c/ce/Special-page-translation-german-introduction-en.png 1.5x"
data-file-width="1000" data-file-height="508" width="800" height="406"
alt="Special-page-translation-german-introduction-en.png" />

A translation has to be entered and the `Publish translation` button
selected to record the translation, in this case in the version of the
document with **/de** appended.

A long document may have many translation units, perhaps even a few
hundred, especially if the original translate tags had been applied
excessively. Sometimes the content to be translated is as simple as `en`
to be translated to `de` for image and link tags. Sometimes the
translate tags have been wrongly placed inside mediawiki markup tags
such as headings or lists instead of outside them. This makes it
difficult for translators to see the context of their translation.
Unfortunately nothing can be done about this without invalidating
existing translations.
