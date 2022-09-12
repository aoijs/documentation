---
description: Loops for every cached guild member executing awaited commands
---

# $forEachMember

This function creates a loop for every user thats' in the current guild

#### Usage

```
$forEachMember[time;{awaitedData};awaitedCommand;awaitedCommand2;...]
```

#### Fields

This function has 2 required field

| Field | Description | Required |
| :--- | :--- | :--- |
| Time | The amount of time to execute the awaited command | Yes |
| Awaited Data | The data you want to change | Yes |
| Awaited Command | The awaited command\(s\) we're executing | Yes |

## Examples

```javascript
bot.command({
name: "forEachMember",
code: `$forEachMember[1s;{"message":"1"};loop1]`
})

bot.awaitedCommand({
name: "loop1",
code: `$setGlobalUserVar[message;$awaitData[message]]`
})

//This will set every guild member message var to 1
```
