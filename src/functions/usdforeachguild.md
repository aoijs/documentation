---
description: Loops for every guild the bot is in executing an awaitedCommand
---

# $forEachGuild

This function creates a loop over every server the bot is in

#### Fields

This function has 1 required field

1. Awaited Command \(Required\)
2. Awaited Command 2 \(Optional\)
3. Etc

Raw Usage: `$forEachGuild[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command\(s\) - The awaited command\(s\) we're executing

#### Usage

```javascript
bot.command({
name: "forEachGuild",
code: "$forEachGuild[loop2]"
})

bot.awaitedCommand({
name: "loop2",
code: `$setServerVar[hello;bye]` //Every servers value for 'hello' will be 'bye'
})
```

