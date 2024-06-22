<!-- Filename: Markdown / Display title: Markdown -->

## About Markdown

Markdown is a simpified method of writing text for use in web documents. It
is usually easy to read because it is not littered with html tags. One snag
is that it comes in different versions. The Markdown for Mediwiki is
different from the Markdown for GitHub and the two are not compatible. The
Markdown adopted for Jdocmanual is known as GitHub Flavoured Markdown or
GFM for short.

In use, the simple Markdown text must be passed through a parser to convert
it into HTML. That stage can go wrong, especially if complext tables are
involved. Best solution: avoid tables if possible.

This is a summary of essential GFM syntax. There are more comprehensive
reference sheets available...

***Reminder:*** This is GFM Syntax. MediaWiki syntax is different!

### Headings

Lines beginning with one or pound symbols (#) followed by a space. Six levels
are available but levels 5 and 6 are rarely used. Examples:

```bash
# Heading Level 1
## Heading Level 2
### Heading Level 3
#### Heading Level 4
```
**Warning:** Do not use any Level 1 headings in Jdocmanual. That would lead
to HTML validation failure.

### HTML Comments

The first line of all Jdocmanual articles should contain a html comment
containing a Filename for the original source and a Display title. This
article has this:
```
<!-- Filename: Markdown / Display title: Markdown -->
```
In the case of Help pages, the Filename is used by the Help proxy server
when you select a Help button in any Joomla core administration page.

The original MediaWiki documents do not include a Display title. It is stored
separately. So this is a simple way of keeping the Title and Content together
in Jdocmanual.

### Paragraphs

Blocks of text separated by blank lines. Example:

```bash
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
parturient montes, nascetur ridiculus mus.

Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla
consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec,
vulputate eget, arcu.

In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum
felis eu pede mollis pretium.
```

### Images

In Jdocmanual images may use Markdown format or HTML. The Markdown format must
be like this and all on one line:

<pre><code>&#33;&#91;alt text]&#40;../../../en/images/jdocmanual/heading-what-it-shows.png "Image Title")
</code></pre>

Including the heading in the image filename just saves creating an extra
depth of folders. The filename should say what the image shows in as few words
as possible. It is best to create an image and place it in the correct image
folder before creating the link.

### Links
Any links to Jdocmanual pages, Mediawiki pages and other website pages should
be like these examples:

<pre><code>&#91;Hosting Setup]&#40;jdocmanual?article=user/getting-started/hosting-setup "Hosting Setup")
&#91;Content Editors]&#40;https://docs.joomla.org/Special:MyLanguage/Content_creators#Content_Editors "Anchor in Content creators")
&#91;Joomla]&#40;https://www.joomla.org/ "The main Joomla website")
</code></pre>

The text within square brackets is the link text. The item in quotes is the link title.

The jdocmanual links have the manual, heading and filename (without .md) separated by a slash (/).

**Note:** Images have an initial bang (!). Links don't.

### lists

**Unordered lists** can begin with *, - or +. Sublists are indented with three
spaces. Example:

```bash
* First item
* Second item
    * Sublist item
    * Sublist item
* Third item
```
Result:

* First item
* Second item
    * Sublist item
    * Sublist item
* Third item

**Ordered lists** begin with any number and start with the first number:
```
2.  First item

    With an indented paragraph

    And another one
6.  Second item
    * Unordered sublist item
    * Unordered sublist item
2.  Third item
```
Result, note that the numbers are now in sequence:

2.  First item

    With an indented paragraph

    And another one
6.  Second item
    * Unordered sublist item
    * Unordered sublist item
2.  Third item

### Emphasis

Bold and Italic text items are placed between asterisk or underscore symbols.
Some examples:
```
* This is *Italic*.
* This is **Bold**.
* This is ***Bold Italic***.
* This is *_*Daft___.
* Asterisks and Underscores must **_balance_**.
```
* This is *Italic*.
* This is **Bold**.
* This is ***Bold Italic***.
* This is *_*Daft___.
* Asterisks and Underscores must **_balance_**.

### Code and Syntax Highlighting

Use single backticks to bracket `inline code`.

Use three backticks (```) at the start of a line to bracket a code block.
The opening backticks may be followed by a language name such as php,
javascript, css or html to provide language specific highlighting. There
should be nothing else on the opening line. The closing three backticks
must be on a new line.

```markdown
Use single backticks to bracket `inline code`. Three backticks (```) at the
start of a line to bracket a code block. The closing three backticks must be
on a new line.
```
### Blockquotes

Start any line or sequence of lines with the > symbol to create a block quote.

```
> Mary had a little lamb.<br>
Its fleece was white as snow.
```
> Mary had a little lamb.<br>
Its fleece was white as snow.

### Horizontal Rule

Three or more hyphens, asterisks or underscores on a single line preceded by
a blank line:

---
***
___

## Tips

* Beware multiple spaces at the end of a line as they may cause a line break.
    It is probably best to use the `<br>` HTML tag to create a new line.
* Remember: Links have no ***Bang!***.
* Avoid tables! But if you need them and other layouts not covered here see
this [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#emphasis).
