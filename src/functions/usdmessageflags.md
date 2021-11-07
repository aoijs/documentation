# $messageFlags

This function returns the flags of the bot's message 

```javascript
bot.command({
name: "test",
code: `Hello
Flags: $messageFlags
`
})
/*
Avalable Flags:
- CROSSPOSTED
- IS_CROSSPOST
- SUPPRESS_EMBEDS
- SOURCE_MESSAGE_DELETED
- URGENT
*/
```

