---
description: Loops for every guild the bot is in executing an awaitedCommand
---

# $forEachGuild

This function creates a loop over every server the bot is in
#### Usage

```
$forEachGuild[time;{awaitedData};awaitedCommand;awaitedCommand2;...]
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

### Examples

```javascript
bot.command({
name: "forEachGuild",
code: `$forEachGuild[1s;{"message":"bye"};loop1]`
})
bot.awaitedCommand({
name: "loop1",
code: `$setServerVar[hello;$awaitData[message]]`
})
//Every servers value for 'hello' will be 'bye'
```
