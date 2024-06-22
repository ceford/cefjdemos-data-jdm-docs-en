<!-- Filename: JDOC:Hatnotes / Display title: Hatnotes -->

Hatnotes look like this.

**Hatnotes** are short notes placed at the top of an article before the
primary topic, generally either to provide disambiguation of closely
related terms or to summarise a topic, and explain its boundaries.
"Hatnote" is also a polite term to refer to **improper disambiguation
links** which exceed standard length, link directly to trivial topics
instead of a disambiguation page.

This style guideline is intended to make this process more efficient by
giving article pages a consistent look, and avoiding distracting
information (such as extraneous links).

## Format

In most cases, a standard [disambiguation
template](https://docs.joomla.org/Category:Disambiguation_and_redirection_templates "Category:Disambiguation and redirection templates")
should be used. This permits the form and structure to change gracefully
and uniformly over time. Currently, each note should be italicized and
indented, without a bullet before the item. A horizontal dividing line
(----) should not be placed under a note, nor after the final item in a
list.

## Summarize or Not?

There is an ongoing dispute (in
<a href="https://en.wikipedia.org/wiki/Main_Page" class="extiw"
title="wikipedia:Main Page">larger wikis</a>) whether hatnote
disambiguation templates should include a brief summary of the article's
topic in their first sentence if they refer to "other uses".

Pro-summarizers argue that it's confusing and bad style to write the
hatnote such that the reader must read the words "other uses", look down
a line, and read the first sentence or paragraph before being able to
understand what the "other uses" actually refers to. Anti-summarizers
feel, on the other hand, that it's pointless and annoying to duplicate a
description that should be in the lead paragraph anyway.

Note that this argument is inapplicable in cases where only one other
use exists. If the phrase "other uses" does not exist, it would appear
no one would strongly favor including an article summary, so it's best
to use a template such as
{{[for](https://docs.joomla.org/Template:For "Template:For")}}.

## Placement

Place hatnotes at the top of the article, before images and templates
(like navigational templates), but below [maintenance
templates](https://docs.joomla.org/Category:Marker_templates "Category:Marker templates")
(like *inuse* templates) For example:

    {{inuse}}             <-- temporary meta content
    {{otheruses}}           <-- meta content
    [[Image:Joomla.png]]      <-- article content
    Joomla! is a '''CMS'''    <-- article content

In terms of document structure, it is awkward to have article content,
then meta content, then article content again. Analogously, in HTML it
would be bad form to put `<title>` and `<meta>` tags within `<body>`.

In terms of accessibility, not everyone is using or has the CSS
functionality that "floats" images and templates to the right or left,
which in turn gives many people the perception that a hatnote placed
after an image or template looks OK. Imagine if someone without CSS
landed on <a
href="https://en.wikipedia.org/w/index.php?title=Bread&amp;oldid=54316323"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">this version of Wikipedia's Bread
article</a> but happened to be in the wrong place. They'd have to
scroll, or perhaps in the case of a blind user, have their screen reader
trudge through a long "cuisine" template before reaching the navigation
aid they desire. Likewise, those who redistribute
<sup>[\[1\]](#cite_note-1)</sup> wiki content may choose to change or
eliminate CSS entirely. (To test the CSS-less realm in Firefox, go to
View, Page Style, No Style.)

Similarly, international wikis may decide to change the look of the
hatnote templates in the future. If such a change were made, hatnotes
that look fine now despite not being at the very top of the article
would visually clash with proximate images and templates.

## Examples of Proper Use

### Two Articles with the Same Title

> This article is about the Joomla! Application. For the user grant
> level, see [Administrator
> (User)](https://docs.joomla.org/Administrator_(User) "Administrator (User)").  
>   
> The *Administrator* allows maintenance and configuration of a Joomla!
> website...

When two articles share the same title, the unambiguated article should
include a hatnote with a link to the other article. It is not necessary
to create a separate disambiguation page.
{{[otheruses4](https://docs.joomla.org/Template:Otheruses4 "Template:Otheruses4")}}
may be used for this.

### Linking to a Disambiguation Page

> For other uses, see
> <a href="https://docs.joomla.org/Administrator_(disambiguation)"
> class="mw-redirect" title="Administrator (disambiguation)">Administrator
> (disambiguation)</a>.  
>   
> The *Administrator* is part of the Joomla! Content Management System
> and one of four web applications...

When a word has a primary meaning and three or more additional meanings,
the hatnote should show a link to a disambiguation page.
{{[otheruses](https://docs.joomla.org/Template:Otheruses "Template:Otheruses")}}
may be used for this.

## Templates

Templates which standardise and shorten the disambiguation hatnotes:

- [Category:Disambiguation and redirection
  templates](https://docs.joomla.org/Category:Disambiguation_and_redirection_templates "Category:Disambiguation and redirection templates")
- [Template:Otheruses
  templates](https://docs.joomla.org/Template:Otheruses_templates "Template:Otheruses templates")

1.  <span id="cite_note-1">[↑](#cite_ref-1) Redistribution of contents
    from the Joomla! Documentation wiki incl. translation is subject to
    the [Joomla! Electronic Documentation
    License](https://docs.joomla.org/JEDL "JEDL").</span>
