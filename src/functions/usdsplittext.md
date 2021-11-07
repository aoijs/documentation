---
description: Grabs split Text value from $textSplit by given index
---

# $splitText

This function grabs  the value from the given index

```javascript
$splitText[index]
```

{% hint style="info" %}
Index = the position of the text
{% endhint %}

```javascript
bot.command({
name: "splitText",
code: `
$splitText[2] = bye
$splitText[1] = hi
$textSplit[hi/bye;/]`
})
```

