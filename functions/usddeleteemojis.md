---
description: Deletes the specified emoji from the guild
---

# $deleteEmojis

This function deletes an emoji from the current guild

#### Fields

This function has 1 required field

1. Emoji \(Required\)
2. Emoji 2 \(Optional\)
3. Etc

Raw Usage: `$deleteEmoji[emoji1;emoji2;...]`

#### Options

* Emoji\(s\) - The emoji\(s\) you want to delete

#### Usage

```javascript
bot.command({
name: "deleteEmojis",
code: `Deleted emojis $deleteEmojis[bruh;sad_dog]`
})
```

