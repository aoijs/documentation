---
description: >-
  An event that gets executed, if the bot sees an invite deletion on a server.
  To let the bot listen to the event, add one bot.onInviteDelete() callback
  inside your mainfile.
---

# bot.onInviteDelete

This callback allows the bot to log every time an invite is deleted

Here are the functions you can use in this callback:

* [$inviteUses ](../functions/usdinviteuses.md)
* [$inviteURL ](../functions/usdinviteurl.md)
* [$inviteCode](../functions/usdinvitecode.md) 
* [$inviteGuildID](../functions/usdinviteguildid.md)
* [$inviteChannelID ](../functions/usdinvitechannelid.md)
* [$inviteUserID ](../functions/usdinviteuserid.md)
* [$inviteMaxUses](../functions/usdinvitemaxuses.md)

#### Usage:

```javascript
bot.inviteDeleteCommand({ // command
    channel: 'channel id', //channel where it logs
    code: `your code`, //code sent to <channel>
})
```

#### Example Command:

```javascript
bot.inviteDeleteCommand({ 
channel: '772414449839636490', 
code: `Invite Info:
Creator: $inviteUserID
URL: $inviteURL
Uses: $inviteUses
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
type: 'inviteDeleteCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `
Invite was deleted:
Creator: $inviteUserID
URL: $inviteURL
Uses: $inviteUses
Channel ID: $inviteChannelID
`,
type: 'inviteDeleteCommand'
})
```
