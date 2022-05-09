---
Description: Show author's accent color.
---
<hr>

# $authorAccentColor

This function will show author's accent color as hex code (which is on user's banner)

### Usage 
```js
$authorAccentColor[custom text]
```

## Example
```js
bot.command({
  name: "author-accent-color",
  code: `
  Your accent color is: $authorAccentColor
  `
//This will return author's accent color.
});
```
