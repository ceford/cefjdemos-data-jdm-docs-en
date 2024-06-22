<!-- Filename: Crowdin / Display title: Crowdin -->

## What is Crowdin?

<a href="https://joomla.crowdin.com" class="external text"
target="_blank" rel="nofollow noreferrer noopener">Crowdin</a> is a
cloud-based solution that streamlines localization (L10N) management for
software projects.

The Joomla CMS official language packs and many other aspects of the
project are managed using Crowdin to facilitate managing L10N
activities.

## What can be translated on Crowdin?

### Joomla! Official Translations

There's a variety of content that needs to be translated and localised
for use with Joomla. Joomla's using Crowdin Enterprise for managing
localisations across the project. A number of leading extension
developers are also using Crowdin as their localisation tool, and you
can see those extensions also listed under Joomla's Crowdin project page
as related projects.

- Joomla! CMS - Core Language packs for Joomla 4
- Joomla! Official Extensions - Extensions created by the Joomla!
  Project such as JEDChecker, Patch Tester, Language Pack component and
  Install From Web Extension
- Joomla! Official Website - Materials for the joomla.org suite of
  websites
- Joomla! Official Website Template - Language strings for the
  Joomla.org website template
- Joomla! Marketing Resources - Internationalising marketing resources
  to promote Joomla around the globe

### Translating Documentation

Joomla Documentation doesn't use Crowdin for translation as it's built
into the wiki. See the [Documentation Translation Quickstart
guide](https://docs.joomla.org/JDOC:Page_Translation_Quickstart_Guide "Special:MyLanguage/JDOC:Page Translation Quickstart Guide")
for more information.

### 3rd Party Extension Translations

A variety of 3rd party extension developers have also chosen Crowdin as
their L10N solution. These are displayed on Joomla's Crowdin, but are
managed by the individual developers.

## Getting Started

### Create an account

To start using Crowdin, create an account at
<a href="https://joomla.crowdin.com" class="external free"
target="_blank"
rel="nofollow noreferrer noopener">https://joomla.crowdin.com</a>. If
you're already using GitHub to contribute to the project, you can use
your GitHub login (along with a few other OAuth options) to sign up to
Crowdin.

Once you've created your account,
<a href="https://joomla.crowdin.com/" class="external text"
target="_blank" rel="nofollow noreferrer noopener">visit the Crowdin
Project for Joomla</a> to contribute to Joomla 4 core translations,
other translations for Joomla websites, Joomla marketing projects and
other Joomla extensions.

*<a href="https://crowdin.com/project/joomla-cms" class="external text"
target="_blank" rel="nofollow noreferrer noopener">Joomla 3
translations</a> are also managed on Crowdin, but are outside Joomla's
Crowdin Enterprise structure. The setup works the same in regards to
contributing translations, however the proofreading and language pack
process is different to the steps described for Joomla 4 in the next
section.*

### Select a Project

Once logged into joomla.crowdin.com you'll see the project dashboard,
showing all of the projects that are available to translate. Click on a
project to then see what the status of each localisation is for that
project. <img
src="https://docs.joomla.org/images/f/ff/Languages-crowdinfeaturedprojects.png"
decoding="async" data-file-width="800" data-file-height="416"
width="800" height="416"
alt="Select a Featured Project to begin translating that project in your language" />

### Select a Language

When you go into a project, you'll see all of the available languages
ready for translation. To start translating, hover on the language and
then click on the "Translate" button that appears.

The progress bars indicate two main aspects of the translation process:

- Blue lines indicate the percentage of strings for this project that
  have been translated for that language. Once translated, proofreaders
  then process the suggested translations and approve them - it's a
  double check in case something has been suggested by accident for that
  language. An example I've found as a proofreader has been that some
  translations have been suggested for the wrong language as the
  translator was not in the correct language when they started
  suggesting phrases. And there are always different opinions on how to
  translate a sentence.
- Green lines indicate that the proofreader has approved the suggested
  translations made by translators for that localisation. Once the
  proofreader approves the translations, the approved translations then
  move into the production phase, where the project's translation
  managers can then package up the translations for the project and
  create packages that can then be installed by users or implemented by
  Joomla's webmasters team on the various Joomla website properties.

<img src="https://docs.joomla.org/images/0/02/Language_List.png"
decoding="async" data-file-width="800" data-file-height="467"
width="800" height="467"
alt="Select your language from the list to begin translating." />

### Start Translating

When you click translate, you'll be taken to the Crowdsourcing language
page.
<img src="https://docs.joomla.org/images/7/78/Crowdsourcing_Screen.png"
decoding="async" data-file-width="800" data-file-height="379"
width="800" height="379"
alt="Parts of the Crowdsourcing screen you see when translating the page." />

1.  On the left is a list of all the strings from the language files for
    the project that need translating. You can filter the list for
    various parameters, but by default the list will show you all of the
    strings available, with the untranslated strings at the top of the
    list (indicated by the red icon before them. Once translated, the
    icon is green).
2.  Clicking on a string you will see it load in the Source String box.
    This is the full text that you need to translate. You will see at
    times various highlighted items, like the green highlighted %s in
    the screenshot below. When you see some of the source string
    highlighted, these parts of the string do not need to be translated
    as they perform a system function that will do a replacement in the
    code with a variable as an example. The highlighted peace can also
    be HTML.
3.  In this area, type your translation for the source string.
4.  You may sometimes see suggestions for some strings in this section.
    If one is suitable, you can click on it to select it as a suitable
    translation for the source string.
5.  If you find there's an issue with a previously suggested
    translation, or have questions about the source string's context
    that you want to clarify, leave a comment in the comments sidebar on
    the page. Translation managers will then be notified and will either
    provide clarification or resolve the issue with the source string if
    required.
6.  Once you are happy with your translation for the source string,
    click Save and the system will mark that string as Done and move on
    to the next untranslated string.

Once you've finished translating all the available strings (or as many
as you have time for in the session) you can exit the editor and return
to the project by going to the menu at the top right of the screen and
select "Quit Editor".

