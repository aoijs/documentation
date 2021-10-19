# $splitText

This function grabs  the value from the given index

```javascript
$splitText[index]
```

> ℹ️ Index = the position of the text

```javascript
bot.command({
name: "splitText",
code: `
$splitText[2] = bye
$splitText[1] = hi
$textSplit[hi/bye;/]`
})
```

