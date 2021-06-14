---
description: Deletes the specified role/roles
---

# $deleteRoles

This function deletes the specified role\(s\)

Fields

This function has 1 required field

1. Role ID \(Required\)
2. Role ID 2 \(Optional\)
3. Etc

Raw Usage: `$deleteRoles[roleID;roleID;etc]`

Options

* Role ID\(s\) - The role\(s\) the bot is deleting

Usage

Deleting the mentioned role

```javascript
bot.command({
name: "deleteRoles",
code: `Deleted a role.
$deleteRoles[$mentionedRoles[1]]`
})
```

Deleting multiple mentioned roles

```javascript
bot.command({
name: "deleteRoles",
code: `Deleted a role.
$deleteRoles[$mentionedRoles[1];$mentionedRoles[2];$mentionedRoles[3]]`
})
```

