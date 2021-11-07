---
description: Loop over every channel this bot can see executing awaited commands.
---

# $forEachChannel

This function creates a loop over ALL channels the bot has access to

#### Fields

This function has 1 required field

1. Awaited Command \(Required\)
2. Awaited Command 2 \(Optional\)
3. Etc

Raw Usage: `$forEachChannel[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command\(s\) - The awaited command\(s\) we're executing

#### Usage

```javascript
bot.command({
name: "forEachChannel",
code: "$forEachChannel[loop1]"
})

bot.awaitedCommand({
name: "loop1",
code: `$setChannelVar[hello;bye]` //Every channels value for 'hello' will be 'bye'
})
```

