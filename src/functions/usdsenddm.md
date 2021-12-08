---
description: Sends a dm to the given user ID with the given message
---

# $sendDM

This function sends a dm to the specified user with &lt;message&gt;

```text
$sendMessage[user ID;message]
```

```javascript
bot.command({
name: "sendDM",
code: `$sendDM[message;userID]`
})
```

