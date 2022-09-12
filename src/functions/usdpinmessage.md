---
description: Pins a message
---

# $pinMessage



This function allows the bot to pin its own message or the given message

```javascript
$pinMessage[messageID (optional);channelID (optional)]
```

Using the function 

```javascript
bot.command({
name: "pin".
code: `Rules: 
1. Be nice
2. No advertising
$pinMessage`
}) //This pins the bot's message

bot.command({
name: "pin",
code: `$pinMessage[1018720477218361364;101556083474485251] I pinned a mesage!`
}) //Pins the given messageID
```

