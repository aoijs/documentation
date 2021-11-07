# $inviteUserID

This function returns the userID of the person who created the newly made/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Creator: $inviteUserID
    `, //returns 535566311942651924
})
bot.onInviteCreate()
```

