---
description: Set a cooldown for a command
---

# $cooldown

This function sets a cooldown to the current command

#### Fields

This function has 2 fields

1. Time \(Required\)
2. Error \(Required\)

Raw Usage: `$cooldown[time;error]`

#### Options

* Time - The time of the cooldown
* Error - The message when the cooldown is in affect
* %time% - You can add this into the error message to show the remaining time left

#### Usage

```javascript
bot.command({
name: "hello", 
code: `
$description[Hello!]
$cooldown[1m;Hey, you need to wait %time%!]
`
})
```

