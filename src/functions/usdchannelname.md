---
description: >-
  Retrieves the Channel Name by Channel ID, if no channel is specified it will
  return the name of the channel where the command was executed.
---

# $channelName

This function allows you to obtain the name of a specific channel indicated by its channel ID, if neither a channel ID is given, the function will return as a product the name of the channel in which the command was executed

### Usage
```php
$channelName[channelID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel whose name is to be returned | number | no |

## Example

```javascript
bot.command({
    name: "name",
    code: `$channelName[$mentionedChannels[1;yes]]`
});
```



