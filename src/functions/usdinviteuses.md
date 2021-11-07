# $inviteUses

This function returns the uses of the newly deleted invite. Only works in bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteDeleteCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Uses: $inviteUSes
    `, //returns 5 
})
bot.onInviteDelete()
```

