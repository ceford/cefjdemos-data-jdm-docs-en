<!-- Filename: JDOC:Using_chunks_in_Joomla_help_screens / Display title: Using chunks in Joomla help screens -->

This article documents how to use "chunks" when writing help screens for
Joomla. Note that we are only using one set of help screens for entire
series. This means the help screen will all use 'Chunk30', 'Chunk4x'.
Examples show version 3.

## What is a "chunk"?

A chunk in MediaWiki jargon is a reusable piece of content. For help
screens, we use chunks for text that will appear more than once in the
help screens.

For example, we have a column called 'Category' in

1.  Articles
2.  Banners
3.  Contacts
4.  News Feeds
5.  User Notes
6.  Web Links

In each of these screens, the Category column shows the category for the
item. So, instead of copying and pasting the same text into these
different help screens, we create a "chunk" for this.

A huge advantage of this approach is that we can edit and improve this
chunk in one place and the new version will automatically show in each
screen.

## Using an Existing Chunk

The syntax for including an existing chunk is as follows:

`{{Chunk30:Help_screen_column_header_Category}}`

The syntax for making the chunk ready for translate:

`{{Chunk30:Help_screen_column_header_Category/en}}`

## Creating a New Chunk

Before creating a new chunk, check to see if it already exists. You can
get a complete list of the used

- <a
  href="https://docs.joomla.org//docs.joomla.org/index.php?title=Special:Allpages&amp;namespace=140"
  class="external text" target="_blank" rel="noreferrer noopener">Chunk30
  page</a>
- <a
  href="https://docs.joomla.org//docs.joomla.org/index.php?title=Special:Allpages&amp;namespace=152"
  class="external text" target="_blank" rel="noreferrer noopener">Chunk4x
  page</a>.

You can get to this page by clicking the 'Special Pages' link on the
toolbox menu:

1.  In the 2nd section (*List of pages*) click *All pages with prefix*
2.  Select the desired Namespace (for example, "Chunk30", "Chunk4x")
    from the dropdown input box
3.  Then press the "Show" button to see a list of all the pages in the
    namespace.

Creating a new chunk is easy. However, please be careful to following
the naming convention so that others will be able to re-use your chunks.

The steps for creating a new chunk are as follows:

1.  Enter the chunk in an article, just as you would for an existing
    chunk. For
    example:`{{Chunk30:Help_screen_column_header_My_New_Chunk}}`
2.  'Preview' the article, scroll to the bottom of the screen, click on
    'Templates used on this page:'. The new chunk will show in red under
    "Templates used in this preview" as in the example below<img
    src="https://docs.joomla.org/images/9/93/Chunk-tutorial-screenshot-20120622-01.png"
    class="thumbborder" decoding="async" data-file-width="443"
    data-file-height="152" width="443" height="152"
    alt="Chunk-tutorial-screenshot-20120622-01.png" />
3.  Open the edit link *in a new browser window*. (Otherwise, you might
    lose your edits on the current article you are editing.) You will be
    taken to a screen where you can enter in the text for this chunk.
    This is just like editing any other wiki article.
4.  After you have entered and saved the text for the chunk, return to
    your original article and again click on 'Preview'. Now you should
    see the chunk show as normal text.

## Naming Conventions

The key idea for naming conventions is to be consistent in how we name
chunks so we don't end up with duplicates. Here are a few guidelines:

- For items that appear in the column heading of a manager screen, use
  the exact column header name (for example, 'Access', 'Created By', and
  so on).
- Generally use initial caps.
- In many cases, we have the same name for a value in a column header as
  we do when entering the value in an edit screen: (For example,
  'Category' or 'Title'.) In these cases, we need different help text
  for the value as a column versus the value as an entry.The convention
  is to use the column name for when the value appears in a manager list
  (for example, *Category*) and the word 'Enter' in front when the value
  is being edited (for example, *Enter Category*).

## Tips

- If you aren't sure whether this chunk will be used somewhere else, you
  don't need to worry about creating a chunk. Just enter the text. It is
  easy to go back later and convert text to chunks if needed.
- Check the existing chunks before creating a new one. Also, use the
  existing chunks as a guide for naming and other conventions when
  creating new chunks.
- Don't be afraid to make a mistake! One great thing about the wiki is
  that we can easily tidy things up later. The main thing is to get
  useful content in the help screens to help users with Joomla.
