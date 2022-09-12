---
description: Deletes the specified role/roles
---

# $deleteRoles

This function deletes the specified role\(s\)

Fields

This function has 2 required field

1. Guild ID \(Required\)
2. Role ID  \(Required\)
3. Role ID 2 \(optional\)
4. Etc

Raw Usage: `$deleteRoles[guildID;roleID;roleID;etc]`

Options

* Role ID\(s\) - The role\(s\) the bot is deleting

Usage

Deleting the mentioned role

```javascript
bot.command({
name: "deleteRoles",
code: `Deleted a role.
$deleteRoles[$guildID;$mentionedRoles[1]]`
})
```

Deleting multiple mentioned roles

```javascript
bot.command({
name: "deleteRoles",
code: `Deleted a role.
$deleteRoles[$guildID;$mentionedRoles[1];$mentionedRoles[2];$mentionedRoles[3]]`
})
```

