---
description: Add reactions to the message the bot has send in the command.
---

# $addReactions

This function will be in charge of adding the 'emojis' previously chosen in the message sent by the bot once triggered the command.

#### Fields

This function has 1 required field

1. Emoji \(Required\)
2. Emoji 2 \(Optional\)
3. Emoji 3 \(Optional\)
4. Etc

Raw Usage: `$addReactions[emoji;emoji2;emoji3;...]`

#### Options

* Emoji - The emoji of which will be reacted to

#### Usage

Singular Reaction

```javascript
bot.command({
    name: "react",
    code: `
    $addReactions[🌸]
    Hi, take a flower
    `
});

```

Multiple Reactions

```javascript
bot.command({
    name: "question",
    code: `
    $addReactions[✔;❌]
    Does someone reads this?
    `
});
```

