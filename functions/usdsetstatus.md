# $setStatus

This function sets the bot's status

```text
$setStatus[text;type;status]
```

> ⚠ Types: "PLAYING", "LISTENING", "WATCHING", "STREAMING", "COMPETING"

> ⚠ STATUS: "dnd", "idle", "online", "invisible"

```javascript
bot.command({
name: "setStatus",
code: `$setStatus[music;LISTENING;dnd] Successfully changed the bot's status <3`
})
```

