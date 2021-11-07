---
description: Modifies a channel's permissions to the given perms
---

# $modifyChannelPerms

This function edit's the specified channels perms

```text
$modifyChannelPerms[channelID;perm1;perm2;perm3;roleID/userID/$guildID]
```

```javascript
/*
TIP:
+ = Allow perms
- = Deny Perms
/ = Defaults the perm
*/
bot.command({
name: "modifyChannelPerms",
code: `Modified the channel permissions!
$modifyChannelPerms[773365032691040277;+sendmessages;-readmessages;/managemessages;$guildID]`
})
/*
This:
Allows send messages
Denies read messages
Defaults manage messages
for the whole guild
*/
```

