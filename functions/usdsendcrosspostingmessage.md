# $sendCrosspostingMessage

This function allows the bot to send 1 message to multiple channels

```text
$sendCrosspostingMessage[message;channelID;channelID;...]
```

```javascript
bot.command({
name: "send", 
code: `$sendCrosspostingMessage[Hello everyone;782007668831027201;773853536797851708]` 
})
```

