---
description: >-
  Gives the Channel ID of the Channel Name. Will return current in if no channel
  name given
---

# $channelID

This channel returns the current channel or the specified channel's ID

#### Fields

This function has 1 field

1. channel Name \(Optional\)

Raw Usage: `$channelID[channel Name]`

#### Options

* Channel Name - The channel name we're getting the channel id from

#### Usage

```javascript
bot.command({
name: "channelID", 
code: `$channelID[$message]` //Gets the channel ID via message
})

bot.command({
name: "channelID", 
code: `$channelID` //Gets the channel ID where the comamnd was ran in
})
```



