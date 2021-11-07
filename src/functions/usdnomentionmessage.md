---
description: Returns user message without any mentions
---

# $noMentionMessage

This function returns the author's message while removing any mentions

```javascript
bot.command({
name: "noMentionMessage",
code: `Your Message: $noMentionMessage`
})
/*
If i say "Hello @kubaturi"
the bot responds with "Hello"

*/
```

