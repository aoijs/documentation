---
description: Returns the user's message ID
---

# $messageID

This function returns the message ID of the message that triggered the command

```javascript
bot.command({
name: "messageID",
code: `Your message ID: $messageID`
//Message ID would be from !messageID
})
```

