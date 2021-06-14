---
description: Splits a text by separator
---

# $textSplit

This function separates text from the given separator

```javascript
$textSplit[text;separator]
```

```javascript
bot.command({
name: "textSplit",
code: `
$splitText[2] = bye
$splitText[1] = hi
$textSplit[hi/bye;/]`
//Separator would be '/'
})
```

