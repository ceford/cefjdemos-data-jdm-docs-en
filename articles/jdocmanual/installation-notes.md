<!-- Filename: Installation_Notes / Display title: Installation Notes -->

## About Jdocmanual

Jdocmanual is designed to deliver Joomla documentation in an easy
reference form with an Index to all articles at the left, the selected
article content in the centre and a list of headings in the article to
the right. It can be used also for other custom documentation.

The data for Jdocmanual are located on GitHub in GitHub Flavoured
Markdown format. Four manuals are available in separate GitHub
repositories. You can choose which to install. Most
of the original content came from the docs.joomla.org MediaWiki
installation and many of the images used here are delivered from that
source.

Version 3 of Jdocmanual is not compatible with previous versions. Any previous
version should be uninstalled before installing this new version.

## Installation In brief
- Install one or more data sets. **They are not Joomla extensions!**
  - **developer:** Information for Joomla developers.<br>
  source: https://github.com/ceford/cefjdemos-data-jdm-developer
  - **docs:** Information for those contributing to Joomla Documentation.<br>
  source: https://github.com/ceford/cefjdemos-data-jdm-docs
  - **help:** The Help screens used for the Administrator pages.<br>
  source: https://github.com/ceford/cefjdemos-data-jdm-help
  - **user:** Information for Joomla users with limited familiarity with
  HTML, CSS and JavaScript.<br>
  source: https://github.com/ceford/cefjdemos-data-jdm-user<br>
- Save a data ZIP file in a folder ending in `/manuals/` outside your web tree.
  Example: `/home/username/data/manuals/`<br>
  An unzipped folder should be renamed to the short name of the manual: one
  of `developer`, `docs`, `help` or `user`. You may then delete the ZIP file.
  Remember the location of your manuals folder!
- Install Jdocmanual on your Joomla site. You can obtain an installable ZIP
  file from: https://github.com/ceford/cefjdemos-com-jdm/archive/refs/heads/main.zip.
  Save it in your Downloads folder and install it in the same way as any
  other Joomla extension.
- Select the Components/Jdocmanual menu item in the Joomla Administrator menu.
  Then select the `Options` button in the Toolbar.
- Set the dataset path and Joomla installation subfolder (if your installation
  is not in your website root). `Save & Close`.
- Build your database articles and menus: select the
  `Jdocmanual/Sources` menu item, then the title of the manual you have
  installed. Use the `Actions` button to `Update HTML`, then `Update Menus`.
  The order is important!
  The Help manual also has an option to `Update Proxy` to build a proxy
  server. Change the Manual's `Status` to `Published`. `Save & Close`.
  Repeat for each manual you wish to use.
- If you wish to use the command line for data maintenance you need to
  install the Jdocmanualcli plugin.
  Source: https://github.com/ceford/j4xdemos-plg-jdocmanualcli

Now select the Jdocmanual/Manuals menu item in the Administrator menu. All
being well you should see Jdocmanual with the default Manual and Article
already selected.

## Help Proxy Server

If you would like to serve your own Help files select the Jdocmanual/Sources
menu item in the Administrator interface and then the title of the Help manual.
Select `Update Proxy` from the `Actions` button in the Toolbar. The process
creates subfolders in a /proxy folder in the root of your Joomla
installation. They contain HTML files generated from the help HTML files
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

- **JDM Author**: allowed to edit content in English and other
languages.
- **JDM Publisher**: allowed to commit and publish
updated content.

The **JDM Author** group should have Public as its parent. The
**JDM Publisher** group should have **JDM Author** as its
parent.

### Users: Viewing Access Levels

**JDM Author** should be set to the Special Viewing Access level.
From the Users / Access Levels page select `Special` and add `JDM
Author` to the User Groups with Viewing Access.

### Global Options

In the Global Options form select the Permissions tab and then the
**JDM Author** item. Set Administrator login to Allowed.

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
