<!-- Filename: JDOC:Page_Translation_Explained / Display title: Page Translation Explained -->

More information on this topic is available at the <a
href="https://www.mediawiki.org/wiki/Help:Extension:Translate/Page_translation_administration"
class="external text" target="_blank"
rel="nofollow noreferrer noopener">Mediawiki</a>

**What.** The page translation feature allows controlled translation of
wiki pages into other languages. That means that the content of each
translation will be, usually, equal to the source page. This is opposed
to, for example, the different language version of articles in different
Wikipedias, which are fully independent of each other. It is assumed
that pages are only translated from one primary language to other
languages, but translators can take advantage of translations in other
languages too if they exist.

**Why.** Without any help, translating more than a few pages into other
languages becomes a time-waster at best, an unmaintainable mess at
worst. With the page translation feature you can avoid the mess and
bring structure to the translation process. The core idea is that the
source text is segmented into smaller units, each of which will be
translated individually. When the source text is segmented into units,
all changes can be isolated and translators only need to update the
translations of units which have had changes in source text. This also
enables translators to work on units of manageable size and share the
work between multiple translators or continue the translation in later
sessions, because they don't need to do all at once.

**Who.** This page provides deeper insight on how the system works, and
suggests best practices for a wide variety of cases. This page is
intended for page translation administrators and generally for everyone
who edits the source text of translatable pages, even if they don't have
the access to the administrative features of approving changes for
translation.

## Life of a translatable page

**Roles.** Multiple people are involved in the process of writing and
translating a wiki page: the initial writer creates a page, someone
corrects spelling errors, a page
<a href="https://docs.joomla.org/JDOC:Translation_Administrators"
class="mw-redirect" title="JDOC:Translation Administrators">translation
administrator</a> marks the page for translation, <a
href="https://docs.joomla.org/index.php?title=JDOC:Translators&amp;action=edit&amp;redlink=1"
class="new"
title="JDOC:Translators (page does not exist)">translators</a>
translate, someone makes changes to the page, a page translation
administrator marks those changes for translation and translators update
translations. Those roles may overlap more or less, but the ultimate
responsibility for a hassle-free translation is left for the page
translation administrator. The administrator decides when the page is
ready for translation the first time, ensures that the segmentation
serves a purpose and approves (or corrects) changes.

