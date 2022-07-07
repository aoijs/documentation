---
description: Unpins a message.
---

# $unPinMessage

This function allows the bot to unpin the given message ID, if it's **pinned**.

### Usage

```php
$unPinMessage[messageID?;channelID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| messageID? | The ID of the message will be unpinned | integer | no |
| channelID? | The ID of the channel | integer | no |

## Example

```javascript
bot.command({
  name: "un-pin-message",
  code: `
  $unPinMessage[790811472829743105;794203850839949372]
  `
// Unpins the given messageID in the given channelID. Giving channel ID, increases findability.
});
```
