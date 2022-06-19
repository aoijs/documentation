---
description: Clones the current channel
---

# $cloneChannel

This function allows the bot to clone the name, topic and channel position of the current or given channel.

### Usage 
```php
$cloneChannel[channelID?;return_new_channelID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel that is to be cloned | number | no |
| return ID | Whether to return the id of the channel created|yes/no|no|

## Example

- Without optional field:

```javascript
bot.command({
name: "clonechannel",
code: `I have cloned this channel!
$cloneChannel`
})
```

- With optional field

```javascript
bot.command({
name: "clonechannel",
code: `I have cloned this channel!
$cloneChannel[$mentionedChannels[1]]`
})

```

With optional field to clone current channel, save the new channel's ID inside [$let\[\] ](usdlet.md)and return the ID of the new channel as a channel mention with [$get\[\]](usdget.md):

```javascript
bot.command({
name: "clonechannel",
code: `$channelSendMessage[$get[new];This is the clone!]
$let[channel;$cloneChannel[$channelID;yes]]
`
})
```

