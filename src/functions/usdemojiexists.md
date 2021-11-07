# $emojiExists

This function will return `true` or `false` depending if given emoji ID is an existent emoji \(Registered in one of the bot's servers\) or not.

#### Fields

This function has 1 field

1. Emoji ID \(Required\)

Raw usage: `$emojiExists[emojiID]`

#### Options

* Emoji ID - The ID of the emoji we're checking

#### Usage

```javascript
bot.command({
    name: "emojiexists",
    code: `The emoji with id $message exists?
    $emojiExists[$message]
    `
});
```

