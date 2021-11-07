---
description: Unpins a message
---

# $unPinMessage

This function allows the bot to unpin the given messageID \(if pinned\)

```javascript
$unPinMessage[channelID;messageID]
```

Using the function

```javascript
bot.command({
name: "unpin",
code: `$unPinMessage[790811472829743105;794203850839949372]`
}) //Unpins the given messageID
```

