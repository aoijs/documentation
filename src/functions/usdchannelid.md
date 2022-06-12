---
description: >-
  Gives the Channel ID of the Channel Name. Will return current in if no channel
  name given
---

# $channelID

This channel returns the current channel or the specified channel's ID

### Usage 
```php
$channelID[channel name?]
```

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel name | The name of the channel | string | no |

## Examples

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



