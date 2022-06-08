---
description: Show author's accent color.
---

# $authorAccentColor

This function will show author's accent color as hex code (which is on user's banner)

### Usage 

```php
$authorAccentColor[custom text]
```

## Example

```javascript
bot.command({
  name: "author-accent-color",
  code: `
  Your accent color is: $authorAccentColor
  `
//This will return author's accent color.
});
```

