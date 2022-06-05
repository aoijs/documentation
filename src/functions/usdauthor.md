---
description: Sets the author in an embed message and authorIcon if it's specified.
---

# $author

This function allows you to add an 'author' to the embed message and an icon to the author if a URL is specified. 

### Usage

```php
$author[index;text;icon url?;redirecting url?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The author embed's index | number | yes |
| text | The text will show up on the author property | string | yes |
| icon url? | The icon will show up next to author property | url | no |
| redirecting url? | The URL of the redirect link | url | no |

###### Footnote
*The icon url must end with `.png`, `.jpg` or `.gif`!*

## Examples

Without hyperlink and icon:

```javascript
bot.command({
  name: "author",
  code: `
  $author[1;$username]
  `
//Returns the user's username
});
```

With hyperlink and icon:

```javascript
bot.command({
  name: "author",
  code: `
  $author[1;$username;$authorAvatar;https://aoi.js.org]
  `
//Returns user's username along with their icon and if clicked, will redirect to aoi.js' website
});
```

