---
description: 'Retrieves, split length.'
---

# $getTextSplitLength

This function returns the amount of values in $textSplit

```javascript
bot.command({
name: "text", 
code: `
$getTextSplitLength 
$textSplit[hi1/hi2/hi3;/]`
//Bot would return: 3
})
```

{% hint style="warning" %}
Text Split functions may be hard to understand. Click [here](https://ptb.discordapp.com/channels/773352845738115102/784626845059383316/786996112098590720) to view
{% endhint %}

