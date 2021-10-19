# $unban

This function unbans the user from the guild

```text
$unban[user ID;reason (optional)]
```

> ℹ️ Reason will show up in audit logs

```javascript
bot.command({
name: "unban",
code: `Unbanned the user with the ID of 535566311942651924
$unban[535566311942651924]`
})
```

