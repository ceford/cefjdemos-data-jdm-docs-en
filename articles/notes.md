<!--
{
  "source": "",
  "title": "Notes",
  "description": "Some temporary notes", 
  "author": ""
}
-->

## Setup Sequence

### Create a child template

...

### Create a Custom Module

- Title: Site Name
- Title: Hide
- Position: below-top
- Content:
```html
<div class="navbar-brand">
<div class="site-logo"><a href="jdocmanual">Jdocmanual Local</a></div>
<div class="site-description">A site for Joomla! documentation</div>
</div>
```
- Advanced / Module Class: flex-grow-1
- Module Style: noCard

### Create a Search Form

- Title: Search Form
- Title: Hide
- Position: below-top
- Search Field Label: Hide
- Advanced / Module Style: noCard

## Search / Replace Metadata

The first try omitted the final \s* - so check on next batch replace:
```
<!-- Filename:\s*(.*?)\s*\/.*Display title:\s*(.*)\s*-->
```
Replacement:
```
<!--
{
  "source": "https://docs.joomla.org/$1",
  "title": "$2",
  "description": "", 
  "author": ""
}
-->
```
