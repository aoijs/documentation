---
description: Displays the channel count in the server.
---

# $channelCount

This function will display the total channel count on the server, including categories.

#### Fields

This function has 1 field

1. Type \(Optional\)

Raw Usage: `$channelCount[type (Optional)]` 

#### Options

* Type - the channel type you want to count \(text, voice, category\)

#### Usage

Standard Use

```javascript
bot.command({
    name: "chanels",
    code: `This guild has $channelCount channels!`
});
```

More detailed use

```javascript
bot.command({
    name: "channels",
    code: `There are $channelCount[category] categories
    $channelCount[text] text channels
    $channelCount[voice] voice channels.`
});
```

