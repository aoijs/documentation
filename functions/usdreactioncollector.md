---
description: Creates a reaction collector for given message ID
---

# $reactionCollector

This function creates a reaction collector for the given message ID

```text
$reactionCollector[messageID;userFilter($authorID/@everyone);time;reaction1,reaction2,...;command1,command2,...;removeReactions (yes/no)]
```

```javascript
bot.awaitedCommand({
  name: "awaitReaction1",
  code: `
  $editMessage[$message[1];
Leref is cool]`})


bot.command({
  name: "help",
  code: `
$reactionCollector[$splitText[1];$authorID;1h;😋;awaitReaction1;yes]
$textSplit[$sendMessage[Reaction with 😋 to get a cool message;yes]; ]`})
```

