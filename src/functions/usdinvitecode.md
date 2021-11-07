# $inviteCode

This function returns the code of the newly created/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Code: $inviteCode
    `, //returns eR5v8KMP2s
})
bot.onInviteCreate()
```



