<!-- Filename: JDOC:Translating_Links / Display title: Translating Links -->

## Introduction

Linking translated pages together is an important part of page
navigation for our users. It is a quick way to send a user to another
page for more information on relevant topics. Translating these links
must be done a specific way to keep a user in their language of choice.
If a person is browsing our documentation in their language, they would
probably prefer to stay in their language if possible. Providing a link
to a page in its English form will work, however, the user must click
the link to their language to read it in their language.

## Link Translation

Translating page links must be done a certain way to send the reader to
another page in the same language. English writers can help by following
this format too. It makes it easier on the translators when they start
translating pages if the correct link for localisation is already used.

In a normal links `[[Component]]` a user is taken to the
[Component](https://docs.joomla.org/Component "Special:MyLanguage/Component")
page when they click the link. If there is a translated version of the
page, for example, French, the French page would be located at
`[[Component/fr]]`.

So what if the page for **Component/fr** has not been created yet? The
user would see a 'red-link' (page doesn't exist) compared to a blue link
(the page exists). Perhaps the page Component will be translated, but it
has not been translated yet. This is why **Special:MyLanguage/** should
always be used as a prefix to the linked page.

    [[Component]] should be written as [[S:MyLanguage/Component|Component]]
     or
    [[Component]] should be written as [[Special:MyLanguage/Component|Component]]

## How "Special:MyLanguage" Works in Links

What does **Special:MyLanguage/** do? It does a few things when
processing a clicked link on a page before sending the user to the page.
Using the page **Component** as an example:

- Gets the language the page is being viewed in.
- Checks if the link for Component exists in French, by adding /fr to
  it.
  - Yes, Component/fr exists and user is sent to the page version in
    French;
  - No, Component/fr does not exist and user is sent to the default
    source language version;

## Links in Help Pages

In Help pages the Special:MyLanguage part of a link is removed. You can
test that by opening this page as a normal document or a help document
and comparing the sources of the links:

- Normal: <a
  href="https://docs.joomla.orghttps://docs.joomla.org/JDOC:Translating_Links"
  class="external free" target="_blank"
  rel="noreferrer noopener">https://docs.joomla.orghttps://docs.joomla.org/JDOC:Translating_Links</a>
- Help: <a
  href="https://help.joomla.org/proxy?keyref=JDOC:Translating_Links&amp;lang=en"
  class="external free" target="_blank"
  rel="noreferrer noopener">https://help.joomla.org/proxy?keyref=JDOC:Translating_Links&amp;lang=en</a>

If you invoke the Help page version you will see that the
Special:MyLanguage/ part has disappeared from the first link above. This
has implications for links within Help pages.

To link to another internal wiki document from a Help page the page
language suffix must be included in the source like this:

    [[Special:MyLanguage/JDOC:Translating_Links/en|Translating Links]]

That gives a translator the option to translate just the text of the
link or both the language and the text. The language is best left as
“en” until the translator is ready to translate the linked page. If the
link text is changed before a translation has been created there will be
no link in the Help page, just the link text, and the translated source
page will have red text giving anyone the option to create the page in
the normal way. It is better for the translator to go to the source page
and select the “Translate this page” link. For similar reasons, authors
should avoid the use of {{#translation:}} to insert the language code of
the current translation.

## Link Format Precedence

If both Special:MyLanguage and the language suffix (/en) are including
in a link then Special:MyLanguage takes precedence. You can confirm that
by trying the following links:

- Special only: <a
  href="https://docs.joomla.orghttps://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions"
  class="external free" target="_blank"
  rel="noreferrer noopener">https://docs.joomla.orghttps://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions</a> -
  Result in English (unless Dutch is your default)
- Both: <a
  href="https://docs.joomla.orghttps://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions/nl"
  class="external free" target="_blank"
  rel="noreferrer noopener">https://docs.joomla.orghttps://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions/nl</a> -
  Result in English (unless Dutch is your default)
- Suffix only: <a
  href="https://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions/nl"
  class="external free" target="_blank"
  rel="noreferrer noopener">https://docs.joomla.org/Chunk4x:Add_Banners_Category_Permissions/nl</a> -
  Result in Dutch

## Usage

### Translators

A setting in documentation has made it easier with an short alias to
"Special:" in links. You may use "S:" instead of "Special:" in a link,
`[[S:MyLanguage/...]]`.

Regular page links

    [[Component]] should be written as [[S:MyLanguage/Component|<{translate this only}>]]
     or
    [[Component]] should be written as [[Special:MyLanguage/Component|<{translate this only}>]]

Namespaced page links

    [[JDOC:Translating Links]] should be written as [[S:MyLanguage/JDOC:Translating Links|<{translate this only}>]]
     or
    [[JDOC:Translating Links]] should be written as [[Special:MyLanguage/JDOC:Translating Links|<{translate this only}>]]

Category page links:

    [[:Category:Glossary_definitions]] should be written as [[S:MyLanguage/:Category:Glossary_definitions|<{translate this only}>]]
     or
    [[:Category:Glossary_definitions]] should be written as [[Special:MyLanguage/:Category:Glossary_definitions|<{translate this only}>]]

### English Page Writers and Editors

All the above in the Translators section applies to English version page
writers and copy editors. You can help with translations by creating
page links in English version pages using **Special:MyLanguage/** or
**S:MyLanguage/** too! A page doesn't need to be marked for translation
or even in the process of being translated. As pages are added to the
translation queue, translators will have an easier time translating the
links on a page.
