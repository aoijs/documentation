---
description: Adds a reaction to the given message ID.
---

# $addMessageReactions

This function will add a reaction to the specified message ID.

### Usage

```php
$addMessageReactions[channelID;messageID;emoji;emoji?;...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel of which message is situated in | number | yes |
| messageID | The message of which the reaction(s) will get react | string | yes |
| emoji | The emojis of which will be reactee to the given messageID | emoji | yes |

## Example

```javascript
bot.command({
  name: "add-message-reactions",
  code: `
  $addMessageReactions[$channelID;$messageID;🌸]
  
  Here's a pretty flower!
  `
});
```

