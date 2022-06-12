---
description: Show author's accent color.
---

# $authorAccentColor

`$authorAccentColor` will show author's accent color as hex code (which is on user's banner)

### Usage 

```php
$authorAccentColor[default?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| default | The text to be displayed if accent color is default | string | no |

## Examples

* Without optional fields

```javascript
bot.command({
  name: "author-accent-color",
  code: `
  Your accent color is: $authorAccentColor
  `
//This will return author's accent color.
});
```

* With optional fields

```javascript
bot.command({
  name: "author-accent-color",
  code: `
  Your accent color is: $authorAccentColor[You have default accent color.]
  `
//This will return author's accent color.
});
```

