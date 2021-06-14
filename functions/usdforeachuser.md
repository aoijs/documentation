---
description: Loop over every cached user executing an awaited command
---

# $forEachUser

This function creates a loop for every user 

#### Fields

This function has 1 required field

1. Awaited Command \(Required\)
2. Awaited Command 2 \(Optional\)
3. Etc

Raw Usage: `$forEachUser[awaitedCommand1;awaitedCommand2;...]`

#### Options

* Awaited Command\(s\) - The awaited command\(s\) we're executing

#### Usage

```javascript
bot.command({
name: "forEachUser",
code: "$forEachUser[loop5]"
})

bot.awaitedCommand({
name: "loop5",
code: `$setGlobalUserVar[hello;bye]` //Every users value for 'hello' will be 'bye'

})
```

