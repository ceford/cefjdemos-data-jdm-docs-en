<!-- Display title: New Article in Jdocmanual -->

## Creating a New Article

The stash for a new article has some differences from that for an existing article.
The `Display Title` field is not set and some related read only fields are not set
either. They are set when the `Display Title` is changed. Also, the `Heading` field
is not set and you have the option to choose from the list of existing headings
or you may enter a new heading. The heading must consist of lower case
alphanumeric words separated by dashes. You will also notice that the
`Page ID` is 0 (zero) as the page does not exist.

![new article form](../../../en/images/jdocmanual/article-new.png "New Article Form")

The `Stash` tab contains an empty edit field as there was no original content
with which to initialise it. However, an initial `Display title` entry is made
from the entry in the Details tab. Example:

```markdown
<!-- Display title: Article Edit -->
```
It is possible to change the Display Title and related fields at any time
until the new article is committed.

## Committing the New Article

**Notes:**
- Always save the Stash content before selecting `Pull Request`.
- Stash content must end with a new line.

When the New Article is committed a new entry will be created for it in the
jdm_articles database table. An entry is made also in articles-index.txt so
that the article can be included when the database is built initially. However,
the new entry is appended to the list of articles rather than the logical
place at the end of a list of headings.

The article will disappear from the New Articles list and appear in the
Articles list.

## Create a Menu Item

After creating a new article you need to create a new menu item for it. Just
follow the procedure described under menu Items. You will need to use the
heading and filename used when creating the new article.
