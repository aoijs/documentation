---
description: >-
  An event that gets executed, if the bot sees an invite creation on a server.
  To let the bot listen to the event, add one bot.onInviteCreate() callback
  inside your mainfile.
---

# bot.onInviteCreate

This callback allows the bot to log every time an invite is created for the current server

Heres all the functions you can use in this callback:

* [$inviteURL ](../functions/usdinviteurl.md)
* [$inviteCode ](../functions/usdinvitecode.md)
* [$inviteGuildID ](../functions/usdinviteguildid.md)
* [$inviteChannelID ](../functions/usdinvitechannelid.md)
* [$inviteUserID ](../functions/usdinviteuserid.md)
* [$inviteMaxUses](../functions/usdinvitemaxuses.md)

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

#### Command Handler Usage:
For people who use `bot.loadCommands()` handler.
```javascript
module.exports = ({
channel: "ID",
code: `
code here
`,
type: 'inviteCreateCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `
Invite was created:
Creator: $inviteUserID
URL: $inviteURL
Channel ID: $inviteChannelID
`,
type: 'inviteCreateCommand'
})
```
