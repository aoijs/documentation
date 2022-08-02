---
description: >-
  An event that gets executed, if the bot sees an invite deletion on a server.
  To let the bot listen to the event, add one bot.onInviteDelete() callback
  inside your mainfile.
---

# bot.onInviteDelete

This callback allows the bot to log every time an invite is deleted

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

Here are the functions you can use in this callback:

* [$inviteUses](broken-reference)
* [$inviteURL](broken-reference)
* [$inviteCode](broken-reference)
* [$inviteGuildID](broken-reference)
* [$inviteChannelID](broken-reference)
* [$inviteUserID](broken-reference)
* [$inviteMaxUses](broken-reference)
