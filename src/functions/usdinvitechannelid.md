# $inviteChannelID

This function returns the channel origin of the newly created/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  Channel: $inviteChannelID
    `, //Returns 773357157394939924
})
bot.onInviteCreate()
```

