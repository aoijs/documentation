---
description: Returns the bots invite
---

# $getBotInvite

This function returns your bots invite

#### Fields

This function has multiple optional fields

1. Permission\(s\) \(Optional\)

Raw Usage: `$getBotInvite[permission1 (optional);permission2 (optional);etc]`

#### Options

* Permissions - The permissions that are given to the bot when joining a server

Find all available permissions [here](../guide/begin/permissions.md)

#### Usage

Without optional fields

```javascript
bot.command({
name: "invite",
code: `Invite: $getBotInvite`
})
```

With optional fields

```javascript
bot.command({
name: "invite",
code: `Invite: $getBotInvite[manageserver;manageroles]`
})
```

