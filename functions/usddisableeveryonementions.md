---
description: Disables all mentions with @everyone Role.
---

# $disableEveryoneMentions

This function sends @everyone mentions from a message without pinging the users. @everyone will be shown as the string but without a ping.

```javascript
bot.command({
name: "say", 
code: `$message
$disableEveryoneMentions` 
})
```

