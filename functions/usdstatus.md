# $status

```javascript
$status[userID (optional)]
```

> ❗ Must enable discord presence intents

```javascript
bot.command({
name: "status",
code: `Your Status: $status`
})
```

> ℹ️ Bot Returns Either: dnd, online, invisible, idle