**Preparation.** To have something translated you have to write it
first. If you already have done translation without the Translate
extension, see below the [section about migrating
translations](#migration). If you want lots of translation and quickly,
it is crucial for the source text to be in good shape. Before marking
page for translation, ask someone else to proofread it and if possible
ask a language specialist to make the text more clear and concise.
Difficult vocabulary and hard to understand sentences are a show stopper
to many volunteer translations. Markup too can cause problems for
translators, but as a translation administrator you can avoid those
issues, see below the [section about handling markup](#segmentation).
Naturally the changes you make to the source text of translation force
update of all existing translations, so it is better to wait until the
contents of the page have stabilized. On the other hand, changes do
happen, and the system handles that well, so check out the [section
about handling changes](#changes) below.

**Tagging.** When the text is otherwise ready for translation, anyone
can mark the translatable parts by wrapping them inside tags and adding
the bar to the page. The latter adds a list of all translations of the
page, with their completion and up-to-date percentages. There is no
other indication that translations exist. See below [how to actually do
the tagging](#markup). The system will detect when the tags are placed
on the translatable page, and the page will have a link to mark it for
translation. It will also complain and prevent saving if you for example
forgot to add a closing tag. The translatable page will also be listed
on Special:PageTranslation as *ready for marking*.

**Marking.** After the tagging, a translation administrator marks the
page for translation. The interface is explained in <a
href="https://docs.joomla.org/Help:Extension:Translate/Page_translation_example"
class="new"
title="Special:MyLanguage/Help:Extension:Translate/Page translation example (page does not exist)">Page
translation example</a>. The translation administrator's responsibility
is to make sure that the segmentation makes sense and that tagging has
been proper. The page can be marked again if it has changed in the
meanwhile. See below [how to make changes that cause minimal
disruptions](#changes). The marking of the page starts a background
process that uses MediaWiki's <a
href="https://docs.joomla.org/index.php?title=Manual:Job_queue&amp;action=edit&amp;redlink=1"
class="new" title="Manual:Job queue (page does not exist)">job queue</a>.
This process goes over each translation page and regenerates it: changes
in the translation page template will be reflected and outdated
translations will be replaced temporarily with the original source text.
On the contrary, the translation interface is updated immediately.

**Changes.** Users can continue making changes to the translatable page
source. The changes will be visible to users viewing the page in the
source language, but translations are done against the translation units
extracted from the last version of the translatable page which has been
marked for translation: the translation pages are reported to be 100 %
up to date if all translation units have been translated, even if the
source page has new changes. You can easily see whether there are
unmarked changes when viewing the translatable page in the source
language: there is a notice at the top which says that you can translate
this page and also links to changes if there are any.

**Source language**. There is also a translation page with the language
code of the source language: it doesn't contain the extra tags and other
markup related to page translation which are used in the translatable
page source. This page is not linked from the interface, but it is handy
for example when you want to transclude the page (typically for
translatable templates) or export it.

**Closed translation requests.** Some translatable pages have a content
that is only interesting for a certain period of time. For example
announcements and regular status updates, like the Wikimedia monthly
highlights. You can keep those pages around with translations, but hide
them from the translation interface. This does not prevent further
translations to the pages, but it greatly reduces the chance that a user
accidentally starts translating the page. Discouraging and its reversion
are done from Special:PageTranslation.

**Prioritizing languages.** You can also define a list of languages that
you specifically want translations into; leaving the language list empty
is interpreted as all languages allowed. The page will behave like a
discouraged page (see previous paragraph) for the languages not in the
priority list and, when translating into them, translators will be given
a notice. You can also prevent the translation in other languages, say
if translations are actually used elsewhere and you won't be able to use
them but in some languages.

**Grouping.** It is possible to group related pages together. These
groups work like all the other message groups. They have their own
statistics and contain all the messages of the subgroups: in this case
translatable pages. This functionality is currently in
[Special:AggregateGroups](https://docs.joomla.org/Special:AggregateGroups "Special:AggregateGroups").
Aggregate message groups are collapsed by default in
[Special:LanguageStats](https://docs.joomla.org/Special:LanguageStats "Special:LanguageStats")
in the group selector at Special:Translate.

**Moving.** You can move translatable pages as you would move any other
page. When moving you can choose whether you want to move any
non-translation subpages too. The move uses a background job to move the
many related pages. While the move is in progress, it is not possible to
translate the page. Completion is noted in the page translation log.

**Deleting.** Like move, deletion is accessed from the normal place. You
can either delete the whole translatable page, or just one translation
of it. To delete one translation, go to the translation page and then
access delete. As in move, a background process will delete the pages
over time. Deletion will also delete the related translation unit pages.
Completion is noted in the page translation log.

**Reverting.** Similarly, reverting incorrect edits works as usual
(including rollback button): you only have to edit the affected
translation unit and the translation page will be updated as well. To
find the edit to the translation unit from the edit to the translation
page, just click the "contribs" link for the editor and look for an edit
at a similar time.

**Protecting.** It is possible to
<a href="https://docs.joomla.org/Help:Protected_pages" class="new"
title="Special:MyLanguage/Help:Protected pages (page does not exist)">protect</a>
the translatable page. Translation pages cannot be protected, nor does
the protection of the translatable page extend to them. To prevent
further edits to translations, you should add the source language as
only priority language and disable translations to other languages, see
*prioritizing languages* above. Together these two actions effectively
prevent changes to both the source page and translation pages with its
translation unit pages. It is possible to protect individual translation
unit pages, though it is not advisable.

**Removal from translation**. It is also possible to unmark a page for
translation. First you need to remove all translate tags from the page.
Then you can use
[Special:PageTranslation](https://docs.joomla.org/Special:PageTranslation "Special:PageTranslation")
or follow the link in the top of translatable page to remove it from
translation. This will remove any structure related to page translation,
but leave all the existing pages in place, freely editable. This action
is not recommended.

## Anatomy of a translatable page

The translation of a translatable page will produce many pages, which
all together compose the translatable page in the broadest sense: their
title is determined by the title of the translatable `Page`:

- `Page` (the source page)
- `Page/<language code>` (the translation pages, plus a copy of the source page without
  markup)
- `Translations:Page/<translation unit identifier>/<language code>` (all the translation unit pages)

In addition to this, there are the translation page template and the
sources of translation units, extracted from the source page and stored
in the database. The system keeps track of which versions of the source
page contain translation tags and which version of them have been marked
for translation.

Every time a translation unit page is updated, the system will also
regenerate the corresponding translation page. This will result in two
edits. The translation unit page edit is hidden by default in recent
changes and can be shown by choosing *show translations* from the
translation filter. Any action other than editing (like deleting and
moving) the translation unit pages will not trigger the regeneration of
the corresponding translation page.

## Segmentation

General principles:

1.  All text intended for translation must be wrapped inside translate
    tags. There can be multiple pairs of tags in one page.
2.  Everything outside those tags will not change in any translation
    page. This static text, together with the placeholders which mark
    the place where the translation of each translation unit will be
    substituted, is called the translation page template.
3.  Too much markup in the text makes it difficult for translators to
    translate. Use more fine grained placing of translate tags when
    there are lots of markup.
4.  The text inside translate tags is split into translation units where
    there is one or more empty lines between them (two or more
    newlines).

**Restrictions.** The page translation feature places some restrictions
on the text. There should not be any markup that spans over two or more
translation units. In other words, each paragraph should be
self-contained. This is currently not enforced in the software, but
violating it will cause invalid rendering of the page, the severity
depending on whether MediaWiki itself is able to fix the resulting html
output or not.

**Parsing order.** Beware, the translate tags work differently from
other tags, because they do not go through the parser. This should not
cause problems usually, but may if you are trying something fancy. In
more detail, they are parsed before any other tags like `<pre>` or 
`<source>`, with the exception of `<nowiki>` which is recognized by 
the Translate extension in some circumstances (such as rendering a page) 
but not in others (such as generating the list on Special:PageTranslation 
of pages containing `<translate>`). If you want to have the literal 
expression "`<translate>`" in the source text, you should escape it 
like "`&lt;translate>`".

**Tag placing.** If possible, try to put the tags on their own lines, 
with no empty lines between the content and the tags. Sometimes this 
is not possible, for example if you want to translate some content 
surrounded by the markup, but not the markup itself. This is fine too, 
for example:

```markdown
{{Template|<translate>Some localised parameter</translate>}}
```

To make this work, the extension has a simple whitespace handling:
whitespace is preserved, except if an opening or closing translate tag
is the only thing on a line. In that case the newline after the opening
tag or before the closing tag is eaten. This means that they don't cause
extra space in the rendered version of the page.

**Variables.** It is possible to use variables similar to template
variables. The syntax for this is `content`. For translators these will
show up only as `content`, and in translation pages will automatically
be replaced by the value defined in the translatable page (so they are
global "constants" across all its translation pages). Variables can be
used to hide untranslatable content in the middle of a translation unit.
It also works for things like numbers that need to be updated often. You
can update the number in all translations by changing the number in the
translatable page source and re-marking the page. You do not need to
invalidate translations, because the number is not part of the
translation unit pages.

## Markup examples

Below are listed some alternatives and suggested ways to handle
different kinds of wiki markup.

<table class="prettytable">

<tbody>
<tr class="odd">
<td width="10%"><strong>Categories</strong></td>
<td width="25%">Categories can be added in two ways: in the translation
page template or in one of the translation units. If you have the
categories in the translation page template, all translations will end
up in the same category. If you have categories inside translation
units, you should teach the users a naming scheme. On the right we show
two possible schemes which are independent of the technical means to
adopt them.</td>
<td><p><strong>No translation</strong>: Category:Cars</p>
<ul>
<li>All translations in same category (good if only few languages, bad
if many).</li>
<li>Category name not translated (can be put as is in the translation
template).</li>
</ul>
<p><strong>Translation by adding language suffix</strong>:
Category:Cars/fi (recommended but unsupported)</p>
<ul>
<li>Category page name not translated (just like the page names).</li>
<li>One category for each language.</li>
<li>Page translation could be used for the category itself: the
categories would be linked together and the headers would be translated
(but not the name of the category in links and such).</li>
<li>This option is not yet supported out of the box by the Translate
extension. You need to either instruct your translators to add the
language code suffix to the category markup in the translation, or leave
the category out of translation and write your own templates which add
the language code automatically.<br />
</li>
</ul>
<p>There are some such templates available on the wikis which use the
Translate extension, but they won't be dealt with here. Additionally,
categories' description pages will have to be created manually and
translated with a non-Translate system, because the extension is not
able to deal with them.</p></td>
</tr>
<tr class="even">
<td><strong>Headers</strong></td>
<td>Headers can in principle be tied to the following paragraph, but it
is better to have them separated. This way someone can quickly translate
the table of contents before going into the contents. When tagging
headers, it is important to include the header markup inside the tags,
or MediaWiki will no longer identify them properly, for example when
trying to edit a specific section of the source page. The markup also
immediately gives translator a context: he/she is translating a
header.</td>
<td><p><strong>Wrong:</strong></p>
<pre><code>== &lt;translate>Culture&lt;/translate> ==</code></pre>
<p><strong>Correct:</strong></p>
<pre><code>&lt;translate>== Culture ==&lt;/translate></code></pre>
<p><strong>Suggested segmentation:</strong></p>
<pre><code>&lt;translate>
== Culture ==
&#10;Lorem ipsum dolor.
&lt;/translate>
</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Images</strong></td>
<td>Images that do contain language specific content like text should
include the full image syntax in an unit. Other images can only tag the
description with optional hint in message documentation of the page
after it has been marked.</td>
<td><pre><code>&lt;translate>
[[File:Europe.png/en|thumb|right|Map of Europe with capital cities]]
&lt;/translate>
&#10;or
[[File:Europe.png/&lt;translate>en&lt;/translate>|thumb|right|&lt;translate>Map of Europe with capital cities&lt;/translate>]]</code></pre>
<pre><code>[[File:Ball.png|50px|&lt;translate>Ball icon&lt;/translate>]]</code></pre></td>
</tr>
<tr class="even">
<td><strong>Links</strong></td>
<td>Links can be included in the paragraph they are inside. This allows
changing the link label, but also changing the link target to a
localized version if one exists.
<p>Because headers are translated, you cannot rely on the automatically
generated id's for headers. You can add your own anchors. To have them
outside of the translation template you need to break up the page into
multiple translate tag pairs around each header you want to have an
anchor to.</p></td>
<td>
<p><strong>Internal links:</strong></p>
<pre><code>&lt;translate>
Helsinki is capital of [[S:MyLanguage/Finland (country)|Finland]].
&lt;/translate>
&#10;In the helpscreens documentation you are not allowed to use S:MyLanguage/in this case you must use:
&lt;translate>
&#10;Helsinki is capital of [[Finland (country)/en|Finland]].
&lt;/translate>
</code></pre>
<p><strong>External links:</strong></p>
<pre><code>&lt;translate>
PHP ([http://php.net website]) is a programming language.
&lt;/translate></code></pre>
<p><strong>Links within a page:</strong></p>
<pre><code>
&lt;translate>
== Culture ==
&#10;Lorem ipsum dolor.
&#10;...
&#10;For more about food, see [[#culture|section about culture]].
&lt;/translate></code></pre></td>
</tr>
<tr class="odd">
<td><strong>Lists</strong></td>
<td>Lists can get long, so you might want to split them into multiple
parts with, for example, five items or fewer in each as shown here. Do
so only if the items are sufficiently independent to be translate
separately in all languages.
<p>Don't create <em>LEGO</em> messages. For instance, you must avoid
splitting a single sentence into multiple units. Do not separate
logically dependent parts which may affect each other. (With regard to
punctuation or style of the list, for instance.) To split a list, use
-tags. Do not insert new lines; this will break the HTML
output.</p></td>
<td><pre><code>&lt;translate>
* General principles
* Headings
* Images
* Tables
* Categories
&lt;/translate>
&#10;
&lt;translate>
* Links
* Templates
&lt;/translate>
</code></pre></td>
</tr>
<tr class="even">
<td><strong>Numbers</strong></td>
<td>With numbers and other non-linguistic elements you may want to pull
the actual number out of translation and make it a variable. This has
multiple benefits:
<ul>
<li>You can update the number without invalidating translations.</li>
<li>Translation memory can work better when the changing number is
ignored.</li>
</ul></td>
<td><pre><code>&lt;translate>
Income this month &lt;tvar|income>{{FORMATNUM:3567800}}&lt;/&gt; EUR
&lt;/translate></code></pre>
<p>Note that this prevents the translators from localising the number by
doing currency conversion. The `FORMATNUM` call makes sure
the number is formatted correctly in the target language.</p>
</td>
</tr>
<tr class="odd">
<td><strong>Templates</strong></td>
<td>Templates have varying functions and purposes, so the best solution
depends on what the template is for. If the template is not a part of
longer paragraph, it should be left out, unless it has parameters that
need to be translated. If the template has no linguistic content itself,
you don't need to do anything for the template itself.</td>
<td>For an example of templates translated with page translation, see <a
href="https://docs.joomla.org/index.php?title=Template:Extension-Translate&amp;action=edit&amp;redlink=1"
class="new"
title="Template:Extension-Translate (page does not exist)">Template:Extension-Translate</a>.
To use this template, you need to have another template similar to <a
href="https://docs.joomla.org/index.php?title=Template:Translatable_navigation_template&amp;action=edit&amp;redlink=1"
class="new"
title="Template:Translatable navigation template (page does not exist)">Template:Translatable
navigation template</a>, because you cannot include the template by
{{TemplateName}} anymore. This is not <em>yet</em> provided by the
Translate extension itself, but that is in the plans.
<p>Another way is to use the <a
href="https://docs.joomla.org/Help:Extension:Translate/Unstructured_element_translation"
class="new"
title="Special:MyLanguage/Help:Extension:Translate/Unstructured element translation (page does not exist)">unstructured
element translation</a> to translate the template, but then the language
of the template will follow the user's interface language, not the
language of the page he is viewing.</p></td>
</tr>
</tbody>
</table>

## Changing the source text

General principles:

- Avoid changes
- Make the changes as isolated as possible
- Do not add translation unit markers yourself

**Unit markers.** When page is marked for translation, the system will
update the translatable page source and add unique identifiers for each
translation unit. See example below. These markers are crucial for the
system, which uses them to track changes to each translation unit. You
should never add unit markers yourself. The markers are always on the
line before the unit; or, if it starts with a header, after the first
header on the same line. The different placement for headers is needed
to keep section editing working as expected.

```markdown
<translate>
== Birds == <!--T:1-->
Birds are animals which....

<!--T:2-->
Birds can fly and...
</translate>
```

**Changing unit text.** Changing is the most common operation for
translation units. You can fix spelling mistakes, correct grammar or do
other changes to the unit. When re-marking the page for translation, you
will see the difference in the unit text. The same difference is also
shown to translators when they update their translations. For simple
spelling fixes and other cases where you don't want the existing
translations to be removed from translation pages, you can avoid
invalidating them: translators will still see the difference if they
ever update the translation for any reason.

**Adding new text.** You can freely add new text inside translate tags.
Make sure that there is one empty line between adjacent units, so that
the system will see it as a new unit. You can also add translate tags
around the new text, if it is not inside existing translate tags. Again,
do not add unit markers yourself, the system will do it.

**Deleting text.** You can delete whole units. If you do so, also remove
the unit marker.

**Splitting units.** You can split existing units by adding an empty
line in the middle of a unit, or by placing translate tags so that they
split the unit. You can either keep the unit marker with the first unit
or remove it altogether. In the first case, translators see the old text
when updating the old translation. If you removed the unit marker, both
units will behave as if no translation ever existed, after the page is
re-marked for translation.

<table class="wikitable">

<tbody>
<tr class="header">
<th>Original state</th>
<th>Keeping the marker</th>
<th>Removing the marker</th>
</tr>
&#10;<tr class="odd">
<td><pre><code>&lt;!--T:1-->
Cat purrs. Dog barks.</code></pre></td>
<td><pre><code>&lt;!--T:1-->
Cat purrs.
&#10; 
&lt;!--T:2--> (Added after remarking)
Dog barks.</code></pre></td>
<td><pre><code>&lt;!--T:2--> (Added after remarking)
Cat purrs.
&#10; 
&lt;!--T:3--> (Added after remarking)
Dog barks.</code></pre></td>
</tr>
<tr class="even">
<td>Cat purrs. Dog barks.</td>
<td>Cat purrs.
<p>Dog barks.</p></td>
<td>Cat purrs.
<p>Dog barks.</p></td>
</tr>
</tbody>
</table>

**Merging units.** If you merge units, you have to remove at least all
but one unit marker. *(See table below)*

**Moving units.** You can move units around without invalidating
translations: just move the unit marker together with the rest of the
unit. *(See table below)*

<table class="wikitable">

<tbody>
<tr class="header">
<th>Original state</th>
<th>After merging units</th>
<th>After moving units</th>
</tr>
&#10;<tr class="odd">
<td><pre><code>&lt;!--T:1--> (Two distinct units)
Cat purrs.
&#10;
&lt;!--T:2-->
Dog barks.</code></pre></td>
<td><pre><code>&lt;!--T:1--> (Two units merged as one)
Dog barks.
&#10;Cat purrs.</code></pre></td>
<td><pre><code>&lt;!--T:2--> (A unit moved up)
Dog barks.
&#10; 
&lt;!--T:1--> (A unit moved down)
Cat purrs.</code></pre></td>
</tr>
<tr class="even">
<td><p>Cat purrs.</p>
<p>Dog barks.</p></td>
<td><p>Cat purrs.</p>
<p>Dog barks.</p></td>
<td><p>Dog barks.</p>
<p>Cat purrs.</p></td>
</tr>
</tbody>
</table>

Before marking the new version of the page for translation, ensure that
the best practices are followed, especially that translators get a new
translation unit if the content has changed. Also make sure that there
are no unnecessary changes to prevent wasting translators time. If the
source page is getting many changes, it may be worthwhile to wait for it
to stabilize, and push the work for translators only after that.

Unused unit translations are not deleted automatically, but that should
not cause trouble.

## Migrating to page translation

If you have been translating pages before using the page translation
system, you might want to migrate the pages to the new system, at least
the ones you expect to have new translations and want statistics for.
You will probably have existing templates for language switching and
maybe different page naming conventions.

You can start migration by cleaning up, tagging and marking the source
page. You can keep the existing language-switching templates while you
migrate the old translations. If your pages follow the language code
subpages naming convention, they will be replaced with the source text
after marking the source page for translation, but you'll still be able
to access translations from history.

This is manual work, where you have to open the old translation page and
copy and paste translations from there to correct translation units in
the new system using the translation interface. For this you need to
roughly know which part of the translation matches which part of the old
text (and hope they match). You might want to consider marking all the
migrated translations as needing update by prepending the string to the
translations and have a translator look at them. Once migrated, you can
delete the old translation pages if they are not using the same naming
convention (or you could have switched them to it before migration).
Once all pages are migrated you can also remove old language navigation
templates.
