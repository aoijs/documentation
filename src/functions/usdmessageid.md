---
description: Returns the user's message ID.
---

# $messageID

This function returns the message ID of the message that the user sent.

### Usage

```php
$messageID
```

## Example
```javascript
bot.command({
  name: "message-id",
  code: `
  Your message ID: $messageID
  `
//Message ID would be from !message-id
});
```
