---
description: Loop over every guild channel in the guild executing an awaited command
---

# $forEachGuildChannel

This function creates a loop for every channel in the current guild
#### Usage

```
$forEachGuildChannel[time;{awaitedData};awaitedCommand;awaitedCommand2;...]
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
name: "forEachGuildChannel",
code: `$forEachGuildChannel[1s;{"channel":"bye"};loop1]`
})
bot.awaitedCommand({
name: "loop1",
code: `$setChannelVar[hello;$awaitData[channel]]`
})
//Every channel in the current guild value for 'hello' will be 'bye'
```
