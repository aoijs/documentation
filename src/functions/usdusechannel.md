---
description: Sends message to specified channel.
---

# $useChannel

This function sends a message to the given channel ID.

### Usage 

```php
$useChannel[channelID]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The ID of the channel | number | yes |

## Example

```javascript
bot.command({
  name: "use-channel",
  code: `
  Hi!
  
  $useChannel[773363417338609674]
  ` 
//Sends 'Hi!' in the given channel
});
```
