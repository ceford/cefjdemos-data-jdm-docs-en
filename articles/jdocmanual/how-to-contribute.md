<!-- Filename: Help6.x:How_to_Contribute / Display title: How to Contribute -->

## Where to Start

Jdocmanual uses separate repositories for each language in each manual. There
are 25 such repositories at the time of writing. All of the manual and language
combinations must have an English original source. Other languages are regarded
as translations from the originals. The greatest need for help is in correction
of automated translations. For this you do not need to be able to read English,
although that helps.

### Example: Help Pages

Take the Joomla Help pages as an example. There are about 250 pages in use in
Joomla 4 and 5 (soon to be 6 too). Few were fully translated for the original
Help server. However, we can now automatically generate screenshots for all 
Help pages in any supported Joomla language. It takes a few minutes and they 
are waiting in the repositories for someone to create the accompanying text.
There is good news there too. We can create textual content with AI although
that part has not yet been automated. The snag is that we need native speakers
to check and correct AI produced text. That seems to be quite good so there may
be precious little work to do.

### Example: Tutorials

Many of the original Joomla tutorials were translated into many languages but
have become out of date, either the original English versions or their
translations. Also, the method of translation was tedious and impossible to
see the context during translation. With Jdocmanual you could choose a single
tutorial to revise in a simple text editor. The source text is in Markdown
format but you can soon master that. It is much more pleasant to work with
than HTML and a WYSIWYG editor.

### Requirements

You may have to learn new technologies, but the learning curve is shallow
and the skills gained may be useful in other contexts. In brief:

- Install git on your computer for free.
- Install VSCode and/or VSCodium on your computer for free.
- Obtain a GitHub account for free.
- Install a Development Environment on your computer for free. This is actually
  optional for contributing to documentation.
- Install Joomla and Jdocmanual on your computer for free. Again, optional for
  contributing to documentation.

The first three of these steps are outlined in more detail below.

## Install Git

Do whatever it says for your platform:

