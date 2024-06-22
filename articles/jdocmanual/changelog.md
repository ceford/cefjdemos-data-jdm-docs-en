<!-- Filename: Changelog / Display title: Changelog -->

## Version 3.0.0

- The data for the four default manuals are now in separate repositories.
- The database tables can be built directly from the Administrator interface.
- Responsive image srcsets are generated for local images.
- It is easy to update content locally with VSCodium or VScode, push changes
  to the remote repo and then rebuild any local installations.
- It is relatively easy to use internal links and images with Markdown code.

## Version 2

For the second version the documents fetched from docs.joomla.org were
converted to GitHub Flavoured Markdown and stored on GitHub. The contents
of four different manuals were in the same repository. That led to memory
and timeout problems when building the database tables. Building a new site
and updating it later was cumbersome.

## Version 1

The first version fetched documents from the docs.joomla.org site and converted
them on demand to HTML suitable for Manual display. It was not reliable,
especially with code conversion.

The version number never actually reached 1.0.0!