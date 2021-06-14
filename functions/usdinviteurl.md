# $inviteURL

This function returns the url of the newly created/deleted invite. Only works in bot.onInviteCreate\(\) and bot.onInviteDelete\(\) and $fetchInvites

```javascript
bot.inviteCreateCommand({
    channel: '772414449839636490', 
    code: `Invite Info:
  URL: $inviteURL
    `, //returns https://discord.gg/eR5v8KMP2s
})
bot.onInviteCreate()
```

