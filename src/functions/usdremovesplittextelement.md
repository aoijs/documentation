---
description: Removes a value from $textSplit by using the given indexes
---

# $removeSplitTextElement

This function removes the value of the given indexes

```text
$removeSplitTextElement[index1;index2;...]
```

```javascript
bot.command({
name: "removeSplitTextElement",
code: `$removeSplitTextElement[1;2]
$textSplit[hi/bye/hello;/]
`
})
// Removes hi and bye from the list of values in $textSplit completely

```

