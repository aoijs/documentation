---
description: Adds a title to the embed
---

# $title

This function adds a title to the embed. URL for hyperlink

```text
$title[index;text;url (optional)]
```

```javascript
bot.command({
name: "title",
code: `$title[1;Aoi.js]` //Here 1 is the index
})
```

Here is an example for multiple embeds with different titles

```javascript
bot.command({
name: "multi-title",
code: `
$title[1;Title 1]
$title[2;Title 2]
$title[3;Title 3]
`
})
```
