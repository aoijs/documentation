# $serverEmojiExists

This function will return `true` or `false` depending if the provided emoji exists inside of the guild or not.

Raw usage: `$serverEmojiExists[ID]`

Example:

```javascript
bot.command({
    name: "emojiexists",
    code: `The emoji with id $message exists inside this server?
    $serverEmojiExists[$message]
    `
});
```