[Git --fast-version-control](https://git-scm.com/)

You also need to be able to use the terminal application on your platform. Once
git is installed you can test it with a simple command that gives a simple
response, example:
```
git -v
git version 2.39.3 (Apple Git-146)
```

## Install VSCode and/or VSCodium

There is a separate [Jdocmanual article on VSCode](jdocmanual?article=developer/getting-started/visual-studio-code-primer). It takes almost no time at all to install on any
modern platform from the following sources:

- [VSCode](https://code.visualstudio.com/)
- [VSCodium](https://vscodium.com/)

Once installed it is worth spending some time going through the **Walkthoughs**
or the **Learn the Fundamentsls** sequences.

## Dry Run?

If you are unsure whether you want to learn how to contribute you can try a
small test after installing Git and VSCode/VScodium.

- Create a folder tree in your personal file space, cd into the directory and
  issue a git clone command, finally rename the cloned directory to its short 
  two letter language code, as in this sequence:
  ```
  mkdir /home/username/data/manuals/help 
  cd /home/username/data/manuals/help
  git clone https://github.com/ceford/cefjdemos-data-jdm-help-en.git
  mv cefjdemos-data-jdm-help-en en
  ```
- Repeat the last two commands for any other language you would like to use but
  substitute the two letter language code. For example, es instead of en for
  Spanish.

- In your GUI (Windows, Mac or Linux) start your VSCode or VSCodium application
  and use File / Open Folder to open the Help folder. Explore!

If you want to get serious, delete the /home/username/data/manuals/help 
directory, get a GitHub account and clone your own repository forks. 

## Get a GitHub Account

See [Creating an account on GitHub](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github)
and do what it says. Think about your username, it will prefix your repository 
forks. You will need a **Token** as described in [Managing your personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).
*Personal access token (Classic)* or *Fine grained personal access token*? You
will be prompted for a token when you first try to push any changes from a local
repository on your computer to your fork of the repository on GitHub.

## Fork the Help repository in English

Make sure you have an empty directory ready on your local computer waiting for
your GitHub clones:
```
mkdir /home/username/data/manuals/help 
cd /home/username/data/manuals/help
```
- Login to your GitHub account. 
- In the search bar, search for `ceford/cefjdemos-data-jdm-help-en` and switch to
that repo.
- In the Fork dropdown list create a new fork of this repo. It will be created
  in your own account.
- In your own fork, select the green *Code* button and copy the HTTPS link.
- Go back to your own computer and clone the url you copied:
```
git clone https://github.com/your-username/cefjdemos-data-jdm-help-en.git
mv cefjdemos-data-jdm-help-en en
```
## Fork the Help repository in another language

Back to GitHub:

- Search for `ceford/cefjdemos-data-jdm-help-es` and switch to it.
- In the Fork dropdown list create a new fork of this repo.
- In your own fork, select the green *Code* button and copy the HTTPS link.
- Go back to your own computer and clone the url you copied:
```
git clone https://github.com/your-username/cefjdemos-data-jdm-help-es.git
mv cefjdemos-data-jdm-help-es es
```

## Issues

It is really important that we keep track of problems and who is working on
them. This is done by creating an issue in the original repo (not your fork).
For example you may see that a page needs updating or that an AI translation
was not very good and needs fixing. There may be a translation missing
completely. Jdocmanual copes with this by displaying the English page in place
of the missing translation.

### Create or take an issue

If you want to work on a problem go to the GitHub *Issues* page for the 
language you are working on to see whether the problem has already been 
reported (just add */issues* to the repository URL as in this example:
`https://github.com/ceford/cefjdemos-data-jdm-help-en/issues`). If not, create
a new issue with the item subdirectory and filename mentioned in the title.
For example: `banners/banners.md needs grammar corrections`. If an issue
already exists but nobody appears to be working on it and you want to fix it
you can add a comment to that effect.

The issue will be marked as *Closed* when a fix is merged into the repo. Back 
to your local computer to work on the fix.

### Create a branch

On your local computer, change to the repository directory, if you are not 
already there, and create a git branch that might contain the issue number:
```
cd /home/username/data/manuals/help/es
git checkout -b issue36
```
The branch name does not need to have an issue-number but it makes it easier to
remember which branch is fixing which problem.

### Make changes and Preview

If you are fixing an existing file just make the necessary changes in VSCode
or VSCodium. 

Select Ctrl+Shift+V (Windows), Shift+cmd+V (Mac) or Ctrl+K+Enter 
(Linux) to Preview the Markdown text rendered as HTML. Read it through to 
check for spelling and grammar mistakes.

If a file is missing in your selected language you will have to create it, and
possibly its parent folder. 

To create a folder:

- Select the *articles* parent folder (beware the articles parent folder may
  contain an articles folder).
- Right click and select the *New Folder* item from the popup menu. Type in the 
  name of the missing folder. It must be exactly the same as the folder in the
  English repo or it will not be found.

To create a file:

- Right click on the file's parent folder and select the *New File* item. Type
  in the name of the file. Again it must exactly match the English repo original
  or it will never be found.

To create a new translation in a selected language using ChatGPT:

- Register with [ChatGPT](https://chatgpt.com/) and login.
- Open the English version of the missing file, select all of the content
  and copy to the Clipboard.
- In ChatGPT type in `Translate Markdown from English to Spanish:` and add
  a couple of hard returns (Shift + Enter). Paste in the just copied text and
  a normal Enter.
- It takes a couple of minutes for ChatGPT to return the translation. If it
  is in a scrolling code box, when finished use the Copy button at the top
  of the box. If the return is just scrolling text use the Copy button after
  the end of output and be prepared to remove some top lines later.
- Paste the result into the empty new file page.
- Check the first line in the file!

### The First Line

The first line in every file is important! It is a HTML comment line but the
parts of it are used in output construction. It looks like this:

```
<!-- Filename: Help4.x:Articles / Display title: Articles -->
```
For Help files, the `Filename: Help4.x:Articles` part contains the key used by
Joomla to find a Help page. the `Help4.x:` or `Help5.x:`  must be present but
is not used. Otherwise, it must be exactly right or selecting a Help button 
in a Joomla Administrator page will return a 404 Not Found response.

For all files, the `Display title: Articles` contains the title of the item
that appears in menus. The `Display title:` part must not be translated. What
follows it should be translated.

If anything is wrong with the line the translated article will not be present
in the output and the English equivalent will be substituted.

### Test with Jdocmanual

The experts in the Joomla Forums recommend installation of a local development
environment for serious Joomla users. It allows testing of new versions, new
extensions and new designs or ideas before installation on a public server. If
you have such a local test installation now would be a good time to install
your own copy of Jdocmanual. You can get an installable 
[ZIP](https://github.com/ceford/cefjdemos-com-jdm/archive/refs/heads/main.zip)
and install it just like any other Joomla extension. Building the database
tables takes a few minutes on first use but it is much quicker when updating
for just one changed file.

Check your changes in the Administrator Manual view. Occasionally something
goes wrong that is not noticed. Most common are mistyping the filename when
creating a new Markdown file or an error in the first line containing the
HTML comment with the Help link and Display name. That may result in an error
during rebuilding of the database, Jdocmanual delivering a page in English
rather than your translation or an untranslated heading and menu link.

If you don't have a local installation you can skip this step. A reviewer
will check your changes but may miss the same problems.

### Commit

Take a break! Come back and read through the Preview of the article again. If
you are completely satisfied it is time to commit the change and push it to
your fork on GitHub.

In VSCode or VSCodium select the branch icon in the left column. It shows the
count of the number of changed files. When selected, there will be a commit
form for each repository in your manuals folder. Enter a short but descriptive
commit message, such as `New translation for articles/articles.md`

At the right of the Commit button is a dropdown list. Select `Commit & Push`.
You will be prompted to confirm that changes should be staged and then
committed. On first use you will also be prompted to enter your GitHub token
so have it ready.

### Submit your changes for review

If you go to your repository on GitHub, you'll see a  `Compare & pull request`
button. Select that button and submit the pull request.

It will then wait for a Review and, if accepted, merged into the original repo.
There will be a notification email once the changes have been merged.

### What Next

It is usually a best to use one Pull Request per issue rather than fixing
several issues in one PR. Remember that your changes are in a branch of your
local repo named `issue36` in this example. You should now leave that branch
as it is and switch back to the main branch of the repo you have been working
on. You need to go back to your terminal and make sure you are in the correct
repo, and checkout the `main` branch:
```
cd /home/username/data/manuals/help/es
git branch
git checkout -b main
```
You can now make another branch to work on another problem.

When the first branch you committed has been merged you can update your
remote fork and your local clone and then delete the issue36 branch.

### Where to go from here?

You just completed the standard _fork -> clone -> edit -> PR_ workflow often
encountered as a contributor!

This article is based on [Contributing to joomlagerman/joomla](https://github.com/joomlagerman/joomla/blob/5.2-dev/.github/CONTRIBUTING.md?plain=1)


