---
description: 'Returns, True or False, if the assigned Author ID, has it.'
---

# $hasPerms

This function checks if the given user has the given permission. Returns boolean.

### Usage
```php
$hasPerms[guildID;userID;perms...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| user ID | The id of the user whose perms are to be checked | number | yes |
| perm| The permission that is to be checked | string | yes |

## Example

```javascript
bot.command({
name: "check", 
code: `
$hasPerms[$guildID;$authorID;admin]`
/*
This will check if the author has the permission 'Administrator'
*/
})
```

