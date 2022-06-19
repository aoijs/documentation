---
description: 'Check if the User, has Roles or Not.'
---

# $hasRoles

This function checks if the given user has the given roles. Returns boolean

### Usage
```php
$hasRole[guildID;userID;roleID...]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| userID | The id of the user whose roles are to be checked | number | yes |
| role | The roles that are to be checked | number | yes |

## Example

```javascript
bot.command({
name: "role", 
code: `
$hasRoles[$guildID;$authorID;$roleID[Developer];$roleID[Moderator]]`
})
```

