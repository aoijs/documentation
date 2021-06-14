---
description: Delete a channel or channels by using their IDs.
---

# $deleteChannels

This function deletes the specified channel\(s\)

#### Fields

This function has 1 required field

1. Channel ID \(Required\)
2. Channel ID 2 \(Optional\)
3. Etc

Raw Usage: `deleteChannels[channel id;channel id;etc]`

#### Options

* Channel ID\(s\) - The channels the bot is deleting

#### Usage

Deleting the mentioned channel

```javascript
bot.command({
name: "deletechannels", 
code: `
I've deleted the mentioned channels!
$deleteChannels[$mentionedChannels[1]]
` 
})
```

Deleting multiple mentioned channels

```javascript
bot.command({
name: "deletechannels", 
code: `
I've deleted all the mentioned channels!
$deleteChannels[$mentionedChannels[1];$mentionedChannels[2];$mentionedChannels[3]]
` 
})
```

