---
description: Loop over every cached user executing an awaited command
---

# $forEachUser

This function creates a loop for every user 

#### Usage

```
$forEachUser[time;{awaitedData};awaitedCommand;awaitedCommand2;...]
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

#### Examples

```javascript
bot.command({
name: "forEachUser",
code: `$forEachUser[1s;{"nickname":"$authorID"};loop1]`
})

bot.awaitedCommand({
name: "loop1",
code: `$nickname[$awaitData[nickname]]`
})

//This will return user nickname
```

