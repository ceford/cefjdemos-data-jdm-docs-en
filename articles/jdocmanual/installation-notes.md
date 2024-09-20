<!-- Filename: Installation_Notes / Display title: Installation Notes -->

## About Jdocmanual

Jdocmanual is designed to deliver Joomla documentation in an easy
reference form with an Index to all articles at the left, the selected
article content in the centre and a list of headings in the article to
the right. It can be used also for other custom documentation.

Version 4 of Jdocmanual is not compatible with previous versions. Any previous
version should be uninstalled before installing this new version.

## Data Sets

The data sets for Jdocmanual are located on GitHub in GitHub Flavoured
Markdown format. Four manuals are available, some in several languages, in
separate GitHub repositories. For example, the source data for the User
Manual in English is https://github.com/ceford/cefjdemos-data-jdm-user-en
You can choose which manual and data sets to install in addition to English,
which is mandatory.

Most of the original content came from the docs.joomla.org MediaWiki
installation and many of the images used here are delivered from that
source.

## Installation In brief

There are full instructions in the [Jdocmanual Repository README](https://github.com/ceford/cefjdemos-com-jdm) file. This brief outline covers installation of the User
Manual in English and German using the git clone method. If you do not have git
you can download the files from the repositories in ZIP format and unpack them.

1. Create a file structure on your platform that is outside your web tree but
   writable by your web server. For example, for the User manual:<br>
   `/home/username/data/manuals/user/`<br>
   The `/manuals/user/` part of the path is mandatory.
2. Change into this directory and clone the Markdown files:<br>
    `git clone https://github.com/ceford/cefjdemos-data-jdm-user-en.git`<br>
    `git clone https://github.com/ceford/cefjdemos-data-jdm-user-de.git`
3.  Rename the created directories to the language names:<br>
    `mv cefjdemos-data-jdm-user-en en`<br>
    `mv cefjdemos-data-jdm-user-de de`
4.  Install Jdocmanual on your Joomla site. You can obtain an installable ZIP
    file from: https://github.com/ceford/cefjdemos-com-jdm/archive/refs/heads/main.zip.
    Save it in your Downloads folder and install it in the same way as any
    other Joomla extension.
5.  Install the Command Line Plugin obtainable is a ZIP file:<br>
    `https://github.com/ceford/cefjdemos-plg-jdocmanualcli/archive/refs/heads/main.zip`
6.  Select the Components/Jdocmanual menu item in the Joomla Administrator menu.
    Then select the `Options` button in the Toolbar.
    - Set the dataset path and Joomla installation subfolder (if your installation
      is not in your website root). `Save & Close`.
7.  Build your database articles and menus:
    - select the `Jdocmanual/Sources` menu item, then the title of the manual
      you have installed. Use the `Actions` button to `Update HTML`, then
      `Update Menus`. The order is important! The articles build process takes
      4 to 6 minutes on a fast workstation or server!
    - Repeat for each manual you wish to use.
8.  If you prefer to use the command line for data maintenance use the
    following commands in sequence:<br>
    ```
    cd /path/to/joomla/web/root/cli
    php joomla.php jdocmanual:action buildarticles user en
    php joomla.php jdocmanual:action buildmenus user en
    php joomla.php jdocmanual:action buildarticles user de
    php joomla.php jdocmanual:action buildmenus user de
    ```
Now select the Jdocmanual/Manuals menu item in the Administrator menu. All
being well you should see Jdocmanual with the default Manual and Article
already selected.

## Help Proxy Server

The proxy server is used in conjunction with the Help Manual to deliver the
help pages seen on selection of any Toolbar Help button:

```
   mkdir /home/username/data/manuals/help
   cd /home/username/data/manuals/help
   git clone https://github.com/ceford/cefjdemos-data-jdm-help-en.git
   mv cefjdemos-data-jdm-help-en en
   cd /path/to/joomla/web/root/cli
   php joomla.php jdocmanual:action buildarticles help en
   php joomla.php jdocmanual:action buildmenus help en
   php joomla.php jdocmanual:action buildproxy help en
```
There is an `Update Proxy` option in the Toolbar `Actions` list for the
Jdocmanual: Edit Source page for the Help Manual.

The build process creates subfolders in a /proxy folder in the root of the
Joomla installation. They contain HTML files generated from the help HTML files
stored in the database.

Then edit your configuration.php file to remove the domain of the
existing Help server. You first need to change its file permissions to 644. It
might look like this:

`public $helpurl = '/xxx?/proxy?keyref=Help{major}{minor}:{keyref}&lang={langcode}'; `

The /xxx? part would be the name of any subfolder where your installation is
located in public_html, or absent if your Joomla installation is in the root of
your site.

Test by selecting the Help button in any **core** Joomla page.

## Site Menu

If you want to show the Manuals on the site just create a Jdocmanual
menu item. Note the single page is for search results but it has not
been implemented.

**Important:** The menu alias must be **jdocmanual** or internal links
will be broken and lead to frontend problems.

You may wish to place the menu on a page without side modules so that
the full width of the page may be used for content.

## User Groups

If you wish to allow others to help maintain content you need to create
two User Groups:

- **JDM Author** Allowed to edit content in English and other languages.
- **JDM Publisher** Allowed to commit and publish updated content.

The **JDM Author** group should have Public as its parent. The
**JDM Publisher** group should have **JDM Author** as its
parent.

### Users: Viewing Access Levels

**JDM Author** should be set to the Special Viewing Access level.
From the Users / Access Levels page select `Special` and add `JDM
Author` to the User Groups with Viewing Access.

### Global Options

In the Global Options form select the Permissions tab and then the
**JDM Author** item. Set Administrator login to *Allowed*.

### Jdocmanual Options

From the Jdocmanual, Manual page select the Options button. In the
Permissions list select **JDM Author** and set the following to
Allowed: - Access Administration Interface - Create - Delete - Edit

Select **JDM Publisher** and set the following to Allowed: - Publish

Save and Close

If you now login as a user in the **JDM Author** group you will see
the Home Dashboard with some modules not relevant for Jdocmanual.

### Turn off the Help menu item

Go to the list of Administrator modules and find the Administrator Menu
module. In the Module tab set the Help Menu item to Hide.

### Unpublish or restrict Access to modules

In the Administrator modules list find the Logged-in Users item used in
the cpanel position (not the cpanel-users position). Either Unpublish it
or set Access to Super Users.

Find and unpublish the Popular Articles and Recently Added Articles
items for the cpanel position (not the cpanel-content position).

There may be other modules needing similar treatment.

The Home Dashboard should now be empty for a **JDM Author**.

## Who can do what?

**JDM Author** and **JDM Publisher** can login but should only
have access to the the Home Dashboard and the Jdocmanual component.

**JDM Author** does not have access to the Commit button in the
Article Edit page toolbar so cannot update the git repository or
displayed page. Otherwise each can use all other features.

**Manager** and **Administrator** can login but will not see the
Jdocmanual component.

**Author**, **Editor** and **Publisher** do not have access
to the Administrator interface.

**Super Users** have complete access.
