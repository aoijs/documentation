---
description: Changes the color of the specified role's ID
---

# $colorRole

This function changes the color of a role

#### Fields

This function has 2 fields

1. Role ID \(Required\)
2. Hex/Int \(Required\)

Raw Usage: `$colorRole[roleID;hex or int color]`

#### Options

* Role ID - The role we're changing the color of
* Hex/Int - The color we're changing the role to

#### Usage

```javascript
bot.command({
name: "crole",
code: `Changed the role's color to #FF0000
$colorRole[$mentionedRoles;FF0000]`
})
```

