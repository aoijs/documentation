---
description: 'Returns role ID from specified role name, mention or id'
---

# $findRole

This function returns the role ID from the given role info

#### Fields

This function has 1 field

1. Role \(Required\)

Raw Usage: `$findRole[role]`

#### Options

* Role - The role we're finding. You can use name/id/mention

#### Usage

```javascript
bot.command({
name: "role",
code: `$findRole[Developer]`
})
```

