<!-- Filename: JDOC:How_to_Create_a_Glossary_Entry / Display title: How to Create a Glossary Entry -->

The
[glossary](https://docs.joomla.org/glossary "Special:MyLanguage/glossary")
is an important reference, especially for users new to Joomla!.
Therefore special attention should be paid to the creation of glossary
entries. This tutorial will provide background information and guide you
through the process of creating an entry.

## What Comprises the Entries on a Glossary Page?

Glossary pages are based on [Glossary
Templates](https://docs.joomla.org/Template:Glossary "Template:Glossary").
When you follow the link you will see the list of glossary templates
available for several languages. These templates use DPL (Dynamic Page
List, a report generating tool used by wiki pages) to pull the titles
and contents of their glossary entries. Those entries are made of chunks
(reusable pieces of text to be be included into other pages). However,
the title of a glossary entry does not link to the chunk, but to the
article with the same name - which may or may not use the same chunk and
may contain additional information.

## Creating a Glossary Entry

In order to work properly, glossary entries need a chunk and an
"ordinary" article with the same name.

### The Article

The easiest way is to create the article page first. Enter:

    https://docs.joomla.org/My_Article_Name

in your browser. An editor window will open. Enter:

    {{Chunk:My_Article_Name}}
    [[Category:Landing Pages]][[Category:Glossary]]

This code will insert the contents of the chunk into the page and assign
categories to the article. The
[Glossary](https://docs.joomla.org/:Category:Glossary "Special:MyLanguage/:Category:Glossary")
category is mandatory, otherwise the article will not be linked. You are
free to add more categories. Note that, after inserting the chunk code,
you may add additional contents. These contents will not be visible on
the glossary page, but only when a user clicks on the linked title.

### The Chunk

After saving your article, you will see a red link taking you to the
(not yet existent) page for the chunk. Enter your definition for the new
glossary term here.

Then add these lines:

```markdown
<noinclude>[[Category:Glossary definitions|{{PAGENAME}}]]</noinclude>
```

This code adds the category to the chunk. If the chunk is not included
in the category [Glossary
Definitions](https://docs.joomla.org/:Category:Glossary_definitions "Special:MyLanguage/:Category:Glossary definitions"),
it will not show up in the glossary.

**Note** If you don't see a red link after saving the article, but text
is already inserted, a chunk with this name already exists. You can look
up all existing chunks <a
href="https://docs.joomla.org/index.php?title=Special%3APrefixIndex&amp;prefix=&amp;namespace=106"
class="external text" target="_blank" rel="noreferrer noopener">here</a>.

## Things To Keep In Mind

- Glossary entries should not be too long, but concise and easy to
  understand. In order to keep the glossary tidy, detailed explanations
  (with examples etc.) should not be placed into the chunk. Instead, you
  can use links inside the chunk pointing to other pages or put any
  additional information into the corresponding article.
- Please make sure your glossary entry is up to date with the latest
  Joomla! version. If your entry is specific to a version, let the
  readers know.
- Be careful when using sub-headings in your chunk. The glossary
  templates are coded in a way that will cut your chunk text at the
  first occurrence of a sub-heading. Consequently, all subsequent text
  will not appear on the glossary page. The chunk will not be truncated
  inside the linked article. So adding a sub-header might come in handy
  to show only the first part of the chunk content on the glossary page
  and the complete chunk on the article page.
