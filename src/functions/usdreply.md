---
description: Replies to given message ID.
---

# $reply

This function allows your bot reply to given message ID with mentioned, or not.

### Usage

```php
$reply[messageID?;mentionUser?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| messageID? | integer | The ID of the message | 
| mentionUser? | string | The parameter for mentioning user or not |

## Example

```javascript
bot.command({
  name: "reply",
  code: `
  $reply[$messageID;yes]
  
  Hello 👋🏻
  `
  // Replies the message.
});
```
