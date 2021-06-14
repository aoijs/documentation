---
description: >-
  Retrieves the Channel Name by Channel ID, if no channel is specified it will
  return the name of the channel where the command was executed.
---

# $channelName

With this function you will be able to obtain the name of a specific channel indicated by its channel ID, if neither a channel ID is given, the function will return as a product the name of the channel in which the command was executed

#### Usage

This function has 1 field

1. Channel ID \(Optional\)

Raw Usage: `$channelName[channelID (optional)]`

#### Options

* Channel ID - The channel id of where we're getting the channel name from

#### Usage

```javascript
bot.command({
    name: "name",
    code: `$channelName[$mentionedChannels[1;yes]]`
});
```



