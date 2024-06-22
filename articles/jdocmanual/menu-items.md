<!-- Filename: Menu_Items / Display title: Menu Items -->

## New Menu Item

To create a new menu item for a new article you need to select the
`Menu Stashes` list and select the Manual you are working on. The stash is a
list of headings and articles. The list controls which articles appear and
in which order. You just need to enter a code line for the new item. The
code lines look like this:

```
; Source for menu build - heading and item order.
; heading=heading=English Heading
; manual=heading=filename

heading=jdocmanual=Jdocmanual
docs=jdocmanual=introduction-to-jdocmanual.md
docs=jdocmanual=source-data.md
docs=jdocmanual=article-edit.md
docs=jdocmanual=article-new.md
```
Note that the `Preview` tab shows the menu. The menu itself does not work!

When you are satisfied, enter an explanatory `Commit Message`` in the `Comments``
tab and then `Commit` the changes.

The changes will be committed and the Menu updated. You will now be able to
view your new article in the Manual view.

## Menu Item Order

The order of menu items is set by the order of lines seen in the stash. To
change the order just cut and paste a line into a new position.