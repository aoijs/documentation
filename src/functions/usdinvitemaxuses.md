# $inviteMaxUses

This function returns the max uses of the newly created/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Max Uses: $inviteMaxUses
    `, //returns 25 
})
bot.onInviteCreate()
```

