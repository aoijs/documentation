---
description: 'Returns the ID of mentioned channels, such as $mentioned function.'
---

# $mentionedChannels

This function returns the ID of the mentioned channel

```javascript
$mentionedChannels[arg]
```

```javascript
bot.command({
name: "channel",
code: `$mentionedChannels[1]`
/*
    Arg Numbers
1- Return the first mentioned
2- Return the second mentioned
and so on
*/
})
```



