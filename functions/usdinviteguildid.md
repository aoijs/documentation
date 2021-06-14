# $inviteGuildID

This function returns the server origin of the newly created/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Guild: $inviteGuildID
    `, //Returns DBD.js Server 
})
bot.onInviteCreate()
```

