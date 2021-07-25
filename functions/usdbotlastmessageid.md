# $botLastMessageID

This function will return the ID of the last message send by the bot.

## Usage

```javascript
bot.command({
    name: "id",
    code: `
Message ID is: $loop[1;cmd]
    `
})

bot.awaitedCommand({
name: "cmd",
code: `$botLastMessageID`
})
```

