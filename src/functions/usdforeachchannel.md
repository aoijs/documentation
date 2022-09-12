---
description: Loop over every channel this bot can see executing awaited commands.
---

# $forEachChannel

This function creates a loop over ALL channels the bot has access to

#### Usage

```
$forEachChannel[time;{awaitedData};awaitedCommand;awaitedCommand2;...]
```

#### Fields

This function has 2 required field

| Field | Description | Required |
| :--- | :--- | :--- |
| Time | The amount of time to execute the awaited command | Yes |
| Awaited Data | The data you want to change | Yes |
| Awaited Command | The awaited command\(s\) we're executing | Yes |


#### Options

* Time - The amount of time to execute the awaited command
* Awaited Data - The data you want to change
* Awaited Command\(s\) - The awaited command\(s\) we're executing

## Examples

```javascript
bot.command({
name: "forEachChannel",
code: `$forEachChannel[1s;{"message":"bye"};loop1]`
})
bot.awaitedCommand({
name: "loop1",
code: `$setChannelVar[hello;$awaitData[message]]`
})
//Every channels value for 'hello' will be 'bye'
```
