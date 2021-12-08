---
Description: Adds a title to the embed
---

# $title

- This function adds a title to the embed. URL for hyperlink
- Index allows you to use multiple embeds. 1 by default

### Usage
`$title[index;text;url (optional)]`

```javascript
bot.command({
name: "title",
code: `$title[1;aoi.js is Cool]`
})
```

### With URL
```javascript
bot.command({
name: "title",
code: `$title[1;aoi.js is Cool;https://npmjs.com/package/aoi.js]`
})
```
