---
description: Adds a reaction to the message who triggered the command.
---

# $addCmdReactions

This function will be in charge of adding the 'emojis' previously chosen in the message of the person who has activated the command.

#### Fields

This function has 1 required field

1. Emoji \(Required\)
2. Emoji 2 \(Optional\)
3. Emoji 3 \(Optional\)
4. Etc

Raw Usage: `$addCmdReactions[emoji1;emoji2;emoji3;...]`

#### Options

* Emoji\(s\) - The emoji that is being reacted

#### Usage

```javascript
bot.command({
    name: "react",
    code: `$addCmdReactions[✔]`
});
```

Multiple Reactions

```javascript
bot.command({
    name: "react",
    code: `$addCmdReactions[🎉;✔]`
});
```

