# bot.onInviteCreate

This callback allows the bot to log every time an invite is created for the current server

#### Usage:

```javascript
bot.inviteCreateCommand({ // command
channel: 'channel id', //channel where it logs
code: `your code` //code sent to <channel>
})
```

#### Example Command:

```javascript
bot.inviteCreateCommand({
channel: '772414449839636490',
code: `
Invite was created:
Creator: $inviteUserID
URL: $inviteURL
Channel ID: $inviteChannelID
`
})
```

Heres all the functions you can use in this callback:

* [$inviteURL ](functions/usdinviteurl.md)
* [$inviteCode ](functions/usdinvitecode.md)
* [$inviteGuildID ](functions/usdinviteguildid.md)
* [$inviteChannelID ](functions/usdinvitechannelid.md)
* [$inviteUserID ](functions/usdinviteuserid.md)
* [$inviteMaxUses](functions/usdinvitemaxuses.md)

