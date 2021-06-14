---
description: Displays the bot as typing
---

# $botTyping

This function just displays the bot as 'Typing'

#### Fields

This function has 1 optional field

1. time \(Optional\)

Raw Usage: `$botTyping[time (Optional)]`

#### Options

* Time - Set how long the bot is typing for

#### Usage

```javascript
bot.command({
name: "bot",
code: `I was just typing
$botTyping`
})
```

![Heres what it would look like. Of course it would be your bots name](../.gitbook/assets/image%20%2848%29.png)

You can also specify the amount of time you want it to type for.

Example:

```javascript
bot.command({
    name: "bot",
    code: `
Haha I made you think i was typing something important
    $botTyping[20s]
    `
})
```

