---
description: Show author's accent color.
---

# $authorAccentColor

This function will show author's accent color as hex code (which is on user's banner)

## Field

It has 1 optional field

- Default (Optional)

### Usage 
```php
$authorAccentColor[def?]
```

## Option

- Default - The custom text to be displayed if the author has default accent color.

## Example

```javascript
bot.command({
  name: "author-accent-color",
  code: `
  Your accent color is: $authorAccentColor[You have default accent color.]
  `
//This will return author's accent color.
});
```
