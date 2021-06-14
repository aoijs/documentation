---
description: Loop over every guild channel in the guild executing an awaited command
---

# $forEachGuildChannel

This function creates a loop for every channel in the current guild

#### Fields

This function has 1 required field

1. Awaited Command \(Required\)
2. Awaited Command 2 \(Optional\)
3. Etc

Raw Usage: `$forEachGuildChannel[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command\(s\) - The awaited command\(s\) we're executing

#### Usage

```javascript
bot.command({
name: "forEachGuildChannel",
code: "$forEachGuildChannel[loop3]"
})

bot.awaitedCommand({
name: "loop3",
code: `$setChannelVar[hello;bye]` //Every channel in the current guild value for 'hello' will be 'bye'
})
```

