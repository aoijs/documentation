---
description: Returns the emoji name the user reacted with
---

# $emojiName

This function returns the emoji name the user reacted with

#### Usage

```javascript
bot.command({
name: "awaitedReaction",
code: `$awaitReaction[everyone;1m;1️⃣;reactionMessage;An error has occured`
})

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ and the ID is $emojiName`
//$emojiName would return 'one'
})
```

