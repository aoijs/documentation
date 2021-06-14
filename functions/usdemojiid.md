---
description: Returns the emoji ID of the emoji the user reacted to
---

# $emojiID

Returns the ID of the emoji the user reacted to

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

