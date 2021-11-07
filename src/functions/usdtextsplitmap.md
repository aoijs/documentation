---
description: Creates a loop over all the indexes of $textSplit
---

# $textSplitMap

This function creates a loop over all the values in $textSplit

```text
$textSplitMap[awaitedCommand]
```

```javascript
bot.command({
name: "loop",
code: `
$textSplitMap[example]
$textSplit[hi/hello/bye/goodbye;/]
`
})
//TIP: To get the textSplit value itself, use $message[1]

bot.awaitedCommand({
name: "example",
code: `
Value => $message[1]
`
})
```

![](../.gitbook/assets/image%20%2865%29.png)



