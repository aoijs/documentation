---
description: Checks if given message exists in the given channel. Returns true/false
---

# $messageExists

This function will check if the indicated message exists on the indicated channel, as result will return true/false depending if it exists or not.

### Usage

```php
$messageExists[messageID;channelID?]
```

### Fields

| Field      | Description                                        | Type   | Required |
| ---------- | -------------------------------------------------- | ------ | -------- |
| message ID | The id of the message to be checked                | number | yes      |
| channel ID | The id of the channel where the message is present | number | no       |

## Examples

```javascript
bot.command({
    name: "exists",
    code: `
    Does the message exist?
    $messageExists[$message]
    `
});

```
