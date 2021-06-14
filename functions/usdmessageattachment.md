---
description: Returns first attachment url of author message (If any)
---

# $messageAttachment

This function returns the url the first attachment the author sends, if they send any

```javascript
bot.command({
name: "getAttachment",
code: `URL of author attachment: $messageAttachment`
})
```

