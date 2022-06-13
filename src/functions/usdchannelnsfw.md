---
description: >-
  Returns True or False, if the channel is NSFW. Will return for current channel
  if no id is given
---

# $channelNSFW

With this function you can show some information about the channel you want, this specific function will return true or false depending on whether the channel is marked as NSFW.

### Usage 
```php
$channelNSFW[channelID?]
```

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel | number | no |

## Examples

```javascript
bot.command({
    name: "NSFW",
    code: `
    Is the channel <#$mentionedChannels[1;yes]> NSFW?
    $channelNSFW[$mentionedChannels[1;yes]]
    `
});
```

