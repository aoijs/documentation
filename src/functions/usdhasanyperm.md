---
description: Checks if the user has at least one of the required perms
---

# $hasAnyPerm

This function will check if the user has at least one of the specified perms inside of the function. Returns boolean.

### Usage
```php
$hasAnyPerm[guildID;userID;perm1;perm2?...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| user ID | The id of the user whose perms are to be checked | number | yes |
| perm1 | The permission that is to be checked | string | yes |
| perm2 | The permission that is to be checked | string | no |

## Example

```javascript
bot.command({
    name: "hasperms",
    code: `
$hasAnyPerm[$guildID;$authorID;addreactions;sendmessages;manageserver]
    `
})
```
#### Footnotes

The bot will reply with `true` if the user has at least one of the 3 perms we requested, in this case `addreactions, sendmessages` or `manageserver`.