When you've begun providing crowdsourcing translations in each of
Joomla's featured projects, you'll be notified when new strings are
available to translate that have been added to the various projects.

## Proofreading

Before translations appear in Joomla as part of an updated language
pack, they need to be approved by that language's proofreader(s). The
role of a proofreader is to:

- Check that the crowdsourcing translations are correct for that
  language
- Resolve issues where multiple translations are suggested, choosing the
  most suitable translation
- For core language packs, package up the completed language pack to
  upload it to Joomla Language Download system.

To become a proofreader, join the [Joomla Translation Program
Team](#Joomla_Translation_Program_Team). For more information on the
processes proofreaders need to complete with making language packs,
please see [Crowdin for
Proofreaders](https://docs.joomla.org/JDOC:Crowdin_for_Proofreaders "Special:MyLanguage/JDOC:Crowdin for Proofreaders").

## Joomla Translation Program Team

The purpose of the <a
href="https://volunteers.joomla.org/teams/joomla-translation-program-team"
class="external text" target="_blank" rel="noreferrer noopener">Joomla
Translation Program</a> within the Programs Department is to coordinate
and supervise the work of hundreds of volunteers globally who translate
the Joomla CMS, Joomla’s official websites, documentation, and marketing
materials into many different languages. If you would like to do more
than just translate your language's strings, join the team to assist
with managing and recruiting translators and proofreaders. For more
information on participating in the Joomla Translation Program join the
<a
href="https://volunteers.joomla.org/teams/joomla-translation-program-team"
class="external text" target="_blank" rel="noreferrer noopener">Joomla
Translation Program Team</a> or find out more information on JDocs <a
href="https://docs.joomla.orghttps://docs.joomla.org/Joomla_Translation_Program"
class="external text" target="_blank" rel="noreferrer noopener">Joomla
Translation Program</a> page.

The also has a range of documentation articles that translators can
contribute to.

## Further Information

- Crowdin have a comprehensive
  <a href="https://support.crowdin.com/" class="external text"
  target="_blank" rel="nofollow noreferrer noopener">Knowledge Base</a>
  which new users would be well served to familiarize themselves with.
- Some of the basic concepts about using Crowdin to translate Joomla are
  explained in more detail in the <a
  href="https://magazine.joomla.org/all-issues/august/joomla-s-l10n-hearted"
  class="external text" target="_blank" rel="noreferrer noopener">Joomla's
  L10N-hearted</a> article from August 2021 in
  <a href="https://magazine.joomla.org" class="external text"
  target="_blank" rel="noreferrer noopener">Joomla Community Magazine</a>.
