---
description: Get the Channel Value.
---

# $getChannelVar

This function gets the given variable value for the current or specified channel

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. Channel ID \(Optional\)

Raw Usage: `$getChannelVar[variable;channelID (optional)]`

#### Options

* Variable - The variable value we're getting for the &lt;channel&gt;
* Channel ID - The channel's variable value we're getting

#### Usage

Current Channel's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getChannelVar[variable]`
})
```

Mentioned Channel's Variable Value

```javascript
bot.command({
name: "get", 
code: `
$getChannelVar[variable;$mentionedChannels[1]]`
})
```

