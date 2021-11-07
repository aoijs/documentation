---
description: Loops for every cached guild member executing awaited commands
---

# $forEachMember

This function creates a loop for every user thats' in the current guild

#### Fields

This function has 1 required field

1. Awaited Command \(Required\)
2. Awaited Command 2 \(Optional\)
3. Etc

Raw Usage: `$forEachMember[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command\(s\) - The awaited command\(s\) we're executing

#### Usage

```javascript
bot.command({
name: "forEachMember",
code: "$forEachMember[loop4]"
})

bot.awaitedCommand({
name: "loop4",
code: `$setUserVar[hello;bye]` //Every user in the current guild value for 'hello' will be 'bye'

})
```

