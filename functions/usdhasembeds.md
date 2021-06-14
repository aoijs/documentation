---
description: Checks if given message has an embed. Returns true/false
---

# $hasEmbeds

This function checks if the given messageID has an embed or not. Returns boolean

```text
$hasEmbeds[channelID;messageID]
```

```javascript
bot.command({
name: "hasEmbeds",
code: `Has an Embed: $hasEmbeds[773353953269252127;781263421387440168]`
)}
```

