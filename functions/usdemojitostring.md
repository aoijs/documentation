---
description: Returns the emoji the user reacted with
---

# $emojiToString

The function returns the emoji the user reacted with

#### Usage

```javascript
bot.command({
name: "awaitedReaction",
code: `$awaitReaction[everyone;1m;1️⃣;reactionMessage;An error has occured`
})

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ and the ID is $emojiID`
})
```

