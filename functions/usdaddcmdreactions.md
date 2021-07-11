---
description: Adds reactions to the message that triggered the command.
---

# $addCmdReactions

### Usage
```
$addCmdReactions[emojis]
```

#### Breakdown

* `emojis` - The emojis that the bot should react with. Separate emojis using `;`.

### Example

```javascript
bot.command({
    name: "react",
    code: `$addCmdReactions[🎉;✔]`
});
```
